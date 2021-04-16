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
ms.openlocfilehash: a8c263104e209a81e33ea0db9e5fecddff3bc95b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809772"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="0da38-103">أحمال تنفيذ التصنيع لوحدات مقياس السحابة والحافة</span><span class="sxs-lookup"><span data-stu-id="0da38-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="0da38-104">لا يتم دعم بعض وظائف الاعمال بشكل كامل في المعاينة العامة عند استخدام حمل العمل على وحدات القياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-104">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="0da38-105">في تنفيذ عمليه التصنيع ، تقوم وحدات السحابة والحافة بتسليم الإمكانيات التالية ، حتى إذا لم تكن وحدات الحافة متصلة بالمركز:</span><span class="sxs-lookup"><span data-stu-id="0da38-105">In manufacturing execution, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the hub:</span></span>

- <span data-ttu-id="0da38-106">ويمكن لمشرفي حاله العمل ومشرفي حاله العمل الوصول إلى خطه الإنتاج الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="0da38-106">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="0da38-107">يمكن لعوامل تشغيل الجهاز الحفاظ علي الخطة محدثه عن طريق تشغيل وظائف التصنيع المنفصلة وعمليات التصنيع.</span><span class="sxs-lookup"><span data-stu-id="0da38-107">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="0da38-108">يمكن لمشرف حاله العمل تسويه خطه التشغيل.</span><span class="sxs-lookup"><span data-stu-id="0da38-108">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="0da38-109">يمكن للعاملين الوصول إلى الوقت والحضور لبدء العمل وإنهاء العمل علي الحافة ، وذلك لضمان حساب دفع العامل الصحيح.</span><span class="sxs-lookup"><span data-stu-id="0da38-109">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="0da38-110">يصف هذا الموضوع كيفيه عمل التصنيع في تنفيذ الاعمال مع وحدات مقياس السحابة والحافة.</span><span class="sxs-lookup"><span data-stu-id="0da38-110">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="0da38-111">دوره حياه التصنيع</span><span class="sxs-lookup"><span data-stu-id="0da38-111">The manufacturing lifecycle</span></span>

