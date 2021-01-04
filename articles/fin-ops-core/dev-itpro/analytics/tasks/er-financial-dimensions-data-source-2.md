---
title: "\"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2 - تعيين النموذج)"
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3214ddb1e077d889fb7b785bee2554b96c3907ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681675"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="cfa6c-103">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2 - تعيين النموذج)</span><span class="sxs-lookup"><span data-stu-id="cfa6c-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfa6c-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="cfa6c-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="cfa6c-106">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1: تصميم نموذج البيانات)‬".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="cfa6c-107">إضافة مصادر البيانات المطلوبة إلى تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="cfa6c-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="cfa6c-108">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="cfa6c-109">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="cfa6c-110">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-110">Click Designer.</span></span>
4. <span data-ttu-id="cfa6c-111">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="cfa6c-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-112">Click New.</span></span>
6. <span data-ttu-id="cfa6c-113">في حقل "التعريف"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="cfa6c-114">في حقل "الاسم"، اكتب "تعيين بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="cfa6c-115">في حقل "الوصف"، اكتب "تعيين بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="cfa6c-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-116">Click Save.</span></span>
10. <span data-ttu-id="cfa6c-117">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-117">Click Designer.</span></span>
11. <span data-ttu-id="cfa6c-118">في الشجرة، حدد "Dynamics 365 for Operations\الجدول".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="cfa6c-119">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-119">Click Add root.</span></span>
13. <span data-ttu-id="cfa6c-120">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="cfa6c-121">في الحقل "الجدول"، اكتب "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="cfa6c-122">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-122">Click OK.</span></span>
16. <span data-ttu-id="cfa6c-123">في الشجرة، حدد "الوظائف\تفاصيل الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="cfa6c-124">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-124">Click Add root.</span></span>
    * <span data-ttu-id="cfa6c-125">يحدد مصدر البيانات هذا كيف سيتم تحديد نطاق الأبعاد المالية لأي تقرير سيستخدم هذا النموذج كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="cfa6c-126">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="cfa6c-127">حدد "نعم" في حقل "طلب الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="cfa6c-128">حدد "نعم" للسماح للمستخدم بتحديد الأبعاد في وقت التشغيل على نموذج مربع حوار "المستخدم".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="cfa6c-129">إذا تم تعيين هذا الخيار إلى "لا"، فسيتم استخدام كافة الأبعاد المالية للمثيل الحالي بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="cfa6c-130">في الحقل "تحديد الأبعاد المالية"، حدد "الكيان القانوني".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="cfa6c-131">حدد "الكل" للسماح للمستخدم بتحديد الأبعاد المطلوبة للمثيل الحالي في حقل "البحث".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="cfa6c-132">حدد "الكيان القانوني" للسماح للمستخدم بتحديد الأبعاد الخاصة بالشركة في حقل "البحث".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="cfa6c-133">حدد "البُعد" للسماح للمستخدم بتحديد الأبعاد باستخدام مجموعة أبعاد واحدة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="cfa6c-134">حدد "نعم" في حقل "طلب الحساب الرئيسي".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="cfa6c-135">عيّن "طلب الحساب الرئيسي" إلى "نعم" للسماح للمستخدمين بتحديد الحساب الرئيسي كجزء من قائمة الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="cfa6c-136">إذا تم تعيين هذا الخيار إلى "لا"، فلن يتم تضمين الحساب الرئيسي في قائمة الأبعاد وسيتم تمكين الخيار "الحساب الرئيسي إلزامي".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="cfa6c-137">إذا تم تعيين الخيار "الحساب الرئيسي إلزامي" إلى "نعم"، فسيتم تضمين الحساب الرئيسي في قائمة الأبعاد بغض النظر عن التحديد الذي أجراه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="cfa6c-138">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-138">Click OK.</span></span>
