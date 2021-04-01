---
title: تزويد حد المنطقة
description: يستخدم التزويد المستند إلى المنطقة استراتيجية التزويد بالحد الأدنى/الحد الأقصى (min/max)، ولكنها تقوم بتقييم مناطق المستودع بالكامل بدلا من المواقع الفردية فقط. بالتالي، يمكن لمديري المستودع أن يعلم بشكل أسرع متى تكون هناك حاجة إلى مخزون إضافي في منطقة الانتقاء.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6aaa139fb206c035b25b7056e681d086fde6447f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245048"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="b1359-104">تزويد حد المنطقة</span><span class="sxs-lookup"><span data-stu-id="b1359-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1359-105">يستخدم التزويد المستند إلى المنطقة استراتيجية [التزويد](replenishment.md) بالحد الأدنى/الحد الأقصى (min/max)، ولكنها تقوم بتقييم مناطق المستودع بالكامل بدلا من المواقع الفردية فقط.</span><span class="sxs-lookup"><span data-stu-id="b1359-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="b1359-106">بالتالي، يمكن لمديري المستودع أن يعلم بشكل أسرع متى تكون هناك حاجة إلى مخزون إضافي في منطقة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="b1359-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="b1359-107">ويشبه إعداد هذه الميزة الإعداد الخاص بالتزويد المعتمد على الموقع.</span><span class="sxs-lookup"><span data-stu-id="b1359-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="b1359-108">ومع ذلك، عندما تقوم بإعداد قالب تزويد الحد الأدنى/الأقصى، يمكنك أيضا تحديد ما إذا كان يجب تقييم الحد لكل موقع أو لكل منطقة.</span><span class="sxs-lookup"><span data-stu-id="b1359-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="b1359-109">إذا قمت بإعداد تقييم يستند إلى المناطق، فيجب إضافة مناطق معينة إلى استعلام تحديد المنطقة.</span><span class="sxs-lookup"><span data-stu-id="b1359-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="b1359-110">كمثل تزويد الحد الأقصى/الأدنى المستند إلى الموقع، فإن تزويد الحد الأقصى/الأدنى المستند إلى المنطقة يعتمد على أدنى حد للمخزون والذي يشغل إنشاء عمل تزويد للأصناف المحددة.</span><span class="sxs-lookup"><span data-stu-id="b1359-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="b1359-111">سيزيد عمل التزويد هذا من المخزون إلى الحد الأقصى المحدد للمنطقة.</span><span class="sxs-lookup"><span data-stu-id="b1359-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="b1359-112">لا يتم دعم عمليات تزويد المناطق الخاصة بمتغيرات المنتج في الإصدار الحالي.</span><span class="sxs-lookup"><span data-stu-id="b1359-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="b1359-113">بخلاف تزويد الحد الأقصى/الأدنى المستند إلى الموقع، فإن تزويد الحد الأقصى/الأدنى المستند إلى المنطقة يتطلب مواقع ثابتة لتقييم ما إذا كان يجب على المواقع تخزين صنف معين أم لا.</span><span class="sxs-lookup"><span data-stu-id="b1359-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="b1359-114">بالتالي، يسمح التزويد المستند إلى المنطقة باستخدام تزويد الحد الأدنى/الأقصى حتى إذا لم يكن لديك مواقع ثابتة لكل صنف أو متغير صنف في المستودع.</span><span class="sxs-lookup"><span data-stu-id="b1359-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="b1359-115">عندما تقل كمية في المنطقة عن الحد الأدنى المحدد، يتم إنشاء عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="b1359-116">ستحدد توجيهات المواقع الموقع المحدد الذي يجب وضع المخزون فيه.</span><span class="sxs-lookup"><span data-stu-id="b1359-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="b1359-117">تشغيل ميزة التزويد حسب حد المنطقة</span><span class="sxs-lookup"><span data-stu-id="b1359-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="b1359-118">قبل أن تتمكن من استخدام ميزة *التزويد حسب حد المنطقة*، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b1359-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b1359-119">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b1359-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b1359-120">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b1359-121">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="b1359-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b1359-122">**اسم الميزة:** *التزويد حسب حد المنطقة*</span><span class="sxs-lookup"><span data-stu-id="b1359-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="b1359-123">إعداد التزويد المعتمد على المنطقة</span><span class="sxs-lookup"><span data-stu-id="b1359-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="b1359-124">لإعداد تزويد يعتمد على المنطقة، يجب تكوين العديد من أجزاء النظام.</span><span class="sxs-lookup"><span data-stu-id="b1359-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="b1359-125">يقدم هذا القسم الإعدادات المختلفة ويوفر قيم البيانات التوضيحية التي يمكنك إدخالها إذا كنت تريد العمل بالسيناريو الموجود في نهاية هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b1359-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="b1359-126">إعداد أكواد التوجيه</span><span class="sxs-lookup"><span data-stu-id="b1359-126">Set up directive codes</span></span>

