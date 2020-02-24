---
title: التقارير الإلكترونية - تعيين مكونات التنسيق المنشأ إلى عناصر نموذج البيانات (نوفمبر 2016)
description: يوضح الإجراء التالي كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تعيين عناصر نموذج بيانات إلى مكونات تكوين التقارير الإلكترونية المنشأ، والذي يحدد تنسيق المستندات الإلكترونية لمجال مدفوعات الأعمال‬.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 548f16034ebdf7e0f29e8e89d85aac880f6323a1
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026230"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="57ecf-103">التقارير الإلكترونية - تعيين مكونات التنسيق المنشأ إلى عناصر نموذج البيانات (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="57ecf-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57ecf-104">يوضح الإجراء التالي كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تعيين عناصر نموذج بيانات إلى مكونات تكوين التقارير الإلكترونية المنشأ، والذي يحدد تنسيق المستندات الإلكترونية لمجال مدفوعات الأعمال‬.</span><span class="sxs-lookup"><span data-stu-id="57ecf-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="57ecf-105">سيتم استخدام التنسيق في وقت لاحق لإنشاء لإنشاء المستندات الإلكترونية لمعالجة المدفوعات</span><span class="sxs-lookup"><span data-stu-id="57ecf-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="57ecf-106">في هذا المثال، ستقوم بإنشاء تكوين تنسيق لشركة نموذجية، وهي ‘Litware, Inc.’.</span><span class="sxs-lookup"><span data-stu-id="57ecf-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="57ecf-107">يمكن تنفيذ هذه الخطوات في أي شركة إذ يمكن مشاركة تكوينات التقارير الإلكترونية لكل الشركات.</span><span class="sxs-lookup"><span data-stu-id="57ecf-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="57ecf-108">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات الموضحة في دليل المهمة "إنشاء تكوين تنسيق‬".</span><span class="sxs-lookup"><span data-stu-id="57ecf-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="57ecf-109">تحديد تكوين تنسيق</span><span class="sxs-lookup"><span data-stu-id="57ecf-109">Select a format configuration</span></span>
1. <span data-ttu-id="57ecf-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="57ecf-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="57ecf-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="57ecf-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="57ecf-112">في الشجرة، قم بتوسيع "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="57ecf-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="57ecf-113">في الشجرة، حدد "Payments (simplified model)\BACS (UK fictitious)".</span><span class="sxs-lookup"><span data-stu-id="57ecf-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="57ecf-114">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="57ecf-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="57ecf-115">تعيين مكونات التنسيق لعناصر نماذج البيانات</span><span class="sxs-lookup"><span data-stu-id="57ecf-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="57ecf-116">انقر فوق "توسيع/طي".</span><span class="sxs-lookup"><span data-stu-id="57ecf-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="57ecf-117">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="57ecf-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="57ecf-118">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="57ecf-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="57ecf-119">في الشجرة، حدد "Xml\الرسالة\ProcessingDate\DateTime".</span><span class="sxs-lookup"><span data-stu-id="57ecf-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="57ecf-120">في الشجرة، حدد "النموذج\ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="57ecf-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="57ecf-121">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-121">Click Bind.</span></span>
7. <span data-ttu-id="57ecf-122">في الشجرة، حدد "Xml\الرسالة\MessageId\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="57ecf-123">في الشجرة، حدد "النموذج\MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="57ecf-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="57ecf-124">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-124">Click Bind.</span></span>
10. <span data-ttu-id="57ecf-125">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="57ecf-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="57ecf-126">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المبلغ\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="57ecf-127">في الشجرة، حدد "النموذج/المدفوعات/InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="57ecf-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="57ecf-128">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-128">Click Bind.</span></span>
14. <span data-ttu-id="57ecf-129">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\TransDate\DateTime".</span><span class="sxs-lookup"><span data-stu-id="57ecf-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="57ecf-130">في الشجرة، حدد "النموذج/المدفوعات/TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="57ecf-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="57ecf-131">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-131">Click Bind.</span></span>
17. <span data-ttu-id="57ecf-132">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الوصف\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="57ecf-133">في الشجرة، حدد "النموذج/المدفوعات/الوصف".</span><span class="sxs-lookup"><span data-stu-id="57ecf-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="57ecf-134">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-134">Click Bind.</span></span>
20. <span data-ttu-id="57ecf-135">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\العملة\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="57ecf-136">في الشجرة، حدد "model\Payments\Currency".</span><span class="sxs-lookup"><span data-stu-id="57ecf-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="57ecf-137">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-137">Click Bind.</span></span>
23. <span data-ttu-id="57ecf-138">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المعرف".</span><span class="sxs-lookup"><span data-stu-id="57ecf-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="57ecf-139">في الشجرة، حدد "النموذج\المدفوعات\End2EndID".</span><span class="sxs-lookup"><span data-stu-id="57ecf-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="57ecf-140">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-140">Click Bind.</span></span>
26. <span data-ttu-id="57ecf-141">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="57ecf-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="57ecf-142">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن/الحساب".</span><span class="sxs-lookup"><span data-stu-id="57ecf-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="57ecf-143">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن/الوكيل".</span><span class="sxs-lookup"><span data-stu-id="57ecf-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="57ecf-144">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="57ecf-145">في الشجرة، حدد "النموذج/المدفوعات/الدائن/الاسم".</span><span class="sxs-lookup"><span data-stu-id="57ecf-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="57ecf-146">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-146">Click Bind.</span></span>
32. <span data-ttu-id="57ecf-147">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\RoutingNumber\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="57ecf-148">في الشجرة، حدد "النموذج\المدفوعات\الدائن\الوكيل\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="57ecf-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="57ecf-149">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-149">Click Bind.</span></span>
35. <span data-ttu-id="57ecf-150">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\AccountNumber\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="57ecf-151">في الشجرة، حدد "النموذج/المدفوعات/الدائن/الحساب/الرقم".</span><span class="sxs-lookup"><span data-stu-id="57ecf-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="57ecf-152">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-152">Click Bind.</span></span>
38. <span data-ttu-id="57ecf-153">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الممول\الاسم\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="57ecf-154">في الشجرة، قم بتوسيع "النموذج/المدفوعات/المدين".</span><span class="sxs-lookup"><span data-stu-id="57ecf-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="57ecf-155">في الشجرة، قم بتوسيع "النموذج/المدفوعات/المدين/الحساب".</span><span class="sxs-lookup"><span data-stu-id="57ecf-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="57ecf-156">في الشجرة، قم بتوسيع "النموذج/المدفوعات/المدين/الوكيل".</span><span class="sxs-lookup"><span data-stu-id="57ecf-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="57ecf-157">في الشجرة، حدد "النموذج/المدفوعات/المدين/الاسم".</span><span class="sxs-lookup"><span data-stu-id="57ecf-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="57ecf-158">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-158">Click Bind.</span></span>
44. <span data-ttu-id="57ecf-159">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\RoutingNumber\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="57ecf-160">في الشجرة، حدد "النموذج\المدفوعات\المدين‬\الوكيل\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="57ecf-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="57ecf-161">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-161">Click Bind.</span></span>
47. <span data-ttu-id="57ecf-162">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\AccountNumber\سلسلة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="57ecf-163">في الشجرة، حدد "النموذج/المدفوعات/المدين/الحساب/الرقم".</span><span class="sxs-lookup"><span data-stu-id="57ecf-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="57ecf-164">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-164">Click Bind.</span></span>
50. <span data-ttu-id="57ecf-165">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف".</span><span class="sxs-lookup"><span data-stu-id="57ecf-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="57ecf-166">في الشجرة، حدد "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="57ecf-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="57ecf-167">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="57ecf-167">Click Bind.</span></span>
53. <span data-ttu-id="57ecf-168">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="57ecf-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="57ecf-169">التحقق من صحة تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="57ecf-169">Validate format mapping</span></span>
1. <span data-ttu-id="57ecf-170">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="57ecf-170">Click Validate.</span></span>
    * <span data-ttu-id="57ecf-171">تحقق من صحة التعيين الجديد للتأكد من صحة كافة عمليات الربط‬.</span><span class="sxs-lookup"><span data-stu-id="57ecf-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="57ecf-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="57ecf-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="57ecf-173">تغيير حالة الإصدار الحالي لتكوين التنسيق</span><span class="sxs-lookup"><span data-stu-id="57ecf-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="57ecf-174">في الخطوات التالية، ستغير حالة تكوين التنسيق من "مسودة" إلى "مكتمل" لجعله متوفراً لإنشاء مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="57ecf-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="57ecf-175">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="57ecf-175">Click Change status.</span></span>
