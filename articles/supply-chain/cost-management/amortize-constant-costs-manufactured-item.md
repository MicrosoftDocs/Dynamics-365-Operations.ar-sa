---
title: استهلاك التكاليف الثابتة لصنف مصنّع
description: تعكس التكاليف الثابتة لصنف مصنّع أوقات إعداد العمليات والمكونات ذات كمية ثابتة أو قيمة خردة ثابتة.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 298b5cbbf955527edb399eae78a1c8e60a8b9ce3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421575"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="6d23f-103">استهلاك التكاليف الثابتة لصنف مصنّع</span><span class="sxs-lookup"><span data-stu-id="6d23f-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d23f-104">تعكس التكاليف الثابتة لصنف مصنّع أوقات إعداد العمليات والمكونات ذات كمية ثابتة أو قيمة خردة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="6d23f-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="6d23f-105">ويستخدم مفهوم حجم دفعة التكلفة لتسديد هذه التكاليف الثابتة في التكلفة المحسوبة للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="6d23f-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="6d23f-106">هناك العديد من المرادفات لهذا المفهوم، أحدها هو حجم دفعة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="6d23f-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="6d23f-107">هناك أيضًا الكثير من المرادفات لمفهوم استهلاك التكاليف الثابتة، أحدها التكاليف الثابتة النسبية.</span><span class="sxs-lookup"><span data-stu-id="6d23f-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="6d23f-108">تُستخدم كمية حجم دفعة التكاليف لصنف مصنّغ في حساب قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="6d23f-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="6d23f-109">وتعتمد الكمية على كيفية بدء حساب شجرة المواد وكيفية إجرائه، كما هو موضح فيما يلي:</span><span class="sxs-lookup"><span data-stu-id="6d23f-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="6d23f-110">كمية الحساب الافتراضية في حساب قائمة مكونات الصنف − تعمل ‏‏كمية الأمر القياسية للصنف بالنسبة إلى المخزون كحجم دفعة التكلفة، ولكن قد تكون القيمة الافتراضية كمية أكبر لتعكس كمية أمر متعددة للصنف.</span><span class="sxs-lookup"><span data-stu-id="6d23f-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="6d23f-111">يمكن تعريف كمية أمر التوريد القياسية والمتعددة للصنف من خلال ‏‏إعدادات الأمر الافتراضية أو ‏‏إعدادات الأوامر الخاصة بالموقع.</span><span class="sxs-lookup"><span data-stu-id="6d23f-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="6d23f-112">كمية الحساب المعينة في حساب شجرة مواد الصنف − تعمل كمية الحساب المعينة كحجم دفعة التكلفة للصنف.</span><span class="sxs-lookup"><span data-stu-id="6d23f-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="6d23f-113">تستخدم كمية الحساب في البداية كمية الأمر القياسية للصنف، ولكن قد يتم تجاوز القيمة الافتراضية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="6d23f-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="6d23f-114">تمثل كمية الحساب المعينة حجم دفعة التكلفة للصنف المحدد، وللمكونات المصنعة التي لديها نوع بند قائمة مكونات صنف خاص بالإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6d23f-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="6d23f-115">هذا لأنه من المفترض أنه سيتم إنتاج المكون بالكمية الدقيقة.</span><span class="sxs-lookup"><span data-stu-id="6d23f-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="6d23f-116">وسيعكس حجم دفعة التكلفة للمكونات المصنعة الأخرى التي لديها نوع بند قائمة مكونات صنف خاص بالصنف كمية الأمر القياسية لديه.</span><span class="sxs-lookup"><span data-stu-id="6d23f-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="6d23f-117">كمية حساب التصنيع حسب الطلب المعينة في حساب شجرة مواد الصنف − تعمل كمية الحساب المعينة كحجم دفعة التكلفة للصنف ومكوناته المصنعة عند استخدام حسابات شجرة المواد لوضع عملية تحديد إجمالي المكونات المطلوبة للتصنيع حسب الطلب.</span><span class="sxs-lookup"><span data-stu-id="6d23f-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="6d23f-118">ومن المفترض أن يتم إنتاج المكونات المصنعة بالكمية الدقيقة، تمامًا مثل المكون المصنع الذي لديه نوع بند قائمة مكونات صنف خاص بالإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6d23f-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="6d23f-119">كمية الحساب المعينة في حساب شجرة المواد الخاصة بالأمر − يمكن إجراء حساب شجرة المواد الخاصة بالأمر لصنف بند في أمر التوريد أو عرض أسعار المبيعات أو أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="6d23f-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="6d23f-120">تستخدم كمية الحساب المعينة الكمية على البند الأصلي، ولكن يمكن تجاوز الكمية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="6d23f-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="6d23f-121">كما يمكنك تحديد استخدام حساب شجرة المواد الخاص بالأمر لوضع عملية تحديد إجمالي المكونات المطلوبة للتصنيع حسب الطلب أو متعدد المستويات.</span><span class="sxs-lookup"><span data-stu-id="6d23f-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="6d23f-122">يسمى المبلغ المحسوب للتكاليف الثابتة المسددة للصنف المصنع المصاريف.</span><span class="sxs-lookup"><span data-stu-id="6d23f-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>





