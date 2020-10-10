---
title: إدارة عمليات تعليق الأمر
description: يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb3c6941af132f9ea1bf9f52f94cd6acc008d6c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830017"
---
# <a name="manage-order-holds"></a><span data-ttu-id="e7efe-103">إدارة عمليات تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="e7efe-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7efe-104">يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر.</span><span class="sxs-lookup"><span data-stu-id="e7efe-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="e7efe-105">قد يتم وضع أمر قيد الانتظار لأسباب عدة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="e7efe-106">على سبيل المثال، قد تضع أمر قيد الانتظار حتى يمكن التحقق من أسلوب الدفع أو عنوان عميل أو حتى يقوم مدير بمراجعة حد الائتمان الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="e7efe-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="e7efe-107">بينما يكون الأمر قيد الانتظار، لا يمكن معالجته بواسطة المستودع لشحنه.</span><span class="sxs-lookup"><span data-stu-id="e7efe-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="e7efe-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="e7efe-109">إعداد تعليقات الأمر</span><span class="sxs-lookup"><span data-stu-id="e7efe-109">Set up order holds</span></span>
1. <span data-ttu-id="e7efe-110">انتقل إلى **جزء التنقل > الوحدات > المبيعات والتسويق > إعداد > أوامر المبيعات > أكواد تعليق الأمر**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="e7efe-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-111">Click **New**.</span></span>
3. <span data-ttu-id="e7efe-112">في حقل **كود التعليق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="e7efe-113">على سبيل المثال، اكتب "استدعاء".</span><span class="sxs-lookup"><span data-stu-id="e7efe-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="e7efe-114">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="e7efe-115">على سبيل المثال، تعليق أمر قيد انتظار استدعاء العميل.</span><span class="sxs-lookup"><span data-stu-id="e7efe-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="e7efe-116">بشكل اختياري، حدد خانة الاختيار **إزالة الحجوزات‬** لإزالة أي حجوزات‬ فعلية من الأمر عند إضافة كود التعليق هذا.</span><span class="sxs-lookup"><span data-stu-id="e7efe-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="e7efe-117">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="e7efe-118">وضع أمر قيد الانتظار</span><span class="sxs-lookup"><span data-stu-id="e7efe-118">Place order on hold</span></span>
1. <span data-ttu-id="e7efe-119">انتقل إلى **جزء التنقل > الوحدات > المبيعات والتسويق > أوامر المبيعات > جميع أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="e7efe-120">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-120">Click **New**.</span></span>
3. <span data-ttu-id="e7efe-121">أدخل قيمة أو حددها في حقل **حساب العميل**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="e7efe-122">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-122">Click **OK**.</span></span>
5. <span data-ttu-id="e7efe-123">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e7efe-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="e7efe-124">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e7efe-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="e7efe-125">في **جزء الإجراءات**، انقر فوق **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="e7efe-126">انقر فوق **تعليقات الأمر**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="e7efe-127">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-127">Click **New**.</span></span>
10. <span data-ttu-id="e7efe-128">في حقل **كود التعليق**، حدد الكود الذي أنشأته في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="e7efe-129">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-129">Click **Save**.</span></span>
12. <span data-ttu-id="e7efe-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-130">Close the page.</span></span>
13. <span data-ttu-id="e7efe-131">انتقل إلى **المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات**. </span><span class="sxs-lookup"><span data-stu-id="e7efe-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="e7efe-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7efe-132">In the list, mark the selected row.</span></span> <span data-ttu-id="e7efe-133">تتضمن الأوامر الموضوعة قيد الانتظار حاليًا الحقلين "‏‫لا تقم بالمعالجة‬ "و"تعليق‬" وقد تم تعليمهما.</span><span class="sxs-lookup"><span data-stu-id="e7efe-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="e7efe-134">في جزء الإجراءات، انقر فوق **انتقاء وتعبئة**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="e7efe-135">إدارة عمليات تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="e7efe-135">Manage order holds</span></span>
1. <span data-ttu-id="e7efe-136">انتقل إلى **المبيعات والتسويق > أوامر المبيعات > الأوامر المفتوحة > تعليقات الأمر**. </span><span class="sxs-lookup"><span data-stu-id="e7efe-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="e7efe-137">تعمل الصفحة **تعليقات الأمر‬** كمنضدة عمل حيث يمكنك الحصول على نظرة عامة على كافة التعليقات الحالية وتلك التي تمت معالجتها، وحيث يمكنك معالجتها كأوامر مبيعات مقترنة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="e7efe-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7efe-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e7efe-139">في **جزء الإجراءات**، انقر فوق **السحب المعلق**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="e7efe-140">انقر فوق **سحب**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-140">Click **Check out**.</span></span>
5. <span data-ttu-id="e7efe-141">في القائمة، قم بإلغاء علامة الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7efe-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="e7efe-142">يعرض الآن حقل **السحب إلى** معرف المستخدم الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e7efe-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="e7efe-143">انقر فوق **مسح السحب**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="e7efe-144">في **جزء الإجراءات**، انقر فوق **مسح التعليق**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="e7efe-145">عندما تصبح جاهزًا لإزالة تعليق الأمر والسماح للأمر بالمتابعة إلى خطوة التنفيذ التالية، يجب مسح التعليق.</span><span class="sxs-lookup"><span data-stu-id="e7efe-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="e7efe-146">إذا لم يتطلب الأمر إجراء أي تغيير، فيمكنك تشغيل الإجراء "مسح التعليقات‬".</span><span class="sxs-lookup"><span data-stu-id="e7efe-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="e7efe-147">ومع ذلك، يمكنك استخدام الإجراء "مسح وتعديل‬"، إذا كان الأمر بحاجة إلى تحديث عند مسح التعليق.</span><span class="sxs-lookup"><span data-stu-id="e7efe-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="e7efe-148">ينطبق الإجراء **مسح وإرسال** فقط عندما تستخدم وظيفة مركز الاتصال‬.</span><span class="sxs-lookup"><span data-stu-id="e7efe-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="e7efe-149">انقر فوق **مسح التعليقات‬**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-149">Click **Clear holds**.</span></span> <span data-ttu-id="e7efe-150">تم الآن مسح التعليق من الأمر وتمت إزالته من قائمة التعليقات النشطة.</span><span class="sxs-lookup"><span data-stu-id="e7efe-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="e7efe-151">لعرض كافة التعليقات أو مجموعتها الفرعية وفقًا لحالة معينة، قم بتغيير القيمة الموجودة في الحقل "إظهار".</span><span class="sxs-lookup"><span data-stu-id="e7efe-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

