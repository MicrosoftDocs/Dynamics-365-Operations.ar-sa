---
title: تقريب عشري لكمية التحديث الفعلي غير صحيح
description: عند إنشاء إيصال تعبئة، يحتوي حمل العمل الصادر على كمية لا تتطابق مع الدقة العشرية المحددة في الوحدة.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248765"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="174d4-103">تقريب عشري لكمية التحديث الفعلي غير صحيح</span><span class="sxs-lookup"><span data-stu-id="174d4-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="174d4-104">رمز الخطأ: SYS19589</span><span class="sxs-lookup"><span data-stu-id="174d4-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="174d4-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="174d4-105">Symptoms</span></span>

<span data-ttu-id="174d4-106">عند إنشاء إيصال تعبئة، يحتوي حمل العمل الصادر على كمية لا تتطابق مع الدقة العشرية المحددة في الوحدة.</span><span class="sxs-lookup"><span data-stu-id="174d4-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="174d4-107">عند محاولة إنشاء إيصال التعبئة، يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="174d4-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="174d4-108">التقريب العشري لكمية التحديث الفعلية في الوحدة %1 غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="174d4-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="174d4-109">وبالتالي، لا يمكنك إنشاء إيصال التعبئة لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="174d4-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="174d4-110">السبب</span><span class="sxs-lookup"><span data-stu-id="174d4-110">Cause</span></span>

<span data-ttu-id="174d4-111">يقوم النظام بتقييم ما إذا كان التقريب العشري لكمية الشحن يتوافق مع الدقة العشرية التي يتم تعريفها لوحدة الشحن.</span><span class="sxs-lookup"><span data-stu-id="174d4-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="174d4-112">عندما يقوم النظام بتقريب كمية الشحن إلى العدد المحدد من المنازل العشرية، إذا وجد أن كمية الشحن التقريبية لا تتطابق مع كمية الشحن الفعلية، فلا يمكنك إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="174d4-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="174d4-113">على سبيل المثال، قد تحدث هذه المشكلة إذا كانت كمية المبيعات 1.75 كجم (كجم)، ولكن يتم تعيين الدقة العشرية إلى *1*.</span><span class="sxs-lookup"><span data-stu-id="174d4-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="174d4-114">الحل</span><span class="sxs-lookup"><span data-stu-id="174d4-114">Resolution</span></span>

<span data-ttu-id="174d4-115">حمل العمل أو الشحنة في حالة فشل فيها إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="174d4-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="174d4-116">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="174d4-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="174d4-117">راجع بنود حمل العمل، وقم بالتسويات للتأكد من أنه يمكن تحويل الكمية بشكل واضح دون أرقام عشرية وأية مشكلات أخرى في التقريب.</span><span class="sxs-lookup"><span data-stu-id="174d4-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="174d4-118">راجع بنود حمل العمل، وقم بالتسويات للتأكد من محاذاة الوحدة والكمية مع الدقة العشرية للوحدة.</span><span class="sxs-lookup"><span data-stu-id="174d4-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="174d4-119">راجع بنود حمل العمل، وقم بالتسويات للتأكد من أنه يمكن تحويل الكمية بشكل واضح دون أرقام عشرية وأية مشكلات أخرى في التقريب</span><span class="sxs-lookup"><span data-stu-id="174d4-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="174d4-120">قم بالإجراء التالي لمراجعة بنود الحمل والقيام بالتسويات للتأكد من أنه يمكن تحويل الكمية بشكل واضح دون أرقام عشرية وأية مشكلات أخرى في التقريب.</span><span class="sxs-lookup"><span data-stu-id="174d4-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="174d4-121">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="174d4-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="174d4-122">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="174d4-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="174d4-123">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="174d4-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="174d4-124">في علامة التبويب **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يسبب مشكلة.</span><span class="sxs-lookup"><span data-stu-id="174d4-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="174d4-125">حدد **تقليل الكمية المنتقاة** لضبط الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="174d4-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="174d4-126">في علامة التبويب  **تفاصيل البنود**، حدد **أمر**.</span><span class="sxs-lookup"><span data-stu-id="174d4-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="174d4-127">قم بتعيين الحقل **الكمية** إلى الكمية المنتقاة (أي، قيمة الحقل **الكمية التي أنشاهأ العمل**)، بحيث يمكن متابعة إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="174d4-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="174d4-128">راجع بنود حمل العمل، وقم بالتسويات للتأكد من محاذاة الوحدة والكمية مع الدقة العشرية للوحدة</span><span class="sxs-lookup"><span data-stu-id="174d4-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="174d4-129">استخدم الإجراء التالي لمراجعة بنود حمل العمل، وقم بالتسويات للتأكد من محاذاة الوحدة والكمية مع الدقة العشرية للوحدة.</span><span class="sxs-lookup"><span data-stu-id="174d4-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="174d4-130">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="174d4-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="174d4-131">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="174d4-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="174d4-132">في علامة التبويب السريعة **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يسبب مشكلة.</span><span class="sxs-lookup"><span data-stu-id="174d4-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="174d4-133">دون ملاحظه قيمة الحقلين **الكمية** و **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="174d4-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="174d4-134">انتقل إلى **إدارة المؤسسة \> الوحدات \> الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="174d4-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="174d4-135">حدد الوحدة الذي لا يمكن إنشاء إيصال التعبئة لها.</span><span class="sxs-lookup"><span data-stu-id="174d4-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="174d4-136">اضبط قيمة الحقل **الدقة العشرية** كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="174d4-136">Adjust the value of the **Decimal precision** field as required.</span></span>
