---
title: أنواع سمات الصيانة
description: يشرح هذا الموضوع كيفية إنشاء أنواع السمات في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b93c2ab284d5746f4ecd48cd8b8ffe59aea9f90
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217235"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="91ced-103">أنواع سمات الصيانة</span><span class="sxs-lookup"><span data-stu-id="91ced-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="91ced-104">يشرح هذا الموضوع كيفية إنشاء أنواع السمات في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="91ced-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="91ced-105">يتم استخدام السمات لوصف خصائص العناصر المختلفة.</span><span class="sxs-lookup"><span data-stu-id="91ced-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="91ced-106">يمكن إعداد سمات على العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="91ced-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="91ced-107">أنواع مواقع العمل</span><span class="sxs-lookup"><span data-stu-id="91ced-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="91ced-108">إنشاء مواقع عمل</span><span class="sxs-lookup"><span data-stu-id="91ced-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="91ced-109">أنواع الأصول</span><span class="sxs-lookup"><span data-stu-id="91ced-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="91ced-110">الأصول</span><span class="sxs-lookup"><span data-stu-id="91ced-110">Assets</span></span>

<span data-ttu-id="91ced-111">تختلف السمات التي يمكنك إعدادها، استنادًا إلى العنصر.</span><span class="sxs-lookup"><span data-stu-id="91ced-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="91ced-112">على سبيل المثال، يمكنك إعداد سمات التكوين والحجم الفعلي للموقع فيما يتعلق بموقع عمل.</span><span class="sxs-lookup"><span data-stu-id="91ced-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="91ced-113">فيما يتعلق بنوع أصل أو أصل، يمكنك إعداد سمات لحجم المحرك واستهلاك الطاقة والحد الأقصى لسعة التحميل في ظروف مختلفة.</span><span class="sxs-lookup"><span data-stu-id="91ced-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="91ced-114">إنشاء أنواع سمات</span><span class="sxs-lookup"><span data-stu-id="91ced-114">Create attribute types</span></span>

<span data-ttu-id="91ced-115">يمكنك إنشاء أنواع سمات خاصة بك.</span><span class="sxs-lookup"><span data-stu-id="91ced-115">You can create your own attribute types.</span></span> <span data-ttu-id="91ced-116">بالإضافة إلى ذلك، يمكنك نقل أبعاد المنتج من أبعاد المنتج إلى صفحة **أنواع السمات**.</span><span class="sxs-lookup"><span data-stu-id="91ced-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="91ced-117">حدد **إدارة الأصول** \> **الإعداد** \> **أنواع السمات**.</span><span class="sxs-lookup"><span data-stu-id="91ced-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="91ced-118">في المرة الأولى التي تقوم فيها بإعداد أنواع السمات، حدد **إنشاء أبعاد المنتج** لنقل أبعاد المنتج القياسية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="91ced-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="91ced-119">حدد **جديد** لإنشاء نوع سمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="91ced-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="91ced-120">في الحقل **نوع السمة**، أدخل اسمًا لنوع السمة.</span><span class="sxs-lookup"><span data-stu-id="91ced-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="91ced-121">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="91ced-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="91ced-122">في حقل **الوحدة**،، حدد وحدة السمات ذات الصلة، حسب الاقتضاء.</span><span class="sxs-lookup"><span data-stu-id="91ced-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="91ced-123">في حقل **نوع البيانات**، حدد نوع بيانات للوحدة.</span><span class="sxs-lookup"><span data-stu-id="91ced-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="91ced-124">إذا حددت **سلسلة** كنوع البيانات، فاتبع الخطوات التالية لإنشاء قيم لنوع السمة:</span><span class="sxs-lookup"><span data-stu-id="91ced-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="91ced-125">حدد نوع السمة، ثم حدد **القيم**.</span><span class="sxs-lookup"><span data-stu-id="91ced-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="91ced-126">في حقل **قيم السمة**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="91ced-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="91ced-127">في الحقل **نوع السمة**، حدد نوع سمة (البُعد).</span><span class="sxs-lookup"><span data-stu-id="91ced-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="91ced-128">في حقل **القيمة**، أدخل قيمة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="91ced-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="91ced-129">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="91ced-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="91ced-130">قم بحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="91ced-130">Save the record.</span></span>
    7. <span data-ttu-id="91ced-131">عد إلى صفحة **أنواع السمات**.</span><span class="sxs-lookup"><span data-stu-id="91ced-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="91ced-132">قم بحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="91ced-132">Save the record.</span></span>

    <span data-ttu-id="91ced-133">يعرض حقل **أنواع مواقع العمل** عدد مواقع العمل التي تستخدم نوع السمة.</span><span class="sxs-lookup"><span data-stu-id="91ced-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="91ced-134">يعرض حقل **أنواع الأصول** أنواع الأصول التي تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="91ced-134">The **Asset types** field shows the number of asset types that are using it.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]