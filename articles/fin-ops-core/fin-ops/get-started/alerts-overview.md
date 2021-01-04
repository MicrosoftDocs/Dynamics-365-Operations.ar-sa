---
title: نظرة عامة على التنبيهات
description: يقدم هذا الموضوع معلومات عامة حول التنبيهات. يمكنك استخدام التنبيهات للتعرف على الأحداث التي تريد تعقبها أثناء يوم العمل.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 191f8a5d788f57964e7870167109e98cbde65c43
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694154"
---
# <a name="alerts-overview"></a><span data-ttu-id="e76c0-104">نظرة عامة على التنبيهات</span><span class="sxs-lookup"><span data-stu-id="e76c0-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="e76c0-105">حول التنبيهات</span><span class="sxs-lookup"><span data-stu-id="e76c0-105">About alerts</span></span>
<span data-ttu-id="e76c0-106">تشكّل التنبيهات نظام إخطار للأحداث المهمة في النظام.</span><span class="sxs-lookup"><span data-stu-id="e76c0-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="e76c0-107">يمكنك استخدام التنبيهات للتعرف على الأحداث التي تريد تعقبها أثناء يوم العمل.</span><span class="sxs-lookup"><span data-stu-id="e76c0-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="e76c0-108">يمكنك بسهولة إنشاء مجموعتك الخاصة من قواعد التنبيهات حتى يتم تنبيهك إلى عمليات التسليم المتأخرة أو الأوامر المحذوفة أو الأسعار التي تغيرت أو الأحداث الأخرى التي يجب أن تستجيب إليها.</span><span class="sxs-lookup"><span data-stu-id="e76c0-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="e76c0-109">في تخطيط موارد المؤسسات (ERP)، هناك العديد من السيناريوهات النموذجية التي يمكنك فيها استخدام ميزة التنبيهات.</span><span class="sxs-lookup"><span data-stu-id="e76c0-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="e76c0-110">فيما يلي بعض الأمثلة.</span><span class="sxs-lookup"><span data-stu-id="e76c0-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="e76c0-111">السيناريو 1: إنشاء قاعدة تنبيه لأوامر توريد جديدة</span><span class="sxs-lookup"><span data-stu-id="e76c0-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="e76c0-112">افتح صفحة **جميع أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="e76c0-113">في جزء الإجراءات، في علامة التبويب **خيارات**، في المجموعة **مشاركة**، حدد **إنشاء تنبيه مخصصة**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="e76c0-114">في مربع الحوار **إنشاء قاعدة تنبيه**، في علامة التبويب السريعة **تنبيهي عند**، في الحقل **حدث**، حدد **تم إنشاء سجل**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="e76c0-115">السيناريو 2: إنشاء قاعدة تنبيه لتأجيل تاريخ تسليم</span><span class="sxs-lookup"><span data-stu-id="e76c0-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="e76c0-116">افتح صفحة **جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="e76c0-117">حدد معرف أمر شراء للوصول إلى تفاصيل أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="e76c0-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="e76c0-118">قم بتوسيع علامة التبويب السريعة **رأس أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="e76c0-119">في جزء الإجراءات، في علامة التبويب **خيارات**، في المجموعة **مشاركة**، حدد **إنشاء تنبيه مخصصة**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="e76c0-120">في مربع الحوار **إنشاء قاعدة تنبيه**، في علامة التبويب السريعة **تنبيهي عند**، في الحقل **حقل**، حدد **تاريخ التسليم**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="e76c0-121">في الحقل **حدث**، حدد **تم تأجيله**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="e76c0-122">بعد أن تغلق مربع الحوار **إنشاء قاعدة تنبيه**، تظهر القاعدة الخاصة بك في صفحة **إدارة قواعد التنبيه**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="e76c0-123">يمكنك استخدام صفحة **إدارة قواعد التنبيه** لتحديث قواعد التنبيه الموجودة.</span><span class="sxs-lookup"><span data-stu-id="e76c0-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="e76c0-124">على سبيل المثال، يمكنك تعديل مشغلات الحدث، وتحديث إعلامات الأحداث، وتحديث تواريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="e76c0-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="e76c0-125">لفتح صفحة **إدارة قواعد التنبيه**، استخدم الزر **تنبيهي** الموجود في علامة التبويب **خيارات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e76c0-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="e76c0-126">ما الذي يحدث عند إنشاء قاعدة تنبيه؟</span><span class="sxs-lookup"><span data-stu-id="e76c0-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="e76c0-127">عند إنشاء قواعد التنبيه، يمكنك ربط حدث معرف مسبقًا بحقل معين.</span><span class="sxs-lookup"><span data-stu-id="e76c0-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="e76c0-128">على سبيل المثال، يصل التاريخ الذي تم تحديده في الحقل، أو تتغير محتويات الحقل.</span><span class="sxs-lookup"><span data-stu-id="e76c0-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="e76c0-129">بدلاً من ذلك، يمكن ربط حدث بالسجلات الموجودة في صفحة محددة.</span><span class="sxs-lookup"><span data-stu-id="e76c0-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="e76c0-130">على سبيل المثال، يتم إنشاء سجل أو حذف سجل.</span><span class="sxs-lookup"><span data-stu-id="e76c0-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="e76c0-131">عندما يقع الحدث المحدد للحقل أو لسجل في الصفحة، فإنه يتم إرسال تنبيه إليك.</span><span class="sxs-lookup"><span data-stu-id="e76c0-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="e76c0-132">على سبيل المثال، يمكنك إنشاء قاعدة يتم فيها ربط الحقل **تاريخ التسليم** في بند أمر شراء معين بحدث **كان مستحقًا منذ هذا القدر من الوقت‬**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="e76c0-133">يمكنك تعيين الإطار الزمني إلى خمسة أيام.</span><span class="sxs-lookup"><span data-stu-id="e76c0-133">You set the time frame to five days.</span></span> <span data-ttu-id="e76c0-134">في هذه الحالة، يتم إرسال تنبيه في غضون خمسة أيام بعد تاريخ تسليم بند أمر الشراء هذا.</span><span class="sxs-lookup"><span data-stu-id="e76c0-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="e76c0-135">بالإضافة إلى ذلك، يمكنك تحسين قواعد التنبيه عن طريق تعيين شروط.</span><span class="sxs-lookup"><span data-stu-id="e76c0-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="e76c0-136">على سبيل المثال، يمكن أن يتم تنبيهك بأوامر الشراء الجديدة التي تم إنشاؤها لحسابات الموردين المحددة.</span><span class="sxs-lookup"><span data-stu-id="e76c0-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="e76c0-137">الاستعداد لتنبيه</span><span class="sxs-lookup"><span data-stu-id="e76c0-137">Preparing for an alert</span></span>

