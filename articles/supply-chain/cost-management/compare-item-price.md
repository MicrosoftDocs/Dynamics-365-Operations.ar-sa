---
title: تقرير مقارنة تخزين أسعار الأصناف
description: التعرف على كيفية إنشاء تقرير مقارنة تخزين أسعار الأصناف ثم استعرض و/أو صدّر النتيجة.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6c8c72a631d361d7dffb8d18e00636e51e7998d3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201929"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="c4077-103">تقرير مقارنة تخزين أسعار الأصناف</span><span class="sxs-lookup"><span data-stu-id="c4077-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4077-104">يوضح هذا الموضوع كيفية تشغيل تقرير **مقارنة تخزين أسعار الصنف** وتوفير المخرجات رقميًا، إما كصفحة تفاعلية في Dynamics 365 Supply Chain Management، أو كمستند مصدّر في أية تنسيقات متعددة.</span><span class="sxs-lookup"><span data-stu-id="c4077-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="c4077-105">عندما تقوم بعرض التقرير في المستعرض، يتم تسوية الأعمدة والأرصدة التجميعية بشكل حيوي، وذلك وفقًا للتخطيط الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="c4077-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="c4077-106">يمكنك فرز النتائج وتصفيتها والتنقل لأسفل إلى البيانات وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="c4077-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="c4077-107">يتم تخزين نتائج التقرير في كيان بيانات **مقارنة أسعار الأصناف**، الذي يتيح لك تصفية النتائج وتصديرها إلى تنسيق مثل CSV أو Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c4077-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="c4077-108">يعتبر تقرير **مقارنة تخزين أسعار الأصناف** مفيدًا في الحالات التي تحتوي بها المخرجات على العديد من الأصناف.</span><span class="sxs-lookup"><span data-stu-id="c4077-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="c4077-109">على سبيل المثال، ستحتوي المخرجات على العديد من الأصناف إذا كان لديك أكثر من 40,000 صنفًا يحتفظ بسعر صنف معلق في إصدار التكاليف.</span><span class="sxs-lookup"><span data-stu-id="c4077-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="c4077-110">تمكين مقارنة تخزين أسعار الأصناف</span><span class="sxs-lookup"><span data-stu-id="c4077-110">Enable compare item prices storage</span></span>

<span data-ttu-id="c4077-111">قبل أن تتمكن من استخدام هذه الميزة، فإنه يجب عليك تمكينه على النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c4077-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="c4077-112">يمكن للمسؤولين [استخدام إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) الإعدادات للتحقق من حالة الميزة وتمكينها إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c4077-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="c4077-113">هنا، يتم إدراج الميزة كـ:</span><span class="sxs-lookup"><span data-stu-id="c4077-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="c4077-114">**الوحدة** - إدارة التكلفة</span><span class="sxs-lookup"><span data-stu-id="c4077-114">**Module** - Cost management</span></span>
- <span data-ttu-id="c4077-115">**اسم الميزة** مقارنة تخزين سعر الصنف</span><span class="sxs-lookup"><span data-stu-id="c4077-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="c4077-116">إنشاء تقرير مقارنة تخزين أسعار الأصناف</span><span class="sxs-lookup"><span data-stu-id="c4077-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="c4077-117">اتبع هذه الخطوات لإنشاء تقرير **مقارنة تخزين أسعار الأصناف** وتخزينه:</span><span class="sxs-lookup"><span data-stu-id="c4077-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="c4077-118">انتقل إلى **إدارة التكاليف > الاستعلامات والتقارير > تقارير التكلفة المحددة مسبقًا > مقارنة تخزين أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="c4077-119">حدد **جديد** لفتح جزء **مقارنة أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="c4077-120">قم بتعيين الخيارات التالية لتحديد الأسعار التي سيتم مقارنتها في التقرير الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="c4077-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="c4077-121">في علامة التبويب السريعة **المعلمات**، أطلق على التقرير **اسم** فريد واستخدم الحقول في الأقسام **الأسعار المعلقة للمقارنة بها** و **الأسعار المستخدمة في المقارنة** لتحديد الأسعار والتواريخ المراد مقارنتها.</span><span class="sxs-lookup"><span data-stu-id="c4077-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="c4077-122">في علامة التبويب السريعة **السجلات المراد تضمينها**، قم بإعداد عوامل التصفية والقيود لتحديد البيانات التي سيتم تضمينها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="c4077-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="c4077-123">في علامة التبويب السريعة **تشغيل في الخلفية**، قم بإعداد الكيفية التي تريد بها إنشاء التقرير ومتى والتكرار.</span><span class="sxs-lookup"><span data-stu-id="c4077-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="c4077-124">يتم تنفيذ هذا التقرير دائمًا كجزء من مهمة مجموعة.</span><span class="sxs-lookup"><span data-stu-id="c4077-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="c4077-125">حدد **موافق** لتطبيق الإعدادات الخاصة بك وإغلاق الجزء.</span><span class="sxs-lookup"><span data-stu-id="c4077-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="c4077-126">بعد اكتمال وظيفة المجموعة، فإنه سيتم إدراجها في الصفحة **مقارنة تخزين أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="c4077-127">قد تحتاج إلى إعادة تنشيط الصفحة للاطلاع على التقرير.</span><span class="sxs-lookup"><span data-stu-id="c4077-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="c4077-128">استكشاف تقرير مقارنة تخزين أسعار الأصناف</span><span class="sxs-lookup"><span data-stu-id="c4077-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="c4077-129">بعد أن تنتهي من إنشاء تقرير، فإنه يمكنك عرضه واستكشافه في أي وقت كما يلي:</span><span class="sxs-lookup"><span data-stu-id="c4077-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="c4077-130">انتقل إلى **إدارة التكاليف > الاستعلامات والتقارير > تقارير التكلفة المحددة مسبقًا > مقارنة تخزين أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="c4077-131">حدد تقرير من القائمة.</span><span class="sxs-lookup"><span data-stu-id="c4077-131">Select a report from the list.</span></span>

