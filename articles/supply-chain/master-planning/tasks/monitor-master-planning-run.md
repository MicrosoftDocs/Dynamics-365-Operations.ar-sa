---
title: مراقبة تشغيل التخطيط الرئيسي
description: يوضح هذا الموضوع كيف يمكن لمخطط الإنتاج معرفه ما إذا كانت هناك عمليه تشغيل تخطيط رئيسي قيد التقدم ام لا.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cbe2c55ef9e3ed35db30ca927f3472c750c1db5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999796"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="29840-103">مراقبة تشغيل التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="29840-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="29840-104">استخدام مخطط Gantt لتمثيل تقدم التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="29840-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="29840-105">من صفحة **عرض تقدم التخطيط الرئيسي**، يمكنك عرض تفاصيل تشغيل التخطيط الرئيسي التاريخي كمخطط Gantt.</span><span class="sxs-lookup"><span data-stu-id="29840-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="29840-106">يمكن أن تساعدك هذه الوظيفة علي فهم الوقت المستغرق في المراحل المتنوعة للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="29840-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="29840-107">بالنسبة لوظيفة التخطيط النشطة الحالية، يمكن استخدام صفحه **عرض تقدم التخطيط الرئيسي** لتعقب التقدم وعرض الوقت المتبقي المقدر.</span><span class="sxs-lookup"><span data-stu-id="29840-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="29840-108">تشغيل واستخدام ميزه المرئيات لتقدم الخطة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="29840-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="29840-109">لاستخدام هذه الوظيفة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="29840-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="29840-110">في مساحة عمل **إدارة الميزات**، في علامة التبويب **جديد**، حدد **مرئيات تقدم التخطيط الرئيسي** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="29840-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="29840-111">إذا لم تظهر الميزة على علامة التبويب **جديد**، فانظر إلى علامتي التبويب **غير ممكن** و **الكل**.</span><span class="sxs-lookup"><span data-stu-id="29840-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="29840-112">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="29840-112">Select **Enable now**.</span></span> <span data-ttu-id="29840-113">بدلاً من ذلك، حدد **جدولة**، ثم حدد الوقت الذي تريد فيه تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="29840-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="29840-114">يمكن لصفحة **عرض تقدم التخطيط الرئيسي** عرض كل من مهام التخطيط التاريخية ووظائف التخطيط النشطة.</span><span class="sxs-lookup"><span data-stu-id="29840-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="29840-115">لعرض مهام التخطيط التاريخية، يوجد خياران.</span><span class="sxs-lookup"><span data-stu-id="29840-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="29840-116">انتقل إلى **التخطيط الرئيسي \> إعداد \> خطط \> الخطط الرئيسية**، ثم في جزء الإجراء، حدد **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="29840-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="29840-117">من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**</span><span class="sxs-lookup"><span data-stu-id="29840-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="29840-118">انتقل إلى **التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي**، في تجانب التخطيط الرئيسي، انقر فوق **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="29840-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="29840-119">من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**</span><span class="sxs-lookup"><span data-stu-id="29840-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="29840-120">لعرض مهام التخطيط النشطة، يوجد خياران.</span><span class="sxs-lookup"><span data-stu-id="29840-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="29840-121">انتقل إلى **التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي**، في جزء الإجراء، حدد **عمليه التخطيط غير المنتهية**.</span><span class="sxs-lookup"><span data-stu-id="29840-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="29840-122">من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**.</span><span class="sxs-lookup"><span data-stu-id="29840-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="29840-123">انتقل إلى **التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي**، في تجانب التخطيط الرئيسي، انقر فوق **عرض التقدم**.</span><span class="sxs-lookup"><span data-stu-id="29840-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="29840-124">من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**</span><span class="sxs-lookup"><span data-stu-id="29840-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="29840-125">لاحظ أنه يمكنك عرض الوظائف النشطة فقط عند قيام وظيفة تخطيط بالمعالجة.</span><span class="sxs-lookup"><span data-stu-id="29840-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="29840-126">تحليل مهمة تخطيط رئيسيه</span><span class="sxs-lookup"><span data-stu-id="29840-126">Analyze a master planning job</span></span>

<span data-ttu-id="29840-127">في مخطط Gantt ، يمكنك توسيع كل من عمليات التخطيط التالية لعرض تفاصيل اضافيه حول الوقت المستغرق:</span><span class="sxs-lookup"><span data-stu-id="29840-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="29840-128">جارٍ تهيئة</span><span class="sxs-lookup"><span data-stu-id="29840-128">Initializing</span></span>
- <span data-ttu-id="29840-129">حذف بيانات وإدراجها</span><span class="sxs-lookup"><span data-stu-id="29840-129">Deleting and inserting data</span></span>
- <span data-ttu-id="29840-130">التخطيط للتغطية</span><span class="sxs-lookup"><span data-stu-id="29840-130">Coverage planning</span></span>
- <span data-ttu-id="29840-131">التأخيرات</span><span class="sxs-lookup"><span data-stu-id="29840-131">Delays</span></span>
- <span data-ttu-id="29840-132">رسائل الإجراءات</span><span class="sxs-lookup"><span data-stu-id="29840-132">Action messages</span></span>
- <span data-ttu-id="29840-133">إكمال</span><span class="sxs-lookup"><span data-stu-id="29840-133">Finalization</span></span>
- <span data-ttu-id="29840-134">التنفيذ التلقائي</span><span class="sxs-lookup"><span data-stu-id="29840-134">Auto-firming</span></span>

