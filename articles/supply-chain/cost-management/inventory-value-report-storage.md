---
title: ‏تقرير تخزين قيمة المخزون
description: يوضح هذا الموضوع كيفية تشغيل تقرير تخزين قيمة المخزون وتوفير المخرجات رقميًا، إما كصفحة تفاعلية في Microsoft Dynamics 365 Supply Chain Management، أو كمستند مصدّر بأي من التنسيقات المتعددة.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0f54c02fc828d60f4ddb28be932bbf8eb137ee92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008134"
---
# <a name="inventory-value-storage-report"></a><span data-ttu-id="1519d-103">‏تقرير تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="1519d-103">Inventory value storage report</span></span>

<span data-ttu-id="1519d-104">يوضح هذا الموضوع كيفية تشغيل تقرير **تخزين قيمة المخزون** وتوفير المخرجات رقميًا، إما كصفحة تفاعلية في Microsoft Dynamics 365 Supply Chain Management أو كمستند مصدّر بأي من التنسيقات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="1519d-104">This topic explains how to run an **Inventory value storage** report and make the output available digitally, either as an interactive page in Microsoft Dynamics 365 Supply Chain Management or as an exported document in any of several formats.</span></span>

<span data-ttu-id="1519d-105">عندما تقوم بعرض التقرير في المستعرض، يتم تسوية الأعمدة والأرصدة التجميعية بشكل ديناميكي، وذلك وفقًا للتخطيط الذي قمت بتكوينه.</span><span class="sxs-lookup"><span data-stu-id="1519d-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on the layout that you've configured.</span></span> <span data-ttu-id="1519d-106">يمكنك فرز النتائج وتصفيتها والتنقل لأسفل إلى البيانات وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="1519d-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="1519d-107">يتم تخزين نتائج التقرير في كيان بيانات **قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-107">Report results are stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="1519d-108">بالتالي، يمكنك تصفية النتائج وتصديرها إلى تنسيق مثل القيم المفصولة بفاصله (CSV) أو تنسيق Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1519d-108">Therefore, you can filter and export the results to a format such as comma-separated values (CSV) or Microsoft Excel format.</span></span>

<span data-ttu-id="1519d-109">يعتبر تقرير **تخزين قيمة المخزون** مفيدًا عندما يحتوي الإخراج على العديد من البنود.</span><span class="sxs-lookup"><span data-stu-id="1519d-109">The **Inventory value storage** report is helpful when the output contains many lines.</span></span> <span data-ttu-id="1519d-110">على سبيل المثال، لديك 50,000 صنف، وتم إنشاء 300 متجر كمستودعات.</span><span class="sxs-lookup"><span data-stu-id="1519d-110">For example, you have 50,000 items, and 300 stores have been created as warehouses.</span></span> <span data-ttu-id="1519d-111">في هذه الحالة، إذا طلبت أرصده نهاية المخزون حسب الصنف والموقع والمستودع، سيحتوي الإخراج على العديد من البنود.</span><span class="sxs-lookup"><span data-stu-id="1519d-111">In this case, if you request inventory ending balances by item, site, and warehouse, the output will contain many lines.</span></span>

> [!NOTE]
> <span data-ttu-id="1519d-112">ولن يشتمل التقرير على الإجماليات الفرعية التي تم تحديدها في تخطيط التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-112">The report won't include subtotals that are defined in the report layout.</span></span> <span data-ttu-id="1519d-113">ولن يتضمن أيضًا أرصده دفتر الأستاذ العام، حتى في حالة تحديدها في تخطيط التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-113">It also won't include general ledger balances, even when they are defined in the report layout.</span></span> <span data-ttu-id="1519d-114">يجب القيام بالتسوية إلى دفتر الأستاذ العام باستخدام موازين المراجعة.</span><span class="sxs-lookup"><span data-stu-id="1519d-114">Reconciliation to the general ledger must be done by using trial balances.</span></span>

## <a name="turn-on-the-inventory-value-storage-feature"></a><span data-ttu-id="1519d-115">تشغيل ميزة تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="1519d-115">Turn on the Inventory value storage feature</span></span>

<span data-ttu-id="1519d-116">قبل أن تتمكن من إنشاء تقرير **تخزين قيمة المخزون**، يجب تشغيل الميزة في النظام.</span><span class="sxs-lookup"><span data-stu-id="1519d-116">Before you can generate an **Inventory value storage** report, you must turn on the feature in your system.</span></span> <span data-ttu-id="1519d-117">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="1519d-117">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1519d-118">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="1519d-118">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1519d-119">**الوحدة** - إدارة التكلفة</span><span class="sxs-lookup"><span data-stu-id="1519d-119">**Module** – Cost management</span></span>
- <span data-ttu-id="1519d-120">**اسم الميزة** – تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="1519d-120">**Feature name** – Inventory value storage</span></span>

