---
title: ValidatePaymentMethodPriceChange
description: API reference for ValidatePaymentMethodPriceChange in Vendr, the eCommerce solution for Umbraco v8+
---
## ValidatePaymentMethodPriceChange

```csharp
public class ValidatePaymentMethodPriceChange : ValidationEventBase
```

**Inheritance**

* class [ValidationEventBase](../validationeventbase/)

**Namespace**
* [Vendr.Core.Events.Validation](../)

### Constructors

#### ValidatePaymentMethodPriceChange

```csharp
public ValidatePaymentMethodPriceChange(PaymentMethodReadOnly paymentMethod, Guid currencyId, 
    ChangingValue<decimal> price, Guid? countryId, Guid? regionId)
```


### Properties

#### CountryId

```csharp
public Guid? CountryId { get; }
```


---

#### CurrencyId

```csharp
public Guid CurrencyId { get; }
```


---

#### PaymentMethod

```csharp
public PaymentMethodReadOnly PaymentMethod { get; }
```


---

#### Price

```csharp
public ChangingValue<decimal> Price { get; }
```


---

#### RegionId

```csharp
public Guid? RegionId { get; }
```


<!-- DO NOT EDIT: generated by xmldocmd for Vendr.Core.dll -->
