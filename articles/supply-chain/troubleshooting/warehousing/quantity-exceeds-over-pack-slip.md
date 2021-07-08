---
title: الكمية تتجاوز النسبة المئوية للتسليم الزائد أثناء إنشاء إيصال التعبئة
description: عند إنشاء إيصال التعبئة، يحتوي حمل العمل الصادر على كمية تتجاوز النسبة المئوية للتسليم الزائد.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249052"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="5f5a7-103">الكمية تتجاوز النسبة المئوية للتسليم الزائد أثناء إنشاء إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="5f5a7-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="5f5a7-104">رمز الخطأ: SYS24920</span><span class="sxs-lookup"><span data-stu-id="5f5a7-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="5f5a7-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="5f5a7-105">Symptoms</span></span>

<span data-ttu-id="5f5a7-106">عند إنشاء إيصال التعبئة، يحتوي حمل العمل الصادر على كمية تتجاوز النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="5f5a7-107">عند محاولة إنشاء إيصال التعبئة، يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="5f5a7-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="5f5a7-108">تبلغ نسبة التسليم الأعلى للبند %1 بالمائة، بينما تبلغ نسبة التسليم الأعلى المسموح بها %2 بالمائة فقط.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="5f5a7-109">وبالتالي، لا يمكنك إنشاء إيصال التعبئة لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="5f5a7-110">السبب</span><span class="sxs-lookup"><span data-stu-id="5f5a7-110">Cause</span></span>

<span data-ttu-id="5f5a7-111">الكمية المنتقاة لحمل العمل أو الشحنة أكثر من الكمية المطلوبة وليست ضمن نطاق النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="5f5a7-112">الحل</span><span class="sxs-lookup"><span data-stu-id="5f5a7-112">Resolution</span></span>

<span data-ttu-id="5f5a7-113">حمل العمل أو الشحنة في حالة فشل فيها إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="5f5a7-114">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="5f5a7-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="5f5a7-115">قم بضبط كمية بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="5f5a7-116">قم بتسوية النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="5f5a7-117">عكس وإجراء تسويات.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="5f5a7-118">قم بضبط كمية بند حمل العمل</span><span class="sxs-lookup"><span data-stu-id="5f5a7-118">Adjust the load line quantity</span></span>

<span data-ttu-id="5f5a7-119">استخدم الإجراء التالي لضبط كمية بند حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="5f5a7-120">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5f5a7-121">حدد حمل العمل الذي لا يمكن إنشاء إيصال التعبئة له.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="5f5a7-122">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="5f5a7-123">في علامة التبويب **بنود حمل العمل**، حدد بند حمل العمل للصنف الذي يتجاوز النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="5f5a7-124">حدد **تقليل الكمية المنتقاة** لضبط الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="5f5a7-125">في علامة التبويب  **تفاصيل البنود**، حدد **أمر**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="5f5a7-126">قم بتعيين الحقل **الكمية** إلى الكمية المنتقاة (أي، قيمة الحقل **الكمية التي أنشاهأ العمل**)، بحيث يمكن متابعة إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="5f5a7-127">قم بتسوية النسبة المئوية للتسليم الزائد</span><span class="sxs-lookup"><span data-stu-id="5f5a7-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="5f5a7-128">استخدم الإجراء التالي لضبط النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="5f5a7-129">انتقل إلى **الحسابات المدينة \> الأوامر‬ \> كافة الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="5f5a7-130">حدد أمر المبيعات الذي لا يمكنك ترحيل إيصال تعبئة لحمل العمل به.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="5f5a7-131">في علامة التبويب **بنود أمر المبيعات**، حدد بند أوامر المبيعات للصنف الذي يتجاوز النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="5f5a7-132">في علامة التبويب  **تفاصيل البنود**، حدد **تسليم**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="5f5a7-133">قم بتعيين الحقل **التسليم الزائد** إلى نسبة مئوية أكبر تستوعب الكمية التي تم انتقاؤها مقابل كمية حمل العمل، بحيث يمكن متابعة إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="5f5a7-134">عكس وإجراء تسويات</span><span class="sxs-lookup"><span data-stu-id="5f5a7-134">Reverse and make adjustments</span></span>

<span data-ttu-id="5f5a7-135">اعكس كل شيء تم ترحيل حمل العمل (على سبيل المثال، إيصال التعبئة وتأكيد الشحن والعمل)، وإجراء تسويات أمر المبيعات، وإصدار الأمر إلى المستودع مرة أخرى، وإكمال إجراء الشحن.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="5f5a7-136">استخدم الإجراء التالي لإلغاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="5f5a7-137">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5f5a7-138">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة **عكس**، حدد **إلغاء إيصالات التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="5f5a7-139">استخدم الإجراء التالي لعكس تأكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="5f5a7-140">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5f5a7-141">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="5f5a7-142">استخدم الإجراء التالي لعكس العمل.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="5f5a7-143">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5f5a7-144">في جزء الإجراءات، ضمن علامة التبويب **أحمال العمل**، في المجموعة **العمل**، حدد **عكس العمل**.</span><span class="sxs-lookup"><span data-stu-id="5f5a7-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
