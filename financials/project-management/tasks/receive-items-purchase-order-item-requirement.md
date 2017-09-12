--- 
title: "تلقي الأصناف على أمر شراء من طلبات الصنف"
description: "يوضح هذا الإجراء كيفية استلام الأصناف في أمر شراء من طلب الصنف."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7c9093439c4c0c4645d96ad97ba56f31026ec334
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="40098-103">تلقي الأصناف على أمر شراء من طلبات الصنف</span><span class="sxs-lookup"><span data-stu-id="40098-103">Receive items on purchase order from item requirement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40098-104">يوضح هذا الإجراء كيفية استلام الأصناف في أمر شراء من طلب الصنف.</span><span class="sxs-lookup"><span data-stu-id="40098-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="40098-105">باستخدام متطلب صنف بدلا من حركة صنف، يمكنك تخطيط التسليم قبل الاستخدام الفعلي للصنف، وإنشاء أمر شراء، وتضمين الصنف في إطار عمل الاتفاقية التجارية، وتضمين متطلب الصنف في تخطيط الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="40098-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="40098-106">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="40098-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="40098-107">انتقل إلى إدارة المشاريع والمحاسبة > المشاريع > جميع المشاريع.</span><span class="sxs-lookup"><span data-stu-id="40098-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="40098-108">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="40098-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="40098-109">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="40098-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="40098-110">انقر فوق "متطلبات الصنف".</span><span class="sxs-lookup"><span data-stu-id="40098-110">Click Item requirements.</span></span>
5. <span data-ttu-id="40098-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="40098-111">Click New.</span></span>
6. <span data-ttu-id="40098-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="40098-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="40098-113">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="40098-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="40098-114">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="40098-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="40098-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="40098-115">Click Save.</span></span>
10. <span data-ttu-id="40098-116">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="40098-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="40098-117">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="40098-117">Click Functions.</span></span>
12. <span data-ttu-id="40098-118">انقر فوق "إنشاء أمر شراء".</span><span class="sxs-lookup"><span data-stu-id="40098-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="40098-119">حدد خانة الاختيار "تضمين".</span><span class="sxs-lookup"><span data-stu-id="40098-119">Select the Include check box.</span></span>
14. <span data-ttu-id="40098-120">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="40098-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="40098-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="40098-121">Click OK.</span></span>
16. <span data-ttu-id="40098-122">انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="40098-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="40098-123">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="40098-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="40098-124">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="40098-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="40098-125">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="40098-125">Click Confirm.</span></span>
20. <span data-ttu-id="40098-126">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="40098-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="40098-127">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="40098-127">Click Product receipt.</span></span>
22. <span data-ttu-id="40098-128">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="40098-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="40098-129">في الحقل "إيصال استلام المنتجات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="40098-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="40098-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="40098-130">Click OK.</span></span>


