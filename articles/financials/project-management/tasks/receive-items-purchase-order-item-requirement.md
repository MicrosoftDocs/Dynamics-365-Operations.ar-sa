---
title: تلقي الأصناف على أمر شراء من متطلبات الصنف
description: يوضح هذا الموضوع كيفية استلام الأصناف في أمر شراء من طلب الصنف.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867282"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="50d2b-103">تلقي الأصناف على أمر شراء من متطلبات الصنف</span><span class="sxs-lookup"><span data-stu-id="50d2b-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50d2b-104">يوضح هذا الموضوع كيفية استلام الأصناف في أمر شراء من طلب الصنف.</span><span class="sxs-lookup"><span data-stu-id="50d2b-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="50d2b-105">باستخدام متطلب صنف بدلا من حركة صنف، يمكنك تخطيط التسليم قبل الاستخدام الفعلي للصنف، وإنشاء أمر شراء، وتضمين الصنف في إطار عمل الاتفاقية التجارية، وتضمين متطلب الصنف في تخطيط الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="50d2b-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="50d2b-106">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="50d2b-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="50d2b-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها‬‬ > المشاريع > جميع المشاريع**‬‬.</span><span class="sxs-lookup"><span data-stu-id="50d2b-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="50d2b-108">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="50d2b-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="50d2b-109">في جزء الإجراءات، حدد **خطة**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="50d2b-110">حدد **متطلبات الصنف‬**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="50d2b-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-111">Select **New**.</span></span>
6. <span data-ttu-id="50d2b-112">في الصف الجديد، أدخل أو حدد قيمة في حقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="50d2b-113">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="50d2b-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="50d2b-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-114">Select **Save**.</span></span>
9. <span data-ttu-id="50d2b-115">في جزء الإجراءات‬، حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="50d2b-116">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-116">Select **Functions**.</span></span>
11. <span data-ttu-id="50d2b-117">حدد **إنشاء أمر شراء**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="50d2b-118">حدد خانة الاختيار **تضمين الكل**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="50d2b-119">في الحقل **حساب المورد**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="50d2b-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="50d2b-120">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-120">Select **OK**.</span></span>
15. <span data-ttu-id="50d2b-121">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة‬ > أوامر الشراء > جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="50d2b-122">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="50d2b-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="50d2b-123">في جزء الإجراءات، انقر فوق **شراء**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="50d2b-124">حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="50d2b-125">في جزء الإجراءات، حدد **استلام**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="50d2b-126">حدد **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="50d2b-127">في حقل **إيصال استلام المنتجات**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50d2b-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="50d2b-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="50d2b-128">Select **OK**.</span></span>

