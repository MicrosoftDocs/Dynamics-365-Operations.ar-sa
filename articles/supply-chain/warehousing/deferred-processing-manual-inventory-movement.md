---
title: المعالجة المؤجلة لحركة المخزون اليدوية
description: يصف هذا الموضوع كيفية استخدام المعالجة المؤجلة لحركة المخزون اليدوية في Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54a202b7e6728bc83022851c901d3c5db17510bf
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956529"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a><span data-ttu-id="dc5af-103">المعالجة المؤجلة لحركة المخزون اليدوية</span><span class="sxs-lookup"><span data-stu-id="dc5af-103">Deferred processing of manual inventory movement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc5af-104">يصف هذا الموضوع كيفية استخدام المعالجة المؤجلة لحركة المخزون اليدوية في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc5af-104">This topic describes how to use deferred processing of manual inventory movement in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="dc5af-105">تتيح المعالجة المؤجلة لعمال المستودعات الاستمرار في القيام بأعمال أخرى أثناء معالجة عملية الوضع في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="dc5af-105">Deferred processing lets warehouse workers continue to do other work while a put operation is processed in the background.</span></span> <span data-ttu-id="dc5af-106">تعد المعالجة المؤجلة مفيدة عندما يكون للخادم زيادات عرضية أو غير مخطط لها في وقت المعالجة، وقد يؤثر وقت المعالجة المتزايد على إنتاجية العامل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-106">Deferred processing is useful when the server can have occasional or unplanned increases in processing time, and the increased processing time might affect worker productivity.</span></span> <span data-ttu-id="dc5af-107">تمت الآن إضافة نوع عمل *حركة المخزون* إلى مجموعة أنواع العمل التي تدعمها هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-107">The *Inventory movement* work type has now been added to the set of work types that this feature supports.</span></span>

<span data-ttu-id="dc5af-108">يتم الحصول على المعالجة الخلفية باستخدام [ميزة أحداث التطبيق الخاصة بمستودع العمليات](warehouse-app-events.md).</span><span class="sxs-lookup"><span data-stu-id="dc5af-108">Background processing is achieved by using the [Process warehouse app events feature](warehouse-app-events.md).</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="dc5af-109">تشغيل هذه الميزة في نظامك</span><span class="sxs-lookup"><span data-stu-id="dc5af-109">Turn on this feature for your system</span></span>

<span data-ttu-id="dc5af-110">لجعل هذه الميزة متوفرة، يمكنك تشغيل الميزات التالية في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dc5af-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span> <span data-ttu-id="dc5af-111">يجب ليك تشغيلها بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="dc5af-111">You must turn them on in this order:</span></span>

1. <span data-ttu-id="dc5af-112">حظر العمل على مستوى المؤسسة</span><span class="sxs-lookup"><span data-stu-id="dc5af-112">Organization-wide work blocking</span></span>
1. <span data-ttu-id="dc5af-113">معالجة أحداث تطبيق المستودع</span><span class="sxs-lookup"><span data-stu-id="dc5af-113">Process warehouse app events</span></span>
1. <span data-ttu-id="dc5af-114">عمليات الوضع المؤجلة</span><span class="sxs-lookup"><span data-stu-id="dc5af-114">Deferred put operations</span></span>
1. <span data-ttu-id="dc5af-115">المعالجة المؤجلة لعملية حركة المخزون اليدوية</span><span class="sxs-lookup"><span data-stu-id="dc5af-115">Deferred processing of manual inventory movement operation</span></span>

## <a name="configure-the-work-processing-policies"></a><span data-ttu-id="dc5af-116">تكوين سياسات معالجة العمل</span><span class="sxs-lookup"><span data-stu-id="dc5af-116">Configure the work processing policies</span></span>

