--- 
title: "شحن الأوامر كعمليات تسليم مباشرة"
description: "يُوضح هذا الإجراء كيفية إنشاء جدول تسليم مباشر لأمر مبيعات."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8691eea1f339902aa74978fa8f27151754cb3e09
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="ship-orders-as-direct-deliveries"></a><span data-ttu-id="224b8-103">شحن الأوامر كعمليات تسليم مباشرة</span><span class="sxs-lookup"><span data-stu-id="224b8-103">Ship orders as direct deliveries</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="224b8-104">يُوضح هذا الإجراء كيفية إنشاء جدول تسليم مباشر لأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="224b8-104">This procedure demonstrates how to create a direct delivery for a sales order.</span></span> <span data-ttu-id="224b8-105">يمكنك استخدام التسليم المباشر عندما تريد شحن البضائع إلى العميل مباشرة من المورد، بدلاً من شحنها إلى المستودع الخاص بك أولاً.</span><span class="sxs-lookup"><span data-stu-id="224b8-105">You use direct delivery when you want to ship goods to the customer directly from your vendor, instead of shipping them to your own warehouse first.</span></span> <span data-ttu-id="224b8-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="224b8-106">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="224b8-107">لإكمال المهمة الفرعية الثانية، "إنشاء عمليات تسليم مباشرة من منضدة العمل" بنجاح، تأكد أن الصنف الذي قمت باختياره في أمر المبيعات له مورد افتراضي محدد بعلامة التبويب السريعة "الشراء" من لأصل المنتج الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="224b8-107">To successfully complete the second sub-task "Create direct deliveries from the workbench", make sure that the item that you choose on the sales order has a default Vendor specified on the Purchase FastTab of the Released product master.</span></span>


## <a name="set-an-individual-order-for-direct-delivery"></a><span data-ttu-id="224b8-108">تعيين ترتيب فردي للتسليم المباشر</span><span class="sxs-lookup"><span data-stu-id="224b8-108">Set an individual order for direct delivery</span></span>
1. <span data-ttu-id="224b8-109">انتقل إلى "كافة أوامر المبيعات‬".</span><span class="sxs-lookup"><span data-stu-id="224b8-109">Go to All sales orders.</span></span>
2. <span data-ttu-id="224b8-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="224b8-110">Click New.</span></span>
3. <span data-ttu-id="224b8-111">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="224b8-111">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="224b8-112">إذا كنت تستخدم USMF، يمكنك تحديد الحساب "الولايات المتحدة-001".</span><span class="sxs-lookup"><span data-stu-id="224b8-112">If you’re using USMF, you can select account US-001.</span></span>  
4. <span data-ttu-id="224b8-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="224b8-113">Click OK.</span></span>
5. <span data-ttu-id="224b8-114">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="224b8-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="224b8-115">إذا كنت تستخدم USMF، يمكنك تحديد الصنف T0020.</span><span class="sxs-lookup"><span data-stu-id="224b8-115">If you’re using USMF, you can select item T0020.</span></span>  
6. <span data-ttu-id="224b8-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="224b8-116">Click Save.</span></span>
7. <span data-ttu-id="224b8-117">في جزء "الإجراءات"، انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="224b8-117">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="224b8-118">انقر فوق "تسليم مباشر".</span><span class="sxs-lookup"><span data-stu-id="224b8-118">Click Direct delivery.</span></span>
    * <span data-ttu-id="224b8-119">تسرد صفحة "إنشاء التسليم" جميع بنود أوامر المبيعات المفتوحة كما يتم نسخها من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="224b8-119">The Create delivery page lists all the open sales order lines as copied from the sales order.</span></span> <span data-ttu-id="224b8-120">يمكنك مراجعة تفاصيل الأوامر، وإذا لزم الأمر، تعديل تفاصيل مثل كمية الشراء وشروط تحديد السعر قبل إنشاء تسليم مباشر.</span><span class="sxs-lookup"><span data-stu-id="224b8-120">You can review the order details, and if required, you can modify details such purchase quantity and pricing terms before you create the direct delivery.</span></span>  
