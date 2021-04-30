---
title: أحمال تنفيذ التصنيع لوحدات مقياس السحابة والحافة
description: يصف هذا الموضوع كيفيه عمل التصنيع في تنفيذ الاعمال مع وحدات مقياس السحابة والحافة.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a6d6979093c67d2d89b88678712f4c0205c63194
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899085"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="f19d9-103">أحمال عمل تنفيذ التصنيع لوحدات النطاق السحابي والحافة</span><span class="sxs-lookup"><span data-stu-id="f19d9-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="f19d9-104">يتوفر حمل العمل الخاص بتنفيذ التصنيع في وضع الإصدار الأولي في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="f19d9-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="f19d9-105">لا يتم دعم بعض وظائف الاعمال بشكل كامل في المعاينة العامة عند استخدام حمل العمل على وحدات القياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="f19d9-106">في تنفيذ التصنيع، تقدم وحدات القياس القدرات التالية:</span><span class="sxs-lookup"><span data-stu-id="f19d9-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="f19d9-107">ويمكن لمشرفي حاله العمل ومشرفي حاله العمل الوصول إلى خطه الإنتاج الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="f19d9-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="f19d9-108">يمكن لعوامل تشغيل الجهاز الحفاظ علي الخطة محدثه عن طريق تشغيل وظائف التصنيع المنفصلة وعمليات التصنيع.</span><span class="sxs-lookup"><span data-stu-id="f19d9-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="f19d9-109">يمكن لمشرف حاله العمل تسويه خطه التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="f19d9-110">يمكن للعاملين الوصول إلى الوقت والحضور لبدء العمل وإنهاء العمل علي الحافة ، وذلك لضمان حساب دفع العامل الصحيح.</span><span class="sxs-lookup"><span data-stu-id="f19d9-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="f19d9-111">يصف هذا الموضوع كيفيه عمل التصنيع في تنفيذ الاعمال مع وحدات مقياس السحابة والحافة.</span><span class="sxs-lookup"><span data-stu-id="f19d9-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="f19d9-112">دوره حياه التصنيع</span><span class="sxs-lookup"><span data-stu-id="f19d9-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="f19d9-113">كما يوضح الرسم التوضيحي التالي ، تنقسم دوره حياه التصنيع إلى ثلاث مراحل: *التخطيط* و *التنفيذ* و *الإنهاء*.</span><span class="sxs-lookup"><span data-stu-id="f19d9-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="f19d9-114">[![مراحل تنفيذ التصنيع عند استخدام بيئة واحده](media/mes-phases.png "مراحل تنفيذ التصنيع عند استخدام بيئة واحده")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="f19d9-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="f19d9-115">تتضمن مرحله _الخطة_ تعريف المنتج والتخطيط وإنشاء الأمر وجدولته وإصداره.</span><span class="sxs-lookup"><span data-stu-id="f19d9-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="f19d9-116">تشير خطوه الإصدار إلى الانتقال من مرحله _التخطيط_ إلى مرحله _التنفيذ_.</span><span class="sxs-lookup"><span data-stu-id="f19d9-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="f19d9-117">عند إصدار أمر إنتاج ، ستكون وظائف أمر الإنتاج مرئية في حاله الإنتاج وتكون جاهزه للتنفيذ.</span><span class="sxs-lookup"><span data-stu-id="f19d9-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="f19d9-118">عند وضع علامة علي مهمة إنتاج كمكتملة ، فانها تنتقل من مرحله _التنفيذ_ إلى مرحلة _الإنهاء_.</span><span class="sxs-lookup"><span data-stu-id="f19d9-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="f19d9-119">في مرحله _الإنهاء_، تمر التسجيلات من مرحله *التنفيذ* خلال سير عمل الاعتماد ، حيث يتم حسابها واعتمادها وتحويلها.</span><span class="sxs-lookup"><span data-stu-id="f19d9-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="f19d9-120">وفي هذه المرحلة ، يتم إكمال أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f19d9-120">At that point, the production order is completed.</span></span> <span data-ttu-id="f19d9-121">التالي ، يتم إنشاء أساس الدفع الخاص بالعاملين.</span><span class="sxs-lookup"><span data-stu-id="f19d9-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="f19d9-122">تقسيم مرحله "التنفيذ" إلى حمل عمل منفصل</span><span class="sxs-lookup"><span data-stu-id="f19d9-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="f19d9-123">كما يوضح الرسم التوضيحي التالي ، عند استخدام وحدات المقياس، يتم تقسيم مرحله _التنفيذ_ كحمل عمل منفصل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="f19d9-124">[![مراحل تنفيذ التصنيع عند استخدام وحدات المقياس](media/mes-phases-workloads.png "مراحل تنفيذ التصنيع عند استخدام وحدات المقياس")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="f19d9-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="f19d9-125">ينتقل الآن الطراز من تثبيت مفرد المثيل إلى طراز يستند إلى وحدات المحور والمقياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="f19d9-126">تعمل مرحلتا _التخطيط_ و _الإنهاء_ كعمليات المكتب الخلفي علي المركز، ويتم تشغيل حمل العمل الخاص بتنفيذ التصنيع علي وحدات المقياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="f19d9-127">يتم نقل البيانات بشكل غير متزامن بين المركز ووحدات القياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="f19d9-128">عند إصدار أمر إنتاج في المركز، يتم تحويل كافة البيانات المطلوبة لمعالجه وظائف الإنتاج إلى وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="f19d9-129">وتشتمل هذه البيانات علي أوامر الإنتاج ومسارات الإنتاج وقائمة مكونات الصنف والمنتجات.</span><span class="sxs-lookup"><span data-stu-id="f19d9-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="f19d9-130">يتم أيضا تحويل البيانات غير المرتبطة بامر الإنتاج (مثل الانشطه غير المباشرة وأكواد الغياب ومحددات الإنتاج) من المركز إلى وحده المقياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="f19d9-131">وكقاعده ، يمكن إنشاء البيانات التي تنشا من المركز والتي تم تحويلها إلى وحده القياس علي المركز فقط.</span><span class="sxs-lookup"><span data-stu-id="f19d9-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="f19d9-132">علي سبيل المثال ، لا يمكن إنشاء كود غياب جديد أو نشاط غير مباشر علي وحده المقياس، يمكن استخدامها فقط للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="f19d9-133">يتم بعد ذلك تحويل التسجيلات التي تم اجراؤها علي وحده القياس اثناء التنفيذ إلى المركز، حيث تتم معالجه الموافقة علي الوقت والحضور والمخزون والتحديثات المالية.</span><span class="sxs-lookup"><span data-stu-id="f19d9-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="f19d9-134">مهام تنفيذ التصنيع التي يمكن تشغيلها علي أحمال العمل</span><span class="sxs-lookup"><span data-stu-id="f19d9-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="f19d9-135">يمكن تشغيل مهام تنفيذ التصنيع التالية علي أحمال العمل حاليا عند استخدام وحدات القياس:</span><span class="sxs-lookup"><span data-stu-id="f19d9-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="f19d9-136">بدء العمل وتسجيل الدخول وإنهاء العمل والغياب</span><span class="sxs-lookup"><span data-stu-id="f19d9-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="f19d9-137">بدء الوظيفة</span><span class="sxs-lookup"><span data-stu-id="f19d9-137">Start job</span></span>
- <span data-ttu-id="f19d9-138">مجموعة الوظائف</span><span class="sxs-lookup"><span data-stu-id="f19d9-138">Bundle jobs</span></span>
- <span data-ttu-id="f19d9-139">تقرير التقدم</span><span class="sxs-lookup"><span data-stu-id="f19d9-139">Report progress</span></span>
- <span data-ttu-id="f19d9-140">التبليغ عن الخردة</span><span class="sxs-lookup"><span data-stu-id="f19d9-140">Report scrap</span></span>
- <span data-ttu-id="f19d9-141">نشاط غير مباشر</span><span class="sxs-lookup"><span data-stu-id="f19d9-141">Indirect activity</span></span>
- <span data-ttu-id="f19d9-142">مقاطعة</span><span class="sxs-lookup"><span data-stu-id="f19d9-142">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="f19d9-143">العمل مع أحمال تنفيذ التصنيع علي المركز</span><span class="sxs-lookup"><span data-stu-id="f19d9-143">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="f19d9-144">عاده ، يتم تشغيل العمليات المطلوبة لتشغيل أحمال التنفيذ التصنيعية تلقائيا للاحتفاظ بالمركز ولكافة وحدات المقياس في المزامنة ، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="f19d9-144">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="f19d9-145">ومع ذلك ، إذا كانت لديك مشكله ، فيمكنك تشغيل معالجه التسجيلات الاوليه التي تم استلامها من أحمال العمل و/أو التحقق من سجل معالجه التسجيل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-145">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="f19d9-146">معالجه التسجيلات الاوليه يدويا</span><span class="sxs-lookup"><span data-stu-id="f19d9-146">Manually process raw registrations</span></span>

<span data-ttu-id="f19d9-147">يتم تشغيل وظيفة المجموعة في Supply Chain Management تلقائيا لمعالجه كافة التسجيلات التي تم استلامها من أحمال العمل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-147">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="f19d9-148">تقوم هذه الوظيفة بإنشاء دفاتر يوميه الإنتاج المطلوبة وإدخالات لوجبوك عند معالجه تسجيل لمهمة مكتملة في حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-148">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="f19d9-149">علي الرغم من ان المهمة عاده ما تعمل تلقائيا ، الا انه يمكن تشغيلها يدويا في اي وقت عن طريق تسجيل الدخول إلى المركز والانتقال إلى **التحكم في الإنتاج \> المهام الدورية \> أداره حمل العمل في المكتب الخلفي\> معالجة عمليات التسجيل الأولي**.</span><span class="sxs-lookup"><span data-stu-id="f19d9-149">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="f19d9-150">التحقق من سجل معالجه التسجيل الاولي</span><span class="sxs-lookup"><span data-stu-id="f19d9-150">Check the raw registration processing log</span></span>

<span data-ttu-id="f19d9-151">لمراجعه سجل معالجه التسجيل ، قم بتسجيل الدخول إلى المركز ، ثم انتقل إلى **التحكم في الإنتاج \>المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \>سجل معالجه التسجيل الاولي**.</span><span class="sxs-lookup"><span data-stu-id="f19d9-151">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="f19d9-152">تعرض الصفحة **سجل معالجه التسجيل الاولي** قائمه بالتسجيلات الاوليه التي تمت معالجتها وحاله كل تسجيل.</span><span class="sxs-lookup"><span data-stu-id="f19d9-152">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="f19d9-153">![صفحة سجل معالجه التسجيل الاولي](media/mes-processing-log.png "صفحة سجل معالجه التسجيل الاولي")</span><span class="sxs-lookup"><span data-stu-id="f19d9-153">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="f19d9-154">يمكنك العمل علي اي تسجيل في القائمة وذلك بتحديده ثم تحديد أحد الأزرار التالية في جزء الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="f19d9-154">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="f19d9-155">**العملية** – معالجه التسجيل المحدد يدويا.</span><span class="sxs-lookup"><span data-stu-id="f19d9-155">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="f19d9-156">يمكن ان يكون هذا الاجراء مفيدا في حاله عدم تشغيل مهمة _معالجة التسجيلات الاوليه_ أو في حاله فشلها.</span><span class="sxs-lookup"><span data-stu-id="f19d9-156">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="f19d9-157">**إلغاء الأمر** – يستخدم للغاء التسجيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="f19d9-157">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="f19d9-158">العمل مع أحمال تنفيذ التصنيع علي وحدة المقياس</span><span class="sxs-lookup"><span data-stu-id="f19d9-158">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="f19d9-159">عاده ، يتم تشغيل العمليات المطلوبة لتشغيل أحمال التنفيذ التصنيعية تلقائيا للاحتفاظ بالمركز ولكافة وحدات المقياس في المزامنة ، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="f19d9-159">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="f19d9-160">ومع ذلك ، إذا كنت تواجه مشكله، فيمكنك التحقق من سجلات الأوامر التي تمت معالجتها علي وحده قياس أو تشغيل مهمة _معالج رسائل مركز التصنيع إلى وحدة القياس_ يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f19d9-160">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="f19d9-161">عرض تاريخ مهام التصنيع التي تمت معالجتها علي وحده قياس</span><span class="sxs-lookup"><span data-stu-id="f19d9-161">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="f19d9-162">لمراجعه سجلات مهام التصنيع التي تمت معالجتها علي وحده قياس ، قم بتسجيل الدخول إلى جهاز وحده القياس ، ثم انتقل إلى **التحكم في الإنتاج\> المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \> سجل معالجة مهام التصنيع**.</span><span class="sxs-lookup"><span data-stu-id="f19d9-162">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="f19d9-163">تعرض صفحه **سجلات معالجه مهام التصنيع** سجل المعالجة الخاص بأوامر الإنتاج في وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-163">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="f19d9-164">يمكنك العمل علي اي أمر إنتاج في القائمة وذلك بتحديده ثم تحديد أحد الأزرار التالية في جزء الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="f19d9-164">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="f19d9-165">**المعالجة** – معالجه أمر الإنتاج المحدد يدويا.</span><span class="sxs-lookup"><span data-stu-id="f19d9-165">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="f19d9-166">**إلغاء الأمر** – يستخدم لإلغاء أمر الإنتاج المحدد.</span><span class="sxs-lookup"><span data-stu-id="f19d9-166">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="f19d9-167">مهمة معالج رسائل مركز التصنيع إلى وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="f19d9-167">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="f19d9-168">تقوم مهمة _معالج رسائل مركز التصنيع إلى وحدة القياس_ بمعالجه البيانات من المركز إلى وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="f19d9-168">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="f19d9-169">يتم بدء هذه الوظيفة تلقائيا عند نشر حمل العمل الخاص بتنفيذ التصنيع.</span><span class="sxs-lookup"><span data-stu-id="f19d9-169">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="f19d9-170">ومع ذلك ، يمكن تشغيلها يدويا في اي وقت عن طريق الانتقال إلى **التحكم في الإنتاج \> المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \> معالج رسائل مركز التصنيع إلى وحدة القياس**.</span><span class="sxs-lookup"><span data-stu-id="f19d9-170">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
