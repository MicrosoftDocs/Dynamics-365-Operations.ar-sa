--- 
title: "تعيين نماذج لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a3eafa7b66dcc0c2481d7eeaf98bed7f58e4be33
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="83315-103">تعيين نماذج لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="83315-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83315-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="83315-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="83315-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="83315-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="83315-106">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1: تصميم نموذج البيانات)‬".</span><span class="sxs-lookup"><span data-stu-id="83315-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="83315-107">إضافة مصادر البيانات المطلوبة إلى تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="83315-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="83315-108">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="83315-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="83315-109">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="83315-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="83315-110">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="83315-110">Click Designer.</span></span>
4. <span data-ttu-id="83315-111">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="83315-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="83315-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="83315-112">Click New.</span></span>
6. <span data-ttu-id="83315-113">في حقل "التعريف"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="83315-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="83315-114">في حقل "الاسم"، اكتب "تعيين بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="83315-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="83315-115">في حقل "الوصف"، اكتب "تعيين بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="83315-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="83315-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="83315-116">Click Save.</span></span>
10. <span data-ttu-id="83315-117">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="83315-117">Click Designer.</span></span>
11. <span data-ttu-id="83315-118">في الشجرة، حدد "Dynamics 365 for Operations\جدول".</span><span class="sxs-lookup"><span data-stu-id="83315-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="83315-119">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="83315-119">Click Add root.</span></span>
13. <span data-ttu-id="83315-120">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="83315-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="83315-121">في الحقل "الجدول"، اكتب "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="83315-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="83315-122">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="83315-122">Click OK.</span></span>
16. <span data-ttu-id="83315-123">في الشجرة، حدد "الوظائف\تفاصيل الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="83315-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="83315-124">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="83315-124">Click Add root.</span></span>
    * <span data-ttu-id="83315-125">يحدد مصدر البيانات هذا كيف سيتم تحديد نطاق الأبعاد المالية لأي تقرير سيستخدم هذا النموذج كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="83315-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="83315-126">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="83315-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="83315-127">حدد "نعم" في حقل "طلب الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="83315-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="83315-128">حدد "نعم" للسماح للمستخدم بتحديد الأبعاد في وقت التشغيل على نموذج مربع حوار "المستخدم".</span><span class="sxs-lookup"><span data-stu-id="83315-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="83315-129">إذا تم تعيين هذا الخيار إلى "لا"، فسيتم استخدام كافة الأبعاد المالية للمثيل الحالي بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="83315-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="83315-130">في الحقل "تحديد الأبعاد المالية"، حدد "الكيان القانوني".</span><span class="sxs-lookup"><span data-stu-id="83315-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="83315-131">حدد "الكل" للسماح للمستخدم بتحديد الأبعاد المطلوبة للمثيل الحالي في حقل "البحث".</span><span class="sxs-lookup"><span data-stu-id="83315-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="83315-132">حدد "الكيان القانوني" للسماح للمستخدم بتحديد الأبعاد الخاصة بالشركة في حقل "البحث".</span><span class="sxs-lookup"><span data-stu-id="83315-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="83315-133">حدد "البُعد" للسماح للمستخدم بتحديد الأبعاد باستخدام مجموعة أبعاد واحدة.</span><span class="sxs-lookup"><span data-stu-id="83315-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="83315-134">حدد "نعم" في حقل "طلب الحساب الرئيسي".</span><span class="sxs-lookup"><span data-stu-id="83315-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="83315-135">عيّن "طلب الحساب الرئيسي" إلى "نعم" للسماح للمستخدمين بتحديد الحساب الرئيسي كجزء من قائمة الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="83315-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="83315-136">إذا تم تعيين هذا الخيار إلى "لا"، فلن يتم تضمين الحساب الرئيسي في قائمة الأبعاد وسيتم تمكين الخيار "الحساب الرئيسي إلزامي".</span><span class="sxs-lookup"><span data-stu-id="83315-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="83315-137">إذا تم تعيين الخيار "الحساب الرئيسي إلزامي" إلى "نعم"، فسيتم تضمين الحساب الرئيسي في قائمة الأبعاد بغض النظر عن التحديد الذي أجراه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="83315-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="83315-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83315-138">Click OK.</span></span>
