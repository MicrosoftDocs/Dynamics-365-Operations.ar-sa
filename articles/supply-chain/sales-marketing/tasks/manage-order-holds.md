---
title: إدارة عمليات تعليق الأمر
description: يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad19ff166c15748b7bbb4b82ef71dbf3e1e8ebd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323952"
---
# <a name="manage-order-holds"></a><span data-ttu-id="6e8c8-103">إدارة عمليات تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="6e8c8-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e8c8-104">يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="6e8c8-105">قد يتم وضع أمر قيد الانتظار لأسباب عدة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="6e8c8-106">على سبيل المثال، قد تضع أمر قيد الانتظار حتى يمكن التحقق من أسلوب الدفع أو عنوان عميل أو حتى يقوم مدير بمراجعة حد الائتمان الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="6e8c8-107">بينما يكون الأمر قيد الانتظار، لا يمكن معالجته بواسطة المستودع لشحنه.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="6e8c8-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="6e8c8-109">إعداد تعليقات الأمر</span><span class="sxs-lookup"><span data-stu-id="6e8c8-109">Set up order holds</span></span>
1. <span data-ttu-id="6e8c8-110">انتقل إلى المبيعات والتسويق > الإعداد > أوامر المبيعات > أكواد تعليق الأمر‬.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="6e8c8-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-111">Click New.</span></span>
3. <span data-ttu-id="6e8c8-112">في الحقل "كود التعليق‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="6e8c8-113">على سبيل المثال، اكتب "استدعاء".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="6e8c8-114">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6e8c8-115">على سبيل المثال، تعليق أمر قيد انتظار استدعاء العميل.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="6e8c8-116">بشكل اختياري، حدد خانة الاختيار "إزالة الحجوزات‬" لإزالة أي حجوزات‬ فعلية من لأمر عند إضافة كود التعليق هذا.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="6e8c8-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="6e8c8-118">وضع أمر قيد الانتظار</span><span class="sxs-lookup"><span data-stu-id="6e8c8-118">Place order on hold</span></span>
1. <span data-ttu-id="6e8c8-119">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6e8c8-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-120">Click New.</span></span>
3. <span data-ttu-id="6e8c8-121">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="6e8c8-122">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-122">Click OK.</span></span>
5. <span data-ttu-id="6e8c8-123">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="6e8c8-124">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="6e8c8-125">في جزء "الإجراءات"، انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="6e8c8-126">انقر فوق "تعليقات الأمر‬".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-126">Click Order holds.</span></span>
9. <span data-ttu-id="6e8c8-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-127">Click New.</span></span>
10. <span data-ttu-id="6e8c8-128">في حقل "كود التعليق"، حدد الكود الذي أنشأته في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="6e8c8-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-129">Click Save.</span></span>
12. <span data-ttu-id="6e8c8-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-130">Close the page.</span></span>
13. <span data-ttu-id="6e8c8-131">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="6e8c8-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e8c8-133">تتضمن الأوامر الموضوعة قيد الانتظار حاليًا الحقلين "‏‫لا تقم بالمعالجة‬ "و"تعليق‬" وقد تم تعليمهما.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="6e8c8-134">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="6e8c8-135">إدارة عمليات تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="6e8c8-135">Manage order holds</span></span>
1. <span data-ttu-id="6e8c8-136">انتقل إلى المبيعات والتسويق > أوامر المبيعات > الأوامر المفتوحة > تعليقات الأمر‬.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="6e8c8-137">تعمل الصفحة "تعليقات الأمر‬" كمنضدة عمل حيث يمكنك الحصول على نظرة عامة على كافة التعليقات الحالية وتلك التي تمت معالجتها، وحيث يمكنك معالجتها كأوامر مبيعات مقترنة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="6e8c8-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6e8c8-139">في جزء الإجراءات، انقر فوق "السحب المعلق".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="6e8c8-140">انقر فوق "سحب".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-140">Click Check out.</span></span>
5. <span data-ttu-id="6e8c8-141">في القائمة، قم بإلغاء علامة الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="6e8c8-142">يعرض الآن حقل "السحب إلى" معرف المستخدم الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="6e8c8-143">انقر فوق "مسح السحب".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="6e8c8-144">في جزء الإجراءات، انقر فوق "مسح التعليق".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="6e8c8-145">عندما تصبح جاهزًا لإزالة تعليق الأمر والسماح للأمر بالمتابعة إلى خطوة التنفيذ التالية، يجب مسح التعليق.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="6e8c8-146">إذا لم يتطلب الأمر إجراء أي تغيير، فيمكنك تشغيل الإجراء "مسح التعليقات‬".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="6e8c8-147">ومع ذلك، يمكنك استخدام الإجراء "مسح وتعديل‬"، إذا كان الأمر بحاجة إلى تحديث عند مسح التعليق.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="6e8c8-148">ينطبق الإجراء "مسح وإرسال" فقط عندما تستخدم وظيفة مركز الاتصال‬.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="6e8c8-149">انقر فوق "مسح التعليقات‬".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-149">Click Clear holds.</span></span>
    * <span data-ttu-id="6e8c8-150">تم الآن مسح التعليق من الأمر وتمت إزالته من قائمة التعليقات النشطة.</span><span class="sxs-lookup"><span data-stu-id="6e8c8-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="6e8c8-151">لعرض كافة التعليقات أو مجموعتها الفرعية وفقًا لحالة معينة، قم بتغيير القيمة الموجودة في الحقل "إظهار".</span><span class="sxs-lookup"><span data-stu-id="6e8c8-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

