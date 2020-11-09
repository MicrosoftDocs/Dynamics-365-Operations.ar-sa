---
title: تقسيم المستودعات
description: يوفر هذا الموضوع معلومات حول تقسيم المستودعات. يتيح تقسيم المستودعات تجميع الطلب حسب الصنف ووحدة القياس من الأوامر بالحالة مطلوبة أو محجوزة أو تم إصدارها. وهي تساعد مديري المستودع في تخطيط مواقع الانتقاء بشكل ذكي قبل قيامهم بإصدار الأوامر إلى المستودع وإنشاء عمل الانتقاء.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017404"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="92745-105">تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="92745-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92745-106">يتيح تقسيم المستودعات تجميع الطلب حسب الصنف ووحدة القياس من الأوامر بالحالة *مطلوبة* أو *محجوزة* أو *تم إصدارها*.</span><span class="sxs-lookup"><span data-stu-id="92745-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="92745-107">يمكن بعد ذلك تطبيق الطلب الذي تم إنشاؤه على المواقع التي سيتم استخدامها للانتقاء، استنادا إلى الكمية والوحدة والأبعاد الفعلية والمواقع الثابتة وغيرها.</span><span class="sxs-lookup"><span data-stu-id="92745-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="92745-108">بعد إنشاء خطة التقسيم، يمكن إنشاء عمل التزويد لجلب المقدار المناسب من المخزون لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="92745-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="92745-109">تساعد هذه الوظيفة مديري المستودع في تخطيط مواقع الانتقاء بشكل ذكي قبل قيامهم بإصدار الأوامر إلى المستودع وإنشاء عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="92745-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="92745-110">تشغيل ميزة تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="92745-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="92745-111">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="92745-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="92745-112">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="92745-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="92745-113">في مساحة عمل **إدارة الميزات** ، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="92745-114">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="92745-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="92745-115">**اسم الميزة:** *ميزة تقسيم المستودعات*</span><span class="sxs-lookup"><span data-stu-id="92745-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="92745-116">إعداد تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="92745-116">Set up warehouse slotting</span></span>

<span data-ttu-id="92745-117">لاستخدام تقسيم المستودعات، يجب إعداد العناصر التالية في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="92745-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="92745-118">إنشاء مستويات وحدات القياس للتقسيم</span><span class="sxs-lookup"><span data-stu-id="92745-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="92745-119">تتيح مستويات وحدات القياس إمكانية تجميع وحدات قياس متعددة معًا لأغراض التقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="92745-120">على سبيل المثال، إذا تم انتقاء أحجام صناديق متعددة جميعًا من نفس منطقة انتقاء الصناديق، فمن الممكن إنشاء مستوى واحد لكافة الأحجام.</span><span class="sxs-lookup"><span data-stu-id="92745-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="92745-121">**يجب إنشاء بند لكل وحدة قياس والتي يجب أن تكون جزءًا من المستوي.**</span><span class="sxs-lookup"><span data-stu-id="92745-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="92745-122">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> تقسيم مستويات وحدات القياس**.</span><span class="sxs-lookup"><span data-stu-id="92745-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="92745-123">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="92745-123">Select **New**.</span></span>
1. <span data-ttu-id="92745-124">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="92745-125">**مستوى وحدة القياس:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="92745-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="92745-126">**الوصف:** *كل بالتة صناديق*</span><span class="sxs-lookup"><span data-stu-id="92745-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="92745-127">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="92745-127">Select **Save**.</span></span>
1. <span data-ttu-id="92745-128">في علامة التبويب السريعة **وحدات القياس** ، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="92745-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="92745-129">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-130">**الوحدة:** *صندوق*</span><span class="sxs-lookup"><span data-stu-id="92745-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="92745-131">**الوصف:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="92745-132">سيتم ملء الحقل تلقائيًا عند حفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="92745-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="92745-133">**فئة الوحدة:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="92745-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="92745-134">حدد **جديد** لإضافة سطر ثان للشبكة.</span><span class="sxs-lookup"><span data-stu-id="92745-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="92745-135">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-136">**الوحدة:** *ea*</span><span class="sxs-lookup"><span data-stu-id="92745-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="92745-137">**الوصف:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="92745-138">سيتم ملء الحقل تلقائيًا عند حفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="92745-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="92745-139">**فئة الوحدة:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="92745-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="92745-140">حدد **جديد** لإضافة سطر ثالث للشبكة.</span><span class="sxs-lookup"><span data-stu-id="92745-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="92745-141">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-142">**الوحدة:** *PL*</span><span class="sxs-lookup"><span data-stu-id="92745-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="92745-143">**الوصف:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="92745-144">سيتم ملء الحقل تلقائيًا عند حفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="92745-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="92745-145">**فئة الوحدة:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="92745-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="92745-146">حدد **حفظ** لحفظ المستوى.</span><span class="sxs-lookup"><span data-stu-id="92745-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="92745-147">إنشاء كود توجيه للتقسيم</span><span class="sxs-lookup"><span data-stu-id="92745-147">Create a directive code for slotting</span></span>

