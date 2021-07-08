---
title: الكمية المنتقاة غير كافية أثناء إنشاء إيصال التعبئة
description: عند إنشاء إيصال تعبئة، يحتوي حمل العمل الصادر على كمية منتقاة لا تتطابق مع كمية العمل المنشأة في بند حمل العمل.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249054"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="851c6-103">الكمية المنتقاة غير كافية أثناء إنشاء إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="851c6-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="851c6-104">رمز الخطأ: SYS54073</span><span class="sxs-lookup"><span data-stu-id="851c6-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="851c6-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="851c6-105">Symptoms</span></span>

<span data-ttu-id="851c6-106">عند إنشاء إيصال تعبئة، يحتوي حمل العمل الصادر على كمية منتقاة لا تتطابق مع كمية العمل المنشأة في بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="851c6-107">عند محاولة إنشاء إيصال التعبئة، يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="851c6-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="851c6-108">نظرًا لانتقاء %1، لا يكفي تحديث %2 عندما يتحتم أن يكون الباقي %3 فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="851c6-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="851c6-109">وبالتالي، لا يمكنك إنشاء إيصال التعبئة لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="851c6-110">السبب</span><span class="sxs-lookup"><span data-stu-id="851c6-110">Cause</span></span>

<span data-ttu-id="851c6-111">لا يمكن إنشاء إيصال التعبئة في حالته الحالية لان إحدي الحالات التالية قد تكون موجودة:</span><span class="sxs-lookup"><span data-stu-id="851c6-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="851c6-112">لم يتم بعد انتقاء العمل ذي الصلة ونقله إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="851c6-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="851c6-113">لا تتطابق كميه العمل المنتقية مع كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="851c6-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="851c6-114">لا تتطابق كمية بند حمل العمل والكمية التي أنشاهأ العمل والكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="851c6-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="851c6-115">الحل</span><span class="sxs-lookup"><span data-stu-id="851c6-115">Resolution</span></span>

<span data-ttu-id="851c6-116">حمل العمل أو الشحنة في حالة فشل فيها إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="851c6-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="851c6-117">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="851c6-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="851c6-118">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="851c6-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="851c6-119">قم بضبط كمية بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="851c6-120">قم بعكس كافة تسجيلات الانتقاء وإعادة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="851c6-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="851c6-121">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة</span><span class="sxs-lookup"><span data-stu-id="851c6-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="851c6-122">استخدم الإجراء التالي لمراجعة بنود حمل العمل الخاصة بك والتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="851c6-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="851c6-123">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="851c6-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="851c6-124">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="851c6-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="851c6-125">في علامة التبويب السريعة **بنود الحمل**، حدد بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="851c6-126">دون ملاحظه قيمة حقل **الكمية التي أنشاهأ العمل**.</span><span class="sxs-lookup"><span data-stu-id="851c6-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="851c6-127">في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="851c6-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="851c6-128">تحقق من اكتمال العمل في موقع الشحن النهائي، وان كميه العمل المنتقية تطابق كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="851c6-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="851c6-129">قم بتكرار هذا الاجراء لكافة بنود التحميل للتاكد من استيفاء كافة المعايير.</span><span class="sxs-lookup"><span data-stu-id="851c6-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="851c6-130">قم بضبط كمية بند حمل العمل</span><span class="sxs-lookup"><span data-stu-id="851c6-130">Adjust the load line quantity</span></span>

<span data-ttu-id="851c6-131">استخدم الإجراء التالي لضبط كمية بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="851c6-132">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="851c6-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="851c6-133">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="851c6-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="851c6-134">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="851c6-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="851c6-135">في علامة التبويب **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يسبب مشكلة.</span><span class="sxs-lookup"><span data-stu-id="851c6-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="851c6-136">حدد **تقليل الكمية المنتقاة** لضبط الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="851c6-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="851c6-137">قم بتعيين الحقل **تقليل بند حمل العمل** لعكس التسويات على بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="851c6-138">قم بعكس كافة تسجيلات الانتقاء وإعادة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="851c6-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="851c6-139">قد تحدث المشكلة لأن شخص ما قد استخدم تسجيل الانتقاء لإغلاق بند حمل عمل بدون عمل.</span><span class="sxs-lookup"><span data-stu-id="851c6-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="851c6-140">في هذه الحالة، يجب عكس تسجيل الانتقاء اليدوي، ويجب إكمال الانتقاء بعد ذلك باستخدام تطبيق Warehouse Management للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="851c6-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="851c6-141">استخدم الإجراء التالي لعكس تسجيل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="851c6-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="851c6-142">انتقل إلى **الحسابات المدينة \> الأوامر‬ \> كافة الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="851c6-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="851c6-143">حدد أمر المبيعات الذي لا يمكنك ترحيل إيصال تعبئة لحمل العمل به.</span><span class="sxs-lookup"><span data-stu-id="851c6-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="851c6-144">في علامة التبويب **بنود أمر المبيعات**، حدد بند أمر المبيعات الذي تم تسجيل الانتقاء له.</span><span class="sxs-lookup"><span data-stu-id="851c6-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="851c6-145">حدد **تحديث البند \> انتقاء** لإلغاء انتقاء الأصناف.</span><span class="sxs-lookup"><span data-stu-id="851c6-145">Select **Update line \> Pick** to unpick the items.</span></span>
