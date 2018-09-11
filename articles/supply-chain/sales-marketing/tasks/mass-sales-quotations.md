--- 
title: "إنشاء شامل لعروض أسعار المبيعات"
description: "يوضح هذا الإجراء كيفية إنشاء عروض أسعار تقدم مجموعة من المنتجات أو الخدمات التي سيتم إرسالها إلى عملاء متعددين بكفاءة."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: fe2d4cff512c32069f6aef3134e604b0ce6e47cc
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="44f2e-103">إنشاء شامل لعروض أسعار المبيعات</span><span class="sxs-lookup"><span data-stu-id="44f2e-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44f2e-104">يوضح هذا الإجراء كيفية إنشاء عروض أسعار تقدم مجموعة من المنتجات أو الخدمات التي سيتم إرسالها إلى عملاء متعددين بكفاءة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="44f2e-105">يعتمد إنشاء عرض الأسعار الجماعي هذا على قوالب عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="44f2e-106">يمكنك تنفيذ هذا الإجراء في البيانات الخاصة بك أو في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="44f2e-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="44f2e-107">إنشاء قالب عروض أسعار</span><span class="sxs-lookup"><span data-stu-id="44f2e-107">Create a quotation template</span></span>
1. <span data-ttu-id="44f2e-108">انتقل إلى المبيعات والتسويق > الإعداد > عروض الأسعار > مجموعات القوالب.</span><span class="sxs-lookup"><span data-stu-id="44f2e-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="44f2e-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="44f2e-109">Click New.</span></span>
3. <span data-ttu-id="44f2e-110">في الحقل "معرف المجموعة"، اكتب معرفاً تختاره.</span><span class="sxs-lookup"><span data-stu-id="44f2e-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="44f2e-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="44f2e-112">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="44f2e-112">Click Save.</span></span>
6. <span data-ttu-id="44f2e-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-113">Close the page.</span></span>
7. <span data-ttu-id="44f2e-114">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="44f2e-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="44f2e-115">Click New.</span></span>
9. <span data-ttu-id="44f2e-116">في الحقل "نوع الحساب"، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="44f2e-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="44f2e-117">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="44f2e-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="44f2e-118">Click OK.</span></span>
    * <span data-ttu-id="44f2e-119">لكي يصبح عرض الأسعار قالبًا، يجب تنفيذ خطوات الإعداد برأس عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="44f2e-120">ويجب إجراء هذا قبل إضافة بنود لعرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="44f2e-121">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="44f2e-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="44f2e-122">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="44f2e-122">Click Change view.</span></span>
