---
title: تحديد تعيينات نماذج التقارير الإلكترونية وتحديد مصادر بيانات لها
description: تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تحديد مصادر البيانات لنموذج بيانات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d57c191761b8e2367ff8806c1cd98d6d83559e3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682107"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="c3152-103">تحديد تعيينات نماذج التقارير الإلكترونية وتحديد مصادر بيانات لها</span><span class="sxs-lookup"><span data-stu-id="c3152-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3152-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تحديد مصادر البيانات لنموذج بيانات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c3152-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="c3152-105">سيتم ربط مصادر البيانات بالمكونات الفردية لنموذج البيانات المحدد في مرحلة التصميم وسيتم نشر بيانات الأعمال إلى نموذج البيانات المشار إليه في مرحلة التشغيل.</span><span class="sxs-lookup"><span data-stu-id="c3152-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="c3152-106">في هذا المثال، ستحدد مصادر البيانات لنموذج بيانات موجود تم إنشاؤه لشركة عينة، .Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء نموذج بيانات جديد".</span><span class="sxs-lookup"><span data-stu-id="c3152-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="c3152-107">فتح شجرة تكوينات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c3152-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="c3152-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="c3152-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c3152-109">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="c3152-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="c3152-110">إدراج تعيين طراز جديد</span><span class="sxs-lookup"><span data-stu-id="c3152-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="c3152-111">في الشجرة، حدد "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="c3152-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="c3152-112">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="c3152-112">Click Designer.</span></span>
3. <span data-ttu-id="c3152-113">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="c3152-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="c3152-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c3152-114">Click New.</span></span>
    * <span data-ttu-id="c3152-115">سيؤدي ذلك إلى إنشاء سجل جديد سيعين نموذج البيانات إلى مصادر البيانات.</span><span class="sxs-lookup"><span data-stu-id="c3152-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="c3152-116">في هذا المثال، ستعيِّنُ نموذج البيانات إلى مصادر البيانات لنوع الدفع المطلوب: تحويل الائتمان.</span><span class="sxs-lookup"><span data-stu-id="c3152-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="c3152-117">ومن الممكن تصميم أكثر من عملية تعيين واحدة لنموذج بيانات معين.</span><span class="sxs-lookup"><span data-stu-id="c3152-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="c3152-118">على سبيل المثال، يمكنك إنشاء تعيين لأنواع مختلفة من المدفوعات، مثل الدين المباشر أو التحويلات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="c3152-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="c3152-119">في هذا المثال، ستقوم بإنشاء تعيين للتحويلات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="c3152-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="c3152-120">في الحقل "الاسم"، اكتب "تعيين CT".</span><span class="sxs-lookup"><span data-stu-id="c3152-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="c3152-121">تعيين CT</span><span class="sxs-lookup"><span data-stu-id="c3152-121">CT mapping</span></span>  
6. <span data-ttu-id="c3152-122">في حقل الوصف، اكتب "تعيين نموذج الدفع CT".</span><span class="sxs-lookup"><span data-stu-id="c3152-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="c3152-123">تعيين نموذج الدفع</span><span class="sxs-lookup"><span data-stu-id="c3152-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="c3152-124">في حقل التعريف، اكتب 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="c3152-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="c3152-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="c3152-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="c3152-126">حل تغييرات التعريف.</span><span class="sxs-lookup"><span data-stu-id="c3152-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="c3152-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c3152-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="c3152-128">تحديد مصادر البيانات المطلوبة لتعيين النموذج الحالي</span><span class="sxs-lookup"><span data-stu-id="c3152-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="c3152-129">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="c3152-129">Click Designer.</span></span>
2. <span data-ttu-id="c3152-130">في الشجرة، حدد "Dynamics 365 for Operations\سجلات الجدول".</span><span class="sxs-lookup"><span data-stu-id="c3152-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="c3152-131">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="c3152-131">Click Add root.</span></span>
    * <span data-ttu-id="c3152-132">أدخل مصدر هذه البيانات للوصول إلى حركات الدفع.</span><span class="sxs-lookup"><span data-stu-id="c3152-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="c3152-133">في الحقل "الاسم"، اكتب "الحركات".</span><span class="sxs-lookup"><span data-stu-id="c3152-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="c3152-134">الحركات</span><span class="sxs-lookup"><span data-stu-id="c3152-134">Transactions</span></span>  
