---
title: تقدير تكلفة أمر الإنتاج
description: توفر هذه المقالة معلومات حول تقدير تكلفة الإنتاج. يزودك تقدير تكلفة الإنتاج بتكاليف المواد المرتقبة واستهلاك القدرة لإنتاج صنف في كمية أمر الإنتاج المخطط.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a101f82e60113941d389421b19cddc1ad123ce9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214495"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="30824-104">تقدير تكلفة أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="30824-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30824-105">توفر هذه المقالة معلومات حول تقدير تكلفة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="30824-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="30824-106">يزودك تقدير تكلفة الإنتاج بتكاليف المواد المرتقبة واستهلاك القدرة لإنتاج صنف في كمية أمر الإنتاج المخطط.</span><span class="sxs-lookup"><span data-stu-id="30824-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="30824-107">بعد إنشاء أمر إنتاج، يجب تقدير تكاليف الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="30824-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="30824-108">ويهدف ذلك إلى تقدير استهلاك الأصناف والمسارات فيما يتعلق بعملية الإنتاج، إذ يتم استخدام هذه التقديرات كأساس لعمليات الجدولة والإنتاج التالية.</span><span class="sxs-lookup"><span data-stu-id="30824-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="30824-109">تقدير تكلفة الإنتاج</span><span class="sxs-lookup"><span data-stu-id="30824-109">Production cost estimation</span></span>
<span data-ttu-id="30824-110">تستند تقديرات تكاليف الإنتاج إلى المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="30824-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="30824-111">كمية أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="30824-111">The quantity on the production order</span></span>
-   <span data-ttu-id="30824-112">المكونات على قائمة مكونات الصنف الخاصة بالإنتاج</span><span class="sxs-lookup"><span data-stu-id="30824-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="30824-113">عمليات التوجيه في مسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="30824-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="30824-114">التكاليف غير المباشرة التي تنطبق على المكونات والعمليات</span><span class="sxs-lookup"><span data-stu-id="30824-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="30824-115">بيانات التكلفة النشطة اعتبارًا من تاريخ الحساب</span><span class="sxs-lookup"><span data-stu-id="30824-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="30824-116">في حال وجود صنف بند وهمي في قائمة مكونات الصنف الخاصة بالإنتاج، تقوم الحسابات بعكس مكونات الصنف الوهمي وعمليات مساره.</span><span class="sxs-lookup"><span data-stu-id="30824-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="30824-117">يمكنك استخدام مهمة التقدير لإعادة حساب التكاليف التقديرية بحيث تعكس المعلومات المحدّثة.</span><span class="sxs-lookup"><span data-stu-id="30824-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="30824-118">على سبيل المثال، قد تكون المعلومات المحدّثة تغييرات في كمية أمر الإنتاج، أو المكونات في قائمة مكونات الصنف الخاصة بالإنتاج، أو عمليات التوجيه في مسار الإنتاج، أو التكاليف غير المباشرة التي تنطبق على هذه المكونات والعمليات، أو بيانات التكلفة النشطة اعتبارًا من تاريخ إعادة الحساب.</span><span class="sxs-lookup"><span data-stu-id="30824-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="30824-119">وتقترح أيضًا حسابات التكلفة التقديرية سعرًا لمبيعات صنف الإنتاج استنادًا إلى منهج التكلفة إضافة إلى زيادة السعر.</span><span class="sxs-lookup"><span data-stu-id="30824-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="30824-120">بإمكان حسابات التكلفة التقديرية أن تنطبق بشكل اختياري على أوامر مرجعية تعكس أوامر إنتاج أخرى ترتبط بأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="30824-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="30824-121">اعرض التكاليف التقديرية</span><span class="sxs-lookup"><span data-stu-id="30824-121">View the estimated costs</span></span>
<span data-ttu-id="30824-122">بعد تشغيل التقدير، يمكنك عرض النتائج في صفحة **حساب السعر**.</span><span class="sxs-lookup"><span data-stu-id="30824-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="30824-123">يحسب التقدير القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="30824-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="30824-124">**تكلفة الإنتاج** - تكلفة الإنتاج هي البند الأول في التقدير.</span><span class="sxs-lookup"><span data-stu-id="30824-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="30824-125">حيث توضح التكلفة الكاملة لتشغيل أمر الإنتاج وسعر إجمالي المبيعات للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="30824-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="30824-126">وهي مجموع كافة بنود التكلفة في التقدير.</span><span class="sxs-lookup"><span data-stu-id="30824-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="30824-127">**تكاليف المسارات أو الموارد** – تكاليف المسارات أو الموارد هي تكاليف عمليات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="30824-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="30824-128">وهي تشمل تكلفة عناصر مثل وقت الإعداد ووقت التشغيل والنفقات العامة.</span><span class="sxs-lookup"><span data-stu-id="30824-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="30824-129">**تكاليف المواد** - تكاليف المواد هي تكاليف وأسعار قائمة مكونات الصنف اللازمة لإنتاج الصنف.</span><span class="sxs-lookup"><span data-stu-id="30824-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="30824-130">وقد تم إنشاء هذه التكاليف في السابق وإدخالها في النظام.</span><span class="sxs-lookup"><span data-stu-id="30824-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="30824-131">استخدامات أخرى لتقدير التكلفة</span><span class="sxs-lookup"><span data-stu-id="30824-131">Other uses of cost estimation</span></span>
<span data-ttu-id="30824-132">يوفر أيضًا تقدير التكلفة المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="30824-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="30824-133">عروض أسعار ذات معنى</span><span class="sxs-lookup"><span data-stu-id="30824-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="30824-134">تقديرات لربحية الأمر</span><span class="sxs-lookup"><span data-stu-id="30824-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="30824-135">تقديرات لاستخدام المواد الخام</span><span class="sxs-lookup"><span data-stu-id="30824-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="30824-136">مقارنات بين معلومات التكلفة من عمليات إنتاج سابقة</span><span class="sxs-lookup"><span data-stu-id="30824-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="30824-137">معلومات الميزانية والتنبؤ</span><span class="sxs-lookup"><span data-stu-id="30824-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="30824-138">تقديرات لحجم الإنتاج اللازم للحفاظ على تكلفة معينة</span><span class="sxs-lookup"><span data-stu-id="30824-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




