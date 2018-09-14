--- 
title: "فائدة العملية"
description: "يوضح هذا الإجراء كيفية إنشاء إشعارات الفوائد وطباعتها وترحيلها."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="process-interest"></a><span data-ttu-id="438dc-103">فائدة العملية</span><span class="sxs-lookup"><span data-stu-id="438dc-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="438dc-104">يوضح هذا الإجراء كيفية إنشاء إشعارات الفوائد وطباعتها وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="438dc-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="438dc-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="438dc-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="438dc-106">إعداد الفائدة على ملف تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="438dc-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="438dc-107">انتقل إلى التحصيلات والائتمان‬ > إعداد > ملفات تعريف ترحيل العميل‬.</span><span class="sxs-lookup"><span data-stu-id="438dc-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="438dc-108">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="438dc-108">Click Edit.</span></span>
    * <span data-ttu-id="438dc-109">حدد إشعار فائدة من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="438dc-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="438dc-110">إذا كنت لا تريد حساب الفائدة للحركات باستخدام ملف تعريف الترحيل هذا، فاترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="438dc-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="438dc-111">تسمح لك علامة التبويب ‏"الجدول" بتغيير الطريقة التي تتم بها معالجة الفائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="438dc-112">إذا تم تعيين هذا الحقل إلى "نعم"، فسيتم حساب الفائدة لملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="438dc-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="438dc-113">حساب الفائدة</span><span class="sxs-lookup"><span data-stu-id="438dc-113">Calculate interest</span></span>
1. <span data-ttu-id="438dc-114">انتقل إلى التحصيلات والائتمان‬ > الفائدة > إنشاء إشعارات الفائدة‬.</span><span class="sxs-lookup"><span data-stu-id="438dc-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="438dc-115">يجب تحديد أنواع الحركات التي سيتم حساب الفائدة لها.</span><span class="sxs-lookup"><span data-stu-id="438dc-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="438dc-116">سيتم تضمين كافة الحركات المفتوحة لهذه الأنواع في الحساب.</span><span class="sxs-lookup"><span data-stu-id="438dc-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="438dc-117">إذا قمت بتحديد "الفائدة"، فستحسب الفائدة على الفائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="438dc-118">قد تحتاج إلى التحقق من القوانين التي تحكم حساب الفائدة على الفائدة قبل تضمين هذه الحركات.</span><span class="sxs-lookup"><span data-stu-id="438dc-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="438dc-119">سيتم حساب الفائدة اعتبارًا من هذا التاريخ حتى "إلى تاريخ".</span><span class="sxs-lookup"><span data-stu-id="438dc-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="438dc-120">إذا لم تحدد "من تاريخ" معينًا، فسيتم عندئذٍ إلغاء كل إشعارات الفوائد‬ غير المرحلة وسيعاد حسابها اعتبارًا من تاريخ الحركة.</span><span class="sxs-lookup"><span data-stu-id="438dc-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="438dc-121">أدخل تاريخ إشعار الفائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="438dc-122">هناك ثلاثة خيارات تتعلق بملف تعريف الترحيل:   الحساب – استخدم ملف تعريف الترحيل الذي تم تعيينه إلى حساب العميل لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="438dc-123">تحديد – استخدم ملف تعريف الترحيل الذي تحدده في الحقل "ملف تعريف الترحيل".</span><span class="sxs-lookup"><span data-stu-id="438dc-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="438dc-124">الحركة – استخدم ملف تعريف الترحيل الفردي من الحركات التي سيتم حساب الفائدة عليها لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="438dc-125">ستستخدم الحركات التي لم يتم تعيين ملف تعريف ترحيل لها ملف تعريف الترحيل المحدد في الناحية "دفتر الأستاذ وضريبة المبيعات‬" في نموذج "محددات الحسابات المدينة‬".</span><span class="sxs-lookup"><span data-stu-id="438dc-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="438dc-126">حدد ملف تعريف ترحيل هنا إذا قمت بتغيير "استخدام ملف تعريف الترحيل من‬" إلى "تحديد".</span><span class="sxs-lookup"><span data-stu-id="438dc-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="438dc-127">قم بتوسيع المقطع "السجلات المطلوب تضمينها‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="438dc-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="438dc-128">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="438dc-128">Click Filter.</span></span>
5. <span data-ttu-id="438dc-129">في الحقل معايير، أدخل "معرف العميل".</span><span class="sxs-lookup"><span data-stu-id="438dc-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="438dc-130">على سبيل المثال، أدخل "US-001".</span><span class="sxs-lookup"><span data-stu-id="438dc-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="438dc-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="438dc-131">Click OK.</span></span>
7. <span data-ttu-id="438dc-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="438dc-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="438dc-133">طباعة إشعارات الفائدة</span><span class="sxs-lookup"><span data-stu-id="438dc-133">Print interest notes</span></span>
1. <span data-ttu-id="438dc-134">انتقل إلى التحصيلات والائتمان‬ > الفائدة > مراجعة إشعارات الفائدة ومعالجتها‬‬.</span><span class="sxs-lookup"><span data-stu-id="438dc-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="438dc-135">في الحقل "الحالة"، حدد "‏‫تم الإنشاء".</span><span class="sxs-lookup"><span data-stu-id="438dc-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="438dc-136">في حقل "الطابعة"، حدد "عدم الطباعة".</span><span class="sxs-lookup"><span data-stu-id="438dc-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="438dc-137">انقر فوق طباعة.</span><span class="sxs-lookup"><span data-stu-id="438dc-137">Click Print.</span></span>
5. <span data-ttu-id="438dc-138">قم بتوسيع المقطع "السجلات المطلوب تضمينها‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="438dc-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="438dc-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="438dc-139">Click OK.</span></span>
7. <span data-ttu-id="438dc-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="438dc-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="438dc-141">ترحيل إشعار الفائدة</span><span class="sxs-lookup"><span data-stu-id="438dc-141">Post the interest note</span></span>
1. <span data-ttu-id="438dc-142">حدد إشعار فائدة جاهزًا للترحيل (يتم إنشاء الحالة).</span><span class="sxs-lookup"><span data-stu-id="438dc-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="438dc-143">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="438dc-143">Click Post.</span></span>
3. <span data-ttu-id="438dc-144">أدخل تاريخ الترحيل لإشعار الفائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="438dc-145">حدد "نعم" لإنشاء حركة دفتر أستاذ عام واحدة لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="438dc-146">إذا لم تحدد "نعم"، فسيتم تجميع الفائدة على كافة إشعارات الفوائد للعميل ثم ترحيلها إلى دفتر الأستاذ العام في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="438dc-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="438dc-147">قم بتوسيع المقطع "السجلات المطلوب تضمينها‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="438dc-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="438dc-148">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="438dc-148">Click OK.</span></span>
6. <span data-ttu-id="438dc-149">في الحقل "الحالة"، حدد "‏‫مرحل‬".</span><span class="sxs-lookup"><span data-stu-id="438dc-149">In the Status field, select 'Posted'.</span></span>


