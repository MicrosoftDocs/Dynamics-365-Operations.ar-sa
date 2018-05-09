--- 
title: "استخدام تكوين تعيين نموذج للحسابات المجمعة على مستوى قاعدة البيانات (التقارير الإلكترونية)"
description: "يوفر هذا الإجراء معلومات حول كيفية تصميم تكوين جديد لتعيين نموذج التقارير الإلكترونية، واستخدم وظائف التقارير الإلكترونية المدمجة لإجراء حسابات مجمعة فعالة."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1dfb0d62f87f4bfdf4916fe2348bee5019841e93
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="34e82-103">استخدام تكوين تعيين نموذج للحسابات المجمعة على مستوى قاعدة البيانات (التقارير الإلكترونية)</span><span class="sxs-lookup"><span data-stu-id="34e82-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34e82-104">يوفر هذا الإجراء معلومات حول كيفية تصميم تكوين جديد لتعيين نموذج التقارير الإلكترونية، واستخدم وظائف التقارير الإلكترونية المدمجة لإجراء حسابات مجمعة فعالة.</span><span class="sxs-lookup"><span data-stu-id="34e82-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="34e82-105">في هذا الإجراء، ستقوم بإنشاء تكوين للشركة النموذجية، Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="34e82-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="34e82-106">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="34e82-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="34e82-107">يمكن إتمام هذه الخطوات باستخدام أي مجموعة بيانات.</span><span class="sxs-lookup"><span data-stu-id="34e82-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="34e82-108">لإتمام هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء، "التقارير الإلكترونية - تحسن فعالية الحسابات المجمعة من خلال تنفيذها على مستوى قاعدة البيانات (الجزء الأول: إعداد التكوينات).</span><span class="sxs-lookup"><span data-stu-id="34e82-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="34e82-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="34e82-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="34e82-110">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="34e82-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="34e82-111">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\تعيين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="34e82-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="34e82-112">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="34e82-112">Click Designer.</span></span>
5. <span data-ttu-id="34e82-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="34e82-113">Click Designer.</span></span>
6. <span data-ttu-id="34e82-114">في الشجرة، حدد "Dynamics 365 for Operations\سجلات جدول".</span><span class="sxs-lookup"><span data-stu-id="34e82-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="34e82-115">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="34e82-115">Click Add root.</span></span>
    * <span data-ttu-id="34e82-116">قم بإضافة مصدر بيانات جديد يمثل السجلات التي تريد تجميعها.</span><span class="sxs-lookup"><span data-stu-id="34e82-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="34e82-117">في الحقل "الاسم"، اكتب "الحركات".</span><span class="sxs-lookup"><span data-stu-id="34e82-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="34e82-118">الحركات</span><span class="sxs-lookup"><span data-stu-id="34e82-118">Transactions</span></span>  