<span data-ttu-id="92745-148">يجب تحديد كود التوجيه الذي يجب أن يكون مقترنًا بأحد القوالب.</span><span class="sxs-lookup"><span data-stu-id="92745-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="92745-149">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> أكواد التوجيه**.</span><span class="sxs-lookup"><span data-stu-id="92745-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="92745-150">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="92745-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="92745-151">في حقل **كود التوجيه** ، أدخل *التقسيم*.</span><span class="sxs-lookup"><span data-stu-id="92745-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="92745-152">في حقل **وصف التوجيه** ، أدخل *التقسيم*.</span><span class="sxs-lookup"><span data-stu-id="92745-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="92745-153">إعداد قوالب التقسيم</span><span class="sxs-lookup"><span data-stu-id="92745-153">Set up slotting templates</span></span>

<span data-ttu-id="92745-154">يتحكم كل قالب تقسيم في كيفية تعيين المخزون إلى مواقع لمستودع معين.</span><span class="sxs-lookup"><span data-stu-id="92745-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="92745-155">ويجب أن يتضمن كل قالب بندًا لكل مواصفة تقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="92745-156">استخدم الإجراءات الواردة في هذا القسم لإعداد قوالب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="92745-157">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التقسيم**.</span><span class="sxs-lookup"><span data-stu-id="92745-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="92745-158">حدد **جديد** ، لإنشاء قالب.</span><span class="sxs-lookup"><span data-stu-id="92745-158">Select **New** to create a template.</span></span>