<span data-ttu-id="e76c0-138">قبل إعداد قاعدة تنبيه، قرر متى وفي أي مواقف تحتاج فيها إلى تلقي التنبيهات.</span><span class="sxs-lookup"><span data-stu-id="e76c0-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="e76c0-139">عندما تعرف الحدث الذي تريد أن يتم إعلامك به، ابحث عن الصفحة التي توجد فيها البيانات التي تؤدي إلى ظهور هذا الحدث.</span><span class="sxs-lookup"><span data-stu-id="e76c0-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="e76c0-140">يمكن أن يكون الحدث تاريخًا يتم بلوغه أو تغييرًا محددًا يحدث.</span><span class="sxs-lookup"><span data-stu-id="e76c0-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="e76c0-141">لذلك، يجب البحث عن الصفحة التي يتم فيها تحديد التاريخ، أو الحقل الذي تظهر فيها هذه التغييرات أو السجل الجديد الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="e76c0-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="e76c0-142">بعد أن تتوفر لديك هذه المعلومات، يمكنك إنشاء قاعدة التنبيه.</span><span class="sxs-lookup"><span data-stu-id="e76c0-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="e76c0-143">مكونات قاعدة التنبيه</span><span class="sxs-lookup"><span data-stu-id="e76c0-143">Components of an alert rule</span></span>

<span data-ttu-id="e76c0-144">تشتمل قاعدة التنبيه على خمسة مكونات:</span><span class="sxs-lookup"><span data-stu-id="e76c0-144">An alert rule has five components:</span></span>

- <span data-ttu-id="e76c0-145">**الحدث** - قد يكون الحدث الذي يقوم بتشغيل قاعدة تنبيه تاريخ يتم بلوغه أو تغييرًا محددًا يحدث.</span><span class="sxs-lookup"><span data-stu-id="e76c0-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="e76c0-146">تحدد أنت الأحداث في علامة التبويب السريعة **إرسال تنبيهات البريد الإلكتروني لتغييرات حالة المهمة** في مربع الحوار **إنشاء قاعدة تنبيه**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="e76c0-147">**الشرط** - في علامة التبويب السريعة **التنبيه عن‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد نطاق الشرط، للتحكم عندما يتم تنبيهك بشأن أحداث.</span><span class="sxs-lookup"><span data-stu-id="e76c0-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="e76c0-148">يمكنك تطبيق القاعدة إما على السجل الحالي فقط أو جميع السجلات التي تظهر على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e76c0-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="e76c0-149">إذا كانت القاعدة تنطبق عبر الكيانات القانونية، يمكنك تعيين الخيار **على مستوى المؤسسة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e76c0-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="e76c0-150">**انتهاء صلاحية القاعدة** - في علامة التبويب السريعة **التنبيه حتى‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد المدة التي يجب أن تكون قاعدة التنبيه نشطة خلالها.</span><span class="sxs-lookup"><span data-stu-id="e76c0-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="e76c0-151">**المحتويات** - في علامة التبويب السريعة **‏‫التنبيه باستخدام‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد نص الموضوع ونص الرسالة التي يجب أن تستخدمها رسائل التنبيه.</span><span class="sxs-lookup"><span data-stu-id="e76c0-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="e76c0-152">**المستخدم** - في علامة التبويب السريعة **تنبيه إلى‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد المستخدم الذي يجب أن يتلقى رسائل التنبيه.</span><span class="sxs-lookup"><span data-stu-id="e76c0-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="e76c0-153">بشكل افتراضي، يتم تحديد معرف المستخدم الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e76c0-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e76c0-154">يتم تقييد هذا الخيار على مسؤولي المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="e76c0-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="e76c0-155">ملفات الفيديو</span><span class="sxs-lookup"><span data-stu-id="e76c0-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="e76c0-156">كيفيه استخدام التنبيهات لمراقبة البيانات المصفاة</span><span class="sxs-lookup"><span data-stu-id="e76c0-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="e76c0-157">تم تضمين الفيديو [كيفيه استخدام التنبيهات لمراقبة البيانات المصفاة](https://youtu.be/ZYKMcv6kl9s) (يظهر أعلاه) في [قائمة تشغيل Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) المتوفرة في YouTube.</span><span class="sxs-lookup"><span data-stu-id="e76c0-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="e76c0-158">خيارات قواعد التنبيه</span><span class="sxs-lookup"><span data-stu-id="e76c0-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="e76c0-159">تم تضمين الفيديو [خيارات قواعد التنبيه](https://youtu.be/cpzimwOjicM) (يظهر أعلاه) في [قائمة تشغيل Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) المتوفرة في YouTube.</span><span class="sxs-lookup"><span data-stu-id="e76c0-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


