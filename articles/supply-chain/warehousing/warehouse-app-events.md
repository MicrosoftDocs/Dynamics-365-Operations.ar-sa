---
title: أحداث تطبيق المستودع
description: يصف هذا الموضوع معالجه حدث تطبيق المستودع المستخدمة في معالجه رسائل حدث تطبيق المستودع كجزء من مهمة دُفعة.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d63cdea8917bed762bf8d970a408e5931aec48b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837383"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="3ccb4-103">معالجة حدث المستودع للتطبيق</span><span class="sxs-lookup"><span data-stu-id="3ccb4-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ccb4-104">يمكن لمهام الدُفعة التي تعمل في Supply Chain Management استخدام بيانات من قائمه انتظار لاحداث المعالجة التي تم إصدارها بواسطة تطبيق إدارة المستودع للأجهزة المحمولة لاستخدام الاحداث التي تمت الاشاره اليها.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the Warehouse Management mobile app to react as needed to the signaled events.</span></span> <span data-ttu-id="3ccb4-105">تضيف هذه الميزة الاحداث ذات الصلة إلى قائمه الانتظار كاستجابة لأنواع معينه من الإجراءات التي تاخذها العمال باستخدام التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="3ccb4-106">مثال علي ذلك، عند استخدام ميزة *إنشاء ومعالجه أوامر التحويل من تطبيق المستودع*، يتم إنشاء وتحديث البنود وراس أمر التحويل في النهاية الخلفية عندما يقوم النظام بتشغيل وظيفة الدُفعة **احداث التطبيق الخاصة بمستودع العمليات**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-106">An example is when using the *Create and process transfer orders from the warehouse app* feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="3ccb4-107">تمكين ميزه احداث التطبيق لمستودع العملية</span><span class="sxs-lookup"><span data-stu-id="3ccb4-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="3ccb4-108">قبل أن تتمكن من استخدام هذه الميزة، يجب تمكينها على النظام.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="3ccb4-109">بإمكان المسؤولين استخدام صفحة [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتمكينها إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="3ccb4-110">تم إدراج ميزه احداث التطبيق لمستودع العملية باعتبارها:</span><span class="sxs-lookup"><span data-stu-id="3ccb4-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="3ccb4-111">**الوحدة** - إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="3ccb4-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="3ccb4-112">**اسم الميزة** - احداث التطبيق لمستودع العملية</span><span class="sxs-lookup"><span data-stu-id="3ccb4-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="3ccb4-113">اعداد مهمة دُفعة لمعالجه احداث التطبيق الخاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="3ccb4-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="3ccb4-114">معالجة أحداث تطبيق المستودع</span><span class="sxs-lookup"><span data-stu-id="3ccb4-114">Process warehouse app events</span></span>

<span data-ttu-id="3ccb4-115">قم باعداد وظيفة دُفعة مجدولة لمعالجه احداث التطبيق الخاصة بالمستودع لعمليات إنشاء أمر التحويل وتحديثات البنود.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="3ccb4-116">انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> أحداث تطبيق مستودع العملية**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="3ccb4-117">يتم فتح مربع الحوار احداث التطبيق مستودع العملية.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="3ccb4-118">قم بتوسيع علامة التبويب السريعة **التشغيل في الخلفية**، قم بتعيين **المعالجة الدُفعية‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="3ccb4-119">على علامة التبويب السريعة **التشغيل في الخلفية** حدد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="3ccb4-120">يفتح مربع الحوار **تحديد التكرار**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="3ccb4-121">قم بتعيين جدول التشغيل الملائم لعملك.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="3ccb4-122">حدد **موافق** للرجوع إلى مربع الحوار **احداث تطبيق مستودع العملية**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="3ccb4-123">حدد **موافق** في مربع الحوار **أحداث تطبيق مستودع العملية** لإضافة وظيفة الدُفعة إلى قائمة انتظار الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="3ccb4-124">احداث تطبيق مستودع الاستعلامات</span><span class="sxs-lookup"><span data-stu-id="3ccb4-124">Query warehouse app events</span></span>

