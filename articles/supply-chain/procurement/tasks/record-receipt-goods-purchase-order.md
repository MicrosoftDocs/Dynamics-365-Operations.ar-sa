--- 
title: "تسجيل استلام البضائع في أمر الشراء"
description: "يوضح هذا الإجراء كيفية تسجيل إيصال استلام البضائع مباشرة على أمر شراء."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="a9e80-103">تسجيل استلام البضائع في أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="a9e80-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9e80-104">يوضح هذا الإجراء كيفية تسجيل إيصال استلام البضائع مباشرة على أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="a9e80-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="a9e80-105">من الممكن أيضًا تسجيل إيصال استلام المنتج في المستودع، ثم تسجيله على أمر الشراء في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="a9e80-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="a9e80-106">يقوم عادةً وكيل الشراء أو منسق الحسابات الدائنة بتنفيذ هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="a9e80-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="a9e80-107">يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="a9e80-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="a9e80-108">يتضمن المثال الخطوات المتعلقة بإنشاء أمر شراء بسيط بحيث يمكنك تشغيل الإجراء كدليل مهمة.</span><span class="sxs-lookup"><span data-stu-id="a9e80-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="a9e80-109">إذا كنت تستخدم الإجراء على بياناتك الخاصة، فيمكنك البدء بالمهمة الفرعية وهي تسجيل استلام البضائع.</span><span class="sxs-lookup"><span data-stu-id="a9e80-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="a9e80-110">إعداد أمر شراء جديد لاستلام البضائع</span><span class="sxs-lookup"><span data-stu-id="a9e80-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="a9e80-111">انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a9e80-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a9e80-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a9e80-112">Click New.</span></span>
3. <span data-ttu-id="a9e80-113">في حقل "حساب المورّد‬"، أدخل "US-101".</span><span class="sxs-lookup"><span data-stu-id="a9e80-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="a9e80-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a9e80-114">Click OK.</span></span>
5. <span data-ttu-id="a9e80-115">في الحقل "رقم الصنف"، أدخل "M0001".</span><span class="sxs-lookup"><span data-stu-id="a9e80-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="a9e80-116">في حقل "الكمية"، أدخل ''5".</span><span class="sxs-lookup"><span data-stu-id="a9e80-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="a9e80-117">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="a9e80-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="a9e80-118">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="a9e80-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="a9e80-119">تسجيل استلام البضائع</span><span class="sxs-lookup"><span data-stu-id="a9e80-119">Record receipt of goods</span></span>
1. <span data-ttu-id="a9e80-120">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="a9e80-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="a9e80-121">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="a9e80-121">Click Product receipt.</span></span>
    * <span data-ttu-id="a9e80-122">يسمح لك حقل "الكمية" بتحديد خيارات مختلفة للكمية التي تريد استلامها.</span><span class="sxs-lookup"><span data-stu-id="a9e80-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="a9e80-123">على سبيل المثال، إذا سبق أن تم تسجيل كمية في المستودع، فيمكنك تحديد "الكمية المسجلة".</span><span class="sxs-lookup"><span data-stu-id="a9e80-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="a9e80-124">لهذا المثال، استخدم قيمة "الكمية المطلوبة".</span><span class="sxs-lookup"><span data-stu-id="a9e80-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="a9e80-125">في الحقل "إيصال استلام المنتجات"، اكتب أي قيمة.</span><span class="sxs-lookup"><span data-stu-id="a9e80-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="a9e80-126">يتم استخدام هذا الحقل لإدخال مرجع سيتم استخدامه كإيصال لدفتر يومية إيصال استلام المنتج.</span><span class="sxs-lookup"><span data-stu-id="a9e80-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="a9e80-127">قم بتوسيع القسم "البنود".</span><span class="sxs-lookup"><span data-stu-id="a9e80-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="a9e80-128">تعيين الكمية إلى "4".</span><span class="sxs-lookup"><span data-stu-id="a9e80-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="a9e80-129">هنا يمكنك أن تحدد يدويًا الكمية التي يتم استلامها لكل بند في الأمر.</span><span class="sxs-lookup"><span data-stu-id="a9e80-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="a9e80-130">قم بطي مقطع "البنود".</span><span class="sxs-lookup"><span data-stu-id="a9e80-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="a9e80-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a9e80-131">Click OK.</span></span>
    * <span data-ttu-id="a9e80-132">تم الآن تسجيل البضائع على أنها مستلمة على أمر إرجاع الشراء، وتم إنشاء دفتر يومية إيصال استلام المنتجات كمستند لإظهار هذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="a9e80-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="a9e80-133">يمكنك استخدام إجراء إيصال استلام المنتجات لمراجعة دفاتر اليومية التي تم إنشاؤها مع أمر الشراء، والاطلاع على المنتجات التي تم استلامها وتاريخ الاستلام.</span><span class="sxs-lookup"><span data-stu-id="a9e80-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


