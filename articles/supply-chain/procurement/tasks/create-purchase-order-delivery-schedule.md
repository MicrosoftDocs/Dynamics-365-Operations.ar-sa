--- 
title: "إنشاء أمر شراء مع جدول تسليم"
description: "يُوضح هذا الإجراء كيفية إنشاء جدول تسليم لأمر شراء."
author: FrankDahl
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ae57d8e64b4888e6ff4678437d0b3da8eb05867d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="124bb-103">إنشاء أمر شراء مع جدول تسليم</span><span class="sxs-lookup"><span data-stu-id="124bb-103">Create a purchase order with a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="124bb-104">يُوضح هذا الإجراء كيفية إنشاء جدول تسليم لأمر شراء.</span><span class="sxs-lookup"><span data-stu-id="124bb-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="124bb-105">يتم استخدام جدول التسليم عندما يتم طلب كمية في أمر أو دفتر يومية بحيث يتم تسليمها بواسطة شحنات متعددة.</span><span class="sxs-lookup"><span data-stu-id="124bb-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="124bb-106">يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="124bb-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="124bb-107">يقوم عادةً وكيل الشراء بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="124bb-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="124bb-108">إنشاء جدول تسليم</span><span class="sxs-lookup"><span data-stu-id="124bb-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="124bb-109">انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="124bb-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="124bb-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="124bb-110">Click New.</span></span>
3. <span data-ttu-id="124bb-111">في حقل "حساب المورّد‬"، أدخل "US-101".</span><span class="sxs-lookup"><span data-stu-id="124bb-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="124bb-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="124bb-112">Click OK.</span></span>
5. <span data-ttu-id="124bb-113">في الحقل "رقم الصنف"، أدخل "M0001".</span><span class="sxs-lookup"><span data-stu-id="124bb-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="124bb-114">في حقل "الكمية"، أدخل ''10".</span><span class="sxs-lookup"><span data-stu-id="124bb-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="124bb-115">انقر فوق سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="124bb-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="124bb-116">انقر فوق "جدول التسليم".</span><span class="sxs-lookup"><span data-stu-id="124bb-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="124bb-117">تسمح لك صفحة "جدول التسليم" بتحديد عدد الشحنات التي سيتم تسليم الكمية الإجمالية لبند الأمر فيها إلى المورّد.</span><span class="sxs-lookup"><span data-stu-id="124bb-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="124bb-118">بشكل افتراضي، ينسخ النظام إجمالي الكمية وتفاصيل التسليم الأخرى لبند أمر الشراء الأصلي إلى البند الأول في جدول التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="124bb-119">في هذا المثال، سننشئ جدولاً لشحنتين، مع إزاحة تاريخ الشحنة الثانية بمقدار أسبوع عن الشحنة الأولى.</span><span class="sxs-lookup"><span data-stu-id="124bb-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="124bb-120">في حقل "الكمية"، غيّر الكمية إلى "4".</span><span class="sxs-lookup"><span data-stu-id="124bb-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="124bb-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="124bb-121">Click New.</span></span>
11. <span data-ttu-id="124bb-122">في حقل "الكمية"، أدخل 6 كالكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="124bb-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="124bb-123">في حقل "تاريخ التسليم"، حدد تاريخًا يقع بعد أسبوع واحد من بند التسليم الأول.</span><span class="sxs-lookup"><span data-stu-id="124bb-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="124bb-124">يمكنك تعقب إجمالي الكمية التي تم تخصيصها إلى بنود جدول التسليم بالنظر إلى حقلي "الإجمالي" و"المتبقي".</span><span class="sxs-lookup"><span data-stu-id="124bb-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="124bb-125">عندما تكون الكمية المتبقية صفر، فهذا يعني أن الكمية الكاملة من البند الأصلي تم تخصيصها للجدول.</span><span class="sxs-lookup"><span data-stu-id="124bb-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="124bb-126">قم بتوسيع مقطع "تحويل التكاليف".</span><span class="sxs-lookup"><span data-stu-id="124bb-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="124bb-127">تسمح لك الخيارات الموجودة هنا بالتحكم في كيفية توزيع المصاريف عبر بنود جدول التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="124bb-128">إذا قمت بتحديد "نسخ إجمالي المبالغ‬"، فسيتم نسخ مبلغ التكلفة على بند الأمر الأصلي إلى كل بند تسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="124bb-129">يقوم الخيار "تخصيص لسطور التسليم‬" بتقسيم تكلفة البند الأصلي وفقًا للكمية في كل بند تسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="124bb-130">قم بطي مقطع "تحويل التكاليف".</span><span class="sxs-lookup"><span data-stu-id="124bb-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="124bb-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="124bb-131">Click OK.</span></span>
    * <span data-ttu-id="124bb-132">تم الآن تطبيق جدول التسليم على الأمر.</span><span class="sxs-lookup"><span data-stu-id="124bb-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="124bb-133">تم تحويل بند الأمر الأصلي، المشار إليه الآن كبند تجاري، إلى بند أمر بعمليات تسليم متعددة.</span><span class="sxs-lookup"><span data-stu-id="124bb-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="124bb-134">تم وضع علامة عليه بواسطة أيقونة مميزة تعمل كرأس لبنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="124bb-135">حدد بند الأمر الثاني، وهو البند الأول من بندي التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="124bb-136">يشكّل البندين الجديدين، المشار إليهما ببنود التسليم، جدول تسليم واحدًا.</span><span class="sxs-lookup"><span data-stu-id="124bb-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="124bb-137">ستتم معالجة الأمر في مقابل هذه البنود وليس البند الأصلي.</span><span class="sxs-lookup"><span data-stu-id="124bb-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="124bb-138">إذا تمت طباعة مستندات، مثل مستندات التأكيد أو دفاتر يومية إيصالات استلام المنتجات‬ أو الفواتير، فإن بنود التسليم وحدها ستظهر.</span><span class="sxs-lookup"><span data-stu-id="124bb-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="124bb-139">تغيير جدول التسليم</span><span class="sxs-lookup"><span data-stu-id="124bb-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="124bb-140">يمكنك تغيير الكمية في بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="124bb-141">إذا قمت بذلك، فسيتم تحديث البند التجاري بشكل تلقائي إلى الكمية الإجمالية في بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="124bb-142">في حقل "الكمية" من بند التسليم الأول، قم بتغيير الكمية من 4 إلى 5.</span><span class="sxs-lookup"><span data-stu-id="124bb-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="124bb-143">حدد بند الأمر الأول (البند التجاري).</span><span class="sxs-lookup"><span data-stu-id="124bb-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="124bb-144">تم تغيير الكمية الموجودة في البند التجاري إلى 11.</span><span class="sxs-lookup"><span data-stu-id="124bb-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="124bb-145">معالجة إيصال استلام المنتجات باستخدام جداول التسليم</span><span class="sxs-lookup"><span data-stu-id="124bb-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="124bb-146">يجب تأكيد أمر الشراء قبل معالجة إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="124bb-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="124bb-147">في هذا المثال، يتم تسجيل إيصال الاستلام بشكل مباشر على أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="124bb-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="124bb-148">من الممكن أيضًا تسجيل إيصال الاستلام عند وصول البضائع إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="124bb-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="124bb-149">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="124bb-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="124bb-150">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="124bb-150">Click Confirm.</span></span>
