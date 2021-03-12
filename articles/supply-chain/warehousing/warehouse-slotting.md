---
title: تقسيم المستودعات
description: يوفر هذا الموضوع معلومات حول تقسيم المستودعات. يتيح تقسيم المستودعات تجميع الطلب حسب الصنف ووحدة القياس من الأوامر بالحالة مطلوبة أو محجوزة أو تم إصدارها. وهي تساعد مديري المستودع في تخطيط مواقع الانتقاء بشكل ذكي قبل قيامهم بإصدار الأوامر إلى المستودع وإنشاء عمل الانتقاء.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993743"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="a5a6f-105">تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="a5a6f-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5a6f-106">تتوفر مجموعة متنوعة من ميزات تقسيم المستودعات لمساعدة مديري المستودع في تخطيط مواقع الانتقاء بشكل ذكي قبل قيامهم بإصدار الأوامر إلى المستودع وإنشاء عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="a5a6f-107">تتيح *ميزة تقسيم المستودعات* تجميع الطلب حسب الصنف ووحدة القياس من الأوامر بالحالة *مطلوبة* أو *محجوزة* أو *تم إصدارها*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="a5a6f-108">يمكن بعد ذلك تطبيق الطلب الذي تم إنشاؤه على المواقع التي سيتم استخدامها للانتقاء، استنادا إلى الكمية والوحدة والأبعاد الفعلية والمواقع الثابتة وغيرها.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="a5a6f-109">بعد إنشاء خطة التقسيم، يمكن إنشاء عمل التزويد لجلب المقدار المناسب من المخزون لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="a5a6f-110">تتيح ميزة *تقسيم المستودعات لأوامر التحويل* لمديري المستودع تزويد مواقع الانتقاء ، استنادا إلى الطلب من أوامر التحويل التي لم يتم إصدارها إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="a5a6f-111">ويضمن ذلك ان مواقع الانتقاء ستتضمن كافة الأصناف المطلوبة لأوامر التحويل بعد إصدارها إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="a5a6f-112">تتطلب هذه الميزة أيضا تشغيل ميزة *ميزه تقسيم المستودعات*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="a5a6f-113">تضيف ميزه *تحسينات تخصيص تقسيم المستودعات* خيارا لبنود القالب المستخدمة بواسطة ميزة *ميزه تقسيم المستودعات*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="a5a6f-114">يمكن الخيار النظام من الأخذ في الاعتبار المخزون الفعلي الموجود في الموقع الهدف.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="a5a6f-115">التالي ، قد يتم إنشاء عدد اقل من عمليات التزويد للتقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="a5a6f-116">تتطلب ميزه *تحسينات تخصيص تقسيم المستودعات* تشغيل ميزة *ميزه تقسيم المستودعات*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="a5a6f-117">ويمكن استخدامه اختياريا مع ميزة *تقسيم المستودعات لأوامر التحويل*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="a5a6f-118">تشغيل ميزات تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="a5a6f-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="a5a6f-119">قبل أن تتمكن من استخدام هذه الميزات، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="a5a6f-120">بإمكان المسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة هاتين الميزتين وتشغيلهما إذا كانتا مطلوبتين.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="a5a6f-121">قم بتشغيل الميزات التالية كما هو مطلوب:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="a5a6f-122">ميزة تقسيم المستودع</span><span class="sxs-lookup"><span data-stu-id="a5a6f-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="a5a6f-123">تقسيم المستودعات لأوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="a5a6f-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a5a6f-124">يجب تشغيل ميزه *ميزه تقسيم المستودعات* قبل هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="a5a6f-125">تحسينات توزيع تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="a5a6f-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a5a6f-126">يجب تشغيل ميزه *ميزه تقسيم المستودعات* قبل هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="a5a6f-127">إعداد تقسيم المستودعات</span><span class="sxs-lookup"><span data-stu-id="a5a6f-127">Set up warehouse slotting</span></span>