9. <span data-ttu-id="224b8-121">حدد "نعم" في الحقل "تضمين الكل".</span><span class="sxs-lookup"><span data-stu-id="224b8-121">Select Yes in the Include all field.</span></span>
    * <span data-ttu-id="224b8-122">إذا أردتَ إنشاء تسليم مباشر لمجموعة فرعية فقط من بنود أوامر المبيعات، فحدد هذه البنود بشكل فردي.</span><span class="sxs-lookup"><span data-stu-id="224b8-122">If you want to generate a direct delivery for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="224b8-123">قد يتم ملء الحقل "حساب المورد" أو قد لا يتم ملؤه بالفعل برقم مورد.</span><span class="sxs-lookup"><span data-stu-id="224b8-123">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="224b8-124">إذا تم إعداد المورد الافتراضي للمنتج (بتغطية الصنف المقترن) سيتم نسخ المورد هذا للبند.</span><span class="sxs-lookup"><span data-stu-id="224b8-124">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied to the line.</span></span> <span data-ttu-id="224b8-125">وإلا، يجب إدخال مورد يدوياً.</span><span class="sxs-lookup"><span data-stu-id="224b8-125">Otherwise, you must enter a vendor manually.</span></span> <span data-ttu-id="224b8-126">في هذا المثال، سنحدد موردًا جديدًا في الخطوة التالية، حتى إذا تم ملء أحد الموردين بالفعل.</span><span class="sxs-lookup"><span data-stu-id="224b8-126">In this example, we’ll select a new vendor in the next step, even if one is already populated.</span></span>   
10. <span data-ttu-id="224b8-127">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="224b8-127">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="224b8-128">إذا كنت تستخدم USMF، يمكنك تحديد الحساب 1001.</span><span class="sxs-lookup"><span data-stu-id="224b8-128">If you’re using USMF, you can select account 1001.</span></span>  
11. <span data-ttu-id="224b8-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="224b8-129">Click OK.</span></span>
    * <span data-ttu-id="224b8-130">تُعلمك هذه الرسالة بأنه تم إنشاء أمر الشراء الآن.</span><span class="sxs-lookup"><span data-stu-id="224b8-130">The message informs you that the purchase order has now been created.</span></span>   
12. <span data-ttu-id="224b8-131">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="224b8-131">Expand the Line details section.</span></span>
13. <span data-ttu-id="224b8-132">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="224b8-132">Click the Delivery tab.</span></span>
    * <span data-ttu-id="224b8-133">سيتم الآن تعيين الحقل "التسليم المباشر" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="224b8-133">The Direct delivery field is now set to Yes.</span></span>  
    * <span data-ttu-id="224b8-134">توضح حالة "التسليم المباشر" أمر الشراء الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="224b8-134">The Direct delivery status shows the Purchase order created.</span></span>   
14. <span data-ttu-id="224b8-135">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="224b8-135">On the Action Pane, click General.</span></span>
15. <span data-ttu-id="224b8-136">انقر فوق "الأوامر المرتبطة".</span><span class="sxs-lookup"><span data-stu-id="224b8-136">Click Related orders.</span></span>
16. <span data-ttu-id="224b8-137">انقر للمتابعة إلى الارتباط الموجود في الحقل "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="224b8-137">Click to follow the link in the Purchase order field.</span></span>
17. <span data-ttu-id="224b8-138">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="224b8-138">Expand the Line details section.</span></span>
18. <span data-ttu-id="224b8-139">انقر فوق علامة التبويب "العنوان".</span><span class="sxs-lookup"><span data-stu-id="224b8-139">Click the Address tab.</span></span>
    * <span data-ttu-id="224b8-140">لاحظ أن عنوان التسليم لبند أمر الشراء هذا هو عنوان التسليم للعميل وليس عنوان الشركة.</span><span class="sxs-lookup"><span data-stu-id="224b8-140">Note that the delivery address for this purchase order line is the customer's delivery address and not your company's address.</span></span>  
    * <span data-ttu-id="224b8-141">إذا قمت بتغيير عنوان التسليم إما في بند أمر المبيعات أو بند أمر المبيعات الأصل، فسيتم تحديث العنوان ببند الأمر الموافق.</span><span class="sxs-lookup"><span data-stu-id="224b8-141">If you change the delivery address on either the purchase order line or the originating sales order line, the address on the corresponding order line will be automatically updated.</span></span>  