14. <span data-ttu-id="44f2e-123">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="44f2e-123">Click Header view.</span></span>
15. <span data-ttu-id="44f2e-124">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="44f2e-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="44f2e-125">في الحقل "معرف المجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="44f2e-126">في الحقل "اسم القالب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="44f2e-127">حدد "نعم" في الحقل "نشط".</span><span class="sxs-lookup"><span data-stu-id="44f2e-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="44f2e-128">يمكن استخدام القوالب النشطة فقط عند تطبيق قالب على عرض أسعار مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="44f2e-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="44f2e-129">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="44f2e-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="44f2e-130">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="44f2e-130">Click Change view.</span></span>
21. <span data-ttu-id="44f2e-131">انقر فوق "عرض البند".</span><span class="sxs-lookup"><span data-stu-id="44f2e-131">Click Line view.</span></span>
22. <span data-ttu-id="44f2e-132">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="44f2e-133">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="44f2e-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-134">Close the page.</span></span>
25. <span data-ttu-id="44f2e-135">في الحقل "‏‫النسبة المئوية‬ للخصم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="44f2e-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="44f2e-136">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="44f2e-136">Click Add line.</span></span>
27. <span data-ttu-id="44f2e-137">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="44f2e-138">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="44f2e-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-139">Close the page.</span></span>
30. <span data-ttu-id="44f2e-140">في الحقل "وحدة السعر"، أدخل سعرًا جديدًا أو قم بتغيير السعر الحالي.</span><span class="sxs-lookup"><span data-stu-id="44f2e-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="44f2e-141">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="44f2e-141">Click Add line.</span></span>
32. <span data-ttu-id="44f2e-142">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="44f2e-143">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="44f2e-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-144">Close the page.</span></span>
35. <span data-ttu-id="44f2e-145">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="44f2e-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="44f2e-146">في الحقل "الخصم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="44f2e-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="44f2e-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="44f2e-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="44f2e-148">تطبيق القالب لإنشاء عرض أسعار مفرد</span><span class="sxs-lookup"><span data-stu-id="44f2e-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="44f2e-149">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="44f2e-150">لاحظ أن عرض الأسعار الذي قمت بإنشائه للتو ه تم تمييز كـ"قالب".</span><span class="sxs-lookup"><span data-stu-id="44f2e-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="44f2e-151">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="44f2e-151">Click New.</span></span>
3. <span data-ttu-id="44f2e-152">في الحقل "نوع الحساب"، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="44f2e-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="44f2e-153">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="44f2e-154">قم بتوسيع القسم "القالب".</span><span class="sxs-lookup"><span data-stu-id="44f2e-154">Expand the Template section.</span></span>
6. <span data-ttu-id="44f2e-155">في الحقل "معرف المجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="44f2e-156">في الحقل "اسم القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="44f2e-157">في الحقل "أسلوب الحساب"، حدد "استناداً إلى قيم القالب".</span><span class="sxs-lookup"><span data-stu-id="44f2e-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="44f2e-158">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="44f2e-158">Click OK.</span></span>
    * <span data-ttu-id="44f2e-159">تم إنشاء عرض الأسعار الجديد الآن استناداً إلى البيانات وشروط القالب.</span><span class="sxs-lookup"><span data-stu-id="44f2e-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="44f2e-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-160">Close the page.</span></span>
11. <span data-ttu-id="44f2e-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44f2e-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="44f2e-162">تطبيق قالب لإنشاء عرض أسعار جماعي</span><span class="sxs-lookup"><span data-stu-id="44f2e-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="44f2e-163">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > تحديث عرض الأسعار > إنشاء شامل لعروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="44f2e-164">في الحقل "نوع الحساب"، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="44f2e-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="44f2e-165">في الحقل "معرف المجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="44f2e-166">في الحقل "اسم القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44f2e-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="44f2e-167">في الحقل "أسلوب الحساب"، حدد "استناداً إلى قيم القالب".</span><span class="sxs-lookup"><span data-stu-id="44f2e-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="44f2e-168">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="44f2e-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="44f2e-169">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="44f2e-169">Click Filter.</span></span>
8. <span data-ttu-id="44f2e-170">في الحقل "المعايير"، قم بتعيين عامل تصفية لتغطية مجموعة من العملاء ترغب في تضمينهم في إنشاء عرض الأسعار الجماعي هذا.</span><span class="sxs-lookup"><span data-stu-id="44f2e-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="44f2e-171">واستخدم التنسيق التالي "Customer1..CustomerN.</span><span class="sxs-lookup"><span data-stu-id="44f2e-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="44f2e-172">على سبيل المثال، يمكنك تعيين عامل التصفية على: الولايات المتحدة-001... الولايات المتحدة-004</span><span class="sxs-lookup"><span data-stu-id="44f2e-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="44f2e-173">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="44f2e-173">Click OK.</span></span>
10. <span data-ttu-id="44f2e-174">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="44f2e-174">Click OK.</span></span>
11. <span data-ttu-id="44f2e-175">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="44f2e-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="44f2e-176">تحقق أنه قد تم إنشاء عروض أسعار لجميع العملاء المحددين في روتين التحديث الجماعي، باعتماد ذلك على القالب المحدد.</span><span class="sxs-lookup"><span data-stu-id="44f2e-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


