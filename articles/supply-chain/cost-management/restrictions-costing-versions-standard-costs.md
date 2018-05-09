---
title: "قيود على إصدارات التكاليف للتكاليف القياسية"
description: "يوضح هذا الموضوع القيود التي يتم تطبيقها على إصدار التكلفة للتكاليف القياسية."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
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
ms.openlocfilehash: adc77f632fecebc39e818fa38f78071842ec8de4
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="f9c0c-103">قيود على إصدارات التكاليف للتكاليف القياسية</span><span class="sxs-lookup"><span data-stu-id="f9c0c-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9c0c-104">يوضح هذا الموضوع القيود التي يتم تطبيقها على إصدار التكلفة للتكاليف القياسية.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="f9c0c-105">تساعد القيود التالية على ضمان الالتزام بمبادئ التكلفة القياسية:</span><span class="sxs-lookup"><span data-stu-id="f9c0c-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="f9c0c-106">يجب تضمين المصاريف في تكلفة الصنف.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="f9c0c-107">وتقدم المصاريف لصنف مصنّع التكاليف الثابتة المستهلكة في قائمة مكونات الصنف (BOM) ومعلومات التوجيه.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="f9c0c-108">لذلك، يجب تضمين المصاريف في تكلفة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="f9c0c-109">كما يتم تضمين المصاريف لصنف تم شراؤه أيضًا في تكلفة وحدة الصنف.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="f9c0c-110">يجب أن يعتمد حساب التكاليف القياسية للأصناف المصنّعة على سجلات التكلفة في إصدار تكلفة للتكاليف القياسية.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="f9c0c-111">ويمكن استخدام المصادر البديلة لبيانات التكلفة فقط مع إصدار تكلفة للتكاليف المخططة، على سبيل المثال، اتفاقيات تجارية بسعر الشراء للأصناف التي تم شراؤها.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="f9c0c-112">يتم تحديد مصادر بديلة لبيانات التكلفة حسب مجموعة حساب قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="f9c0c-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="f9c0c-113">يجب تنفيذ عمليات حساب قائمة مكونات الصنف (BOM) في وضع عملية تحديد إجمالي المكونات المطلوبة بمستوى واحد.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="f9c0c-114">يمكن نسخ بيانات تكلفة الصنف للتكاليف القياسية إلى إصدار تكلفة آخر يحتوي على تكاليف قياسية أو تكاليف مخططة.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="f9c0c-115">ومع ذلك؛ لا يمكن نسخ بيانات تكلفة الصنف للتكاليف المخططة إلى إصدار تكلفة يحتوي على تكاليف قياسية؛ وذلك لأن القيود التي تم إدراجها في بداية هذا الموضوع لا تنطبق على التكاليف المخططة.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="f9c0c-116">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="f9c0c-116">Related topics</span></span>
--------

[<span data-ttu-id="f9c0c-117">إصدارات التكلفة</span><span class="sxs-lookup"><span data-stu-id="f9c0c-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="f9c0c-118">تحديث التكاليف المعيارية في بيئة غير مصنعة</span><span class="sxs-lookup"><span data-stu-id="f9c0c-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="f9c0c-119">الإعداد للاحتفاظ بالتكاليف القياسية للأصناف المصنعة</span><span class="sxs-lookup"><span data-stu-id="f9c0c-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