<span data-ttu-id="29840-135">يعتبر مخطط Gantt أداه مفيده إذا كنت ترغب في عرض تاثير استخدام رسائل الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="29840-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="29840-136">التنقل في مخطط Gantt</span><span class="sxs-lookup"><span data-stu-id="29840-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="29840-137">لتوسيع المجموعة المحددة وإظهار التفاصيل ، حدد علامة الجمع (**+**) في طريقه العرض الشجري.</span><span class="sxs-lookup"><span data-stu-id="29840-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="29840-138">لطي المجموعة المحددة ، حدد علامة الطرح (**–**) في طريقة عرض الشجرة.</span><span class="sxs-lookup"><span data-stu-id="29840-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="29840-139">يمكنك استخدام لوحه المفاتيح للتنقل.</span><span class="sxs-lookup"><span data-stu-id="29840-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="29840-140">استخدم مفتاحي **سهم لأعلى** و **سهم لأسفل** للتنقل بين الصفوف.</span><span class="sxs-lookup"><span data-stu-id="29840-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="29840-141">استخدم مفتاحي **السهم لليمين** و **السهم لليسار** لتوسيع وطي المجموعات.</span><span class="sxs-lookup"><span data-stu-id="29840-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="29840-142">لفتح كافة المستويات في مخطط Gantt أو إغلاقها، حدد **توسيع الكل** أو **طي الكل**.</span><span class="sxs-lookup"><span data-stu-id="29840-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="29840-143">لعرض وقت المعالجة المرتبط ، قم بالمرور فوق أحدي المهام.</span><span class="sxs-lookup"><span data-stu-id="29840-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="29840-144">(تعتبر المهام هي المستوي الأدنى في مخطط Gantt.)</span><span class="sxs-lookup"><span data-stu-id="29840-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="29840-145">عرض تخطيط رئيسي إضافي التشغيل لمقارنه الوظائف</span><span class="sxs-lookup"><span data-stu-id="29840-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="29840-146">ومن خلال تحديد مهمة تخطيط رئيسيه في الحقل **إظهار تشغيل التخطيط الرئيسي الإضافي**، يمكنك عرض تخطيط رئيسي إضافي في مخطط Gantt ومقارنه الوظيفتين.</span><span class="sxs-lookup"><span data-stu-id="29840-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="29840-147">العرض على مستوي قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="29840-147">BOM-level display</span></span>

