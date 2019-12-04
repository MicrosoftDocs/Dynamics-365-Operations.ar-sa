---
title: أنواع سمات الصيانة
description: يشرح هذا الموضوع كيفية إنشاء أنواع السمات في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 625e2c6a6b385c69d33ec4325a462310a37f1eed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812181"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="bbd6a-103">أنواع سمات الصيانة</span><span class="sxs-lookup"><span data-stu-id="bbd6a-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="bbd6a-104">يشرح هذا الموضوع كيفية إنشاء أنواع السمات في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="bbd6a-105">يتم استخدام السمات لوصف خصائص العناصر المختلفة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="bbd6a-106">يمكن إعداد سمات على العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="bbd6a-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="bbd6a-107">أنواع مواقع العمل</span><span class="sxs-lookup"><span data-stu-id="bbd6a-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="bbd6a-108">إنشاء مواقع عمل</span><span class="sxs-lookup"><span data-stu-id="bbd6a-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="bbd6a-109">أنواع الأصول</span><span class="sxs-lookup"><span data-stu-id="bbd6a-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="bbd6a-110">الأصول</span><span class="sxs-lookup"><span data-stu-id="bbd6a-110">Assets</span></span>

<span data-ttu-id="bbd6a-111">تختلف السمات التي يمكنك إعدادها، استنادًا إلى العنصر.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="bbd6a-112">على سبيل المثال، يمكنك إعداد سمات التكوين والحجم الفعلي للموقع فيما يتعلق بموقع عمل.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="bbd6a-113">فيما يتعلق بنوع أصل أو أصل، يمكنك إعداد سمات لحجم المحرك واستهلاك الطاقة والحد الأقصى لسعة التحميل في ظروف مختلفة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="bbd6a-114">إنشاء أنواع سمات</span><span class="sxs-lookup"><span data-stu-id="bbd6a-114">Create attribute types</span></span>

<span data-ttu-id="bbd6a-115">يمكنك إنشاء أنواع سمات خاصة بك.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-115">You can create your own attribute types.</span></span> <span data-ttu-id="bbd6a-116">بالإضافة إلى ذلك، يمكنك نقل أبعاد المنتج من أبعاد المنتج إلى صفحة **أنواع السمات**.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="bbd6a-117">حدد **إدارة الأصول** \> **الإعداد** \> **أنواع السمات**.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="bbd6a-118">في المرة الأولى التي تقوم فيها بإعداد أنواع السمات، حدد **إنشاء أبعاد المنتج** لنقل أبعاد المنتج القياسية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="bbd6a-119">حدد **جديد** لإنشاء نوع سمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="bbd6a-120">في الحقل **نوع السمة**، أدخل اسمًا لنوع السمة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="bbd6a-121">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="bbd6a-122">في حقل **الوحدة**،، حدد وحدة السمات ذات الصلة، حسب الاقتضاء.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="bbd6a-123">في حقل **نوع البيانات**، حدد نوع بيانات للوحدة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="bbd6a-124">إذا حددت **سلسلة** كنوع البيانات، فاتبع الخطوات التالية لإنشاء قيم لنوع السمة:</span><span class="sxs-lookup"><span data-stu-id="bbd6a-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="bbd6a-125">حدد نوع السمة، ثم حدد **القيم**.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="bbd6a-126">في حقل **قيم السمة**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="bbd6a-127">في الحقل **نوع السمة**، حدد نوع سمة (البُعد).</span><span class="sxs-lookup"><span data-stu-id="bbd6a-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="bbd6a-128">في حقل **القيمة**، أدخل قيمة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="bbd6a-129">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="bbd6a-130">قم بحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-130">Save the record.</span></span>
    7. <span data-ttu-id="bbd6a-131">عد إلى صفحة **أنواع السمات**.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="bbd6a-132">قم بحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-132">Save the record.</span></span>

    <span data-ttu-id="bbd6a-133">يعرض حقل **أنواع مواقع العمل** عدد مواقع العمل التي تستخدم نوع السمة.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="bbd6a-134">يعرض حقل **أنواع الأصول** أنواع الأصول التي تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="bbd6a-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
