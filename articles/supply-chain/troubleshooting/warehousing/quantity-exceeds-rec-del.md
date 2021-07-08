---
title: الكمية التي تحاول تحديثها تتجاوز الكمية المستلمة/التي تم تسليمها.
description: عند إنشاء إيصال تعبئة، يحتوي حمل العمل الصادر على كمية منتقاة لا تتطابق مع كمية العمل المنتقاة والمحفوظة أمر المبيعات.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249055"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="eabbe-103">الكمية التي تحاول تحديثها تتجاوز الكمية المستلمة/التي تم تسليمها</span><span class="sxs-lookup"><span data-stu-id="eabbe-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="eabbe-104">رمز الخطأ: SYS7676</span><span class="sxs-lookup"><span data-stu-id="eabbe-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="eabbe-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="eabbe-105">Symptoms</span></span>

<span data-ttu-id="eabbe-106">عند إنشاء إيصال تعبئة، يحتوي حمل العمل الصادر على كمية منتقاة لا تتطابق مع كمية العمل المنتقاة والمحفوظة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="eabbe-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="eabbe-107">عند محاولة إنشاء إيصال التعبئة، يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="eabbe-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="eabbe-108">يجب أن تتجاوز الكمية التي تحاول تحديثها الكمية المستلمة/المسلّمة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="eabbe-109">وبالتالي، لا يمكنك إنشاء إيصال التعبئة لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="eabbe-110">السبب</span><span class="sxs-lookup"><span data-stu-id="eabbe-110">Cause</span></span>

<span data-ttu-id="eabbe-111">لا تتطابق كميه العمل المنتقية مع كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="eabbe-112">على سبيل المثال، قد تحدث هذه المشكلة إذا كانت كمية بند حمل العمل أو كمية العمل التي تم إنشائها أو الكمية المنتقاة غير دقيقة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="eabbe-113">الحل</span><span class="sxs-lookup"><span data-stu-id="eabbe-113">Resolution</span></span>

<span data-ttu-id="eabbe-114">حمل العمل أو الشحنة في حالة فشل فيها إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="eabbe-115">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="eabbe-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="eabbe-116">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="eabbe-117">قم بضبط كمية بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="eabbe-118">قم بعكس كافة تسجيلات الانتقاء وإعادة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="eabbe-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="eabbe-119">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة</span><span class="sxs-lookup"><span data-stu-id="eabbe-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="eabbe-120">استخدم الإجراء التالي لمراجعة بنود حمل العمل الخاصة بك والتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="eabbe-121">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="eabbe-122">حدد حمل العمل الذي لا يمكن إنشاء الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="eabbe-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="eabbe-123">في علامة التبويب السريعة **بنود الحمل**، حدد بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="eabbe-124">دون ملاحظه قيمة حقل **الكمية التي أنشاهأ العمل**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="eabbe-125">في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="eabbe-126">تحقق من اكتمال العمل في موقع الشحن النهائي، وان كميه العمل المنتقية تطابق كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="eabbe-127">قم بتكرار هذا الاجراء لكافة بنود التحميل للتاكد من استيفاء كافة المعايير.</span><span class="sxs-lookup"><span data-stu-id="eabbe-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="eabbe-128">قم بضبط كمية بند حمل العمل</span><span class="sxs-lookup"><span data-stu-id="eabbe-128">Adjust the load line quantity</span></span>

<span data-ttu-id="eabbe-129">استخدم الإجراء التالي لضبط كمية بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="eabbe-130">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="eabbe-131">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="eabbe-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="eabbe-132">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="eabbe-133">في علامة التبويب **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يسبب مشكلة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="eabbe-134">حدد **تقليل الكمية المنتقاة** لضبط الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="eabbe-135">قم بتعيين الحقل **تقليل بند حمل العمل** لعكس التسويات على بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="eabbe-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="eabbe-136">قم بعكس كافة تسجيلات الانتقاء وإعادة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="eabbe-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="eabbe-137">في حالة استخدام شخص ما تسجيل الانتقاء لإغلاق بند حمل العمل دون عمل، يمكن أن يحدث اختلاف بين كمية بند حمل العمل والكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="eabbe-138">في هذه الحالة، يجب عكس تسجيل الانتقاء اليدوي، ويجب إكمال الانتقاء بعد ذلك باستخدام تطبيق Warehouse Management للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="eabbe-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="eabbe-139">استخدم الإجراء التالي لعكس تسجيل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="eabbe-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="eabbe-140">انتقل إلى **الحسابات المدينة \> الأوامر‬ \> كافة الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="eabbe-141">حدد أمر المبيعات الذي لا يمكنك ترحيل إيصال تعبئة لحمل العمل به.</span><span class="sxs-lookup"><span data-stu-id="eabbe-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="eabbe-142">في علامة التبويب **بنود أمر المبيعات**، حدد بند أمر المبيعات الذي تم تسجيل الانتقاء له.</span><span class="sxs-lookup"><span data-stu-id="eabbe-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="eabbe-143">حدد **تحديث البند \> انتقاء** لإلغاء انتقاء الأصناف.</span><span class="sxs-lookup"><span data-stu-id="eabbe-143">Select **Update line \> Pick** to unpick the items.</span></span>
