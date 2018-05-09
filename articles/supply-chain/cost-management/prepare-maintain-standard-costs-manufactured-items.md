---
title: "الإعداد للاحتفاظ بالتكاليف القياسية للأصناف المصنعة"
description: "يوضح هذا الموضوع خطوات الإعداد للحفاظ على التكاليف للأصناف المصنعة."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9846f66997090de0219f59b4ba33efa15694ce8d
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="a306a-103">الإعداد للاحتفاظ بالتكاليف القياسية للأصناف المصنعة</span><span class="sxs-lookup"><span data-stu-id="a306a-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a306a-104">يوضح هذا الموضوع خطوات الإعداد للحفاظ على التكاليف للأصناف المصنعة.</span><span class="sxs-lookup"><span data-stu-id="a306a-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="a306a-105">تختلف الخطوات الخاصة بالأصناف المصنعة اختلافًا طفيفًا عن الخطوات الخاصة بالأصناف التي تم شراؤها.</span><span class="sxs-lookup"><span data-stu-id="a306a-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="a306a-106">وقد تؤثر النهج المعينة للأصناف المصنعة على عمليات حساب التكاليف للأصناف المصنعة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="a306a-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="a306a-107">للإعداد للاحتفاظ بالتكاليف للأصناف المصنعة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a306a-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="a306a-108">قم بتعيين مجموعة نموذج صنف للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="a306a-109">تحدد مجموعة نموذج الصنف أنه سيتم استخدام التكاليف القياسية.</span><span class="sxs-lookup"><span data-stu-id="a306a-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="a306a-110">قم بتخصيص مجموعة أصناف للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="a306a-111">تحتوي مجموعة الأصناف على حسابات دفتر الأستاذ التي تنطبق على الصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="a306a-112">وتشمل حسابات دفتر الأستاذ للصنف المصنع بنموذج المخزون للتكلفة القياسية على نسب الفرق في تسعير الإنتاج ونسب الفرق في تغيير القيمة وإعادة تقييم تكلفة المخزون.</span><span class="sxs-lookup"><span data-stu-id="a306a-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="a306a-113">قم بتخصيص وحدة قياس المخزون للصنف.</span><span class="sxs-lookup"><span data-stu-id="a306a-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="a306a-114">تتم الإشارة إلى تكاليف الصنف بوحدة قياس مخزون الصنف.</span><span class="sxs-lookup"><span data-stu-id="a306a-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="a306a-115">لا تقم بتعيين مجموعة تكاليف للصنف المصنع، إلا إذا كانت ستتم معاملته كصنف تم شراؤه.</span><span class="sxs-lookup"><span data-stu-id="a306a-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="a306a-116">قم بتعيين مجموعة حساب قائمة مكونات الصنف (BOM) إلى الصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="a306a-117">تحدد مجموعة حساب قائمة مكونات الصنف للصنف شروط التحذير التي يتم تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="a306a-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="a306a-118">وبهذه الطريقة، عند القيام بحساب قائمة مكونات الصنف، يمكن إنشاء رسائل تحذير بشأن المصادر المحتملة لأخطاء الحساب.</span><span class="sxs-lookup"><span data-stu-id="a306a-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="a306a-119">فمثلاً، يمكن أن تقوم رسالة تحذير بتحديد الوقت الذي لا توجد فيه قائمة مكونات صنف أو مسار نشط.</span><span class="sxs-lookup"><span data-stu-id="a306a-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="a306a-120">تحتوي مجموعة حساب شجرة المواد على نهج إيقاف عملية تحديد إجمالي المكونات المطلوبة. التي توضح وقت وجوب معاملة الصنف المصنع كصنف مشترى.</span><span class="sxs-lookup"><span data-stu-id="a306a-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="a306a-121">قم بتعيين كمية الأمر القياسية للصنف المصنع عندما يكون له تكاليف ثابتة.</span><span class="sxs-lookup"><span data-stu-id="a306a-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="a306a-122">كمية الأمر القياسية تحسب حجم الدفعة لسداد التكاليف الثابتة.</span><span class="sxs-lookup"><span data-stu-id="a306a-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="a306a-123">تتضمن أمثلة التتكاليف الثابتة أوقات الإعداد في عمليات التوجيه وكمية مكونات ثابتة في قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="a306a-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="a306a-124">قم بتعريف شجرة المواد للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="a306a-125">يمكن تعريف إصدار شجرة مواد واحد أو أكثر للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="a306a-126">تحقق من أن الإصدارات التي تريدها تم تعليمها كمعتمدة ونشطة وأنها تحتوي على التواريخ السارية التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="a306a-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="a306a-127">ويمكن أن يكون إصدار شجرة المواد على مستوى الشركة ككل أو خاصًا بموقع معين.</span><span class="sxs-lookup"><span data-stu-id="a306a-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="a306a-128">قم بتعريف المسار للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="a306a-129">يمكن تعريف إصدار مسار واحد أو أكثر للصنف المصنع.</span><span class="sxs-lookup"><span data-stu-id="a306a-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="a306a-130">تحقق من أن الإصدارات التي تريدها تم تعليمها كمعتمدة ونشطة وأنها تحتوي على التواريخ السارية التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="a306a-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="a306a-131">ويجب أن يكون إصدار المسار خاصًا بموقع معين.</span><span class="sxs-lookup"><span data-stu-id="a306a-131">The route version must be site-specific.</span></span>

<span data-ttu-id="a306a-132">إذا أردت استخدام معلومات التوجيه لأغراض التكلفة، يلزم وجود خطوات إعداد إضافية.</span><span class="sxs-lookup"><span data-stu-id="a306a-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="a306a-133">فمثلاً، يجب أن تكون فئات التكلفة التي يتم تعيينها لعمليات التوجيه صحيحة وكاملة.</span><span class="sxs-lookup"><span data-stu-id="a306a-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="a306a-134">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="a306a-134">Related topics</span></span>
--------

[<span data-ttu-id="a306a-135">استهلاك أصول التكلفة الثابتة لصنف مصنّع</span><span class="sxs-lookup"><span data-stu-id="a306a-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="a306a-136">إعداد المنتجات التي يمكن أن تكون منتجة أو مشتراة</span><span class="sxs-lookup"><span data-stu-id="a306a-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)


