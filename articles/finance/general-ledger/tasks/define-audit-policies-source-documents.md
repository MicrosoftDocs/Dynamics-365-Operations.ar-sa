---
title: تحديد سياسات المراجعة للمستندات المصدر
description: يوضح هذا الموضوع كيفية إعداد وتشغيل قواعد سياسة التدقيق.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
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
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145019"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="f2c32-103">تحديد سياسات المراجعة للمستندات المصدر</span><span class="sxs-lookup"><span data-stu-id="f2c32-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2c32-104">يوضح هذا الموضوع كيفية إعداد وتشغيل قواعد سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="f2c32-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="f2c32-105">يستخدم المثال تقارير المصروفات مع نوع مصروفات الفندق.</span><span class="sxs-lookup"><span data-stu-id="f2c32-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="f2c32-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="f2c32-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f2c32-107">يحتوي دور المراجع يحتوي على الأذونات الصحيحة لتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="f2c32-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="f2c32-108">في جزء التنقل، انتقل إلى **الوحدات النمطية > منضدة عمل التدقيق‬ >الإعداد > نوع قاعدة السياسة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="f2c32-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-109">Select **New**.</span></span>
3. <span data-ttu-id="f2c32-110">في الحقل **اسم القاعدة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2c32-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="f2c32-111">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2c32-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f2c32-112">في الحقل **اسم الاستعلام**، حدد **بند تقرير المصروفات**</span><span class="sxs-lookup"><span data-stu-id="f2c32-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="f2c32-113">في الحقل **نوع الاستعلام**، حدد **مجمَّع‬**</span><span class="sxs-lookup"><span data-stu-id="f2c32-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="f2c32-114">في الحقل **الكيان القانوني**، حدد **الكيان القانوني**</span><span class="sxs-lookup"><span data-stu-id="f2c32-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="f2c32-115">في حقل **مرجع تاريخ المستند**، حدد **تاريخ ووقت التعديل‬**</span><span class="sxs-lookup"><span data-stu-id="f2c32-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="f2c32-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-116">Select **Save**.</span></span>
10. <span data-ttu-id="f2c32-117">في جزء التنقل، انتقل إلى **الوحدات النمطية > منضدة عمل التدقيق‬ >الإعداد > سياسات التدقيق**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="f2c32-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-118">Select **New**.</span></span>
12. <span data-ttu-id="f2c32-119">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2c32-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="f2c32-120">وسّع قسم **مؤسسات السياسات‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="f2c32-121">في الشجرة، حدد **Contoso Entertainment System USA**، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="f2c32-122">في الشجرة، حدد **Contoso Consulting USA**، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="f2c32-123">في الشجرة، حدد **Contoso Retail USA**، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="f2c32-124">قم بطيّ قسم **مؤسسات السياسات‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="f2c32-125">وسّع قسم **قواعد السياسة‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="f2c32-126">في القائمة، ابحث عن "قاعدة السياسة" التي تم إنشاؤها في السابق وحددها.</span><span class="sxs-lookup"><span data-stu-id="f2c32-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="f2c32-127">حدد **إنشاء قاعدة السياسة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="f2c32-128">في الحقل **تاريخ السريان**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f2c32-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="f2c32-129">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-129">Select **Filter**.</span></span>
23. <span data-ttu-id="f2c32-130">في القائمة، حدد صف **فئة المصروفات**، وعيّن التفاصيل إلى **فندق**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="f2c32-131">في الحقل **المعايير‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f2c32-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="f2c32-132">حدد علامة التبويب **تجميع‬**:</span><span class="sxs-lookup"><span data-stu-id="f2c32-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="f2c32-133">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-133">Select **Add**.</span></span>
27. <span data-ttu-id="f2c32-134">في القائمة، حدد قيمة حقل **مبلغ الحركة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="f2c32-135">في حقل **الحقل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f2c32-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="f2c32-136">في حقل **AggregateFunction**، حدد **المجموع**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="f2c32-137">حدد علامة التبويب **تجميع حسب**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="f2c32-138">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-138">Select **Add**.</span></span>
32. <span data-ttu-id="f2c32-139">في القائمة، حدد قيمة **الموظف**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="f2c32-140">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-140">Select **Add**.</span></span>
34. <span data-ttu-id="f2c32-141">في القائمة، حدد قيمة **فئة المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="f2c32-142">في حقل **الحقل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f2c32-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="f2c32-143">حدد علامة التبويب **يحتوي**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="f2c32-144">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-144">Select **Add**.</span></span>
38. <span data-ttu-id="f2c32-145">حدد **مبلغ الحركة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="f2c32-146">في حقل **الحقل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f2c32-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="f2c32-147">في حقل **AggregateFunction**، حدد **المجموع**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="f2c32-148">في حقل **المعايير‏‎**، اكتب `>2000`.</span><span class="sxs-lookup"><span data-stu-id="f2c32-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="f2c32-149">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-149">Select **OK**.</span></span>
43. <span data-ttu-id="f2c32-150">حدد **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-150">Select **Test**.</span></span>
44. <span data-ttu-id="f2c32-151">في الحقل **تاريخ بدء تحديد المستند‬**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f2c32-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="f2c32-152">في الحقل **تاريخ انتهاء تحديد المستند‬**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f2c32-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="f2c32-153">حدد **تشغيل الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-153">Select **Run test**.</span></span>
47. <span data-ttu-id="f2c32-154">في جزء الإجراءات، حدد **سياسة التدقيق**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="f2c32-155">حدد **خيارات إضافية**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="f2c32-156">في الحقل **تاريخ البدء**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f2c32-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="f2c32-157">في الحقل **تاريخ الانتهاء‬**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f2c32-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="f2c32-158">حدد **الدُفعة**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-158">Select **Batch**.</span></span>
52. <span data-ttu-id="f2c32-159">وسّع القسم **تشغيل في الخلفية‬‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="f2c32-160">حدد **نعم** في حقل **معالجة الدُفعات**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="f2c32-161">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-161">Select **OK**.</span></span>
55. <span data-ttu-id="f2c32-162">في جزء التنقل، انتقل إلى **الوحدات النمطية > منضدة عمل التدقيق‬ >الإعداد > تدقيق الحالات**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="f2c32-163">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2c32-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="f2c32-164">وسّع القسم **اقترانات‬‬‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="f2c32-165">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2c32-165">In the list, find and select the desired record.</span></span>

