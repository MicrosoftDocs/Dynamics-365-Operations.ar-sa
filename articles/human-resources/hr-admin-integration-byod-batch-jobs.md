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
ms.openlocfilehash: f21e9b94b5aa30b2cdb18692e8cc9c8d00f758d6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805024"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a><span data-ttu-id="2ad63-103">تحسين مهام دفعات BYOD المجدولة</span><span class="sxs-lookup"><span data-stu-id="2ad63-103">Optimize BYOD scheduled batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2ad63-104">يوضح هذا الموضوع كيفية تحسين الأداء عند استخدام ميزة ‏‫إحضار قاعدة بياناتك الخاصة‬ (BYOD) .</span><span class="sxs-lookup"><span data-stu-id="2ad63-104">This topic explains how to optimize performance when you're using the bring your own database (BYOD) feature.</span></span> <span data-ttu-id="2ad63-105">لمزيد من المعلومات حول ميزة BYOD، راجع [إحضار قاعدة بياناتك الخاصة (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2ad63-105">For more information about BYOD, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="performance-considerations-for-data-export"></a><span data-ttu-id="2ad63-106">اعتبارات الأداء لتصدير البيانات</span><span class="sxs-lookup"><span data-stu-id="2ad63-106">Performance considerations for data export</span></span>

<span data-ttu-id="2ad63-107">بعد نشر الكيانات إلى قاعدة البيانات الوجهة، يمكنك استخدام وظيفة "تصدير" في مساحة عمل **إدارة البيانات** لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="2ad63-107">After entities are published to the destination database, you can use the Export function in the **Data management** workspace to move data.</span></span> <span data-ttu-id="2ad63-108">تتيح لك وظيفة "تصدير" تحديد مهمة حركه البيانات التي تحتوي علي كيان واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="2ad63-108">The Export function lets you define a Data movement job that contains one or more entities.</span></span> <span data-ttu-id="2ad63-109">لمزيد من المعلومات حول تصدير البيانات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2ad63-109">For more information about data export, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json).</span></span>

<span data-ttu-id="2ad63-110">يمكنك استخدام صفحة **تصدير** لتصدير بيانات إلى تنسيقات بيانات هدف مختلفة، مثل ملف قيم مفصولة بفاصلة (CSV).</span><span class="sxs-lookup"><span data-stu-id="2ad63-110">You can use the **Export** page to export data into different target data formats, such as a comma-separated values (CSV) file.</span></span> <span data-ttu-id="2ad63-111">وتدعم هذه الصفحة أيضًا قواعد بيانات SQL كوجهة أخرى.</span><span class="sxs-lookup"><span data-stu-id="2ad63-111">This page also supports SQL databases as another destination.</span></span>

<span data-ttu-id="2ad63-112">يمكنك إنشاء مشروع بيانات يحتوي على كيانات متعددة واستخدام وظيفة دُفعية لجدولة تشغيل مشروع البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="2ad63-112">You can create a data project that has multiple entities and use a batch job to schedule that data project to run.</span></span> <span data-ttu-id="2ad63-113">إذا قمت بتحديد خيار **تصدير دُفعي** يمكنك جدولة مهمة تصدير البيانات ليتم تشغيلها بشكل دوري.</span><span class="sxs-lookup"><span data-stu-id="2ad63-113">If you select the **Export in batch** option, you can schedule the data export job to run periodically.</span></span>

<span data-ttu-id="2ad63-114">للمساعدة في الحفاظ علي الثقة الكلية لعمليه تصدير BYOD، يجب توخي الحذر عند إضافة كيانات متعددة إلى مشروع تصدير.</span><span class="sxs-lookup"><span data-stu-id="2ad63-114">To help preserve the overall reliability of the BYOD export, you must be careful when you add multiple entities to an export project.</span></span> <span data-ttu-id="2ad63-115">عندما تقوم بتحديد عدد الكيانات التي ستتم إضافتها إلى نفس المشروع، يجب مراعاة المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="2ad63-115">When you're determining the number of entities to add to the same project, consider the following parameters:</span></span>

- <span data-ttu-id="2ad63-116">تعقيد الكيانات</span><span class="sxs-lookup"><span data-stu-id="2ad63-116">The complexity of the entities</span></span>
- <span data-ttu-id="2ad63-117">وحده تخزين البيانات المتوقعة لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="2ad63-117">The expected data volume per entity</span></span>
- <span data-ttu-id="2ad63-118">الوقت الكلي المطلوب لإكمال التصدير على مستوى الوظيفة</span><span class="sxs-lookup"><span data-stu-id="2ad63-118">The overall time that will be required to complete the export at the job level</span></span>

