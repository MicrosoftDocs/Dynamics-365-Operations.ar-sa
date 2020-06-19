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
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426972"
---
# <a name="inventory-availability"></a><span data-ttu-id="cee13-103">توفر المخزون</span><span class="sxs-lookup"><span data-stu-id="cee13-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="cee13-104">باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى نماذج **عروض الأسعار** أو **الأوامر** أو **الفواتير** في التطبيقات المستندة إلى نموذج في Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cee13-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="cee13-105">على سبيل المثال، يعتبر فحص المخزون وتحديد تاريخ التنفيذ مهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="cee13-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="cee13-106">إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها.</span><span class="sxs-lookup"><span data-stu-id="cee13-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="cee13-107">يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="cee13-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="cee13-108">المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="cee13-108">On-hand Inventory</span></span> 

<span data-ttu-id="cee13-109">في رأس نماذج **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="cee13-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="cee13-110">عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي.</span><span class="sxs-lookup"><span data-stu-id="cee13-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="cee13-111">إنه يُرجع معلومات المخزون من Dynamics 365 Supply Chain Management، ويعرض المعلومات نفسها كما في [المخزون الفعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="cee13-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="cee13-112">وتتضمن المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="cee13-112">The information includes these quantities:</span></span>

- <span data-ttu-id="cee13-113">**الكمية الفعلية**</span><span class="sxs-lookup"><span data-stu-id="cee13-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="cee13-114">**الكمية المحجوزة**</span><span class="sxs-lookup"><span data-stu-id="cee13-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="cee13-115">**الكمية الفعلية المتوفرة**</span><span class="sxs-lookup"><span data-stu-id="cee13-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="cee13-116">**الكمية المطلوبة**</span><span class="sxs-lookup"><span data-stu-id="cee13-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="cee13-117">**الكمية تحت الطلب**</span><span class="sxs-lookup"><span data-stu-id="cee13-117">**On-order Quantity**</span></span>
- <span data-ttu-id="cee13-118">**الكمية المطلوبة المحجوزة**</span><span class="sxs-lookup"><span data-stu-id="cee13-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="cee13-119">**إجمالي الكمية المتوفرة**</span><span class="sxs-lookup"><span data-stu-id="cee13-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="cee13-120">معلومات ATP</span><span class="sxs-lookup"><span data-stu-id="cee13-120">ATP information</span></span>

<span data-ttu-id="cee13-121">في عناصر بنود **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **معلومات ATP**.</span><span class="sxs-lookup"><span data-stu-id="cee13-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="cee13-122">عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر.</span><span class="sxs-lookup"><span data-stu-id="cee13-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="cee13-123">وهو يُرجع **معلومات ATP** من Supply Chain Management ويعرض الإعدادات التي ورد وصفها في [التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="cee13-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="cee13-124">تتضمن المعلومات **كمية ATP** و**كمية الإيصال** و**كمية الإصدار** و**الكمية الفعلية**.</span><span class="sxs-lookup"><span data-stu-id="cee13-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