<span data-ttu-id="29840-148">يتم عرض مستويات قائمة مكونات الصنف بشكل مختلف لتخطيط التغطية والتاخيرات والإجراءات والتاكيد.</span><span class="sxs-lookup"><span data-stu-id="29840-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="29840-149">**تخطيط التغطية** – تظهر مستويات قائمة مكونات الصنف بالشكل المتوقع.</span><span class="sxs-lookup"><span data-stu-id="29840-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="29840-150">يتم حسابها من الأعلى إلى أسفل.</span><span class="sxs-lookup"><span data-stu-id="29840-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="29840-151">**مثال:** مستوي قائمة مكونات الصنف 0، 1، 2</span><span class="sxs-lookup"><span data-stu-id="29840-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="29840-152">**التأخيرات** - يتم عرض مستويات قائمة مكونات الصنف علي انها مستويات قائمة مكونات الصنف لتخطيط التغطية مضروبةً في –1.</span><span class="sxs-lookup"><span data-stu-id="29840-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="29840-153">(بمعني آخر، يكون لها علامة سالبة).</span><span class="sxs-lookup"><span data-stu-id="29840-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="29840-154">**مثال:** مستوي قائمة مكونات الصنف –2، –1، 0</span><span class="sxs-lookup"><span data-stu-id="29840-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="29840-155">**رسالة الإجراء** – تظهر مستويات قائمة مكونات الصنف بالشكل المتوقع.</span><span class="sxs-lookup"><span data-stu-id="29840-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="29840-156">يتم حسابها من الأعلى إلى أسفل.</span><span class="sxs-lookup"><span data-stu-id="29840-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="29840-157">**مثال:** مستوي قائمة مكونات الصنف 0، 1، 2</span><span class="sxs-lookup"><span data-stu-id="29840-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="29840-158">**التأكيد التلقائي** – يتم عرض مستويات قائمة مكونات الصنف كـ 999 ناقص مستوى قائمة مكونات الصنف لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="29840-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="29840-159">**مثال:** مستوي قائمة مكونات الصنف 999، 998، 997</span><span class="sxs-lookup"><span data-stu-id="29840-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="29840-160">يلخص الجدول التالي السلوك.</span><span class="sxs-lookup"><span data-stu-id="29840-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="29840-161">مستوي قائمة مكونات الصنف المعروض</span><span class="sxs-lookup"><span data-stu-id="29840-161">BOM level that is shown</span></span> | <span data-ttu-id="29840-162">الصنف النهائي</span><span class="sxs-lookup"><span data-stu-id="29840-162">End item</span></span> | <span data-ttu-id="29840-163">المكون الفرعي</span><span class="sxs-lookup"><span data-stu-id="29840-163">Subcomponent</span></span> | <span data-ttu-id="29840-164">المادة الخام</span><span class="sxs-lookup"><span data-stu-id="29840-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="29840-165">التخطيط للتغطية</span><span class="sxs-lookup"><span data-stu-id="29840-165">Coverage planning</span></span> | <span data-ttu-id="29840-166">0</span><span class="sxs-lookup"><span data-stu-id="29840-166">0</span></span> | <span data-ttu-id="29840-167">1</span><span class="sxs-lookup"><span data-stu-id="29840-167">1</span></span> | <span data-ttu-id="29840-168">2</span><span class="sxs-lookup"><span data-stu-id="29840-168">2</span></span> |
| <span data-ttu-id="29840-169">التأخيرات</span><span class="sxs-lookup"><span data-stu-id="29840-169">Delays</span></span> | <span data-ttu-id="29840-170">0</span><span class="sxs-lookup"><span data-stu-id="29840-170">0</span></span> | <span data-ttu-id="29840-171">–1</span><span class="sxs-lookup"><span data-stu-id="29840-171">–1</span></span> | <span data-ttu-id="29840-172">–2</span><span class="sxs-lookup"><span data-stu-id="29840-172">–2</span></span> |
| <span data-ttu-id="29840-173">رسالة إجراء</span><span class="sxs-lookup"><span data-stu-id="29840-173">Action message</span></span> | <span data-ttu-id="29840-174">0</span><span class="sxs-lookup"><span data-stu-id="29840-174">0</span></span> | <span data-ttu-id="29840-175">1</span><span class="sxs-lookup"><span data-stu-id="29840-175">1</span></span> | <span data-ttu-id="29840-176">2</span><span class="sxs-lookup"><span data-stu-id="29840-176">2</span></span> |
| <span data-ttu-id="29840-177">التنفيذ التلقائي</span><span class="sxs-lookup"><span data-stu-id="29840-177">Auto-firming</span></span> | <span data-ttu-id="29840-178">999</span><span class="sxs-lookup"><span data-stu-id="29840-178">999</span></span> | <span data-ttu-id="29840-179">998</span><span class="sxs-lookup"><span data-stu-id="29840-179">998</span></span> | <span data-ttu-id="29840-180">997</span><span class="sxs-lookup"><span data-stu-id="29840-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="29840-181">تمثيل التقدم</span><span class="sxs-lookup"><span data-stu-id="29840-181">Visualize progress</span></span>

<span data-ttu-id="29840-182">إذا قمت بعرض مهمة تخطيط رئيسيه قيد التشغيل حاليا، يتم عرض التقدم من خلال ألوان الموجودة في مخطط Gantt.</span><span class="sxs-lookup"><span data-stu-id="29840-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="29840-183">تنطبق الألوان التالية على النسق الأزرق.</span><span class="sxs-lookup"><span data-stu-id="29840-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="29840-184">بالنسبة لنسق الألوان الأخرى ، ستختلف ألوان.</span><span class="sxs-lookup"><span data-stu-id="29840-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="29840-185">**ازرق داكن** – مهام التخطيط المكتملة.</span><span class="sxs-lookup"><span data-stu-id="29840-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="29840-186">**برتقالي** -المهمة قيد التقدم في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="29840-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="29840-187">**ازرق فاتح** - تقدير المهام المتبقية.</span><span class="sxs-lookup"><span data-stu-id="29840-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="29840-188">يتم عرض اللون فقط على المستوي الأقل في مخطط Gantt.</span><span class="sxs-lookup"><span data-stu-id="29840-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="29840-189">حدد **توسيع الكل** لعرض كافة المهام الموجودة في مهمة التخطيط الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="29840-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="29840-190">يعتمد تقدير المهام المتبقية على وظائف التخطيط الرئيسية التاريخية.</span><span class="sxs-lookup"><span data-stu-id="29840-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="29840-191">تشغيل التخطيط الرئيسي وتعقب وقت المعالجة</span><span class="sxs-lookup"><span data-stu-id="29840-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="29840-192">في لوحة المعلومات الافتراضية، حدد **‏‫التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="29840-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="29840-193">في حقل **الخطة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="29840-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="29840-194">حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="29840-194">Select **Run**.</span></span>
1. <span data-ttu-id="29840-195">قم بتعيين خيار **تعقب وقت المعالجة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="29840-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="29840-196">في الحقل **عدد السلاسل**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="29840-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="29840-197">في علامة التبويب السريعة **السجلات المُراد تضمينها**، حدد **تصفية**.</span><span class="sxs-lookup"><span data-stu-id="29840-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="29840-198">في الشبكة، حدد الصف الذي فيه تعيين حقل **الحقل** إلى **قم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="29840-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="29840-199">في حقل **المعايير**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="29840-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="29840-200">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="29840-200">Select **OK**.</span></span>