<span data-ttu-id="a5a6f-128">لاستخدام تقسيم المستودعات، يجب إعداد العناصر التالية في النظام الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="a5a6f-129">طبقات وحدة قياس التقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="a5a6f-130">أكواد التوجيه</span><span class="sxs-lookup"><span data-stu-id="a5a6f-130">Directive codes</span></span>
- <span data-ttu-id="a5a6f-131">قوالب التقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-131">Slotting templates</span></span>
- <span data-ttu-id="a5a6f-132">توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="a5a6f-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="a5a6f-133">إنشاء مستويات وحدات القياس للتقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="a5a6f-134">تتيح مستويات وحدات القياس إمكانية تجميع وحدات قياس متعددة معًا لأغراض التقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="a5a6f-135">على سبيل المثال، إذا تم انتقاء أحجام صناديق متعددة جميعًا من نفس منطقة انتقاء الصناديق، فمن الممكن إنشاء مستوى واحد لكافة الأحجام.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="a5a6f-136">**يجب إنشاء بند لكل وحدة قياس والتي يجب أن تكون جزءًا من المستوي.**</span><span class="sxs-lookup"><span data-stu-id="a5a6f-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="a5a6f-137">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> تقسيم مستويات وحدات القياس**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="a5a6f-138">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-138">Select **New**.</span></span>
1. <span data-ttu-id="a5a6f-139">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-140">**مستوى وحدة القياس:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="a5a6f-141">**الوصف:** *كل بالتة صناديق*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="a5a6f-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-142">Select **Save**.</span></span>
1. <span data-ttu-id="a5a6f-143">في علامة التبويب السريعة **وحدات القياس**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a5a6f-144">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-145">**الوحدة:** *صندوق*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="a5a6f-146">**الوصف:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="a5a6f-147">سيتم ملء الحقل تلقائيًا عند حفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="a5a6f-148">**فئة الوحدة:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="a5a6f-149">حدد **جديد** لإضافة سطر ثان للشبكة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="a5a6f-150">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-151">**الوحدة:** *ea*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="a5a6f-152">**الوصف:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="a5a6f-153">سيتم ملء الحقل تلقائيًا عند حفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="a5a6f-154">**فئة الوحدة:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="a5a6f-155">حدد **جديد** لإضافة سطر ثالث للشبكة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="a5a6f-156">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-157">**الوحدة:** *PL*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="a5a6f-158">**الوصف:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="a5a6f-159">سيتم ملء الحقل تلقائيًا عند حفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="a5a6f-160">**فئة الوحدة:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="a5a6f-161">حدد **حفظ** لحفظ المستوى.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="a5a6f-162">إنشاء كود توجيه للتقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-162">Create a directive code for slotting</span></span>

<span data-ttu-id="a5a6f-163">يجب تحديد كود التوجيه الذي يجب أن يكون مقترنًا بأحد القوالب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="a5a6f-164">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> أكواد التوجيه**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="a5a6f-165">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a5a6f-166">في حقل **كود التوجيه**، أدخل *التقسيم*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="a5a6f-167">في حقل **وصف التوجيه**، أدخل *التقسيم*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="a5a6f-168">إعداد قوالب التقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-168">Set up slotting templates</span></span>

<span data-ttu-id="a5a6f-169">يتحكم كل قالب تقسيم في كيفية تعيين المخزون إلى مواقع لمستودع معين.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="a5a6f-170">ويجب أن يتضمن كل قالب بندًا لكل مواصفة تقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="a5a6f-171">استخدم الإجراءات الواردة في هذا القسم لإعداد قوالب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="a5a6f-172">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التقسيم**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="a5a6f-173">حدد **جديد**، لإنشاء قالب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-173">Select **New** to create a template.</span></span>