<span data-ttu-id="92745-159">بعد ذلك، يجب عليك إعداد رأس القالب ومواصفات التقسيم وتوجيهات المواقع، كما هو موضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="92745-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="92745-160">إعداد رأس قالب التقسيم</span><span class="sxs-lookup"><span data-stu-id="92745-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="92745-161">في رأس القالب، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="92745-162">**قالب التقسيم:** _61_</span><span class="sxs-lookup"><span data-stu-id="92745-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="92745-163">**‏‏الوصف:** _61_</span><span class="sxs-lookup"><span data-stu-id="92745-163">**Description:** _61_</span></span>
    - <span data-ttu-id="92745-164">**نوع الطب:** *أمر مبيعات*</span><span class="sxs-lookup"><span data-stu-id="92745-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="92745-165">وفي الوقت الحالي، فإن *أمر المبيعات* هو نوع المستند الوحيد المدعوم.</span><span class="sxs-lookup"><span data-stu-id="92745-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="92745-166">**استراتيجية الطلب:** _مطلوب_</span><span class="sxs-lookup"><span data-stu-id="92745-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="92745-167">تتوفر القيم التالية في هذ الحقل:</span><span class="sxs-lookup"><span data-stu-id="92745-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="92745-168">**مطلوب** – يجب اعتبار الكمية المطلوبة بأكملها في أمر المبيعات هي الطلب.</span><span class="sxs-lookup"><span data-stu-id="92745-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="92745-169">**محجوز** – يجب اعتبار كميات بند أمر المبيعات التي تم حجزها (الفعلية والمطلوبة) هي الطلب.</span><span class="sxs-lookup"><span data-stu-id="92745-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="92745-170">**المستودع:** _61_</span><span class="sxs-lookup"><span data-stu-id="92745-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="92745-171">**السماح بطلب الموجه لاستخدام كميات غير محجوزة:** _نعم_</span><span class="sxs-lookup"><span data-stu-id="92745-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="92745-172">يمكنك أيضا تحديد استعلام لتضييق نطاق الطلب الذي يتم تقييمه.</span><span class="sxs-lookup"><span data-stu-id="92745-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="92745-173">إعداد مواصفات التقسيم لكل قالب</span><span class="sxs-lookup"><span data-stu-id="92745-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="92745-174">بالنسبة لكل قالب قمت بإنشائه، اتبع الخطوات التالية لإضافة بند لكل مواصفات تقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="92745-175">في علامة التبويب السريعة **تفاصيل قالب التقسيم** ، حدد **جديد** لإنشاء سطر قالب.</span><span class="sxs-lookup"><span data-stu-id="92745-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="92745-176">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-177">**التسلسل:** _1_</span><span class="sxs-lookup"><span data-stu-id="92745-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="92745-178">**الوصف:** _موقع ثابت_</span><span class="sxs-lookup"><span data-stu-id="92745-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="92745-179">**الحد الأدنى للكمية:** _1_</span><span class="sxs-lookup"><span data-stu-id="92745-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="92745-180">يحدد هذا الحقل الحد الأدنى لكمية الطلب المطلوبة للبند.</span><span class="sxs-lookup"><span data-stu-id="92745-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="92745-181">**الحد الأقصى للكمية:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="92745-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="92745-182">يحدد هذا الحقل الحد الأقصى لكمية الطلب الصالحة للبند.</span><span class="sxs-lookup"><span data-stu-id="92745-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="92745-183">**الوحدة:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="92745-184">يحدد هذا الحقل وحدة القياس وأدنى وأقصى كميات تشير إليها.</span><span class="sxs-lookup"><span data-stu-id="92745-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="92745-185">**مستوى وحدة القياس:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="92745-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="92745-186">يحدد هذا الحقل وحدات القياس للطلب الصالحة للبند.</span><span class="sxs-lookup"><span data-stu-id="92745-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="92745-187">(لمزيد من المعلومات، راجع قسم [إعداد مستويات وحدات القياس للتقسيم](#unit-tiers) المذكورة سابقًا في هذا الموضوع.)</span><span class="sxs-lookup"><span data-stu-id="92745-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="92745-188">**تعيين معايير القسمة:** _مراعاة الكمية_</span><span class="sxs-lookup"><span data-stu-id="92745-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="92745-189">تتوفر القيم التالية في هذ الحقل:</span><span class="sxs-lookup"><span data-stu-id="92745-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="92745-190">**افترض الفراغ** – يجب أن يفترض هذا النظام أن كافة المواقع في منطقة الانتقاء فارغة ولا يجب عليه فحص هذه المواقع بحثًا عن مخزون.</span><span class="sxs-lookup"><span data-stu-id="92745-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="92745-191">**افترض الكمية** – يجب أن يفحص النظام المواقع في منطقة الانتقاء بحثًا عن مخزون ويجب أن يتخطى أي المواقع ليست فارغة.</span><span class="sxs-lookup"><span data-stu-id="92745-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="92745-192">**كود التوجيه:** _التقسيم_</span><span class="sxs-lookup"><span data-stu-id="92745-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="92745-193">يحدد هذا الحقل توجيه الموقع المستخدم للعثور على موقع الانتقاء لعمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="92745-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="92745-194">**موقع التدفق:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="92745-195">يحدد هذا الحقل الموقع الذي يتم وضع فيه إذا تعذر العثور على موقع للكمية عند معالجة البند.</span><span class="sxs-lookup"><span data-stu-id="92745-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="92745-196">**السماح بالترك:** _نعم_</span><span class="sxs-lookup"><span data-stu-id="92745-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="92745-197">عند تعيين هذا الخيار على *نعم* ، إذا تعذر تقسيم أي طلب، سيتم إنشاء عمل حركة لإخراج المخزون من المواقع التي يوجد بها المخزون، ولكن لم يتم تقسيم أي شيء.</span><span class="sxs-lookup"><span data-stu-id="92745-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="92745-198">بعد ذلك يتم تشغيل القالب مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="92745-198">The template is then run again.</span></span> <span data-ttu-id="92745-199">في هذه المرة، يتم تجاهل المخزون في المواقع.</span><span class="sxs-lookup"><span data-stu-id="92745-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="92745-200">تعمل هذه الوظيفة بشكل أفضل عند تعيين حقل **تعيين معايير القسمة** على _مراعاة الكمية_.</span><span class="sxs-lookup"><span data-stu-id="92745-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="92745-201">**استخدام الموقع الثابت:** _المواقع الثابتة فقط للمنتج_</span><span class="sxs-lookup"><span data-stu-id="92745-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="92745-202">تتوفر القيم التالية في هذ الحقل:</span><span class="sxs-lookup"><span data-stu-id="92745-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="92745-203">**المواقع الثابتة وغير الثابتة** – لا ينبغي حصر النظام على استخدام المواقع الثابتة فقط.</span><span class="sxs-lookup"><span data-stu-id="92745-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="92745-204">**المواقع الثابتة فقط للمنتج** - يجب أن يقوم النظام بالتقسيم فقط إلى المواقع الثابتة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="92745-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="92745-205">**المواقع الثابتة فقط لمتغير المنتج** - يجب أن يقوم النظام بالتقسيم فقط إلى المواقع الثابتة لمتغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="92745-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="92745-206">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="92745-206">Select **Save**.</span></span>