<span data-ttu-id="dc5af-117">لاستخدام المعالجة المؤجلة، يجب عليك إعداد واستخدام سياسة معالجة العمل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-117">To use deferred processing, you must set up and use a work processing policy.</span></span> <span data-ttu-id="dc5af-118">بالنسبة لمعالجة الوضع المؤجل، تدعم [المعالجة المؤجلة لميزة عمل المستودعات](deferred-put.md) أنواع العمل التالية: *أمر المبيعات*، و *مشكلة أمر التحويل*، و *التزويد*.</span><span class="sxs-lookup"><span data-stu-id="dc5af-118">For deferred put processing, the [Deferred processing of warehouse work feature](deferred-put.md) supports the following work types: *Sales order*, *Transfer order issue*, and *Replenishment*.</span></span> <span data-ttu-id="dc5af-119">تضيف ميزات *المعالجة المؤجلة لعملية حركة المخزون اليدوية* نوع عمل جديدًا: *حركة المخزون*.</span><span class="sxs-lookup"><span data-stu-id="dc5af-119">The *Deferred processing of manual inventory movement operation* features adds a new work type: *Inventory movement*.</span></span>

<span data-ttu-id="dc5af-120">لإعداد سياسة معالجة العمل، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="dc5af-120">To set up a work processing policy, follow these steps.</span></span>

1. <span data-ttu-id="dc5af-121">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> سياسات معالجة العمل**.</span><span class="sxs-lookup"><span data-stu-id="dc5af-121">Go to **Warehouse management \> Setup \> Work \> Work processing policies**.</span></span>
1. <span data-ttu-id="dc5af-122">حدد سياسة حالية في القائمة، أو أنشئ سياسة جديدة عن طريق تحديد **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="dc5af-122">Either select an existing policy in the list, or create a new policy by selecting **New** on the Action Pane.</span></span> <span data-ttu-id="dc5af-123">يحتوي عنوان كل سياسة على الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="dc5af-123">The header of every policy has the following fields:</span></span>

    - <span data-ttu-id="dc5af-124">**اسم سياسة معالجة العمل** – اسم سياسة معالجة العمل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-124">**Work processing policy name** – The name of the work processing policy.</span></span>
    - <span data-ttu-id="dc5af-125">**الوصف** – وصف لسياسة معالجة العمل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-125">**Description** – A description of the work processing policy.</span></span>