<span data-ttu-id="b1359-127">[أكواد التوجيه](control-warehouse-location-directives.md) تتيح لك أن تكون أكثر تحديدًا عندما تقوم بتعريف قالب الموقع الذي يتم استخدامه في قالب العمل.</span><span class="sxs-lookup"><span data-stu-id="b1359-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="b1359-128">يحدد كل كود قيمة عامة يمكنك الرجوع إليها عند تكوين كل نوع من القوالب.</span><span class="sxs-lookup"><span data-stu-id="b1359-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="b1359-129">عرض وتحرير أكواد التوجيه</span><span class="sxs-lookup"><span data-stu-id="b1359-129">View and edit directive codes</span></span>

<span data-ttu-id="b1359-130">لعرض أو تحرير أكواد التوجيه الخاصة بك، انتقل إلى **إدارة المستودعات \> الإعداد \> أكواد التوجيه**.</span><span class="sxs-lookup"><span data-stu-id="b1359-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="b1359-131">إعداد أكواد التوجيه لبيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="b1359-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="b1359-132">يوضح هذا المثال كيفية تجهيز أكواد التوجيه.</span><span class="sxs-lookup"><span data-stu-id="b1359-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="b1359-133">إذا كنت تخطط للعمل بالسيناريو الموجود في نهاية هذا الموضوع، فاستخدم قيم البيانات التوضيحية المتوفرة هنا.</span><span class="sxs-lookup"><span data-stu-id="b1359-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b1359-134">خلاف ذلك، استخدم القيم الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b1359-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b1359-135">حدد الكيان القانوني **USMF** للعمل بالبيانات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="b1359-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b1359-136">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> أكواد التوجيه**.</span><span class="sxs-lookup"><span data-stu-id="b1359-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="b1359-137">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-138">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-139">**كود التوجيه:** _تزويد حسب المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="b1359-140">**وصف التوجيه:** _تزويد حسب المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="b1359-141">حدد **حفظ** لحفظ الكود الجديد.</span><span class="sxs-lookup"><span data-stu-id="b1359-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="b1359-142">إعداد قوالب التزويد</span><span class="sxs-lookup"><span data-stu-id="b1359-142">Set up replenishment templates</span></span>

<span data-ttu-id="b1359-143">تُعد [قوالب الحد الأدنى/الحد الأقصى لعملية التزويد](tasks/set-up-min-max-replenishment-process.md) الآلية الرئيسية للحفاظ على المستويات المثلى في مواقع الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="b1359-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="b1359-144">في هذه القوالب، يجب عليك إعداد القواعد التي سيتم استخدامها لتزويد المخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="b1359-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="b1359-145">يتضمن التزويد الذي يمكن استخدام القوالب فيه التزويد المستند إلى المنطقة.</span><span class="sxs-lookup"><span data-stu-id="b1359-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="b1359-146">عرض قوالب التزويد وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="b1359-146">View and edit replenishment templates</span></span>

