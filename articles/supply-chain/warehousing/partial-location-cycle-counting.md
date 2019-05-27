---
title: الجرد الدوري الجزئي للمواقع
description: تقوم خطط الجرد الدوري‬ بإرشاد عمليات الجرد الفعلية. يمكنك أن تطلب جرد منتجات ومتغيرات منتجات معينة فقط بدلاً من المخزون الفعلي‬ بكامله في أحد المواقع.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570564"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="b9c0f-104">الجرد الدوري الجزئي للمواقع</span><span class="sxs-lookup"><span data-stu-id="b9c0f-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9c0f-105">تقوم خطط الجرد الدوري‬ بإرشاد عمليات الجرد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="b9c0f-106">يمكنك أن تطلب جرد منتجات ومتغيرات منتجات معينة فقط بدلاً من المخزون الفعلي‬ بكامله في أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="b9c0f-107">باستخدام خطط الجرد الدوري‬ لإنشاء عمل الجرد، يمكنك إرشاد عمليات الجرد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="b9c0f-108">يمكنك أن تطلب جرد منتجات ومتغيرات منتجات معينة فقط بدلاً من المخزون الفعلي‬ بكامله في أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="b9c0f-109">باستطاعة مدير المستودع، من خلال تصفية منتجات معينة، تقليل مصروفات المراجعة وتجنب أخطاء الدمج وتوفير الوقت.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="b9c0f-110">كيفية تكوين جرد دوري لموقع جزئي</span><span class="sxs-lookup"><span data-stu-id="b9c0f-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="b9c0f-111">عند استخدام معالجة عمل المستودع لعمليات الجرد، يتم إنشاء رأس عمل لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="b9c0f-112">عندما تقوم بتعريف خطة الجرد الدوري، يمكنك استخدام استعلام **تحديد المواقع‬** لتقييد عمل الجرد الدوري الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="b9c0f-113">عندما تقوم بتحديد منتجات لخطة الجرد الدوري، يمكنك تحديد استعلامات المنتجات ومتغيرات المنتجات لضبط ما يتم جرده.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="b9c0f-114">يمكنك ربط **قالب عمل** بخطة جرد دوري لتحديد كيفية إنشاء عمل الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="b9c0f-115">تتم الإشارة إلى قالب العمل الخاص بعمليات الجرد مباشرة من خطة الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="b9c0f-116">عندما تقوم بتعريف تفاصيل قالب العمل، يمكنك استخدام الخيار **فواصل بنود العمل** لتحديد ما إذا كان يجب تجميع بنود عمل الجرد حسب رقم الصنف أو رقم متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="b9c0f-117">أنت تحتاج إلى تنفيذ عملية الإعداد إذا كنت تريد فقط جرد المخزون الفعلي لمنتجات معينة في موقع ما.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="b9c0f-118">ستكون لبنود عمل الجرد الدوري التي يتم إنشاؤها مستوى المعلومات الذي تحدده هنا، وستتم معالجة عملية جرد الموجهة، استنادًا إلى هذا المستوى.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="b9c0f-119">إذا قمت بربط خطط الجرد الدوري بقوالب العمل باستخدام الخيار **فواصل بنود العمل**، فسيتم تحديد الحقل **جرد دوري جزئي‬** لعمل الجرد الدوري الذي تم إنشاؤه، وسيتم إنشاء بنود عمل جرد دوري متعددة استنادًا إلى تعريف قالب العمل.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="b9c0f-120">قبل أن تتم معالجة عمل الجرد الدوري الجزئي، يجب عليك، بالحد الأدنى، تحديد **عرض رقم الصنف** لعنصر قائمة الجهاز المحمول كجزء من إعداد الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="b9c0f-121">سوف تتم مطالبة عامل المستودع بتسجيل معلومات الجرد التي ترتبط فقط ببنود الجرد (أرقام الأصناف وأبعاد المنتج).</span><span class="sxs-lookup"><span data-stu-id="b9c0f-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="b9c0f-122">وسيتم تجاهل المخزون الفعلي بكامله لعملية الجرد هذه.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="b9c0f-123">بالنسبة إلى عملية الجرد الدوري الجزئي، لن يتم تحديث تاريخ/وقت **آخر جرد دوري‬** للموقع.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="b9c0f-124">مثال</span><span class="sxs-lookup"><span data-stu-id="b9c0f-124">Example</span></span>
<span data-ttu-id="b9c0f-125">على سبيل المثال، يجب أن يتم جرد رقم الصنف A0001 فقط في المستودع 61.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="b9c0f-126">يتم إنشاء قالب عمل جديد للجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="b9c0f-127">يُستخدم الخيار **فواصل بنود العمل‬** لتجميع بنود عمل الجرد حسب رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="b9c0f-128">وبالتالي، سيتضمن عمل الجرد الدوري الذي تم إنشاؤه بنودًا لكل رقم صنف.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="b9c0f-129">يمكنك أيضًا تجميع البنود حسب رقم متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="b9c0f-130">يتم إنشاء خطة جرد دوري جديدة تشير إلى قالب العمل الذي تم إنشاؤه حديثًا.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="b9c0f-131">تتضمن خطة الجرد الدوري كافة المواقع في المستودع 61 (استعلام **تحديد المواقع**) التي تتضمن مخزون رقم الصنف A0001.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="b9c0f-132">يتحدد اختيار منتجات معينة في المقطع **اختيارات المنتجات لخطة الجرد الدوري‬**.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="b9c0f-133">يمكنك اختيار المنتجات لخطط الجرد الدوري عن طريق تعيين حقل **‬‏‫المواقع الفارغة** إلى **‬‏‫استبعاد الفارغ**.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="b9c0f-134">عندما تتم معالجة خطة الجرد الدوري، يتم إنشاء عمل جرد دوري جزئي لرقم صنف A0001.‬</span><span class="sxs-lookup"><span data-stu-id="b9c0f-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="b9c0f-135">يمكن تنفيذ عملية الجرد الفعلي باستخدام عنصر قائمة جهاز محمول للجرد الدوري الموجه.</span><span class="sxs-lookup"><span data-stu-id="b9c0f-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="b9c0f-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b9c0f-136">Additional resources</span></span>
--------

[<span data-ttu-id="b9c0f-137">الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="b9c0f-137">Cycle counting</span></span>](cycle-counting.md)