5. <span data-ttu-id="c3152-135">في الحقل "التسمية"، أدخل "الحركات".</span><span class="sxs-lookup"><span data-stu-id="c3152-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="c3152-136">الحركات</span><span class="sxs-lookup"><span data-stu-id="c3152-136">Transactions</span></span>  
6. <span data-ttu-id="c3152-137">في الحقل "التعليمات"، أدخل "بنود دفتر يومية دفتر الأستاذ".</span><span class="sxs-lookup"><span data-stu-id="c3152-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="c3152-138">بنود دفتر يومية دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="c3152-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="c3152-139">حدد "نعم" في حقل "طلب الاستعلام".</span><span class="sxs-lookup"><span data-stu-id="c3152-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="c3152-140">حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="c3152-140">Select Yes.</span></span>  
8. <span data-ttu-id="c3152-141">في الحقل "الجدول"، اكتب 'LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="c3152-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="c3152-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="c3152-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="c3152-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3152-143">Click OK.</span></span>
    * <span data-ttu-id="c3152-144">حدد الجدول LedgerJournalTrans كمصدر بيانات لنموذج البيانات الحالي.</span><span class="sxs-lookup"><span data-stu-id="c3152-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="c3152-145">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="c3152-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="c3152-146">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c3152-146">Click Add.</span></span>
    * <span data-ttu-id="c3152-147">انقر فوق "إضافة" لإضافة حقل محسوب جديد.</span><span class="sxs-lookup"><span data-stu-id="c3152-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="c3152-148">في الحقل "الاسم"، اكتب "$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="c3152-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="c3152-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="c3152-149">$EndToEndID</span></span>  
13. <span data-ttu-id="c3152-150">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="c3152-150">Click Edit formula.</span></span>
14. <span data-ttu-id="c3152-151">في الشجرة، حدد "سلسلة/تسلسل".</span><span class="sxs-lookup"><span data-stu-id="c3152-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="c3152-152">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="c3152-152">Click Add function.</span></span>
16. <span data-ttu-id="c3152-153">في الشجرة، قم بتوسيع "الحركات".</span><span class="sxs-lookup"><span data-stu-id="c3152-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="c3152-154">في الشجرة، حدد "الحركات/الإيصال".</span><span class="sxs-lookup"><span data-stu-id="c3152-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="c3152-155">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="c3152-155">Click Add data source.</span></span>
19. <span data-ttu-id="c3152-156">في حقل الصيغة، أدخل 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="c3152-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="c3152-157">اكتب [ , "-", ] في نهاية المعادلة.</span><span class="sxs-lookup"><span data-stu-id="c3152-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="c3152-158">في الشجرة، حدد "السلسلة/النص".</span><span class="sxs-lookup"><span data-stu-id="c3152-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="c3152-159">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="c3152-159">Click Add function.</span></span>
22. <span data-ttu-id="c3152-160">في الشجرة، حدد 'Transactions\Record-ID(RecId)'.</span><span class="sxs-lookup"><span data-stu-id="c3152-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="c3152-161">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="c3152-161">Click Add data source.</span></span>
24. <span data-ttu-id="c3152-162">في حقل الصيغة، أدخل 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="c3152-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="c3152-163">اكتب [))] في نهاية المعادلة.</span><span class="sxs-lookup"><span data-stu-id="c3152-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="c3152-164">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="c3152-164">Click Save.</span></span>
    * <span data-ttu-id="c3152-165">تأكد من أنه لم يتم اكتشاف أية أخطاء للمعادلة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c3152-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="c3152-166">راجع علامة التبويب "أخطاء" أسفل عنصر التحكم في محرر المعادلة.</span><span class="sxs-lookup"><span data-stu-id="c3152-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="c3152-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3152-167">Close the page.</span></span>
