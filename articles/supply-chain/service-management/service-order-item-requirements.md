---
title: متطلبات صنف أمر الخدمة‬
description: إذا كنت تحتاج إلى حجز أصناف محددة لأمر خدمة، يمكنك إنشاء متطلبات صنف مخزون لها.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e31f58cf8782c715b97bdae0e89f684b15a76d2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215069"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="c7b4b-103">متطلبات صنف أمر الخدمة‬</span><span class="sxs-lookup"><span data-stu-id="c7b4b-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c7b4b-104">يمكنك إنشاء أمر خدمة لتعقب وإدارة الخدمات التي توفرها للعملاء.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="c7b4b-105">إذا كنت تحتاج إلى حجز أصناف محددة لأمر خدمة، يمكنك إنشاء متطلبات صنف مخزون لها.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="c7b4b-106">يمكن استهلاك متطلبات صنف مباشرة من المخزون أو يمكن بدء أمر إنتاج للصنف.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="c7b4b-107">باستخدام متطلب صنف بدلا من حركة صنف، يمكنك تخطيط التسليم قبل الاستخدام الفعلي للصنف، وإنشاء أمر شراء، وتضمين الصنف في إطار عمل الاتفاقية التجارية، وتضمين متطلب الصنف في تخطيط الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="c7b4b-108">تتم معالجة متطلبات الصنف لأوامر الخدمة من خلال مشروع.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="c7b4b-109">لإنشاء متطلب صنف في أمر خدمة، يجب أن يتم إلحاق أمر الخدمة بمشروع.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="c7b4b-110">حالما يتم إنشاء متطلب صنف لأمر خدمة، يمكن عرضه من **المشروع** في أمر الخدمة الفردي أو من خلال النموذج **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="c7b4b-111">عرض متطلب صنف من أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="c7b4b-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="c7b4b-112">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="c7b4b-113">انقر فوق **الإرسال**، ثم انقر فوق **متطلب صنف** لفتح النموذج **متطلبات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="c7b4b-114">انقر فوق علامة التبويب **المشروع**، ثم حدد الحقل **أمر الخدمة** لعرض أوامر الخدمة لمتطلب الصنف.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="c7b4b-115">حذف أوامر الخدمة التي بها متطلبات صنف</span><span class="sxs-lookup"><span data-stu-id="c7b4b-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="c7b4b-116">إذا تم إنشاء متطلب صنف في أمر الخدمة، فلا يمكنك إلغاء أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="c7b4b-117">يجب حذف متطلب الصنف لكي يمكنك حذف أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="c7b4b-118">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="c7b4b-119">انقر فوق **الإرسال**، ثم انقر فوق **متطلب صنف** لفتح النموذج **متطلبات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="c7b4b-120">يسرد هذا النموذج متطلبات الصنف التي تم إنشاؤها في أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="c7b4b-121">حدد متطلب الصنف المطلوب حذفه، ثم انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="c7b4b-122">–أو –</span><span class="sxs-lookup"><span data-stu-id="c7b4b-122">–or–</span></span>

1.  <span data-ttu-id="c7b4b-123">انقر فوق **إدارة المشاريع‬ والمحاسبة** \> **عام** \> **المشاريع** \> **كل المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="c7b4b-124">قم بفتح المشروع الموجود به أمر الخدمة الذي تم إنشاء متطلب صنف به.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="c7b4b-125">في نموذج **المشاريع**، في الجزء الأيسر، انقر فوق **متطلبات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="c7b4b-126">النموذج **متطلبات الأصناف** يسرد متطلبات الصنف التي تم إقرانها بالمشروع الذي تم تحديده.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="c7b4b-127">حدد متطلب الصنف المطلوب حذفه، ثم انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="c7b4b-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7b4b-128">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="c7b4b-128">See also</span></span>

<span data-ttu-id="c7b4b-129">[متطلبات الصنف (نموذج)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="c7b4b-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

