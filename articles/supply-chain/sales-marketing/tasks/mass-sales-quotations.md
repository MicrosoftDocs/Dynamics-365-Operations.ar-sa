---
title: إنشاء شامل لعروض أسعار المبيعات
description: يوضح هذا الإجراء كيفية إنشاء عروض أسعار تقدم مجموعة من المنتجات أو الخدمات التي سيتم إرسالها إلى عملاء متعددين بكفاءة.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77f7a2df813eb0bf211b72646c1e99306fdf3f88
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148597"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="c3704-103">إنشاء شامل لعروض أسعار المبيعات</span><span class="sxs-lookup"><span data-stu-id="c3704-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3704-104">يوضح هذا الإجراء كيفية إنشاء عروض أسعار تقدم مجموعة من المنتجات أو الخدمات التي سيتم إرسالها إلى عملاء متعددين بكفاءة.</span><span class="sxs-lookup"><span data-stu-id="c3704-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="c3704-105">يعتمد إنشاء عرض الأسعار الجماعي هذا على قوالب عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="c3704-106">يمكنك تنفيذ هذا الإجراء في البيانات الخاصة بك أو في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c3704-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="c3704-107">إنشاء قالب عروض أسعار</span><span class="sxs-lookup"><span data-stu-id="c3704-107">Create a quotation template</span></span>
1. <span data-ttu-id="c3704-108">انتقل إلى المبيعات والتسويق > الإعداد > عروض الأسعار > مجموعات القوالب.</span><span class="sxs-lookup"><span data-stu-id="c3704-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="c3704-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c3704-109">Click New.</span></span>
3. <span data-ttu-id="c3704-110">في الحقل "معرف المجموعة"، اكتب معرفاً تختاره.</span><span class="sxs-lookup"><span data-stu-id="c3704-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="c3704-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3704-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c3704-112">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c3704-112">Click Save.</span></span>
6. <span data-ttu-id="c3704-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3704-113">Close the page.</span></span>
7. <span data-ttu-id="c3704-114">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="c3704-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c3704-115">Click New.</span></span>
9. <span data-ttu-id="c3704-116">في الحقل "نوع الحساب"، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="c3704-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="c3704-117">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="c3704-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3704-118">Click OK.</span></span>
    * <span data-ttu-id="c3704-119">لكي يصبح عرض الأسعار قالبًا، يجب تنفيذ خطوات الإعداد برأس عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="c3704-120">ويجب إجراء هذا قبل إضافة بنود لعرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="c3704-121">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="c3704-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="c3704-122">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="c3704-122">Click Change view.</span></span>
14. <span data-ttu-id="c3704-123">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="c3704-123">Click Header view.</span></span>
15. <span data-ttu-id="c3704-124">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="c3704-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="c3704-125">في الحقل "معرف المجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="c3704-126">في الحقل "اسم القالب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3704-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="c3704-127">حدد "نعم" في الحقل "نشط".</span><span class="sxs-lookup"><span data-stu-id="c3704-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="c3704-128">يمكن استخدام القوالب النشطة فقط عند تطبيق قالب على عرض أسعار مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="c3704-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="c3704-129">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="c3704-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="c3704-130">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="c3704-130">Click Change view.</span></span>
21. <span data-ttu-id="c3704-131">انقر فوق "عرض البند".</span><span class="sxs-lookup"><span data-stu-id="c3704-131">Click Line view.</span></span>
22. <span data-ttu-id="c3704-132">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="c3704-133">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3704-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="c3704-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3704-134">Close the page.</span></span>
25. <span data-ttu-id="c3704-135">في الحقل "‏‫النسبة المئوية‬ للخصم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c3704-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="c3704-136">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="c3704-136">Click Add line.</span></span>
27. <span data-ttu-id="c3704-137">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="c3704-138">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3704-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="c3704-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3704-139">Close the page.</span></span>
30. <span data-ttu-id="c3704-140">في الحقل "وحدة السعر"، أدخل سعرًا جديدًا أو قم بتغيير السعر الحالي.</span><span class="sxs-lookup"><span data-stu-id="c3704-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="c3704-141">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="c3704-141">Click Add line.</span></span>
32. <span data-ttu-id="c3704-142">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="c3704-143">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3704-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="c3704-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3704-144">Close the page.</span></span>
35. <span data-ttu-id="c3704-145">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c3704-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="c3704-146">في الحقل "الخصم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c3704-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="c3704-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c3704-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="c3704-148">تطبيق القالب لإنشاء عرض أسعار مفرد</span><span class="sxs-lookup"><span data-stu-id="c3704-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="c3704-149">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="c3704-150">لاحظ أن عرض الأسعار الذي قمت بإنشائه للتو ه تم تمييز كـ"قالب".</span><span class="sxs-lookup"><span data-stu-id="c3704-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="c3704-151">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c3704-151">Click New.</span></span>
3. <span data-ttu-id="c3704-152">في الحقل "نوع الحساب"، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="c3704-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="c3704-153">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="c3704-154">قم بتوسيع القسم "القالب".</span><span class="sxs-lookup"><span data-stu-id="c3704-154">Expand the Template section.</span></span>
6. <span data-ttu-id="c3704-155">في الحقل "معرف المجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="c3704-156">في الحقل "اسم القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="c3704-157">في الحقل "أسلوب الحساب"، حدد "استناداً إلى قيم القالب".</span><span class="sxs-lookup"><span data-stu-id="c3704-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="c3704-158">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3704-158">Click OK.</span></span>
    * <span data-ttu-id="c3704-159">تم إنشاء عرض الأسعار الجديد الآن استناداً إلى البيانات وشروط القالب.</span><span class="sxs-lookup"><span data-stu-id="c3704-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="c3704-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3704-160">Close the page.</span></span>
11. <span data-ttu-id="c3704-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3704-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="c3704-162">تطبيق قالب لإنشاء عرض أسعار جماعي</span><span class="sxs-lookup"><span data-stu-id="c3704-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="c3704-163">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > تحديث عرض الأسعار > إنشاء شامل لعروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="c3704-164">في الحقل "نوع الحساب"، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="c3704-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="c3704-165">في الحقل "معرف المجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="c3704-166">في الحقل "اسم القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c3704-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="c3704-167">في الحقل "أسلوب الحساب"، حدد "استناداً إلى قيم القالب".</span><span class="sxs-lookup"><span data-stu-id="c3704-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="c3704-168">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="c3704-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c3704-169">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="c3704-169">Click Filter.</span></span>
8. <span data-ttu-id="c3704-170">في الحقل "المعايير"، قم بتعيين عامل تصفية لتغطية مجموعة من العملاء ترغب في تضمينهم في إنشاء عرض الأسعار الجماعي هذا.</span><span class="sxs-lookup"><span data-stu-id="c3704-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="c3704-171">واستخدم التنسيق التالي "Customer1..CustomerN.</span><span class="sxs-lookup"><span data-stu-id="c3704-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="c3704-172">على سبيل المثال، يمكنك تعيين عامل التصفية على: الولايات المتحدة-001... الولايات المتحدة-004</span><span class="sxs-lookup"><span data-stu-id="c3704-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="c3704-173">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3704-173">Click OK.</span></span>
10. <span data-ttu-id="c3704-174">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3704-174">Click OK.</span></span>
11. <span data-ttu-id="c3704-175">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c3704-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="c3704-176">تحقق أنه قد تم إنشاء عروض أسعار لجميع العملاء المحددين في روتين التحديث الجماعي، باعتماد ذلك على القالب المحدد.</span><span class="sxs-lookup"><span data-stu-id="c3704-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