1. <span data-ttu-id="dc5af-126">في علامة التبويب السريع **قواعد المعالجة**، قم بإعداد مجموعة القواعد التي ستطبقها السياسة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-126">On the **Processing rules** FastTab, set up the collection of rules that the policy will apply.</span></span> <span data-ttu-id="dc5af-127">استخدم الأزرار الموجودة على شريط الأدوات لإضافة القواعد أو إزالتها كما تريد.</span><span class="sxs-lookup"><span data-stu-id="dc5af-127">Use the buttons on the toolbar to add or remove rules as you require.</span></span> <span data-ttu-id="dc5af-128">بالنسبة لكل قاعدة، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="dc5af-128">For each rule, set the following fields:</span></span>

    - <span data-ttu-id="dc5af-129">**نوع أمر العمل** – حدد نوع العمل الذي تنطبق عليه السياسة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-129">**Work order type** – Select the work type that the policy applies to.</span></span>
    - <span data-ttu-id="dc5af-130">**العملية** – حدد العملية التي يتم استخدام السياسة لمعالجتها.</span><span class="sxs-lookup"><span data-stu-id="dc5af-130">**Operation** – Select the operation that the policy is used to process.</span></span> <span data-ttu-id="dc5af-131">إذا حددت *حركة المخزون* في حقل **نوع أمر العمل**، لا يتعين عليك تعيين هذا الحقل، لأنه تتم معالجة كل من عمليات الانتقاء وعملية الوضع كحدث واحد.</span><span class="sxs-lookup"><span data-stu-id="dc5af-131">If you selected *Inventory movement* in the **Work order type** field, you don't have to set this field, because both pick operations and put operations are processed as a single event.</span></span>
    - <span data-ttu-id="dc5af-132">**أسلوب معالجة العمل** – حدد الطريقة المستخدمة لمعالجة بند العمل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-132">**Work processing method** – Select the method that is used to process the work line.</span></span> <span data-ttu-id="dc5af-133">إذا حددت *فوري*، فان السلوك يشابه السلوك عند عدم استخدام أي سياسة معالجة عمل لمعالجة البند.</span><span class="sxs-lookup"><span data-stu-id="dc5af-133">If you select *Immediate*, the behavior resembles the behavior when no work processing policies are used to process the line.</span></span> <span data-ttu-id="dc5af-134">إذا حددت *مؤجل*، فسيقوم النظام بتطبيق المعالجة المؤجلة التي تستخدم إطار عمل الدفعة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-134">If you select *Deferred*, the system will apply deferred processing that uses the batch framework.</span></span>
    - <span data-ttu-id="dc5af-135">**عتبة المعالجة المؤجلة‬** – إذا قمت بعيين هذا الحقل إلى *0* (صفر)، لا توجد عتبة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-135">**Deferred processing threshold** – If you set this field to *0* (zero), there is no threshold.</span></span> <span data-ttu-id="dc5af-136">في هذه الحالة، يتم استخدام أسلوب المعالجة *المؤجلة* إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="dc5af-136">In this case, the *Deferred* processing method is used if possible.</span></span> <span data-ttu-id="dc5af-137">إذا كان حساب الحد المعين أقل من الحد، يتم استخدام الأسلوب *الفوري*.</span><span class="sxs-lookup"><span data-stu-id="dc5af-137">If the specific threshold calculation is below the threshold, the *Immediate* method is used.</span></span> <span data-ttu-id="dc5af-138">وبخلاف ذلك، يتم استخدام الأسلوب *المؤجل* إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="dc5af-138">Otherwise, the *Deferred* method is used if possible.</span></span> <span data-ttu-id="dc5af-139">بالنسبة للعمل المرتبط بالمبيعات والنقل، يتم حساب الحد على أنه عدد بنود حمل المصدر المقترنة والتي تتم معالجتها للعمل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-139">For sales and transfer-related work, the threshold is calculated as the number of associated source load lines that are being processed for the work.</span></span> <span data-ttu-id="dc5af-140">بالنسبة لعمل التزويد، يتم حساب الحد كعدد بنود العمل التي يتم تزويدها بواسطة العمل.</span><span class="sxs-lookup"><span data-stu-id="dc5af-140">For replenishment work, the threshold is calculated as the number of work lines that are being replenished by the work.</span></span> <span data-ttu-id="dc5af-141">ومن خلال إعداد الحد، على سبيل المثال، إلى *5* للمبيعات، فإنك تضمن أن الأعمال الصغيرة التي تحتوي على أقل من خمسة بنود تحميل مصدر أولية لن تستخدم المعالجة المؤجلة، ولكن الأعمال الأكبر سوف تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="dc5af-141">By setting a threshold of, for example, *5* for sales, you ensure that smaller works that have fewer than five initial source load lines won't use deferred processing, but larger works will use it.</span></span> <span data-ttu-id="dc5af-142">ويكون للعتبة تأثير فقط في حالة تعيين حقل **طريقة معالجة العمل** إلى *مؤجلة*.</span><span class="sxs-lookup"><span data-stu-id="dc5af-142">The threshold has an effect only if the **Work processing method** field is set to *Deferred*.</span></span>
    - <span data-ttu-id="dc5af-143">**مجموعه دفعات المعالجة المؤجلة** - حدد مجموعة الدُفعات المستخدمة للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-143">**Deferred processing batch group** – Specify the batch group that is used for processing.</span></span> <span data-ttu-id="dc5af-144">إذا حددت *حركة المخزون* في حقل **نوع أمر العمل**، لا يتعين عليك تعيين هذا الحقل، نظرًا لتحديد مجموعة الدفعات في مربع الحوار **معالجة أحداث تطبيق المستودع**.</span><span class="sxs-lookup"><span data-stu-id="dc5af-144">If you selected *Inventory movement* in the **Work order type** field, you don't have to set this field, because the batch group is selected in the **Process warehouse app events** dialog box.</span></span>

