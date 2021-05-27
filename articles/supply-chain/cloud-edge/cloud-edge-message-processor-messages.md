---
title: رسائل معالج الرسالة
description: يوفر هذا الموضوع معلومات حول ميزة رسائل معالج الرسائل لأحمال عمل وحدة القياس.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021045"
---
# <a name="message-processor-messages"></a><span data-ttu-id="bec76-103">رسائل معالج الرسالة</span><span class="sxs-lookup"><span data-stu-id="bec76-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bec76-104">تُستخدم رسائل معالج الرسائل عند تشغيل وحدات القياس السحابية والحافة لـ [أحمال عمل التصنيع](cloud-edge-workload-manufacturing.md) و[أحمال عمل إدارة المستودع](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="bec76-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="bec76-105">يتم تبادل قدر كبير من البيانات بين المحور وبيئات نشر وحدة القياس لإبقائها متزامنة، ولكن سيتم معالجة عدد قليل فقط من عمليات تبادل البيانات هذه بواسطة *معالج الرسائل*.</span><span class="sxs-lookup"><span data-stu-id="bec76-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="bec76-106">يمكنك عرض الرسائل التي تمت معالجتها بواسطة معالج الرسائل بالانتقال إلى **إدارة النظام > معالج الرسائل > رسائل معالج الرسائل**.</span><span class="sxs-lookup"><span data-stu-id="bec76-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="bec76-107">أعمده وعوامل تصفية شبكه الرسائل</span><span class="sxs-lookup"><span data-stu-id="bec76-107">Message grid columns and filters</span></span>

<span data-ttu-id="bec76-108">يمكنك استخدام الحقول الموجودة أعلى صفحة **رسائل معالج الرسائل** للمساعدة في العثور على أي رسائل معينة تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="bec76-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="bec76-109">تطابق معظم عوامل التصفية هذه عناوين الأعمدة في شبكة الرسائل.</span><span class="sxs-lookup"><span data-stu-id="bec76-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="bec76-110">تتوفر عوامل التصفية وعناوين الأعمده التالية:</span><span class="sxs-lookup"><span data-stu-id="bec76-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="bec76-111">**نوع الرسالة** – يحدد نوع الرسالة.</span><span class="sxs-lookup"><span data-stu-id="bec76-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="bec76-112">**قائمة انتظار الرسائل** – تحدد اسم قائمة الانتظار التي ستتم معالجة الرسالة فيها.</span><span class="sxs-lookup"><span data-stu-id="bec76-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="bec76-113">يتم توفير قوائم الانتظار التالية:</span><span class="sxs-lookup"><span data-stu-id="bec76-113">The following queues are provided:</span></span>
  - <span data-ttu-id="bec76-114">*وحدة القياس إلى المركز*</span><span class="sxs-lookup"><span data-stu-id="bec76-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="bec76-115">*وحده مقياس تنفيذ المركز إلى المستودع*</span><span class="sxs-lookup"><span data-stu-id="bec76-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="bec76-116">*المركز لوحدة قياس تنفيذ التصنيع*</span><span class="sxs-lookup"><span data-stu-id="bec76-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="bec76-117">**حالة الرسالة** – تحدد حالة الرسالة.</span><span class="sxs-lookup"><span data-stu-id="bec76-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="bec76-118">تتوفر الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="bec76-118">The following states exists:</span></span>
  - <span data-ttu-id="bec76-119">*في قائمة الانتظار* – الرسالة جاهزة للمعالجة بواسطة معالج الرسائل.</span><span class="sxs-lookup"><span data-stu-id="bec76-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="bec76-120">*تمت المعالجة* – تمت معالجة الرسالة بنجاح بواسطة معالج الرسائل.</span><span class="sxs-lookup"><span data-stu-id="bec76-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="bec76-121">*تم الإلغاء* – تمت معالجة الرسالة ولكن فشلت المعالجة.</span><span class="sxs-lookup"><span data-stu-id="bec76-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="bec76-122">**محتوى الرسالة** – يقوم عامل التصفية هذا بالبحث عن نص كامل لمحتوى الرسالة.</span><span class="sxs-lookup"><span data-stu-id="bec76-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="bec76-123">(لا يظهر محتوى الرسالة في الشبكة.) يعامل عامل التصفية الرموز الخاصة (مثل "-") على أنها مسافات، ويعامل جميع أحرف المسافات كعوامل تشغيل OR منطقية.</span><span class="sxs-lookup"><span data-stu-id="bec76-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="bec76-124">T = على سبيل المثال، هذا يعني أنك إذا كنت تبحث عن قيمة `journalid` محددة تساوي "USMF-123456"، سيجد النظام جميع الرسائل التي تحتوي على "USMF" أو "123456"، والتي من المحتمل أن تكون قائمة طويلة.</span><span class="sxs-lookup"><span data-stu-id="bec76-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="bec76-125">ولذلك، من الأفضل إدخال "123456" فقط لأن ذلك سيؤدي إلى نتائج أكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="bec76-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="bec76-126">مثال لنوع الرسالة: طلب تحديث مالي لتسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="bec76-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="bec76-127">على سبيل المثال، يتم استخدام **نوع الرسالة** *طلب تحديث مالي لتسوية المخزون* لإنشاء ونشر دفتر يومية جرد على المركز عندما يستخدم عامل تطبيق المستودع من أجل [تسجيل تسوية مخزون](cloud-edge-warehouse-inventory-adjustment.md) في حمل عمل إدارة مستودع وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="bec76-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="bec76-128">لأن هذه العملية المحددة تنشأ من وحدة قياس، فإن **قائمة انتظار الرسائل** ستعرض قيمة *وحدة القياس للمركز*.</span><span class="sxs-lookup"><span data-stu-id="bec76-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="bec76-129">بالنسبة لنوع الرسالة هذا، يسجل حمل عمل وحدة القياس الرسالة كجزء من عملية تسوية مخزون تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="bec76-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="bec76-130">يتم بعد ذلك نقل بيانات الرسالة إلى الموزع كجزء من نفس العملية المستخدمة في [بنية Commerce data exchange](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="bec76-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="bec76-131">سيتم تحديث الرسالة لعرض **حالة الرسالة** كـ *في قائمة الانتظار*.</span><span class="sxs-lookup"><span data-stu-id="bec76-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="bec76-132">ثم يحاول معالج الرسائل معالجة الرسالة ويقوم بتحديث **حالة الرسالة** إلى *تمت المعالجة* في حالة النجاح أو *تم الإلغاء* في حالة الفشل.</span><span class="sxs-lookup"><span data-stu-id="bec76-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="bec76-133">عرض سجل الرسائل ومحتوى الرسائل والتفاصيل</span><span class="sxs-lookup"><span data-stu-id="bec76-133">View the message log, message content, and details</span></span>

