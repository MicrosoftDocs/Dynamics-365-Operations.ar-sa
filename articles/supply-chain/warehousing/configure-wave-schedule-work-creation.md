---
title: جدوله إنشاء العمل اثناء الموجه
description: يوضح هذا الموضوع كيفيه اعداد أسلوب معالجه الموجه واستخدامه في إنشاء العمل.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078228"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="71ea0-103">جدوله إنشاء العمل اثناء الموجه</span><span class="sxs-lookup"><span data-stu-id="71ea0-103">Schedule work creation during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71ea0-104">استخدم ميزة *جدوله إنشاء العمل* كجزء من عمليه إنشاء الموجات الخاصة بك للمساعدة في زيادة صافي معالجه الموجه وذلك بجعل النظام يقوم بإنشاء عمل باستخدام المعالجة المتوازية.</span><span class="sxs-lookup"><span data-stu-id="71ea0-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="71ea0-105">عند تمكين وظيفة، سيتم إنشاء العمل المخطط له تلقائيا، والذي سيقوم النظام أخيرا بمعالجته لإنشاء العمل الفعلي.</span><span class="sxs-lookup"><span data-stu-id="71ea0-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="71ea0-106">إذا وصل عدد أسطر تحميل الموجه إلى عتبه محدده مسبقا، سيقوم النظام بإنشاء العمل الفعلي بسرعة من خلال تطبيق المعالجة المتوازية غير المتزامنة.</span><span class="sxs-lookup"><span data-stu-id="71ea0-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="71ea0-107">تمكين ميزه جدوله إنشاء العمل</span><span class="sxs-lookup"><span data-stu-id="71ea0-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="71ea0-108">تمكين ميزة في إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="71ea0-108">Enable the feature in feature management</span></span>

<span data-ttu-id="71ea0-109">قبل أن تتمكن من استخدام ميزة *إنشاء جدولة العمل*، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="71ea0-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="71ea0-110">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="71ea0-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="71ea0-111">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="71ea0-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="71ea0-112">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="71ea0-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="71ea0-113">**اسم الميزة:** *جدوله إنشاء العمل*</span><span class="sxs-lookup"><span data-stu-id="71ea0-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="71ea0-114">يجب تمكين ميزه *حظر العمل علي مستوي المؤسسة* قبل ان تتمكن من تمكين *إنشاء عمل الجدولة*.</span><span class="sxs-lookup"><span data-stu-id="71ea0-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="71ea0-115">تمكين معالجه المجموعة الخاصة بالأمواج يدويا</span><span class="sxs-lookup"><span data-stu-id="71ea0-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="71ea0-116">للاستفادة من أسلوب غير متزامن متوازي لإنشاء عمل المستودع، يجب ان تكون عمليه الموجه الخاصة بك تعمل في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="71ea0-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="71ea0-117">لإعداد الأعمدة:</span><span class="sxs-lookup"><span data-stu-id="71ea0-117">To set this up:</span></span>

