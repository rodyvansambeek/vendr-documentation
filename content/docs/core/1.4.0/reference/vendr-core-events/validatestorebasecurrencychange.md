---
title: ValidateStoreBaseCurrencyChange
description: API reference for ValidateStoreBaseCurrencyChange in Vendr, the eCommerce solution for Umbraco v8+
---
## ValidateStoreBaseCurrencyChange

```csharp
public class ValidateStoreBaseCurrencyChange : ValidationEventBase
```

**Inheritance**

* class [ValidationEventBase](../validationeventbase/)

**Namespace**
* [Vendr.Core.Events.Validation](../)

### Constructors

#### ValidateStoreBaseCurrencyChange

```csharp
public ValidateStoreBaseCurrencyChange(StoreReadOnly store, ChangingValue<Guid?> currencyId)
```


### Properties

#### CurrencyId

```csharp
public ChangingValue<Guid?> CurrencyId { get; }
```


---

#### Store

```csharp
public StoreReadOnly Store { get; }
```


<!-- DO NOT EDIT: generated by xmldocmd for Vendr.Core.dll -->
