---
title: تحسين مهام دفعات BYOD المجدولة
description: يوضح هذا الموضوع كيفية تحسين الأداء عند استخدام ميزة ‏‫إحضار قاعدة بياناتك الخاصة‬ (BYOD) مع Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 0c29d68b29475c2c7040d06e60f7624c49a42002
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951922"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a><span data-ttu-id="21991-103">تحسين مهام دفعات BYOD المجدولة</span><span class="sxs-lookup"><span data-stu-id="21991-103">Optimize BYOD scheduled batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="21991-104">يوضح هذا الموضوع كيفية تحسين الأداء عند استخدام ميزة ‏‫إحضار قاعدة بياناتك الخاصة‬ (BYOD) .</span><span class="sxs-lookup"><span data-stu-id="21991-104">This topic explains how to optimize performance when you're using the bring your own database (BYOD) feature.</span></span> <span data-ttu-id="21991-105">لمزيد من المعلومات حول ميزة BYOD، راجع [إحضار قاعدة بياناتك الخاصة (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="21991-105">For more information about BYOD, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

## <a name="performance-considerations-for-data-export"></a><span data-ttu-id="21991-106">اعتبارات الأداء لتصدير البيانات</span><span class="sxs-lookup"><span data-stu-id="21991-106">Performance considerations for data export</span></span>

