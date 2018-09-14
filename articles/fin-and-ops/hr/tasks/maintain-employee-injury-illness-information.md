--- 
title: "الاحتفاظ بمعلومات إصابة ومرض الموظف"
description: "يوصى باستكمال دليل مهمة \"إعداد الإصابات والأمراض\" أولاً، نظرًا لاستخدام بعض معلومات الإعداد هنا."
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 03d1e7f7b648e65cbe628aa4ff8b39dfa03ce96b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="08043-103">الاحتفاظ بمعلومات إصابة ومرض الموظف</span><span class="sxs-lookup"><span data-stu-id="08043-103">Maintain employee injury and illness information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08043-104">يوصى باستكمال دليل مهمة "إعداد الإصابات والأمراض" أولاً، نظرًا لاستخدام بعض معلومات الإعداد هنا.</span><span class="sxs-lookup"><span data-stu-id="08043-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="08043-105">يغطي تسجيل المهمة هذا الخطوات الأساسية لإنشاء حالة الإصابة أو المرض.</span><span class="sxs-lookup"><span data-stu-id="08043-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="08043-106">بالإضافة إلى تتبع تفاصيل الإصابة أو المرض، هناك حالة مشكلة يتم تتبعها أيضًا.</span><span class="sxs-lookup"><span data-stu-id="08043-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="08043-107">يتم تعيين الحالة الافتراضية للمشكلة بالوضع "مفتوحة".</span><span class="sxs-lookup"><span data-stu-id="08043-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="08043-108">يمكن إدارة الحالات من عنصر القائمة "حالة المشكلة" في شريط التطبيق في الجزء العلوي من النموذج.</span><span class="sxs-lookup"><span data-stu-id="08043-108">The statuses can be managed from the 'Case status' menu item in the application bar at the top of the form.</span></span>

