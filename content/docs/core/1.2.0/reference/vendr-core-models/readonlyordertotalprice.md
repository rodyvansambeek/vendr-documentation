---
title: ReadOnlyOrderTotalPrice
description: API reference for ReadOnlyOrderTotalPrice in Vendr, the eCommerce solution for Umbraco v8+
---
## ReadOnlyOrderTotalPrice

```csharp
public class ReadOnlyOrderTotalPrice : ReadOnlyTotalPriceWithPreviousDiscount
```

**Inheritance**

* class [ReadOnlyTotalPriceWithPreviousDiscount](../readonlytotalpricewithpreviousdiscount/)

**Namespace**
* [Vendr.Core.Models](../)

### Properties

#### GiftCardsAmount

```csharp
public Amount GiftCardsAmount { get; }
```


---

#### WithDiscounts

```csharp
public Price WithDiscounts { get; }
```


### Methods

#### ZeroValue

```csharp
public static ReadOnlyOrderTotalPrice ZeroValue(Guid currencyId)
```


---

#### DeepClone

```csharp
public override object DeepClone()
```


---

#### GetHashCode

```csharp
public override int GetHashCode()
```


<!-- DO NOT EDIT: generated by xmldocmd for Vendr.Core.dll -->