<span data-ttu-id="b1359-147">قالب التزويد هو مجموعة من القواعد التي تتحكم متى وكيف يتم تزويد الموقع.</span><span class="sxs-lookup"><span data-stu-id="b1359-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="b1359-148">وعليك اختيار قالب للتحكم في متى وكيف يتم إجراء التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="b1359-149">لعرض أو تحرير قوالب التزويد، انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="b1359-150">تجهيز قالب تزويد بالبيانات التجريبية</span><span class="sxs-lookup"><span data-stu-id="b1359-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="b1359-151">يوضح هذا المثال كيفية تجهيز قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="b1359-152">إذا كنت تخطط للعمل بالسيناريو الموجود في نهاية هذا الموضوع، فاستخدم قيم البيانات التوضيحية المتوفرة هنا.</span><span class="sxs-lookup"><span data-stu-id="b1359-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b1359-153">خلاف ذلك، استخدم القيم الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b1359-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b1359-154">حدد الكيان القانوني **USMF** للعمل بالبيانات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="b1359-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b1359-155">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="b1359-156">حدد **تحرير** لوضع الصفحة في وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="b1359-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="b1359-157">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى شبكة **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="b1359-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="b1359-158">في الصف الجديد، عيّن القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b1359-158">In the new row, set the following values.</span></span> <span data-ttu-id="b1359-159">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="b1359-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b1359-160">**قالب التزويد:** _تزويد الحد الأدنى/الأقصى حسب المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="b1359-161">**الوصف:** _تزويد الحد الأدنى/الأقصى حسب المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="b1359-162">**نوع التزويد:** _الحد الأدنى أو الحد الأقصى_</span><span class="sxs-lookup"><span data-stu-id="b1359-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="b1359-163">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b1359-163">Select **Save**.</span></span>
1. <span data-ttu-id="b1359-164">بينما لا يزال الصف الجديد محددًا في شبكة **النظرة العامة**، حدد **جديد** أعلى شبكة **تفاصيل قالب التزويد** لإضافة صف مرتبط بقالب التزويد *تزويد الحد الأدنى/الأقصى حسب المنطقة* الذي قمت بإنشائه للتو.</span><span class="sxs-lookup"><span data-stu-id="b1359-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="b1359-165">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-166">**رقم المسلسل:** أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="b1359-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b1359-167">**الوصف:** أدخل _انتقاء تزويد حسب المنطقة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="b1359-168">**وحدة التزويد:** حدد _وحدة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="b1359-169">**نوع الطلب** – اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b1359-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="b1359-170">**كود التوجيه:** يربط هذا الحقل قالب التزويد بتوجيه موقع.</span><span class="sxs-lookup"><span data-stu-id="b1359-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="b1359-171">حدد كود التوجيه الخاص ببيانات العرض التوضيحي الذي قمت بإنشائه سابقا (_تزويد حسب المنطقة_).</span><span class="sxs-lookup"><span data-stu-id="b1359-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="b1359-172">**قالب العمل:** – اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b1359-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="b1359-173">**الحد الأدنى للكمية:** يعين هذا الحقل الكمية التي سيتم تشغيل التزويد عندها.</span><span class="sxs-lookup"><span data-stu-id="b1359-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="b1359-174">أدخل _50_.</span><span class="sxs-lookup"><span data-stu-id="b1359-174">Enter _50_.</span></span>
    - <span data-ttu-id="b1359-175">**الحد الأقصى للكمية:** يعين هذا الحقل الحد الأقصى لكمية الصنف التي يمكن أن تكون موجودة في إحدى المناطق.</span><span class="sxs-lookup"><span data-stu-id="b1359-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="b1359-176">يؤدي عمل التزويد الذي تم إنشاؤه إلى زيادة المخزون إلى هذه الكمية.</span><span class="sxs-lookup"><span data-stu-id="b1359-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="b1359-177">أدخل _150_.</span><span class="sxs-lookup"><span data-stu-id="b1359-177">Enter _150_.</span></span>
    - <span data-ttu-id="b1359-178">**الوحدة:** يعين هذا الحقل وحدة قيم الحد الأدنى والحد الأقصى.</span><span class="sxs-lookup"><span data-stu-id="b1359-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="b1359-179">حدد _وحدة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-179">Select _ea_.</span></span>
    - <span data-ttu-id="b1359-180">**زيادة الطلب:** حدد _تقريب لأعلى_.</span><span class="sxs-lookup"><span data-stu-id="b1359-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="b1359-181">**تزويد المواقع الثابتة الفارغة:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="b1359-182">**تزويد المواقع الثابتة فقط:** قم بإلغاء اختيار خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-183">**وضع استعلام المنتج:** قم بتحديد _استعلام المنتج_.</span><span class="sxs-lookup"><span data-stu-id="b1359-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="b1359-184">**مجال حد التزويد:** يحدد هذا الحقل ما إذا كان يجب أن يتم تقييم القالب حسب المنطقة أو حسب الموقع المحدد.</span><span class="sxs-lookup"><span data-stu-id="b1359-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="b1359-185">حدد _المنطقة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-185">Select _Zone_.</span></span>
    - <span data-ttu-id="b1359-186">**المستودع:** حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="b1359-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="b1359-187">حدد **تحديد المنتجات** أعلى شبكة **تفاصيل قالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b1359-188">في مربع حوار **استعلام المنتج**، ضمن علامة التبويب **النطاق**، حدد **إضافة** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-189">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-190">**الجدول:** _الأصناف_</span><span class="sxs-lookup"><span data-stu-id="b1359-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="b1359-191">**الجدول المشتق:** _الأصناف_</span><span class="sxs-lookup"><span data-stu-id="b1359-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="b1359-192">**الحقل:** _رقم الصنف_</span><span class="sxs-lookup"><span data-stu-id="b1359-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="b1359-193">**المعايير:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="b1359-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="b1359-194">حدد **موافق** لحفظ الاستعلام الخاص بك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b1359-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b1359-195">حدد **تحديد المناطق اللتزويد** أعلى شبكة **تفاصيل قالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b1359-196">في مربع حوار **استعلام المنطقة**، ضمن علامة التبويب **النطاق**، أصف صفًا إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-197">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-198">**الجدول:** _منطقة المستودع_</span><span class="sxs-lookup"><span data-stu-id="b1359-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b1359-199">**الجدول المشتق:** _منطقة المستودع_</span><span class="sxs-lookup"><span data-stu-id="b1359-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b1359-200">**الحقل:** _معرف المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b1359-201">**المعايير:** _الأرضية_</span><span class="sxs-lookup"><span data-stu-id="b1359-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b1359-202">حدد **موافق** لحفظ الاستعلام الخاص بك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b1359-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="b1359-203">إعداد توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="b1359-203">Set up location directives</span></span>