<span data-ttu-id="0da38-112">كما يوضح الرسم التوضيحي التالي ، تنقسم دوره حياه التصنيع إلى ثلاث مراحل: *التخطيط* و *التنفيذ* و *الإنهاء*.</span><span class="sxs-lookup"><span data-stu-id="0da38-112">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="0da38-113">[![مراحل تنفيذ التصنيع عند استخدام بيئة واحده](media/mes-phases.png "مراحل تنفيذ التصنيع عند استخدام بيئة واحده")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="0da38-113">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="0da38-114">تتضمن مرحله _الخطة_ تعريف المنتج والتخطيط وإنشاء الأمر وجدولته وإصداره.</span><span class="sxs-lookup"><span data-stu-id="0da38-114">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="0da38-115">تشير خطوه الإصدار إلى الانتقال من مرحله _التخطيط_ إلى مرحله _التنفيذ_.</span><span class="sxs-lookup"><span data-stu-id="0da38-115">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="0da38-116">عند إصدار أمر إنتاج ، ستكون وظائف أمر الإنتاج مرئية في حاله الإنتاج وتكون جاهزه للتنفيذ.</span><span class="sxs-lookup"><span data-stu-id="0da38-116">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="0da38-117">عند وضع علامة علي مهمة إنتاج كمكتملة ، فانها تنتقل من مرحله _التنفيذ_ إلى مرحلة _الإنهاء_.</span><span class="sxs-lookup"><span data-stu-id="0da38-117">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="0da38-118">في مرحله _الإنهاء_، تمر التسجيلات من مرحله *التنفيذ* خلال سير عمل الاعتماد ، حيث يتم حسابها واعتمادها وتحويلها.</span><span class="sxs-lookup"><span data-stu-id="0da38-118">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="0da38-119">وفي هذه المرحلة ، يتم إكمال أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="0da38-119">At that point, the production order is completed.</span></span> <span data-ttu-id="0da38-120">التالي ، يتم إنشاء أساس الدفع الخاص بالعاملين.</span><span class="sxs-lookup"><span data-stu-id="0da38-120">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="0da38-121">تقسيم مرحله "التنفيذ" إلى حمل عمل منفصل</span><span class="sxs-lookup"><span data-stu-id="0da38-121">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="0da38-122">كما يوضح الرسم التوضيحي التالي ، عند استخدام وحدات المقياس، يتم تقسيم مرحله _التنفيذ_ كحمل عمل منفصل.</span><span class="sxs-lookup"><span data-stu-id="0da38-122">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="0da38-123">[![مراحل تنفيذ التصنيع عند استخدام وحدات المقياس](media/mes-phases-workloads.png "مراحل تنفيذ التصنيع عند استخدام وحدات المقياس")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="0da38-123">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="0da38-124">ينتقل الآن الطراز من تثبيت مفرد المثيل إلى طراز يستند إلى وحدات المحور والمقياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-124">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="0da38-125">تعمل مرحلتا _التخطيط_ و _الإنهاء_ كعمليات المكتب الخلفي علي المركز، ويتم تشغيل حمل العمل الخاص بتنفيذ التصنيع علي وحدات المقياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-125">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="0da38-126">يتم نقل البيانات بشكل غير متزامن بين المركز ووحدات القياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-126">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="0da38-127">عند إصدار أمر إنتاج في المركز، يتم تحويل كافة البيانات المطلوبة لمعالجه وظائف الإنتاج إلى وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-127">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="0da38-128">وتشتمل هذه البيانات علي أوامر الإنتاج ومسارات الإنتاج وقائمة مكونات الصنف والمنتجات.</span><span class="sxs-lookup"><span data-stu-id="0da38-128">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="0da38-129">يتم أيضا تحويل البيانات غير المرتبطة بامر الإنتاج (مثل الانشطه غير المباشرة وأكواد الغياب ومحددات الإنتاج) من المركز إلى وحده المقياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-129">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="0da38-130">وكقاعده ، يمكن إنشاء البيانات التي تنشا من المركز والتي تم تحويلها إلى وحده القياس علي المركز فقط.</span><span class="sxs-lookup"><span data-stu-id="0da38-130">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="0da38-131">علي سبيل المثال ، لا يمكن إنشاء كود غياب جديد أو نشاط غير مباشر علي وحده المقياس، يمكن استخدامها فقط للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="0da38-131">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="0da38-132">يتم بعد ذلك تحويل التسجيلات التي تم اجراؤها علي وحده القياس اثناء التنفيذ إلى المركز، حيث تتم معالجه الموافقة علي الوقت والحضور والمخزون والتحديثات المالية.</span><span class="sxs-lookup"><span data-stu-id="0da38-132">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="0da38-133">مهام تنفيذ التصنيع التي يمكن تشغيلها علي أحمال العمل</span><span class="sxs-lookup"><span data-stu-id="0da38-133">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="0da38-134">يمكن تشغيل مهام تنفيذ التصنيع التالية علي أحمال العمل حاليا عند استخدام وحدات القياس:</span><span class="sxs-lookup"><span data-stu-id="0da38-134">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="0da38-135">بدء العمل وتسجيل الدخول وإنهاء العمل والغياب</span><span class="sxs-lookup"><span data-stu-id="0da38-135">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="0da38-136">بدء الوظيفة</span><span class="sxs-lookup"><span data-stu-id="0da38-136">Start job</span></span>
- <span data-ttu-id="0da38-137">مجموعة الوظائف</span><span class="sxs-lookup"><span data-stu-id="0da38-137">Bundle jobs</span></span>
- <span data-ttu-id="0da38-138">تقرير التقدم</span><span class="sxs-lookup"><span data-stu-id="0da38-138">Report progress</span></span>
- <span data-ttu-id="0da38-139">التبليغ عن الخردة</span><span class="sxs-lookup"><span data-stu-id="0da38-139">Report scrap</span></span>
- <span data-ttu-id="0da38-140">نشاط غير مباشر</span><span class="sxs-lookup"><span data-stu-id="0da38-140">Indirect activity</span></span>
- <span data-ttu-id="0da38-141">مقاطعة</span><span class="sxs-lookup"><span data-stu-id="0da38-141">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="0da38-142">العمل مع أحمال تنفيذ التصنيع علي المركز</span><span class="sxs-lookup"><span data-stu-id="0da38-142">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="0da38-143">عاده ، يتم تشغيل العمليات المطلوبة لتشغيل أحمال التنفيذ التصنيعية تلقائيا للاحتفاظ بالمركز ولكافة وحدات المقياس في المزامنة ، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="0da38-143">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="0da38-144">ومع ذلك ، إذا كانت لديك مشكله ، فيمكنك تشغيل معالجه التسجيلات الاوليه التي تم استلامها من أحمال العمل و/أو التحقق من سجل معالجه التسجيل.</span><span class="sxs-lookup"><span data-stu-id="0da38-144">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="0da38-145">معالجه التسجيلات الاوليه يدويا</span><span class="sxs-lookup"><span data-stu-id="0da38-145">Manually process raw registrations</span></span>

<span data-ttu-id="0da38-146">يتم تشغيل وظيفة المجموعة في Supply Chain Management تلقائيا لمعالجه كافة التسجيلات التي تم استلامها من أحمال العمل.</span><span class="sxs-lookup"><span data-stu-id="0da38-146">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="0da38-147">تقوم هذه الوظيفة بإنشاء دفاتر يوميه الإنتاج المطلوبة وإدخالات لوجبوك عند معالجه تسجيل لمهمة مكتملة في حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="0da38-147">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="0da38-148">علي الرغم من ان المهمة عاده ما تعمل تلقائيا ، الا انه يمكن تشغيلها يدويا في اي وقت عن طريق تسجيل الدخول إلى المركز والانتقال إلى **التحكم في الإنتاج \> المهام الدورية \> أداره حمل العمل في المكتب الخلفي\> معالجة عمليات التسجيل الأولي**.</span><span class="sxs-lookup"><span data-stu-id="0da38-148">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="0da38-149">التحقق من سجل معالجه التسجيل الاولي</span><span class="sxs-lookup"><span data-stu-id="0da38-149">Check the raw registration processing log</span></span>

<span data-ttu-id="0da38-150">لمراجعه سجل معالجه التسجيل ، قم بتسجيل الدخول إلى المركز ، ثم انتقل إلى **التحكم في الإنتاج \>المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \>سجل معالجه التسجيل الاولي**.</span><span class="sxs-lookup"><span data-stu-id="0da38-150">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="0da38-151">تعرض الصفحة **سجل معالجه التسجيل الاولي** قائمه بالتسجيلات الاوليه التي تمت معالجتها وحاله كل تسجيل.</span><span class="sxs-lookup"><span data-stu-id="0da38-151">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="0da38-152">![صفحة سجل معالجه التسجيل الاولي](media/mes-processing-log.png "صفحة سجل معالجه التسجيل الاولي")</span><span class="sxs-lookup"><span data-stu-id="0da38-152">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="0da38-153">يمكنك العمل علي اي تسجيل في القائمة وذلك بتحديده ثم تحديد أحد الأزرار التالية في جزء الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="0da38-153">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="0da38-154">**العملية** – معالجه التسجيل المحدد يدويا.</span><span class="sxs-lookup"><span data-stu-id="0da38-154">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="0da38-155">يمكن ان يكون هذا الاجراء مفيدا في حاله عدم تشغيل مهمة _معالجة التسجيلات الاوليه_ أو في حاله فشلها.</span><span class="sxs-lookup"><span data-stu-id="0da38-155">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="0da38-156">**إلغاء الأمر** – يستخدم للغاء التسجيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="0da38-156">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="0da38-157">العمل مع أحمال تنفيذ التصنيع علي وحدة المقياس</span><span class="sxs-lookup"><span data-stu-id="0da38-157">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="0da38-158">عاده ، يتم تشغيل العمليات المطلوبة لتشغيل أحمال التنفيذ التصنيعية تلقائيا للاحتفاظ بالمركز ولكافة وحدات المقياس في المزامنة ، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="0da38-158">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="0da38-159">ومع ذلك ، إذا كنت تواجه مشكله، فيمكنك التحقق من سجلات الأوامر التي تمت معالجتها علي وحده قياس أو تشغيل مهمة _معالج رسائل مركز التصنيع إلى وحدة القياس_ يدويًا.</span><span class="sxs-lookup"><span data-stu-id="0da38-159">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="0da38-160">عرض تاريخ مهام التصنيع التي تمت معالجتها علي وحده قياس</span><span class="sxs-lookup"><span data-stu-id="0da38-160">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="0da38-161">لمراجعه سجلات مهام التصنيع التي تمت معالجتها علي وحده قياس ، قم بتسجيل الدخول إلى جهاز وحده القياس ، ثم انتقل إلى **التحكم في الإنتاج\> المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \> سجل معالجة مهام التصنيع**.</span><span class="sxs-lookup"><span data-stu-id="0da38-161">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="0da38-162">تعرض صفحه **سجلات معالجه مهام التصنيع** سجل المعالجة الخاص بأوامر الإنتاج في وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-162">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="0da38-163">يمكنك العمل علي اي أمر إنتاج في القائمة وذلك بتحديده ثم تحديد أحد الأزرار التالية في جزء الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="0da38-163">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="0da38-164">**المعالجة** – معالجه أمر الإنتاج المحدد يدويا.</span><span class="sxs-lookup"><span data-stu-id="0da38-164">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="0da38-165">**إلغاء الأمر** – يستخدم لإلغاء أمر الإنتاج المحدد.</span><span class="sxs-lookup"><span data-stu-id="0da38-165">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="0da38-166">مهمة معالج رسائل مركز التصنيع إلى وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="0da38-166">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="0da38-167">تقوم مهمة _معالج رسائل مركز التصنيع إلى وحدة القياس_ بمعالجه البيانات من المركز إلى وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="0da38-167">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="0da38-168">يتم بدء هذه الوظيفة تلقائيا عند نشر حمل العمل الخاص بتنفيذ التصنيع.</span><span class="sxs-lookup"><span data-stu-id="0da38-168">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="0da38-169">ومع ذلك ، يمكن تشغيلها يدويا في اي وقت عن طريق الانتقال إلى **التحكم في الإنتاج \> المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \> معالج رسائل مركز التصنيع إلى وحدة القياس**.</span><span class="sxs-lookup"><span data-stu-id="0da38-169">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]