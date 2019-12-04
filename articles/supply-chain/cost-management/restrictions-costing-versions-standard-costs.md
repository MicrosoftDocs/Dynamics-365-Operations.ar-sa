---
title: قيود على إصدارات التكاليف للتكاليف القياسية
description: يوضح هذا الموضوع القيود التي يتم تطبيقها على إصدار التكلفة للتكاليف القياسية.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 484471c6bbda1d7396dfcfa34c33f50d247dad98
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812662"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="baad3-103">قيود على إصدارات التكاليف للتكاليف القياسية</span><span class="sxs-lookup"><span data-stu-id="baad3-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="baad3-104">يوضح هذا الموضوع القيود التي يتم تطبيقها على إصدار التكلفة للتكاليف القياسية.</span><span class="sxs-lookup"><span data-stu-id="baad3-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="baad3-105">تساعد القيود التالية على ضمان الالتزام بمبادئ التكلفة القياسية:</span><span class="sxs-lookup"><span data-stu-id="baad3-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="baad3-106">يجب تضمين المصاريف في تكلفة الصنف.</span><span class="sxs-lookup"><span data-stu-id="baad3-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="baad3-107">وتقدم المصاريف لصنف مصنّع التكاليف الثابتة المستهلكة في قائمة مكونات الصنف (BOM) ومعلومات التوجيه.</span><span class="sxs-lookup"><span data-stu-id="baad3-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="baad3-108">لذلك، يجب تضمين المصاريف في تكلفة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="baad3-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="baad3-109">كما يتم تضمين المصاريف لصنف تم شراؤه أيضًا في تكلفة وحدة الصنف.</span><span class="sxs-lookup"><span data-stu-id="baad3-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="baad3-110">يجب أن يعتمد حساب التكاليف القياسية للأصناف المصنّعة على سجلات التكلفة في إصدار تكلفة للتكاليف القياسية.</span><span class="sxs-lookup"><span data-stu-id="baad3-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="baad3-111">ويمكن استخدام المصادر البديلة لبيانات التكلفة فقط مع إصدار تكلفة للتكاليف المخططة، على سبيل المثال، اتفاقيات تجارية بسعر الشراء للأصناف التي تم شراؤها.</span><span class="sxs-lookup"><span data-stu-id="baad3-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="baad3-112">يتم تحديد مصادر بديلة لبيانات التكلفة حسب مجموعة حساب قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="baad3-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="baad3-113">يجب تنفيذ عمليات حساب قائمة مكونات الصنف (BOM) في وضع عملية تحديد إجمالي المكونات المطلوبة بمستوى واحد.</span><span class="sxs-lookup"><span data-stu-id="baad3-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="baad3-114">يمكن نسخ بيانات تكلفة الصنف للتكاليف القياسية إلى إصدار تكلفة آخر يحتوي على تكاليف قياسية أو تكاليف مخططة.</span><span class="sxs-lookup"><span data-stu-id="baad3-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="baad3-115">ومع ذلك؛ لا يمكن نسخ بيانات تكلفة الصنف للتكاليف المخططة إلى إصدار تكلفة يحتوي على تكاليف قياسية؛ وذلك لأن القيود التي تم إدراجها في بداية هذا الموضوع لا تنطبق على التكاليف المخططة.</span><span class="sxs-lookup"><span data-stu-id="baad3-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="baad3-116">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="baad3-116">Related topics</span></span>
--------

[<span data-ttu-id="baad3-117">نظرة عامة حول إصدارات التكاليف</span><span class="sxs-lookup"><span data-stu-id="baad3-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="baad3-118">تحديث التكاليف القياسية في بيئة غير تصنيع</span><span class="sxs-lookup"><span data-stu-id="baad3-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="baad3-119">الإعداد للاحتفاظ بالتكاليف القياسية للأصناف المصنعة</span><span class="sxs-lookup"><span data-stu-id="baad3-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

