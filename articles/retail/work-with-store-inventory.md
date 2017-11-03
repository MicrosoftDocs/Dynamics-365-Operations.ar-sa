---
title: "إدارة مخزون المتجر"
description: "توضح هذه المقالة أنواع المستندات التي يمكنك استخدامها لإدارة المخزون."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6245d37ace9f46ecce83a0cf80a014d5de898bbc
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="9c685-103">إدارة مخزون المتجر</span><span class="sxs-lookup"><span data-stu-id="9c685-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9c685-104">توضح هذه المقالة أنواع المستندات التي يمكنك استخدامها لإدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="9c685-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="9c685-105">يمكنك استخدام الأنواع التالية من المستندات لإدارة المخزون الخاصة بمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="9c685-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="9c685-106">أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="9c685-106">Purchase orders</span></span>
<span data-ttu-id="9c685-107">يتم إنشاء أوامر الشراء في المقر الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="9c685-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="9c685-108">‏‫وإذا تم تضمين مستودع البيع بالتجزئة في رأس أمر الشراء، فيمكن تلقي الأمر في المتجر باستخدام نقاط البيع الحديثة أو نقاط بيع المجموعة في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="9c685-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="9c685-109">وبعد أن يتم إدخال الكميات التي يتم تلقيها في المتجر، يمكن حفظها محلياً لتعديلات إضافية.‬</span><span class="sxs-lookup"><span data-stu-id="9c685-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9c685-110">وبدلاً من ذلك، يمكن تنفيذ الكميات وإرسالها إلى المكتب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="9c685-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9c685-111">وفي المقر الرئيسي، يتم عرض الكميات التي تم تلقيها في المتجر في Dynamics 365 for Retail، في حقل **تلقي الآن** في أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9c685-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="9c685-112">أوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="9c685-112">Transfer orders</span></span>
<span data-ttu-id="9c685-113">يمكن لأمر تحويل تحديد أن متجر معين هو موقع يمكن شحن الأصناف منه.</span><span class="sxs-lookup"><span data-stu-id="9c685-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="9c685-114">في هذه الحالة، يظهر أمر التحويل في المتجر كطلب انتقاء في نقطة البيع الحديثة أو نقطة بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9c685-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9c685-115">وبعد أن يتم انتقاء الكميات المطلوبة، يتم الالتزام بها وإرسالها إلى المقر الرئيسي.‬</span><span class="sxs-lookup"><span data-stu-id="9c685-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="9c685-116">في المقر الرئيسي، يتم انتقاء الكميات التي تم تلقيها في المتجر في Dynamics 365 for Retail، في حقل **شحن الآن** في أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="9c685-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="9c685-117">ويمكن لأمر تحويل تحديد أن متجر معين هو موقع يمكن شحن الأصناف إليه.</span><span class="sxs-lookup"><span data-stu-id="9c685-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="9c685-118">في هذه الحالة، يظهر أمر التحويل في المتجر كطلب تلقي في نقطة البيع الحديثة أو نقطة بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9c685-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9c685-119">وبعد أن يتم إدخال الكميات التي يتم تلقيها في المتجر، يمكن حفظها محلياً لتعديلات إضافية.‬</span><span class="sxs-lookup"><span data-stu-id="9c685-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9c685-120">وبدلاً من ذلك، يمكن تنفيذ الكميات وإرسالها إلى المكتب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="9c685-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9c685-121">وفي المقر الرئيسي، يتم عرض الكميات التي تم تلقيها في المتجر في Dynamics 365 for Retail، في حقل **تلقي الآن** في أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="9c685-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="9c685-122">عمليات جرد المخزون</span><span class="sxs-lookup"><span data-stu-id="9c685-122">Stock counts</span></span>
<span data-ttu-id="9c685-123">قد تكون عمليات جرد المخزون مجدولة أو غير مجدولة.</span><span class="sxs-lookup"><span data-stu-id="9c685-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="9c685-124">يتم البدء في جرد المخزون المجدول في المكتب الرئيسي، الذي يحدد الأصناف التي يجب جردها.</span><span class="sxs-lookup"><span data-stu-id="9c685-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="9c685-125">يُنشئ المكتب الرئيسي مستند جرد يمكن استلامه في المتجر، حيث يتم إدخال كميات المخزون الفعلي المتوفر في نقطة البيع الحديثة أو نقطة بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9c685-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="9c685-126">ويتم البدء في عمليات جرد المخزون غير المجدولة في المتجر، ويتم تحديث كميات المخزون الفعلي المتوفر في نقطة البيع الحديثة أو نقاط بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9c685-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="9c685-127">وعلى عكس الجرد المجدول، لا تحتوي عمليات جرد المخزون غير المجدولة على قائمة بالأصناف محددة مسبقاً.‬</span><span class="sxs-lookup"><span data-stu-id="9c685-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="9c685-128">وعند اكتمال عملية جرد مخزون من أي نوع، فإنه يتم الالتزام بها وإرسالها إلى المكتب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="9c685-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="9c685-129">وفي المكتب الرئيسي، يتم التحقق من صحة الجرد وترحيله.</span><span class="sxs-lookup"><span data-stu-id="9c685-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="9c685-130">البحث في المخزون</span><span class="sxs-lookup"><span data-stu-id="9c685-130">Inventory lookup</span></span>
<span data-ttu-id="9c685-131">كمية المنتجات الحالية الفعلية للعديد من المتاجر والمستودعات التي يمكنك عرضها في صفحة البحث في المخزون.</span><span class="sxs-lookup"><span data-stu-id="9c685-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="9c685-132">بالإضافة إلى الكمية الحالية الفعلية، يمكن عرض الكميات المستقبلية المتاحة للتعهد (ATP) لكل متجر فردي.</span><span class="sxs-lookup"><span data-stu-id="9c685-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="9c685-133">للقيام بذلك، حدد المتجر الذي ترغب في عرض كمية ATP الخاصة به، ثم انقر فوق **إظهار توافر المتجر‬**.</span><span class="sxs-lookup"><span data-stu-id="9c685-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