<span data-ttu-id="2ad63-119">للحصول على أفضل أداء، تجنب إضافة مئات الكيانات إلى مشروع واحد.</span><span class="sxs-lookup"><span data-stu-id="2ad63-119">For the best performance, avoid adding hundreds of entities to a single project.</span></span> <span data-ttu-id="2ad63-120">نوصي بإنشاء العديد من الوظائف التي تحتوي كل منها على كيانات أقل.</span><span class="sxs-lookup"><span data-stu-id="2ad63-120">We recommend that you create multiple jobs, each of which contains fewer entities.</span></span>

## <a name="scheduling-byod-batch-jobs"></a><span data-ttu-id="2ad63-121">جدولة مهام دفعات BYOD</span><span class="sxs-lookup"><span data-stu-id="2ad63-121">Scheduling BYOD batch jobs</span></span>

<span data-ttu-id="2ad63-122">للمساعدة في تقليل التأثير على مستخدمي Microsoft Dynamics 365 Human Resources، قم بتشغيل الوظائف الدُفعية لميزة BYOD في الليل أو بعد ساعات العمل.</span><span class="sxs-lookup"><span data-stu-id="2ad63-122">To help reduce the impact on users of Microsoft Dynamics 365 Human Resources, run BYOD batch jobs at night or after hours.</span></span> <span data-ttu-id="2ad63-123">تأكد من التحقق من المنطقة الزمنية لهذه الوظائف الدفعية المتكررة.</span><span class="sxs-lookup"><span data-stu-id="2ad63-123">Be sure to check the time zone for recurring batch jobs.</span></span> <span data-ttu-id="2ad63-124">قد تستخدم بعض الوظائف الدفعية التوقيت الرسمي الباسيفيكي (PST).</span><span class="sxs-lookup"><span data-stu-id="2ad63-124">Some batch jobs might use Pacific Standard Time (PST).</span></span>

<span data-ttu-id="2ad63-125">للمساعدة على تجنب مشكلات الأداء، خذ بعين الاعتبار العوامل التالية عند تكوين تكرار الجدولة لوظائف BYOD الدُفعية:</span><span class="sxs-lookup"><span data-stu-id="2ad63-125">To help avoid performance issues, consider the following factors when you configure the scheduling frequency for BYOD batch jobs:</span></span>

- <span data-ttu-id="2ad63-126">الوقت المطلوب لإكمال كل وظيفة دفعية</span><span class="sxs-lookup"><span data-stu-id="2ad63-126">The time that is required to complete each batch job</span></span>
- <span data-ttu-id="2ad63-127">احتياجات الأعمال للبيانات الموجودة في BYOD</span><span class="sxs-lookup"><span data-stu-id="2ad63-127">The business need for the data in BYOD</span></span>

<span data-ttu-id="2ad63-128">قم بتعيين تكرار كل وظيفة دُفعية إلى قيمة تؤكد أن الوظيفة يمكن إكمالها جيدا قبل وقت التشغيل المجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="2ad63-128">Set the frequency for each batch job to a value that ensures that the job can be completed well before its next scheduled run time.</span></span> <span data-ttu-id="2ad63-129">تجنب تشغيل وظائف متعددة بشكل متزامن، لأن هذا المنهد يمكن أن يؤثر سلبيا على أداء الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="2ad63-129">Avoid running multiple jobs in parallel, because this approach can negatively affect the performance of Human Resources.</span></span>

<span data-ttu-id="2ad63-130">للحصول على أفضل أداء، دائما استخدم خيار **تصدير دُفعي** على صفحة **تصدير** لجدولة وظائف BYOD الدُفعية.</span><span class="sxs-lookup"><span data-stu-id="2ad63-130">For the best performance, always use the **Export in batch** option on the **Export** page to schedule BYOD batch jobs.</span></span> <span data-ttu-id="2ad63-131">تجنب جدولة التصدير المتكرر في **إدارة \> إدارة وظائف البيانات المتكررة**.</span><span class="sxs-lookup"><span data-stu-id="2ad63-131">Avoid scheduling recurring exports at **Manage \> Manage recurring data jobs**.</span></span>

## <a name="incremental-export"></a><span data-ttu-id="2ad63-132">تصدير تزايدي</span><span class="sxs-lookup"><span data-stu-id="2ad63-132">Incremental export</span></span>