23. <span data-ttu-id="83315-139">في الشجرة، حدد "Dynamics 365 for Operations\سجلات جدول".</span><span class="sxs-lookup"><span data-stu-id="83315-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="83315-140">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="83315-140">Click Add root.</span></span>
25. <span data-ttu-id="83315-141">في حقل "الاسم"، اكتب "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="83315-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="83315-142">حدد "نعم" في حقل "طلب الاستعلام".</span><span class="sxs-lookup"><span data-stu-id="83315-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="83315-143">في الحقل "الجدول"، اكتب "LedgerJournalTable".</span><span class="sxs-lookup"><span data-stu-id="83315-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="83315-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83315-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="83315-145">تعيين عناصر نموذج البيانات إلى مصادر بيانات مضافة</span><span class="sxs-lookup"><span data-stu-id="83315-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="83315-146">في الشجرة، قم بتوسيع "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="83315-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="83315-147">في الشجرة، قم بتوسيع "دفتر اليومية\الحركة".</span><span class="sxs-lookup"><span data-stu-id="83315-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="83315-148">في الشجرة، قم بتوسيع "دفتر اليومية\الحركة\بيانات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="83315-149">في الشجرة، قم بتوسيع "إعداد الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="83315-150">في الشجرة، قم بتوسيع "LedgerJournal''.</span><span class="sxs-lookup"><span data-stu-id="83315-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="83315-151">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات".</span><span class="sxs-lookup"><span data-stu-id="83315-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="83315-152">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="83315-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="83315-153">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الإيصال".</span><span class="sxs-lookup"><span data-stu-id="83315-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="83315-154">في الشجرة، حدد "دفتر اليومية\الحركة\الإيصال".</span><span class="sxs-lookup"><span data-stu-id="83315-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="83315-155">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-155">Click Bind.</span></span>
11. <span data-ttu-id="83315-156">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="83315-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="83315-157">لاحظ أنه بالنسبة إلى أي مرجع يتم تعيين الأبعاد المالية إليه، على سبيل المثال LedgerDimension، يتوفر بند مصدر بيانات مناظر (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="83315-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="83315-158">يوفر عنصر مصدر البيانات هذا الأبعاد المالية الخاصة بمجموعة الأبعاد تلك كقائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="83315-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="83315-159">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="83315-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="83315-160">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="83315-161">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة'.</span><span class="sxs-lookup"><span data-stu-id="83315-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="83315-162">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\التعريف".</span><span class="sxs-lookup"><span data-stu-id="83315-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="83315-163">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\التعريف\الاسم".</span><span class="sxs-lookup"><span data-stu-id="83315-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="83315-164">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="83315-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="83315-165">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-165">Click Bind.</span></span>
19. <span data-ttu-id="83315-166">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة\الوصف".</span><span class="sxs-lookup"><span data-stu-id="83315-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="83315-167">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الوصف".</span><span class="sxs-lookup"><span data-stu-id="83315-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="83315-168">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-168">Click Bind.</span></span>
22. <span data-ttu-id="83315-169">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة\الكود".</span><span class="sxs-lookup"><span data-stu-id="83315-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="83315-170">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الكود".</span><span class="sxs-lookup"><span data-stu-id="83315-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="83315-171">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-171">Click Bind.</span></span>
25. <span data-ttu-id="83315-172">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="83315-173">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="83315-174">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-174">Click Bind.</span></span>
28. <span data-ttu-id="83315-175">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الدين(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="83315-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="83315-176">في الشجرة، حدد "دفتر اليومية\الحركة\الدين".</span><span class="sxs-lookup"><span data-stu-id="83315-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="83315-177">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-177">Click Bind.</span></span>
31. <span data-ttu-id="83315-178">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\التاريخ(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="83315-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="83315-179">في الشجرة، حدد "دفتر اليومية\الحركة\التاريخ".</span><span class="sxs-lookup"><span data-stu-id="83315-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="83315-180">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-180">Click Bind.</span></span>
34. <span data-ttu-id="83315-181">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\العملة(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="83315-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="83315-182">في الشجرة، حدد "دفتر اليومية\الحركة\العملة".</span><span class="sxs-lookup"><span data-stu-id="83315-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="83315-183">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-183">Click Bind.</span></span>
37. <span data-ttu-id="83315-184">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الائتمان(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="83315-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="83315-185">في الشجرة، حدد "دفتر اليومية\الحركة\الائتمان".</span><span class="sxs-lookup"><span data-stu-id="83315-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="83315-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-186">Click Bind.</span></span>
40. <span data-ttu-id="83315-187">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="83315-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="83315-188">في الشجرة، حدد "دفتر اليومية\الحركة".</span><span class="sxs-lookup"><span data-stu-id="83315-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="83315-189">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-189">Click Bind.</span></span>
43. <span data-ttu-id="83315-190">في الشجرة، حدد 'LedgerJournal\رقم دُفعة دفتر اليومية‬(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="83315-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="83315-191">في الشجرة، حدد "دفتر اليومية\الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="83315-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="83315-192">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-192">Click Bind.</span></span>
46. <span data-ttu-id="83315-193">في الشجرة، حدد "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="83315-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="83315-194">في الشجرة، حدد "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="83315-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="83315-195">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-195">Click Bind.</span></span>
49. <span data-ttu-id="83315-196">في الشجرة، قم بتوسيع "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="83315-197">في الشجرة، قم بتوسيع "الأبعاد\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="83315-198">في الشجرة، قم بتوسيع "الأبعاد\الحساب الرئيسي والأبعاد\التعريف".</span><span class="sxs-lookup"><span data-stu-id="83315-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="83315-199">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد\التعريف\الاسم".</span><span class="sxs-lookup"><span data-stu-id="83315-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="83315-200">في الشجرة، حدد "إعداد الأبعاد\الكود".</span><span class="sxs-lookup"><span data-stu-id="83315-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="83315-201">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-201">Click Bind.</span></span>
55. <span data-ttu-id="83315-202">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد\التعريف\اسم عمود التقرير‬".</span><span class="sxs-lookup"><span data-stu-id="83315-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="83315-203">في الشجرة، حدد "إعداد الأبعاد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="83315-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="83315-204">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-204">Click Bind.</span></span>
58. <span data-ttu-id="83315-205">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="83315-206">في الشجرة، حدد "إعداد الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="83315-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="83315-207">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83315-207">Click Bind.</span></span>
61. <span data-ttu-id="83315-208">في الشجرة، حدد "الشركة".</span><span class="sxs-lookup"><span data-stu-id="83315-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="83315-209">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="83315-209">Click Edit.</span></span>
63. <span data-ttu-id="83315-210">في الحقل expressionAsStringText، أدخل 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="83315-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="83315-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="83315-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="83315-212">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="83315-212">Click Save.</span></span>
65. <span data-ttu-id="83315-213">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="83315-213">Close the page.</span></span>
66. <span data-ttu-id="83315-214">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="83315-214">Click Save.</span></span>
67. <span data-ttu-id="83315-215">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="83315-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="83315-216">إكمال إصدار نموذج المسودة هذا</span><span class="sxs-lookup"><span data-stu-id="83315-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="83315-217">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="83315-217">Close the page.</span></span>
2. <span data-ttu-id="83315-218">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="83315-218">Close the page.</span></span>
3. <span data-ttu-id="83315-219">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="83315-219">Click Change status.</span></span>
4. <span data-ttu-id="83315-220">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="83315-220">Click Complete.</span></span>
5. <span data-ttu-id="83315-221">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83315-221">Click OK.</span></span>


