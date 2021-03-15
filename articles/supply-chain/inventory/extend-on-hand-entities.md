---
title: توسيع كيانات بيانات المخزون الفعلي
description: يقدم هذا الموضوع مثالاً يوضح كيفية إضافة حقول موسعة إلى طرق العرض INVENTORSITEONHANDENTITY وINVENTWAREHOUSEONHANDENTITY، بحيث يمكن لقدرات كيانات بيانات المخزون الفعلي العمل مع الملحقات.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2e805b9379c73f7b7eb2820662fad70e28181ebf
ms.sourcegitcommit: f59df61799915f6a79aec7e3e8664c02df6597da
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/22/2021
ms.locfileid: "5043383"
---
# <a name="extend-inventory-on-hand-data-entities"></a>توسيع كيانات بيانات المخزون الفعلي

[!include [banner](../includes/banner.md)]

يوفر Microsoft Dynamics 365 Supply Chain Management ميزات [قابلية التوسعة](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) التي تسمح لك [بإضافة حقول إلى الجداول عبر الملحق](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). يقدم هذا الموضوع مثالاً يوضح كيفية إضافة حقول موسعة إلى طرق العرض `INVENTORSITEONHANDENTITY` و`INVENTWAREHOUSEONHANDENTITY`، بحيث يمكن لقدرات كيانات بيانات المخزون الفعلي العمل مع الملحقات. للحصول على مزيد من المعلومات حول كيانات البيانات، راجع [نظرة عامة حول إدارة البيانات](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> فيما يلي قائمة ببعض كيانات بيانات المخزون الفعلي:
>
> - الكمية المتاحة من المخزون حسب الموقع
> - الكمية المتاحة من المخزون حسب الموقع V2
> - المخزون الفعلي حسب المستودع
> - المخزون الفعلي حسب المستودع v2

بعد إضافة حقول إلى الجداول المستخدمة بواسطة طريقة العرض `inventSiteOnHandView`، يجب عليك مزامنة المحرك بحيث يتم التعرف علي الملحقات بشكل صحيح.

1. قم بتوسيع طريقة العرض `InventSiteOnHandView` عن طريق إضافة حقل الملحق
1. قم بتوسيع طريقة العرض `InventSiteOnHandAggregatedView` بواسطة حقول الملحق
1. قم بتوسيع فئة `InventSiteOnHandAggregatedViewBuilder` viewBuilder عن طريق تعديل أسلوب `getExtensionFields()`. وبهذه الطريقة، يمكنك تعيين حقول العرض القديمة إلى حقول العرض الجديدة عند تشغيل مزامنة viewBuilder.

على سبيل المثال، لقد قمت بإضافة الحقول الأربعة التالية إلى الجدول `InventTable` عبر الملحق:

- الحقل المخصص 1
- الحقل المخصص 2
- الحقل المخصص 3
- الحقل المخصص 4

في هذه الحالة، يجب عليك تعديل الأسلوب `getExtensionFields()` بالطريقة التالية.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

بعد إكمال هذه الخطوات، يمكنك توسيع كيانات بيانات المخزون الفعلي حسب الموقع والمخزون الفعلي حسب المستودع عن طريق إضافة الحقول الجديدة. وبهذه الطريقة، تتأكد من أن أنه يتم التعرف على الحقول الموسعة ويتم تضمينها أثناء ترحيل البيانات التي تستخدم كيانات البيانات هذه.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]