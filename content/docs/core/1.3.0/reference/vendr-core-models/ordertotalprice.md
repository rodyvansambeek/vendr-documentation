---
title: OrderTotalPrice
description: API reference for OrderTotalPrice in Vendr, the eCommerce solution for Umbraco v8+
---
## OrderTotalPrice

```csharp
public class OrderTotalPrice : OrderSubtotalPrice
```

**Inheritance**

* class [OrderSubtotalPrice](../ordersubtotalprice/)

**Namespace**
* [Vendr.Core.Models](../)

### Properties

#### GiftCardsAmount

```csharp
public Amount GiftCardsAmount { get; set; }
```


---

#### WithDiscounts

```csharp
public Price WithDiscounts { get; set; }
```


### Methods

#### ZeroValue

```csharp
public static OrderTotalPrice ZeroValue(Guid currencyId)
```


---

#### AsReadOnly

```csharp
public virtual ReadOnlyOrderTotalPrice AsReadOnly()
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