<span data-ttu-id="a5a6f-174">بعد ذلك، يجب عليك إعداد رأس القالب ومواصفات التقسيم وتوجيهات المواقع، كما هو موضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="a5a6f-175">ويمثل اعداد التقسيم لأوامر التحويل الاعداد الخاص بتقسيم أوامر المبيعات، ولكن يتم تعيين أوامر التحويل للحقل **نوع الطلب** على *أوامر التحويل* بدلا من *أمر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="a5a6f-176">اعداد الراس لقالب تقسيم أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="a5a6f-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="a5a6f-177">في رأس القالب، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-178">**قالب التقسيم:** _61_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="a5a6f-179">**‏‏الوصف:** _61_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-179">**Description:** _61_</span></span>
    - <span data-ttu-id="a5a6f-180">**نوع الطب:** *أمر مبيعات*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="a5a6f-181">حاليا ، *أوامر المبيعات* و *أوامر التحويل* هي أنواع الطلب المعتمدة فقط.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="a5a6f-182">يمكنك تحديد *أوامر التحويل* فقط إذا كان *تقسيم المستودعات لأوامر التحويل* قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="a5a6f-183">**استراتيجية الطلب:** _مطلوب_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="a5a6f-184">تتوفر القيم التالية في هذ الحقل:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="a5a6f-185">**مطلوب** – يجب اعتبار الكمية المطلوبة بأكملها في أمر المبيعات هي الطلب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="a5a6f-186">**محجوز** – يجب اعتبار كميات بند أمر المبيعات التي تم حجزها (الفعلية والمطلوبة) هي الطلب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="a5a6f-187">**تم الإصدار** – ينبغي اعتبار الكمية التي تم إصدارها هي المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="a5a6f-188">**المستودع:** _61_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="a5a6f-189">**السماح بطلب الموجه لاستخدام كميات غير محجوزة:** _نعم_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="a5a6f-190">يمكنك أيضا تحديد استعلام لتضييق نطاق الطلب الذي يتم تقييمه.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="a5a6f-191">إعداد مواصفات التقسيم لكل قالب</span><span class="sxs-lookup"><span data-stu-id="a5a6f-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="a5a6f-192">بالنسبة لكل أمر مبيعات قمت بإنشائه، اتبع الخطوات التالية لإضافة بند لكل مواصفات تقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="a5a6f-193">في علامة التبويب السريعة **تفاصيل قالب التقسيم**، حدد **جديد** لإنشاء سطر قالب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="a5a6f-194">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-195">**التسلسل:** _1_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="a5a6f-196">**الوصف:** _موقع ثابت_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="a5a6f-197">**الحد الأدنى للكمية:** _1_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="a5a6f-198">يحدد هذا الحقل الحد الأدنى لكمية الطلب المطلوبة للبند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="a5a6f-199">**الحد الأقصى للكمية:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="a5a6f-200">يحدد هذا الحقل الحد الأقصى لكمية الطلب الصالحة للبند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="a5a6f-201">**الوحدة:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="a5a6f-202">يحدد هذا الحقل وحدة القياس وأدنى وأقصى كميات تشير إليها.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="a5a6f-203">**مستوى وحدة القياس:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="a5a6f-204">يحدد هذا الحقل وحدات القياس للطلب الصالحة للبند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="a5a6f-205">(لمزيد من المعلومات، راجع قسم [إعداد مستويات وحدات القياس للتقسيم](#unit-tiers) المذكورة سابقًا في هذا الموضوع.)</span><span class="sxs-lookup"><span data-stu-id="a5a6f-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="a5a6f-206">**تعيين معايير القسمة:** _مراعاة الكمية_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="a5a6f-207">تتوفر القيم التالية في هذ الحقل:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="a5a6f-208">**افترض الفراغ** – يجب أن يفترض هذا النظام أن كافة المواقع في منطقة الانتقاء فارغة ولا يجب عليه فحص هذه المواقع بحثًا عن مخزون.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="a5a6f-209">**افترض الكمية** – يجب أن يفحص النظام المواقع في منطقة الانتقاء بحثًا عن مخزون ويجب أن يتخطى أي المواقع ليست فارغة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="a5a6f-210">**مراعاه الكمية الحالية** – يجب علي النظام فحص ما إذا كان اي موقع هدف يحتوي علي كميات غير محجوزة للصنف الموجود في بند الطلب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="a5a6f-211">إذا كانت الكمية كبيره بالقدر الكافي لاستيفاء وحده واحده علي الأقل من بنود الطلب ، فان سجل خطه التقسيم الذي تم إنشاؤه يتم تقليله حسب المبلغ المتاح.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="a5a6f-212">علي سبيل المثال ، إذا كان الطلب هو 10 حالات ، وكانت حاله واحده متاحه ، فان الطلب الذي تم تحديده سيكون تسع حالات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="a5a6f-213">إذا كان الطلب هو 10 حالات ، وكانت حاله واحده متاحه ، فان الطلب الذي تم تحديده سيكون تسع حالات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="a5a6f-214">تتوفر هذه القيمة فقط عند تشغيل ميزة *تحسينات تخصيص تقسيم المستودعات*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="a5a6f-215">**كود التوجيه:** _التقسيم_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="a5a6f-216">يحدد هذا الحقل توجيه الموقع المستخدم للعثور على موقع الانتقاء لعمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="a5a6f-217">**موقع التدفق:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="a5a6f-218">يحدد هذا الحقل الموقع الذي يتم وضع فيه إذا تعذر العثور على موقع للكمية عند معالجة البند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="a5a6f-219">**السماح بالترك:** _نعم_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="a5a6f-220">عند تعيين هذا الخيار على *نعم*، إذا تعذر تقسيم أي طلب، سيتم إنشاء عمل حركة لإخراج المخزون من المواقع التي يوجد بها المخزون، ولكن لم يتم تقسيم أي شيء.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="a5a6f-221">بعد ذلك يتم تشغيل القالب مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-221">The template is then run again.</span></span> <span data-ttu-id="a5a6f-222">في هذه المرة، يتم تجاهل المخزون في المواقع.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="a5a6f-223">تعمل هذه الوظيفة بشكل أفضل عند تعيين حقل **تعيين معايير القسمة** على _مراعاة الكمية_.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="a5a6f-224">**استخدام الموقع الثابت:** _المواقع الثابتة فقط للمنتج_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="a5a6f-225">تتوفر القيم التالية في هذ الحقل:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="a5a6f-226">**المواقع الثابتة وغير الثابتة** – لا ينبغي حصر النظام على استخدام المواقع الثابتة فقط.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="a5a6f-227">**المواقع الثابتة فقط للمنتج** - يجب أن يقوم النظام بالتقسيم فقط إلى المواقع الثابتة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="a5a6f-228">**المواقع الثابتة فقط لمتغير المنتج** - يجب أن يقوم النظام بالتقسيم فقط إلى المواقع الثابتة لمتغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="a5a6f-229">إذا كان قالب التقسيم يحتوي علي بند واحد علي الأقل يتم فيه تعيين الحقل **تعيين معايير التقسيم** من أجل *اعتبار الكمية الحالية*، فلن يتم السماح بإعداد أي بند في القالب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="a5a6f-230">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-230">Select **Save**.</span></span>
1. <span data-ttu-id="a5a6f-231">حدد **جديد** لإنشاء بند قالب ثان.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="a5a6f-232">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-233">**التسلسل:** _2_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="a5a6f-234">**الوصف:** _غير ذلك_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="a5a6f-235">**الحد الأدنى للكمية:** _1_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="a5a6f-236">**الحد الأقصى للكمية:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="a5a6f-237">**الوحدة:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="a5a6f-238">**مستوى وحدة القياس:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="a5a6f-239">**تعيين معايير القسمة:** _مراعاة الكمية_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="a5a6f-240">**كود التوجيه:** _التقسيم_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="a5a6f-241">**موقع التدفق:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="a5a6f-242">**السماح بالترك:** _نعم_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="a5a6f-243">**استخدام المواقع الثابتة:** _المواقع الثابتة وغير الثابتة_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="a5a6f-244">في الاستعلام الخاص بالبند الثاني، ستقوم الآن بتحديد المعايير المستخدمة لتحديد ما المواقع التي يمكن فيها تقسيم الطلب لهذا البند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="a5a6f-245">حدد البند الذي تم فيه تعيين حقل **التسلسل** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="a5a6f-246">حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="a5a6f-247">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="a5a6f-248">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-249">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="a5a6f-250">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="a5a6f-251">**الحقل:** *معرف ملف الموقع*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="a5a6f-252">**المعايير:** *انتقاء-06* (حدد علامة الجمع المزدوجة \[**++**\] في الحقل لتوسيع القائمة، ثم حدد *انتقاء-06* - *موقع الانتقاء 6*.)</span><span class="sxs-lookup"><span data-stu-id="a5a6f-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="a5a6f-253">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="a5a6f-254">إعداد توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="a5a6f-254">Set up location directives</span></span>

<span data-ttu-id="a5a6f-255">يجب إعداد توجيه واحد على الأقل لدعم عمليات الانتقاء للتقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="a5a6f-256">استخدم الإجراءات الواردة في هذا القسم لإعداد *توجيه موقع تزويد* جديد لعمليات الانتقاء للتقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="a5a6f-257">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a5a6f-258">في الجزء الأيسر في حقل **نوع أمر العمل**، حدد *تزويد*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="a5a6f-259">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a5a6f-260">في رأس توجيه الموقع الجديد، في حقل **الاسم**، أدخل *انتقاء التقسيم 61*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="a5a6f-261">في حقل **الرقم التسلسلي**، اقبل القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="a5a6f-262">علامة التبويب السريعة تكوين توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="a5a6f-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="a5a6f-263">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية</span><span class="sxs-lookup"><span data-stu-id="a5a6f-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="a5a6f-264">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="a5a6f-265">**نوع العمل:** _انتقاء_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="a5a6f-266">**الموقع:** _6_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-266">**Site:** _6_</span></span>
    - <span data-ttu-id="a5a6f-267">**المستودع:** _61_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="a5a6f-268">**كود التوجيه:** _التقسيم_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="a5a6f-269">حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="a5a6f-270">علامة التبويب السريعة تكوين البنود</span><span class="sxs-lookup"><span data-stu-id="a5a6f-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="a5a6f-271">في علامة التبويب السريعة **البنود**، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="a5a6f-272">في البند الجديد، قم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="a5a6f-273">**من الكمية:** _0_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="a5a6f-274">**إلى الكمية:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="a5a6f-275">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="a5a6f-276">حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="a5a6f-277">علامة التبويب السريعة تكوين إجراءات توجيه الموقع</span><span class="sxs-lookup"><span data-stu-id="a5a6f-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="a5a6f-278">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="a5a6f-279">في البند الجديد، قم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-279">On the new line, set the following values.</span></span> <span data-ttu-id="a5a6f-280">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="a5a6f-281">**الرقم التسلسلي:** قبول القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="a5a6f-282">**الاسم:** _مجمع_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="a5a6f-283">**الاستراتيجية:** _بلا_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="a5a6f-284">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="a5a6f-285">حدد **حفظ** لجعل زر **تحرير الاستعلام** متاحا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="a5a6f-286">تحرير الاستعلام</span><span class="sxs-lookup"><span data-stu-id="a5a6f-286">Edit the query</span></span>

1. <span data-ttu-id="a5a6f-287">في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="a5a6f-288">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="a5a6f-289">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-290">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="a5a6f-291">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="a5a6f-292">**الحقل:** *معرف المنطقة*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="a5a6f-293">**المعايير:** *مجمع* (حدد علامة الجمع المزدوجة \[**++**\] في الحقل لتوسيع القائمة، ثم حدد *مجمع*.)</span><span class="sxs-lookup"><span data-stu-id="a5a6f-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="a5a6f-294">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="a5a6f-295">سيناريو</span><span class="sxs-lookup"><span data-stu-id="a5a6f-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="a5a6f-296">إعداد السيناريو</span><span class="sxs-lookup"><span data-stu-id="a5a6f-296">Set up the scenario</span></span>

<span data-ttu-id="a5a6f-297">بالنسبة لهذا السيناريو، استخدم نموذج البيانات المضمن، وقم بإنشاء السجلات الموضحة في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="a5a6f-298">استخدام نموذج بيانات USMF</span><span class="sxs-lookup"><span data-stu-id="a5a6f-298">Use the USMF sample data</span></span>

<span data-ttu-id="a5a6f-299">للعمل بهذا السيناريو باستخدام السجلات والقيم النموذجية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a5a6f-300">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="a5a6f-301">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="a5a6f-301">Create demand</span></span>

<span data-ttu-id="a5a6f-302">اتبع الخطوات التالية لإنشاء الطلب الذي ستقوم بتطبيق التقسيم عليه.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="a5a6f-303">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="a5a6f-304">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a5a6f-305">في مربع الحوار **إنشاء أمر مبيعات**، في حقل **حساب العميل**، وحدد _US-007_.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="a5a6f-306">في حقل **المستودع**، حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="a5a6f-307">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-307">Select **OK**.</span></span>
1. <span data-ttu-id="a5a6f-308">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-308">The new sales order is opened.</span></span> <span data-ttu-id="a5a6f-309">ويتضمن بندًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a5a6f-310">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-311">**الصنف:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="a5a6f-312">**الكمية:** _20_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="a5a6f-313">حدد **إضافة بند** لإضافة بند جديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="a5a6f-314">**الصنف:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="a5a6f-315">**الكمية:** _8_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="a5a6f-316">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-316">Select **Save**.</span></span>
1. <span data-ttu-id="a5a6f-317">حدد **جديد** لإنشاء أمر مبيعات ثان.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="a5a6f-318">في مربع الحوار **إنشاء أمر مبيعات**، في حقل **حساب العميل**، وحدد _US-008_.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="a5a6f-319">في حقل **المستودع**، حدد _61_.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="a5a6f-320">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-320">The new sales order is opened.</span></span> <span data-ttu-id="a5a6f-321">ويتضمن بندًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a5a6f-322">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="a5a6f-323">**الصنف:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="a5a6f-324">**الكمية:** _1_</span><span class="sxs-lookup"><span data-stu-id="a5a6f-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="a5a6f-325">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="a5a6f-326">التنقل عبر سيناريو تقسيم نموذجي</span><span class="sxs-lookup"><span data-stu-id="a5a6f-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="a5a6f-327">بعد تحقيق كافة عناصر المتطلبات المسبقة، كما هو موضح في القسم السابق، تصبح مستعدًا لتجربة الميزة بالعمل من خلال مطالعة كل تمرين في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="a5a6f-328">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="a5a6f-328">Generate demand</span></span>

1. <span data-ttu-id="a5a6f-329">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التقسيم**، وحدد قالب التقسيم الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="a5a6f-330">في جزء الإجراءات، حدد **إنشاء طلب**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="a5a6f-331">يقوم هذا الأمر بتقييم كافة الطلبات الموجودة في النظام، والتي تطابق استعلام قالب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="a5a6f-332">يتم بعد ذلك دمج الطلب الإجمالي لكافة الأوامر إلى بند واحد لكل كمية/وحدة قياس.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="a5a6f-333">تظهر رسالة معلوماتية عند اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="a5a6f-334">طلب التقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-334">Slotting demand</span></span>

<span data-ttu-id="a5a6f-335">يعرض *طلب التقسيم* نتائج إنشاء الطلب، استنادا إلى إعداد قالب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="a5a6f-336">في جزء الإجراءات، حدد **طلب التقسيم** لعرض النتائج من أمر **إنشاء الطلب**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="a5a6f-337">يمكن تحرير البنود الموجودة في طلب التقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="a5a6f-338">يمكنك حذف بند، أو إضافة بند جديد، أو تحرير تفاصيل البند.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="a5a6f-339">يمكنك تحرير الطلب يدويًا، أو يمكنك استيراده من نظام خارجي باستخدام إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="a5a6f-340">سيتم استخدام كل ما في طلب التقسيم في الخطوة التالية، بصرف النظر عن المكان الذي أتى منه.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="a5a6f-341">موقع الطلب</span><span class="sxs-lookup"><span data-stu-id="a5a6f-341">Locate demand</span></span>

<span data-ttu-id="a5a6f-342">بعد إنشاء الطلب، يجب عليك استخدام أمر **تحديد موقع الطلب** لإنشاء *خطه التقسيم*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="a5a6f-343">في جزء الإجراءات، حدد **تحديد موقع الطلب**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="a5a6f-344">يتم تشغيل عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-344">The slotting process runs.</span></span> <span data-ttu-id="a5a6f-345">تظهر رسالة معلوماتية عند اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="a5a6f-346">خطة التقسيم</span><span class="sxs-lookup"><span data-stu-id="a5a6f-346">Slotting plan</span></span>

<span data-ttu-id="a5a6f-347">تعرض خطة التقسيم الموقع الذي تم تعيين كل صنف/كمية له، وما إذا كان قد تم استخدام التجاوز أم لا، وما إذا كان قد تم إنشاء عمل ترك أم لا، وبند القالب الذي تم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="a5a6f-348">*يتم تظليل أي طلب تعذر تقسيمه باللون الأحمر.*</span><span class="sxs-lookup"><span data-stu-id="a5a6f-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="a5a6f-349">في جزء الإجراءات، حدد **خطة التقسيم** لعرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="a5a6f-350">يتم الآن تشغيل عمليات **طلب الإنشاء** و **تحديد موقع الطلب** و **تشغيل التزويد** في اليه تحديد الصلاحيات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="a5a6f-351">(تتوفر هذه العمليات من جزء الإجراءات في صفحه **قوالب التقسيم**.)</span><span class="sxs-lookup"><span data-stu-id="a5a6f-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="a5a6f-352">تتضمن عمليات **طلب الإنشاء** و **تحديد موقع الطلب** و **تشغيل التزويد** تامينا لضمان عدم امكانيه تشغيلها في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="a5a6f-353">وبخلاف ذلك ، يمكن حذف البيانات المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="a5a6f-354">تظهر عمليات **إنشاء الطلب** و **تحديد مواقع الطلب** تحذيرا إذا لم يقم التشغيل بإنشاء سجلات ، أو إذا كانت السجلات تفتقد للمعلومات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="a5a6f-355">عند تحديد **خطه التقسيم**، لا تحتوي الصفحة علي أزرار **جديد** أو **تحرير** أو **حذف** في جزء الاجراء، لأنه لا يمكن تحرير مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="a5a6f-356">عند تحديد **تشغيل التزويد**، يقوم النظام بالتحقق من صحة قالب وعمليات الفتحات المحددة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="a5a6f-357">إنشاء تزويد</span><span class="sxs-lookup"><span data-stu-id="a5a6f-357">Create replenishment</span></span>

<span data-ttu-id="a5a6f-358">بعد إنشاء خطة التقسيم، يجب إنشاء *عمل التزويد*، استنادًا إلى الخطة.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="a5a6f-359">في جزء الإجراءات، حدد **تشغيل التزويد**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="a5a6f-360">تظهر رسالة معلوماتية عند اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="a5a6f-361">تشير هذه الرسالة إلى عدد الرؤوس التي تم إنشاؤها لمعرف بناء العمل.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="a5a6f-362">يتم تحديد توجيهات المواقع التي سيتم استخدامها استنادًا إلى كود التوجيه المحدد في كل بند قالب.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="a5a6f-363">تلميحات</span><span class="sxs-lookup"><span data-stu-id="a5a6f-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="a5a6f-364">إعداد التقسيم التلقائي</span><span class="sxs-lookup"><span data-stu-id="a5a6f-364">Set up automatic slotting</span></span>

<span data-ttu-id="a5a6f-365">بعد تحقيق كافة العناصر المطلوبة، يمكنك إعداد تشغيل التقسيم تلقائيًا باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="a5a6f-366">انتقل إلى **إدارة المستودعات \> التزويد \> تشغيل التزويد**.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="a5a6f-367">حدد خطوات التقسيم المطلوب تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="a5a6f-368">حدد واحدة أو أكثر من خطوات التقسيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a5a6f-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="a5a6f-369">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="a5a6f-369">Generate demand</span></span>
    - <span data-ttu-id="a5a6f-370">موقع الطلب</span><span class="sxs-lookup"><span data-stu-id="a5a6f-370">Locate demand</span></span>
    - <span data-ttu-id="a5a6f-371">إنشاء عمل التزويد</span><span class="sxs-lookup"><span data-stu-id="a5a6f-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="a5a6f-372">تعتبر خطوات التقسيم متتالية.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-372">The slotting steps are progressive.</span></span> <span data-ttu-id="a5a6f-373">إذا كنت ترغب في اختيار *تحديد موقع الطلب*، فيجب عليك أولاً تحديد *إنشاء طلب*.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="a5a6f-374">حدد قالب التقسيم الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="a5a6f-375">قم بتعيين التكرار ليتم تشغيله تلقائيًا، إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="a5a6f-376">بالنسبة للتدريبات في السيناريو، **لا** تقم بإعداد التقسيم التلقائي.</span><span class="sxs-lookup"><span data-stu-id="a5a6f-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