## <a name="assign-the-work-creation-policy"></a><span data-ttu-id="dc5af-145">تعيين سياسة إنشاء العمل</span><span class="sxs-lookup"><span data-stu-id="dc5af-145">Assign the work creation policy</span></span>

<span data-ttu-id="dc5af-146">للحصول على تفاصيل حول كيفية تعيين سياسة إنشاء العمل، راجع [المعالجة المؤجلة لأعمال المستودعات](deferred-put.md).</span><span class="sxs-lookup"><span data-stu-id="dc5af-146">For details about how to assign a work creation policy, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="dc5af-147">اعداد مهمة دُفعة لمعالجه احداث التطبيق الخاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="dc5af-147">Set up a batch job to process warehouse app events</span></span>

<span data-ttu-id="dc5af-148">لاستخدام عملية *المعالجة المؤجلة لعملية حركة المخزون اليدوية*، قم بإعداد وظيفة دفعة مجدولة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-148">To use the *Deferred processing of manual inventory movement operation* process, set up a scheduled batch job.</span></span>

1. <span data-ttu-id="dc5af-149">انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> أحداث تطبيق مستودع العملية**.</span><span class="sxs-lookup"><span data-stu-id="dc5af-149">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="dc5af-150">في مربع الحوار **معالجة أحداث تطبيق المستودع**، على علامة التبويب السريعة **تشغيل في الخلفية**، قم بتعيين خيار **معالجة الدفعات** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="dc5af-150">In the **Process warehouse app events** dialog box, on the **Run in background** FastTab, set the **Batch processing** option to *Yes*.</span></span>
1. <span data-ttu-id="dc5af-151">حدد **تكرار**، وقم بإعداد جدول تشغيل يلبي متطلبات عملك.</span><span class="sxs-lookup"><span data-stu-id="dc5af-151">Select **Recurrence**, and set up a run schedule that meets the requirements of your business.</span></span>
1. <span data-ttu-id="dc5af-152">حدد **موافق** في كل مربع حوار.</span><span class="sxs-lookup"><span data-stu-id="dc5af-152">Select **OK** in each dialog box.</span></span>

## <a name="inquire-about-the-warehouse-app-events"></a><span data-ttu-id="dc5af-153">الاستعلام عن أحداث تطبيق المستودع</span><span class="sxs-lookup"><span data-stu-id="dc5af-153">Inquire about the warehouse app events</span></span>

<span data-ttu-id="dc5af-154">يمكنك عرض قائمة انتظار الأحداث ورسائل الأحداث التي ينشئها تطبيق المستودع بالانتقال إلى **إدارة المستودع \> الاستعلامات والتقارير \> سجلات الأجهزة المحمولة \> أحداث تطبيق المستودع**.</span><span class="sxs-lookup"><span data-stu-id="dc5af-154">You can view the event queue and event messages that the warehouse app generates by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

<span data-ttu-id="dc5af-155">ستكون رسائل أحداث *حركة المخزون* بحالة *في قائمة الانتظار* عند إنشائها لأول مرة.</span><span class="sxs-lookup"><span data-stu-id="dc5af-155">The *Inventory movement* event messages will have a status of *Queued* when they are first created.</span></span> <span data-ttu-id="dc5af-156">تشير هذه الحالة إلى أن وظيفة دفعة **معالحة أحداث تطبيق المستودع** ستلتقط رسائل الأحداث وستعالجها.</span><span class="sxs-lookup"><span data-stu-id="dc5af-156">This status indicates that the **Process warehouse app events** batch job will pick up the event messages and process them.</span></span> <span data-ttu-id="dc5af-157">عند تحديث الحالة إلى *مكتمل*، يتم حذف جميع الأحداث ذات الصلة من قائمة الانتظار.</span><span class="sxs-lookup"><span data-stu-id="dc5af-157">When the status is updated to *Completed*, all the related events are deleted from the queue.</span></span>