1. <span data-ttu-id="71ea0-118">انتقل إلى  **إدارة المستودعات \> الإعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="71ea0-119">في علامة التبويب **عام** قم بتعيين الخيار **معالجة الموجات في دُفعة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="71ea0-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="71ea0-120">بشكل اختياري، يمكنك أيضا تحديد **مجموعه دفعة معالجة الموجات** لمنع تشغيل معالجه قائمه انتظار الدفعات في نفس الوقت الذي يتم فيه تنفيذ العمليات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="71ea0-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="71ea0-121">تعيين **وقت الانتظار للتامين (بالملي ثانيه)**، والذي يتم تطبيقه عند قيام النظام بمعالجه عده موجات في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="71ea0-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="71ea0-122">للحصول علي العديد من عمليات إنشاء الموجات، نوصي بالقيمة *60000*.</span><span class="sxs-lookup"><span data-stu-id="71ea0-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="71ea0-123">تمكين الأسلوب الجديد لخطوه الموجة لقوالب الموجات الموجودة يدويا</span><span class="sxs-lookup"><span data-stu-id="71ea0-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="71ea0-124">أبدا بإنشاء طريقه جديده لخطوه الموجه وتمكينها لمعالجه المهام غير المتزامنة المتوازية.</span><span class="sxs-lookup"><span data-stu-id="71ea0-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="71ea0-125">انتقل إلى  **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="71ea0-126">حدد  **أسلوب أعاده الإنشاء** ولاحظ انه قد تمت أضافه قد تمت أضافه *WHSScheduleWorkCreationWaveStepMethod* إلى قائمه أساليب معالجه الموجات التي يمكنك استخدامها في قوالب موجه الشحن الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="71ea0-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="71ea0-127">حدد السجل الذي يحتوي علي **اسم الأسلوب** *WHSScheduleWorkCreationWaveStepMethod* وحدد **تكوين المهمة**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="71ea0-128">لإضافة صف في جزء الإجراء، حدد **جديد** في جزء الإجراء، ثم استخدم الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="71ea0-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="71ea0-129">**المستودع** - حدد المستودع الذي ستستخدمه لجدوله معالجه إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="71ea0-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="71ea0-130">**الحد الأقصى لعدد مهام المجموعات** - تحديد الحد الأقصى لعدد مهام الدفعات.</span><span class="sxs-lookup"><span data-stu-id="71ea0-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="71ea0-131">في معظم الحالات، يجب ان تكون هذه القيمة في النطاق من 8-16، ومع ذلك نوصي بتجربة الاعداد الأمثل وفقا للسيناريوهات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="71ea0-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="71ea0-132">**مجموعه الدفعة لمعالجه الموجه** - حدد مجموعه دفعات مخصصه لمعالجه الموجات لتحسين معالجه قائمه انتظار الدفعات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="71ea0-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="71ea0-133">الآن أنت مستعد لتحديث قالب الموجة موجود (أو إنشاء قالب جديد واحد) لاستخدام *أسلوب جدوله إنشاء الموجه لإنشاء العمل*.</span><span class="sxs-lookup"><span data-stu-id="71ea0-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="71ea0-134">انتقل إلى  **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="71ea0-135">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="71ea0-136">في جزء "القائمة"، حدد قالب الموجة الذي ترغب في تحديثه (إذا كنت تختبر باستخدام البيانات التجريبية، عندئذ يمكنك استخدام *24 الشحن الافتراضي*).</span><span class="sxs-lookup"><span data-stu-id="71ea0-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="71ea0-137">قم بتوسيع علامة التبويب السريعة **الأساليب** وحدد الصف الذي يحتوي علي **اسم** *إنشاء عمل جدول* في الشبكة التي تحتوي علي **الأساليب المتبقية**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="71ea0-138">حدد السهم الذي يشير إلى العمود **الأساليب المحددة** لنقل الصف المحدد إلى ذلك العمود.</span><span class="sxs-lookup"><span data-stu-id="71ea0-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="71ea0-139">(يمكن ان يكون لديك أسلوب واحد محدد فقط في الوقت الذي يستخدم اما *WHSScheduleWorkCreationWaveStepMethod* أو *createWork*، لذا فان الصف الموجود **باسم الأسلوب** *createWork* يتم نقله تلقائيا إلى شبكه **بقية الأساليب**.)</span><span class="sxs-lookup"><span data-stu-id="71ea0-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="71ea0-140">تعيين بيانات عتبه معالجه المهمة الموجهة</span><span class="sxs-lookup"><span data-stu-id="71ea0-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="71ea0-141">سيقوم النظام بإنشاء بيانات عتبه معالجه المهام الموجهة الافتراضية في المرة الاولي التي يتم فيها تشغيل عمليه موجه باستخدام إيه معالجه تستند إلى المهام.</span><span class="sxs-lookup"><span data-stu-id="71ea0-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="71ea0-142">يتم استخدام البيانات للتحكم في الوقت الذي سيتم فيه تشغيل معالجه الموجات بشكل غير متزامن وتستند إلى المهام ، والذي يمكنها من معالجه العمل وإنشاءه بالتوازي.</span><span class="sxs-lookup"><span data-stu-id="71ea0-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="71ea0-143">ستقوم البيانات الافتراضية في البداية باستخدام قيمه العتبة 15 للحد الأدنى لعدد خطوط التحميل (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="71ea0-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="71ea0-144">وهذا يعني انه عندما يعالج النظام موجه يحتوي علي أكثر من 15 سطرا يحمل الأسطر، فانه سيستخدم معالجه مهمة غير متزامنة.</span><span class="sxs-lookup"><span data-stu-id="71ea0-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="71ea0-145">يمكنك يدويا ادراج/تحديث هذه البيانات في الجدول **WHSWaveTaskProcessingThresholdParameters** في بيئات الاختبار الخاصة بك، ولكن إذا كنت بحاجه إلى تغيير هذا الاعداد في بيئة الإنتاج، فيجب عليك الاتصال بدعم Microsoft لطلب التحديث.</span><span class="sxs-lookup"><span data-stu-id="71ea0-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="71ea0-146">العمل مع الميزة</span><span class="sxs-lookup"><span data-stu-id="71ea0-146">Work with the feature</span></span>