<span data-ttu-id="2ad63-133">عند إضافة كيان لتصدير البيانات، يمكنك إجراء إما دفع تزايدي (تصدير) أو دفع كامل.</span><span class="sxs-lookup"><span data-stu-id="2ad63-133">When you add an entity for data export, you can do either an incremental push (export) or a full push.</span></span> <span data-ttu-id="2ad63-134">يقوم الدفع الكامل بحذف كافة السجلات الموجودة من أحد الكيانات في قاعدة بيانات BYOD.</span><span class="sxs-lookup"><span data-stu-id="2ad63-134">A full push deletes all existing records from an entity in the BYOD database.</span></span> <span data-ttu-id="2ad63-135">ثم يقوم بإدراج مجموعة السجلات الحالية من كيان الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="2ad63-135">It then inserts the current set of records from the Human Resources entity.</span></span>

<span data-ttu-id="2ad63-136">لإجراء عملية دفع تزايديه، يجب تشغيل تعقب التغيير لكل كيان في صفحة **الكيانات**.</span><span class="sxs-lookup"><span data-stu-id="2ad63-136">To do an incremental push, you must turn on change tracking for each entity on the **Entities** page.</span></span> <span data-ttu-id="2ad63-137">لمزيد من المعلومات، راجع [‏‫تمكين تعقب التغيير للكيانات‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2ad63-137">For more information, see [Enable change tracking for entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).</span></span>

<span data-ttu-id="2ad63-138">إذا قمت بتحديد دفع تزايدي، فان الدفع الأول دائمًا يكون دفعا كاملا.</span><span class="sxs-lookup"><span data-stu-id="2ad63-138">If you select an incremental push, the first push is always a full push.</span></span> <span data-ttu-id="2ad63-139">يقوم SQL بتعقب التغييرات من الدفع الكامل الأول.</span><span class="sxs-lookup"><span data-stu-id="2ad63-139">SQL tracks changes from this first full push.</span></span> <span data-ttu-id="2ad63-140">عند إدراج سجل جديد أو عند تحديث سجل أو حذفه، ينعكس التغيير في الكيان الوجهة.</span><span class="sxs-lookup"><span data-stu-id="2ad63-140">When a new record is inserted, or when a record is updated or deleted, the change is reflected in the destination entity.</span></span>

## <a name="time-outs"></a><span data-ttu-id="2ad63-141">المهلات</span><span class="sxs-lookup"><span data-stu-id="2ad63-141">Time-outs</span></span>

<span data-ttu-id="2ad63-142">فيما يلي المهلات الافتراضية لعمليات تصدير BYOD:</span><span class="sxs-lookup"><span data-stu-id="2ad63-142">Here are the default time-outs for BYOD exports:</span></span>

- <span data-ttu-id="2ad63-143">عشر دقائق لعمليات الاقتطاع</span><span class="sxs-lookup"><span data-stu-id="2ad63-143">Ten minutes for truncation operations</span></span>
- <span data-ttu-id="2ad63-144">ساعة واحدة لعمليات الإدراج المجمع</span><span class="sxs-lookup"><span data-stu-id="2ad63-144">One hour for bulk insert operations</span></span>

<span data-ttu-id="2ad63-145">عندما تكون وحدات التخزين عالية، فقد لا تكون إعدادات هذه المهلة كافيه.</span><span class="sxs-lookup"><span data-stu-id="2ad63-145">When volumes are high, these time-out settings might not be sufficient.</span></span> <span data-ttu-id="2ad63-146">لتحديثها، انتقل إلى **إدارة البيانات \> معلمات إطار العمل \>‫ إحضار قاعدة بياناتك الخاصة‬**.</span><span class="sxs-lookup"><span data-stu-id="2ad63-146">To update them, go to **Data management \> Framework parameters \> Bring your own database**.</span></span> <span data-ttu-id="2ad63-147">هذه المهلات خاصه بالشركة ويجب تعيينها بشكل منفصل لكل شركة.</span><span class="sxs-lookup"><span data-stu-id="2ad63-147">These time-outs are company-specific and must be set separately for each company.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="2ad63-148">القيود المعروفة</span><span class="sxs-lookup"><span data-stu-id="2ad63-148">Known limitations</span></span>

<span data-ttu-id="2ad63-149">ميزة BYOD بها القيود التالية:</span><span class="sxs-lookup"><span data-stu-id="2ad63-149">The BYOD feature has the following limitations:</span></span>

- <span data-ttu-id="2ad63-150">يجب ألا تكون هناك أية تامينات نشطة على قاعدة البيانات اثناء المزامنة.</span><span class="sxs-lookup"><span data-stu-id="2ad63-150">There should be no active locks on your database during synchronization.</span></span> <span data-ttu-id="2ad63-151">يمكن أن تؤدي عمليات التأمين النشطة إلى بطء الكتابة أو حتى الفشل في تصدير البيانات إلى قاعدة بيانات Azure SQL الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2ad63-151">Active locks can cause slow writes or even failure to export data to your Azure SQL database.</span></span>
- <span data-ttu-id="2ad63-152">لا يمكنك تصدير كيانات مركبة إلى قاعدة البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2ad63-152">You can't export composite entities into your own database.</span></span> <span data-ttu-id="2ad63-153">لا يتم دعم الكيانات المركبة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="2ad63-153">Currently, composite entities aren't supported.</span></span> <span data-ttu-id="2ad63-154">يجب تصدير الكيانات الفردية التي تشكل الكيان المركب.</span><span class="sxs-lookup"><span data-stu-id="2ad63-154">You must export individual entities that make up the composite entity.</span></span> <span data-ttu-id="2ad63-155">ومع ذلك يمكن تصدير كلا الكيانين في نفس مشروع البيانات.</span><span class="sxs-lookup"><span data-stu-id="2ad63-155">However, you can export both entities in the same data project.</span></span>
- <span data-ttu-id="2ad63-156">لا يمكن تصدير الكيانات التي لا تحتوي على مفاتيح فريدة باستخدام الدفع التزايدي.</span><span class="sxs-lookup"><span data-stu-id="2ad63-156">Entities that don't have unique keys can't be exported by using incremental push.</span></span> <span data-ttu-id="2ad63-157">قد تواجه هذه القيود خاصة عندما تحاول تصدير السجلات بشكل متزايد من بعض الكيانات الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="2ad63-157">You might face this limitation especially when you try to incrementally export records from a few ready-made entities.</span></span> <span data-ttu-id="2ad63-158">ونظرًا لان هذه الكيانات قد تم تصميمها لتمكين استيراد البيانات، فانها لا تحتوي على مفتاح فريد.</span><span class="sxs-lookup"><span data-stu-id="2ad63-158">Because these entities were designed to enable the import of data, they don't have a unique key.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2ad63-159">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="2ad63-159">Troubleshooting</span></span>

### <a name="incremental-push-doesnt-work-correctly"></a><span data-ttu-id="2ad63-160">لا يعمل الدفع التزايدي بشكل صحيح</span><span class="sxs-lookup"><span data-stu-id="2ad63-160">Incremental push doesn't work correctly</span></span>

<span data-ttu-id="2ad63-161">**المشكلة:** عند حدوث دفع كامل لأحد الكيانات، تشاهد مجموعة كبيرة من السجلات في BYOD عند استخدام عبارة **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="2ad63-161">**Issue:** When a full push occurs for an entity, you see a large set of records in BYOD when you use a **select** statement.</span></span> <span data-ttu-id="2ad63-162">ومع ذلك ، عندما تقوم بالدفع المتزايد، يمكنك الاطلاع على عدد قليل فقط من السجلات في BYOD.</span><span class="sxs-lookup"><span data-stu-id="2ad63-162">However, when you do an incremental push, you see only a few records in BYOD.</span></span> <span data-ttu-id="2ad63-163">ويبدو وكأن الدفع التزايدي قد حذف كافة السجلات وأضاف فقط السجلات التي تم تغييرها في BYOD.</span><span class="sxs-lookup"><span data-stu-id="2ad63-163">It seems as though the incremental push deleted all the records and added only the changed records in BYOD.</span></span>

<span data-ttu-id="2ad63-164">**الحل:** قد لا تكون جداول تتبع التغييرات في SQL في الحالة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="2ad63-164">**Solution:** The SQL change tracking tables might not be in the expected state.</span></span> <span data-ttu-id="2ad63-165">وفي هذه الحالات، نوصي بإيقاف تشغيل تعقب التغييرات للكيان ثم تشغيله مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="2ad63-165">In cases of this type, we recommend that you turn off change tracking for the entity and then turn it back on.</span></span> <span data-ttu-id="2ad63-166">لمزيد من المعلومات، راجع [‏‫تمكين تعقب التغيير للكيانات‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2ad63-166">For more information, see [Enable change tracking for entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="2ad63-167">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="2ad63-167">See also</span></span>

[<span data-ttu-id="2ad63-168">نظرة عامة حول إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="2ad63-168">Data management overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages?toc=/dynamics365/human-resources/toc.json)<br>
[<span data-ttu-id="2ad63-169">إحضار قاعدة بياناتك الخاصة (BYOD)</span><span class="sxs-lookup"><span data-stu-id="2ad63-169">Bring your own database (BYOD)</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)<br>
[<span data-ttu-id="2ad63-170">نظرة عامة حول مهام استيراد البيانات وتصديرها</span><span class="sxs-lookup"><span data-stu-id="2ad63-170">Data import and export jobs overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)<br>
[<span data-ttu-id="2ad63-171">تمكين تعقب التغيير للكيانات</span><span class="sxs-lookup"><span data-stu-id="2ad63-171">Enable change tracking for entities</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]