---
title: تسجيل استلام البضائع في أمر الشراء
description: يوضح هذا الموضوع كيفية تسجيل استلام البضائع مباشرة على أمر شراء.
author: FrankDahl
manager: AnnBe
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e81bb3fe95326636c28885d4decad69f841e3db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843999"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="e01b7-103">تسجيل استلام البضائع في أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="e01b7-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e01b7-104">يوضح هذا الموضوع كيفية تسجيل استلام البضائع مباشرة على أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="e01b7-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="e01b7-105">من الممكن أيضًا تسجيل إيصال استلام المنتج في المستودع، ثم تسجيله على أمر الشراء في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="e01b7-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="e01b7-106">يقوم عادةً وكيل الشراء أو منسق الحسابات الدائنة بتنفيذ هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="e01b7-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="e01b7-107">يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="e01b7-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="e01b7-108">يتضمن المثال الخطوات المتعلقة بإنشاء أمر شراء بسيط بحيث يمكنك تشغيل الإجراء كدليل مهمة.</span><span class="sxs-lookup"><span data-stu-id="e01b7-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="e01b7-109">إذا كنت تستخدم الإجراء على بياناتك الخاصة، فيمكنك البدء بالمهمة الفرعية وهي **تسجيل استلام البضائع**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="e01b7-110">إعداد أمر شراء جديد لاستلام البضائع</span><span class="sxs-lookup"><span data-stu-id="e01b7-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="e01b7-111">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد > أوامر الشراء > جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="e01b7-112">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-112">Select **New**.</span></span>
3. <span data-ttu-id="e01b7-113">في حقل **حساب المورّد‬**، أدخل `US-101`.</span><span class="sxs-lookup"><span data-stu-id="e01b7-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="e01b7-114">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-114">Select **OK**.</span></span>
5. <span data-ttu-id="e01b7-115">في الحقل **رقم الصنف**، أدخل `M0001`.</span><span class="sxs-lookup"><span data-stu-id="e01b7-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="e01b7-116">في حقل **الكمية**، أدخل `5`.</span><span class="sxs-lookup"><span data-stu-id="e01b7-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="e01b7-117">في جزء الإجراءات، انقر فوق **شراء**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="e01b7-118">حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="e01b7-119">تسجيل استلام البضائع</span><span class="sxs-lookup"><span data-stu-id="e01b7-119">Record receipt of goods</span></span>
1. <span data-ttu-id="e01b7-120">في جزء الإجراءات، حدد **استلام**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="e01b7-121">حدد **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-121">Select **Product receipt**.</span></span> <span data-ttu-id="e01b7-122">يسمح لك حقل **الكمية** بتحديد خيارات مختلفة للكمية التي تريد استلامها.</span><span class="sxs-lookup"><span data-stu-id="e01b7-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="e01b7-123">على سبيل المثال، إذا سبق أن تم تسجيل كمية في المستودع، فيمكنك تحديد **الكمية المسجلة**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="e01b7-124">لهذا المثال، استخدم قيمة **الكمية المطلوبة**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="e01b7-125">توسيع القسم **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="e01b7-126">في الحقل **إيصال استلام المنتجات**، اكتب أي قيمة.</span><span class="sxs-lookup"><span data-stu-id="e01b7-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="e01b7-127">يتم استخدام هذا الحقل لإدخال مرجع سيتم استخدامه كإيصال لدفتر يومية إيصال استلام المنتج.</span><span class="sxs-lookup"><span data-stu-id="e01b7-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="e01b7-128">قم بتوسيع القسم **البنود**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="e01b7-129">تعيين **الكمية** إلى "4".</span><span class="sxs-lookup"><span data-stu-id="e01b7-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="e01b7-130">هنا يمكنك أن تحدد يدويًا الكمية التي يتم استلامها لكل بند في الأمر.</span><span class="sxs-lookup"><span data-stu-id="e01b7-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="e01b7-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e01b7-131">Select **OK**.</span></span> <span data-ttu-id="e01b7-132">تم الآن تسجيل البضائع على أنها مستلمة على أمر إرجاع الشراء، وتم إنشاء دفتر يومية إيصال استلام المنتجات كمستند لإظهار هذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="e01b7-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="e01b7-133">يمكنك استخدام إجراء إيصال استلام المنتجات لمراجعة دفاتر اليومية التي تم إنشاؤها مع أمر الشراء، والاطلاع على المنتجات التي تم استلامها وتاريخ الاستلام.</span><span class="sxs-lookup"><span data-stu-id="e01b7-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

