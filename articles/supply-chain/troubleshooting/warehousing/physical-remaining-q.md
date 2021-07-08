---
title: يجب ألا تكون الكمية الفعلية المتبقية في الوحدة صفرًا
description: عند إنشاء إيصال تعبئة، تحتوي البيانات التي يتم توفيرها له على كمية مخزون غير صفرية ولكن كمية مبيعات صفرية.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248764"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="640de-103">يجب ألا تكون الكمية الفعلية المتبقية في الوحدة صفرًا</span><span class="sxs-lookup"><span data-stu-id="640de-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="640de-104">رمز الخطأ: SYS19591</span><span class="sxs-lookup"><span data-stu-id="640de-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="640de-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="640de-105">Symptoms</span></span>

<span data-ttu-id="640de-106">عند إنشاء إيصال تعبئة، تحتوي البيانات التي يتم توفيرها له على كمية مخزون غير صفرية ولكن كمية مبيعات صفرية.</span><span class="sxs-lookup"><span data-stu-id="640de-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="640de-107">عند محاولة إنشاء إيصال التعبئة، يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="640de-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="640de-108">يجب أن تكون الكمية الفعلية المتبقية في الوحدة %1 شيئًا غير الصفر.</span><span class="sxs-lookup"><span data-stu-id="640de-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="640de-109">وبالتالي، لا يمكنك إنشاء إيصال التعبئة لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="640de-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="640de-110">السبب</span><span class="sxs-lookup"><span data-stu-id="640de-110">Cause</span></span>

<span data-ttu-id="640de-111">يقوم النظام بتقييم الكمية الفعلية المتبقية في وحدة المخزون والكمية الفعلية المتبقية في وحدة الشحن.</span><span class="sxs-lookup"><span data-stu-id="640de-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="640de-112">إذا وجد النظام أن الكمية الفعلية المتبقية في وحدة الشحن هي 0 (صفر)، ولكن الكمية الفعلية المتبقية في وحدة المخزون ليست 0، فلا يمكنك إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="640de-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="640de-113">على سبيل المثال، قد تحدث هذه المشكلة إذا كانت وحدة المبيعات ووحدة المخزون للصنف مختلفة، ولم يكن التحويل بين الوحدات دقيقًا.</span><span class="sxs-lookup"><span data-stu-id="640de-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="640de-114">الحل</span><span class="sxs-lookup"><span data-stu-id="640de-114">Resolution</span></span>

<span data-ttu-id="640de-115">حمل العمل أو الشحنة في حالة فشل فيها إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="640de-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="640de-116">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="640de-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="640de-117">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="640de-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="640de-118">راجع بنود حمل العمل، وقم بالتسويات للتأكد من أنه يمكن تحويل الكمية بشكل واضح دون أية مشكلات في التقريب.</span><span class="sxs-lookup"><span data-stu-id="640de-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="640de-119">راجع بنود حمل العمل، وقم بالتسويات للتأكد من محاذاة الوحدة والكمية مع الدقة العشرية للوحدة.</span><span class="sxs-lookup"><span data-stu-id="640de-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="640de-120">تأكد من أن وحدة قياس المخزون أصغر من وحدة قياس المبيعات.</span><span class="sxs-lookup"><span data-stu-id="640de-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="640de-121">راجع بنود حمل العمل الخاصة بك وتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة</span><span class="sxs-lookup"><span data-stu-id="640de-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="640de-122">استخدم الإجراء التالي لمراجعة بنود حمل العمل الخاصة بك والتأكد من اكتمال كافة الأعمال ذات الصلة في موقع الشحن النهائي، وأن الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="640de-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="640de-123">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="640de-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="640de-124">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="640de-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="640de-125">في علامة التبويب السريعة **بنود الحمل**، حدد بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="640de-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="640de-126">دون ملاحظه قيمة حقل **الكمية التي أنشاهأ العمل**.</span><span class="sxs-lookup"><span data-stu-id="640de-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="640de-127">في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="640de-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="640de-128">تحقق من اكتمال العمل في موقع الشحن النهائي، وان كميه العمل المنتقية تطابق كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="640de-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="640de-129">قم بتكرار هذا الاجراء لكافة بنود التحميل للتاكد من استيفاء كافة المعايير.</span><span class="sxs-lookup"><span data-stu-id="640de-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="640de-130">راجع بنود حمل العمل، وقم بالتسويات للتأكد من أنه يمكن تحويل الكمية بشكل واضح دون أية مشكلات في التقريب</span><span class="sxs-lookup"><span data-stu-id="640de-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="640de-131">قم بالإجراء التالي لمراجعة بنود الحمل والقيام بالتسويات للتأكد من أنه يمكن تحويل الكمية بشكل واضح دون مشكلات في التقريب.</span><span class="sxs-lookup"><span data-stu-id="640de-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="640de-132">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="640de-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="640de-133">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="640de-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="640de-134">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="640de-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="640de-135">في علامة التبويب **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يتجاوز التسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="640de-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="640de-136">حدد **تقليل الكمية المنتقاة** لضبط الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="640de-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="640de-137">في علامة التبويب  **تفاصيل البنود**، حدد **أمر**.</span><span class="sxs-lookup"><span data-stu-id="640de-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="640de-138">قم بتعيين الحقل **الكمية** إلى الكمية المنتقاة (أي، قيمة الحقل **الكمية التي أنشاهأ العمل**)، بحيث يمكن متابعة إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="640de-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="640de-139">راجع بنود حمل العمل، وقم بالتسويات للتأكد من محاذاة الوحدة والكمية مع الدقة العشرية للوحدة</span><span class="sxs-lookup"><span data-stu-id="640de-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="640de-140">استخدم الإجراء التالي لمراجعة بنود حمل العمل، وقم بالتسويات للتأكد من محاذاة الوحدة والكمية مع الدقة العشرية للوحدة.</span><span class="sxs-lookup"><span data-stu-id="640de-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="640de-141">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="640de-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="640de-142">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="640de-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="640de-143">في علامة التبويب السريعة **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يسبب مشكلة.</span><span class="sxs-lookup"><span data-stu-id="640de-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="640de-144">دون ملاحظه قيمة الحقلين **الكمية** و **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="640de-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="640de-145">انتقل إلى **إدارة المؤسسة \> الوحدات \> الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="640de-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="640de-146">حدد الوحدة الذي لا يمكن إنشاء إيصال التعبئة لها.</span><span class="sxs-lookup"><span data-stu-id="640de-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="640de-147">اضبط قيمة الحقل **الدقة العشرية** كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="640de-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="640de-148">تأكد من أن وحدة قياس المخزون أصغر من وحدة قياس المبيعات</span><span class="sxs-lookup"><span data-stu-id="640de-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="640de-149">تأكد من أن وحدة قياس المخزون أصغر من وحدة قياس المبيعات.</span><span class="sxs-lookup"><span data-stu-id="640de-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="640de-150">ضع في اعتبارك إعادة تكوين وحدة القياس للصنف كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="640de-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