9. <span data-ttu-id="34e82-119">في الحقل "الجدول"، اكتب "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="34e82-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="34e82-120">نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="34e82-120">Intrastat</span></span>  
10. <span data-ttu-id="34e82-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="34e82-121">Click OK.</span></span>
11. <span data-ttu-id="34e82-122">في الشجرة، حدد "Functions\Group by".</span><span class="sxs-lookup"><span data-stu-id="34e82-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="34e82-123">يتم استخدام نوع مصدر البيانات هذا لتقديم مصدر بيانات جديد أثناء وقت التشغيل لتجميع السجلات وحساب التجميعات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="34e82-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="34e82-124">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="34e82-124">Click Add root.</span></span>
13. <span data-ttu-id="34e82-125">في حقل "الاسم"، اكتب "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="34e82-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="34e82-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="34e82-127">انقر فوق تحرير تجميع حسب.</span><span class="sxs-lookup"><span data-stu-id="34e82-127">Click Edit group by.</span></span>
15. <span data-ttu-id="34e82-128">في الشجرة، حدد "الحركات".</span><span class="sxs-lookup"><span data-stu-id="34e82-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="34e82-129">حدد مصدر البيانات المضاف من النوع "قائمة السجلات" الذي يمثل السجلات التي تريد تجميعها.</span><span class="sxs-lookup"><span data-stu-id="34e82-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="34e82-130">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="34e82-130">Click Add field to.</span></span>
17. <span data-ttu-id="34e82-131">انقر فوق ما يتم تجميعه.</span><span class="sxs-lookup"><span data-stu-id="34e82-131">Click What to group.</span></span>
18. <span data-ttu-id="34e82-132">في الشجرة، قم بتوسيع "الحركات".</span><span class="sxs-lookup"><span data-stu-id="34e82-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="34e82-133">في الشجرة، حدد "حركات\اتجاه".</span><span class="sxs-lookup"><span data-stu-id="34e82-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="34e82-134">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="34e82-134">Click Add field to.</span></span>
21. <span data-ttu-id="34e82-135">انقر فوق "الحقول مجمعَة".</span><span class="sxs-lookup"><span data-stu-id="34e82-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="34e82-136">حدد الحقل لتحديد مستوى التجميع.</span><span class="sxs-lookup"><span data-stu-id="34e82-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="34e82-137">استنادًا إلى هذا التحديد، سوف يُرجع مصدر البيانات في وقت التشغيل العديد من مجموعات الحركات بمقدار أكواد الاتجاه والتي سيتم تطبيقها في جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="34e82-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="34e82-138">في الشجرة، حدد "حركات\مبلغ الفاتورة(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="34e82-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="34e82-139">حدد الحقل لتحديد مصدر لحساب التجميع.</span><span class="sxs-lookup"><span data-stu-id="34e82-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="34e82-140">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="34e82-140">Click Add field to.</span></span>
24. <span data-ttu-id="34e82-141">انقر فوق حقول التجميع.</span><span class="sxs-lookup"><span data-stu-id="34e82-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="34e82-142">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="34e82-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="34e82-143">في حقل "الأسلوب"، حدد "مجموع".</span><span class="sxs-lookup"><span data-stu-id="34e82-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="34e82-144">حدد نوع التجميع.</span><span class="sxs-lookup"><span data-stu-id="34e82-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="34e82-145">في حقل "الاسم"، اكتب "SumOfAmountMST".</span><span class="sxs-lookup"><span data-stu-id="34e82-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="34e82-146">حدد اسم هذا التجميع في مصدر البيانات الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="34e82-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="34e82-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="34e82-147">Click Save.</span></span>
    * <span data-ttu-id="34e82-148">لاحظ أن الحقل "التنفيذ في" يشير إلى أنه سيتم إنجاز هذا التجميع في وقت التشغيل في قاعدة بيانات SQL.</span><span class="sxs-lookup"><span data-stu-id="34e82-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="34e82-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="34e82-149">Close the page.</span></span>
30. <span data-ttu-id="34e82-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="34e82-150">Click OK.</span></span>
31. <span data-ttu-id="34e82-151">في الشجرة، قم بتوسيع "إجماليات".</span><span class="sxs-lookup"><span data-stu-id="34e82-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="34e82-152">في الشجرة، قم بتوسيع "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="34e82-153">في الشجرة، قم بتوسيع "TransactionsGroups\مجمعة".</span><span class="sxs-lookup"><span data-stu-id="34e82-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="34e82-154">في الشجرة، حدد "TransactionsGroups\مجمعة\SumOfAmountMST".</span><span class="sxs-lookup"><span data-stu-id="34e82-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="34e82-155">في الشجرة، حدد "إجماليات\إجمالي قيمة الفاتورة(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')".</span><span class="sxs-lookup"><span data-stu-id="34e82-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="34e82-156">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="34e82-156">Click Bind.</span></span>
    * <span data-ttu-id="34e82-157">استنادًا إلى هذا الإعداد، سيقوم مصدر البيانات هذا بحساب مجموع القيم للحقل "AmountMST" لكل مجموعة حركات.</span><span class="sxs-lookup"><span data-stu-id="34e82-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="34e82-158">سيكون حساب التجميع هذا متوفرًا كصنف TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="34e82-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="34e82-159">في الشجرة، قم بتوسيع "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="34e82-160">في الشجرة، حدد "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="34e82-161">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="34e82-161">Click Edit.</span></span>
40. <span data-ttu-id="34e82-162">انقر فوق تحرير تجميع حسب.</span><span class="sxs-lookup"><span data-stu-id="34e82-162">Click Edit group by.</span></span>
41. <span data-ttu-id="34e82-163">في الشجرة، قم بتوسيع "الحركات".</span><span class="sxs-lookup"><span data-stu-id="34e82-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="34e82-164">في الشجرة، حدد "حركات\مبلغ الفاتورة(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="34e82-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="34e82-165">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="34e82-165">Click Add field to.</span></span>
44. <span data-ttu-id="34e82-166">انقر فوق حقول التجميع.</span><span class="sxs-lookup"><span data-stu-id="34e82-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="34e82-167">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="34e82-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="34e82-168">في حقل "الأسلوب"، حدد "الحد الأقصى".</span><span class="sxs-lookup"><span data-stu-id="34e82-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="34e82-169">في حقل "الاسم"، اكتب "MaxOfAmountMST".</span><span class="sxs-lookup"><span data-stu-id="34e82-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="34e82-170">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="34e82-170">Click Save.</span></span>
    * <span data-ttu-id="34e82-171">في الوقت الحالي، يمكن ترجمة تنفيذ مصادر بيانات GROUPBY إلى مستوى قاعدة البيانات مع وجود بعض القيود.</span><span class="sxs-lookup"><span data-stu-id="34e82-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="34e82-172">يمكن إجراء الترجمة لأي من مصادر البيانات من النوع "قائمة السجلات" أو مصادر البيانات الممثلة كتعبير باستخدام الدالة FILTER.</span><span class="sxs-lookup"><span data-stu-id="34e82-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="34e82-173">ويمكن إجراء الترجمة أيضًا عند تكوين تجميع واحد فقط لحقل واحد من السجلات المجمعة.</span><span class="sxs-lookup"><span data-stu-id="34e82-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="34e82-174">لاحظ أنه على الرغم من تكوين أكثر من تجميع واحد للحقل AmountMST، يستمر حقل "التنفيذ في" في الإشارة إلى أن تنفيذ هذا التجميع سوف يتم في وقت التشغيل في قاعدة بيانات SQL.</span><span class="sxs-lookup"><span data-stu-id="34e82-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="34e82-175">ويعود السبب في ذلك إلى ارتباط تجميع واحد فقط بصنف نموذج البيانات، وسوف يتم استخدامه في وقت التشغيل لسحب البيانات من مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="34e82-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="34e82-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="34e82-176">Close the page.</span></span>
50. <span data-ttu-id="34e82-177">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="34e82-177">Click OK.</span></span>
51. <span data-ttu-id="34e82-178">في الشجرة، قم بتوسيع "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="34e82-179">في الشجرة، قم بتوسيع "TransactionsGroups\مجمعة".</span><span class="sxs-lookup"><span data-stu-id="34e82-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="34e82-180">في الشجرة، حدد "TransactionsGroups\مجمعة\MaxOfAmountMST".</span><span class="sxs-lookup"><span data-stu-id="34e82-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="34e82-181">في الشجرة، حدد "إجماليات\إجمالي القيمة الإحصائية‬(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span><span class="sxs-lookup"><span data-stu-id="34e82-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="34e82-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="34e82-182">Click Bind.</span></span>
56. <span data-ttu-id="34e82-183">في الشجرة، قم بتوسيع "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="34e82-184">في الشجرة، حدد "TransactionsGroups".</span><span class="sxs-lookup"><span data-stu-id="34e82-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="34e82-185">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="34e82-185">Click Edit.</span></span>
59. <span data-ttu-id="34e82-186">انقر فوق تحرير تجميع حسب.</span><span class="sxs-lookup"><span data-stu-id="34e82-186">Click Edit group by.</span></span>
    * <span data-ttu-id="34e82-187">لاحظ أن حقل "التنفيذ في" يشير إلى أنه سيتم تنفيذ هذا التجميع في وقت التشغيل في الذاكرة نظرًا لارتباط التجميعين للحقل نفسه بأصناف نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="34e82-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="34e82-188">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="34e82-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="34e82-189">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="34e82-189">Click Delete.</span></span>
62. <span data-ttu-id="34e82-190">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="34e82-190">Click Yes.</span></span>
63. <span data-ttu-id="34e82-191">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="34e82-191">Click Delete.</span></span>
64. <span data-ttu-id="34e82-192">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="34e82-192">Click Yes.</span></span>
65. <span data-ttu-id="34e82-193">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="34e82-193">Click Add field to.</span></span>
66. <span data-ttu-id="34e82-194">انقر فوق ما يتم تجميعه.</span><span class="sxs-lookup"><span data-stu-id="34e82-194">Click What to group.</span></span>
67. <span data-ttu-id="34e82-195">في الشجرة، قم بتوسيع "سجل السلع‬(نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي)".</span><span class="sxs-lookup"><span data-stu-id="34e82-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="34e82-196">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="34e82-196">Click Save.</span></span>
    * <span data-ttu-id="34e82-197">لاحظ أن حقل "التنفيذ في" يشير إلى أنه سيتم تنفيذ هذا التجميع في وقت التشغيل في الذاكرة على الرغم من عدم تحديد أي تجميعات ولأن مصدر البيانات المحدد لنوع "سجلات الجدول" يشير إلى جدول "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي" نفسه.</span><span class="sxs-lookup"><span data-stu-id="34e82-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="34e82-198">يعود السبب في ذلك إلى احتواء مصدر البيانات على بعض الحقول المحسوبة التي لا يتم ترجمتها بعد إلى مستوى قاعدة بيانات SQL.</span><span class="sxs-lookup"><span data-stu-id="34e82-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  


