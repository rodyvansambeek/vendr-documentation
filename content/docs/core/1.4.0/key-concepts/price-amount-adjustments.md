---
title: Price/Amount Adjustments
description: Adjusting prices in Vendr, the eCommerce solution for Umbraco v8+
---

Quite often in a solution you may want to tweak the figures of an order, be that reducing the price of a product if a customer purchases a given amount of a product, or maybe specific customers incur an additional fee. To handle this, Vendr has the concept of Price/Amount Adjustments. What adjustments allow you to do is create a record/log of any changes that occur to a price/amount throughout the calculation process. Vendr then uses these adjustments in the calculation process to work out it's final pricing, and also provides this list of all the adjustments on the order for easy reference reference, making it clear exactly how the price was calculated.

Vendr has two types of adjustments:

* **Price Adjustment** - Adjusts one of the orders price properties (ie. discounts, fees).
* **Amount Adjustment** - Adjusts the final transaction amount of an order (ie. gift cards, loyalty points).

## Creating Custom Adjustments

Adjustments are applied using a `IPriceAdjuster` or `IAmountAdjuster` with developers able to create their own adjusters to apply custom adjustments.

````csharp
public class MyPriceAdjuster : PriceAdjusterBase
{
    public override void ApplyPriceAdjustments(PriceAdjusterArgs args)
    {
        // TODO: Calculate adjustment
        args.SubtotalPriceAdjustments.Add(new MyAdjustment());
    }
}
````

Adjusters apply adjustments to their given price they wish to affect. Adjustments are strongly typed and so each adjuster should defined their own adjustment type, providing properties to collect any relevant information for the adjustment (this "meta data" gets serialized with the adjustment as is constantly available when accessing the given adjustment).  

````csharp
public class MyAdjustment : PriceAdjustment<DiscountAdjustment>
{
    public string MyAdjustmentRef { get; set; }

    public MyAdjustment (string name, string ref)
        : base(name)
    {
        MyAdjustmentRef = ref;
    }
}
````

Adjustments inherit from either `PriceAdjustment<TSelf>` or `AmountAdjustment<TSelf>` depending on the type of adjustment being applied. Both base classes follow a similar structure, the difference being whether the adjustment value is a `Price` or `Amount`.

````csharp
public abstract class PriceAdjustment<TSelf> 
{
    public Type Type { get; }
    public string Name { get; }
    public Price Price { get; }
    public Price OriginalPrice { get; }
}
````

Once defined, the adjuster should be registered with the DI container to enable Vendr to be aware of it and include it in it's calculation process.


````csharp
[ComposeAfter(typeof(VendrWebComposer))]
public class MyComposer : IUserComposer
{
    public void Compose(Composition composition)
    {
        composition.WithPriceAdjusters()
            .Append<MyPriceAdjuster>();
    }
}
