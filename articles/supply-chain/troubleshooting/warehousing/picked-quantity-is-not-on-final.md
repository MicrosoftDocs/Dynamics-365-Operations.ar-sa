---
title: لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف
description: لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301295"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="1da0a-103">لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف</span><span class="sxs-lookup"><span data-stu-id="1da0a-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="1da0a-104">رمز الخطأ: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="1da0a-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="1da0a-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="1da0a-105">Symptoms</span></span>

<span data-ttu-id="1da0a-106">عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="1da0a-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="1da0a-107">لم يتم انتقاء بعض الأصناف اللازمة لحمل العمل %1 ولا نقلها إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="1da0a-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="1da0a-108">وبالتالي، لا يمكنك تاكيد الشحن للتحميل.</span><span class="sxs-lookup"><span data-stu-id="1da0a-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="1da0a-109">السبب</span><span class="sxs-lookup"><span data-stu-id="1da0a-109">Cause</span></span>

<span data-ttu-id="1da0a-110">لا يمكن تاكيد التحميل أو الشحن في حالته الحالية لان أحدي الحالات التالية قد تكون موجودة:</span><span class="sxs-lookup"><span data-stu-id="1da0a-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="1da0a-111">لم يتم بعد انتقاء العمل ذي الصلة ونقله إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="1da0a-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="1da0a-112">لا تتطابق كميه العمل المنتقية مع كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="1da0a-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="1da0a-113">تم تكوين توجيه الموقع بموقع تعبئة كموقع شحن نهائي أثناء استخدام التعبئة في حاويات قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="1da0a-114">الحل</span><span class="sxs-lookup"><span data-stu-id="1da0a-114">Resolution</span></span>

<span data-ttu-id="1da0a-115">الحمولة أو الشحنة في حالة فشل فيها تأكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="1da0a-116">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="1da0a-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="1da0a-117">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="1da0a-118">قم بإلغاء معرفات العمل التي تم إنشاؤها باستخدام موقع التعبئة كموقع الشحن النهائي، وأعد تكوين توجيه الموقع، ثم قم بإصدار حمل العمل مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="1da0a-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="1da0a-119">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة</span><span class="sxs-lookup"><span data-stu-id="1da0a-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="1da0a-120">استخدم الإجراء التالي لمراجعة بنود حمل العمل الخاصة بك والتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="1da0a-121">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1da0a-122">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="1da0a-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="1da0a-123">في علامة التبويب السريعة **بنود الحمل**، حدد بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="1da0a-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="1da0a-124">دون ملاحظه قيمة حقل **الكمية التي أنشاهأ العمل**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="1da0a-125">في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="1da0a-126">تحقق من اكتمال العمل في موقع الشحن النهائي، وان كميه العمل المنتقية تطابق كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="1da0a-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="1da0a-127">قم بتكرار هذا الاجراء لكافة بنود التحميل للتاكد من استيفاء كافة المعايير.</span><span class="sxs-lookup"><span data-stu-id="1da0a-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="1da0a-128">قم بإلغاء معرفات العمل التي تم إنشاؤها باستخدام موقع التعبئة كموقع الشحن النهائي، وأعد تكوين توجيه الموقع، ثم قم إصدار حمل العمل مرة أخرى</span><span class="sxs-lookup"><span data-stu-id="1da0a-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="1da0a-129">استخدم الإجراء التالي لإلغاء معرفات العمل التي لها موقع التعبئة كموقع الوضع النهائي مع وضع التعبئة التلقائية في حاويات في مكانها.</span><span class="sxs-lookup"><span data-stu-id="1da0a-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="1da0a-130">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="1da0a-131">يفتح مربع حوار **إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="1da0a-132">في حقل **معرف العمل**، حدد معرف العمل الذي ترغب في إلغائه.</span><span class="sxs-lookup"><span data-stu-id="1da0a-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="1da0a-133">يجب أن يحتوى معرف العمل المحدد على قيمة **حالة العمل** وهي *مفتوح* أو *قيد التقدم* أو *ملغي*  أو *مجمع* أو *مغلق*.</span><span class="sxs-lookup"><span data-stu-id="1da0a-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="1da0a-134">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-134">Select **OK**.</span></span>
1. <span data-ttu-id="1da0a-135">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="1da0a-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="1da0a-136">كرر هذا الإجراء لمعرفات العمل الأخرى حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="1da0a-137">لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="1da0a-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="1da0a-138">استخدم الإجراء التالي لإعادة تكوين توجيه الموقع بحيث لا يستخدم موقع التعبئة كموقع الشحن النهائي عند إعداد التعبئة التلقائية في حاويات لقالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="1da0a-139">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1da0a-140">في الحقل **نوع أمر العمل**، حدد *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="1da0a-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="1da0a-141">حدد توجيه الموقع الذي تستخدمه للتعبئة التلقائية في حاويات.</span><span class="sxs-lookup"><span data-stu-id="1da0a-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="1da0a-142">في شريط أدوات علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="1da0a-143">في مربع الحوار محرر Power Query، في علامة التبويب **النطاق**، ابحث عن الصف حيث يتم تعيين **الحقل** إلى *ملف تعريف الموقع*، وتأكد من عدم تعيين الحقل **معايير** لذلك الصف إلى ملف تعريف الموقع الذي يحتوي على **نوع موقع** *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="1da0a-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="1da0a-144">قم بتعديل الحقل **المعايير** لتصحيح موقع الوضع النهائي.</span><span class="sxs-lookup"><span data-stu-id="1da0a-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="1da0a-145">استخدم الإجراء التالي لإصدار حمل العمل مرة أخرى وإنشاء معرفات العمل باستخدام موقع الشحن النهائي الصحيح.</span><span class="sxs-lookup"><span data-stu-id="1da0a-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="1da0a-146">انتقل إلى **إدارة المستودعات \> الأحمال \> منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="1da0a-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="1da0a-147">في القسم **أحمال العمل**، ابحث عن التحميل المطلوب إصداره.</span><span class="sxs-lookup"><span data-stu-id="1da0a-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="1da0a-148">في شريط أدوات القسم **أحمال العمل**، حدد **إصدار \> إصدار إلى المستودع** لإصدار حمل العمل المحدد إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="1da0a-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="1da0a-149">كرر هذا الإجراء لأحمال العمل الأخرى حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="1da0a-149">Repeat this procedure for the other loads as needed.</span></span>
