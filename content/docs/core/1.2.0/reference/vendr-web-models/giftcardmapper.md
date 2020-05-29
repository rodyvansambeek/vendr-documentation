---
title: GiftCardMapper
description: API reference for GiftCardMapper in Vendr, the eCommerce solution for Umbraco v8+
---
## GiftCardMapper

```csharp
public static class GiftCardMapper
```

**Namespace**
* [Vendr.Web.Models.Mappers](../)

### Methods

#### GiftCardEntitiesToBasicDtos

```csharp
public static IEnumerable<GiftCardBasicDto> GiftCardEntitiesToBasicDtos(
    IEnumerable<GiftCardReadOnly> entities)
```


---

#### GiftCardEntityToBasicDto

```csharp
public static GiftCardBasicDto GiftCardEntityToBasicDto(GiftCardReadOnly entity, 
    GiftCardBasicDto dto = null)
```


---

#### GiftCardEntityToEditDto

```csharp
public static GiftCardEditDto GiftCardEntityToEditDto(GiftCardReadOnly entity, 
    GiftCardEditDto dto = null)
```


---

#### GiftCardSaveDtoToEntity

```csharp
public static GiftCard GiftCardSaveDtoToEntity(GiftCardSaveDto dto, GiftCard entity)
```


<!-- DO NOT EDIT: generated by xmldocmd for Vendr.Web.dll -->