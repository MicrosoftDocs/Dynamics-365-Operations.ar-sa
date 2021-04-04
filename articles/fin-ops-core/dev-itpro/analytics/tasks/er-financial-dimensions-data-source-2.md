---
title: "\"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2 - تعيين النموذج)"
description: يوضح هذا الموضوع كيفيه تكوين نموذج التقرير الكتروني (ER) لاستخدام الابعاد المالية كمصدر بيانات لتقارير ER. (جزء 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59f65962ef8f6ae79190b6595a313831eca53830
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570158"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="8b213-104">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2 - تعيين النموذج)</span><span class="sxs-lookup"><span data-stu-id="8b213-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b213-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8b213-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="8b213-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="8b213-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="8b213-107">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1: تصميم نموذج البيانات)‬".</span><span class="sxs-lookup"><span data-stu-id="8b213-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="8b213-108">إضافة مصادر البيانات المطلوبة إلى تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="8b213-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="8b213-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="8b213-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8b213-110">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="8b213-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8b213-111">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="8b213-111">Click Designer.</span></span>
4. <span data-ttu-id="8b213-112">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="8b213-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="8b213-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8b213-113">Click New.</span></span>
6. <span data-ttu-id="8b213-114">في حقل "التعريف"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="8b213-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="8b213-115">في حقل "الاسم"، اكتب "تعيين بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="8b213-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="8b213-116">في حقل "الوصف"، اكتب "تعيين بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="8b213-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="8b213-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8b213-117">Click Save.</span></span>
10. <span data-ttu-id="8b213-118">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="8b213-118">Click Designer.</span></span>
11. <span data-ttu-id="8b213-119">في الشجرة، حدد "Dynamics 365 for Operations\الجدول".</span><span class="sxs-lookup"><span data-stu-id="8b213-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="8b213-120">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="8b213-120">Click Add root.</span></span>
13. <span data-ttu-id="8b213-121">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="8b213-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="8b213-122">في الحقل "الجدول"، اكتب "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="8b213-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="8b213-123">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="8b213-123">Click OK.</span></span>
16. <span data-ttu-id="8b213-124">في الشجرة، حدد "الوظائف\تفاصيل الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="8b213-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="8b213-125">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="8b213-125">Click Add root.</span></span>
    * <span data-ttu-id="8b213-126">يحدد مصدر البيانات هذا كيف سيتم تحديد نطاق الأبعاد المالية لأي تقرير سيستخدم هذا النموذج كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="8b213-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="8b213-127">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8b213-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="8b213-128">حدد "نعم" في حقل "طلب الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="8b213-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="8b213-129">حدد "نعم" للسماح للمستخدم بتحديد الأبعاد في وقت التشغيل على نموذج مربع حوار "المستخدم".</span><span class="sxs-lookup"><span data-stu-id="8b213-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="8b213-130">إذا تم تعيين هذا الخيار إلى "لا"، فسيتم استخدام كافة الأبعاد المالية للمثيل الحالي بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="8b213-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="8b213-131">في الحقل "تحديد الأبعاد المالية"، حدد "الكيان القانوني".</span><span class="sxs-lookup"><span data-stu-id="8b213-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="8b213-132">حدد "الكل" للسماح للمستخدم بتحديد الأبعاد المطلوبة للمثيل الحالي في حقل "البحث".</span><span class="sxs-lookup"><span data-stu-id="8b213-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="8b213-133">حدد "الكيان القانوني" للسماح للمستخدم بتحديد الأبعاد الخاصة بالشركة في حقل "البحث".</span><span class="sxs-lookup"><span data-stu-id="8b213-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="8b213-134">حدد "البُعد" للسماح للمستخدم بتحديد الأبعاد باستخدام مجموعة أبعاد واحدة.</span><span class="sxs-lookup"><span data-stu-id="8b213-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="8b213-135">حدد "نعم" في حقل "طلب الحساب الرئيسي".</span><span class="sxs-lookup"><span data-stu-id="8b213-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="8b213-136">عيّن "طلب الحساب الرئيسي" إلى "نعم" للسماح للمستخدمين بتحديد الحساب الرئيسي كجزء من قائمة الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="8b213-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="8b213-137">إذا تم تعيين هذا الخيار إلى "لا"، فلن يتم تضمين الحساب الرئيسي في قائمة الأبعاد وسيتم تمكين الخيار "الحساب الرئيسي إلزامي".</span><span class="sxs-lookup"><span data-stu-id="8b213-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="8b213-138">إذا تم تعيين الخيار "الحساب الرئيسي إلزامي" إلى "نعم"، فسيتم تضمين الحساب الرئيسي في قائمة الأبعاد بغض النظر عن التحديد الذي أجراه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="8b213-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="8b213-139">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="8b213-139">Click OK.</span></span>
