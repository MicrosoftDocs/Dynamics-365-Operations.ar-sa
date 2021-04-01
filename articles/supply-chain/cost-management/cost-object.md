---
title: كائنات التكلفة
description: توفر هذه المقالة معلومات حول كائنات التكاليف وتشرح كيفية تراكم التكاليف والكميات. كائن التكلفة هو كيان تتراكم له التكاليف والكميات. وبإمكان كائن التكلفة أن يكون عبارة عن منتج أو متغيرات منتج، كمتغيرات النمط واللون.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee7c170d5a330c0080931a67c1548eb0d3522bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232388"
---
# <a name="cost-objects"></a><span data-ttu-id="58bf1-105">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="58bf1-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58bf1-106">توفر هذه المقالة معلومات حول كائنات التكاليف وتشرح كيفية تراكم التكاليف والكميات.</span><span class="sxs-lookup"><span data-stu-id="58bf1-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="58bf1-107">كائن التكلفة هو كيان تتراكم له التكاليف والكميات.</span><span class="sxs-lookup"><span data-stu-id="58bf1-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="58bf1-108">وبإمكان كائن التكلفة أن يكون عبارة عن منتج أو متغيرات منتج، كمتغيرات النمط واللون.</span><span class="sxs-lookup"><span data-stu-id="58bf1-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="58bf1-109">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="58bf1-109">Cost objects</span></span>

<span data-ttu-id="58bf1-110">تسرد صفحة **كائنات التكلفة** كافة كائنات التكلفة التي تم تسجيلها في منتج.</span><span class="sxs-lookup"><span data-stu-id="58bf1-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="58bf1-111">ويتم تحديد كائنات التكلفة حسب البيانات من المصادر التالية:</span><span class="sxs-lookup"><span data-stu-id="58bf1-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="58bf1-112">منتج</span><span class="sxs-lookup"><span data-stu-id="58bf1-112">Product</span></span>
-   <span data-ttu-id="58bf1-113">مجموعة أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="58bf1-113">Product dimension group</span></span>
-   <span data-ttu-id="58bf1-114">مجموعة أبعاد التخزين</span><span class="sxs-lookup"><span data-stu-id="58bf1-114">Storage dimension group</span></span>
-   <span data-ttu-id="58bf1-115">مجموعة أبعاد التعقب</span><span class="sxs-lookup"><span data-stu-id="58bf1-115">Tracking dimension group</span></span>