1. <span data-ttu-id="92745-207">حدد **جديد** لإنشاء بند قالب ثان.</span><span class="sxs-lookup"><span data-stu-id="92745-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="92745-208">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-209">**التسلسل:** _2_</span><span class="sxs-lookup"><span data-stu-id="92745-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="92745-210">**الوصف:** _غير ذلك_</span><span class="sxs-lookup"><span data-stu-id="92745-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="92745-211">**الحد الأدنى للكمية:** _1_</span><span class="sxs-lookup"><span data-stu-id="92745-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="92745-212">**الحد الأقصى للكمية:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="92745-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="92745-213">**الوحدة:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="92745-214">**مستوى وحدة القياس:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="92745-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="92745-215">**تعيين معايير القسمة:** _مراعاة الكمية_</span><span class="sxs-lookup"><span data-stu-id="92745-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="92745-216">**كود التوجيه:** _التقسيم_</span><span class="sxs-lookup"><span data-stu-id="92745-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="92745-217">**موقع التدفق:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="92745-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="92745-218">**السماح بالترك:** _نعم_</span><span class="sxs-lookup"><span data-stu-id="92745-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="92745-219">**استخدام المواقع الثابتة:** _المواقع الثابتة وغير الثابتة_</span><span class="sxs-lookup"><span data-stu-id="92745-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="92745-220">في الاستعلام الخاص بالبند الثاني، ستقوم الآن بتحديد المعايير المستخدمة لتحديد ما المواقع التي يمكن فيها تقسيم الطلب لهذا البند.</span><span class="sxs-lookup"><span data-stu-id="92745-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="92745-221">حدد البند الذي تم فيه تعيين حقل **التسلسل** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="92745-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="92745-222">حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="92745-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="92745-223">في علامة التبويب **النطاق** ، حدد **إضافة** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="92745-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="92745-224">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-225">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="92745-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="92745-226">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="92745-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="92745-227">**الحقل:** *معرف ملف الموقع*</span><span class="sxs-lookup"><span data-stu-id="92745-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="92745-228">**المعايير:** *انتقاء-06* (حدد علامة الجمع المزدوجة \[**++**\] في الحقل لتوسيع القائمة، ثم حدد *انتقاء-06* - *موقع الانتقاء 6*.)</span><span class="sxs-lookup"><span data-stu-id="92745-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="92745-229">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="92745-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="92745-230">إعداد توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="92745-230">Set up location directives</span></span>