<span data-ttu-id="3ccb4-125">يمكنك عرض قائمه انتظار الاحداث ورسائل الاحداث التي تم إنشاؤها بواسطة تطبيق إدارة المستودع للأجهزة المحمولة عن طريق الانتقال إلى **استعلامات أداره المستودعات \> الاستعلامات والتقارير \> سجلات الاجهزه المحمولة \> احداث تطبيق مستودع**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-125">You can view the event queue and events messages generated by the Warehouse Management mobile app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="3ccb4-126">عمليه قائمه انتظار الأحداث القياسية</span><span class="sxs-lookup"><span data-stu-id="3ccb4-126">The standard event queue process</span></span>

<span data-ttu-id="3ccb4-127">وعاده ما يتم استخدام قائمه انتظار احداث تطبيق المستودع مع التدفق الموصوف التالي:</span><span class="sxs-lookup"><span data-stu-id="3ccb4-127">The warehouse app events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="3ccb4-128">تتم أضافه حدث إلى قائمه الانتظار مع رسالة حدث.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="3ccb4-129">ويكون للرسالة الجديدة في البداية حاله حدث **قيد الانتظار**، مما يعني ان الوظيفة الدفعيه **احداث تطبيق مستودع العملية** لن تقوم بالتقاط هذه الرسالة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="3ccb4-130">وبمجرد تحديث حاله الرسالة إلى وضع **الانتظار**، ستقوم وظيفة الدُفعة احداث **تطبيق مستودع العملية** بالتقاط الحدث ومعالجته.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="3ccb4-131">تقوم وظيفة الدُفعة بتحديث حالات الاحداث اما **مكتملة** أو **فاشله**، استنادا إلى ما إذا كانت العملية المطلوبة ممكنة ام لا.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="3ccb4-132">عندما تكون كافة رسائل الاحداث ذات الصلة بالحالة **مكتملة**، يتم حذف الحدث من قائمه الانتظار.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="3ccb4-133">للحصول على مثال تفصيلي، راجع [إنشاء أمر تحويل من عملية تطبيق المستودع](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="3ccb4-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="3ccb4-134">معالجه أخطاء الاحداث</span><span class="sxs-lookup"><span data-stu-id="3ccb4-134">Handle event errors</span></span>

<span data-ttu-id="3ccb4-135">وكجزء من معالجه حدث المستودع، قد لا يتلقى نشاط الرسالة المطلوب عمليات من وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="3ccb4-136">في هذه الحالة ، ستتغير رسالة الحدث إلى **فاشل**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="3ccb4-137">يمكنك استخدام معلومات **سجل الدُفعة** لمعرفه السبب وراء اتخاذ الإجراءات المطلوبة لتصحيح أيه مشكلات.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="3ccb4-138">للحصول على مثال تفصيلي، راجع [إنشاء أمر تحويل من تطبيق المستودع](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="3ccb4-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="3ccb4-139">لأعاده تعيين رسالة حدث فشل لتطبيق المستودع:</span><span class="sxs-lookup"><span data-stu-id="3ccb4-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="3ccb4-140">الانتقال إلى **أداره المستودعات \> الاستعلامات والتقارير \> سجلات الاجهزه المحمولة \> احداث تطبيق المستودع**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="3ccb4-141">في علامة التبويب السريعة **رسائل حدث تطبيق المستودع**، ابحث عن حدث ذي صله يظهر بالحالة **فاشل** وحدده في العمود **حاله الحدث**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="3ccb4-142">حدد **أعاده التعيين** من شريط الادوات **رسائل احداث تطبيق المستودع**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="3ccb4-143">متابعه العمل حتى تتم أعاده تعيين كافة الرسائل ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="3ccb4-144">يمكنك أيضا أزاله رسالة حدث بالحالة **فاشل** باستخدام الخيار **حذف** الموجود في شريط الادوات **رسائل حدث تطبيق المستودع**.</span><span class="sxs-lookup"><span data-stu-id="3ccb4-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]