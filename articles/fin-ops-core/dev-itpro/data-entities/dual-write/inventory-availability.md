---
title: توفر المخزون في الكتابة المزدوجة
description: يوفر هذا الموضوع معلومات حول فحص توفر المخزون في الكتابة المزدوجة.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443862"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="b0742-103">توفر المخزون في الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="b0742-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0742-104">باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى صفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b0742-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="b0742-105">على سبيل المثال، يمكنك فحص المخزون وتحديد تاريخ التنفيذ كمهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="b0742-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="b0742-106">إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها.</span><span class="sxs-lookup"><span data-stu-id="b0742-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="b0742-107">يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="b0742-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="b0742-108">المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="b0742-108">On-hand inventory</span></span>

<span data-ttu-id="b0742-109">في رأس صفحات **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="b0742-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="b0742-110">عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي.</span><span class="sxs-lookup"><span data-stu-id="b0742-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="b0742-111">يظهر مربع الحوار هذا نفس المعلومات كـ [مخزون فعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="b0742-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="b0742-112">يقوم مربع الحوار بإرجاع معلومات المخزون من Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b0742-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b0742-113">تشمل هذه المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0742-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="b0742-114">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="b0742-114">On-hand quantity</span></span>
- <span data-ttu-id="b0742-115">الكمية المحجوزة</span><span class="sxs-lookup"><span data-stu-id="b0742-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="b0742-116">الكمية الفعلية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="b0742-116">Available on-hand quantity</span></span>
- <span data-ttu-id="b0742-117">الكمية المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b0742-117">Ordered quantity</span></span>
- <span data-ttu-id="b0742-118">الكمية تحت الطلب</span><span class="sxs-lookup"><span data-stu-id="b0742-118">On-order quantity</span></span>
- <span data-ttu-id="b0742-119">الكمية المطلوبة المحجوزة</span><span class="sxs-lookup"><span data-stu-id="b0742-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="b0742-120">إجمالي الكمية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="b0742-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="b0742-121">معلومات ATP</span><span class="sxs-lookup"><span data-stu-id="b0742-121">ATP information</span></span>

<span data-ttu-id="b0742-122">في Sales، تمت إضافة زر **معلومات ATP** جديد إلى أصناف البند في صفحة **عروض الأسعار** و **الأوامر** و **الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="b0742-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="b0742-123">عند تحديد هذا الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر.</span><span class="sxs-lookup"><span data-stu-id="b0742-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="b0742-124">لمربع الحوار هذا نفس الإعدادات الموضحة في [‏‫التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="b0742-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="b0742-125">يقوم مربع الحوار بإرجاع معلومات ATP من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b0742-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="b0742-126">تشمل هذه المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0742-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="b0742-127">كمية ATP</span><span class="sxs-lookup"><span data-stu-id="b0742-127">ATP quantity</span></span>
- <span data-ttu-id="b0742-128">كمية الإيصال</span><span class="sxs-lookup"><span data-stu-id="b0742-128">Receipt quantity</span></span>
- <span data-ttu-id="b0742-129">كمية الإصدار</span><span class="sxs-lookup"><span data-stu-id="b0742-129">Issue quantity</span></span>
- <span data-ttu-id="b0742-130">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="b0742-130">On-hand quantity</span></span>