<span data-ttu-id="92745-231">يجب إعداد توجيه واحد على الأقل لدعم عمليات الانتقاء للتقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="92745-232">استخدم الإجراءات الواردة في هذا القسم لإعداد *توجيه موقع تزويد* جديد لعمليات الانتقاء للتقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="92745-233">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="92745-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="92745-234">في الجزء الأيسر في حقل **نوع أمر العمل** ، حدد *تزويد*.</span><span class="sxs-lookup"><span data-stu-id="92745-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="92745-235">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="92745-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="92745-236">في رأس توجيه الموقع الجديد، في حقل **الاسم** ، أدخل *انتقاء التقسيم 61*</span><span class="sxs-lookup"><span data-stu-id="92745-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="92745-237">علامة التبويب السريعة تكوين توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="92745-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="92745-238">في علامة التبويب السريعة **توجيهات الموقع** ، عيّن القيم التالية</span><span class="sxs-lookup"><span data-stu-id="92745-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="92745-239">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="92745-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="92745-240">**نوع العمل:** _انتقاء_</span><span class="sxs-lookup"><span data-stu-id="92745-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="92745-241">**الموقع:** _6_</span><span class="sxs-lookup"><span data-stu-id="92745-241">**Site:** _6_</span></span>
    - <span data-ttu-id="92745-242">**المستودع:** _61_</span><span class="sxs-lookup"><span data-stu-id="92745-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="92745-243">**كود التوجيه:** _التقسيم_</span><span class="sxs-lookup"><span data-stu-id="92745-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="92745-244">حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.</span><span class="sxs-lookup"><span data-stu-id="92745-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="92745-245">علامة التبويب السريعة تكوين البنود</span><span class="sxs-lookup"><span data-stu-id="92745-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="92745-246">في علامة التبويب السريعة **البنود** ، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="92745-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="92745-247">في البند الجديد، قم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="92745-247">On the new line, set the following values.</span></span> <span data-ttu-id="92745-248">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="92745-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="92745-249">**من الكمية:** _0_</span><span class="sxs-lookup"><span data-stu-id="92745-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="92745-250">**إلى الكمية:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="92745-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="92745-251">حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="92745-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="92745-252">علامة التبويب السريعة تكوين إجراءات توجيه الموقع</span><span class="sxs-lookup"><span data-stu-id="92745-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="92745-253">في علامة التبويب السريعة **إجراءات توجيه الموقع** ، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="92745-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="92745-254">في البند الجديد، قم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="92745-254">On the new line, set the following values.</span></span> <span data-ttu-id="92745-255">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="92745-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="92745-256">**الاسم:** _مجمع_</span><span class="sxs-lookup"><span data-stu-id="92745-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="92745-257">**الاستراتيجية:** _بلا_</span><span class="sxs-lookup"><span data-stu-id="92745-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="92745-258">حدد **حفظ** لجعل زر **تحرير الاستعلام** متاحا.</span><span class="sxs-lookup"><span data-stu-id="92745-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="92745-259">تحرير الاستعلام</span><span class="sxs-lookup"><span data-stu-id="92745-259">Edit the query</span></span>

1. <span data-ttu-id="92745-260">في علامة التبويب السريعة **إجراءات توجيه المواقع** ، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="92745-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="92745-261">في علامة التبويب **النطاق** ، حدد **إضافة** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="92745-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="92745-262">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="92745-263">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="92745-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="92745-264">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="92745-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="92745-265">**الحقل:** *معرف المنطقة*</span><span class="sxs-lookup"><span data-stu-id="92745-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="92745-266">**المعايير:** *مجمع* (حدد علامة الجمع المزدوجة \[**++**\] في الحقل لتوسيع القائمة، ثم حدد *مجمع*.)</span><span class="sxs-lookup"><span data-stu-id="92745-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="92745-267">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="92745-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="92745-268">سيناريو</span><span class="sxs-lookup"><span data-stu-id="92745-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="92745-269">إعداد السيناريو</span><span class="sxs-lookup"><span data-stu-id="92745-269">Set up the scenario</span></span>

<span data-ttu-id="92745-270">بالنسبة لهذا السيناريو، استخدم نموذج البيانات المضمن، وقم بإنشاء السجلات الموضحة في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="92745-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="92745-271">استخدام نموذج بيانات USMF</span><span class="sxs-lookup"><span data-stu-id="92745-271">Use the USMF sample data</span></span>

<span data-ttu-id="92745-272">للعمل بهذا السيناريو باستخدام السجلات والقيم النموذجية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="92745-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="92745-273">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="92745-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="92745-274">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="92745-274">Create demand</span></span>

