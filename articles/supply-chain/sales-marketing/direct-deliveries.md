---
title: "عمليات التسليم المباشرة"
description: "يوفر هذا المقال معلومات حول عمليات التسليم المباشرة‬. عمليات التسليم المباشرة‬ عبارة عن عمليات تسليم يتم إرسالها من المورّد إلى عمليك بشكل مباشر."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1f2cdae674dc88a4d533258e24b1ecf7ec4cf55b
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="direct-deliveries"></a><span data-ttu-id="ce9bc-104">عمليات التسليم المباشرة</span><span class="sxs-lookup"><span data-stu-id="ce9bc-104">Direct deliveries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ce9bc-105">يوفر هذا المقال معلومات حول عمليات التسليم المباشرة‬.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-105">This article provides information about direct deliveries.</span></span> <span data-ttu-id="ce9bc-106">عمليات التسليم المباشرة‬ عبارة عن عمليات تسليم يتم إرسالها من المورّد إلى عمليك بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-106">Direct deliveries are deliveries that are sent directly from the vendor to your customer.</span></span>

<span data-ttu-id="ce9bc-107">تقوم عمليات التسليم المباشرة بتوفير وقت التسليم والحد من التكاليف المرتبطة بنقل المخزون، وذلك نظرًا لأنك لا تحتفظ بالمنتجات في المستودع الخاص بك قبل شحنها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-107">Direct deliveries save delivery time and reduce the costs that are associated with carrying inventory, because you don't hold the products in your warehouse before you ship them to the customer.</span></span>  

<span data-ttu-id="ce9bc-108">يمكنك إنشاء عمليات تسليم مباشرة من صفحة **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-108">You can create direct deliveries from the **Sales order** page.</span></span> <span data-ttu-id="ce9bc-109">وأولاً، أنشئ أمر مبيعات وبنود أمر.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-109">First, create a sales order and order lines.</span></span> <span data-ttu-id="ce9bc-110">وبعد ذلك، في جزء الإجراءات، في علامة التبويب **أمر المبيعات**، حدد **التسليم المباشر**.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-110">Then, on the Action Pane, on the **Sales order** tab, select **Direct delivery**.</span></span> <span data-ttu-id="ce9bc-111">وأخيرًا، حدد البنود التي ينبغي تناولها كتسليم مباشر.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-111">Finally, specify the lines that must be handled as a direct delivery.</span></span> <span data-ttu-id="ce9bc-112">ويتم الآن إنشاء ارتباط بين سطور أمر المبيعات للتسليم المباشر، وسطور أمر الشراء المقابلة لها.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-112">A link is now created between the sales order lines for the direct delivery and the corresponding purchase order lines.</span></span>  

<span data-ttu-id="ce9bc-113">**ملاحظة:** إذا كان قد تم بالفعل تسليم جزء من الكمية المطلوبة، يجب عليك تقسيم الكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-113">**Note:** If part of the ordered quantity has already been delivered, you must split the remaining quantity.</span></span> <span data-ttu-id="ce9bc-114">قم بإنشاء بند جديد بالكمية التي يتم تسليمها مباشرة وطرح هذه الكمية من الكمية الموجودة في البند الأصلي.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-114">Create a new line for the quantity that must be directly delivered, and subtract that quantity from the quantity on the original line.</span></span> <span data-ttu-id="ce9bc-115">على سبيل المثال، إذا كانت الكمية الأصلية 15 وتم تسليم خمسة، يجب إنشاء سطر جديد للكمية المتبقية من 10، ثم تقليل الكمية الأصلية بمقدار هذا المبلغ.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-115">For example, if the original quantity was 15, and five have been delivered, you must create a new line for the remaining quantity, 10, and then reduce the original quantity by that amount.</span></span>  

<span data-ttu-id="ce9bc-116">وبعد إنشاء ارتباط التسليم المباشر بين بنود أمر المبيعات وبنود أمر الشراء، يمكنك تحديث أمر المبيعات باستخدام إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-116">After you create the direct delivery link between the sales order lines and the purchase order lines, you can update the sales order by using a packing slip.</span></span> <span data-ttu-id="ce9bc-117">قم بتشغيل تحديث إيصال التعبئة أو تحديث فاتورة من أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-117">Run either a packing slip update or an invoice update from the purchase order.</span></span> <span data-ttu-id="ce9bc-118">يجب فوترة تحديث أمر المبيعات من صفحة **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-118">You must invoice-update the sales order from the **Sales order** page.</span></span> <span data-ttu-id="ce9bc-119">ولا يمكن أن يؤدي تحديث الفاتورة إلى أن تتجاوز الكمية في أمر المبيعات الكمية التي تم تسجيل استلامها.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-119">An invoice update can't cause the quantity on the sales order to exceed the quantity that has been registered as received.</span></span> <span data-ttu-id="ce9bc-120">على سبيل المثال، بند أمر المبيعات يحتوي على 10 قطع، لكن تم تحديث 5 قطع فقط من بند أمر المبيعات باستخدام إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-120">For example, a sales order line has 10 pieces, but only five pieces from the sales order line have been updated by using a packing slip.</span></span> <span data-ttu-id="ce9bc-121">وإذا قمت بتحديد **الكل** في قائمة **الجودة** عند فوترة تحديث أمر المبيعات، فقط تلك الأصناف التي تم استلامها فعلياً، أو تحديثها باستخدام إيصال التعبئة، تعد تحديث الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-121">If you select **All** in the **Quantity** list when you invoice-update the sales order, only those items that have been physically received, or updated by using a packing slip, are invoice-updated.</span></span> <span data-ttu-id="ce9bc-122">لا يتم تحديث بند أمر المبيعات بالكامل.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-122">The whole sales order line isn't updated.</span></span>

