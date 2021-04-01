---
title: أبعاد عنصر التكلفة
description: تعتبر أبعاد عنصر التكلفة أحد الركائز الأساسية في محاسبة التكاليف، ويتم استخدامها لتصنيف وتعقب الأماكن التي تتدفق التكاليف إليها.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: be2f984c1ce5c76e3f995108d25f57c29e8c8457
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226337"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="46c1e-103">أبعاد عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="46c1e-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46c1e-104">تعتبر أبعاد عنصر التكلفة أحد الركائز الأساسية في محاسبة التكاليف، ويتم استخدامها لتصنيف وتعقب الأماكن التي تتدفق التكاليف إليها.</span><span class="sxs-lookup"><span data-stu-id="46c1e-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="46c1e-105">يتطابق عنصر التكلفة مع عنصر ذي صلة بالتكلفة في دليل الحسابات.</span><span class="sxs-lookup"><span data-stu-id="46c1e-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="46c1e-106">وباستطاعته أن يكون، بشكل أساسي، أي نوع عنصر عند أدنى مستوى في الشركة يمكن أن تتدفق التكاليف إليه.</span><span class="sxs-lookup"><span data-stu-id="46c1e-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="46c1e-107">تتراوح عناصر التكلفة كمفهوم من حسابات دفتر الأستاذ إلى كافة موارد التكلفة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="46c1e-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="46c1e-108">في الوقت الحالي، تدعم محاسبة التكاليف حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="46c1e-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="46c1e-109">نوعان من عناصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="46c1e-109">Two types of cost elements</span></span>
<span data-ttu-id="46c1e-110">هناك نوعان من عناصر التكلفة: عناصر التكلفة الأساسية وعناصر التكلفة الثانوية.</span><span class="sxs-lookup"><span data-stu-id="46c1e-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="46c1e-111">يصف الجدول التالي الفرق بين النوعين.</span><span class="sxs-lookup"><span data-stu-id="46c1e-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46c1e-112"><strong>عناصر التكلفة الأساسية</strong></span><span class="sxs-lookup"><span data-stu-id="46c1e-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="46c1e-113"><strong>عناصر التكلفة الثانوية</strong></span><span class="sxs-lookup"><span data-stu-id="46c1e-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46c1e-114">تمثل عناصر التكلفة الأساسية تدفق التكاليف من المحاسبة المالية إلى محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="46c1e-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="46c1e-115">تتطابق بنية عنصر التكلفة مع بنية حساب الأرباح والخسائر في دفتر الأستاذ العام، حيث يمكن أن يتطابق عنصر تكلفة مع حساب رئيسي.</span><span class="sxs-lookup"><span data-stu-id="46c1e-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="46c1e-116">من غير الضروري أن تتمثل كافة الحسابات الرئيسية كعناصر تكلفة، وهذا يتوقف على احتياجات العمل.</span><span class="sxs-lookup"><span data-stu-id="46c1e-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="46c1e-117">تتضمن الأمثلة عن عناصر التكلفة الأساسية:</span><span class="sxs-lookup"><span data-stu-id="46c1e-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="46c1e-118">تكلفة البضائع المبيعة (COG)</span><span class="sxs-lookup"><span data-stu-id="46c1e-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="46c1e-119">التكاليف المادية غير المباشرة</span><span class="sxs-lookup"><span data-stu-id="46c1e-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="46c1e-120">تكاليف الموظفين</span><span class="sxs-lookup"><span data-stu-id="46c1e-120">Personnel costs</span></span></li>
<li><span data-ttu-id="46c1e-121">تكاليف الطاقة</span><span class="sxs-lookup"><span data-stu-id="46c1e-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="46c1e-122">تمثل عناصر التكلفة الثانوية تدفق التكاليف داخليًا، إذ يتم إنشاء هذه التكاليف واستخدامها فقط في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="46c1e-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="46c1e-123">ويتم استخدامها لضمان إمكانية تتبع مصدر التكاليف.</span><span class="sxs-lookup"><span data-stu-id="46c1e-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="46c1e-124">يتم استخدام عناصر التكلفة هذه في عمليات توزيع التكلفة وحسابات النفقات العامة.</span><span class="sxs-lookup"><span data-stu-id="46c1e-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="46c1e-125">تتضمن الأمثلة عن عناصر التكلفة الثانوية:</span><span class="sxs-lookup"><span data-stu-id="46c1e-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="46c1e-126">تكاليف الإنتاج</span><span class="sxs-lookup"><span data-stu-id="46c1e-126">Production costs</span></span></li>
<li><span data-ttu-id="46c1e-127">نفقات الإنتاج والمواد والتسويق</span><span class="sxs-lookup"><span data-stu-id="46c1e-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="46c1e-128">أبعاد عنصر التكلفة وأعضاء أبعاد عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="46c1e-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="46c1e-129">يُشار إلى عناصر التكلفة باسم *أبعاد عنصر التكلفة* .</span><span class="sxs-lookup"><span data-stu-id="46c1e-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="46c1e-130">وتسمى قيم الأبعاد الفردية *أعضاء أبعاد عنصر التكلفة*.</span><span class="sxs-lookup"><span data-stu-id="46c1e-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="46c1e-131">على سبيل المثال، لديك بنية دليل حسابات الولايات المتحدة (COA) وهو عبارة عن قاعدة للتقارير التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="46c1e-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="46c1e-132">يتم استخدام COA كبعد عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="46c1e-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="46c1e-133">ويتم تمثيل الحسابات، وهي عناصر التكلفة الأساسية، كأعضاء أبعاد عنصر التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="46c1e-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="46c1e-134">تظهر لقطة الشاشة التالية للحسابات الرئيسية كبعد عنصر التكلفة مع حساباته الرئيسية الفعلية كأعضاء أبعاد عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="46c1e-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="46c1e-135">[![لقطة شاشة للحسابات الرئيسية كبعد عنصر تكلفة](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="46c1e-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="46c1e-136">استيراد أعضاء أبعاد عنصر التكلفة من خلال موصلات البيانات</span><span class="sxs-lookup"><span data-stu-id="46c1e-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="46c1e-137">لتسهيل عملية إعداد أعضاء أبعاد عنصر التكلفة في محاسبة التكاليف، يمكنك استخدام موصلات البيانات المبنية بشكل مسبق أو قمت أنت ببنائها بشكل مخصص لاسترداد عناصر التكلفة الأساسية من نظام مصدر واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="46c1e-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="46c1e-138">اعتبارات التنفيذ</span><span class="sxs-lookup"><span data-stu-id="46c1e-138">Implementation considerations</span></span>
<span data-ttu-id="46c1e-139">بما أن عناصر التكلفة تمثل أدنى مستوى من تفاصيل التكلفة، يجب التأكد من تضمين عناصر التكلفة المطلوبة لإنشاء التقارير الإدارية عند تنفيذ بنية عناصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="46c1e-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="46c1e-140">قد يكون من الصعب العثور على عدد مناسب من عناصر التكلفة لمراقبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="46c1e-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="46c1e-141">فع وجود الآلاف من عناصر التكلفة قد يكون الصعب مراقبة كل عنصر من عناصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="46c1e-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="46c1e-142">وكبديل لذلك، يمكنك تجميع عناصر التكلفة وإدارة مراقبة التكاليف على المستوى المجمع.</span><span class="sxs-lookup"><span data-stu-id="46c1e-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]