19. <span data-ttu-id="224b8-142">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="224b8-142">Click the Delivery tab.</span></span>
    * <span data-ttu-id="224b8-143">وعلى غرار بند أمر المبيعات، يتم تعيين نوع بند أمر الشراء المقترن أيضًا على التسليم المباشر.</span><span class="sxs-lookup"><span data-stu-id="224b8-143">Like the sales order line, the associated purchase order line type is also set to Direct delivery.</span></span>  
    * <span data-ttu-id="224b8-144">يتم تعيين تاريخ التسليم لبند أمر الشراء وتاريخ التسليم المؤكد على تاريخ الاستلام المطلوب وتاريخ الاستلام المؤكد لأمر المبيعات الأصلي بالترتيب.</span><span class="sxs-lookup"><span data-stu-id="224b8-144">The purchase order line's Delivery  date and the Confirmed delivery date are set to the Requested receipt date and Confirmed receipt date of the originating sales order line respectively.</span></span>   
    * <span data-ttu-id="224b8-145">إذا قمت بتحديث أي من هذه التواريخ إما ببند الشراء أو بند المبيعات، سيتم تحديث التواريخ بالبند الموافق تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="224b8-145">If you update any of these dates on either the purchase line or the sales line, the dates on the corresponding order will be automatically updated.</span></span>     
    * <span data-ttu-id="224b8-146">ويتم ربط أمر الشراء الذي تم تعيينه لتسليم البضائع مباشرة للعميل بأمر المبيعات الأصلي عن طريق اقتران خاص.</span><span class="sxs-lookup"><span data-stu-id="224b8-146">The purchase order that is set to deliver goods directly the customer is linked to the originating sales order by means of a special association.</span></span> <span data-ttu-id="224b8-147">يفرض هذا الاقتران القاعدة التي تحدد أنه لا يمكن تنفيذ تحديث إيصال التعبئة لأمر المبيعات من أمر المبيعات نفسه ويجب تنفيذه باستخدام أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="224b8-147">This association imposes the rule that the packing slip update of the sales order can't be done from the sales order itself and must be done by using the purchase order.</span></span> <span data-ttu-id="224b8-148">ومع ذلك، يجب تنفيذ فوترة العميل من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="224b8-148">However, customer invoicing must be carried out from the sales order.</span></span>  
20. <span data-ttu-id="224b8-149">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="224b8-149">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="224b8-150">انقر فوق"تأكيد".</span><span class="sxs-lookup"><span data-stu-id="224b8-150">Click Confirmation.</span></span>
22. <span data-ttu-id="224b8-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="224b8-151">Click OK.</span></span>
23. <span data-ttu-id="224b8-152">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="224b8-152">On the Action Pane, click Receive.</span></span>
24. <span data-ttu-id="224b8-153">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="224b8-153">Click Product receipt.</span></span>
25. <span data-ttu-id="224b8-154">في الحقل "إيصال استلام المنتجات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="224b8-154">In the Product receipt field, type a value.</span></span>
26. <span data-ttu-id="224b8-155">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="224b8-155">Click OK.</span></span>
27. <span data-ttu-id="224b8-156">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="224b8-156">On the Action Pane, click General.</span></span>
28. <span data-ttu-id="224b8-157">انقر فوق "الأوامر المرتبطة".</span><span class="sxs-lookup"><span data-stu-id="224b8-157">Click Related orders.</span></span>
29. <span data-ttu-id="224b8-158">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="224b8-158">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="224b8-159">بعد أن يتم تحديث أمر الشراء باعتباره "تم استلامه" أو بعبارة أخرى، بعد أن يشحن المورد البضائع إلى عنوان العميل، يتم تحديث حالة أمر المبيعات الأصلي تلقائياً إلى "تم تسليمه".</span><span class="sxs-lookup"><span data-stu-id="224b8-159">After the purchase order has been updated as received, or in other words, after the vendor has shipped the goods to your customer's address, the status of the originating sales order is automatically updated to Delivered.</span></span>  
    * <span data-ttu-id="224b8-160">ويمكن الآن فوترة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="224b8-160">The sales order can now be invoiced.</span></span>    
30. <span data-ttu-id="224b8-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="224b8-161">Click OK.</span></span>
31. <span data-ttu-id="224b8-162">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="224b8-162">Close the page.</span></span>
32. <span data-ttu-id="224b8-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="224b8-163">Click OK.</span></span>

## <a name="create-direct-deliveries-from-the-workbench"></a><span data-ttu-id="224b8-164">إنشاء عمليات تسليم مباشرة من منضدة العمل</span><span class="sxs-lookup"><span data-stu-id="224b8-164">Create direct deliveries from the workbench</span></span>
1. <span data-ttu-id="224b8-165">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="224b8-165">Close the page.</span></span>
2. <span data-ttu-id="224b8-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="224b8-166">Close the page.</span></span>
3. <span data-ttu-id="224b8-167">انتقل إلى "كافة أوامر المبيعات‬".</span><span class="sxs-lookup"><span data-stu-id="224b8-167">Go to All sales orders.</span></span>
4. <span data-ttu-id="224b8-168">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="224b8-168">Click New.</span></span>
5. <span data-ttu-id="224b8-169">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="224b8-169">In the Customer account field, enter or select a value.</span></span>
6. <span data-ttu-id="224b8-170">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="224b8-170">Click OK.</span></span>
7. <span data-ttu-id="224b8-171">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="224b8-171">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="224b8-172">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="224b8-172">Expand the Line details section.</span></span>
9. <span data-ttu-id="224b8-173">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="224b8-173">Click the Delivery tab.</span></span>
    * <span data-ttu-id="224b8-174">بدلاً من إنشاء تسليم مباشر كجزء من معالجة أمر المبيعات كما هو موضح في الإجراء السابق، يمكنك اختيار تسليم هذه المهمة إلى أخصائي شراء.</span><span class="sxs-lookup"><span data-stu-id="224b8-174">Instead of creating a direct delivery as part of the sales order processing as in the previous procedure, you can choose to hand over this task to a purchasing professional.</span></span> <span data-ttu-id="224b8-175">لتضمين بند أمر المبيعات في عملية معالجة التسليم المباشر، يجب تمييز البند للتسليم المباشر.</span><span class="sxs-lookup"><span data-stu-id="224b8-175">To include the sales order line in the direct delivery handling process, you must mark the line for direct delivery.</span></span>  