<span data-ttu-id="8b213-140">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="8b213-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="8b213-141">في الشجرة، حدد "Dynamics 365 for Operations\سجلات الجدول".</span><span class="sxs-lookup"><span data-stu-id="8b213-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="8b213-142">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="8b213-142">Click Add root.</span></span>
25. <span data-ttu-id="8b213-143">في حقل "الاسم"، اكتب "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="8b213-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="8b213-144">حدد "نعم" في حقل "طلب الاستعلام".</span><span class="sxs-lookup"><span data-stu-id="8b213-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="8b213-145">في الحقل "الجدول"، اكتب "LedgerJournalTable".</span><span class="sxs-lookup"><span data-stu-id="8b213-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="8b213-146">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="8b213-146">Click OK.</span></span>
<span data-ttu-id="8b213-147">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="8b213-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="8b213-148">تعيين عناصر نموذج البيانات إلى مصادر بيانات مضافة</span><span class="sxs-lookup"><span data-stu-id="8b213-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="8b213-149">في الشجرة، قم بتوسيع "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="8b213-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="8b213-150">في الشجرة، قم بتوسيع "دفتر اليومية\الحركة".</span><span class="sxs-lookup"><span data-stu-id="8b213-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="8b213-151">في الشجرة، قم بتوسيع "دفتر اليومية\الحركة\بيانات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="8b213-152">في الشجرة، قم بتوسيع "إعداد الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="8b213-153">في الشجرة، قم بتوسيع "LedgerJournal''.</span><span class="sxs-lookup"><span data-stu-id="8b213-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="8b213-154">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات".</span><span class="sxs-lookup"><span data-stu-id="8b213-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="8b213-155">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="8b213-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="8b213-156">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الإيصال".</span><span class="sxs-lookup"><span data-stu-id="8b213-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="8b213-157">في الشجرة، حدد "دفتر اليومية\الحركة\الإيصال".</span><span class="sxs-lookup"><span data-stu-id="8b213-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="8b213-158">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-158">Click Bind.</span></span>
11. <span data-ttu-id="8b213-159">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="8b213-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="8b213-160">لاحظ أنه بالنسبة إلى أي مرجع يتم تعيين الأبعاد المالية إليه، على سبيل المثال LedgerDimension، يتوفر بند مصدر بيانات مناظر (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="8b213-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="8b213-161">يوفر عنصر مصدر البيانات هذا الأبعاد المالية الخاصة بمجموعة الأبعاد تلك كقائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="8b213-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="8b213-162">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="8b213-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="8b213-163">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="8b213-164">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة'.</span><span class="sxs-lookup"><span data-stu-id="8b213-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="8b213-165">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\التعريف".</span><span class="sxs-lookup"><span data-stu-id="8b213-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="8b213-166">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\التعريف\الاسم".</span><span class="sxs-lookup"><span data-stu-id="8b213-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="8b213-167">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="8b213-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="8b213-168">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-168">Click Bind.</span></span>
19. <span data-ttu-id="8b213-169">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة\الوصف".</span><span class="sxs-lookup"><span data-stu-id="8b213-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="8b213-170">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الوصف".</span><span class="sxs-lookup"><span data-stu-id="8b213-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="8b213-171">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-171">Click Bind.</span></span>
22. <span data-ttu-id="8b213-172">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة\الكود".</span><span class="sxs-lookup"><span data-stu-id="8b213-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="8b213-173">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الكود".</span><span class="sxs-lookup"><span data-stu-id="8b213-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="8b213-174">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-174">Click Bind.</span></span>
25. <span data-ttu-id="8b213-175">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="8b213-176">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="8b213-177">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-177">Click Bind.</span></span>
<span data-ttu-id="8b213-178">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="8b213-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="8b213-179">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الدين(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="8b213-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="8b213-180">في الشجرة، حدد "دفتر اليومية\الحركة\الدين".</span><span class="sxs-lookup"><span data-stu-id="8b213-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="8b213-181">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-181">Click Bind.</span></span>
31. <span data-ttu-id="8b213-182">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\التاريخ(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="8b213-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="8b213-183">في الشجرة، حدد "دفتر اليومية\الحركة\التاريخ".</span><span class="sxs-lookup"><span data-stu-id="8b213-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="8b213-184">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-184">Click Bind.</span></span>
34. <span data-ttu-id="8b213-185">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\العملة(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="8b213-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="8b213-186">في الشجرة، حدد "دفتر اليومية\الحركة\العملة".</span><span class="sxs-lookup"><span data-stu-id="8b213-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="8b213-187">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-187">Click Bind.</span></span>
37. <span data-ttu-id="8b213-188">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الائتمان(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="8b213-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="8b213-189">في الشجرة، حدد "دفتر اليومية\الحركة\الائتمان".</span><span class="sxs-lookup"><span data-stu-id="8b213-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="8b213-190">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-190">Click Bind.</span></span>
40. <span data-ttu-id="8b213-191">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="8b213-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="8b213-192">في الشجرة، حدد "دفتر اليومية\الحركة".</span><span class="sxs-lookup"><span data-stu-id="8b213-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="8b213-193">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-193">Click Bind.</span></span>
43. <span data-ttu-id="8b213-194">في الشجرة، حدد 'LedgerJournal\رقم دُفعة دفتر اليومية‬(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="8b213-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="8b213-195">في الشجرة، حدد "دفتر اليومية\الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="8b213-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="8b213-196">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-196">Click Bind.</span></span>
46. <span data-ttu-id="8b213-197">في الشجرة، حدد "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="8b213-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="8b213-198">في الشجرة، حدد "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="8b213-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="8b213-199">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-199">Click Bind.</span></span>
49. <span data-ttu-id="8b213-200">في الشجرة، قم بتوسيع "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="8b213-201">في الشجرة، قم بتوسيع "الأبعاد\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="8b213-202">في الشجرة، قم بتوسيع "الأبعاد\الحساب الرئيسي والأبعاد\التعريف".</span><span class="sxs-lookup"><span data-stu-id="8b213-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="8b213-203">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد\التعريف\الاسم".</span><span class="sxs-lookup"><span data-stu-id="8b213-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="8b213-204">في الشجرة، حدد "إعداد الأبعاد\الكود".</span><span class="sxs-lookup"><span data-stu-id="8b213-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="8b213-205">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-205">Click Bind.</span></span>
55. <span data-ttu-id="8b213-206">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد\التعريف\اسم عمود التقرير‬".</span><span class="sxs-lookup"><span data-stu-id="8b213-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="8b213-207">في الشجرة، حدد "إعداد الأبعاد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="8b213-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="8b213-208">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-208">Click Bind.</span></span>
58. <span data-ttu-id="8b213-209">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="8b213-210">في الشجرة، حدد "إعداد الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="8b213-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="8b213-211">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="8b213-211">Click Bind.</span></span>
61. <span data-ttu-id="8b213-212">في الشجرة، حدد "الشركة".</span><span class="sxs-lookup"><span data-stu-id="8b213-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="8b213-213">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="8b213-213">Click Edit.</span></span>
63. <span data-ttu-id="8b213-214">في الحقل expressionAsStringText، أدخل 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="8b213-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="8b213-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="8b213-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="8b213-216">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="8b213-216">Click Save.</span></span>
<span data-ttu-id="8b213-217">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="8b213-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="8b213-218">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b213-218">Close the page.</span></span>
66. <span data-ttu-id="8b213-219">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="8b213-219">Click Save.</span></span>
67. <span data-ttu-id="8b213-220">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b213-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="8b213-221">إكمال إصدار نموذج المسودة هذا</span><span class="sxs-lookup"><span data-stu-id="8b213-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="8b213-222">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b213-222">Close the page.</span></span>
2. <span data-ttu-id="8b213-223">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b213-223">Close the page.</span></span>
3. <span data-ttu-id="8b213-224">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="8b213-224">Click Change status.</span></span>
4. <span data-ttu-id="8b213-225">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="8b213-225">Click Complete.</span></span>
5. <span data-ttu-id="8b213-226">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="8b213-226">Click OK.</span></span>
<span data-ttu-id="8b213-227">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="8b213-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]