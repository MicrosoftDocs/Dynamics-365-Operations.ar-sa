--- 
title: "إدارة عمليات تعليق الأمر"
description: "يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3edb8d2fe0fda6634bc2edb8e3bafc5a60344b7a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="manage-order-holds"></a><span data-ttu-id="3c804-103">إدارة عمليات تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="3c804-103">Manage order holds</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c804-104">يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر.</span><span class="sxs-lookup"><span data-stu-id="3c804-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="3c804-105">قد يتم وضع أمر قيد الانتظار لأسباب عدة.</span><span class="sxs-lookup"><span data-stu-id="3c804-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="3c804-106">على سبيل المثال، قد تضع أمر قيد الانتظار حتى يمكن التحقق من أسلوب الدفع أو عنوان عميل أو حتى يقوم مدير بمراجعة حد الائتمان الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="3c804-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="3c804-107">بينما يكون الأمر قيد الانتظار، لا يمكن معالجته بواسطة المستودع لشحنه.</span><span class="sxs-lookup"><span data-stu-id="3c804-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="3c804-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="3c804-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="3c804-109">إعداد تعليقات الأمر</span><span class="sxs-lookup"><span data-stu-id="3c804-109">Set up order holds</span></span>
1. <span data-ttu-id="3c804-110">انتقل إلى المبيعات والتسويق > الإعداد > أوامر المبيعات > أكواد تعليق الأمر‬.</span><span class="sxs-lookup"><span data-stu-id="3c804-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="3c804-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c804-111">Click New.</span></span>
3. <span data-ttu-id="3c804-112">في الحقل "كود التعليق‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c804-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="3c804-113">على سبيل المثال، اكتب "استدعاء".</span><span class="sxs-lookup"><span data-stu-id="3c804-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="3c804-114">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c804-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3c804-115">على سبيل المثال، تعليق أمر قيد انتظار استدعاء العميل.</span><span class="sxs-lookup"><span data-stu-id="3c804-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="3c804-116">بشكل اختياري، حدد خانة الاختيار "إزالة الحجوزات‬" لإزالة أي حجوزات‬ فعلية من لأمر عند إضافة كود التعليق هذا.</span><span class="sxs-lookup"><span data-stu-id="3c804-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="3c804-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c804-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="3c804-118">وضع أمر قيد الانتظار</span><span class="sxs-lookup"><span data-stu-id="3c804-118">Place order on hold</span></span>
1. <span data-ttu-id="3c804-119">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3c804-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="3c804-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c804-120">Click New.</span></span>
3. <span data-ttu-id="3c804-121">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c804-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="3c804-122">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="3c804-122">Click OK.</span></span>
5. <span data-ttu-id="3c804-123">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c804-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="3c804-124">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3c804-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="3c804-125">في جزء "الإجراءات"، انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="3c804-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="3c804-126">انقر فوق "تعليقات الأمر‬".</span><span class="sxs-lookup"><span data-stu-id="3c804-126">Click Order holds.</span></span>
9. <span data-ttu-id="3c804-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c804-127">Click New.</span></span>
10. <span data-ttu-id="3c804-128">في حقل "كود التعليق"، حدد الكود الذي أنشأته في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="3c804-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="3c804-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c804-129">Click Save.</span></span>
12. <span data-ttu-id="3c804-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3c804-130">Close the page.</span></span>
13. <span data-ttu-id="3c804-131">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3c804-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="3c804-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c804-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3c804-133">تتضمن الأوامر الموضوعة قيد الانتظار حاليًا الحقلين "‏‫لا تقم بالمعالجة‬ "و"تعليق‬" وقد تم تعليمهما.</span><span class="sxs-lookup"><span data-stu-id="3c804-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="3c804-134">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="3c804-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="3c804-135">إدارة عمليات تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="3c804-135">Manage order holds</span></span>
1. <span data-ttu-id="3c804-136">انتقل إلى المبيعات والتسويق > أوامر المبيعات > الأوامر المفتوحة > تعليقات الأمر‬.</span><span class="sxs-lookup"><span data-stu-id="3c804-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="3c804-137">تعمل الصفحة "تعليقات الأمر‬" كمنضدة عمل حيث يمكنك الحصول على نظرة عامة على كافة التعليقات الحالية وتلك التي تمت معالجتها، وحيث يمكنك معالجتها كأوامر مبيعات مقترنة.</span><span class="sxs-lookup"><span data-stu-id="3c804-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="3c804-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c804-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3c804-139">في جزء الإجراءات، انقر فوق "السحب المعلق".</span><span class="sxs-lookup"><span data-stu-id="3c804-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="3c804-140">انقر فوق "سحب".</span><span class="sxs-lookup"><span data-stu-id="3c804-140">Click Check out.</span></span>
5. <span data-ttu-id="3c804-141">في القائمة، قم بإلغاء علامة الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c804-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="3c804-142">يعرض الآن حقل "السحب إلى" معرف المستخدم الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3c804-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="3c804-143">انقر فوق "مسح السحب".</span><span class="sxs-lookup"><span data-stu-id="3c804-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="3c804-144">في جزء الإجراءات، انقر فوق "مسح التعليق".</span><span class="sxs-lookup"><span data-stu-id="3c804-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="3c804-145">عندما تصبح جاهزًا لإزالة تعليق الأمر والسماح للأمر بالمتابعة إلى خطوة التنفيذ التالية، يجب مسح التعليق.</span><span class="sxs-lookup"><span data-stu-id="3c804-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="3c804-146">إذا لم يتطلب الأمر إجراء أي تغيير، فيمكنك تشغيل الإجراء "مسح التعليقات‬".</span><span class="sxs-lookup"><span data-stu-id="3c804-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="3c804-147">ومع ذلك، يمكنك استخدام الإجراء "مسح وتعديل‬"، إذا كان الأمر بحاجة إلى تحديث عند مسح التعليق.</span><span class="sxs-lookup"><span data-stu-id="3c804-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="3c804-148">ينطبق الإجراء "مسح وإرسال" فقط عندما تستخدم وظيفة مركز الاتصال‬.</span><span class="sxs-lookup"><span data-stu-id="3c804-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="3c804-149">انقر فوق "مسح التعليقات‬".</span><span class="sxs-lookup"><span data-stu-id="3c804-149">Click Clear holds.</span></span>
    * <span data-ttu-id="3c804-150">تم الآن مسح التعليق من الأمر وتمت إزالته من قائمة التعليقات النشطة.</span><span class="sxs-lookup"><span data-stu-id="3c804-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="3c804-151">لعرض كافة التعليقات أو مجموعتها الفرعية وفقًا لحالة معينة، قم بتغيير القيمة الموجودة في الحقل "إظهار".</span><span class="sxs-lookup"><span data-stu-id="3c804-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

