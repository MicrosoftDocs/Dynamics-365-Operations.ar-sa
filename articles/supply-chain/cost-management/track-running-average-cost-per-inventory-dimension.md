---
title: تتبع متوسط تكلفة التشغيل لكل بُعد مخزون
description: يتم إرفاق مجموعة أبعاد مخزون لكل صنف بالمخزون. ولذلك، يتم احتساب متوسط سعر التكلفة الحالي للصنف استنادًا إلى أبعاد المخزون المحددة التي يتم تعقبها ماليًا.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2bf04a42edf09c35e81742b1c60db8944eba2ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252860"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="9dfe0-104">تتبع متوسط تكلفة التشغيل لكل بُعد مخزون</span><span class="sxs-lookup"><span data-stu-id="9dfe0-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dfe0-105">يتم إرفاق مجموعة أبعاد مخزون لكل صنف بالمخزون.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="9dfe0-106">ولذلك، يتم احتساب متوسط سعر التكلفة الحالي للصنف استنادًا إلى أبعاد المخزون المحددة التي يتم تعقبها ماليًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="9dfe0-107">هناك ثلاثة أنواع من أبعاد المخزون: المنتج، والتخزين، والتعقب.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="9dfe0-108">تتضمن أبعاد المنتج التكوين والحجم واللون.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="9dfe0-109">كما يتم دومًا تعقب أبعاد المنتج ماليًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="9dfe0-110">بينما تتضمن أبعاد التخزين والتعقب الموقع والمستودع والمكان وحالة المخزون ولوحة الترخيص ورقم الدُفعة والرقم المسلسل.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="9dfe0-111">ويمكنك اختيار أبعاد التخزين والتعقب التي يتم تعقبها ماليًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="9dfe0-112">**مثال 1**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-112">**Example 1**</span></span> 

<span data-ttu-id="9dfe0-113">في حالة تعقب مجموعة أبعاد التخزين المرفقة بالصنف ماليًا حسب المستودع، يتم حساب متوسط سعر التكلفة الحالي لكل مستودع.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="9dfe0-114">تمت فوترة أوامر الشراء التالية:</span><span class="sxs-lookup"><span data-stu-id="9dfe0-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="9dfe0-115">تمت فوترة أمر شراء لكمية قيمتها 2 بسعر تكلفة يبلغ 10.00 دولارات أمريكية للمستودع العام (GW).</span><span class="sxs-lookup"><span data-stu-id="9dfe0-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="9dfe0-116">تمت فوترة أمر شراء لكمية قيمتها 3 بسعر تكلفة يبلغ 12.00 دولارًا أمريكيًا للمستودع العام (GW).</span><span class="sxs-lookup"><span data-stu-id="9dfe0-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="9dfe0-117">تمت فوترة أمر شراء لكمية قيمتها 5 بسعر تكلفة يبلغ 15.00 دولارًا أمريكيًا للمستودع الرئيسي (MW).</span><span class="sxs-lookup"><span data-stu-id="9dfe0-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="9dfe0-118">يبلغ متوسط سعر التكلفة الحالي للمستودع العام 11.20 دولار أمريكي، ويبلغ متوسط سعر التكلفة الحالي للمستودع الرئيسي (MW‏) 15.00 دولارًا أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="9dfe0-119">ويتم ترحيل فاتورة أمر المبيعات للمستودع العام (GW).</span><span class="sxs-lookup"><span data-stu-id="9dfe0-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="9dfe0-120">وتبلغ قيمة المخزون وتكلفة البضائع المبيعة (قبل تشغيل إغلاق المخزون وبدون تمييز) هو 11.20 دولارًا أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="9dfe0-121">ويتم ترحيل فاتورة أمر مبيعات أخرى للمستودع الرئيسي (MW).</span><span class="sxs-lookup"><span data-stu-id="9dfe0-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="9dfe0-122">وتبلغ قيمة المخزون وتكلفة البضائع المبيعة (قبل تشغيل إغلاق المخزون وبدون تمييز) هو 15.00 دولارًا أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="9dfe0-123">**المثال 2** إذا كان يتم تعقب مجموعة أبعاد التخزين المرتبطة بالصنف ماليًا حسب المستودع، يتم تعقب مجموعة أبعاد التعقب ماليًا حسب رقم الدُفعة، ويتم حساب متوسط سعر التكلفة الحالي لكل دُفعة.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="9dfe0-124">**ملاحظة:** نوصيك دومًا بعرض سعر التكلفة لكافة الأبعاد المالية التي يتم تعقبها.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="9dfe0-125">تمت فوترة أوامر الشراء التالية:</span><span class="sxs-lookup"><span data-stu-id="9dfe0-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="9dfe0-126">أمر شراء لكمية قيمتها 2 بسعر تكلفة يبلغ 10.00 دولارات أمريكية تمت فوترته للمستودع العام (GW) والدُفعة AAA.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="9dfe0-127">أمر شراء لكمية قيمتها 3 بسعر تكلفة يبلغ 12.00 دولارًا أمريكيًا تمت فوترته للمستودع العام (GW) والدُفعة AAA.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="9dfe0-128">أمر شراء لكمية قيمتها 2 بسعر تكلفة يبلغ 15.00 دولارًا أمريكيًا تمت فوترته للمستودع العام (GW) والدُفعة BBB.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="9dfe0-129">متوسط سعر التكلفة الحالي للمستودع العام (GW) ودُفعة AAA يبلغ ‏11.20 دولار أمريكي، ومتوسط سعر التكلفة الحالي للمستودع العام (GW‏) ودُفعة BBB يبلغ 15.00 دولارًا أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]