<span data-ttu-id="cfa6c-139">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="cfa6c-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="cfa6c-140">في الشجرة، حدد "Dynamics 365 for Operations\سجلات الجدول".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="cfa6c-141">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-141">Click Add root.</span></span>
25. <span data-ttu-id="cfa6c-142">في حقل "الاسم"، اكتب "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="cfa6c-143">حدد "نعم" في حقل "طلب الاستعلام".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="cfa6c-144">في الحقل "الجدول"، اكتب "LedgerJournalTable".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="cfa6c-145">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-145">Click OK.</span></span>
<span data-ttu-id="cfa6c-146">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="cfa6c-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="cfa6c-147">تعيين عناصر نموذج البيانات إلى مصادر بيانات مضافة</span><span class="sxs-lookup"><span data-stu-id="cfa6c-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="cfa6c-148">في الشجرة، قم بتوسيع "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="cfa6c-149">في الشجرة، قم بتوسيع "دفتر اليومية\الحركة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="cfa6c-150">في الشجرة، قم بتوسيع "دفتر اليومية\الحركة\بيانات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="cfa6c-151">في الشجرة، قم بتوسيع "إعداد الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="cfa6c-152">في الشجرة، قم بتوسيع "LedgerJournal''.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="cfa6c-153">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="cfa6c-154">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="cfa6c-155">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الإيصال".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="cfa6c-156">في الشجرة، حدد "دفتر اليومية\الحركة\الإيصال".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="cfa6c-157">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-157">Click Bind.</span></span>
11. <span data-ttu-id="cfa6c-158">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="cfa6c-159">لاحظ أنه بالنسبة إلى أي مرجع يتم تعيين الأبعاد المالية إليه، على سبيل المثال LedgerDimension، يتوفر بند مصدر بيانات مناظر (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="cfa6c-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="cfa6c-160">يوفر عنصر مصدر البيانات هذا الأبعاد المالية الخاصة بمجموعة الأبعاد تلك كقائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="cfa6c-161">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="cfa6c-162">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="cfa6c-163">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة'.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="cfa6c-164">في الشجرة، قم بتوسيع "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\التعريف".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="cfa6c-165">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\التعريف\الاسم".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="cfa6c-166">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="cfa6c-167">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-167">Click Bind.</span></span>
19. <span data-ttu-id="cfa6c-168">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة\الوصف".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="cfa6c-169">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الوصف".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="cfa6c-170">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-170">Click Bind.</span></span>
22. <span data-ttu-id="cfa6c-171">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد\القيمة\الكود".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="cfa6c-172">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد\الكود".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="cfa6c-173">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-173">Click Bind.</span></span>
25. <span data-ttu-id="cfa6c-174">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="cfa6c-175">في الشجرة، حدد "دفتر اليومية\الحركة\بيانات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="cfa6c-176">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-176">Click Bind.</span></span>
<span data-ttu-id="cfa6c-177">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="cfa6c-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="cfa6c-178">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الدين(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="cfa6c-179">في الشجرة، حدد "دفتر اليومية\الحركة\الدين".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="cfa6c-180">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-180">Click Bind.</span></span>
31. <span data-ttu-id="cfa6c-181">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\التاريخ(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="cfa6c-182">في الشجرة، حدد "دفتر اليومية\الحركة\التاريخ".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="cfa6c-183">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-183">Click Bind.</span></span>
34. <span data-ttu-id="cfa6c-184">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\العملة(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="cfa6c-185">في الشجرة، حدد "دفتر اليومية\الحركة\العملة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="cfa6c-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-186">Click Bind.</span></span>
37. <span data-ttu-id="cfa6c-187">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans\الائتمان(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="cfa6c-188">في الشجرة، حدد "دفتر اليومية\الحركة\الائتمان".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="cfa6c-189">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-189">Click Bind.</span></span>
40. <span data-ttu-id="cfa6c-190">في الشجرة، حدد "LedgerJournal\<العلاقات\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="cfa6c-191">في الشجرة، حدد "دفتر اليومية\الحركة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="cfa6c-192">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-192">Click Bind.</span></span>
43. <span data-ttu-id="cfa6c-193">في الشجرة، حدد 'LedgerJournal\رقم دُفعة دفتر اليومية‬(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="cfa6c-194">في الشجرة، حدد "دفتر اليومية\الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="cfa6c-195">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-195">Click Bind.</span></span>
46. <span data-ttu-id="cfa6c-196">في الشجرة، حدد "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="cfa6c-197">في الشجرة، حدد "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="cfa6c-198">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-198">Click Bind.</span></span>
49. <span data-ttu-id="cfa6c-199">في الشجرة، قم بتوسيع "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="cfa6c-200">في الشجرة، قم بتوسيع "الأبعاد\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="cfa6c-201">في الشجرة، قم بتوسيع "الأبعاد\الحساب الرئيسي والأبعاد\التعريف".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="cfa6c-202">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد\التعريف\الاسم".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="cfa6c-203">في الشجرة، حدد "إعداد الأبعاد\الكود".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="cfa6c-204">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-204">Click Bind.</span></span>
55. <span data-ttu-id="cfa6c-205">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد\التعريف\اسم عمود التقرير‬".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="cfa6c-206">في الشجرة، حدد "إعداد الأبعاد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="cfa6c-207">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-207">Click Bind.</span></span>
58. <span data-ttu-id="cfa6c-208">في الشجرة، حدد "الأبعاد\الحساب الرئيسي والأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="cfa6c-209">في الشجرة، حدد "إعداد الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="cfa6c-210">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-210">Click Bind.</span></span>
61. <span data-ttu-id="cfa6c-211">في الشجرة، حدد "الشركة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="cfa6c-212">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-212">Click Edit.</span></span>
63. <span data-ttu-id="cfa6c-213">في الحقل expressionAsStringText، أدخل 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="cfa6c-214">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="cfa6c-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="cfa6c-215">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-215">Click Save.</span></span>
<span data-ttu-id="cfa6c-216">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="cfa6c-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="cfa6c-217">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-217">Close the page.</span></span>
66. <span data-ttu-id="cfa6c-218">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-218">Click Save.</span></span>
67. <span data-ttu-id="cfa6c-219">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="cfa6c-220">إكمال إصدار نموذج المسودة هذا</span><span class="sxs-lookup"><span data-stu-id="cfa6c-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="cfa6c-221">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-221">Close the page.</span></span>
2. <span data-ttu-id="cfa6c-222">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-222">Close the page.</span></span>
3. <span data-ttu-id="cfa6c-223">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-223">Click Change status.</span></span>
4. <span data-ttu-id="cfa6c-224">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="cfa6c-224">Click Complete.</span></span>
5. <span data-ttu-id="cfa6c-225">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-225">Click OK.</span></span>
<span data-ttu-id="cfa6c-226">![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="cfa6c-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