<span data-ttu-id="dc5af-158">يتم تكديس جميع أحداث *حركة المخزون* ضمن مجموعة واحدة لكل نوع حدث ومستودع.</span><span class="sxs-lookup"><span data-stu-id="dc5af-158">All the *Inventory movement* events are accumulated under one collection per event type and warehouse.</span></span>

<span data-ttu-id="dc5af-159">ستعمل وظيفة الدُفعة على معالجة أحداث تطبيق المستودع وفقًا للتكرار الذي تم إعداده في مربع الحوار **معالجة أحداث تطبيق المستودع**.</span><span class="sxs-lookup"><span data-stu-id="dc5af-159">The batch job will process the warehouse app events according to the recurrence that is set up in the **Process warehouse app events** dialog box.</span></span> <span data-ttu-id="dc5af-160">لذلك، حتى تتم معالجة الرسالة، يمكنك العثور على معرف المستودع من خلال البحث في حقل **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="dc5af-160">Therefore, until a message is processed, you can find the warehouse ID by looking in the **Identifier** field.</span></span>

<span data-ttu-id="dc5af-161">تحتوي تفاصيل الرسالة على تفاصيل الحركة (على سبيل المثال، مواقع "من" و "إلى").</span><span class="sxs-lookup"><span data-stu-id="dc5af-161">The details of the message contain the details of the movement (for example, the "from" and "to" locations).</span></span>

<span data-ttu-id="dc5af-162">لمزيد من المعلومات، راجع [معالجه حدث تطبيق المستودع](warehouse-app-events.md).</span><span class="sxs-lookup"><span data-stu-id="dc5af-162">For more information, see [Warehouse app event processing](warehouse-app-events.md).</span></span>

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a><span data-ttu-id="dc5af-163">تكوين قائمة الجهاز المحمول لتخطي سياسة المعالجة المؤجلة</span><span class="sxs-lookup"><span data-stu-id="dc5af-163">Configure the mobile device menu to skip the deferred processing policy</span></span>

<span data-ttu-id="dc5af-164">للحصول على تفاصيل حول كيفية تكوين قائمة الجهاز المحمول لتخطي سياسة المعالجة المؤجلة، راجع [المعالجة المؤجلة لعمل المستودع](deferred-put.md).</span><span class="sxs-lookup"><span data-stu-id="dc5af-164">For details about how to configure the mobile device menu to skip the deferred processing policy, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="impact-on-closed-work-dates"></a><span data-ttu-id="dc5af-165">التأثير على تواريخ الأعمال المقفلة</span><span class="sxs-lookup"><span data-stu-id="dc5af-165">Impact on closed work dates</span></span>

<span data-ttu-id="dc5af-166">للحصول على تفاصيل حول التأثير على تواريخ العمل المغلقة، راجع [المعالجة المؤجلة لعمل المستودع](deferred-put.md).</span><span class="sxs-lookup"><span data-stu-id="dc5af-166">For details about the impact on closed work dates, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc5af-167">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dc5af-167">Additional resources</span></span>

- [<span data-ttu-id="dc5af-168">المعالجة المؤجلة لعمل المستودع</span><span class="sxs-lookup"><span data-stu-id="dc5af-168">Deferred processing of warehouse work</span></span>](deferred-put.md)
- [<span data-ttu-id="dc5af-169">معالجه حدث تطبيق المستودع</span><span class="sxs-lookup"><span data-stu-id="dc5af-169">Warehouse app event processing</span></span>](warehouse-app-events.md)
- [<span data-ttu-id="dc5af-170">إعداد الأجهزة المحمولة لعمل المستودع</span><span class="sxs-lookup"><span data-stu-id="dc5af-170">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
