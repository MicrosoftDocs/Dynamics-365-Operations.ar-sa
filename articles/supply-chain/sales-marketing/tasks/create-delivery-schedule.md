---
title: إنشاء جدول تسليم
description: يُوضح هذا الإجراء كيفية إنشاء جدول تسليم لأمر مبيعات.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dccc90321977382c7625ca1785427a6d26a14f27
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835612"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="37546-103">إنشاء جدول تسليم</span><span class="sxs-lookup"><span data-stu-id="37546-103">Create delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37546-104">يُوضح هذا الإجراء كيفية إنشاء جدول تسليم لأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="37546-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="37546-105">يتم استخدام جدول التسليم عندما يتم طلب كمية في أمر أو عرض أسعار بحيث يتم التسليم بواسطة شحنات متعددة.</span><span class="sxs-lookup"><span data-stu-id="37546-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="37546-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="37546-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="37546-107">إنشاء جدول تسليم</span><span class="sxs-lookup"><span data-stu-id="37546-107">Create delivery schedule</span></span>
1. <span data-ttu-id="37546-108">انتقل إلى "كافة أوامر المبيعات‬".</span><span class="sxs-lookup"><span data-stu-id="37546-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="37546-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37546-109">Click New.</span></span>
3. <span data-ttu-id="37546-110">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37546-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="37546-111">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="37546-111">Click OK.</span></span>
5. <span data-ttu-id="37546-112">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37546-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="37546-113">في الحقل "الكمية"، أدخل رقمًا أكبر من 1.</span><span class="sxs-lookup"><span data-stu-id="37546-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="37546-114">انقر فوق بند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="37546-114">Click Sales order line.</span></span>
8. <span data-ttu-id="37546-115">انقر فوق "جدول التسليم".</span><span class="sxs-lookup"><span data-stu-id="37546-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="37546-116">الصفحة "جدول التسليم" هي المكان حيث يمكنك تحديد عدد الشحنات التي سيتم تسليم الكمية الإجمالية لبند الأمر فيها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="37546-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="37546-117">بشكل افتراضي، ينسخ النظام إجمالي الكمية وتفاصيل التسليم الأخرى لبند المبيعات الأصلي إلى البند الأول في جدول التسليم.</span><span class="sxs-lookup"><span data-stu-id="37546-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="37546-118">في هذا المثال، سننشئ جدولاً لشحنتين، مع إزاحة تاريخ الشحنة الثانية بمقدار أسبوع عن الشحنة الأولى.</span><span class="sxs-lookup"><span data-stu-id="37546-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="37546-119">في الحقل "الكمية"، أدخل رقمًا يشكل جزءًا من إجمالي الكمية.</span><span class="sxs-lookup"><span data-stu-id="37546-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="37546-120">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="37546-120">Click New.</span></span>
11. <span data-ttu-id="37546-121">في الحقل "الكمية"، أدخل الكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="37546-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="37546-122">في الحقل "تاريخ الشحن المطلوب"، أدخل تاريخًا يكون عبارة عن أسبوع واحد يسبق تاريخ بند التسليم الأول.</span><span class="sxs-lookup"><span data-stu-id="37546-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="37546-123">يتحكم الخياران على علامة التبويب السريعة "تحويل التكاليف‬" في الطريقة التي تريد بها توزيع التكاليف‬ عبر بنود جدول التسليم، حالما تم تعيينها إلى بند الأمر الأصلي.</span><span class="sxs-lookup"><span data-stu-id="37546-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="37546-124">إذا قمت بتحديد "نسخ إجمالي المبالغ‬"، فسيتم نسخ مبلغ التكلفة نفسه إلى كل بند.</span><span class="sxs-lookup"><span data-stu-id="37546-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="37546-125">يقوم الخيار "تخصيص لبنود التسليم‬" بتقسيم التكلفة بطريقة متساوية عبر بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="37546-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="37546-126">يمكن تقسيم التكاليف الثابتة فقط، بينما سيستمر نسخ التكاليف المتغيرة إلى البنود.</span><span class="sxs-lookup"><span data-stu-id="37546-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="37546-127">انقل المؤشر بعيدًا عن خط التسليم الثاني لتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37546-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="37546-128">يمكنك تعقب إجمالي الكمية التي تم تخصيصها إلى بنود جدول التسليم بالنظر إلى حقلي "الإجمالي" و"المتبقي".</span><span class="sxs-lookup"><span data-stu-id="37546-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="37546-129">عندما تكون الكمية المتبقية صفر، فهذا يعني أن الكمية الكاملة من البند الأصلي تم تخصيصها للجدول.</span><span class="sxs-lookup"><span data-stu-id="37546-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="37546-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37546-130">Click OK.</span></span>
    * <span data-ttu-id="37546-131">تم الآن نسخ جدول التسليم إلى بنود الأمر.</span><span class="sxs-lookup"><span data-stu-id="37546-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="37546-132">تم تحويل بند الأمر الأصلي، المشار إليه كبند تجاري، إلى بند أمر بعمليات تسليم متعددة.</span><span class="sxs-lookup"><span data-stu-id="37546-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="37546-133">تم وضع علامة عليه بواسطة أيقونة مميزة ويعمل كرأس لبنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="37546-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="37546-134">يشكّل البندين الجديدين، المشار إليهما ببنود التسليم، جدول تسليم واحدًا.</span><span class="sxs-lookup"><span data-stu-id="37546-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="37546-135">ستتم معالجة الأمر في مقابل هذه البنود وليس البند الأصلي.</span><span class="sxs-lookup"><span data-stu-id="37546-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="37546-136">إذا تمت طباعة مستندات، مثل إيصالات التأكيد أو قوائم الانتقاء أو إيصالات التعبئة أو الفواتير، فإن بنود التسليم وحدها ستظهر.</span><span class="sxs-lookup"><span data-stu-id="37546-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="37546-137">بإمكان بنود التسليم أن تتضمن تواريخ تسليم وكميات وأوضاع تسليم وأبعاد تخزين مختلفة، مثل الموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="37546-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="37546-138">ومع ذلك، يجب أن تتطابق أبعاد المنتج دائمًا مع تلك الموجودة في البند التجاري ولا يمكن تغييرها.</span><span class="sxs-lookup"><span data-stu-id="37546-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="37546-139">في الحقل "الكمية"، أدخل رقمًا أكبر من الرقم الحالي.</span><span class="sxs-lookup"><span data-stu-id="37546-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="37546-140">حدد البند التجاري لمعرفة تأثير إعادة حساب الكمية.</span><span class="sxs-lookup"><span data-stu-id="37546-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="37546-141">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="37546-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="37546-142">انقر فوق "ترحيل إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="37546-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="37546-143">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="37546-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="37546-144">في الحقل "الكمية"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="37546-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="37546-145">لاحظ أنه سيتم إنشاء إيصال التعبئة لبندين من بنود جدول تسليم وليس بند الأمر الأصلي.</span><span class="sxs-lookup"><span data-stu-id="37546-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="37546-146">حدد "نعم" في الحقل "طباعة إيصال التعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="37546-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="37546-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37546-147">Click OK.</span></span>
23. <span data-ttu-id="37546-148">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="37546-148">Click Yes.</span></span>
24. <span data-ttu-id="37546-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37546-149">Close the page.</span></span>

