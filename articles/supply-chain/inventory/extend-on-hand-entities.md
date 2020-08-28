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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: e276348a63bfdb9e712c0ea86e6c2a68c50872c0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665394"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="0ea4b-103">توسيع كيانات بيانات المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="0ea4b-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ea4b-104">يوفر Microsoft Dynamics 365 Supply Chain Management ميزات [قابلية التوسعة](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) التي تسمح لك [بإضافة حقول إلى الجداول عبر الملحق](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span><span class="sxs-lookup"><span data-stu-id="0ea4b-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="0ea4b-105">يقدم هذا الموضوع مثالاً يوضح كيفية إضافة حقول موسعة إلى طرق العرض `INVENTORSITEONHANDENTITY` و`INVENTWAREHOUSEONHANDENTITY`، بحيث يمكن لقدرات كيانات بيانات المخزون الفعلي العمل مع الملحقات.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="0ea4b-106">للحصول على مزيد من المعلومات حول كيانات البيانات، راجع [نظرة عامة حول إدارة البيانات](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0ea4b-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0ea4b-107">فيما يلي قائمة ببعض كيانات بيانات المخزون الفعلي:</span><span class="sxs-lookup"><span data-stu-id="0ea4b-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="0ea4b-108">الكمية المتاحة من المخزون حسب الموقع</span><span class="sxs-lookup"><span data-stu-id="0ea4b-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="0ea4b-109">الكمية المتاحة من المخزون حسب الموقع V2</span><span class="sxs-lookup"><span data-stu-id="0ea4b-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="0ea4b-110">المخزون الفعلي حسب المستودع</span><span class="sxs-lookup"><span data-stu-id="0ea4b-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="0ea4b-111">المخزون الفعلي حسب المستودع v2</span><span class="sxs-lookup"><span data-stu-id="0ea4b-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="0ea4b-112">بعد إضافة حقول إلى الجداول المستخدمة بواسطة طريقة العرض `inventSiteOnHandView`، يجب عليك مزامنة المحرك بحيث يتم التعرف علي الملحقات بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="0ea4b-113">قم بتوسيع طريقة العرض `InventSiteOnHandView` عن طريق إضافة حقل الملحق</span><span class="sxs-lookup"><span data-stu-id="0ea4b-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="0ea4b-114">قم بتوسيع طريقة العرض `InventSiteOnHandAggregatedView` بواسطة حقول الملحق</span><span class="sxs-lookup"><span data-stu-id="0ea4b-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="0ea4b-115">قم بتوسيع فئة `InventSiteOnHandAggregatedViewBuilder` viewBuilder عن طريق تعديل أسلوب `getExtensionFields()`.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="0ea4b-116">وبهذه الطريقة، يمكنك تعيين حقول العرض القديمة إلى حقول العرض الجديدة عند تشغيل مزامنة viewBuilder.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="0ea4b-117">على سبيل المثال، لقد قمت بإضافة الحقول الأربعة التالية إلى الجدول `InventTable` عبر الملحق:</span><span class="sxs-lookup"><span data-stu-id="0ea4b-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="0ea4b-118">الحقل المخصص 1</span><span class="sxs-lookup"><span data-stu-id="0ea4b-118">Custom field 1</span></span>
- <span data-ttu-id="0ea4b-119">الحقل المخصص 2</span><span class="sxs-lookup"><span data-stu-id="0ea4b-119">Custom field 2</span></span>
- <span data-ttu-id="0ea4b-120">الحقل المخصص 3</span><span class="sxs-lookup"><span data-stu-id="0ea4b-120">Custom field 3</span></span>
- <span data-ttu-id="0ea4b-121">الحقل المخصص 4</span><span class="sxs-lookup"><span data-stu-id="0ea4b-121">Custom field 4</span></span>

<span data-ttu-id="0ea4b-122">في هذه الحالة، يجب عليك تعديل الأسلوب `getExtensionFields()` بالطريقة التالية.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

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

<span data-ttu-id="0ea4b-123">بعد إكمال هذه الخطوات، يمكنك توسيع كيانات بيانات المخزون الفعلي حسب الموقع والمخزون الفعلي حسب المستودع عن طريق إضافة الحقول الجديدة.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="0ea4b-124">وبهذه الطريقة، تتأكد من أن أنه يتم التعرف على الحقول الموسعة ويتم تضمينها أثناء ترحيل البيانات التي تستخدم كيانات البيانات هذه.</span><span class="sxs-lookup"><span data-stu-id="0ea4b-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
