---
title: "عرض المصاريف لصنف مصنّع"
description: "تعكس التكاليف الثابتة لصنف مصنّع أوقات إعداد العمليات والمكونات ذات كمية ثابتة أو قيمة خردة ثابتة."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9f41939554cd22045940af937f227f43ba098394
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="f5b5d-103">عرض المصاريف لصنف مصنّع</span><span class="sxs-lookup"><span data-stu-id="f5b5d-103">Display charges for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f5b5d-104">تعكس التكاليف الثابتة لصنف مصنّع أوقات إعداد العمليات والمكونات ذات كمية ثابتة أو قيمة خردة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="f5b5d-105">يمكن عرض المبلغ المحسوب لمصاريف صنف ما مع تكاليف وحدة الصنف.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="f5b5d-106">ومع ذلك، تظهر المصاريف في بعض الأحيان كحقول منفصلة، ولا يتم تضمينها في تكاليف وحدة الصنف.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="f5b5d-107">عندما تظهر المصاريف كحقول منفصلة، يعرض أحد الحقول إجمالي مبلغ المصاريف، بينما يعرض الحقل الآخر حجم دفعة التكلفة المستخدم لاستهلاك المبلغ.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="f5b5d-108">على سبيل المثال، تعرض صفحة سعر الصنف المصاريف كحقلين منفصلين.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="f5b5d-109">ومع ذلك، تعرض الصفحة "كامل" إجمالي تكلفة الصنف لكل وحدة، ويتم تضمين التكاليف المستهلكة في تكاليف الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>
<span data-ttu-id="f5b5d-110">يتم دائمًا تضمين المصاريف لصنف مصنّع في تكلفة وحدة الصنف لأغراض التكلفة القياسية.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="f5b5d-111">ويمكن تضمينها بشكل اختياري لأغراض التكلفة المخططة.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="f5b5d-112">تقوم سياسة في إصدار التكاليف بفرض تضمين المصاريف في تكلفة الصنف المصنّع.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="f5b5d-113">عند تنشيط سجل التكلفة لصنف ما، ستقوم بتحديث المصاريف لمعلومات التكلفة الأساسية الخاصة بالصنف، التي تظهر في صفحة سعر الصنف.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="f5b5d-114">تظهر المصاريف كحقلين منفصلين، ولا يتم تضمينها في تكلفة وحدة الصنف.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="f5b5d-115">وتقوم كل عملية تنشيط بتحديث معلومات التكلفة الأساسية، حتى لو كانت جهود التنشيط تعكس مواقع مختلفة.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="f5b5d-116">وبالتالي، يجب عرض معلومات التكلفة الأساسية كمعلومات مرجعية.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-116">Therefore, you should view the base cost information as reference information.</span></span>