## <a name="delivery-date"></a><span data-ttu-id="ce9bc-123">تاريخ التسليم</span><span class="sxs-lookup"><span data-stu-id="ce9bc-123">Delivery date</span></span>
<span data-ttu-id="ce9bc-124">وعند قيامك بتحديث حقل **تاريخ الاستلام المطلوب** في بند أمر المبيعات، ويتم أيضًا تحديث حقل **تاريخ التسليم** في بند أمر الشراء المقابل.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-124">When you update the **Requested receipt date** field on the sales order line, the **Delivery date** field on the corresponding purchase order line is also updated.</span></span> <span data-ttu-id="ce9bc-125">بالمثل، عند تحديث حقل **مؤكد** في بند أمر الشراء، يتم تحديث حقلي **تاريخ الاستم المؤكد** و**تاريخ الشحن المؤكد** في بند أمر المبيعات المطابق.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-125">Similarly, when you update the **Confirmed** field on the purchase order line, the **Confirmed receipt date** and **Confirmed ship date** fields on the corresponding sales order line are also updated.</span></span>

## <a name="delivery-address"></a><span data-ttu-id="ce9bc-126">عنوان التسليم</span><span class="sxs-lookup"><span data-stu-id="ce9bc-126">Delivery address</span></span>
<span data-ttu-id="ce9bc-127">عادةً ما يكون عنوان التسليم لأمر الشراء هو عنوان الشركة.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-127">Typically, the delivery address for a purchase order is the company's address.</span></span> <span data-ttu-id="ce9bc-128">ومع ذلك، عندما تقوم بإنشاء تسليم مباشر، تقوم بإدخال عنوان العميل على أنه عنوان التسليم.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-128">However, when you create a direct delivery, you enter the customer's address as the delivery address.</span></span> <span data-ttu-id="ce9bc-129">وإذا قمت بتغيير عنوان التسليم لبند أمر الشراء الذي من نوع تسليم **التسليم المباشر**، فإنه يتم أيضًا تحديث عنوان التسليم لبند أمر المبيعات المطابق.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-129">If you change the delivery address on a purchase order line that has a delivery type of **Direct delivery**, the delivery address on the corresponding sales order line is also updated.</span></span> <span data-ttu-id="ce9bc-130">وبالمثل، إذا قمت بتغيير عنوان التسليم في سطر أمر المبيعات، فإنه يتم تحديث عنوان التسليم في سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-130">Similarly, if you change the delivery address on the sales order line, the delivery address on the purchase order line is also updated.</span></span>

## <a name="deleting-order-lines"></a><span data-ttu-id="ce9bc-131">حذف سطور الأمر</span><span class="sxs-lookup"><span data-stu-id="ce9bc-131">Deleting order lines</span></span>
<span data-ttu-id="ce9bc-132">إذا حاولت حذف بند أمر مبيعات من نوع تسليم **التسليم المباشر**, يفيد مربع رسالة توضح بأن بنود أمر الشراء مرفقة بالبند.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-132">If you try to delete a sales order line that has a delivery type of **Direct delivery**, a message box states that purchase order lines are attached to the line.</span></span> <span data-ttu-id="ce9bc-133">وإذا تم تسليم بند أمر امبيعات بشكلٍ جزئي، فلا يمكنك حذف بند أمر المبيعات أو بنود أمر الشراء المرفقة به.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-133">If the sales order line has been partially delivered, you can't delete the sales order line or the purchase order lines that are attached to it.</span></span>

## <a name="warehouse"></a><span data-ttu-id="ce9bc-134">المستودع</span><span class="sxs-lookup"><span data-stu-id="ce9bc-134">Warehouse</span></span>
<span data-ttu-id="ce9bc-135">عندما تقوم بإنشاء تسليم مباشر، فالأصناف التي تقوم ببيعها لا تصل مطلقًا إلى المستودع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-135">When you create a direct delivery, the items that you sell never physically arrive at your warehouse.</span></span> <span data-ttu-id="ce9bc-136">ومع ذلك، لا يزال يجب تحديد مستودع في سطر أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-136">However, you must still specify a warehouse on the sales order line.</span></span> <span data-ttu-id="ce9bc-137">وبالمثل، انتقاء متطلبات قد يتم تحديدها للصنف في مجموعة نموذج الصنف.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-137">Similarly, picking requirements might be specified on the item model group for the item.</span></span> <span data-ttu-id="ce9bc-138">ومع ذلك، نظراً لاستحالة وصول الأصناف فعلياً في المستودع الخاص بك، يتم تجاهل هذه المتطلبات عندما يكون أمر التوريد تسليم مباشر.</span><span class="sxs-lookup"><span data-stu-id="ce9bc-138">However, because the items never physically arrive at your warehouse, these requirements are ignored when the sales order is a direct delivery.</span></span>




