---
title: الجرد الدوري الجزئي للمواقع
description: تقوم خطط الجرد الدوري‬ بإرشاد عمليات الجرد الفعلية. يمكنك أن تطلب جرد منتجات ومتغيرات منتجات معينة فقط بدلاً من المخزون الفعلي‬ بكامله في أحد المواقع.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46365f618b13c2bcaef9a45d2a835fda27019857
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759997"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="67034-104">الجرد الدوري الجزئي للمواقع</span><span class="sxs-lookup"><span data-stu-id="67034-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67034-105">تقوم خطط الجرد الدوري‬ بإرشاد عمليات الجرد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="67034-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="67034-106">يمكنك أن تطلب جرد منتجات ومتغيرات منتجات معينة فقط بدلاً من المخزون الفعلي‬ بكامله في أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="67034-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="67034-107">باستخدام خطط الجرد الدوري‬ لإنشاء عمل الجرد، يمكنك إرشاد عمليات الجرد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="67034-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="67034-108">يمكنك أن تطلب جرد منتجات ومتغيرات منتجات معينة فقط بدلاً من المخزون الفعلي‬ بكامله في أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="67034-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="67034-109">باستطاعة مدير المستودع، من خلال تصفية منتجات معينة، تقليل مصروفات المراجعة وتجنب أخطاء الدمج وتوفير الوقت.</span><span class="sxs-lookup"><span data-stu-id="67034-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="67034-110">كيفية تكوين جرد دوري لموقع جزئي</span><span class="sxs-lookup"><span data-stu-id="67034-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="67034-111">عند استخدام معالجة عمل المستودع لعمليات الجرد، يتم إنشاء رأس عمل لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="67034-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="67034-112">عندما تقوم بتعريف خطة الجرد الدوري، يمكنك استخدام استعلام **تحديد المواقع‬** لتقييد عمل الجرد الدوري الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="67034-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="67034-113">عندما تقوم بتحديد منتجات لخطة الجرد الدوري، يمكنك تحديد استعلامات المنتجات ومتغيرات المنتجات لضبط ما يتم جرده.</span><span class="sxs-lookup"><span data-stu-id="67034-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="67034-114">يمكنك ربط **قالب عمل** بخطة جرد دوري لتحديد كيفية إنشاء عمل الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="67034-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="67034-115">تتم الإشارة إلى قالب العمل الخاص بعمليات الجرد مباشرة من خطة الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="67034-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="67034-116">عندما تقوم بتعريف تفاصيل قالب العمل، يمكنك استخدام الخيار **فواصل بنود العمل** لتحديد ما إذا كان يجب تجميع بنود عمل الجرد حسب رقم الصنف أو رقم متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="67034-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="67034-117">أنت تحتاج إلى تنفيذ عملية الإعداد إذا كنت تريد فقط جرد المخزون الفعلي لمنتجات معينة في موقع ما.</span><span class="sxs-lookup"><span data-stu-id="67034-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="67034-118">ستكون لبنود عمل الجرد الدوري التي يتم إنشاؤها مستوى المعلومات الذي تحدده هنا، وستتم معالجة عملية جرد الموجهة، استنادًا إلى هذا المستوى.</span><span class="sxs-lookup"><span data-stu-id="67034-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="67034-119">إذا قمت بربط خطط الجرد الدوري بقوالب العمل باستخدام الخيار **فواصل بنود العمل**، فسيتم تحديد الحقل **جرد دوري جزئي‬** لعمل الجرد الدوري الذي تم إنشاؤه، وسيتم إنشاء بنود عمل جرد دوري متعددة استنادًا إلى تعريف قالب العمل.</span><span class="sxs-lookup"><span data-stu-id="67034-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="67034-120">قبل أن تتم معالجة عمل الجرد الدوري الجزئي، يجب عليك، بالحد الأدنى، تحديد **عرض رقم الصنف** لعنصر قائمة الجهاز المحمول كجزء من إعداد الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="67034-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="67034-121">سوف تتم مطالبة عامل المستودع بتسجيل معلومات الجرد التي ترتبط فقط ببنود الجرد (أرقام الأصناف وأبعاد المنتج).</span><span class="sxs-lookup"><span data-stu-id="67034-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="67034-122">وسيتم تجاهل المخزون الفعلي بكامله لعملية الجرد هذه.</span><span class="sxs-lookup"><span data-stu-id="67034-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="67034-123">بالنسبة لعملية الجرد الدوري الجزئي، لن يتم تحديث تاريخ/وقت **الجرد الدوري الأخير** للموقع، على الرغم من إجراء جرد لجميع الأصناف المتوفرة في موقع معين.</span><span class="sxs-lookup"><span data-stu-id="67034-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location, even though all the items on hand at a given location are counted.</span></span> <span data-ttu-id="67034-124">لا يأخذ الجرد الدوري الجزئي في الاعتبار المعلمة **عدد الأيام بين الجرد الدوري** في صفحة **خطط الجرد الدوري**.</span><span class="sxs-lookup"><span data-stu-id="67034-124">The partial cycle count doesn't consider the parameter **Days between cycle counting** on  the **Cycle count plans** page.</span></span> <span data-ttu-id="67034-125">لا يدعم الجرد الدوري الجزئي الجرد المتزامن لأصناف متعددة في نفس الموقع.</span><span class="sxs-lookup"><span data-stu-id="67034-125">Partial cycle count doesn't support simultaneous counting of multiple items at the same location.</span></span> <span data-ttu-id="67034-126">قد ينتج عن وظيفة الجرد الدوري الجزئي إجراء جرد للموقع نفسه عدة مرات لصنف ما عند تشغيل **معالجة خطة الجرد الدوري**.</span><span class="sxs-lookup"><span data-stu-id="67034-126">Partial cycle count functionality may result in the same location being counted multiple times for an item when **Process cycle counting plan** is run.</span></span> <span data-ttu-id="67034-127">لتجنب هذا السيناريو، حدد عوامل التصفية في الحقل **تحديد المواقع**.</span><span class="sxs-lookup"><span data-stu-id="67034-127">To avoid that scenario, specify filters in the **Select locations** field.</span></span>

