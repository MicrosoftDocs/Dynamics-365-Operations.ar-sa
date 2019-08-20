---
title: تحديد سياسات المراجعة للمستندات المصدر
description: يوضح هذا الإجراء كيفية إعداد وتشغيل قواعد سياسة التدقيق.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17b712f07a0ffe6874eb6d98b47ced96f5a54483
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846477"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="9d9d9-103">تحديد سياسات المراجعة للمستندات المصدر</span><span class="sxs-lookup"><span data-stu-id="9d9d9-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d9d9-104">يوضح هذا الإجراء كيفية إعداد وتشغيل قواعد سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="9d9d9-105">يستخدم المثال تقارير المصروفات مع نوع مصروفات الفندق.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="9d9d9-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="9d9d9-107">يحتوي دور المراجع يحتوي على الأذونات الصحيحة لتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="9d9d9-108">انتقل إلى منضدة عمل التدقيق‬ > إعداد > نوع قاعدة السياسة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="9d9d9-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-109">Click New.</span></span>
3. <span data-ttu-id="9d9d9-110">في الحقل "اسم القاعدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="9d9d9-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9d9d9-112">في الحقل "اسم الاستعلام"، حدد "بند تقرير المصروفات"</span><span class="sxs-lookup"><span data-stu-id="9d9d9-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="9d9d9-113">في الحقل "نوع الاستعلام"، حدد "مجمَّع‬"</span><span class="sxs-lookup"><span data-stu-id="9d9d9-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="9d9d9-114">في الحقل "كيان قانوني"، حدد كيانًا قانونيًا</span><span class="sxs-lookup"><span data-stu-id="9d9d9-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="9d9d9-115">في حقل "مرجع تاريخ المستند"، حدد "تاريخ ووقت التعديل‬"</span><span class="sxs-lookup"><span data-stu-id="9d9d9-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="9d9d9-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-116">Click Save.</span></span>
10. <span data-ttu-id="9d9d9-117">انتقل إلى منضدة عمل التدقيق‬ > إعداد > سياسات التدقيق.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="9d9d9-118">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-118">Click New.</span></span>
12. <span data-ttu-id="9d9d9-119">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="9d9d9-120">وسّع المقطع "مؤسسات السياسات‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="9d9d9-121">في الشجرة، حدد '"Contoso Entertainment System USA".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="9d9d9-122">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-122">Click Add.</span></span>
16. <span data-ttu-id="9d9d9-123">في الشجرة، حدد '"Contoso Consulting USA".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="9d9d9-124">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-124">Click Add.</span></span>
18. <span data-ttu-id="9d9d9-125">في الشجرة، حدد '"Contoso Retail USA".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="9d9d9-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-126">Click Add.</span></span>
20. <span data-ttu-id="9d9d9-127">قم بطيّ المقطع "مؤسسات السياسات‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="9d9d9-128">وسّع المقطع "قواعد السياسة‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="9d9d9-129">في القائمة، ابحث عن "قاعدة السياسة" التي تم إنشاؤها في السابق وحددها.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="9d9d9-130">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="9d9d9-131">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="9d9d9-132">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-132">Click Filter.</span></span>
26. <span data-ttu-id="9d9d9-133">في القائمة، حدد الصف لفئة المصروفات وعيّن التفاصيل إلى "الفندق"</span><span class="sxs-lookup"><span data-stu-id="9d9d9-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="9d9d9-134">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="9d9d9-135">انقر فوق علامة التبويب "مجمَّع‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="9d9d9-136">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-136">Click Add.</span></span>
30. <span data-ttu-id="9d9d9-137">في القائمة، حدد قيمة حقل "مبلغ الحركة"</span><span class="sxs-lookup"><span data-stu-id="9d9d9-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="9d9d9-138">في حقل "الحقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="9d9d9-139">في حقل AggregateFunction، حدد "المجموع".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="9d9d9-140">انقر فوق علامة التبويب "تجميع حسب‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="9d9d9-141">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-141">Click Add.</span></span>
35. <span data-ttu-id="9d9d9-142">في القائمة، حدد قيمة "الموظف" </span><span class="sxs-lookup"><span data-stu-id="9d9d9-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="9d9d9-143">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-143">Click Add.</span></span>
37. <span data-ttu-id="9d9d9-144">في القائمة، حدد قيمة "فئة المصروفات"</span><span class="sxs-lookup"><span data-stu-id="9d9d9-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="9d9d9-145">في حقل "الحقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="9d9d9-146">انقر فوق علامة التبويب "لديّ".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-146">Click the Having tab.</span></span>
40. <span data-ttu-id="9d9d9-147">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-147">Click Add.</span></span>
41. <span data-ttu-id="9d9d9-148">حدد مبلغ الحركة</span><span class="sxs-lookup"><span data-stu-id="9d9d9-148">Select Transaction amount</span></span>
42. <span data-ttu-id="9d9d9-149">في حقل "الحقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="9d9d9-150">في حقل AggregateFunction، حدد "المجموع".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="9d9d9-151">في الحقل "المعايير، اكتب ''>2000".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="9d9d9-152">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-152">Click OK.</span></span>
46. <span data-ttu-id="9d9d9-153">انقر فوق اختبار.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-153">Click Test.</span></span>
47. <span data-ttu-id="9d9d9-154">في الحقل "تاريخ بدء تحديد المستند‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="9d9d9-155">في الحقل "تاريخ انتهاء تحديد المستند‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="9d9d9-156">انقر فوق "تشغيل الاختبار‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-156">Click Run test.</span></span>
50. <span data-ttu-id="9d9d9-157">في جزء الإجراءات، انقر فوق "سياسة التدقيق".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="9d9d9-158">انقر فوق "خيارات إضافية".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-158">Click Additional options.</span></span>
52. <span data-ttu-id="9d9d9-159">في الحقل "تاريخ البدء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="9d9d9-160">في الحقل "تاريخ الانتهاء‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="9d9d9-161">انقر فوق "دُفعة".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-161">Click Batch.</span></span>
55. <span data-ttu-id="9d9d9-162">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="9d9d9-163">حدد "نعم" في حقل "معالجة الدُفعات‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="9d9d9-164">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-164">Click OK.</span></span>
58. <span data-ttu-id="9d9d9-165">انتقل إلى منضدة عمل التدقيق‬ > تدقيق الحالات‬.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="9d9d9-166">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="9d9d9-167">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="9d9d9-168">وسّع المقطع "اقترانات‬‬‬".</span><span class="sxs-lookup"><span data-stu-id="9d9d9-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="9d9d9-169">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="9d9d9-170">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-170">In the list, click the link in the selected row.</span></span>