<span data-ttu-id="b1359-204">بخلاف التزويد بالحد الأدنى/الأقصى المستند إلى الموقع، فإن التزويد بالحد الأدنى/الأقصى المعتمد على المنطقة يتطلب أن تقوم بإعداد كلا من توجيهات موقع الانتقاء وتوجيهات موقع الوضع، لأن النظام يقيّم المنطقة بأكملها بدلا من موقع الانتقاء للعمل الصادر فقط.</span><span class="sxs-lookup"><span data-stu-id="b1359-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="b1359-205">عرض توجيهات المواقع وتحريرها</span><span class="sxs-lookup"><span data-stu-id="b1359-205">View and edit location directives</span></span>

<span data-ttu-id="b1359-206">لعرض أو تحرير توجيهات الموقع، انتقل إلى **إدارة المستودعات \> الإعداد \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b1359-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="b1359-207">للحصول على أمثلة توضح كيفية استخدام الإعدادات لإنشاء توجيهات موقع الانتقاء المطلوبة وتوجيهات موقع الوضع، راجع القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="b1359-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="b1359-208">إعداد توجيهات الموقع لبيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="b1359-208">Prepare demo data location directives</span></span>

<span data-ttu-id="b1359-209">لإعداد بيانات العرض التوضيحي بحيث يمكن استخدامها في السيناريو في نهاية هذا الموضوع، يجب إنشاء موجهي موقع: واحد للانتقاء وآخر للوضع.</span><span class="sxs-lookup"><span data-stu-id="b1359-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="b1359-210">إنشاء توجيه انتقاء للتزويد</span><span class="sxs-lookup"><span data-stu-id="b1359-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="b1359-211">حدد الكيان القانوني **USMF** للعمل بالبيانات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="b1359-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b1359-212">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b1359-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b1359-213">في الجزء الأيسر، قم بتعيين حقل **نوع أمر العمل** إلى _التزويد_.</span><span class="sxs-lookup"><span data-stu-id="b1359-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="b1359-214">في جزء الإجراءات، حدد **جديد** لإنشاء توجيه جديد.</span><span class="sxs-lookup"><span data-stu-id="b1359-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="b1359-215">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-215">Set the following values:</span></span>

    - <span data-ttu-id="b1359-216">**الرقم التسلسلي:** قبول القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b1359-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b1359-217">**الاسم:** ادخل _انتقاء المنطقة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="b1359-218">**نوع العمل:** حدد _انتقاء_.</span><span class="sxs-lookup"><span data-stu-id="b1359-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="b1359-219">**الموقع:** حدد _6_.</span><span class="sxs-lookup"><span data-stu-id="b1359-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b1359-220">**المستودع:** حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="b1359-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b1359-221">**كود التوجيه:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b1359-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="b1359-222">**تعدد SKU:** قم بتعييين هذا الخيار إلى _لا_.</span><span class="sxs-lookup"><span data-stu-id="b1359-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b1359-223">حدد **حفظ** لإنشاء توجيه يتضمن الإعدادات التي قمت بتكوينها حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="b1359-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b1359-224">في علامة التبويب السريعة **السطور**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b1359-225">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b1359-226">**رقم المسلسل:** أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="b1359-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b1359-227">**من الكمية:** أدخل _0_.</span><span class="sxs-lookup"><span data-stu-id="b1359-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b1359-228">**إلى الكمية:** أدخل _10000000_.</span><span class="sxs-lookup"><span data-stu-id="b1359-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b1359-229">**الوحدة:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b1359-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b1359-230">**تحديد موقع الكمية:** حدد _بلا_.</span><span class="sxs-lookup"><span data-stu-id="b1359-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b1359-231">**التقييد حسب الوحدة:** قم بإلغاء اختيار هذه الخانة.</span><span class="sxs-lookup"><span data-stu-id="b1359-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-232">**التقريب للوحدة:** قم بإلغاء اختيار هذه الخانة.</span><span class="sxs-lookup"><span data-stu-id="b1359-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-233">**تحديد موقع كمية التعبئة‬:** قم بإلغاء اختيار هذه الخانة.</span><span class="sxs-lookup"><span data-stu-id="b1359-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-234">**السماح بالتقسيم:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b1359-235">حدد **حفظ** لحفظ السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="b1359-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b1359-236">بينما لا يزال البند الجديد محددًا في شبكة **السطور**، حدد **جديد** في علامة التبويب السريعة **إجراءات توجيه الموقع** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-237">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-238">**رقم المسلسل:** أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="b1359-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b1359-239">**الاسم:** أدخل _انتقاء من مجمع_.</span><span class="sxs-lookup"><span data-stu-id="b1359-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="b1359-240">**استخدام الموقع الثابت:** حدد _المواقع الثابتة وغير الثابتة_</span><span class="sxs-lookup"><span data-stu-id="b1359-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b1359-241">**السماح بالمخزون السالب:** قم بإلغاء تحديد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-242">**تمكين الدفعة:** قم بإلغاء تحديد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-243">**الاستراتيجية:** حدد _بلا_.</span><span class="sxs-lookup"><span data-stu-id="b1359-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="b1359-244">حدد **حفظ** لحفظ الإجراء الجديد.</span><span class="sxs-lookup"><span data-stu-id="b1359-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b1359-245">بينما لا يزال الإجراء الجديد محددًا، حدد **تحرير استعلام** أعلى شبكة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b1359-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b1359-246">يظهر مربع حوار الاستعلام، حيث يمكنك تحديد المواقع المطلوب التزويد منها.</span><span class="sxs-lookup"><span data-stu-id="b1359-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="b1359-247">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-248">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-249">**الجدول:** _المواقع_</span><span class="sxs-lookup"><span data-stu-id="b1359-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b1359-250">**الجدول المشتق:** _المواقع_</span><span class="sxs-lookup"><span data-stu-id="b1359-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b1359-251">**الحقل:** _معرف المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b1359-252">**المعايير:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="b1359-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="b1359-253">حدد **موافق** لحفظ الاستعلام الخاص بك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b1359-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b1359-254">حدد **حفظ** لحفظ توجيه الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b1359-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="b1359-255">إنشاء توجيه وضع للتزويد</span><span class="sxs-lookup"><span data-stu-id="b1359-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="b1359-256">في صفحة **توجيهات الموقع**، في الجزء الأيمن، تأكد من أن حقل **نوع أمر العمل** لا يزال معينا على _التزويد_.</span><span class="sxs-lookup"><span data-stu-id="b1359-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="b1359-257">في جزء الإجراءات، حدد **جديد** لإنشاء توجيه آخر.</span><span class="sxs-lookup"><span data-stu-id="b1359-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="b1359-258">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-258">Set the following values:</span></span>

    - <span data-ttu-id="b1359-259">**الرقم التسلسلي:** قبول القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b1359-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b1359-260">**الاسم:** ادخل _وضع المنطقة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b1359-261">**نوع أمر العمل:** حدد _وضع_.</span><span class="sxs-lookup"><span data-stu-id="b1359-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="b1359-262">**الموقع:** حدد _6_.</span><span class="sxs-lookup"><span data-stu-id="b1359-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b1359-263">**المستودع:** حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="b1359-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b1359-264">**كود التوجيه** حدد _تزويد المنطقة_ لربط توجيه الموقع الحالي بقالب التزويد الذي قمت بإنشائه سابقًا باستخدام الكود الذي قمت بإنشائه سابقا.</span><span class="sxs-lookup"><span data-stu-id="b1359-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="b1359-265">**تعدد SKU:** قم بتعييين هذا الخيار إلى _لا_.</span><span class="sxs-lookup"><span data-stu-id="b1359-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b1359-266">حدد **حفظ** لإنشاء توجيه يتضمن الإعدادات التي قمت بتكوينها حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="b1359-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b1359-267">في علامة التبويب السريعة **السطور**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b1359-268">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b1359-269">**رقم المسلسل:** أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="b1359-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b1359-270">**من الكمية:** أدخل _0_.</span><span class="sxs-lookup"><span data-stu-id="b1359-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b1359-271">**إلى الكمية:** أدخل _10000000_.</span><span class="sxs-lookup"><span data-stu-id="b1359-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b1359-272">**الوحدة:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b1359-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b1359-273">**تحديد موقع الكمية:** حدد _بلا_.</span><span class="sxs-lookup"><span data-stu-id="b1359-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b1359-274">**التقييد حسب الوحدة:** قم بإلغاء اختيار هذه الخانة.</span><span class="sxs-lookup"><span data-stu-id="b1359-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-275">**التقريب للوحدة:** قم بإلغاء اختيار هذه الخانة.</span><span class="sxs-lookup"><span data-stu-id="b1359-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-276">**تحديد موقع كمية التعبئة‬:** قم بإلغاء اختيار هذه الخانة.</span><span class="sxs-lookup"><span data-stu-id="b1359-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-277">**السماح بالتقسيم:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b1359-278">حدد **حفظ** لحفظ السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="b1359-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b1359-279">بينما لا يزال البند الجديد محددًا في شبكة **السطور**، حدد **جديد** في علامة التبويب السريعة **إجراءات توجيه الموقع** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-280">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-281">**رقم المسلسل:** أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="b1359-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b1359-282">**الاسم:** ادخل _وضع المنطقة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b1359-283">**استخدام الموقع الثابت:** حدد _المواقع الثابتة وغير الثابتة_</span><span class="sxs-lookup"><span data-stu-id="b1359-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b1359-284">**السماح بالمخزون السالب:** قم بإلغاء تحديد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-285">**تمكين الدفعة:** قم بإلغاء تحديد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="b1359-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b1359-286">**الاستراتيجية:** حدد _دمج_.</span><span class="sxs-lookup"><span data-stu-id="b1359-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="b1359-287">حدد **حفظ** لحفظ الإجراء الجديد.</span><span class="sxs-lookup"><span data-stu-id="b1359-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b1359-288">بينما لا يزال الإجراء الجديد محددًا، حدد **تحرير استعلام** أعلى شبكة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b1359-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b1359-289">يظهر مربع حوار الاستعلام، حيث يمكنك تحديد المنطقة المطلوب التزويد إليها.</span><span class="sxs-lookup"><span data-stu-id="b1359-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="b1359-290">يجب أن تكون هذه المنطقة هي نفس المنطقة المحددة في قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="b1359-291">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b1359-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b1359-292">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b1359-293">**الجدول:** _المواقع_</span><span class="sxs-lookup"><span data-stu-id="b1359-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b1359-294">**الجدول المشتق:** _المواقع_</span><span class="sxs-lookup"><span data-stu-id="b1359-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b1359-295">**الحقل:** _معرف المنطقة_</span><span class="sxs-lookup"><span data-stu-id="b1359-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b1359-296">**المعايير:** _الأرضية_</span><span class="sxs-lookup"><span data-stu-id="b1359-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b1359-297">حدد **موافق** لحفظ الاستعلام الخاص بك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b1359-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b1359-298">حدد **حفظ** لحفظ توجيه الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b1359-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="b1359-299">سيناريو</span><span class="sxs-lookup"><span data-stu-id="b1359-299">Scenario</span></span>

