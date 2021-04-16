---
title: إنشاء nomenclature لرقم منتج لمتغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا الإجراء كيفية إعداد كود nomenclature لرقم المنتج لمتغيرات المنتج المكوّنة، وكيف يمكن إرفاقه بأصل منتج قابل للتكوين.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f342831d95f9988f9bb7807bac986e43cb317e0f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819989"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="cd2f2-103">إنشاء nomenclature لرقم منتج لمتغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="cd2f2-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd2f2-104">يوضح هذا الإجراء كيفية إعداد كود nomenclature لرقم المنتج لمتغيرات المنتج المكوّنة، وكيف يمكن إرفاقه بأصل منتج قابل للتكوين.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="cd2f2-105">يوضح هذا الإجراء أيضًا كيف يمكنك بناء nomenclature تكوين لمكون نموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="cd2f2-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cd2f2-107">يتم تعيين nomenclature رقم المنتج الجديد إلى أصل المنتج D0004.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="cd2f2-108">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="cd2f2-109">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="cd2f2-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="cd2f2-110">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="cd2f2-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="cd2f2-111">انقر فوق "كود nomenclature للمنتج‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="cd2f2-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-112">Click New.</span></span>
4. <span data-ttu-id="cd2f2-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cd2f2-114">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cd2f2-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-115">Click Add.</span></span>
7. <span data-ttu-id="cd2f2-116">انقر فوق "رقم أصل المنتج".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-116">Click Product master number.</span></span>
8. <span data-ttu-id="cd2f2-117">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-117">Click Add.</span></span>
9. <span data-ttu-id="cd2f2-118">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-118">Click Text constant.</span></span>
10. <span data-ttu-id="cd2f2-119">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="cd2f2-120">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="cd2f2-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-121">Click Add.</span></span>
13. <span data-ttu-id="cd2f2-122">انقر فوق "التكوين".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-122">Click Configuration.</span></span>
14. <span data-ttu-id="cd2f2-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="cd2f2-124">تعيين nomenclature رقم المنتج إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="cd2f2-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="cd2f2-125">انقر فوق "أصول المنتجات".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-125">Click Product masters.</span></span>
2. <span data-ttu-id="cd2f2-126">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cd2f2-127">على سبيل المثال، قم بإجراء التصفية على الحقل "رقم المنتج" باستخدام القيمة "D".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="cd2f2-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cd2f2-129">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-129">Click Edit.</span></span>
5. <span data-ttu-id="cd2f2-130">حدد "نعم" في الحقل "استخدام كود nomenclature".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="cd2f2-131">في حقل "كود nomenclature لرقم متغير المنتج‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="cd2f2-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-132">Close the page.</span></span>
8. <span data-ttu-id="cd2f2-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="cd2f2-134">إنشاء nomenclature لمكون نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="cd2f2-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="cd2f2-135">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="cd2f2-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cd2f2-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cd2f2-138">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-138">Click Edit.</span></span>
5. <span data-ttu-id="cd2f2-139">حدد "نعم" في الحقل "استخدام كود nomenclature للتكوين‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="cd2f2-140">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-140">Click Add.</span></span>
7. <span data-ttu-id="cd2f2-141">انقر فوق "قيمة السمة‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-141">Click Attribute value.</span></span>
8. <span data-ttu-id="cd2f2-142">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="cd2f2-143">في حقل "التسمية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="cd2f2-144">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-144">Click Add.</span></span>
11. <span data-ttu-id="cd2f2-145">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-145">Click Text constant.</span></span>
12. <span data-ttu-id="cd2f2-146">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="cd2f2-147">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="cd2f2-148">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-148">Click Add.</span></span>
15. <span data-ttu-id="cd2f2-149">انقر فوق "قيمة السمة‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-149">Click Attribute value.</span></span>
16. <span data-ttu-id="cd2f2-150">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="cd2f2-151">في حقل "التسمية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="cd2f2-152">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-152">Click Add.</span></span>
19. <span data-ttu-id="cd2f2-153">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-153">Click Text constant.</span></span>
20. <span data-ttu-id="cd2f2-154">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="cd2f2-155">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="cd2f2-156">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-156">Click Add.</span></span>
23. <span data-ttu-id="cd2f2-157">انقر فوق "قيمة السمة‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-157">Click Attribute value.</span></span>
24. <span data-ttu-id="cd2f2-158">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="cd2f2-159">في حقل "التسمية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="cd2f2-160">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-160">Click Add.</span></span>
27. <span data-ttu-id="cd2f2-161">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-161">Click Text constant.</span></span>
28. <span data-ttu-id="cd2f2-162">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="cd2f2-163">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="cd2f2-164">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-164">Click Add.</span></span>
31. <span data-ttu-id="cd2f2-165">انقر فوق "قيمة السمة‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-165">Click Attribute value.</span></span>
32. <span data-ttu-id="cd2f2-166">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="cd2f2-167">في حقل "التسمية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="cd2f2-168">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-168">Click Add.</span></span>
35. <span data-ttu-id="cd2f2-169">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-169">Click Text constant.</span></span>
36. <span data-ttu-id="cd2f2-170">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="cd2f2-171">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="cd2f2-172">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-172">Click Add.</span></span>
39. <span data-ttu-id="cd2f2-173">انقر فوق "قيمة التسلسل الرقمي".</span><span class="sxs-lookup"><span data-stu-id="cd2f2-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="cd2f2-174">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="cd2f2-175">في حقل "التسلسل الرقمي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="cd2f2-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-176">Close the page.</span></span>
43. <span data-ttu-id="cd2f2-177">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-177">Close the page.</span></span>
44. <span data-ttu-id="cd2f2-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd2f2-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]