---
title: استكشاف مشكلات الأداء وإصلاحها في تكوينات التقارير الإلكترونية
description: يشرح هذا الموضوع كيفية البحث عن مشكلات الأداء وإصلاحها في تكوينات التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216855"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="188e5-103">استكشاف مشكلات الأداء وإصلاحها في تكوينات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="188e5-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="188e5-104">يشرح هذا الموضوع كيفية البحث عن مشكلات الأداء وحلها في [التقارير الإلكترونية](general-electronic-reporting.md) (ER) [تكوينات](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="188e5-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="188e5-105">بشكل عام، يتكون تحقيق الأداء من عدة خطوات.</span><span class="sxs-lookup"><span data-stu-id="188e5-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="188e5-106">[جمع](#collecting-data) البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="188e5-107">قم بتحليل البيانات التي تم جمعها.</span><span class="sxs-lookup"><span data-stu-id="188e5-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="188e5-108">استنادًا إلى نتائج التحليل، استخدم تكوينات التقارير الإلكترونية [لإجراء التغييرات](#making-changes)، أو قرر جمع المزيد من البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="188e5-109">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="188e5-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="188e5-110">تحليل وقت التنفيذ</span><span class="sxs-lookup"><span data-stu-id="188e5-110">Analyze execution time</span></span>

<span data-ttu-id="188e5-111">يمكن أن يعتمد وقت التنفيذ على عوامل غير متوقعة، مثل المهام الأخرى التي يتم تشغيلها في البيئة نفسها والتخزين المؤقت الذي يستخدم البيانات عند استدعائها للمرة الأولى.</span><span class="sxs-lookup"><span data-stu-id="188e5-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="188e5-112">لذلك، يجب تكرار التنفيذ والقياس عدة مرات.</span><span class="sxs-lookup"><span data-stu-id="188e5-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="188e5-113">في بعض الأحيان، لا تحدث مشكلات الأداء بسبب تكوين تنسيق التقارير الإلكترونية المستخدم في إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="188e5-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="188e5-114">بدلاً من ذلك، تتم بسبب بواسطة الكود X++ المستخدمة لفتح تكوين تنسيق التقارير الإلكترونية ذلك.</span><span class="sxs-lookup"><span data-stu-id="188e5-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="188e5-115">في كل من [مركز الإجراءات](#infolog-time) أو [سجل الأحداث](#event-log-time)، انظر إلى وقت تنفيذ التقرير.</span><span class="sxs-lookup"><span data-stu-id="188e5-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="188e5-116">قم بمقارنة وقت تنفيذ التقرير مع إجمالي وقت التنفيذ في السيناريو.</span><span class="sxs-lookup"><span data-stu-id="188e5-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="188e5-117">إذا كان وقت تنفيذ التقرير أقل بكثير من إجمالي وقت التنفيذ، فضع في اعتبارك مقدار البيانات التي يعالجها التقرير:</span><span class="sxs-lookup"><span data-stu-id="188e5-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="188e5-118">إذا كان التقرير يعالج كمية صغيرة من البيانات، قد تتضمن المشكلة وقت تحميل التكوين.</span><span class="sxs-lookup"><span data-stu-id="188e5-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="188e5-119">إذا كان التقرير يعالج كمية كبيرة من البيانات، قد تتضمن المشكلة المعالجة المسبقة X++.</span><span class="sxs-lookup"><span data-stu-id="188e5-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="188e5-120">استخدم [محلل التتبع](#analyze-trace-parser-trace) لتحليل هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="188e5-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="188e5-121">بالنسبة للحالات الأخرى، راجع الأقسام التالية.</span><span class="sxs-lookup"><span data-stu-id="188e5-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="188e5-122">قم بتشغيل اختبارات متعددة تتضمن كميات مختلفة من البيانات لتحديد كيفية اعتماد وقت التنفيذ على مقدار البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="188e5-123">تحليل التتبعات باستخدام محلل التتبع</span><span class="sxs-lookup"><span data-stu-id="188e5-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="188e5-124">إعداد مثال صغير أو تجميع عدة تتبعات خلال أجزاء عشوائية من إنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="188e5-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="188e5-125">ثم، في [محلل التتبع](#trace-parser)، قم بإجراء تحليل قياسي من أسفل إلى أعلى، قم أجب على الأسئلة التالية:</span><span class="sxs-lookup"><span data-stu-id="188e5-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="188e5-126">ما أفضل الطرق من حيث استهلاك الوقت؟</span><span class="sxs-lookup"><span data-stu-id="188e5-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="188e5-127">ما الجزء من الوقت الإجمالي الذي تستخدمه هذه الأساليب؟</span><span class="sxs-lookup"><span data-stu-id="188e5-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="188e5-128">أجب على الأسئلة نفسها للاستعلامات.</span><span class="sxs-lookup"><span data-stu-id="188e5-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="188e5-129">إذا رأيت أن الأساليب مسبوقة ب "التقارير الإلكترونية"، انتقل إلى القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="188e5-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="188e5-130">إذا رأيت أن تلك الأساليب أو الاستعلامات نشأت في مجموعة التطبيقات، خذ بعين الاعتبار تحسينات عامة (على سبيل المثال، إنشاء فهارس).</span><span class="sxs-lookup"><span data-stu-id="188e5-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="188e5-131">قم بتحليل عدد الاستدعاءات.</span><span class="sxs-lookup"><span data-stu-id="188e5-131">Analyze the number of calls.</span></span> <span data-ttu-id="188e5-132">إذا كان الرقم أعلى بكثير من المتوقع، خذ بعين الاعتبار تخزين المؤقت للعقد المطابقة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="188e5-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="188e5-133">تحليل استدعاءات قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="188e5-133">Analyze database calls</span></span>

<span data-ttu-id="188e5-134">قم بإعداد مثال يحتوي على كمية صغيرة من البيانات، بحيث يمكنك جمع [تتبع التقارير الإلكترونية](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="188e5-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="188e5-135">ثم افتح التتبع في مصمم تعيين نموذج التقارير الإلكترونية، وانظر إلى أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="188e5-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="188e5-136">أجب عن الأسئلة التالية:</span><span class="sxs-lookup"><span data-stu-id="188e5-136">Answer the following questions:</span></span>

- <span data-ttu-id="188e5-137">هل هناك أي تكرار للاستعلام؟</span><span class="sxs-lookup"><span data-stu-id="188e5-137">Is there any query duplication?</span></span> <span data-ttu-id="188e5-138">إذا كان هناك تكرار، خذ بعين الاعتبار أحد الإصلاحات التالية:</span><span class="sxs-lookup"><span data-stu-id="188e5-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="188e5-139">[استخدم التخزين المؤقت](#use-caching) إذا كنت تعتقد أن هناك العديد من الاستدعاءات داخل سجل أصل واحد.</span><span class="sxs-lookup"><span data-stu-id="188e5-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="188e5-140">[استخدم حقل محسوب ذا معلمات مخزن مؤقتًا](#cached-parameterized) إذا كنت تعتقد أن هناك استدعاءات إلى نفس السجل داخل سجلات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="188e5-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="188e5-141">[استخدم مصدر البيانات **JOIN** ](#use-join-datasource) إذا كان يجب عليك قراءة عدد كبير من السجلات المختلفة من قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="188e5-142">هل يتوافق عدد الاستعلامات والسجلات التي تم إحضارها مع إجمالي كمية البيانات؟</span><span class="sxs-lookup"><span data-stu-id="188e5-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="188e5-143">على سبيل المثال، إذا كان المستند يحتوي على 10 أسطر، هل توضح الإحصائيات أن التقرير يستخرج 10 أسطر أو 1000 سطر؟</span><span class="sxs-lookup"><span data-stu-id="188e5-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="188e5-144">إذا كان لديك عدد كبير من السجلات التي تم إحضارها، خذ بعين الاعتبار أحد الإصلاحات التالية:</span><span class="sxs-lookup"><span data-stu-id="188e5-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="188e5-145">[استخدم الوظيفة **FILTER** بدلاً من الوظيفة **WHERE** ](#filter) لمعالجة البيانات على جانب خادم SQL.</span><span class="sxs-lookup"><span data-stu-id="188e5-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="188e5-146">استخدم التخزين المؤقت لتجنب إحضار نفس البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="188e5-147">[استخدم وظائف البيانات المجمعة](#collected-data) لتجنب إحضار نفس البيانات للتلخيص.</span><span class="sxs-lookup"><span data-stu-id="188e5-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="188e5-148">تحليل تتبع PerfView</span><span class="sxs-lookup"><span data-stu-id="188e5-148">Analyze PerfView traces</span></span>

<span data-ttu-id="188e5-149">[PerfView](#perfview) عبارة أداة للمطورين ذوي الخبرة.</span><span class="sxs-lookup"><span data-stu-id="188e5-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="188e5-150">للحصول على مزيد من المعلومات التفصيلية حول الخطوات التالية، راجع [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="188e5-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="188e5-151">اجمع تتبع باستخدام وقت المؤشر.</span><span class="sxs-lookup"><span data-stu-id="188e5-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="188e5-152">قم فقط بتضمين المكدسات التي تستخدم **runUnattended**، لتصفية المؤشر الذي يحتوي على تنفيذ التكوين فقط.</span><span class="sxs-lookup"><span data-stu-id="188e5-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="188e5-153">(أضف **runUnattended** إلى مربع إدخال **IncPats** input box.)</span><span class="sxs-lookup"><span data-stu-id="188e5-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="188e5-154">قم بطي كل وحدات المعالجة المركزية والشبكات والأوقات المحظورة.</span><span class="sxs-lookup"><span data-stu-id="188e5-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="188e5-155">تحميل [إعدادات التقارير الإلكترونية المسبقة لـ PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="188e5-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="188e5-156">حدد **التقارير الإلكترونية** \> **إعداد مسبق آخر**.</span><span class="sxs-lookup"><span data-stu-id="188e5-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="188e5-157">انظر إلى الأسماء:</span><span class="sxs-lookup"><span data-stu-id="188e5-157">Look at the names:</span></span>

    - <span data-ttu-id="188e5-158">من المحتمل أن تشاهد كود النظام الأساسي الذي يستهلك معظم الوقت.</span><span class="sxs-lookup"><span data-stu-id="188e5-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="188e5-159">يمكنك الضغط ضغطًا مزدوجًا (أو النقر نقرًا مزدوجًا) والخروج من خلال **المتصل بهم**.</span><span class="sxs-lookup"><span data-stu-id="188e5-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="188e5-160">إذا وجدت الدرجات التي تحتوي على البادئة "ERExpression"، وإذا كانت الوظائف مرتبطة بالمعادلات، يمكنك تخمين اسم الوظيفة استنادًا إلى اسم الفئة، ويمكنك إلقاء نظرة على مستودع التقارير الإلكترونية لعرض السمات.</span><span class="sxs-lookup"><span data-stu-id="188e5-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="188e5-161">إصلاحات</span><span class="sxs-lookup"><span data-stu-id="188e5-161">Fixes</span></span>

- <span data-ttu-id="188e5-162">إذا كنت ترى أنه يتم استهلاك معظم وقت وحدة المعالجة المركزية بواسطة الاستعلامات، حاول تقليل عدد الاستعلامات:</span><span class="sxs-lookup"><span data-stu-id="188e5-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="188e5-163">[راجع تتبع التقارير الإلكترونية](#analyze-database-calls) بالنسبة للاستعلامات المتكررة.</span><span class="sxs-lookup"><span data-stu-id="188e5-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="188e5-164">راجع عدد السجلات التي يتم إحضارها، وقم بتقييم مقدار البيانات التي يجب إحضارها نظريًا.</span><span class="sxs-lookup"><span data-stu-id="188e5-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="188e5-165">إذا كنت ترى أنه يتم استهلاك معظم وقت وحدة المعالجة المركزية بواسطة الوظائف المستخدمة، حاول العثور على المكان الموجود في التكوين الذي يستهلك معظم الموارد.</span><span class="sxs-lookup"><span data-stu-id="188e5-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="188e5-166">إذا كنت ترى أنه يتم استهلاك معظم الوقت وحدة المعالجة المركزية بواسطة وظائف تجميع البيانات، خذ بعين الاعتبار استبدالها بـ *تجميع SQL حسب* على جانب تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="188e5-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="188e5-167">تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="188e5-167">Collecting data</span></span>

<span data-ttu-id="188e5-168">بناءً على البيئة الخاصة بك، هناك عدة طرق لجمع البيانات المتوفرة:</span><span class="sxs-lookup"><span data-stu-id="188e5-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="188e5-169">احصل على إجمالي وقت التشغيل:</span><span class="sxs-lookup"><span data-stu-id="188e5-169">Get the total running time:</span></span>

    - <span data-ttu-id="188e5-170">من مركز الإجراءات</span><span class="sxs-lookup"><span data-stu-id="188e5-170">From the Action center</span></span>
    - <span data-ttu-id="188e5-171">من سجل الأحداث</span><span class="sxs-lookup"><span data-stu-id="188e5-171">From the event log</span></span>

- <span data-ttu-id="188e5-172">ملف تعريف التنفيذ:</span><span class="sxs-lookup"><span data-stu-id="188e5-172">Profile the execution:</span></span>

    - <span data-ttu-id="188e5-173">باستخدام أدوات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="188e5-173">By using ER tools</span></span>
    - <span data-ttu-id="188e5-174">باستخدام محلل التتبع</span><span class="sxs-lookup"><span data-stu-id="188e5-174">By using Trace parser</span></span>
    - <span data-ttu-id="188e5-175">باستخدام PerfView</span><span class="sxs-lookup"><span data-stu-id="188e5-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="188e5-176">جمع البيانات في بيئة التشغيل</span><span class="sxs-lookup"><span data-stu-id="188e5-176">Collecting data in a production environment</span></span>

<span data-ttu-id="188e5-177">في بعض الأحيان، يمكن إعادة الإنتاج في بيئة التشغيل فقط.</span><span class="sxs-lookup"><span data-stu-id="188e5-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="188e5-178">يمكن جمع البيانات بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="188e5-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="188e5-179">باستخدام تتبعات [محلل التتبع](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="188e5-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="188e5-180">باستخدام [تنفيذ التقارير الإلكترونية](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="188e5-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="188e5-181">باستخدام إجمالي وقت التنفيذ</span><span class="sxs-lookup"><span data-stu-id="188e5-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="188e5-182">جمع البيانات في بيئة التطوير</span><span class="sxs-lookup"><span data-stu-id="188e5-182">Collecting data in a development environment</span></span>

<span data-ttu-id="188e5-183">بالإضافة إلى الأدوات التي يمكن استخدامها في بيئة التشغيل، هناك العديد من الأدوات التي يمكنك استخدامها في بيئة تطوير:</span><span class="sxs-lookup"><span data-stu-id="188e5-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="188e5-184">سجل الأحداث (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="188e5-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="188e5-185">يمكن أن يمنحك هذا السجل إجمالي وقت التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="188e5-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="188e5-186">أدوات .NET العامة، مثل PerfView.</span><span class="sxs-lookup"><span data-stu-id="188e5-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="188e5-187">بالإضافة إلى ذلك، تمنحك بيئة التطوير مرونة أكبر للتجربة.</span><span class="sxs-lookup"><span data-stu-id="188e5-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="188e5-188">على سبيل المثال، يمكنك إيقاف تشغيل أجزاء التقارير لمعرفة كيفية تأثر وقت التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="188e5-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="188e5-189">أدوات</span><span class="sxs-lookup"><span data-stu-id="188e5-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="188e5-190">وقت التنفيذ في مركز الإجراءات</span><span class="sxs-lookup"><span data-stu-id="188e5-190">Execution time in the Action center</span></span>

<span data-ttu-id="188e5-191">يمكن أن تظهر التقارير الإلكترونية وقت تنفيذ التكوين في مركز الإجراء.</span><span class="sxs-lookup"><span data-stu-id="188e5-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="188e5-192">يعمل هذا الخيار فقط لمستخدم معين وشركة معينة، ولجلسات العمل التفاعلية.</span><span class="sxs-lookup"><span data-stu-id="188e5-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="188e5-193">لتوفير هذه الميزة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="188e5-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="188e5-194">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="188e5-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="188e5-195">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="188e5-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="188e5-196">في مربع حوار **معلمات المستخدم**، قم بتعيين الخيار **عرض وقت إنشاء الملف** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="188e5-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="188e5-197">وقت التنفيذ في سجل الأحداث</span><span class="sxs-lookup"><span data-stu-id="188e5-197">Execution time in the event log</span></span>

1. <span data-ttu-id="188e5-198">افتح عارض أحداث Windows.</span><span class="sxs-lookup"><span data-stu-id="188e5-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="188e5-199">ضمن **سجلات التطبيقات والخدمات**، افتح **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="188e5-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="188e5-200">ابحث عن أحداث **FormatMapingRun** حيث **EventID=2**، لأن هذه الأحداث تحتوي على معلومات حول الوقت المنقضي.</span><span class="sxs-lookup"><span data-stu-id="188e5-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="188e5-201">التتبعات باستخدام محلل التتبع</span><span class="sxs-lookup"><span data-stu-id="188e5-201">Trace parser traces</span></span> 

<span data-ttu-id="188e5-202">نظرًا لأنه يتم تنفيذ التقارير الإلكترونية في X++، فإنه يمكنك استخدام أدوات X++ العامة لتحليل الأداء.</span><span class="sxs-lookup"><span data-stu-id="188e5-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="188e5-203">لمزيد من المعلومات، راجع [‏‫التقاط تتبعات باستخدام محلل التتبع‬](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="188e5-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="188e5-204">وهناك بعض القيود على هذا الأسلوب.</span><span class="sxs-lookup"><span data-stu-id="188e5-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="188e5-205">نظرًا لأنه يتم تنفيذ جزء من التقارير الإلكترونية في C#، لن تتوفر جميع التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="188e5-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="188e5-206">ومع ذلك، يمكنك عرض تفاصيل استخدام البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-206">However, you can view the data usage details.</span></span> <span data-ttu-id="188e5-207">بالإضافة إلى ذلك، يمكن أن يتجاوز تشغيل التقرير الطويل قيود تخزين التتبع.</span><span class="sxs-lookup"><span data-stu-id="188e5-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="188e5-208">تتبعات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="188e5-208">ER traces</span></span>

<span data-ttu-id="188e5-209">يمكن أن تجمع التقارير الإلكترونية تتبعاتها الخاصة، ولديها أدوات مرئيات وتحليل لتلك التتبعات.</span><span class="sxs-lookup"><span data-stu-id="188e5-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="188e5-210">لمزيد من المعلومات، راجع [تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="188e5-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="188e5-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="188e5-211">PerfView</span></span>

<span data-ttu-id="188e5-212">نظرًا لأنه يتم تنفيذ كل من X++ والتقارير الإلكترونية أعلى النظام الأساسي .NET، فإنه يمكنك استخدام أدوات .NET العامة.</span><span class="sxs-lookup"><span data-stu-id="188e5-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="188e5-213">على سبيل المثال، يمكنك استخدام أداة [PerfView](https://github.com/Microsoft/perfview) مجانية.</span><span class="sxs-lookup"><span data-stu-id="188e5-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="188e5-214">يمكنك أيضًا تجميع البيانات من سطر الأوامر.</span><span class="sxs-lookup"><span data-stu-id="188e5-214">You can also collect data from the command line.</span></span> <span data-ttu-id="188e5-215">على سبيل المثال، يجمع البرنامج النصي Windows PowerShell التالي وقت التنفيذ حتى يتم إيقاف أي تنفيذ تنسيق على الجهاز.</span><span class="sxs-lookup"><span data-stu-id="188e5-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="188e5-216">وهناك بعض القيود على هذا الأسلوب.</span><span class="sxs-lookup"><span data-stu-id="188e5-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="188e5-217">يجب أن يكون لديك حق الوصول الإداري إلى الجهاز.</span><span class="sxs-lookup"><span data-stu-id="188e5-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="188e5-218">بالإضافة إلى ذلك، يجب أن تكون مطور ذو خبرة، لأن هناك منحنى تعلم قوي.</span><span class="sxs-lookup"><span data-stu-id="188e5-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="188e5-219">إجراء التغييرات</span><span class="sxs-lookup"><span data-stu-id="188e5-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="188e5-220">استخدام التخزين المؤقت</span><span class="sxs-lookup"><span data-stu-id="188e5-220">Use caching</span></span>

<span data-ttu-id="188e5-221">على الرغم من أن التخزين المؤقت يقلل مقدار الوقت المطلوب لإحضار البيانات مرة أخرى، فإنه يكلف الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="188e5-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="188e5-222">استخدم التخزين المؤقت في الحالات التي لا يكون فيها مقدار البيانات التي تم إحضارها كبيرًا جدًا.</span><span class="sxs-lookup"><span data-stu-id="188e5-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="188e5-223">لمزيد من المعلومات ومثال يوضح كيفية استخدام التخزين المؤقت، راجع [تحسين تعيين النموذج استنادًا إلى المعلومات من تتبع التنفيذ](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="188e5-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="188e5-224">استخدام حقل محسوب ذا معلمات ومُخزن مؤقتًا</span><span class="sxs-lookup"><span data-stu-id="188e5-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="188e5-225">في بعض الأحيان، يجب البحث عن القيم بشكل متكرر.</span><span class="sxs-lookup"><span data-stu-id="188e5-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="188e5-226">تتضمن الأمثلة أسماء الحسابات وأرقام الحسابات.</span><span class="sxs-lookup"><span data-stu-id="188e5-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="188e5-227">للمساعدة في توفير الوقت، يمكنك إنشاء حقل محسوب يحتوي على معلمات في المستوى الأعلى، ثم قم بإضافة الحقل إلى التخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="188e5-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="188e5-228">نوصي باستخدام هذا الأسلوب فقط عندما يكون حجم البيانات المخزنة مؤقتًا صغيرًا.</span><span class="sxs-lookup"><span data-stu-id="188e5-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="188e5-229">لمزيد من المعلومات، راجع [تحسين أداء حلول التقارير الإلكترونية عن طريق إضافة مصادر بيانات CALCULATED FIELD ذات المعلمات](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="188e5-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="188e5-230">استخدام مصدر بيانات JOIN</span><span class="sxs-lookup"><span data-stu-id="188e5-230">Use a JOIN data source</span></span>

<span data-ttu-id="188e5-231">يتيح مصدر البيانات **JOIN** سجلات متصلة متعددة ليتم إحضارها بواسطة استعلام واحد.</span><span class="sxs-lookup"><span data-stu-id="188e5-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="188e5-232">لا يلزم استخدام استعلام منفصل لإحضار كل سجل متصل.</span><span class="sxs-lookup"><span data-stu-id="188e5-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="188e5-233">على سبيل المثال، إذا كان لديك 1000 سطر، وكنت تحضر بيانات الصنف لكل سطر حسب العلاقة، سيكون لديك 1001 استعلام (= 1.000 + 1).</span><span class="sxs-lookup"><span data-stu-id="188e5-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="188e5-234">إذا كنت تستخدم مصدر بيانات **JOIN**، سوف تستخدم استعلام واحد فقط لإحضار البيانات نفسها.</span><span class="sxs-lookup"><span data-stu-id="188e5-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="188e5-235">للحصول على المزيد من المعلومات، راجع [استخدام مصادر بيانات في تعيينات نموذج التقارير الإلكترونية للحصول على البيانات من جداول التطبيقات المتعددة](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="188e5-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="188e5-236">استخدام الوظيفة FILTER بدلاً من الوظيفة WHERE</span><span class="sxs-lookup"><span data-stu-id="188e5-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="188e5-237">تعمل الوظيفة **[FILTER](er-functions-list-filter.md)** على تشغيل الشروط على خادم SQL، في حين أن الوظيفة **WHERE** تعمل على إحضار كافة البيانات من القائمة، سجل واحد في كل مرة وتطبيق الشرط لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="188e5-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="188e5-238">على سبيل المثال، تريد تحديد سجل واحد من أصل 1000 سجل.</span><span class="sxs-lookup"><span data-stu-id="188e5-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="188e5-239">إذا كنت تستخدم **WHERE**، فإنه سيتم إحضار كافة السجلات والتي يبلغ عددها 1000 سجلاً.</span><span class="sxs-lookup"><span data-stu-id="188e5-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="188e5-240">ومع ذلك، إذا كنت تستخدم **FILTER**، سيتم إحضار سجلاً واحدًا فقط.</span><span class="sxs-lookup"><span data-stu-id="188e5-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="188e5-241">يمكن لـ **FILTER** أيضًا استخدام الفهارس على جانب قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="188e5-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="188e5-242">استخدام وظائف البيانات المجمعة أو مصدر بيانات البيانات التراكمية</span><span class="sxs-lookup"><span data-stu-id="188e5-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="188e5-243">إذا كان التكوين الخاص بك يحتوي على مكون *تجميع حسب* الذي يلخص البيانات التي تم إحضارها مسبقًا حسب التقرير، فسيعمل المكون على إحضار كافة البيانات مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="188e5-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="188e5-244">باستخدام وظائف البيانات المجمعة، فإنك تقوم بتمكين التقارير الإلكترونية من تجميع البيانات أثناء عملية الإحضار الأولى.</span><span class="sxs-lookup"><span data-stu-id="188e5-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="188e5-245">لمزيد من المعلومات، راجع [التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="188e5-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="188e5-246">إعادة كتابة أجزاء من التكوين في X++</span><span class="sxs-lookup"><span data-stu-id="188e5-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="188e5-247">تعمل التقارير الإلكترونية على تدعيم طرق استدعاء الجداول والفئات، بما في ذلك الملحقات.</span><span class="sxs-lookup"><span data-stu-id="188e5-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="188e5-248">ضع في اعتبارك إعادة كتابة أجزاء من تعيين النموذج في X++ للمساعدة في تحسين الأداء.</span><span class="sxs-lookup"><span data-stu-id="188e5-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="188e5-249">يمكن أن تستهلك التقارير الإلكترونية البيانات من المصادر التالية:</span><span class="sxs-lookup"><span data-stu-id="188e5-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="188e5-250">الفئات (مصادر بيانات **الكائن** و **الفئة**)</span><span class="sxs-lookup"><span data-stu-id="188e5-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="188e5-251">الجداول (مصادر البيانات **الجدول** و **سجلات الجداول**)</span><span class="sxs-lookup"><span data-stu-id="188e5-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="188e5-252">يوفر [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) أيضًا طريقة لإرسال البيانات المحسوب مسبقًا من كود الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="188e5-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="188e5-253">تحتوي مجموعة التطبيقات على العديد من الأمثلة على هذا الأسلوب.</span><span class="sxs-lookup"><span data-stu-id="188e5-253">The application suite contains numerous examples of this approach.</span></span>