## <a name="generate-an-inventory-value-storage-report"></a><span data-ttu-id="1519d-121">إنشاء ‏تقرير تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="1519d-121">Generate an Inventory value storage report</span></span>

<span data-ttu-id="1519d-122">اتبع هذه الخطوات لإنشاء تقرير **تخزين قيمة المخزون** وتخزينه:</span><span class="sxs-lookup"><span data-stu-id="1519d-122">Follow these steps to generate and store an **Inventory value storage** report.</span></span>

1. <span data-ttu-id="1519d-123">انتقل إلى **إدارة التكاليف \> الاستعلامات والتقارير \> تخزين تقرير قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-123">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="1519d-124">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1519d-124">Select **New**.</span></span>
1. <span data-ttu-id="1519d-125">في مربع حوار **قيمة المخزون** الذي يظهر، قم بتعيين القيم التالية لتحديد السجلات التي سيتم تضمينها في التقرير:</span><span class="sxs-lookup"><span data-stu-id="1519d-125">In the **Inventory value** dialog box that appears, set the following values to define which records are included in your report:</span></span>

    - <span data-ttu-id="1519d-126">في علامة التبويب السريعة **المعلمات**، أدخل اسمًا فريدًا للتقرير، واستخدم الحقول الموجودة في قسم **فتره التاريخ** لتحديد السجلات التي سيتم تضمينها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-126">On the **Parameters** FastTab, enter a unique name for the report, and use the fields in the **Date interval** section to define which records are included in the report.</span></span> <span data-ttu-id="1519d-127">لتحديد فترة التاريخ، يمكنك إما تحديد نطاق معد مسبقًا (يتعلق بتاريخ إنشاء التقرير) في حقل **‏‫كود الفاصل الزمني‬**، أو تحديد تواريخ معينة في حقول **من تاريخ** و **إلى تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="1519d-127">To define the date interval, you can either select a preset range (relative to the report generation date) in the **Date interval code** field, or select specific dates in the **From date** and **To date** fields.</span></span>
    - <span data-ttu-id="1519d-128">في علامة التبويب السريعة **السجلات المراد تضمينها**، قم بإعداد عوامل التصفية والقيود لتحديد أي البيانات سيتم تضمينها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-128">On the **Records to include** FastTab, set up filters and constraints to define which data is included in the report.</span></span>
    - <span data-ttu-id="1519d-129">في علامة التبويب السريعة **تشغيل في الخلفية**، حدد كيف ومتى وعدد المرات التي يتم فيها إنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-129">On the **Run in the background** FastTab, specify how, when, and how often the report is generated.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1519d-130">يتم تشغيل هذا التقرير دائمًا كجزء من مهمة مجموعة.</span><span class="sxs-lookup"><span data-stu-id="1519d-130">This report is always run as part of a batch job.</span></span>

1. <span data-ttu-id="1519d-131">حدد **موافق** لتطبيق إعداداتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="1519d-131">Select **OK** to apply your settings and close the dialog box.</span></span>

<span data-ttu-id="1519d-132">بعد إكمال الوظيفة الدفعية، يتم سرد التقرير في صفحة **تخزين تقرير قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-132">After the batch job is completed, the report will be listed on the **Inventory value report storage** page.</span></span> <span data-ttu-id="1519d-133">قد تحتاج إلى تحديث الصفحة لعرض التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-133">You might have to refresh the page to see the report.</span></span>

## <a name="explore-an-inventory-value-storage-report"></a><span data-ttu-id="1519d-134">اكتشف ‏تقرير تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="1519d-134">Explore an Inventory value storage report</span></span>

<span data-ttu-id="1519d-135">بعد أن تنتهي من إنشاء تقرير، فإنه يمكنك عرضه واستكشافه في أي وقت باتباع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="1519d-135">After you've generated a report, you can view and explore it at any time by following these steps.</span></span>