1. <span data-ttu-id="08043-109">انتقل إلى الموارد البشرية > العمال > الإصابة والمرض > حوادث الإصابة أو المرض.</span><span class="sxs-lookup"><span data-stu-id="08043-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="08043-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="08043-110">Click New.</span></span>
3. <span data-ttu-id="08043-111">في حقل "وصف المشكلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="08043-112">مثال: إصابة المعصم</span><span class="sxs-lookup"><span data-stu-id="08043-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="08043-113">في حقل "العامل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-114">مثال: أحمد بارنيت</span><span class="sxs-lookup"><span data-stu-id="08043-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="08043-115">في حقل "تاريخ ووقت الحادث"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="08043-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="08043-116">مثال: 1/20/2016 10:00 صباحًا</span><span class="sxs-lookup"><span data-stu-id="08043-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="08043-117">في حقل "نوع الإصابة أو المرض"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-118">على سبيل المثال: كسر</span><span class="sxs-lookup"><span data-stu-id="08043-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="08043-119">في حقل "‏‫جزء الجسم‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-120">على سبيل المثال: المعصم</span><span class="sxs-lookup"><span data-stu-id="08043-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="08043-121">في حقل "نوع الناتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-122">على سبيل المثال: العلاج</span><span class="sxs-lookup"><span data-stu-id="08043-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="08043-123">في حقل "التاريخ والوقت المبلغ عنهما"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="08043-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="08043-124">يجب أن يكون التاريخ والوقت المبلغ عنهم لاحقين لتاريخ ووقت الحدث.</span><span class="sxs-lookup"><span data-stu-id="08043-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="08043-125">في حقل "الشخص الذي قام بالإبلاغ عن المشكلة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-126">وهذا يمكن أن يكون الموظف أو شاهد آخر على الحادث.</span><span class="sxs-lookup"><span data-stu-id="08043-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="08043-127">مثال: أحمد بارنيت</span><span class="sxs-lookup"><span data-stu-id="08043-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="08043-128">قم بتوسيع قسم الحادث.</span><span class="sxs-lookup"><span data-stu-id="08043-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="08043-129">في حقل "مكان وقوع الحادث"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="08043-130">مثال: المستودع</span><span class="sxs-lookup"><span data-stu-id="08043-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="08043-131">حدد "نعم" في حقل "في أماكن العمل‬".</span><span class="sxs-lookup"><span data-stu-id="08043-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="08043-132">إذا وقع الحادث في أماكن العمل، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="08043-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="08043-133">في حقل "تاريخ ووقت بدأ العمل"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="08043-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="08043-134">أدخل التاريخ والوقت اللذين أثرا على الشخص الذي بدأ العمل، قبل وقوع الحادث.</span><span class="sxs-lookup"><span data-stu-id="08043-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="08043-135">في حقل وظيفة الموظف أو مهمته، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="08043-136">أدخل الوظيفة أو المهمة التي كان يؤديها العامل عند وقوع الحادث.</span><span class="sxs-lookup"><span data-stu-id="08043-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="08043-137">مثال: تحميل الصناديق</span><span class="sxs-lookup"><span data-stu-id="08043-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="08043-138">في حقل "سبب الحادث"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="08043-139">أدخل سبب الحادث.</span><span class="sxs-lookup"><span data-stu-id="08043-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="08043-140">مثال: الانزلاق على أرض رطبة</span><span class="sxs-lookup"><span data-stu-id="08043-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="08043-141">في حقل "مستوى الشدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="08043-142">في حقل "‏‫الإجراء المطلوب اتخاذه"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="08043-143">مثال: تنظيف البقع فورًا</span><span class="sxs-lookup"><span data-stu-id="08043-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="08043-144">في حقل "‏‫أيام الانقطاع عن العمل المتوقعة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="08043-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="08043-145">أدخل عدد الأيام التي يتوقع أن ينقطع فيها هذا الشخص عن العمل.</span><span class="sxs-lookup"><span data-stu-id="08043-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="08043-146">بمجرد عودة هذا الشخص للعمل، قم بتحديث الحقل "أيام الانقطاع عن العمل" بالعدد الفعلي للأيام التي انقطع فيها عن العمل.</span><span class="sxs-lookup"><span data-stu-id="08043-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="08043-147">قم بتوسيع قسم "تكاليف الإصابة أو المرض".</span><span class="sxs-lookup"><span data-stu-id="08043-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="08043-148">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="08043-148">Click Add.</span></span>
22. <span data-ttu-id="08043-149">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="08043-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="08043-150">في حقل "نوع التكلفة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-151">مثال: العلاج    يمكنك أيضًا إدخال المبلغ، وإرفاق أي وثائق داعمة مثل الفواتير أو ملاحظات الطبيب إلى بند التكلفة.</span><span class="sxs-lookup"><span data-stu-id="08043-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="08043-152">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="08043-152">Click Add.</span></span>
25. <span data-ttu-id="08043-153">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="08043-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="08043-154">في حقل "نوع التكلفة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-155">مثال: الطبيب</span><span class="sxs-lookup"><span data-stu-id="08043-155">Example: Doctor</span></span>  
27. <span data-ttu-id="08043-156">قم بتوسيع قسم "علاجات الإصابة أو المرض".</span><span class="sxs-lookup"><span data-stu-id="08043-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="08043-157">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="08043-157">Click Add.</span></span>
29. <span data-ttu-id="08043-158">في حقل "تاريخ العلاج"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="08043-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="08043-159">في حقل "نوع العلاج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08043-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="08043-160">مثال: جبيرة</span><span class="sxs-lookup"><span data-stu-id="08043-160">Example:  Splint</span></span>  
31. <span data-ttu-id="08043-161">بشكل اختياري، قم بتعيين قسم "‏‫زيارة حجرة الطوارئ بالمستشفى‬" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="08043-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="08043-162">في حقل "‏‫تعليقات العلاج‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="08043-163">مثال: جبيرة لمدة أسبوعين</span><span class="sxs-lookup"><span data-stu-id="08043-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="08043-164">في حقل "اسم الطبيب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="08043-165">مثال: الطبيب. أندرسون</span><span class="sxs-lookup"><span data-stu-id="08043-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="08043-166">في حقل "‏‫موقع ومنشأة العلاج"، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="08043-167">مثال: شارع إلم. حالة طوارئ</span><span class="sxs-lookup"><span data-stu-id="08043-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="08043-168">في حقل "‏‫تفاصيل العلاج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08043-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="08043-169">مثال: الأشعة السينية تؤكد وجود كسر، وارتداء جبيرة</span><span class="sxs-lookup"><span data-stu-id="08043-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="08043-170">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="08043-170">Click Save.</span></span>
    * <span data-ttu-id="08043-171">يمكن تحديث حالة المشكلة في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="08043-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="08043-172">تعيين الحالة إلى قيد التنفيذ، إذا كانت معالجة الإصابة أو المرض قيد التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="08043-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="08043-173">وبمجرد إغلاق الحادث، لا يمكنك إلا إضافة أو حذف التكاليف أو العلاج أو الإيداعات المتعلقة بالحادث.</span><span class="sxs-lookup"><span data-stu-id="08043-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="08043-174">لتعديل معلومات أخرى، قم بإعادة فتح القضية.</span><span class="sxs-lookup"><span data-stu-id="08043-174">To modify other information, reopen the case.</span></span>  


