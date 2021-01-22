---
title: فائدة العملية
description: يوضح هذا الإجراء كيفية إنشاء إشعارات الفوائد وطباعتها وترحيلها.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140135"
---
# <a name="process-interest"></a><span data-ttu-id="9269b-103">فائدة العملية</span><span class="sxs-lookup"><span data-stu-id="9269b-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9269b-104">يوضح هذا الإجراء كيفية إنشاء إشعارات الفوائد وطباعتها وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="9269b-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="9269b-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="9269b-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="9269b-106">إعداد الفائدة على ملف تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="9269b-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="9269b-107">في **جزء التنقل**، انتقل إلى **الوحدات النمطية‬ > عمليات التحصيل والائتمان‬ > الإعداد > ملفات تعريف ترحيل العملاء**.</span><span class="sxs-lookup"><span data-stu-id="9269b-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="9269b-108">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9269b-108">Click **Edit**.</span></span>
3. <span data-ttu-id="9269b-109">على علامة التبويب السريعة **الإعداد**، في حقل **كود الفائدة**، حدد كود الفائدة من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="9269b-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="9269b-110">إذا كنت لا تريد حساب الفائدة للحركات باستخدام ملف تعريف الترحيل هذا، فاترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="9269b-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="9269b-111">تسمح لك علامة التبويب السريعة **تقييد الجدول** بتغيير الطريقة التي تتم بها معالجة الفائدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="9269b-112">إذا تم تعيين هذا الحقل إلى "نعم"، فسيتم حساب الفائدة لملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="9269b-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="9269b-113">حساب الفائدة</span><span class="sxs-lookup"><span data-stu-id="9269b-113">Calculate interest</span></span>
1. <span data-ttu-id="9269b-114">في **جزء التنقل**، انتقل إلى **الوحدات النمطية‬ > عمليات التحصيل والائتمان‬ > الفائدة > إنشاء إشعارات الفائدة‬**.</span><span class="sxs-lookup"><span data-stu-id="9269b-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="9269b-115">يجب تحديد أنواع الحركات التي سيتم حساب الفائدة لها.</span><span class="sxs-lookup"><span data-stu-id="9269b-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="9269b-116">سيتم تضمين كافة الحركات المفتوحة لهذه الأنواع في الحساب.</span><span class="sxs-lookup"><span data-stu-id="9269b-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="9269b-117">إذا قمت بتعيين **الفائدة إلى نعم**، فستحسب الفائدة على الفائدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="9269b-118">قد تحتاج إلى التحقق من القوانين التي تحكم حساب الفائدة على الفائدة قبل تضمين هذه الحركات.</span><span class="sxs-lookup"><span data-stu-id="9269b-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="9269b-119">في الحقل **من تاريخ**، أدخل تاريخًا سيتم حساب الفائدة بدءًا منه.</span><span class="sxs-lookup"><span data-stu-id="9269b-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="9269b-120">إذا لم تحدد **من تاريخ** معينًا، فسيتم عندئذٍ إلغاء كل إشعارات الفوائد‬ غير المرحلة وسيعاد حسابها اعتبارًا من تاريخ الحركة.</span><span class="sxs-lookup"><span data-stu-id="9269b-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="9269b-121">في الحقل **إلى تاريخ**، أدخل تاريخًا سيتم حساب الفائدة وصولاً إليه.</span><span class="sxs-lookup"><span data-stu-id="9269b-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="9269b-122">حدد خيارًا في الحقل **استخدام ملف تعريف الترحيل من‬**.</span><span class="sxs-lookup"><span data-stu-id="9269b-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="9269b-123">هناك ثلاثة خيارات لملفات تعريف الترحيل:</span><span class="sxs-lookup"><span data-stu-id="9269b-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="9269b-124">الحساب – تستخدم ملف تعريف الترحيل الذي تم تعيينه لحساب العميل لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="9269b-125">تحديد – استخدم ملف تعريف الترحيل الذي تحدده في الحقل "ملف تعريف الترحيل".</span><span class="sxs-lookup"><span data-stu-id="9269b-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="9269b-126">الحركة – استخدم ملف تعريف الترحيل الفردي من الحركات التي سيتم حساب الفائدة عليها لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="9269b-127">ستستخدم الحركات التي لم يتم تعيين ملف تعريف ترحيل لها ملف تعريف الترحيل المحدد في الناحية "دفتر الأستاذ وضريبة المبيعات‬" في نموذج "محددات الحسابات المدينة‬".</span><span class="sxs-lookup"><span data-stu-id="9269b-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="9269b-128">وسّع علامة التبويب السريعة **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="9269b-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="9269b-129">انقر فوق **تصفية**.</span><span class="sxs-lookup"><span data-stu-id="9269b-129">Click **Filter**.</span></span>
9. <span data-ttu-id="9269b-130">في حقل **المعايير**، أدخل معرّف العميل.</span><span class="sxs-lookup"><span data-stu-id="9269b-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="9269b-131">على سبيل المثال، أدخل "US-001".</span><span class="sxs-lookup"><span data-stu-id="9269b-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="9269b-132">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9269b-132">Click **OK**.</span></span>
7. <span data-ttu-id="9269b-133">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9269b-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="9269b-134">طباعة إشعارات الفائدة</span><span class="sxs-lookup"><span data-stu-id="9269b-134">Print interest notes</span></span>
1. <span data-ttu-id="9269b-135">في **جزء التنقل**، انتقل إلى **الوحدات النمطية‬ > عمليات التحصيل والائتمان‬ > الفائدة > مراجعة إشعارات الفائدة ومعالجتها‬‬**.</span><span class="sxs-lookup"><span data-stu-id="9269b-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="9269b-136">في الحقل **الحالة**، حدد ‏"تم الإنشاء".</span><span class="sxs-lookup"><span data-stu-id="9269b-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="9269b-137">في الحقل **مطبوع**، حدد 'غير مطبوع'.</span><span class="sxs-lookup"><span data-stu-id="9269b-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="9269b-138">انقر فوق **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="9269b-138">Click **Print**.</span></span>
5. <span data-ttu-id="9269b-139">وسّع علامة التبويب السريعة **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="9269b-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="9269b-140">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9269b-140">Click **OK**.</span></span>
7. <span data-ttu-id="9269b-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9269b-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="9269b-142">ترحيل إشعار الفائدة</span><span class="sxs-lookup"><span data-stu-id="9269b-142">Post the interest note</span></span>
1. <span data-ttu-id="9269b-143">حدد إشعار فائدة جاهزًا للترحيل (يتم إنشاء الحالة).</span><span class="sxs-lookup"><span data-stu-id="9269b-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="9269b-144">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="9269b-144">Click **Post**.</span></span>
3. <span data-ttu-id="9269b-145">أدخل تاريخ الترحيل لإشعار الفائدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="9269b-146">حدد "نعم" لإنشاء حركة دفتر أستاذ عام واحدة لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="9269b-147">إذا لم تحدد "نعم"، فسيتم تجميع الفائدة على كافة إشعارات الفوائد للعميل ثم ترحيلها إلى دفتر الأستاذ العام في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="9269b-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="9269b-148">وسّع علامة التبويب السريعة **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="9269b-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="9269b-149">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9269b-149">Click **OK**.</span></span>
6. <span data-ttu-id="9269b-150">في الحقل **الحالة**، حدد "‏‫مرحّل‬".</span><span class="sxs-lookup"><span data-stu-id="9269b-150">In the **Status** field, select 'Posted'.</span></span>