<span data-ttu-id="58bf1-116">**ملاحظة:** يمثل كائن التكلفة عنصر تكلفة من نوع **المواد المباشرة** فقط.</span><span class="sxs-lookup"><span data-stu-id="58bf1-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="58bf1-117">يختلف كائن التكلفة وكائن المخزون في الطريقة حيث إن كائن التكلفة يتم تحديده حسب أبعاد المخزون التي تم تحديدها للمخزون المالي.</span><span class="sxs-lookup"><span data-stu-id="58bf1-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="58bf1-118">على سبيل المثال، صنف يشتمل على التكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="58bf1-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="58bf1-119">**الموقع:** المخزون الفعلي = نعم، المخزون المالي = نعم</span><span class="sxs-lookup"><span data-stu-id="58bf1-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="58bf1-120">**المستودع:** المخزون الفعلي = نعم، المخزون المالي = لا</span><span class="sxs-lookup"><span data-stu-id="58bf1-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="58bf1-121">**رقم الدُفعة:** المخزون الفعلي = نعم، المخزون المالي = لا</span><span class="sxs-lookup"><span data-stu-id="58bf1-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="58bf1-122">يوضح الجدول التالي المقصود بكائن التكلفة والمقصود بكائن المخزون.</span><span class="sxs-lookup"><span data-stu-id="58bf1-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="58bf1-123">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="58bf1-123">Object type</span></span>      | <span data-ttu-id="58bf1-124">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="58bf1-124">Item number</span></span> | <span data-ttu-id="58bf1-125">الموقع</span><span class="sxs-lookup"><span data-stu-id="58bf1-125">Site</span></span> | <span data-ttu-id="58bf1-126">المستودع</span><span class="sxs-lookup"><span data-stu-id="58bf1-126">Warehouse</span></span> | <span data-ttu-id="58bf1-127">رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="58bf1-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="58bf1-128">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="58bf1-128">Cost object</span></span>      | <span data-ttu-id="58bf1-129">×</span><span class="sxs-lookup"><span data-stu-id="58bf1-129">x</span></span>           | <span data-ttu-id="58bf1-130">×</span><span class="sxs-lookup"><span data-stu-id="58bf1-130">x</span></span>    |           |           |
| <span data-ttu-id="58bf1-131">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="58bf1-131">Inventory object</span></span> | <span data-ttu-id="58bf1-132">×</span><span class="sxs-lookup"><span data-stu-id="58bf1-132">x</span></span>           | <span data-ttu-id="58bf1-133">×</span><span class="sxs-lookup"><span data-stu-id="58bf1-133">x</span></span>    |  <span data-ttu-id="58bf1-134">×</span><span class="sxs-lookup"><span data-stu-id="58bf1-134">x</span></span>        | <span data-ttu-id="58bf1-135">×</span><span class="sxs-lookup"><span data-stu-id="58bf1-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="58bf1-136">تراكم التكاليف والكميات</span><span class="sxs-lookup"><span data-stu-id="58bf1-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="58bf1-137">القيمة في حقل **القيمة** هي مجموع القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="58bf1-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="58bf1-138">مبلغ تكلفة المخزون الفعلية</span><span class="sxs-lookup"><span data-stu-id="58bf1-138">Physical cost amount</span></span>
    -   <span data-ttu-id="58bf1-139">مبلغ التكلفة المالية</span><span class="sxs-lookup"><span data-stu-id="58bf1-139">Financial cost amount</span></span>
    -   <span data-ttu-id="58bf1-140">التسويات</span><span class="sxs-lookup"><span data-stu-id="58bf1-140">Adjustments</span></span>
-   <span data-ttu-id="58bf1-141">القيمة في حقل **الكمية** هي مجموع القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="58bf1-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="58bf1-142">مُستَلم</span><span class="sxs-lookup"><span data-stu-id="58bf1-142">Received</span></span>
    -   <span data-ttu-id="58bf1-143">مخفض</span><span class="sxs-lookup"><span data-stu-id="58bf1-143">Deducted</span></span>
    -   <span data-ttu-id="58bf1-144">الكمية التي تم ترحيلها</span><span class="sxs-lookup"><span data-stu-id="58bf1-144">Posted quantity</span></span>
-   <span data-ttu-id="58bf1-145">حقل **متوسط تكلفة الوحدة** عبارة عن حقل محسوب.</span><span class="sxs-lookup"><span data-stu-id="58bf1-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="58bf1-146">ويتم حساب القيمة بقسمة قيمة **القيمة** على قيمة **الكمية**.</span><span class="sxs-lookup"><span data-stu-id="58bf1-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="58bf1-147">**ملاحظة:** لا تؤثر معلمة **تضمين القيمة الفعلية** في الحسابات السابقة.</span><span class="sxs-lookup"><span data-stu-id="58bf1-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="58bf1-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="58bf1-148">Additional resources</span></span>
--------

[<span data-ttu-id="58bf1-149">مجموعة أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="58bf1-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="58bf1-150">مجموعة أبعاد التخزين</span><span class="sxs-lookup"><span data-stu-id="58bf1-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="58bf1-151">مجموعة أبعاد التعقب</span><span class="sxs-lookup"><span data-stu-id="58bf1-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="58bf1-152">ما الجديد أو التغيير</span><span class="sxs-lookup"><span data-stu-id="58bf1-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="58bf1-153">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="58bf1-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]