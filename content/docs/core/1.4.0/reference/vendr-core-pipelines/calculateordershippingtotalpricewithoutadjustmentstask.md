---
title: CalculateOrderShippingTotalPriceWithoutAdjustmentsTask
description: API reference for CalculateOrderShippingTotalPriceWithoutAdjustmentsTask in Vendr, the eCommerce solution for Umbraco v8+
---
## CalculateOrderShippingTotalPriceWithoutAdjustmentsTask

```csharp
public class CalculateOrderShippingTotalPriceWithoutAdjustmentsTask : 
    PipelineTaskWithTypedArgsBase<OrderCalculationPipelineArgs, OrderCalculation>
```

**Inheritance**

* class [PipelineTaskWithTypedArgsBase&lt;TArgs,T&gt;](../pipelinetaskwithtypedargsbase-2/)

**Namespace**
* [Vendr.Core.Pipelines.Order.Tasks](../)

### Constructors

#### CalculateOrderShippingTotalPriceWithoutAdjustmentsTask

```csharp
public CalculateOrderShippingTotalPriceWithoutAdjustmentsTask(
    IShippingCalculator shippingCalculator)
```


### Methods

#### Execute

```csharp
public override PipelineResult<OrderCalculation> Execute(OrderCalculationPipelineArgs args)
```


<!-- DO NOT EDIT: generated by xmldocmd for Vendr.Core.dll -->