<span data-ttu-id="71ea0-147">عند تمكين وظيفة *إنشاء عمل العمل*، ستقوم معالجه الموجه بإنشاء العمل المخطط له ، والذي سيتم استخدامه أخيرا بواسطة عمليه إنشاء العمل الجديدة.</span><span class="sxs-lookup"><span data-stu-id="71ea0-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="71ea0-148">واثناء إنشاء العمل، سيتم حظر العمل باستخدام *ميزه الحظر الخاصة بالعمل علي مستوي المؤسسة*.</span><span class="sxs-lookup"><span data-stu-id="71ea0-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="71ea0-149">يوضح المخطط الانسيابي التالي كيفيه إنشاء العمل المخطط اثناء معالجه الموجه.</span><span class="sxs-lookup"><span data-stu-id="71ea0-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![جدولة إنشاء العمل](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="71ea0-151">العمل المخطط</span><span class="sxs-lookup"><span data-stu-id="71ea0-151">Planned work</span></span>

<span data-ttu-id="71ea0-152">تظهر صفحه **تفاصيل العمل المخططة** (**إدارة المستودع \> العمل \>تفاصيل العمل المخططة**) معلومات حول العمل المخطط له، والذي يتم إنشاؤه مبدئيا اثناء معالجه الموجه.</span><span class="sxs-lookup"><span data-stu-id="71ea0-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="71ea0-153">وتتوفر قيم **حالة التقديم** التالية:</span><span class="sxs-lookup"><span data-stu-id="71ea0-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="71ea0-154">**في قائمه الانتظار** - ينتظر العمل المخطط استخدامه لإنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="71ea0-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="71ea0-155">**مكتمل** - تم استخدام العمل المخطط لإنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="71ea0-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="71ea0-156">**فشل** – فشلت معالجه الموجه.</span><span class="sxs-lookup"><span data-stu-id="71ea0-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="71ea0-157">لاحظ ان العمل المخطط يمكن ان يكون في حاله **فاشله** مع العمل الفعلي ذي الصلة أو بدونه.</span><span class="sxs-lookup"><span data-stu-id="71ea0-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="71ea0-158">عند فشل عمليه إنشاء العمل الفعلي، يظل العمل الفعلي في الحالة *ملغي*.</span><span class="sxs-lookup"><span data-stu-id="71ea0-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="71ea0-159">مهمة المجموعة لعمليه إنشاء العمل</span><span class="sxs-lookup"><span data-stu-id="71ea0-159">Batch job for the work creation process</span></span>

<span data-ttu-id="71ea0-160">لعرض وظائف المجموعة لمعالجه الموجات، حدد **وظائف الدفعة** في جزء الإجراءات في الصفحة **كافة الامواجات**.</span><span class="sxs-lookup"><span data-stu-id="71ea0-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="71ea0-161">من هنا ، يمكنك عرض كافة تفاصيل مهام المجموعة لكل معرف من معرفات الوظيفة الدفعيه.</span><span class="sxs-lookup"><span data-stu-id="71ea0-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>
