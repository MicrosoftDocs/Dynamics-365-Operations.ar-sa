--- 
title: "تصميم نموذج بيانات لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مسؤول النظام أو مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.openlocfilehash: d8a03c4b85666975a7b42d46f3afdd35019e9b93
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="467d2-103">تصميم نموذج بيانات لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="467d2-103">Design data model to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="467d2-104">تشرح الخطوات التالية كيف يستطيع مسؤول النظام أو مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="467d2-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="467d2-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="467d2-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="467d2-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="467d2-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="467d2-107">إنشاء نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="467d2-107">Create a new data model</span></span>
1. <span data-ttu-id="467d2-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="467d2-109">تأكد من أن “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="467d2-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="467d2-110">متوفر ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="467d2-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="467d2-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="467d2-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="467d2-112">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="467d2-113">في حقل "الاسم"، اكتب "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="467d2-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="467d2-114">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="467d2-114">Click Create configuration.</span></span>
6. <span data-ttu-id="467d2-115">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="467d2-115">Click Designer.</span></span>
7. <span data-ttu-id="467d2-116">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="467d2-117">في حقل "الاسم"، اكتب "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="467d2-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="467d2-118">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-118">Click Add.</span></span>
10. <span data-ttu-id="467d2-119">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="467d2-120">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="467d2-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="467d2-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-121">Click Add.</span></span>
    * <span data-ttu-id="467d2-122">سوف نضيف إلى نموذجنا قائمة سجلات جديدة.</span><span class="sxs-lookup"><span data-stu-id="467d2-122">We will add to our model a new record list.</span></span> <span data-ttu-id="467d2-123">ستعرض هذه القائمة (لأي تقارير إلكترونية تستخدم هذا النموذج كمصدر بيانات) إعدادات أبعاد مالية محددة.</span><span class="sxs-lookup"><span data-stu-id="467d2-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="467d2-124">سيتم تقديم كل واحد من الأبعاد المالية في هذه القائمة كسجل مع حقول مناسبة تمثل إعداد البُعد.</span><span class="sxs-lookup"><span data-stu-id="467d2-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="467d2-125">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="467d2-126">في حقل "الاسم"، اكتب "إعداد الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="467d2-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="467d2-127">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="467d2-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="467d2-128">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-128">Click Add.</span></span>
17. <span data-ttu-id="467d2-129">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="467d2-130">في حقل "الاسم"، اكتب "الكود".</span><span class="sxs-lookup"><span data-stu-id="467d2-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="467d2-131">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="467d2-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="467d2-132">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-132">Click Add.</span></span>
21. <span data-ttu-id="467d2-133">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="467d2-134">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="467d2-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="467d2-135">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-135">Click Add.</span></span>
24. <span data-ttu-id="467d2-136">في الشجرة، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="467d2-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="467d2-137">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="467d2-138">في حقل "الاسم"، اكتب "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="467d2-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="467d2-139">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="467d2-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="467d2-140">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-140">Click Add.</span></span>
29. <span data-ttu-id="467d2-141">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="467d2-142">في حقل "الاسم"، اكتب "الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="467d2-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="467d2-143">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="467d2-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="467d2-144">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-144">Click Add.</span></span>
33. <span data-ttu-id="467d2-145">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="467d2-146">في حقل "الاسم"، اكتب "الحركة".</span><span class="sxs-lookup"><span data-stu-id="467d2-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="467d2-147">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="467d2-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="467d2-148">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-148">Click Add.</span></span>
37. <span data-ttu-id="467d2-149">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="467d2-150">في حقل "الاسم"، اكتب "التاريخ".</span><span class="sxs-lookup"><span data-stu-id="467d2-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="467d2-151">في الحقل "نوع الصنف"، حدد "تاريخ".</span><span class="sxs-lookup"><span data-stu-id="467d2-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="467d2-152">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-152">Click Add.</span></span>
41. <span data-ttu-id="467d2-153">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="467d2-154">في حقل "الاسم"، اكتب "الدين".</span><span class="sxs-lookup"><span data-stu-id="467d2-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="467d2-155">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="467d2-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="467d2-156">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-156">Click Add.</span></span>
45. <span data-ttu-id="467d2-157">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="467d2-158">في حقل "الاسم"، اكتب "الائتمان".</span><span class="sxs-lookup"><span data-stu-id="467d2-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="467d2-159">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-159">Click Add.</span></span>
48. <span data-ttu-id="467d2-160">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="467d2-161">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="467d2-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="467d2-162">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="467d2-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="467d2-163">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-163">Click Add.</span></span>
52. <span data-ttu-id="467d2-164">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="467d2-165">في حقل "الاسم"، اكتب "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="467d2-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="467d2-166">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-166">Click Add.</span></span>
55. <span data-ttu-id="467d2-167">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="467d2-168">في حقل "الاسم"، اكتب "بيانات الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="467d2-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="467d2-169">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="467d2-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="467d2-170">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-170">Click Add.</span></span>
    * <span data-ttu-id="467d2-171">لقد أضفنا قائمة سجلات جديدة إلى نموذجنا.</span><span class="sxs-lookup"><span data-stu-id="467d2-171">We added to our model a new record list.</span></span> <span data-ttu-id="467d2-172">ستعرض هذه القائمة (لأي تقارير إلكترونية تستخدم هذا النموذج كمصدر بيانات) قيم أبعاد مالية محددة.</span><span class="sxs-lookup"><span data-stu-id="467d2-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="467d2-173">سيتم تقديم كل واحد من الأبعاد المالية في هذه القائمة كسجل مع حقول مناسبة تمثل قيم البُعد.</span><span class="sxs-lookup"><span data-stu-id="467d2-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="467d2-174">سيتم أيضًا تقديم اسم البُعد في هذا السجل كحقل يجب استخدامه، إذا لزم الأمر، لأغراض التحديد.</span><span class="sxs-lookup"><span data-stu-id="467d2-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="467d2-175">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="467d2-176">في حقل "الاسم"، اكتب "الكود".</span><span class="sxs-lookup"><span data-stu-id="467d2-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="467d2-177">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="467d2-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="467d2-178">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-178">Click Add.</span></span>
63. <span data-ttu-id="467d2-179">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="467d2-180">في الحقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="467d2-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="467d2-181">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-181">Click Add.</span></span>
66. <span data-ttu-id="467d2-182">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="467d2-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="467d2-183">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="467d2-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="467d2-184">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="467d2-184">Click Add.</span></span>
69. <span data-ttu-id="467d2-185">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="467d2-185">Click Save.</span></span>
70. <span data-ttu-id="467d2-186">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="467d2-186">Close the page.</span></span>