10. <span data-ttu-id="224b8-176">حدد "نعم" في الحقل "التسليم المباشر".</span><span class="sxs-lookup"><span data-stu-id="224b8-176">Select Yes in the Direct delivery field.</span></span>
    *   <span data-ttu-id="224b8-177">إذا كان الصنف قد تم إعداده بالفعل للتسليم المباشر بشكل افتراضي، سيتم تعيين الحقل تلقائياً على "نعم" في إدخال بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="224b8-177">If the item has already been set up for direct delivery by default, the field will automatically be set to Yes at the order line entry.</span></span> <span data-ttu-id="224b8-178">يمكنك إعداد صنف للتسليم المباشر في أصل منتج تم إصداره عن طريق تعيين خيار التسليم المباشر على "نعم" وتحديد مستودع تسليم مباشر.</span><span class="sxs-lookup"><span data-stu-id="224b8-178">You can set up an item for direct delivery on the Released product's master by setting the Direct delivery option to Yes and selecting a default Direct delivery warehouse.</span></span>  
    * <span data-ttu-id="224b8-179">نظرًا لأنه لم يتم إنشاء أمر الشراء بعد، سيتم تعيين حالة التسليم المباشر على "سيتم تسليمه بشكل مباشر".</span><span class="sxs-lookup"><span data-stu-id="224b8-179">Because the purchase order has not yet been created, the Direct delivery status is set to To be direct delivered.</span></span>   
11. <span data-ttu-id="224b8-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="224b8-180">Close the page.</span></span>
12. <span data-ttu-id="224b8-181">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="224b8-181">Close the page.</span></span>
13. <span data-ttu-id="224b8-182">انتقل إلى "التسليم المباشر".</span><span class="sxs-lookup"><span data-stu-id="224b8-182">Go to Direct delivery.</span></span>
    * <span data-ttu-id="224b8-183">تعمل صفحة التسليم المباشر كمنضدة عمل توفر نظرة عامة لوكيل الشراء بجميع بنود أوامر المبيعات التي سيتم تسليمها بشكل مباشر وتتيح له إنشاء أوامر الشراء المعنية.</span><span class="sxs-lookup"><span data-stu-id="224b8-183">The Direct delivery page acts as a workbench that provides the purchasing agent with an overview of all the sales order lines that are to be direct delivered and it allows them to create the respective purchase orders.</span></span> <span data-ttu-id="224b8-184">علاوة على ذلك، يمكنها عرض أوامر التسليم المفتوحة والأوامر المؤكدة في علامتي التبويب التأكيد والتسليم.</span><span class="sxs-lookup"><span data-stu-id="224b8-184">In addition, they can view the open direct delivery orders and the confirmed orders on the Confirmation and Delivery tabs.</span></span>   
14. <span data-ttu-id="224b8-185">انقر فوق "إنشاء تسليم مباشر".</span><span class="sxs-lookup"><span data-stu-id="224b8-185">Click Create direct delivery.</span></span>
15. <span data-ttu-id="224b8-186">انقر فوق علامة التبويب "التأكيد".</span><span class="sxs-lookup"><span data-stu-id="224b8-186">Click the Confirmation tab.</span></span>
    * <span data-ttu-id="224b8-187">بعد إنشاء أمر تسليم مباشر، يتم نقله تلقائيًا إلى علامة التبويب "تأكيد". يمكنك اختيار تأكيد الأمر مباشرة من هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="224b8-187">After you have created a direct delivery order, it automatically moved to the Confirmation tab. You can choose to confirm the order directly from this page.</span></span> <span data-ttu-id="224b8-188">عندما يتم تأكيد الشراء, ستنتقل الصفحة تلقائياً إلى علامة التبويب "التسليم"، التي يمكنك تسجيل الاستلام منها.</span><span class="sxs-lookup"><span data-stu-id="224b8-188">When the purchase is confirmed, it will automatically move to the Delivery tab, from which you can registered its receipt.</span></span>  