## <a name="example"></a><span data-ttu-id="67034-128">مثال</span><span class="sxs-lookup"><span data-stu-id="67034-128">Example</span></span>
<span data-ttu-id="67034-129">على سبيل المثال، يجب أن يتم جرد رقم الصنف A0001 فقط في المستودع 61.</span><span class="sxs-lookup"><span data-stu-id="67034-129">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="67034-130">يتم إنشاء قالب عمل جديد للجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="67034-130">A new work template for cycle counting is created.</span></span> <span data-ttu-id="67034-131">يُستخدم الخيار **فواصل بنود العمل‬** لتجميع بنود عمل الجرد حسب رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="67034-131">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="67034-132">وبالتالي، سيتضمن عمل الجرد الدوري الذي تم إنشاؤه بنودًا لكل رقم صنف.</span><span class="sxs-lookup"><span data-stu-id="67034-132">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="67034-133">يمكنك أيضًا تجميع البنود حسب رقم متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="67034-133">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="67034-134">يتم إنشاء خطة جرد دوري جديدة تشير إلى قالب العمل الذي تم إنشاؤه حديثًا.</span><span class="sxs-lookup"><span data-stu-id="67034-134">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="67034-135">تتضمن خطة الجرد الدوري كافة المواقع في المستودع 61 (استعلام **تحديد المواقع**) التي تتضمن مخزون رقم الصنف A0001.</span><span class="sxs-lookup"><span data-stu-id="67034-135">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="67034-136">يتحدد اختيار منتجات معينة في المقطع **اختيارات المنتجات لخطة الجرد الدوري‬**.</span><span class="sxs-lookup"><span data-stu-id="67034-136">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="67034-137">يمكنك اختيار المنتجات لخطط الجرد الدوري عن طريق تعيين حقل **‬‏‫المواقع الفارغة** إلى **‬‏‫استبعاد الفارغ**.</span><span class="sxs-lookup"><span data-stu-id="67034-137">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="67034-138">عندما تتم معالجة خطة الجرد الدوري، يتم إنشاء عمل جرد دوري جزئي لرقم صنف A0001.‬</span><span class="sxs-lookup"><span data-stu-id="67034-138">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="67034-139">يمكن تنفيذ عملية الجرد الفعلي باستخدام عنصر قائمة جهاز محمول للجرد الدوري الموجه.</span><span class="sxs-lookup"><span data-stu-id="67034-139">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="67034-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="67034-140">Additional resources</span></span>
--------

[<span data-ttu-id="67034-141">الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="67034-141">Cycle counting</span></span>](cycle-counting.md)