<span data-ttu-id="92745-275">اتبع الخطوات التالية لإنشاء الطلب الذي ستقوم بتطبيق التقسيم عليه.</span><span class="sxs-lookup"><span data-stu-id="92745-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="92745-276">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="92745-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="92745-277">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="92745-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="92745-278">في مربع الحوار **إنشاء أمر مبيعات** ، في حقل **حساب العميل** ، وحدد _US-007_.</span><span class="sxs-lookup"><span data-stu-id="92745-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="92745-279">في حقل **المستودع** ، حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="92745-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="92745-280">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="92745-280">Select **OK**.</span></span>
1. <span data-ttu-id="92745-281">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="92745-281">The new sales order is opened.</span></span> <span data-ttu-id="92745-282">ويتضمن بندًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="92745-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="92745-283">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="92745-284">**الصنف:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="92745-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="92745-285">**الكمية:** _20_</span><span class="sxs-lookup"><span data-stu-id="92745-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="92745-286">حدد **إضافة بند** لإضافة بند جديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="92745-287">**الصنف:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="92745-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="92745-288">**الكمية:** _8_</span><span class="sxs-lookup"><span data-stu-id="92745-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="92745-289">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="92745-289">Select **Save**.</span></span>
1. <span data-ttu-id="92745-290">حدد **جديد** لإنشاء أمر مبيعات ثان.</span><span class="sxs-lookup"><span data-stu-id="92745-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="92745-291">في مربع الحوار **إنشاء أمر مبيعات** ، في حقل **حساب العميل** ، وحدد _US-008_.</span><span class="sxs-lookup"><span data-stu-id="92745-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="92745-292">في حقل **المستودع** ، حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="92745-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="92745-293">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="92745-293">The new sales order is opened.</span></span> <span data-ttu-id="92745-294">ويتضمن بندًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="92745-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="92745-295">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="92745-296">**الصنف:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="92745-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="92745-297">**الكمية:** _1_</span><span class="sxs-lookup"><span data-stu-id="92745-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="92745-298">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="92745-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="92745-299">التنقل عبر سيناريو تقسيم نموذجي</span><span class="sxs-lookup"><span data-stu-id="92745-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="92745-300">بعد تحقيق كافة عناصر المتطلبات المسبقة، كما هو موضح في القسم السابق، تصبح مستعدًا لتجربة الميزة بالعمل من خلال مطالعة كل تمرين في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="92745-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="92745-301">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="92745-301">Generate demand</span></span>

1. <span data-ttu-id="92745-302">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التقسيم** ، وحدد قالب التقسيم الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="92745-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="92745-303">في جزء الإجراءات، حدد **إنشاء طلب**.</span><span class="sxs-lookup"><span data-stu-id="92745-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="92745-304">يقوم هذا الأمر بتقييم كافة الطلبات الموجودة في النظام، والتي تطابق استعلام قالب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="92745-305">يتم بعد ذلك دمج الطلب الإجمالي لكافة الأوامر إلى بند واحد لكل كمية/وحدة قياس.</span><span class="sxs-lookup"><span data-stu-id="92745-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="92745-306">تظهر رسالة معلوماتية عند اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="92745-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="92745-307">طلب التقسيم</span><span class="sxs-lookup"><span data-stu-id="92745-307">Slotting demand</span></span>

<span data-ttu-id="92745-308">يعرض *طلب التقسيم* نتائج إنشاء الطلب، استنادا إلى إعداد قالب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="92745-309">في جزء الإجراءات، حدد **طلب التقسيم** لعرض النتائج من أمر **إنشاء الطلب**.</span><span class="sxs-lookup"><span data-stu-id="92745-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="92745-310">يمكن تحرير البنود الموجودة في طلب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="92745-311">يمكنك حذف بند، أو إضافة بند جديد، أو تحرير تفاصيل البند.</span><span class="sxs-lookup"><span data-stu-id="92745-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="92745-312">يمكنك تحرير الطلب يدويًا، أو يمكنك استيراده من نظام خارجي باستخدام إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="92745-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="92745-313">سيتم استخدام كل ما في طلب التقسيم في الخطوة التالية، بصرف النظر عن المكان الذي أتى منه.</span><span class="sxs-lookup"><span data-stu-id="92745-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="92745-314">موقع الطلب</span><span class="sxs-lookup"><span data-stu-id="92745-314">Locate demand</span></span>

