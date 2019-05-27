---
title: تحديد كيفية التخلص من الأصناف المرتجعة
description: تحديد كيفية التخلص من الأصناف المرتجعة.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6fcdfec083aeb9c58d63f6e03542758e4d07e4d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560084"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="b6b02-103">تحديد كيفية التخلص من الأصناف المرتجعة</span><span class="sxs-lookup"><span data-stu-id="b6b02-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b6b02-104">عند معالجة أمر إرجاع، عليك تحديد كود سبب إرجاع لتحديد سبب إرجاع المنتج.</span><span class="sxs-lookup"><span data-stu-id="b6b02-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="b6b02-105">يجب عليك أيضًا تحديد رمز الإرجاع وإجراء الإرجاع الذي يجب اتخاذه مع المنتج المرتجع ذاته.</span><span class="sxs-lookup"><span data-stu-id="b6b02-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="b6b02-106">يمكن تطبيق كود الترتيب عند إنشاء أمر الإرجاع وتسجيل وصول صنف أو تحديث كشف التعبئة الخاص بوصول صنف وكذلك عند إنهاء أمر إدخال مخزن الفحص.</span><span class="sxs-lookup"><span data-stu-id="b6b02-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="b6b02-107">يمكنك تحديد أية رموز إرجاع ضرورية تحتاجها لدعم عمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="b6b02-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="b6b02-108">ويوفر الجدول التالي مجموعة من الرموز المستخدمة بشكلٍ نموذجي لتعيين ترتيب صنف مرتجع.</span><span class="sxs-lookup"><span data-stu-id="b6b02-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6b02-109">نوع الترتيب</span><span class="sxs-lookup"><span data-stu-id="b6b02-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="b6b02-110">الكود العام</span><span class="sxs-lookup"><span data-stu-id="b6b02-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="b6b02-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="b6b02-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-112">التخلص</span><span class="sxs-lookup"><span data-stu-id="b6b02-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b6b02-113">SC</span><span class="sxs-lookup"><span data-stu-id="b6b02-113">SC</span></span></p></td>
<td><p><span data-ttu-id="b6b02-114">خردة/تالف</span><span class="sxs-lookup"><span data-stu-id="b6b02-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-115">التخلص</span><span class="sxs-lookup"><span data-stu-id="b6b02-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b6b02-116">DC</span><span class="sxs-lookup"><span data-stu-id="b6b02-116">DC</span></span></p></td>
<td><p><span data-ttu-id="b6b02-117">التبرع للأعمال الخيرية</span><span class="sxs-lookup"><span data-stu-id="b6b02-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-118">التخلص</span><span class="sxs-lookup"><span data-stu-id="b6b02-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b6b02-119">TD</span><span class="sxs-lookup"><span data-stu-id="b6b02-119">TD</span></span></p></td>
<td><p><span data-ttu-id="b6b02-120">التخلص الخاص بجهة أخرى</span><span class="sxs-lookup"><span data-stu-id="b6b02-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-121">التخلص</span><span class="sxs-lookup"><span data-stu-id="b6b02-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b6b02-122">SL</span><span class="sxs-lookup"><span data-stu-id="b6b02-122">SL</span></span></p></td>
<td><p><span data-ttu-id="b6b02-123">المسترد</span><span class="sxs-lookup"><span data-stu-id="b6b02-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-124">التخلص</span><span class="sxs-lookup"><span data-stu-id="b6b02-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b6b02-125">TS</span><span class="sxs-lookup"><span data-stu-id="b6b02-125">TS</span></span></p></td>
<td><p><span data-ttu-id="b6b02-126">مبيعات جهة أخرى (أسواق ثانوية)</span><span class="sxs-lookup"><span data-stu-id="b6b02-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-127">إصلاح/تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b6b02-128">RW</span><span class="sxs-lookup"><span data-stu-id="b6b02-128">RW</span></span></p></td>
<td><p><span data-ttu-id="b6b02-129">إعادة العمل</span><span class="sxs-lookup"><span data-stu-id="b6b02-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-130">إصلاح/تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b6b02-131">RF</span><span class="sxs-lookup"><span data-stu-id="b6b02-131">RF</span></span></p></td>
<td><p><span data-ttu-id="b6b02-132">جهة إعادة التصنيع/التجديد</span><span class="sxs-lookup"><span data-stu-id="b6b02-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-133">إصلاح/تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b6b02-134">MD</span><span class="sxs-lookup"><span data-stu-id="b6b02-134">MD</span></span></p></td>
<td><p><span data-ttu-id="b6b02-135">تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-136">إصلاح/تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b6b02-137">RP</span><span class="sxs-lookup"><span data-stu-id="b6b02-137">RP</span></span></p></td>
<td><p><span data-ttu-id="b6b02-138">تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-139">إصلاح/تعديل</span><span class="sxs-lookup"><span data-stu-id="b6b02-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b6b02-140">RV</span><span class="sxs-lookup"><span data-stu-id="b6b02-140">RV</span></span></p></td>
<td><p><span data-ttu-id="b6b02-141">إرجاع إلى المورّد</span><span class="sxs-lookup"><span data-stu-id="b6b02-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-142">أخرى</span><span class="sxs-lookup"><span data-stu-id="b6b02-142">Other</span></span></p></td>
<td><p><span data-ttu-id="b6b02-143">AI</span><span class="sxs-lookup"><span data-stu-id="b6b02-143">AI</span></span></p></td>
<td><p><span data-ttu-id="b6b02-144">الاستخدام على حالتها</span><span class="sxs-lookup"><span data-stu-id="b6b02-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-145">آخر</span><span class="sxs-lookup"><span data-stu-id="b6b02-145">Other</span></span></p></td>
<td><p><span data-ttu-id="b6b02-146">RS</span><span class="sxs-lookup"><span data-stu-id="b6b02-146">RS</span></span></p></td>
<td><p><span data-ttu-id="b6b02-147">إعادة البيع</span><span class="sxs-lookup"><span data-stu-id="b6b02-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-148">آخر</span><span class="sxs-lookup"><span data-stu-id="b6b02-148">Other</span></span></p></td>
<td><p><span data-ttu-id="b6b02-149">EX</span><span class="sxs-lookup"><span data-stu-id="b6b02-149">EX</span></span></p></td>
<td><p><span data-ttu-id="b6b02-150">التبادل</span><span class="sxs-lookup"><span data-stu-id="b6b02-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-151">آخر</span><span class="sxs-lookup"><span data-stu-id="b6b02-151">Other</span></span></p></td>
<td><p><span data-ttu-id="b6b02-152">سيدة</span><span class="sxs-lookup"><span data-stu-id="b6b02-152">MS</span></span></p></td>
<td><p><span data-ttu-id="b6b02-153">متنوع</span><span class="sxs-lookup"><span data-stu-id="b6b02-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6b02-154">عليك تحديد إجراء الترتيب لكل رمز ترتيب تقوم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="b6b02-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="b6b02-155">يحدد إجراء الترتيب المعاني الفعلية والمالية لرموز الترتيب.</span><span class="sxs-lookup"><span data-stu-id="b6b02-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="b6b02-156">على سبيل المثال، يحدد إجراء الترتيب المعالجة الفعلية للصنف المرتجع، والتأثير المالي للصنف المرتجع، وما إذا كان يجب إرسال صنف استبدال للعميل.</span><span class="sxs-lookup"><span data-stu-id="b6b02-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="b6b02-157">يمكنك تحديد عدد غير محدود لرموز الإرجاع وفقًا لاحتياجات العمل الخاصة بك، ولكن يوجد فقط ستة إجراءات ترتيب معرفة مسبقًا يجب أن تحدد منها.</span><span class="sxs-lookup"><span data-stu-id="b6b02-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="b6b02-158">ويسرد الجدول التالي إجراءات الترتيب وتعريفاتها.</span><span class="sxs-lookup"><span data-stu-id="b6b02-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6b02-159">إجراءات الترتيب</span><span class="sxs-lookup"><span data-stu-id="b6b02-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="b6b02-160">الوصف</span><span class="sxs-lookup"><span data-stu-id="b6b02-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-161"><strong>يضع في الحساب مبلغاً دائناً</strong></span><span class="sxs-lookup"><span data-stu-id="b6b02-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="b6b02-162">إرجاع الصنف إلى المخزون وائتمان العميل.</span><span class="sxs-lookup"><span data-stu-id="b6b02-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-163"><strong>يضع في الحساب مبلغاً دائناً فقط</strong></span><span class="sxs-lookup"><span data-stu-id="b6b02-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="b6b02-164">ائتمان العميل بدون السؤال عن أو توقع إرجاع الصنف.</span><span class="sxs-lookup"><span data-stu-id="b6b02-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-165"><strong>خردة</strong></span><span class="sxs-lookup"><span data-stu-id="b6b02-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="b6b02-166">تخريد الصنف وائتمان العميل.</span><span class="sxs-lookup"><span data-stu-id="b6b02-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-167"><strong>استبدال وائتمان</strong></span><span class="sxs-lookup"><span data-stu-id="b6b02-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="b6b02-168">إرجاع الصنف إلى المخزون وإنشاء أمر استبدال وائتمان العميل.</span><span class="sxs-lookup"><span data-stu-id="b6b02-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b02-169"><strong>استبدال وتخريد</strong></span><span class="sxs-lookup"><span data-stu-id="b6b02-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="b6b02-170">تخريد الصنف وإنشاء أمر استبدال وائتمان العميل.</span><span class="sxs-lookup"><span data-stu-id="b6b02-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b02-171"><strong>إرجاع إلى العميل</strong></span><span class="sxs-lookup"><span data-stu-id="b6b02-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="b6b02-172">رفض الصنف المرتجع وإعادته إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="b6b02-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="b6b02-173">تحديد كود توزيع لأمر إدخال مخزن الفحص</span><span class="sxs-lookup"><span data-stu-id="b6b02-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="b6b02-174">‏‫انقر فوق **‏‫إدارة المخزون‬** \> **دوري** \> **إدارة الجودة** \>‏‫ **أوامر إدخال مخزن الفحص**.</span><span class="sxs-lookup"><span data-stu-id="b6b02-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="b6b02-175">بالنسبة لأمر إدخال مخزن الفحص الموجود، حدد إجراءً من الحقل **رمز الإرجاع** من علامة التبويب **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="b6b02-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="b6b02-176">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b6b02-176">See also</span></span>

<span data-ttu-id="b6b02-177">[أمر إدخال مخزن الفحص (نموذج)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="b6b02-177">[Quarantine order (form)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="b6b02-178">[أكواد الترتيب (نموذج)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b6b02-178">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

  