<span data-ttu-id="bec76-134">يمكنك العثور على معلومات مفصلة حول رسالة عن طريق تحديدها في الشبكة ثم فتح علامة التبويب **السجل** أو **محتوى الرسالة** ضمن شبكة الرسائل، حيث يتم عرض كل حدث معالجة.</span><span class="sxs-lookup"><span data-stu-id="bec76-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="bec76-135">يعتمد **محتوى الرسالة** على **نوع الرسالة** وبالتالي سيكون له طول نص مختلف.</span><span class="sxs-lookup"><span data-stu-id="bec76-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="bec76-136">سيبدأ نص محتوى الرسالة النموذجي بـ **{** وسينتهي بـ **}** وبينهما يكون له أسماء حقول مثل `journalId` متبوعة بـ **:** وقيمة مثل *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="bec76-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="bec76-137">يتضمن شريط الأدوات الموجود في علامة التبويب **السجل** الأزرار التالية:</span><span class="sxs-lookup"><span data-stu-id="bec76-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="bec76-138">**السجل** – يعرض نتائج المعالجة.</span><span class="sxs-lookup"><span data-stu-id="bec76-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="bec76-139">هذا مفيد بشكل خاص لفهم أسباب فشل معالجة الرسائل التي تحتوي على **نتيجة معالجة** بالحالة *فاشلة*.</span><span class="sxs-lookup"><span data-stu-id="bec76-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="bec76-140">**مجموعة** – يمكن تشغيل عمليات معالجة الرسائل المتعددة كجزء من نفس عملية الدفعة.</span><span class="sxs-lookup"><span data-stu-id="bec76-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="bec76-141">حدد هذا الزر لعرض هذه البيانات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="bec76-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="bec76-142">على سبيل المثال، يمكنك معرفة ما إذا كانت التبعيات موجودة والتي تتطلب من النظام معالجة رسائل معينة في تسلسل معين.</span><span class="sxs-lookup"><span data-stu-id="bec76-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="bec76-143">وظيفة دفعة معالج الرسائل</span><span class="sxs-lookup"><span data-stu-id="bec76-143">Message processor batch job</span></span>

<span data-ttu-id="bec76-144">عند تشغيل سحابة ونشر الحافة، يتم إلغاء وظيفة دفعة *معالج الرسائل* تلقائيًا عند إنشاء رسالة جديدة للمعالجة، لذا لن تحتاج إلى جدولة هذه المهمة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="bec76-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="bec76-145">وإذا لزم الأمر، يمكنك الوصول إلى وظيفة الدفعة بواسطة الانتقال إلى **إدارة النظام > معالج الرسائل > معالج الرسائل**.</span><span class="sxs-lookup"><span data-stu-id="bec76-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="bec76-146">معالجة رسالة أو إلغاؤها يدويًا</span><span class="sxs-lookup"><span data-stu-id="bec76-146">Manually process or cancel a message</span></span>

