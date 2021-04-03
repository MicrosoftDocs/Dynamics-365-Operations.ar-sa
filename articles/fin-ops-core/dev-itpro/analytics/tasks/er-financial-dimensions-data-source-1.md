---
title: "\"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1 - تصميم نموذج البيانات)"
description: يوضح هذا الموضوع كيفيه تكوين نموذج التقرير الكتروني (ER) لاستخدام الابعاد المالية كمصدر بيانات لتقارير ER. (جزء 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570182"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="ea98d-104">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1 - تصميم نموذج البيانات)</span><span class="sxs-lookup"><span data-stu-id="ea98d-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea98d-105">تشرح الخطوات التالية كيف يستطيع مسؤول النظام أو مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ea98d-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ea98d-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="ea98d-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="ea98d-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="ea98d-108">إنشاء نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="ea98d-108">Create a new data model</span></span>
1. <span data-ttu-id="ea98d-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ea98d-110">تأكد من أن موفر “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="ea98d-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="ea98d-111">متوفر ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="ea98d-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="ea98d-112">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="ea98d-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ea98d-113">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="ea98d-114">في حقل "الاسم"، اكتب "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="ea98d-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="ea98d-115">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="ea98d-115">Click Create configuration.</span></span>
6. <span data-ttu-id="ea98d-116">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="ea98d-116">Click Designer.</span></span>
7. <span data-ttu-id="ea98d-117">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="ea98d-118">في حقل "الاسم"، اكتب "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="ea98d-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="ea98d-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-119">Click Add.</span></span>
10. <span data-ttu-id="ea98d-120">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="ea98d-121">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="ea98d-122">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-122">Click Add.</span></span>
    * <span data-ttu-id="ea98d-123">سوف نضيف إلى نموذجنا قائمة سجلات جديدة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-123">We will add to our model a new record list.</span></span> <span data-ttu-id="ea98d-124">ستعرض هذه القائمة (لأي تقارير إلكترونية تستخدم هذا النموذج كمصدر بيانات) إعدادات أبعاد مالية محددة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="ea98d-125">سيتم تقديم كل واحد من الأبعاد المالية في هذه القائمة كسجل مع حقول مناسبة تمثل إعداد البُعد.</span><span class="sxs-lookup"><span data-stu-id="ea98d-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="ea98d-126">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="ea98d-127">في حقل "الاسم"، اكتب "إعداد الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="ea98d-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="ea98d-128">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="ea98d-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="ea98d-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-129">Click Add.</span></span>
17. <span data-ttu-id="ea98d-130">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="ea98d-131">في حقل "الاسم"، اكتب "الكود".</span><span class="sxs-lookup"><span data-stu-id="ea98d-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="ea98d-132">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="ea98d-133">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-133">Click Add.</span></span>
21. <span data-ttu-id="ea98d-134">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="ea98d-135">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="ea98d-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="ea98d-136">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-136">Click Add.</span></span>
24. <span data-ttu-id="ea98d-137">في الشجرة، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="ea98d-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="ea98d-138">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="ea98d-139">في حقل "الاسم"، اكتب "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="ea98d-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="ea98d-140">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="ea98d-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="ea98d-141">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-141">Click Add.</span></span>
29. <span data-ttu-id="ea98d-142">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="ea98d-143">في حقل "الاسم"، اكتب "الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="ea98d-144">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="ea98d-145">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-145">Click Add.</span></span>
33. <span data-ttu-id="ea98d-146">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="ea98d-147">في حقل "الاسم"، اكتب "الحركة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="ea98d-148">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="ea98d-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="ea98d-149">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-149">Click Add.</span></span>
37. <span data-ttu-id="ea98d-150">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="ea98d-151">في حقل "الاسم"، اكتب "التاريخ".</span><span class="sxs-lookup"><span data-stu-id="ea98d-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="ea98d-152">في الحقل "نوع الصنف"، حدد "تاريخ".</span><span class="sxs-lookup"><span data-stu-id="ea98d-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="ea98d-153">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-153">Click Add.</span></span>
41. <span data-ttu-id="ea98d-154">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="ea98d-155">في حقل "الاسم"، اكتب "الدين".</span><span class="sxs-lookup"><span data-stu-id="ea98d-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="ea98d-156">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="ea98d-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="ea98d-157">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-157">Click Add.</span></span>
45. <span data-ttu-id="ea98d-158">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="ea98d-159">في حقل "الاسم"، اكتب "الائتمان".</span><span class="sxs-lookup"><span data-stu-id="ea98d-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="ea98d-160">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-160">Click Add.</span></span>
48. <span data-ttu-id="ea98d-161">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="ea98d-162">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="ea98d-163">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="ea98d-164">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-164">Click Add.</span></span>
52. <span data-ttu-id="ea98d-165">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="ea98d-166">في حقل "الاسم"، اكتب "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="ea98d-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="ea98d-167">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-167">Click Add.</span></span>
55. <span data-ttu-id="ea98d-168">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="ea98d-169">في حقل "الاسم"، اكتب "بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="ea98d-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="ea98d-170">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="ea98d-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="ea98d-171">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-171">Click Add.</span></span>
    * <span data-ttu-id="ea98d-172">لقد أضفنا قائمة سجلات جديدة إلى نموذجنا.</span><span class="sxs-lookup"><span data-stu-id="ea98d-172">We added to our model a new record list.</span></span> <span data-ttu-id="ea98d-173">ستعرض هذه القائمة (لأي تقارير إلكترونية تستخدم هذا النموذج كمصدر بيانات) قيم أبعاد مالية محددة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="ea98d-174">سيتم تقديم كل واحد من الأبعاد المالية في هذه القائمة كسجل مع حقول مناسبة تمثل قيم البُعد.</span><span class="sxs-lookup"><span data-stu-id="ea98d-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="ea98d-175">سيتم أيضًا تقديم اسم البُعد في هذا السجل كحقل يجب استخدامه، إذا لزم الأمر، لأغراض التحديد.</span><span class="sxs-lookup"><span data-stu-id="ea98d-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="ea98d-176">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="ea98d-177">في حقل "الاسم"، اكتب "الكود".</span><span class="sxs-lookup"><span data-stu-id="ea98d-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="ea98d-178">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="ea98d-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="ea98d-179">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-179">Click Add.</span></span>
63. <span data-ttu-id="ea98d-180">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="ea98d-181">في الحقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="ea98d-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="ea98d-182">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-182">Click Add.</span></span>
66. <span data-ttu-id="ea98d-183">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ea98d-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="ea98d-184">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="ea98d-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="ea98d-185">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-185">Click Add.</span></span>
69. <span data-ttu-id="ea98d-186">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="ea98d-186">Click Save.</span></span>
70. <span data-ttu-id="ea98d-187">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea98d-187">Close the page.</span></span>

![صفحة مصمم نموذج بيانات التقارير الإلكترونية](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]