<span data-ttu-id="92745-315">بعد إنشاء الطلب، يجب عليك استخدام أمر **تحديد موقع الطلب** لإنشاء *خطه التقسيم*.</span><span class="sxs-lookup"><span data-stu-id="92745-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="92745-316">في جزء الإجراءات، حدد **تحديد موقع الطلب**.</span><span class="sxs-lookup"><span data-stu-id="92745-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="92745-317">يتم تشغيل عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="92745-317">The slotting process runs.</span></span> <span data-ttu-id="92745-318">تظهر رسالة معلوماتية عند اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="92745-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="92745-319">خطة التقسيم</span><span class="sxs-lookup"><span data-stu-id="92745-319">Slotting plan</span></span>

<span data-ttu-id="92745-320">تعرض خطة التقسيم الموقع الذي تم تعيين كل صنف/كمية له، وما إذا كان قد تم استخدام التجاوز أم لا، وما إذا كان قد تم إنشاء عمل ترك أم لا، وبند القالب الذي تم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="92745-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="92745-321">**يتم تظليل أي طلب تعذر تقسيمه باللون الأحمر.**</span><span class="sxs-lookup"><span data-stu-id="92745-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="92745-322">في جزء الإجراءات، حدد **خطة التقسيم** لعرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="92745-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="92745-323">إنشاء تزويد</span><span class="sxs-lookup"><span data-stu-id="92745-323">Create replenishment</span></span>

<span data-ttu-id="92745-324">بعد إنشاء خطة التقسيم، يجب إنشاء *عمل التزويد* ، استنادًا إلى الخطة.</span><span class="sxs-lookup"><span data-stu-id="92745-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="92745-325">في جزء الإجراءات، حدد **تشغيل التزويد**.</span><span class="sxs-lookup"><span data-stu-id="92745-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="92745-326">تظهر رسالة معلوماتية عند اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="92745-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="92745-327">تشير هذه الرسالة إلى عدد الرؤوس التي تم إنشاؤها لمعرف بناء العمل.</span><span class="sxs-lookup"><span data-stu-id="92745-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="92745-328">يتم تحديد توجيهات المواقع التي سيتم استخدامها استنادًا إلى كود التوجيه المحدد في كل بند قالب.</span><span class="sxs-lookup"><span data-stu-id="92745-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="92745-329">تلميحات</span><span class="sxs-lookup"><span data-stu-id="92745-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="92745-330">إعداد التقسيم التلقائي</span><span class="sxs-lookup"><span data-stu-id="92745-330">Set up automatic slotting</span></span>

<span data-ttu-id="92745-331">بعد تحقيق كافة العناصر المطلوبة، يمكنك إعداد تشغيل التقسيم تلقائيًا باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92745-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="92745-332">انتقل إلى **إدارة المستودعات \> التزويد \> تشغيل التزويد**.</span><span class="sxs-lookup"><span data-stu-id="92745-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="92745-333">حدد خطوات التقسيم المطلوب تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="92745-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="92745-334">حدد واحدة أو أكثر من خطوات التقسيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92745-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="92745-335">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="92745-335">Generate demand</span></span>
    - <span data-ttu-id="92745-336">موقع الطلب</span><span class="sxs-lookup"><span data-stu-id="92745-336">Locate demand</span></span>
    - <span data-ttu-id="92745-337">إنشاء عمل التزويد</span><span class="sxs-lookup"><span data-stu-id="92745-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="92745-338">تعتبر خطوات التقسيم متتالية.</span><span class="sxs-lookup"><span data-stu-id="92745-338">The slotting steps are progressive.</span></span> <span data-ttu-id="92745-339">إذا كنت ترغب في اختيار *تحديد موقع الطلب* ، فيجب عليك أولاً تحديد *إنشاء طلب*.</span><span class="sxs-lookup"><span data-stu-id="92745-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="92745-340">حدد قالب التقسيم الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="92745-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="92745-341">قم بتعيين التكرار ليتم تشغيله تلقائيًا، إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="92745-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="92745-342">بالنسبة للتدريبات في السيناريو، **لا** تقم بإعداد التقسيم التلقائي.</span><span class="sxs-lookup"><span data-stu-id="92745-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
