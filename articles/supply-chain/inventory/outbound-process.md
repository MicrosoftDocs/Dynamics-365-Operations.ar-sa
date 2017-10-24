---
title: "العملية الصادرة"
description: "يوفر هذا الموضوع نظرة عامة حول العملية الصادرة في إدارة المخزون."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: ar-sa
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="f1bad-103">العملية الصادرة</span><span class="sxs-lookup"><span data-stu-id="f1bad-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f1bad-104">يوفر هذا الموضوع نظرة عامة حول العملية الصادرة في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="f1bad-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="f1bad-105">أوامر المخرجات</span><span class="sxs-lookup"><span data-stu-id="f1bad-105">Output orders</span></span>

<span data-ttu-id="f1bad-106">يتم استخدام أوامر المخرجات لربط بنود أوامر المبيعات وبنود أوامر التحويل مع عمليات الانتقاء الصادرة التي تستخدم قوائم الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="f1bad-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="f1bad-107">عندما يتم إنشاء قوائم الانتقاء إما من أوامر المبيعات أو من أوامر التحويل، يتم تلقائيًا إنشاء أوامر المخرجات والشحنات.</span><span class="sxs-lookup"><span data-stu-id="f1bad-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="f1bad-108">هناك علاقة واحد بواحد بين قائمة الانتقاء والشحنة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="f1bad-109">يمكن معالجة شحنة أمر التحويل أو قائمة انتقاء أمر المبيعات من الشحنة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="f1bad-110">يعرض المخطط‬ التالي نظرة عامة على عملية الأوامر الصادرة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="f1bad-111">[![نظرة عامة على عملية الأوامر الصادرة](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="f1bad-112">يمكنك إعداد قواعد الأوامر الصادرة لتحديد الطريقة التي تريد من خلالها أن يتعامل البرنامج مع عملية الأوامر الصادرة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="f1bad-113">يمكنك استخدام هذه القواعد للتحكم في عملية الشحن.</span><span class="sxs-lookup"><span data-stu-id="f1bad-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="f1bad-114">وبشكل خاص، يمكنك استخدام القواعد لتحديد المرحلة في العملية التي يمكن خلالها إرسال الشحنة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="f1bad-115">تحدد الإعدادات التالية كيفية التعامل مع العمليات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="f1bad-116">استخدام حالة مسار الانتقاء لأوامر المبيعات وأوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="f1bad-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="f1bad-117">انتقل إلى **الحسابات المدينة** \> **الإعداد** \> **محددات الحسابات المدينة‬‏‫**، ثم على علامة تبويب **التحديثات**، حدد قيمة في حقل **حالة مسار الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="f1bad-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="f1bad-118">[![حقل حالة مسار الانتقاء لأوامر المبيعات](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="f1bad-119">إذا تم تعيين حقل **حالة مسار الانتقاء** الحقل إلى **مكتمل**، فإن عملية الانتقاء تحدث تلقائيًا كجزء من عملية إنشاء قوائم الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="f1bad-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="f1bad-120">إذا تم تعيين الحقل إلى **نشط**، فيجب تحديث بنود قائمة الانتقاء يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f1bad-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="f1bad-121">ينطبق الإعداد نفسه على أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="f1bad-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="f1bad-122">انتقل إلى **إدارة المخزون** \> **الإعداد** \> **محددات إدارة المستودعات والمخزون‬**، ثم على علامة التبويب **نقل**، حدد قيمة في حقل **حالة مسار الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="f1bad-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="f1bad-123">[![حقل حالة مسار الانتقاء لأوامر التحويل](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="f1bad-124">إنهاء أوامر مخزنية للمخرجات</span><span class="sxs-lookup"><span data-stu-id="f1bad-124">End output inventory orders</span></span>

<span data-ttu-id="f1bad-125">انتقل إلى **إدارة المخزون** \> **الإعداد** \> **محددات إدارة المستودعات والمخزون‬**، ثم على علامة التبويب **عام**، عيّن الخيار **إنهاء أمر مخزني للمخرجات**.</span><span class="sxs-lookup"><span data-stu-id="f1bad-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="f1bad-126">[![الخيار إنهاء أمر مخزني للمخرجات](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="f1bad-127">في بعض الأحيان، لا يمكن انتقاء بعض العناصر الموجودة في المخزون كجزء من عملية معالجة قائمة انتقاء.</span><span class="sxs-lookup"><span data-stu-id="f1bad-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="f1bad-128">على سبيل المثال، قد تحدث هذه الحالة إذا قام عامل مستودع بتقليل الكميات في بنود الانتقاء وقام بمعالجة قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="f1bad-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="f1bad-129">إذا تم تعيين الخيار **إنهاء أمر مخزني للمخرجات‬** إلى **نعم**، فسيتم الإبلاغ عن الكميات المتبقية غير المنتقاة لإعادتها إلى مستوى الأمر.</span><span class="sxs-lookup"><span data-stu-id="f1bad-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="f1bad-130">إذا تم تعيين الخيار إلى **لا**، فسيتم الاحتفاظ بالكميات المتبقية غير المنتقاة ككمية أمر مخرجات مفتوح.</span><span class="sxs-lookup"><span data-stu-id="f1bad-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="f1bad-131">في هذه الحالة، تبقى الكميات صادرة إلى المستودع ويجب إضافتها إلى قائمة انتقاء جديدة كجزء من وظيفة **فتح أوامر المخرجات**.</span><span class="sxs-lookup"><span data-stu-id="f1bad-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="f1bad-132">[![الأمر "فتح أوامر المخرجات" في قائمة "الوظائف"](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="f1bad-133">[![قائمة "الوظائف" في صفحة "فتح أوامر المخرجات"](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="f1bad-134">خفض الكمية</span><span class="sxs-lookup"><span data-stu-id="f1bad-134">Reduce quantity</span></span>

<span data-ttu-id="f1bad-135">المعلمة الثالثة التي يمكنك استخدامها كجزء من عملية إنشاء قوائم الانتقاء هي المعلمة **خفض الكمية‬**.</span><span class="sxs-lookup"><span data-stu-id="f1bad-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="f1bad-136">يعمل إعداد هذه المعلمة مع إعداد **الحجز** الذي يقوم بتشغيل عملية حجز كجزء من الإصدار إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="f1bad-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="f1bad-137">[![معلمة خفض الكمية](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="f1bad-138">مثال عملية صادرة‬ لأمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="f1bad-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="f1bad-139">بالنسبة إلى هذا المثال، هناك أمر مبيعات لصنفين.</span><span class="sxs-lookup"><span data-stu-id="f1bad-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="f1bad-140">أثناء إنشاء قائمة الانتقاء، حدد معلمة **خفض الكمية**.</span><span class="sxs-lookup"><span data-stu-id="f1bad-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="f1bad-141">لذلك، يمكنك إصدار وإنشاء بنود الانتقاء فقط للمخزون الفعلي المتاح.</span><span class="sxs-lookup"><span data-stu-id="f1bad-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="f1bad-142">يجب الإعلام عن الانتقاء من خلال عملية تسجيل لقوائم الانتقاء (**حالة مسار الانتقاء** = **نشط**).</span><span class="sxs-lookup"><span data-stu-id="f1bad-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="f1bad-143">يتم حجز المخزون الذي لم يتم حجزه بالفعل أثناء إنشاء قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="f1bad-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="f1bad-144">يمكن إزالة المخزون غير المتوفر من أمر المبيعات أو يمكن إصداره إلى المستودع لمعالجة الصادر لاحقًا، عندما يكون المخزون متوفرًا للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="f1bad-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="f1bad-145">[![تحديث قائمة الانتقاء](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="f1bad-146">بمجرد انتقاء كافة بنود الانتقاء في صفحة **تسجيل قائمة الانتقاء**، يتم إكمال الشحنة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="f1bad-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="f1bad-147">يمكن تهيئة عملية إيصالات التعبئة لأوامر المبيعات استنادًا إلى المخزون المنتقى.</span><span class="sxs-lookup"><span data-stu-id="f1bad-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="f1bad-148">[![تحديث الشحنات الصادرة](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="f1bad-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