<span data-ttu-id="21991-107">بعد نشر الكيانات إلى قاعدة البيانات الوجهة، يمكنك استخدام وظيفة "تصدير" في مساحة عمل **إدارة البيانات** لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="21991-107">After entities are published to the destination database, you can use the Export function in the **Data management** workspace to move data.</span></span> <span data-ttu-id="21991-108">تتيح لك وظيفة "تصدير" تحديد مهمة حركه البيانات التي تحتوي علي كيان واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="21991-108">The Export function lets you define a Data movement job that contains one or more entities.</span></span> <span data-ttu-id="21991-109">لمزيد من المعلومات حول تصدير البيانات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="21991-109">For more information about data export, see [Data import and export jobs overview](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

<span data-ttu-id="21991-110">يمكنك استخدام صفحة **تصدير** لتصدير بيانات إلى تنسيقات بيانات هدف مختلفة، مثل ملف قيم مفصولة بفاصلة (CSV).</span><span class="sxs-lookup"><span data-stu-id="21991-110">You can use the **Export** page to export data into different target data formats, such as a comma-separated values (CSV) file.</span></span> <span data-ttu-id="21991-111">وتدعم هذه الصفحة أيضًا قواعد بيانات SQL كوجهة أخرى.</span><span class="sxs-lookup"><span data-stu-id="21991-111">This page also supports SQL databases as another destination.</span></span>

<span data-ttu-id="21991-112">يمكنك إنشاء مشروع بيانات يحتوي على كيانات متعددة واستخدام وظيفة دُفعية لجدولة تشغيل مشروع البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="21991-112">You can create a data project that has multiple entities and use a batch job to schedule that data project to run.</span></span> <span data-ttu-id="21991-113">إذا قمت بتحديد خيار **تصدير دُفعي** يمكنك جدولة مهمة تصدير البيانات ليتم تشغيلها بشكل دوري.</span><span class="sxs-lookup"><span data-stu-id="21991-113">If you select the **Export in batch** option, you can schedule the data export job to run periodically.</span></span>

<span data-ttu-id="21991-114">للمساعدة في الحفاظ علي الثقة الكلية لعمليه تصدير BYOD، يجب توخي الحذر عند إضافة كيانات متعددة إلى مشروع تصدير.</span><span class="sxs-lookup"><span data-stu-id="21991-114">To help preserve the overall reliability of the BYOD export, you must be careful when you add multiple entities to an export project.</span></span> <span data-ttu-id="21991-115">عندما تقوم بتحديد عدد الكيانات التي ستتم إضافتها إلى نفس المشروع، يجب مراعاة المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="21991-115">When you're determining the number of entities to add to the same project, consider the following parameters:</span></span>

- <span data-ttu-id="21991-116">تعقيد الكيانات</span><span class="sxs-lookup"><span data-stu-id="21991-116">The complexity of the entities</span></span>
- <span data-ttu-id="21991-117">وحده تخزين البيانات المتوقعة لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="21991-117">The expected data volume per entity</span></span>
- <span data-ttu-id="21991-118">الوقت الكلي المطلوب لإكمال التصدير على مستوى الوظيفة</span><span class="sxs-lookup"><span data-stu-id="21991-118">The overall time that will be required to complete the export at the job level</span></span>

<span data-ttu-id="21991-119">للحصول على أفضل أداء، تجنب إضافة مئات الكيانات إلى مشروع واحد.</span><span class="sxs-lookup"><span data-stu-id="21991-119">For the best performance, avoid adding hundreds of entities to a single project.</span></span> <span data-ttu-id="21991-120">نوصي بإنشاء العديد من الوظائف التي تحتوي كل منها على كيانات أقل.</span><span class="sxs-lookup"><span data-stu-id="21991-120">We recommend that you create multiple jobs, each of which contains fewer entities.</span></span>

## <a name="scheduling-byod-batch-jobs"></a><span data-ttu-id="21991-121">جدولة مهام دفعات BYOD</span><span class="sxs-lookup"><span data-stu-id="21991-121">Scheduling BYOD batch jobs</span></span>

<span data-ttu-id="21991-122">للمساعدة في تقليل التأثير على مستخدمي Microsoft Dynamics 365 Human Resources، قم بتشغيل الوظائف الدُفعية لميزة BYOD في الليل أو بعد ساعات العمل.</span><span class="sxs-lookup"><span data-stu-id="21991-122">To help reduce the impact on users of Microsoft Dynamics 365 Human Resources, run BYOD batch jobs at night or after hours.</span></span> <span data-ttu-id="21991-123">تأكد من التحقق من المنطقة الزمنية لهذه الوظائف الدفعية المتكررة.</span><span class="sxs-lookup"><span data-stu-id="21991-123">Be sure to check the time zone for recurring batch jobs.</span></span> <span data-ttu-id="21991-124">قد تستخدم بعض الوظائف الدفعية التوقيت الرسمي الباسيفيكي (PST).</span><span class="sxs-lookup"><span data-stu-id="21991-124">Some batch jobs might use Pacific Standard Time (PST).</span></span>

<span data-ttu-id="21991-125">للمساعدة على تجنب مشكلات الأداء، خذ بعين الاعتبار العوامل التالية عند تكوين تكرار الجدولة لوظائف BYOD الدُفعية:</span><span class="sxs-lookup"><span data-stu-id="21991-125">To help avoid performance issues, consider the following factors when you configure the scheduling frequency for BYOD batch jobs:</span></span>

- <span data-ttu-id="21991-126">الوقت المطلوب لإكمال كل وظيفة دفعية</span><span class="sxs-lookup"><span data-stu-id="21991-126">The time that is required to complete each batch job</span></span>
- <span data-ttu-id="21991-127">احتياجات الأعمال للبيانات الموجودة في BYOD</span><span class="sxs-lookup"><span data-stu-id="21991-127">The business need for the data in BYOD</span></span>

<span data-ttu-id="21991-128">قم بتعيين تكرار كل وظيفة دُفعية إلى قيمة تؤكد أن الوظيفة يمكن إكمالها جيدا قبل وقت التشغيل المجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="21991-128">Set the frequency for each batch job to a value that ensures that the job can be completed well before its next scheduled run time.</span></span> <span data-ttu-id="21991-129">تجنب تشغيل وظائف متعددة بشكل متزامن، لأن هذا المنهد يمكن أن يؤثر سلبيا على أداء الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="21991-129">Avoid running multiple jobs in parallel, because this approach can negatively affect the performance of Human Resources.</span></span>

<span data-ttu-id="21991-130">للحصول على أفضل أداء، دائما استخدم خيار **تصدير دُفعي** على صفحة **تصدير** لجدولة وظائف BYOD الدُفعية.</span><span class="sxs-lookup"><span data-stu-id="21991-130">For the best performance, always use the **Export in batch** option on the **Export** page to schedule BYOD batch jobs.</span></span> <span data-ttu-id="21991-131">تجنب جدولة التصدير المتكرر في **إدارة \> إدارة وظائف البيانات المتكررة**.</span><span class="sxs-lookup"><span data-stu-id="21991-131">Avoid scheduling recurring exports at **Manage \> Manage recurring data jobs**.</span></span>

## <a name="incremental-export"></a><span data-ttu-id="21991-132">تصدير تزايدي</span><span class="sxs-lookup"><span data-stu-id="21991-132">Incremental export</span></span>

<span data-ttu-id="21991-133">عند إضافة كيان لتصدير البيانات، يمكنك إجراء إما دفع تزايدي (تصدير) أو دفع كامل.</span><span class="sxs-lookup"><span data-stu-id="21991-133">When you add an entity for data export, you can do either an incremental push (export) or a full push.</span></span> <span data-ttu-id="21991-134">يقوم الدفع الكامل بحذف كافة السجلات الموجودة من أحد الكيانات في قاعدة بيانات BYOD.</span><span class="sxs-lookup"><span data-stu-id="21991-134">A full push deletes all existing records from an entity in the BYOD database.</span></span> <span data-ttu-id="21991-135">ثم يقوم بإدراج مجموعة السجلات الحالية من كيان الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="21991-135">It then inserts the current set of records from the Human Resources entity.</span></span>

<span data-ttu-id="21991-136">لإجراء عملية دفع تزايديه، يجب تشغيل تعقب التغيير لكل كيان في صفحة **الكيانات**.</span><span class="sxs-lookup"><span data-stu-id="21991-136">To do an incremental push, you must turn on change tracking for each entity on the **Entities** page.</span></span> <span data-ttu-id="21991-137">لمزيد من المعلومات، راجع [‏‫تمكين تعقب التغيير للكيانات‬](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="21991-137">For more information, see [Enable change tracking for entities](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

<span data-ttu-id="21991-138">إذا قمت بتحديد دفع تزايدي، فان الدفع الأول دائمًا يكون دفعا كاملا.</span><span class="sxs-lookup"><span data-stu-id="21991-138">If you select an incremental push, the first push is always a full push.</span></span> <span data-ttu-id="21991-139">يقوم SQL بتعقب التغييرات من الدفع الكامل الأول.</span><span class="sxs-lookup"><span data-stu-id="21991-139">SQL tracks changes from this first full push.</span></span> <span data-ttu-id="21991-140">عند إدراج سجل جديد أو عند تحديث سجل أو حذفه، ينعكس التغيير في الكيان الوجهة.</span><span class="sxs-lookup"><span data-stu-id="21991-140">When a new record is inserted, or when a record is updated or deleted, the change is reflected in the destination entity.</span></span>

## <a name="time-outs"></a><span data-ttu-id="21991-141">المهلات</span><span class="sxs-lookup"><span data-stu-id="21991-141">Time-outs</span></span>

<span data-ttu-id="21991-142">فيما يلي المهلات الافتراضية لعمليات تصدير BYOD:</span><span class="sxs-lookup"><span data-stu-id="21991-142">Here are the default time-outs for BYOD exports:</span></span>

- <span data-ttu-id="21991-143">عشر دقائق لعمليات الاقتطاع</span><span class="sxs-lookup"><span data-stu-id="21991-143">Ten minutes for truncation operations</span></span>
- <span data-ttu-id="21991-144">ساعة واحدة لعمليات الإدراج المجمع</span><span class="sxs-lookup"><span data-stu-id="21991-144">One hour for bulk insert operations</span></span>

<span data-ttu-id="21991-145">عندما تكون وحدات التخزين عالية، فقد لا تكون إعدادات هذه المهلة كافيه.</span><span class="sxs-lookup"><span data-stu-id="21991-145">When volumes are high, these time-out settings might not be sufficient.</span></span> <span data-ttu-id="21991-146">لتحديثها، انتقل إلى **إدارة البيانات \> معلمات إطار العمل \>‫ إحضار قاعدة بياناتك الخاصة‬**.</span><span class="sxs-lookup"><span data-stu-id="21991-146">To update them, go to **Data management \> Framework parameters \> Bring your own database**.</span></span> <span data-ttu-id="21991-147">هذه المهلات خاصه بالشركة ويجب تعيينها بشكل منفصل لكل شركة.</span><span class="sxs-lookup"><span data-stu-id="21991-147">These time-outs are company-specific and must be set separately for each company.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="21991-148">القيود المعروفة</span><span class="sxs-lookup"><span data-stu-id="21991-148">Known limitations</span></span>

<span data-ttu-id="21991-149">ميزة BYOD بها القيود التالية:</span><span class="sxs-lookup"><span data-stu-id="21991-149">The BYOD feature has the following limitations:</span></span>

- <span data-ttu-id="21991-150">يجب ألا تكون هناك أية تامينات نشطة على قاعدة البيانات اثناء المزامنة.</span><span class="sxs-lookup"><span data-stu-id="21991-150">There should be no active locks on your database during synchronization.</span></span> <span data-ttu-id="21991-151">يمكن أن تؤدي عمليات التأمين النشطة إلى بطء الكتابة أو حتى الفشل في تصدير البيانات إلى قاعدة بيانات Azure SQL الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="21991-151">Active locks can cause slow writes or even failure to export data to your Azure SQL database.</span></span>
- <span data-ttu-id="21991-152">لا يمكنك تصدير كيانات مركبة إلى قاعدة البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="21991-152">You can't export composite entities into your own database.</span></span> <span data-ttu-id="21991-153">لا يتم دعم الكيانات المركبة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="21991-153">Currently, composite entities aren't supported.</span></span> <span data-ttu-id="21991-154">يجب تصدير الكيانات الفردية التي تشكل الكيان المركب.</span><span class="sxs-lookup"><span data-stu-id="21991-154">You must export individual entities that make up the composite entity.</span></span> <span data-ttu-id="21991-155">ومع ذلك يمكن تصدير كلا الكيانين في نفس مشروع البيانات.</span><span class="sxs-lookup"><span data-stu-id="21991-155">However, you can export both entities in the same data project.</span></span>
- <span data-ttu-id="21991-156">لا يمكن تصدير الكيانات التي لا تحتوي على مفاتيح فريدة باستخدام الدفع التزايدي.</span><span class="sxs-lookup"><span data-stu-id="21991-156">Entities that don't have unique keys can't be exported by using incremental push.</span></span> <span data-ttu-id="21991-157">قد تواجه هذه القيود خاصة عندما تحاول تصدير السجلات بشكل متزايد من بعض الكيانات الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="21991-157">You might face this limitation especially when you try to incrementally export records from a few ready-made entities.</span></span> <span data-ttu-id="21991-158">ونظرًا لان هذه الكيانات قد تم تصميمها لتمكين استيراد البيانات، فانها لا تحتوي على مفتاح فريد.</span><span class="sxs-lookup"><span data-stu-id="21991-158">Because these entities were designed to enable the import of data, they don't have a unique key.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="21991-159">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="21991-159">Troubleshooting</span></span>

### <a name="incremental-push-doesnt-work-correctly"></a><span data-ttu-id="21991-160">لا يعمل الدفع التزايدي بشكل صحيح</span><span class="sxs-lookup"><span data-stu-id="21991-160">Incremental push doesn't work correctly</span></span>

<span data-ttu-id="21991-161">**المشكلة:** عند حدوث دفع كامل لأحد الكيانات، تشاهد مجموعة كبيرة من السجلات في BYOD عند استخدام عبارة **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="21991-161">**Issue:** When a full push occurs for an entity, you see a large set of records in BYOD when you use a **select** statement.</span></span> <span data-ttu-id="21991-162">ومع ذلك ، عندما تقوم بالدفع المتزايد، يمكنك الاطلاع على عدد قليل فقط من السجلات في BYOD.</span><span class="sxs-lookup"><span data-stu-id="21991-162">However, when you do an incremental push, you see only a few records in BYOD.</span></span> <span data-ttu-id="21991-163">ويبدو وكأن الدفع التزايدي قد حذف كافة السجلات وأضاف فقط السجلات التي تم تغييرها في BYOD.</span><span class="sxs-lookup"><span data-stu-id="21991-163">It seems as though the incremental push deleted all the records and added only the changed records in BYOD.</span></span>

<span data-ttu-id="21991-164">**الحل:** قد لا تكون جداول تتبع التغييرات في SQL في الحالة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="21991-164">**Solution:** The SQL change tracking tables might not be in the expected state.</span></span> <span data-ttu-id="21991-165">وفي هذه الحالات، نوصي بإيقاف تشغيل تعقب التغييرات للكيان ثم تشغيله مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="21991-165">In cases of this type, we recommend that you turn off change tracking for the entity and then turn it back on.</span></span> <span data-ttu-id="21991-166">لمزيد من المعلومات، راجع [‏‫تمكين تعقب التغيير للكيانات‬](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="21991-166">For more information, see [Enable change tracking for entities](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="staging-tables-arent-clearing"></a><span data-ttu-id="21991-167">لا يتم مسح الجداول المرحلية</span><span class="sxs-lookup"><span data-stu-id="21991-167">Staging tables aren't clearing</span></span>

<span data-ttu-id="21991-168">**المشكلة:** عند استخدام المراحل للمشروع، لا يتم مسح الجداول المرحلية بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="21991-168">**Issue:** When using staging for the project, the staging tables don't clear out correctly.</span></span> <span data-ttu-id="21991-169">ثم تستمر البيانات الموجودة في الجداول في النمو، مما يتسبب في حدوث مشكلات في الأداء.</span><span class="sxs-lookup"><span data-stu-id="21991-169">The data in the tables then continues to grow, causing performance issues.</span></span>

<span data-ttu-id="21991-170">**الحل:** يتم الاحتفاظ بسبعة أيام من التاريخ في جداول المراحل.</span><span class="sxs-lookup"><span data-stu-id="21991-170">**Solution:** Seven days of history is maintained in the staging tables.</span></span> <span data-ttu-id="21991-171">يتم مسح البيانات التاريخية الأقدم من سبعة أيام تلقائيًا من الجداول المرحلية بواسطة وظيفة دفعة **تنظيف مراحل التصدير والاستيراد**.</span><span class="sxs-lookup"><span data-stu-id="21991-171">Historical data older than seven days is automatically cleared from the staging tables by the **Import export staging cleanup** batch job.</span></span> <span data-ttu-id="21991-172">إذا تعطلت هذه المهمة، فلن يتم مسح الجداول بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="21991-172">If this job gets stuck, the tables won't clear out correctly.</span></span> <span data-ttu-id="21991-173">ستؤدي إعادة تشغيل وظيفة المجموعة هذه إلى متابعة العملية لمسح جداول المراحل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="21991-173">Restarting this batch job will continue the process to automatically clear out the staging tables.</span></span>

## <a name="see-also"></a><span data-ttu-id="21991-174">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="21991-174">See also</span></span>

[<span data-ttu-id="21991-175">نظرة عامة حول إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="21991-175">Data management overview</span></span>](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="21991-176">إحضار قاعدة بياناتك الخاصة (BYOD)</span><span class="sxs-lookup"><span data-stu-id="21991-176">Bring your own database (BYOD)</span></span>](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="21991-177">نظرة عامة حول مهام استيراد البيانات وتصديرها</span><span class="sxs-lookup"><span data-stu-id="21991-177">Data import and export jobs overview</span></span>](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="21991-178">تمكين تعقب التغيير للكيانات</span><span class="sxs-lookup"><span data-stu-id="21991-178">Enable change tracking for entities</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