<span data-ttu-id="b1359-300">يوفر هذا القسم سيناريو نموذجي يوضح كيفية العمل مع الميزة.</span><span class="sxs-lookup"><span data-stu-id="b1359-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="b1359-301">إعداد نموذج البيانات المطلوب لسيناريو المثال</span><span class="sxs-lookup"><span data-stu-id="b1359-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="b1359-302">قبل البدء في العمل خلال السيناريو، يجب تنشيط بيانات العينة وإعداد الميزة كما هو موضح في هذا القسم وفي الأقسام السابقة من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b1359-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="b1359-303">استخدام الكيان القانوني USMF</span><span class="sxs-lookup"><span data-stu-id="b1359-303">Use the USMF legal entity</span></span>

<span data-ttu-id="b1359-304">للعمل بالسيناريو باستخدام السجلات والقيم النموذجية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="b1359-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b1359-305">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="b1359-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="b1359-306">تجهيز نموذج بيانات إضافي</span><span class="sxs-lookup"><span data-stu-id="b1359-306">Prepare additional sample data</span></span>

<span data-ttu-id="b1359-307">بعد تحديد الكيان القانوني **USMF**، أضف بيانات المثال الإضافية المطلوبة، كما هو موضح في قسم [إعداد التزويد المعتمد على المنطقة](#setup) الموضح سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b1359-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="b1359-308">التحقق من المخزون الفعلي لديك</span><span class="sxs-lookup"><span data-stu-id="b1359-308">Check your on-hand inventory</span></span>

<span data-ttu-id="b1359-309">اتبع الخطوات التالية للتأكد من أن النظام الخاص بك يتضمن مخزونًا كافيًا لدعم نموذج السيناريو.</span><span class="sxs-lookup"><span data-stu-id="b1359-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="b1359-310">تأكد من وجود مخزون فعلي للصنف *A0001* في موقعين مختلفين في منطقة الانتقاء (*الأرضية*) المحدد في قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="b1359-311">ومع ذلك، يجب أن يكون إجمالي المخزون أقل من الحد الأدنى المطلوب للكمية (*50*) المحدد في قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="b1359-312">بهذه الطريقة، يمكنك محاكاة كيفية حدوث العملية الحسابية للمنطقة بالكامل بدلا من القيام بذلك فقط لموقع فردي.</span><span class="sxs-lookup"><span data-stu-id="b1359-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="b1359-313">**استخدم أي من عمليات المستودع لتسوية المخزون كما هو مطلوب.**</span><span class="sxs-lookup"><span data-stu-id="b1359-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="b1359-314">تأكد من وجود مخزون كاف للصنف *A0001* في موقع مجمع والذي تم تحديده في توجيه موقع الانتقاء الخاص بالمنطقة حيث يجب ينتقي عمل التزويد الأصناف من معرف المنطقة *‎BULK*.</span><span class="sxs-lookup"><span data-stu-id="b1359-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="b1359-315">يجب أن يكون إجمالي المخزون أكبر من الحد الأقصى المطلوب للكمية (*150*) المحدد في قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="b1359-316">اختياري ولكن يوصي به: اتبع الخطوات التالية لإنشاء دفتر يومية لتسوية المخزون:</span><span class="sxs-lookup"><span data-stu-id="b1359-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="b1359-317">انتقل إلى **إدارة المخزون \> إدخالات دفتر اليومية \> الأصناف \> تسوية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="b1359-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="b1359-318">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-318">Select **New**.</span></span>
    1. <span data-ttu-id="b1359-319">في مربع الحوار **إنشاء دفتر يومية المخزون**، في حقل **المستودع**، حدد *61*.</span><span class="sxs-lookup"><span data-stu-id="b1359-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="b1359-320">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b1359-320">Select **OK**.</span></span>
    1. <span data-ttu-id="b1359-321">في علامة التبويب السريعة **بنود دفتر اليومية**، استخدم زر **جديد** لإضافة ثلاثة بنود إلى الشبكة، وقم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b1359-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="b1359-322">بعد الانتهاء من إعداد كل بند، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b1359-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="b1359-323">**السطر 1:**</span><span class="sxs-lookup"><span data-stu-id="b1359-323">**Line 1:**</span></span>

            - <span data-ttu-id="b1359-324">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b1359-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b1359-325">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="b1359-325">**Site:** *6*</span></span>
            - <span data-ttu-id="b1359-326">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b1359-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b1359-327">**الموقع:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b1359-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="b1359-328">**لوحة الترخيص**: حدد لوحة ترخيص موجودة في القائمة، أو قم بإنشاء لوحة ترخيص جديدة.</span><span class="sxs-lookup"><span data-stu-id="b1359-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b1359-329">**الكمية:** *1000*</span><span class="sxs-lookup"><span data-stu-id="b1359-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="b1359-330">**السطر 2:**</span><span class="sxs-lookup"><span data-stu-id="b1359-330">**Line 2:**</span></span>

            - <span data-ttu-id="b1359-331">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b1359-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b1359-332">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="b1359-332">**Site:** *6*</span></span>
            - <span data-ttu-id="b1359-333">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b1359-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b1359-334">**الموقع:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="b1359-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="b1359-335">**لوحة الترخيص**: حدد لوحة ترخيص موجودة في القائمة، أو قم بإنشاء لوحة ترخيص جديدة.</span><span class="sxs-lookup"><span data-stu-id="b1359-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b1359-336">**الكمية:** *15*</span><span class="sxs-lookup"><span data-stu-id="b1359-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="b1359-337">**السطر 3:**</span><span class="sxs-lookup"><span data-stu-id="b1359-337">**Line 3:**</span></span>

            - <span data-ttu-id="b1359-338">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b1359-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b1359-339">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="b1359-339">**Site:** *6*</span></span>
            - <span data-ttu-id="b1359-340">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b1359-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b1359-341">**الموقع:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b1359-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="b1359-342">**لوحة الترخيص**: حدد لوحة ترخيص موجودة في القائمة، أو قم بإنشاء لوحة ترخيص جديدة.</span><span class="sxs-lookup"><span data-stu-id="b1359-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b1359-343">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="b1359-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="b1359-344">في جزء الإجراءات، حدد **التحقق**.</span><span class="sxs-lookup"><span data-stu-id="b1359-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="b1359-345">قم بمعالجة أي أخطاء يتم العثور عليها قبل الانتقال إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="b1359-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="b1359-346">في جزء الإجراءات، حدد **ترحيل** لترحيل المخزون إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="b1359-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="b1359-347">نموذج السيناريو: تشغيل تزويد الحد الأدنى/الأقصى المستند إلى المنطقة</span><span class="sxs-lookup"><span data-stu-id="b1359-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="b1359-348">بعد توفير كافة البيانات النموذجية للمتطلبات الأساسية، يمكنك تشغيل التزويد باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b1359-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="b1359-349">انتقل إلى **إدارة المستودعات \> التزويد \> عمليات التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="b1359-350">في مربع حوار **التزويد**، في علامة التبويب السريعة **السجلات المطلوب تضمينها**، حدد **عامل التصفية**.</span><span class="sxs-lookup"><span data-stu-id="b1359-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="b1359-351">في مربع الحوار **استعلام**، من علامة التبويب **النطاق**، قم بتحرير صف الجدول الافتراضي بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="b1359-352">**الجدول:** حدد _قوالب التزويد_.</span><span class="sxs-lookup"><span data-stu-id="b1359-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b1359-353">**الجدول المشتق:** حدد _قوالب التزويد_.</span><span class="sxs-lookup"><span data-stu-id="b1359-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b1359-354">**الحقل:** حدد _قالب التزويد_.</span><span class="sxs-lookup"><span data-stu-id="b1359-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="b1359-355">**المعايير:** حدد _تزيد الحد الأدنى/الأقصى حسب المنطقة_.</span><span class="sxs-lookup"><span data-stu-id="b1359-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="b1359-356">يعد قالب التزويد هذا هو قالب التزويد الذي قمت بإنشائه أثناء تجهيز بيانات العرض التوضيحي لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="b1359-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="b1359-357">حدد **موافق** لحفظ الاستعلام والرجوع إلى مربع حوار **التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b1359-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="b1359-358">حدد **موافق** لتشغيل قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b1359-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="b1359-359">تم الآن إنشاء عمل التزويد لانتقاء المخزون من منطقة *مجمعة* وتزويدها إلى منطقة *الأرضية*.</span><span class="sxs-lookup"><span data-stu-id="b1359-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="b1359-360">ملاحظات وتلميحات</span><span class="sxs-lookup"><span data-stu-id="b1359-360">Notes and tips</span></span>

<span data-ttu-id="b1359-361">فيما يلي بعض الملاحظات وتلميحات حول العمل مع الميزة:</span><span class="sxs-lookup"><span data-stu-id="b1359-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="b1359-362">لإعداد عمل التزويد الذي ينتقل إلى المنطقة المطلوبة، يمكنك ربط بنود قالب التزويد وتوجيهات المواقع بإحدى الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="b1359-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="b1359-363">قم بتحرير استعلام رأس التوجيه للموقع، ثم قم بتصفية بنود قالب التزويد المحددة.</span><span class="sxs-lookup"><span data-stu-id="b1359-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="b1359-364">استخدم كود التوجيه‬ في بند قالب التزويد، وقم بمطابقته بتوجيه موقع الوضع.</span><span class="sxs-lookup"><span data-stu-id="b1359-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="b1359-365">إذا كنت تستخدم مواقع ديناميكية، سيتم إنشاء عمل التزويد إما للموقع الأول المتاح أو للموقع الذي يحتوي على المخزون بالفعل، وذلك في حالة إعداد إجراء توجيه الموقع لاستخدام استراتيجية **الدمج**.</span><span class="sxs-lookup"><span data-stu-id="b1359-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="b1359-366">إذا كنت تستخدم مواقع ثابتة بدلا من المناطق، يجب استخدام [تزويد الحد الأدنى/الأقصى القياسي](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="b1359-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]