3. <span data-ttu-id="124bb-151">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="124bb-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="124bb-152">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="124bb-152">Click Product receipt.</span></span>
5. <span data-ttu-id="124bb-153">في الحقل "إيصال استلام المنتجات"، اكتب أي قيمة.</span><span class="sxs-lookup"><span data-stu-id="124bb-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="124bb-154">يتم استخدام هذا الحقل لإدخال مرجع سيتم استخدامه كإيصال لدفتر يومية إيصال استلام المنتج.</span><span class="sxs-lookup"><span data-stu-id="124bb-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="124bb-155">في حقل "الكمية"، حدد "الكمية المطلوبة".</span><span class="sxs-lookup"><span data-stu-id="124bb-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="124bb-156">يعني هذا الخيار أن إيصال الاستلام سيعالج الكمية التي تم إنشاء بنود الأمر معها.</span><span class="sxs-lookup"><span data-stu-id="124bb-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="124bb-157">تأكد من تعيين الحقل "طباعة إيصال استلام المنتجات‬" إلى "لا".</span><span class="sxs-lookup"><span data-stu-id="124bb-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="124bb-158">الطباعة غير مطلوبة في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="124bb-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="124bb-159">قم بتوسيع القسم "البنود".</span><span class="sxs-lookup"><span data-stu-id="124bb-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="124bb-160">لاحظ كيف تم إنشاء إيصال استلام المنتجات لبندي التسليم وليس لبند الأمر الأصلي.</span><span class="sxs-lookup"><span data-stu-id="124bb-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="124bb-161">إذا تم تسجيل إيصال الاستلام في المستودع، فقد يتم أيضًا تسجيله على بنود جدول التسليم.</span><span class="sxs-lookup"><span data-stu-id="124bb-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="124bb-162">قم بطي مقطع "البنود".</span><span class="sxs-lookup"><span data-stu-id="124bb-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="124bb-163">انقر فوق "موافق" لترحيل إيصال الاستلام.</span><span class="sxs-lookup"><span data-stu-id="124bb-163">Click OK to post the receipt.</span></span>