1. <span data-ttu-id="1519d-136">انتقل إلى **إدارة التكاليف \> الاستعلامات والتقارير \> تخزين تقرير قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-136">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="1519d-137">حدد أحد التقارير في القائمة.</span><span class="sxs-lookup"><span data-stu-id="1519d-137">Select a report in the list.</span></span>
1. <span data-ttu-id="1519d-138">حدد **عرض تفاصيل** لإظهار محتوى التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-138">Select **View details** to show the report content.</span></span>
1. <span data-ttu-id="1519d-139">استكشف التقرير باتباع أي من الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="1519d-139">Explore the report by following any of these steps:</span></span>

    - <span data-ttu-id="1519d-140">كما هو الحال مع معظم الصفحات القياسية في Supply Chain Management، يمكنك تحديد تقريبًا أي عنوان عمود لفرز أو تصفية الشبكة حسب القيم الموجودة في هذا العمود</span><span class="sxs-lookup"><span data-stu-id="1519d-140">As for most standard pages in Supply Chain Management, you can select almost any column heading to sort or filter the grid by the values in that column.</span></span>
    - <span data-ttu-id="1519d-141">استخدم حقل **التصفية** لتصفية التقرير حسب أية قيمة في أي من الأعمدة المتعددة المتاحة.</span><span class="sxs-lookup"><span data-stu-id="1519d-141">Use the **Filter** field to filter the report by any value in any of several available columns.</span></span>
    - <span data-ttu-id="1519d-142">استخدم قائمة عرض (أعلى حقل **التصفية**) لحفظ المجموعات المفضلة الخاصة بك وتحميلها من خيارات الفرز والتصفية.</span><span class="sxs-lookup"><span data-stu-id="1519d-142">Use the view menu (above the **Filter** field) to save and load your favorite combinations of sort and filter options.</span></span>

## <a name="export-an-inventory-value-storage-report"></a><span data-ttu-id="1519d-143">تصدير ‏تقرير تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="1519d-143">Export an Inventory value storage report</span></span>

<span data-ttu-id="1519d-144">يتم تخزين كل تقرير تقوم بإنشائه في كيان بيانات **قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-144">Every report that you generate is stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="1519d-145">يمكنك استخدام الميزات القياسية لإدارة البيانات الخاصة بـ Supply Chain Management لتصدير البيانات من هذا الكيان لأي تنسيق بيانات مدعوم، مثل CSV أو تنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="1519d-145">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, such as CSV or Excel format.</span></span>

<span data-ttu-id="1519d-146">يوضح المثال التالي كيفية تصدير تقرير **قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-146">The following example shows how to export an **Inventory value report** report.</span></span>

1. <span data-ttu-id="1519d-147">اذهب إلى **إدارة النظام \> مساحات العمل \> إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="1519d-147">Go to **System administration \> Workspaces \> Data management**.</span></span>
1. <span data-ttu-id="1519d-148">في قسم **استيراد / تصدير**، حدد تجانب **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="1519d-148">In the **Import / Export** section, select the **Export** tile.</span></span> 
1. <span data-ttu-id="1519d-149">في صفحة **تصدير** التي تظهر، ستقوم بإعداد مهمة التصدير.</span><span class="sxs-lookup"><span data-stu-id="1519d-149">On the **Export** page that appears, you will set up the export job.</span></span> <span data-ttu-id="1519d-150">أدخل أولا اسم مجموعة للمهمة.</span><span class="sxs-lookup"><span data-stu-id="1519d-150">First enter a group name for the job.</span></span>
1. <span data-ttu-id="1519d-151">في قسم **الكيانات المحددة**، حدد **إضافة كيان**.</span><span class="sxs-lookup"><span data-stu-id="1519d-151">In the **Selected entities** section, select **Add entity**.</span></span>
1. <span data-ttu-id="1519d-152">في مربع الحوار الذي يظهر، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="1519d-152">In the dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="1519d-153">**اسم الكيان** – حدد **قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-153">**Entity name** – Select **Inventory value**.</span></span>
    - <span data-ttu-id="1519d-154">**تنسيق البيانات المستهدفة** - حدد التنسيق الذي سيتم تصدير البيانات إليه.</span><span class="sxs-lookup"><span data-stu-id="1519d-154">**Target data format** – Select the format to export data to.</span></span>

