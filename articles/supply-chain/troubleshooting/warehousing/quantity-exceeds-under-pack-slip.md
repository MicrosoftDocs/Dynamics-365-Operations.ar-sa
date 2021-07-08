---
title: الكمية تتجاوز النسبة المئوية للتسليم الناقص أثناء إنشاء إيصال التعبئة
description: عند إنشاء إيصال التعبئة، يحتوي حمل العمل الصادر على كمية تتجاوز النسبة المئوية للتسليم الناقص.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249050"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="6f55c-103">الكمية تتجاوز النسبة المئوية للتسليم الناقص أثناء إنشاء إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f55c-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="6f55c-104">رمز الخطأ: SYS24921</span><span class="sxs-lookup"><span data-stu-id="6f55c-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="6f55c-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="6f55c-105">Symptoms</span></span>

<span data-ttu-id="6f55c-106">عند إنشاء إيصال التعبئة، يحتوي حمل العمل الصادر على كمية تتجاوز النسبة المئوية للتسليم الناقص.</span><span class="sxs-lookup"><span data-stu-id="6f55c-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="6f55c-107">عند محاولة إنشاء إيصال التعبئة، يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="6f55c-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="6f55c-108">تبلغ نسبة التسليم بالأقل للبند %1 بالمائة، بينما تبلغ نسبة التسليم بالأقل المسموح بها %2 بالمائة فقط.</span><span class="sxs-lookup"><span data-stu-id="6f55c-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="6f55c-109">وبالتالي، لا يمكنك إنشاء إيصال التعبئة لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="6f55c-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="6f55c-110">السبب</span><span class="sxs-lookup"><span data-stu-id="6f55c-110">Cause</span></span>

<span data-ttu-id="6f55c-111">الكمية المنتقاة لحمل العمل أو الشحنة أقل من الكمية المطلوبة وليست ضمن نطاق النسبة المئوية للتسليم الناقص.</span><span class="sxs-lookup"><span data-stu-id="6f55c-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="6f55c-112">الحل</span><span class="sxs-lookup"><span data-stu-id="6f55c-112">Resolution</span></span>

<span data-ttu-id="6f55c-113">حمل العمل أو الشحنة في حالة فشل فيها إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="6f55c-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="6f55c-114">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="6f55c-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="6f55c-115">قم بتسوية النسبة المئوية للتسليم الناقص.</span><span class="sxs-lookup"><span data-stu-id="6f55c-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="6f55c-116">عكس وإجراء تسويات.</span><span class="sxs-lookup"><span data-stu-id="6f55c-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="6f55c-117">قم بتسوية النسبة المئوية للتسليم الناقص</span><span class="sxs-lookup"><span data-stu-id="6f55c-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="6f55c-118">استخدم الإجراء التالي لضبط النسبة المئوية للتسليم الناقص.</span><span class="sxs-lookup"><span data-stu-id="6f55c-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="6f55c-119">انتقل إلى **الحسابات المدينة \> الأوامر‬ \> كافة الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="6f55c-120">حدد أمر المبيعات الذي لا يمكنك ترحيل إيصال تعبئة لحمل العمل به.</span><span class="sxs-lookup"><span data-stu-id="6f55c-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="6f55c-121">في علامة التبويب **بنود أمر المبيعات**، حدد بند أوامر المبيعات للصنف الذي يتجاوز النسبة المئوية للتسليم الناقص.</span><span class="sxs-lookup"><span data-stu-id="6f55c-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="6f55c-122">في علامة التبويب  **تفاصيل البنود**، حدد **تسليم**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="6f55c-123">قم بتعيين الحقل **التسليم الناقص** إلى نسبة مئوية أكبر تستوعب الكمية التي تم انتقاؤها مقابل كمية حمل العمل، بحيث يمكن متابعة إنشاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="6f55c-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="6f55c-124">عكس وإجراء تسويات</span><span class="sxs-lookup"><span data-stu-id="6f55c-124">Reverse and make adjustments</span></span>

<span data-ttu-id="6f55c-125">اعكس كل شيء تم ترحيل حمل العمل (على سبيل المثال، إيصال التعبئة وتأكيد الشحن والعمل)، وإجراء تسويات أمر المبيعات، وإصدار الأمر إلى المستودع مرة أخرى، وإكمال إجراء الشحن.</span><span class="sxs-lookup"><span data-stu-id="6f55c-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="6f55c-126">استخدم الإجراء التالي لإلغاء إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="6f55c-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="6f55c-127">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6f55c-128">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة **عكس**، حدد **إلغاء إيصالات التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="6f55c-129">استخدم الإجراء التالي لعكس تأكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="6f55c-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="6f55c-130">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6f55c-131">في جزء الإجراءات، في علامة التبويب **الشحن والاستلام**، في المجموعة  **عكس**، حدد **عكس تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="6f55c-132">استخدم الإجراء التالي لعكس العمل.</span><span class="sxs-lookup"><span data-stu-id="6f55c-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="6f55c-133">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6f55c-134">في جزء الإجراءات، ضمن علامة التبويب **أحمال العمل**، في المجموعة **العمل**، حدد **عكس العمل**.</span><span class="sxs-lookup"><span data-stu-id="6f55c-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