2. <span data-ttu-id="57ecf-176">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="57ecf-176">Click Complete.</span></span>
3. <span data-ttu-id="57ecf-177">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="57ecf-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="57ecf-178">على سبيل المثال، "الإصدار 1".</span><span class="sxs-lookup"><span data-stu-id="57ecf-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="57ecf-179">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="57ecf-179">Click OK.</span></span>
5. <span data-ttu-id="57ecf-180">حدد الإصدار المكتمل للتكوين الحالي.</span><span class="sxs-lookup"><span data-stu-id="57ecf-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="57ecf-181">لاحظ أنه يتم حفظ التكوين كالإصدار المكتمل 1.1: الإصدار 1 من التنسيق المستند إلى الإصدار 1 من نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="57ecf-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="57ecf-182">تحديد التاريخ الفعلي لإصدار تنسيق مكتمل</span><span class="sxs-lookup"><span data-stu-id="57ecf-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="57ecf-183">يمكن تكوين كل إصدار تنسيق كمتوفرة للاستخدام بدءاً من تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="57ecf-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="57ecf-184">عندما يكون أكثر من إصدار تنسيق واحد نشطاً في تاريخ معين، سيتم تحديد أحدث تنسيق (استناداً إلى رقم الإصدار) للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="57ecf-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="57ecf-185">يتم استخدام قيمة تاريخ الجلسة لتحديد الإصدار الصحيح.</span><span class="sxs-lookup"><span data-stu-id="57ecf-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="57ecf-186">تقييد الوصول إلى التنسيق الذي تم إنشاؤه من الشركات</span><span class="sxs-lookup"><span data-stu-id="57ecf-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="57ecf-187">قم بتوسيع قسم أكواد ISO للبلد/المنطقة‬.</span><span class="sxs-lookup"><span data-stu-id="57ecf-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="57ecf-188">يمكن تقييد كل عملية وصول إلى التنسيق بتحديد بلدان/مناطق معينة يكون التنسيق قابلاً للتطبيق بها.</span><span class="sxs-lookup"><span data-stu-id="57ecf-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="57ecf-189">عندما تكون قائمة البلدان/المناطق لتنسيق معين فارغة، يمكنك استخدام هذا التنسيق في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="57ecf-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="57ecf-190">عندما يتم إدراج بعض أكواد بلد/منطقة ISO في قائمة البلدان/المناطق، فلا يمكن استخدام التنسيق في الشركات إلا إذا كان العنوان الرئيسي موجودًا في البلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="57ecf-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