1. <span data-ttu-id="1519d-155">حدد **إضافة** لإضافة الصف الجديد، ثم حدد **إغلاق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="1519d-155">Select **Add** to add the new row, and then select **Close** to close the dialog box.</span></span>
1. <span data-ttu-id="1519d-156">في العادة، ستقوم بتصدير تقرير واحد في المرة.</span><span class="sxs-lookup"><span data-stu-id="1519d-156">Usually, you will export one report at a time.</span></span> <span data-ttu-id="1519d-157">لتصدير تقرير واحد، قم بإعداد عامل تصفية للصف الذي قمت للتو بإضافته إلى مربع حوار **الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="1519d-157">To export a single report, set up a filter for the row that you just added to the **Inquiry** dialog box.</span></span> <span data-ttu-id="1519d-158">بهذه الطريقة، يمكنك تحديد التقرير من الكيان **قيمة المخزون** الذي سيتم تضمينه في عملية التصدير.</span><span class="sxs-lookup"><span data-stu-id="1519d-158">In this way, you can define which report from the **Inventory value** entity is included in your export.</span></span> <span data-ttu-id="1519d-159">اتبع هذه الخطوات لتعيين خيارات التصفية التالية لتصدير تقرير واحد:</span><span class="sxs-lookup"><span data-stu-id="1519d-159">Follow these steps to set the following filter options to export a single report:</span></span>

    1. <span data-ttu-id="1519d-160">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة صف.</span><span class="sxs-lookup"><span data-stu-id="1519d-160">On the **Range** tab, select **Add** to add a row.</span></span>
    2. <span data-ttu-id="1519d-161">قتم بتعيين‏‎ حقل **الجدول** إلى **قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-161">Set the **Table** field to **Inventory value**.</span></span>
    3. <span data-ttu-id="1519d-162">قتم بتعيين‏‎ حقل **جدول مشتق** إلى **قيمة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1519d-162">Set the **Derived table** field to **Inventory value**.</span></span>
    4. <span data-ttu-id="1519d-163">قم بتعيين حقل **الحقل** إلى الحقل الذي ترغب في إجراء التصفية باستخدامه.</span><span class="sxs-lookup"><span data-stu-id="1519d-163">Set the **Field** field to the field that you want to filter by.</span></span> <span data-ttu-id="1519d-164">في العادة، ستستخدم حقل **اسم التنفيذ** و/أو حقل **وقت التنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="1519d-164">Usually, you will use the **Execution name** field and/or the **Execution time** field.</span></span>
    5. <span data-ttu-id="1519d-165">قم بتعيين حقل **المعايير** إلى القيمة التي تريد البحث عنها في الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="1519d-165">Set the **Criteria** field to the value that you want to look for in the selected field.</span></span> <span data-ttu-id="1519d-166">(إذا قمت بتحديد الحقل **اسم التنفيذ** في الخطوة السابقة، ستكون هذه القيمة اسم التقرير.</span><span class="sxs-lookup"><span data-stu-id="1519d-166">(If you selected the **Execution name** field in the previous step, this value will be the name of the report.</span></span> <span data-ttu-id="1519d-167">وإذا قمت بتحديد الحقل **وقت التنفيذ**، سيكون هو وقت إنشاء التقرير.)</span><span class="sxs-lookup"><span data-stu-id="1519d-167">If you selected the **Execution time** field, it will be the time when the report was generated.)</span></span>
    6. <span data-ttu-id="1519d-168">قم بإضافة المزيد من الصفوف إلى علامة تبويب **النطاق** حسب الحاجة، حتى تقوم بتعريف التقرير الذي تبحث عنه بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="1519d-168">Add more rows to the **Range** tab as you require, until you've uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="1519d-169">حدد **موافق** لحفظ إعداداتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="1519d-169">Select **OK** to save your settings and close the dialog box.</span></span>
1. <span data-ttu-id="1519d-170">حدد **حفظ** لحفظ إعداد التصدير الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1519d-170">Select **Save** to save your export setup.</span></span>
1. <span data-ttu-id="1519d-171">في علامة التبويب **خيارات التصدير**، حدد **تصدير الآن** لإنشاء ملف التصدير.</span><span class="sxs-lookup"><span data-stu-id="1519d-171">On the **Export options** tab, select **Export now** to generate the export file.</span></span>
1. <span data-ttu-id="1519d-172">في صفحة **ملخص التنفيذ** التي تظهر، يمكنك عرض حالة مهمة التصدير الخاصة بك وقائمة بالكيانات التي تم تصديرها.</span><span class="sxs-lookup"><span data-stu-id="1519d-172">On the **Execution summary** page that appears, you can view the status of your export job and a list of the entities that were exported.</span></span> <span data-ttu-id="1519d-173">في قسم **حالة معالجة الكيان**، حدد كيان **قيمة المخزون** في القائمة وحدد **تنزيل ملف** لتنزيل البيانات التي تم تصديرها من ذلك الكيان.</span><span class="sxs-lookup"><span data-stu-id="1519d-173">In the **Entity processing status** section, select the **Inventory value** entity in the list, and then select **Download file** to download the data that was exported from that entity.</span></span>

<span data-ttu-id="1519d-174">لمزيد من المعلومات حول كيفية استخدام إدارة البيانات لتصدير البيانات، راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="1519d-174">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