27. <span data-ttu-id="c3152-168">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3152-168">Click OK.</span></span>
    * <span data-ttu-id="c3152-169">أضف الحقل المحسوب إلى مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="c3152-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="c3152-170">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c3152-170">Click Add.</span></span>
    * <span data-ttu-id="c3152-171">انقر فوق "إضافة" لإضافة حقل محسوب جديد.</span><span class="sxs-lookup"><span data-stu-id="c3152-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="c3152-172">في الحقل "الاسم"، اكتب "$Amount".</span><span class="sxs-lookup"><span data-stu-id="c3152-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="c3152-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="c3152-173">$Amount</span></span>  
30. <span data-ttu-id="c3152-174">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="c3152-174">Click Edit formula.</span></span>
31. <span data-ttu-id="c3152-175">في الشجرة، قم بتوسيع "الحركات".</span><span class="sxs-lookup"><span data-stu-id="c3152-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="c3152-176">في الشجرة، حدد "Transactions\Debit(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="c3152-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="c3152-177">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="c3152-177">Click Add data source.</span></span>
34. <span data-ttu-id="c3152-178">في حقل الصيغة، أدخل 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="c3152-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="c3152-179">اكتب [ - ] في نهاية المعادلة.</span><span class="sxs-lookup"><span data-stu-id="c3152-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="c3152-180">في الشجرة، حدد "الحركات/Credit(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="c3152-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="c3152-181">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="c3152-181">Click Add data source.</span></span>
37. <span data-ttu-id="c3152-182">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c3152-182">Click Save.</span></span>
38. <span data-ttu-id="c3152-183">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3152-183">Close the page.</span></span>
39. <span data-ttu-id="c3152-184">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3152-184">Click OK.</span></span>
    * <span data-ttu-id="c3152-185">سيؤدي هذا إلى إضافة حقل $Amount المحسوب إلى مصدر البيانات المحدد لنموذج البيانات الحالي.</span><span class="sxs-lookup"><span data-stu-id="c3152-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="c3152-186">في الشجرة، حدد "الحركات\$المبلغ".</span><span class="sxs-lookup"><span data-stu-id="c3152-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="c3152-187">في الشجرة، قم بتوسيع "الحركات".</span><span class="sxs-lookup"><span data-stu-id="c3152-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="c3152-188">في الشجرة، قم بتوسيع أو طي "الحركات\$المبلغ".</span><span class="sxs-lookup"><span data-stu-id="c3152-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="c3152-189">في الشجرة، قم بتوسيع أو طي 'الحركات'.</span><span class="sxs-lookup"><span data-stu-id="c3152-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="c3152-190">في الشجرة، حدد "Dynamics 365 for Operations\سجلات الجدول".</span><span class="sxs-lookup"><span data-stu-id="c3152-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="c3152-191">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="c3152-191">Click Add root.</span></span>
    * <span data-ttu-id="c3152-192">أدخل مصدر البيانات هذا للوصول إلى تفاصيل الحساب البنكي للشركة.</span><span class="sxs-lookup"><span data-stu-id="c3152-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="c3152-193">في الحقل "الاسم"، اكتب "BankAccount".</span><span class="sxs-lookup"><span data-stu-id="c3152-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="c3152-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="c3152-194">BankAccount</span></span>  
47. <span data-ttu-id="c3152-195">في الحقل "التسمية"، أدخل "Bank Account".</span><span class="sxs-lookup"><span data-stu-id="c3152-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="c3152-196">الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="c3152-196">Bank Account</span></span>  
48. <span data-ttu-id="c3152-197">في الحقل "العليمات"، أدخل "حساب البنك".</span><span class="sxs-lookup"><span data-stu-id="c3152-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="c3152-198">الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="c3152-198">Bank Account</span></span>  
49. <span data-ttu-id="c3152-199">حدد "نعم" في حقل "طلب الاستعلام".</span><span class="sxs-lookup"><span data-stu-id="c3152-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="c3152-200">حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="c3152-200">Select Yes.</span></span>  
50. <span data-ttu-id="c3152-201">في الحقل "الجدول"، اكتب "BankAccountTable".</span><span class="sxs-lookup"><span data-stu-id="c3152-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="c3152-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="c3152-202">BankAccountTable</span></span>  
51. <span data-ttu-id="c3152-203">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3152-203">Click OK.</span></span>
    * <span data-ttu-id="c3152-204">حدد الجدول BankAccountTable كمصدر بيانات لنموذج البيانات الحالي.</span><span class="sxs-lookup"><span data-stu-id="c3152-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="c3152-205">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="c3152-205">Click Add root.</span></span>
    * <span data-ttu-id="c3152-206">أدخل مصدر البيانات هذا للوصول إلى متطلبات الشركة.</span><span class="sxs-lookup"><span data-stu-id="c3152-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="c3152-207">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="c3152-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="c3152-208">الشركة</span><span class="sxs-lookup"><span data-stu-id="c3152-208">Company</span></span>  
54. <span data-ttu-id="c3152-209">في الحقل "التسمية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3152-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="c3152-210">معلومات الشركة</span><span class="sxs-lookup"><span data-stu-id="c3152-210">Company information</span></span>  
55. <span data-ttu-id="c3152-211">في الحقل "التعليمات"، أدخل "معلومات الشركة".</span><span class="sxs-lookup"><span data-stu-id="c3152-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="c3152-212">معلومات الشركة</span><span class="sxs-lookup"><span data-stu-id="c3152-212">Company information</span></span>  
56. <span data-ttu-id="c3152-213">حدد "نعم" في حقل "طلب الاستعلام".</span><span class="sxs-lookup"><span data-stu-id="c3152-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="c3152-214">حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="c3152-214">Select Yes.</span></span>  
57. <span data-ttu-id="c3152-215">في الحقل "الجدول"، اكتب "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="c3152-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="c3152-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="c3152-216">CompanyInfo</span></span>  
58. <span data-ttu-id="c3152-217">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3152-217">Click OK.</span></span>
    * <span data-ttu-id="c3152-218">حدد الجدول CompanyInfo كمصدر بيانات لنموذج البيانات الحالي.</span><span class="sxs-lookup"><span data-stu-id="c3152-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="c3152-219">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="c3152-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="c3152-220">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="c3152-220">Click Add root.</span></span>
    * <span data-ttu-id="c3152-221">أدرج حقلاً محسوبًا كمصدر بيانات جديد.</span><span class="sxs-lookup"><span data-stu-id="c3152-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="c3152-222">في الحقل "الاسم، اكتب "ProcessingDateTime".‬</span><span class="sxs-lookup"><span data-stu-id="c3152-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="c3152-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="c3152-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="c3152-224">في الحقل "التسمية"، أدخل "تاريخ المعالجة ووقتها".</span><span class="sxs-lookup"><span data-stu-id="c3152-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="c3152-225">تاريخ المعالجة ووقتها</span><span class="sxs-lookup"><span data-stu-id="c3152-225">Processing date & time</span></span>  
63. <span data-ttu-id="c3152-226">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="c3152-226">Click Edit formula.</span></span>
64. <span data-ttu-id="c3152-227">في الشجرة، حدد "التاريخ/الوقت\SESSIONNOW".</span><span class="sxs-lookup"><span data-stu-id="c3152-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="c3152-228">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="c3152-228">Click Add function.</span></span>
66. <span data-ttu-id="c3152-229">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c3152-229">Click Save.</span></span>
67. <span data-ttu-id="c3152-230">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3152-230">Close the page.</span></span>
68. <span data-ttu-id="c3152-231">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3152-231">Click OK.</span></span>
    * <span data-ttu-id="c3152-232">أضف الحقل المحسوب ProcessingDateTime كمصدر بيانات لنموذج البيانات الحالي.</span><span class="sxs-lookup"><span data-stu-id="c3152-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="c3152-233">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c3152-233">Click Save.</span></span>
70. <span data-ttu-id="c3152-234">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3152-234">Close the page.</span></span>
71. <span data-ttu-id="c3152-235">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3152-235">Close the page.</span></span>
72. <span data-ttu-id="c3152-236">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3152-236">Close the page.</span></span>