1. <span data-ttu-id="c4077-132">قم بأحد الإجراءين التاليين:</span><span class="sxs-lookup"><span data-stu-id="c4077-132">Do one of the following:</span></span>

    - <span data-ttu-id="c4077-133">حدد **نظرة عامة** للحصول على نظرة عامة عن نتائج التقرير.</span><span class="sxs-lookup"><span data-stu-id="c4077-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="c4077-134">حدد **عرض تفاصيل** للحصول على عرض أكثر تفصيلاً للتقرير الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c4077-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="c4077-135">بعد أن يتم فتح طريقة العرض المحددة، يمكنك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="c4077-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="c4077-136">حدد تقريبًا أي عنوان عمود لفرز الجدول أو تصفيته حسب القيم الموجودة في هذا العمود، تمامًا كما هو الحال مع معظم النماذج القياسية في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c4077-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="c4077-137">ملاحظة، لا يمكنك فرز أو تصفية عمود **صافي سعر التغيير %** لأنه حقل محسوب.</span><span class="sxs-lookup"><span data-stu-id="c4077-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="c4077-138">حدد **عرض البُعد** لفتح جزء حيث يمكنك اختيار عمود البُعد الذي سيتم تضمينه في النموذج.</span><span class="sxs-lookup"><span data-stu-id="c4077-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="c4077-139">قم بتعيين **حفظ الإعداد** على **نعم** إذا كنت ترغب في حفظ هذه الإعدادات لكي يتم الاحتفاظ بها في المرة التالية التي تقوم بها بفتح التقرير.</span><span class="sxs-lookup"><span data-stu-id="c4077-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="c4077-140">حدد **موافق** لتطبيق الإعدادات الخاصة بك والإغلاق.</span><span class="sxs-lookup"><span data-stu-id="c4077-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="c4077-141">حدد أي صف في النموذج ثم حدد **عرض التفاصيل** لعرض المزيد من المعلومات حول الصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c4077-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="c4077-142">ستتمكن من التنقل لأسفل داخل البيانات هنا.</span><span class="sxs-lookup"><span data-stu-id="c4077-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="c4077-143">حدد أي صف في النموذج ثم حدد **عرض مخطط المقارنة** لمشاهدة تمثيل رسومي تفاعلي للنتائج الخاصة بك كما ترتبط بالصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c4077-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="c4077-144">يمكنك استكشاف هذه النتائج عن طريق تحديد العديد من العناصر الرسومية في المخطط ووسيلة إيضاح المخطط.</span><span class="sxs-lookup"><span data-stu-id="c4077-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="c4077-145">حدد أي صف في النموذج ثم حدد **عرض تفاصيل الحساب** لعرض المزيد من المعلومات حول الحسابات المرتبطة بالصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c4077-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="c4077-146">ستتمكن من التنقل لأسفل داخل البيانات هنا.</span><span class="sxs-lookup"><span data-stu-id="c4077-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="c4077-147">تصدير تقرير مقارنة تخزين أسعار الأصناف</span><span class="sxs-lookup"><span data-stu-id="c4077-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="c4077-148">يتم تخزين كل تقرير تقوم بإنشاؤه في كيان بيانات **مقارنه أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="c4077-149">يمكنك استخدام الميزات القياسية لإدارة البيانات الخاصة بـ Supply Chain Management لتصدير البيانات من هذا الكيان لأي تنسيق بيانات مدعوم، بما في ذلك CSV أو Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c4077-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="c4077-150">فيما يلي مثال على كيفية تصدير تقرير **مقارنة تخزين أسعار الأصناف**:</span><span class="sxs-lookup"><span data-stu-id="c4077-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="c4077-151">انتقل إلى **نظام الإدارة > مساحات العمل > إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="c4077-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="c4077-152">حدد الزر **تصدير** الموجود في القسم **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="c4077-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="c4077-153">تفتح الصفحة **تصدير**، التي ستستخدمها لإعداد وظيفة التصدير الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c4077-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="c4077-154">أبدا بإطلاق **اسم مجموعة** على الوظيفة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c4077-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="c4077-155">في القسم **الكيانات المحددة**، حدد **إضافة كيان** لفتح مربع حوار حيث يمكنك تعيين الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4077-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="c4077-156">**اسم الكيان** - حدد **مقارنة أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="c4077-157">**تنسيق بيانات الهدف** - اختر التنسيق الذي ترغب في التصدير إليه.</span><span class="sxs-lookup"><span data-stu-id="c4077-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="c4077-158">حدد **إضافة** لإضافة الصف الجديد، ثم حدد **إغلاق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="c4077-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="c4077-159">عادة، ستقوم بتصدير تقرير واحد في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="c4077-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="c4077-160">للقيام بذلك، قم بإعداد **عامل تصفية** للصف الذي أضفته للتو إلى جزء **استعلام**.</span><span class="sxs-lookup"><span data-stu-id="c4077-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="c4077-161">سيسمح لك هذا بتحديد التقارير من الكيان **مقارنة أسعار الأصناف** الذي ترغب في تضمينه في التصدير الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c4077-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="c4077-162">قم بتعيين خيارات التصفية التالية لتصدير تقرير واحد:</span><span class="sxs-lookup"><span data-stu-id="c4077-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="c4077-163">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة صف جديد.</span><span class="sxs-lookup"><span data-stu-id="c4077-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="c4077-164">قم بتعيين **جدول** إلى **مقارنة أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="c4077-165">قم بتعيين **جدول مشتق** إلى **مقارنة أسعار الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c4077-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="c4077-166">قم بتعيين **الحقل** إلى الحقل الذي ترغب في إجراء التصفية باستخدامه.</span><span class="sxs-lookup"><span data-stu-id="c4077-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="c4077-167">عادة، ستستخدم **اسم التنفيذ** أو **وقت التنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="c4077-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="c4077-168">قم بتعيين **المعايير** إلى القيمة من الحقل المحدد الذي تريد البحث عنه (إما اسم التقرير أو وقت إنشاء التقرير).</span><span class="sxs-lookup"><span data-stu-id="c4077-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="c4077-169">إذا لزم الأمر، قم بإضافة المزيد من الصفوف إلى الجدول **النطاق** حتى تقوم بتعريف التقرير الذي تبحث عنه بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="c4077-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="c4077-170">حدد **موافق** لحفظ الإعدادات الخاصة بك والإغلاق.</span><span class="sxs-lookup"><span data-stu-id="c4077-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="c4077-171">حدد **حفظ** لحفظ إعداد التصدير الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c4077-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="c4077-172">افتح علامة التبويب **خيارات التصدير** وحدد **تصدير الآن** لإنشاء ملف التصدير.</span><span class="sxs-lookup"><span data-stu-id="c4077-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="c4077-173">تفتح صفحة **ملخص التنفيذ**، حيث يمكنك عرض حالة وظيفة التصدير وقائمة بالكيانات التي تم تصديرها.</span><span class="sxs-lookup"><span data-stu-id="c4077-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="c4077-174">حدد الكيان **مقارنة أسعار الأصناف** الذي تم إدراجه في المنطقة **حالة معالجة الكيان** ثم حدد **تنزيل ملف** لتنزيل البيانات المصدرة من ذلك الكيان.</span><span class="sxs-lookup"><span data-stu-id="c4077-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="c4077-175">لمزيد من المعلومات حول كيفية استخدام إدارة البيانات لتصدير البيانات، راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="c4077-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
