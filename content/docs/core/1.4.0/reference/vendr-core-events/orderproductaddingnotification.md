---
title: OrderProductAddingNotification
description: API reference for OrderProductAddingNotification in Vendr, the eCommerce solution for Umbraco v8+
---
## OrderProductAddingNotification

```csharp
public class OrderProductAddingNotification : OrderProductAddNotificationBase<Order>
```

**Inheritance**

* class [OrderProductAddNotificationBase&lt;TEntity&gt;](../orderproductaddnotificationbase-1/)

**Namespace**
* [Vendr.Core.Events.Notification](../)

### Constructors

#### OrderProductAddingNotification

```csharp
public OrderProductAddingNotification(Order order, string productReference, decimal qty, 
    IDictionary<string, string> properties, string bundleId, string parentBundleId)
```


<!-- DO NOT EDIT: generated by xmldocmd for Vendr.Core.dll -->