<span data-ttu-id="bec76-147">إذا لزم الأمر، يمكنك معالجه رسالة أو إلغاؤها يدويًا، وذلك وفقًا لحالتها الحالية.</span><span class="sxs-lookup"><span data-stu-id="bec76-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="bec76-148">للقيام بذلك، حدد الرسالة الموجودة في الشبكة ثم حدد **معالجة** أو **إلغاء الأمر** في جزء الإجراءات</span><span class="sxs-lookup"><span data-stu-id="bec76-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="bec76-149">إعداد أحداث العمل لتسليم تنبيهات لنتائج المعالجة الفاشلة</span><span class="sxs-lookup"><span data-stu-id="bec76-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="bec76-150">بالإضافة إلى أن تصفية قيمة **حالة الرسالة** *تم إلغاؤها* للاستعلام عن الرسائل الفاشلة، يمكنك إعداد [أحداث الأعمال](../../fin-ops-core/dev-itpro/business-events/home-page.md) في المركز لتنبيهك إلى نتائج المعالجة الفاشلة.</span><span class="sxs-lookup"><span data-stu-id="bec76-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="bec76-151">للقيام بذلك، قم بتنشيط حدث العمل المسمى *تمت معالجة رسالة معالج الرسائل* في صفحة **كتالوج أحداث الأعمال** (**إدارة النظام > الإعداد > أحداث الأعمال > كتالوج أحداث الأعمال**).</span><span class="sxs-lookup"><span data-stu-id="bec76-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="bec76-152">كجزء من عملية التنشيط، سيتم إرشادك لتحديد ما إذا كان الحدث خاصًا بواحد أو جميع الكيانات القانونية وتقديم **اسم النهاية**، الذي يجب تحديده أولاً.</span><span class="sxs-lookup"><span data-stu-id="bec76-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="bec76-153">في حالة تعيين **عند حدوث حدث أعمال** إلى *Microsoft Power Automate* (بدلاً من *HTTPS*، مثلاً)، فسيتم إنشاء **اسم نقطة النهاية** تلقائيًا في Supply Chain Management استنادًا إلى إعداد *Microsoft Power Automate*.</span><span class="sxs-lookup"><span data-stu-id="bec76-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="bec76-154">مثال لـ Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="bec76-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="bec76-155">في هذا المثال، استخدم **عند حدوث حدث أعمال** مع قيام *Microsoft Power Automate* بإرسال رسائل البريد الإلكتروني التي تحتوي على رسائل InfoLog والارتباطات التشعبية لفتح صفحة **رسائل معالج الرسائل** للحصول على رسالة فاشلة محددة في توزيع المركز.</span><span class="sxs-lookup"><span data-stu-id="bec76-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="bec76-156">إذا لزم الأمر، يمكنك إضافة منطق إضافي لإرسال الإشعارات بالتوازي باستخدام قنوات مختلفة والتحكم في المستلمين بناءً على بيانات الحدث.</span><span class="sxs-lookup"><span data-stu-id="bec76-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="bec76-157">في [Power Automate](https://preview.flow.microsoft.com)، أنشئ تدفقًا سحابيًا تلقائيًا جديدًا لمشغل التدفق **عند حدوث حدث عمل - تطبيق Fin & Ops ‏(Dynamics 365)** متبوعةً بخطوتي **تحليل JSON** و **إرسال رسالة بريد إلكتروني**، كما هو مبين في الرسو التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="bec76-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="تدفق السحابة التلقائي في Power Automate":::

1. <span data-ttu-id="bec76-159">في خطوة **عند حدوث حدث أعمال**، يمكنك البحث أو إدخال **مثيل** المركز متبوعًا بـ **الفئة** ثم **حدث الأعمال** *تمت معالجة رسالة معالج الرسائل*، كما هو مبين في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="bec76-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate خطوة عند حدوث حدث أعمال":::

1. <span data-ttu-id="bec76-161">بالنسبة لخطوة **تحليل JSON**، أدخل **المخطط** الذي يحدد الحقول الموسعة.</span><span class="sxs-lookup"><span data-stu-id="bec76-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="bec76-162">يمكنك استخدام خيار *تنزيل المخطط* في صفحة **كتالوج أحداث الأعمال** في Supply Chain Management أو ابدأ باللصق في مثال نص المخطط.</span><span class="sxs-lookup"><span data-stu-id="bec76-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="bec76-163">يتم توفير نص المثال هذا بعد الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="bec76-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate خطوة تحليل JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="bec76-165">في خطوة **إرسال رسالة بريد إلكتروني**، يمكنك تحديد الحقول الفردية أو البدء بلصق مثال نص البريد الإلكتروني في حقل **المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="bec76-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="bec76-166">يتم توفير هذا المثال بعد الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="bec76-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="خطة إرسال رسالة بريد إلكتروني في Power Automate":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="bec76-168">عند حفظ حدث العمل، سيتم تنشيطه تلقائيًا ويكون جاهزًا للاستخدام كجزء من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bec76-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
