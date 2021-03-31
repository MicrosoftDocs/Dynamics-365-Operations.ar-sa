---
title: تزويد أعلى من سعة الموقع
description: يوفر هذا الموضوع معلومات حول ميزة التزويد الأعلى من سعة الموقع. تعمل هذه الميزة على تمكين عمل التزويد بكامله المطلوب إنشاؤه في اليوم وتدير توافر عمل التزويد لضمان عدم نفاد موقع الانتقاء من المخزون أو انتقاله إلى وضع تجاوز السعة.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 1e4acfea3484acaafd982d0f22c2303f921f909f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228383"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="b2233-104">تزويد أعلى من سعة الموقع</span><span class="sxs-lookup"><span data-stu-id="b2233-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2233-105">يجب أن تقوم بعض المستودعات الكبيرة الحجم أو المقيدة المساحة بشحن كمية أكبر مما يستطيع موقع الانتقاء استيعابه خلال اليوم.</span><span class="sxs-lookup"><span data-stu-id="b2233-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="b2233-106">تمكّن الميزة *تزويد أعلى من سعة الموقع* عمل التزويد بكامله المطلوب إنشاؤه في اليوم وتدير توافر عمل التزويد لضمان عدم نفاد موقع الانتقاء من المخزون أو انتقاله إلى وضع تجاوز السعة.</span><span class="sxs-lookup"><span data-stu-id="b2233-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="b2233-107">تمكّن الميزة إنشاء عمل تزويد يزيد عما يستطيع الموقع استيعابه، وهي تمنع إكمال عمل التزويد عندما يكون الموقع ممتلئًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="b2233-108">عندما ينخفض المخزون في موقع الانتقاء إلى أقل من الحد القابل للتكوين، يُتاح المزيد من عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="b2233-109">تشغيل ميزة التزويد الأعلى من سعة الموقع</span><span class="sxs-lookup"><span data-stu-id="b2233-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="b2233-110">لإتاحة هذه الميزة، شغِّل الميزات التالية في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (بالترتيب التالي):</span><span class="sxs-lookup"><span data-stu-id="b2233-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="b2233-111">حظر العمل على مستوى المؤسسة</span><span class="sxs-lookup"><span data-stu-id="b2233-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="b2233-112">تزويد أعلى من سعة الموقع</span><span class="sxs-lookup"><span data-stu-id="b2233-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="b2233-113">إعداد الميزة السيناريو المثال</span><span class="sxs-lookup"><span data-stu-id="b2233-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="b2233-114">يوفر هذا القسم إرشادات ومثال يوضح كيفيه إعداد هذه الميزة وتجهيز عينة البيانات للسيناريو المثال الذي يتم توفيره لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b2233-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="b2233-115">تمكين عينة البيانات</span><span class="sxs-lookup"><span data-stu-id="b2233-115">Enable sample data</span></span>

<span data-ttu-id="b2233-116">للعمل عبر [السيناريو المثال](#example-scenario) باستخدام عينات البيانات والسجلات المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span><span class="sxs-lookup"><span data-stu-id="b2233-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b2233-117">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="b2233-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="b2233-118">ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="b2233-118">Location profile</span></span>

<span data-ttu-id="b2233-119">تمكين ميزة التزويد الأعلى من سعة الموقع في ملف تعريف الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2233-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="b2233-120">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b2233-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="b2233-121">في الجزء الأيمن، حدد **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="b2233-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="b2233-122">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b2233-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b2233-123">في علامة التبويب السريعة **التزويد**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b2233-124">**تجاوز سعة الموقع:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="b2233-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="b2233-125">عند تمكين هذا الحقل، سيسمح بتجاوز السعة القصوى للموقع بواسطة عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="b2233-126">ويؤدي ذلك أيضًا إلى تمكين الحقول الأخرى الموجودة علامة التبويب السريع **تزويد**.</span><span class="sxs-lookup"><span data-stu-id="b2233-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="b2233-127">**نوع حد توافر العمل:** *الكمية*</span><span class="sxs-lookup"><span data-stu-id="b2233-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="b2233-128">يحدد هذا الحقل الطريقة التي يتم استخدامها لتحديد الوقت الذي ينبغي فيه إصدار مزيد من العمل.</span><span class="sxs-lookup"><span data-stu-id="b2233-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="b2233-129">يمكنك إصداره حسب الكمية أو النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="b2233-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="b2233-130">*النسبة المئوية* – حدد هذا الخيار لاستخدام سعة النسبة المئوية التي تستند إلى حدود المخزون أو مقاييس الحجم.</span><span class="sxs-lookup"><span data-stu-id="b2233-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="b2233-131">يؤدي تحديد هذا الخيار إلى تمكين حقل **النسبة المئوية للتجاوز** وتعطيل حقلي الكمية المرتبطين، **كمية تجاوز السعة** و **وحدة تجاوز السعة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="b2233-132">يمكنك استخدام هذا الخيار إذا كانت مواقع الانتقاء تستخدم مقاييس الحجم.</span><span class="sxs-lookup"><span data-stu-id="b2233-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="b2233-133">إذا تم تحديد هذا الخيار، فعيّن الحقل **النسبة المئوية لتجاوز السعة** إلى النسبة المئوية التي سيتم عندما جعل عمل التزويد متاحًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="b2233-134">*الكمية* – حدد هذا الخيار لاستخدام قيمة كمية محددة..</span><span class="sxs-lookup"><span data-stu-id="b2233-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="b2233-135">يؤدي تحديد هذا الخيار إلى تعطيل حقل **النسبة المئوية لتجاوز السعة** وتمكين الحقلين **كمية تجاوز السعة** و **وحدة تجاوز السعة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="b2233-136">استخدم هذا الخيار عندما لا تستخدم مقاييس الحجم للمواقع التي يجري تزويدها، أو عندما يكون لديك كميات متناسقة التي يتم عندها إحضار المخزون إلى الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2233-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="b2233-137">إذا تم تحديد هذا الخيار، فقم بتعيين الحقلين **كمية تجاوز السعة** و **وحدة تجاوز السعة** إلى الكمية والوحدة التي سيتم عندها إتاحة عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="b2233-138">**كمية تجاوز السعة:** *0.65*</span><span class="sxs-lookup"><span data-stu-id="b2233-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="b2233-139">يحدد هذا الحقل الكمية التي يحدث عندها تجاوز سعة الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2233-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="b2233-140">سيكون العمل متوفرًا كلما كان مجموع الكمية المتاحة في الموقع وكمية العمل أقل من هذه القيمة.</span><span class="sxs-lookup"><span data-stu-id="b2233-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="b2233-141">سيتم حظر أي عمل تزويد يفوق هذه القيمة، ويجب إلغاء حظره يدويًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="b2233-142">تؤخذ حدود مخزون الموقع في الاعتبار عند حساب كمية العمل.</span><span class="sxs-lookup"><span data-stu-id="b2233-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="b2233-143">**وحدة تجاوز السعة:** *PL*</span><span class="sxs-lookup"><span data-stu-id="b2233-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="b2233-144">يحدد هذا الحقل الوحدة المرتبطة بكمية تجاوز السعه.</span><span class="sxs-lookup"><span data-stu-id="b2233-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="b2233-145">في هذه الحالة، سيتوفر مزيد من عمل التزويد عندما يصل الموقع إلى 0.65 بالته (بل).</span><span class="sxs-lookup"><span data-stu-id="b2233-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="b2233-146">**النسبة المئوية للتجاوز**</span><span class="sxs-lookup"><span data-stu-id="b2233-146">**Overflow percentage**</span></span>

        <span data-ttu-id="b2233-147">يحدد هذا الحقل النسبة المئوية التي يحدث عندها تجاوز سعة الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2233-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="b2233-148">سيكون العمل متوفرًا كلما كان مجموع الكمية المتاحة في الموقع وكمية العمل أقل من هذه النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="b2233-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="b2233-149">سيتم حظر أي نسبة مئوية لكمية أعمال التزويد فوق هذه القيمة، ويجب إلغاء حظرها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="b2233-150">تؤخذ حدود مخزون الموقع في الاعتبار عند حساب النسبة المئوية لكمية العمل.</span><span class="sxs-lookup"><span data-stu-id="b2233-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="b2233-151">إذا لم يتم تحديد حدود تخزين الموقع، فسيتم حساب النسبة المئوية لكمية العمل حسب الحجم إذا تم تحديد قيود الحجم لملف تعريف الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2233-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2233-152">إذا كنت تستخدم بيانات العرض التوضيحي للكيان القانوني **USMF** وقمت في وقت سابق بتشغيل الميزة *تحديد موضع لوحة ترخيص الموقع‬*، فيجب عليك إيقاف تشغيل الإعداد **تمكين تحديد موضع لوحة ترخيص الموقع** لملف تعريف الموقع **BULK-06** لإكمال خطوات المحمول في هذا السيناريو المثال.</span><span class="sxs-lookup"><span data-stu-id="b2233-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="b2233-153">رمز خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="b2233-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="b2233-154">لإعداد رمز خطوة الموجة كما هو موضح هنا، قد يتعين عليك أولا استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزة المسماة *رمز خطوة الموجة على مستوى المؤسسة*.</span><span class="sxs-lookup"><span data-stu-id="b2233-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="b2233-155">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> أكواد خطوة الموجة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="b2233-156">حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="b2233-157">**كود خطوة الموجة:** *تزويد*</span><span class="sxs-lookup"><span data-stu-id="b2233-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="b2233-158">**وصف خطوة الموجة:** *تزويد*</span><span class="sxs-lookup"><span data-stu-id="b2233-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="b2233-159">**نوع خطوة الموجة:** *تزويد*</span><span class="sxs-lookup"><span data-stu-id="b2233-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="b2233-160">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b2233-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="b2233-161">قالب التزويد</span><span class="sxs-lookup"><span data-stu-id="b2233-161">Replenishment template</span></span>

<span data-ttu-id="b2233-162">قوالب التزويد هي مجموعة من القواعد التي تتحكم في وقت تزويد الموقع وكيفية تزويده.</span><span class="sxs-lookup"><span data-stu-id="b2233-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="b2233-163">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b2233-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="b2233-164">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b2233-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b2233-165">في القسم **نظرة عامة**، حدد البند حيث تم تعيين الحقل **قالب إعادة التزويد** إلى *طلب التزويد*.</span><span class="sxs-lookup"><span data-stu-id="b2233-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="b2233-166">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-166">Set the following values:</span></span>

    - <span data-ttu-id="b2233-167">**كود خطوة الموجة:** *تزويد*</span><span class="sxs-lookup"><span data-stu-id="b2233-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="b2233-168">**السماح بطلب الموجه لاستخدام كميات غير محجوزة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="b2233-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="b2233-169">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b2233-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="b2233-170">قالب الموجة</span><span class="sxs-lookup"><span data-stu-id="b2233-170">Wave template</span></span>

1. <span data-ttu-id="b2233-171">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b2233-172">في الجزء الأيمن، قم بتعيين حقل **نوع قالب الموجة** إلى *شحن*.</span><span class="sxs-lookup"><span data-stu-id="b2233-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="b2233-173">حدد القالب **61 شحن** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="b2233-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="b2233-174">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b2233-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b2233-175">في علامة التبويب السريعة **عام**، قم بتعيين خيار **أتمتة إصدار عمل التزويد‬** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="b2233-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="b2233-176">عيّن هذا الخيار إلى *لا* لإنشاء عمل التزويد على أساس الطلب وإصداره تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="b2233-177">يجب إضافة أسلوب موجة التزويد إلى قالب الموجة، وإنشاء قالب تزويد من نوع **طلب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="b2233-178">قم بإعداد قالب تزويد في صفحة **قوالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b2233-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="b2233-179">لإعداد قالب تزويد، يجب إضافة أسلوب التزويد إلى قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="b2233-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="b2233-180">على علامة التبويب السريع **الأساليب**، في عمود **الأساليب المحددة**، ابحث عن البند التالي:</span><span class="sxs-lookup"><span data-stu-id="b2233-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="b2233-181">**اسم الأسلوب:** *تزويد*</span><span class="sxs-lookup"><span data-stu-id="b2233-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="b2233-182">**الاسم:** *تزويد*</span><span class="sxs-lookup"><span data-stu-id="b2233-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="b2233-183">قم بتعيين الحقل **كود خطوة الموجة** لهذا البند إلى *تزويد*.</span><span class="sxs-lookup"><span data-stu-id="b2233-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="b2233-184">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b2233-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b2233-185">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="b2233-185">Example scenario</span></span>

<span data-ttu-id="b2233-186">بعد جعل كافة عينات البيانات التي تم وصفها سابقًا متوفرة ثم إعدادها، يمكنك العمل عبر هذا السيناريو لتجربة ميزة *تزويد أعلى من سعة الموقع‬*.</span><span class="sxs-lookup"><span data-stu-id="b2233-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="b2233-187">تفترض القيم التي يتم عرضها في هذا السيناريو أنك تعمل مع بيانات العرض التوضيحي القياسية، وأنك حددت الكيان القانوني **USMF**، وأنك أعددت عينات السجلات التي ورد وصفها سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b2233-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="b2233-188">يعمل هذا السيناريو أيضًا كمثال يوضح كيفية استخدام الميزة في إعداد الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b2233-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="b2233-189">إنشاء عمل التزويد</span><span class="sxs-lookup"><span data-stu-id="b2233-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="b2233-190">إنشاء أمر مبيعات 1</span><span class="sxs-lookup"><span data-stu-id="b2233-190">Create sales order 1</span></span>

1. <span data-ttu-id="b2233-191">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="b2233-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b2233-192">في جزء الإجراءات، حدد **جديد** لفتح مربع حوار لإنشاء أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="b2233-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="b2233-193">في مربع الحوار، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="b2233-194">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b2233-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b2233-195">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b2233-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b2233-196">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b2233-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="b2233-197">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="b2233-197">The new sales order is opened.</span></span> <span data-ttu-id="b2233-198">ويتضمن بندًا جديدًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b2233-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2233-199">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2233-200">**رقم الصنف:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="b2233-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="b2233-201">**الكمية:** *40*</span><span class="sxs-lookup"><span data-stu-id="b2233-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="b2233-202">على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="b2233-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="b2233-203">في صفحة **الحجز**، حدد **حجز دفعة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="b2233-204">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2233-204">Close the page.</span></span>
1. <span data-ttu-id="b2233-205">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="b2233-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b2233-206">ستتلقى رسائل إخبارية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b2233-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="b2233-207">كما يتم إنشاء موجة تزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="b2233-208">تتلقى أيضًا رسالة تحذير تفيد بما يلي "لا يمكن إلغاء حظر معرف العمل XXXX بسبب وجود عمل تزويد غير منجز."</span><span class="sxs-lookup"><span data-stu-id="b2233-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="b2233-209">إنشاء أمر مبيعات 2</span><span class="sxs-lookup"><span data-stu-id="b2233-209">Create sales order 2</span></span>

1. <span data-ttu-id="b2233-210">في صفحة **كافة أوامر المبيعات**، في جزء الإجراءات، حدد **جديد** لفتح مربع حوار لإنشاء أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="b2233-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="b2233-211">في مربع الحوار، قم بتعيين القيمة التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="b2233-212">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b2233-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b2233-213">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b2233-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b2233-214">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b2233-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="b2233-215">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="b2233-215">The new sales order is opened.</span></span> <span data-ttu-id="b2233-216">ويتضمن بندًا جديدًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b2233-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2233-217">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2233-218">**رقم الصنف:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="b2233-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="b2233-219">**الكمية:** *60*</span><span class="sxs-lookup"><span data-stu-id="b2233-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="b2233-220">على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="b2233-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="b2233-221">في صفحة **الحجز**، حدد **حجز دفعة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="b2233-222">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2233-222">Close the page.</span></span>
1. <span data-ttu-id="b2233-223">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="b2233-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b2233-224">ستتلقى رسائل إخبارية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b2233-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="b2233-225">كما يتم إنشاء موجة تزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="b2233-226">تتلقى أيضًا رسالة تحذير تفيد بما يلي "لا يمكن إلغاء حظر معرف العمل XXXX بسبب وجود عمل تزويد غير منجز."</span><span class="sxs-lookup"><span data-stu-id="b2233-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="b2233-227">إنشاء أمر مبيعات 3</span><span class="sxs-lookup"><span data-stu-id="b2233-227">Create sales order 3</span></span>

1. <span data-ttu-id="b2233-228">في صفحة **كافة أوامر المبيعات**، في جزء الإجراءات، حدد **جديد** لفتح مربع حوار لإنشاء أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="b2233-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="b2233-229">في مربع الحوار، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="b2233-230">**حساب العميل:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b2233-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="b2233-231">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b2233-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b2233-232">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b2233-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="b2233-233">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="b2233-233">The new sales order is opened.</span></span> <span data-ttu-id="b2233-234">ويتضمن بندًا جديدًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b2233-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2233-235">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b2233-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2233-236">**رقم الصنف:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="b2233-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="b2233-237">**الكمية:** *30*</span><span class="sxs-lookup"><span data-stu-id="b2233-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="b2233-238">على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="b2233-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="b2233-239">في صفحة **الحجز**، حدد **حجز دفعة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="b2233-240">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2233-240">Close the page.</span></span>
1. <span data-ttu-id="b2233-241">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="b2233-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b2233-242">ستتلقى رسائل إخبارية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b2233-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="b2233-243">كما يتم إنشاء موجة تزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="b2233-244">تتلقى أيضًا رسالة تحذير تفيد بما يلي "لا يمكن إلغاء حظر معرف العمل XXXX بسبب وجود عمل تزويد غير منجز."</span><span class="sxs-lookup"><span data-stu-id="b2233-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="b2233-245">عرض تفاصيل العمل</span><span class="sxs-lookup"><span data-stu-id="b2233-245">View work details</span></span>

1. <span data-ttu-id="b2233-246">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="b2233-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b2233-247">في القسم **نظرة عامة**، قم بتصفية عمود **المستودع** للمستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="b2233-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="b2233-248">يجب أن يتبين لك أنه تم إنشاء سبعة معرفات عمل لأوامر المبيعات الثلاث عند الطلب.</span><span class="sxs-lookup"><span data-stu-id="b2233-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="b2233-249">تتضمن ثلاثة معرفات من معرفات العمل السبعة قيمة **التزويد** بالنسبة إلى *نوع أمر العمل*، وتتضمن أربعة من هذه المعرفات قيمة **أوامر المبيعات** بالنسبة إلى *نوع أمر العمل*.</span><span class="sxs-lookup"><span data-stu-id="b2233-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="b2233-250">تتضمن معرفات العمل الثلاثة التي لديها قيمة **التزويد** بالنسبة إلى *نوع أمر العمل* مواقع *الانتقاء* و *التخزين* نفسها في قسم **البنود**:</span><span class="sxs-lookup"><span data-stu-id="b2233-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="b2233-251">**انتقاء:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="b2233-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="b2233-252">**تخزين:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="b2233-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="b2233-253">تم إنشاء معرفي عمل لأمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="b2233-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="b2233-254">قم بتدوين معرفات العمل لأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b2233-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="b2233-255">بحسب الكميات الفعلية، قد تختلف كميات العمل التي يتم إنشاؤها بشكل طفيف.</span><span class="sxs-lookup"><span data-stu-id="b2233-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="b2233-256">ومع ذلك، يجب ان تتطابق رؤوس العمل التي يتم إنشاؤها مع مثال السيناريو هذا بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="b2233-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="b2233-257">معرف لوحة ترخيص المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="b2233-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="b2233-258">في وقت لاحق في هذا السيناريو، ستستخدم تطبيق المستودع (أو المحاكي) ، حيث يجب عليك تحديد لوحة الترخيص لإكمال سيناريوهات الانتقاء والتزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="b2233-259">للعثور على معرفات لوحة الترخيص التي ستحتاج اليها لاحقًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b2233-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="b2233-260">انتقل إلى **إدارة المخزون \> الاستعلامات والتقارير \> قائمة المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="b2233-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="b2233-261">حدد الزر **إظهار عوامل التصفية** لفتح جزء عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="b2233-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="b2233-262">أدخل معايير التصفية التالية للحصول على لوحات الترخيص للسيناريو.</span><span class="sxs-lookup"><span data-stu-id="b2233-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="b2233-263">استخدم عامل التصفية *يبدأ بـ*.</span><span class="sxs-lookup"><span data-stu-id="b2233-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="b2233-264">**رقم الصنف:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="b2233-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="b2233-265">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="b2233-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b2233-266">حدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-266">Select **Apply**.</span></span>
1. <span data-ttu-id="b2233-267">في جزء الإجراءات، حدد **الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="b2233-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="b2233-268">في مربع الحوار **عرض الأبعاد**، في قسم **أبعاد التخزين**، حدد جميع القيم.</span><span class="sxs-lookup"><span data-stu-id="b2233-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="b2233-269">في قسم **الحركات**، حدد **رقم الصنف** و **الكمية \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="b2233-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="b2233-270">عند الانتهاء، حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b2233-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="b2233-271">تعرض شبكة **المخزون الفعلي** أرقام ألواح الترخيص للصنف *T0100* في كل موقع.</span><span class="sxs-lookup"><span data-stu-id="b2233-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="b2233-272">قم بتدوين لوحة الترخيص الموجودة في كل موقع، لأنك ستحتاج إلى هذه المعلومات لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="b2233-273">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2233-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="b2233-274">خطوات العملية</span><span class="sxs-lookup"><span data-stu-id="b2233-274">Process steps</span></span>

<span data-ttu-id="b2233-275">ستقوم بتنفيذ تزويد موقع المستودع لأول معرّفي عمل.</span><span class="sxs-lookup"><span data-stu-id="b2233-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="b2233-276">سيتم حظر العمل على عمل التزويد الثالث حتى ينخفض مستوى المخزون في موقع الانتقاء إلى أقل من الحد.</span><span class="sxs-lookup"><span data-stu-id="b2233-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="b2233-277">تزويد</span><span class="sxs-lookup"><span data-stu-id="b2233-277">Replenishment</span></span>

1. <span data-ttu-id="b2233-278">سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="b2233-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="b2233-279">(قم بإدخال *61* كمعرف المستخدم و *1* ككلمة مرور.)</span><span class="sxs-lookup"><span data-stu-id="b2233-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="b2233-280">انتقل إلى **المخزون \> التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b2233-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="b2233-281">تتم مطالبتك بإكمال عمل التزويد الأول.</span><span class="sxs-lookup"><span data-stu-id="b2233-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="b2233-282">يظهر رقم الصنف والكمية وموقع الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="b2233-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="b2233-283">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="b2233-284">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="b2233-285">يقوم النظام بإنشاء رقم لوحة الترخيص الهدف للوحة الترخيص الجديدة للصنف المنتقى.</span><span class="sxs-lookup"><span data-stu-id="b2233-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="b2233-286">حدد **موافق** لتأكيد القيمة.</span><span class="sxs-lookup"><span data-stu-id="b2233-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="b2233-287">يظهر عمل التخزين الذي يرشد المستخدم لوضع لوحة الترخيص الهدف في موقع التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="b2233-288">موقع *التخزين‏‎* يجب أن يكون **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="b2233-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="b2233-289">أكد تفاصيل التخزين، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="b2233-290">تتلقى رسالة "اكتمل العمل"، وتظهر تفاصيل مهمة انتقاء التزويد التالية: رقم الصنف والكمية والموقع للانتقاء منه.</span><span class="sxs-lookup"><span data-stu-id="b2233-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="b2233-291">سيكون موقع الانتقاء هو نفسه موقع التزويد الأول.</span><span class="sxs-lookup"><span data-stu-id="b2233-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="b2233-292">وبالتالي، سيكون للوحة الترخيص معرف لوحة الترخيص نفسه الذي تم استخدامه لمهمة عمل التزويد الأول.</span><span class="sxs-lookup"><span data-stu-id="b2233-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="b2233-293">كرر الخطوات السابقة لإكمال عمل التزويد لمهمة العمل الثانية.</span><span class="sxs-lookup"><span data-stu-id="b2233-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="b2233-294">سوف تختلف لوحة الترخيص الهدف والكمية عن لوحة الترخيص والكمية الهدف لمهمة العمل الأولى.</span><span class="sxs-lookup"><span data-stu-id="b2233-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="b2233-295">بعد اكتمال عمل التزويد الثاني، ستتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b2233-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b2233-296">يعلمك الجهاز المحمول أيضًا بعدم وجود عمل متاح، حتى لو تبقى بعض عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="b2233-297">يحدث هذا السلوك لأن حالة توافر عمل التزويد هي *معلّق* وبالتالي يحمل علامة **محظور**.</span><span class="sxs-lookup"><span data-stu-id="b2233-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="b2233-298">تم تشغيل الحالة *معلّق* لأن قيمة ملف تعريف الموقع لموقع الانتقاء الذي تم تعيين العمل له هي **كمية تجاوز السعة** من *0.65 PL*.</span><span class="sxs-lookup"><span data-stu-id="b2233-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="b2233-299">قامت المهمتان السابقتان لعمل التزويد بملء الموقع وصولاً إلى حد تجاوز السعة تقريبًا للصنف *T0100*.</span><span class="sxs-lookup"><span data-stu-id="b2233-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="b2233-300">(وحدة التحويل للصنف هي *1 PL = 100 ea*.) وبالتالي، قد يتسبب عمل التزويد المتبقي في تجاوز الموقع حد تجاوز السعة.</span><span class="sxs-lookup"><span data-stu-id="b2233-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="b2233-301">حتى يتم انتقاء مخزون كافٍ من الموقع لخفضه إلى أقل من حد إصدار العمل على قائمة الجهاز المحمول، سيبقى عمل التزويد هذا محظورًا.</span><span class="sxs-lookup"><span data-stu-id="b2233-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="b2233-302">انتقاء أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="b2233-302">Sales order pick</span></span>

<span data-ttu-id="b2233-303">قبل إتمام مهمة أمر عمل التزويد المتبقي، يجب تفريغ موقع الانتقاء من المخزون إلى مستوى حيث يمكن إلغاء حظر عمل التزويد المتبقي.</span><span class="sxs-lookup"><span data-stu-id="b2233-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="b2233-304">بمعنى آخر ، لا يمكن لمجموع كمية المخزون الفعلي في الموقع وكمية التزويد تجاوز القيمة **قيمة تجاوز السعة**.</span><span class="sxs-lookup"><span data-stu-id="b2233-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="b2233-305">عندما يكون هذا المجموعة أقل من كمية تجاوز السعة، سيتم حظر عمل التزويد المتبقي.</span><span class="sxs-lookup"><span data-stu-id="b2233-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="b2233-306">سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="b2233-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="b2233-307">(قم بإدخال *61* كمعرف المستخدم و *1* ككلمة مرور.)</span><span class="sxs-lookup"><span data-stu-id="b2233-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="b2233-308">انتقل إلى **الصادر \> انتقاء المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b2233-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="b2233-309">ادخل معرف العمل الأول لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="b2233-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="b2233-310">راجع معرفات العمل الخاصة بأوامر المبيعات التي سجلتها في وقت سابق، في صفحة **تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="b2233-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="b2233-311">سيقوم معرف العمل الذي تقوم بإدخاله هنا بإنشاء عمل الانتقاء للكمية 10 وحدات من موقعين منفصلين.</span><span class="sxs-lookup"><span data-stu-id="b2233-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="b2233-312">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-312">Select **OK**.</span></span>

    <span data-ttu-id="b2233-313">تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه للموقع الأول.</span><span class="sxs-lookup"><span data-stu-id="b2233-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="b2233-314">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="b2233-315">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="b2233-316">تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه للموقع التالي.</span><span class="sxs-lookup"><span data-stu-id="b2233-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="b2233-317">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="b2233-318">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="b2233-319">ترشدك صفحة **أوامر المبيعات: تخزين** إلى تخزين عملي الانتقاء المكتملين في الموقع المرحلي الصادر.</span><span class="sxs-lookup"><span data-stu-id="b2233-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="b2233-320">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-320">Select **OK**.</span></span>

    <span data-ttu-id="b2233-321">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b2233-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b2233-322">ادخل معرف العمل الثاني لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="b2233-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="b2233-323">توجد مهمة انتقاء واحدة فقط لمعرف العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="b2233-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="b2233-324">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-324">Select **OK**.</span></span>

    <span data-ttu-id="b2233-325">تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه.</span><span class="sxs-lookup"><span data-stu-id="b2233-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="b2233-326">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="b2233-327">ستكون لوحة الترخيص التي تحددها إحدى لوحات الترخيص التي أنشأها النظام من مهام عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="b2233-328">للتأكد من التقاط المعرف الصحيح للوحة الترخيص، راجع المخزون في صفحة **قائمة المخزون الفعلي** للصنف والموقع والكمية.</span><span class="sxs-lookup"><span data-stu-id="b2233-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="b2233-329">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="b2233-330">أكد الإرشادات الخاصة بمهمة التخزين في الموقع المرحلي الصادر.</span><span class="sxs-lookup"><span data-stu-id="b2233-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="b2233-331">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-331">Select **OK**.</span></span>

    <span data-ttu-id="b2233-332">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b2233-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="b2233-333">يتم حظر أمر المبيعات من الانتقاء لأن مهمة التزويد المرتبط بها غير مكتملة.</span><span class="sxs-lookup"><span data-stu-id="b2233-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="b2233-334">في الوقت الحالي، لا يزال هناك كميه تبلغ 30 وحدة في موقع الانتقاء، وكمية التزويد لأمر المبيعات 2 هي 60 وحدة.</span><span class="sxs-lookup"><span data-stu-id="b2233-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="b2233-335">يتجاوز مجموع المخزون الفعلي ومخزون التزويد (90 وحدة) كمية التجاوز التي تبلغ 0.65 بل (أو 65 وحدة).</span><span class="sxs-lookup"><span data-stu-id="b2233-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="b2233-336">قبل أن يتم إكمال عمل التزويد، يجب انتقاء أمر المبيعات 3.</span><span class="sxs-lookup"><span data-stu-id="b2233-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="b2233-337">ادخل معرف العمل لأمر المبيعات رقم 3.</span><span class="sxs-lookup"><span data-stu-id="b2233-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="b2233-338">توجد مهمة انتقاء واحدة فقط لمعرف العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="b2233-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="b2233-339">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-339">Select **OK**.</span></span>

    <span data-ttu-id="b2233-340">تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه.</span><span class="sxs-lookup"><span data-stu-id="b2233-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="b2233-341">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="b2233-342">ستكون لوحة الترخيص التي تحددها إحدى لوحات الترخيص التي أنشأها النظام من مهام عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="b2233-343">للتأكد من التقاط المعرف الصحيح للوحة الترخيص، راجع المخزون في صفحة **قائمة المخزون الفعلي** للصنف والموقع والكمية.</span><span class="sxs-lookup"><span data-stu-id="b2233-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="b2233-344">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="b2233-345">أكد الإرشادات الخاصة بمهمة التخزين في الموقع المرحلي الصادر.</span><span class="sxs-lookup"><span data-stu-id="b2233-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="b2233-346">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-346">Select **OK**.</span></span>

    <span data-ttu-id="b2233-347">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b2233-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="b2233-348">فور أن يصبح مجموعة الكمية الفعلية في موقع الانتقاء وكمية التزويد أقل من الحد، ستتمكن من معالجة عمل التزويد المتبقي.</span><span class="sxs-lookup"><span data-stu-id="b2233-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="b2233-349">عد إلى صفحة **تفاصيل العمل**، ولاحظ أن توافر عمل التزويد للقطعة الأخيرة من التزويد (لأمر المبيعات 2) هي *مفتوح*، بسبب وجود مساحة كافية في الموقع لقبول التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="b2233-350">يمكنك الآن معالجة عمل التزويد عبر الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="b2233-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="b2233-351">انتقل إلى **المخزون \> التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b2233-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="b2233-352">تتم مطالبتك بإكمال عمل التزويد المتبقي.</span><span class="sxs-lookup"><span data-stu-id="b2233-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="b2233-353">يظهر رقم الصنف والكمية وموقع الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="b2233-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="b2233-354">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="b2233-355">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="b2233-356">يقوم النظام بإنشاء رقم لوحة الترخيص الهدف للوحة الترخيص الجديدة للصنف المنتقى.</span><span class="sxs-lookup"><span data-stu-id="b2233-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="b2233-357">حدد **موافق** لتأكيد القيمة.</span><span class="sxs-lookup"><span data-stu-id="b2233-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="b2233-358">يظهر عمل التخزين الذي يرشد المستخدم لوضع لوحة الترخيص الهدف في موقع التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="b2233-359">موقع *التخزين‏‎* يجب أن يكون **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="b2233-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="b2233-360">أكد تفاصيل التخزين، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="b2233-361">تتلقى الرسالتين "اكتمل العمل" و"لا يوجد عمل متاح".</span><span class="sxs-lookup"><span data-stu-id="b2233-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="b2233-362">يمكنك الآن انتقاء أمر المبيعات رقم 2.</span><span class="sxs-lookup"><span data-stu-id="b2233-362">You can now pick sales order 2.</span></span> <span data-ttu-id="b2233-363">أصبح غير محظور عند اكتمال عمل التزويد المرتبط بأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b2233-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="b2233-364">ادخل معرف العمل لأمر المبيعات رقم 2.</span><span class="sxs-lookup"><span data-stu-id="b2233-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="b2233-365">توجد مهمة انتقاء واحدة فقط لمعرف العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="b2233-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="b2233-366">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-366">Select **OK**.</span></span>

    <span data-ttu-id="b2233-367">تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه.</span><span class="sxs-lookup"><span data-stu-id="b2233-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="b2233-368">في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="b2233-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="b2233-369">ستكون لوحة الترخيص التي تحددها لوحة الترخيص التي أنشأها النظام من مهمة عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="b2233-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="b2233-370">للتأكد من التقاط المعرف الصحيح للوحة الترخيص، راجع المخزون في صفحة **قائمة المخزون الفعلي** للصنف والموقع والكمية.</span><span class="sxs-lookup"><span data-stu-id="b2233-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="b2233-371">حدد الزر **موافق** (أيقونة علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="b2233-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="b2233-372">أكد الإرشادات الخاصة بمهمة التخزين في الموقع المرحلي الصادر.</span><span class="sxs-lookup"><span data-stu-id="b2233-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="b2233-373">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b2233-373">Select **OK**.</span></span>

    <span data-ttu-id="b2233-374">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b2233-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="b2233-375">ملاحظات وتلميحات</span><span class="sxs-lookup"><span data-stu-id="b2233-375">Notes and tips</span></span>

- <span data-ttu-id="b2233-376">تعمل هذه الوظيفة مع كافة أنواع التزويد: طلب الموجة والحد الأدنى/الحد الأقصى وطلب التحميل وتقسيم المستودع.</span><span class="sxs-lookup"><span data-stu-id="b2233-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="b2233-377">يمكنك تجاوز توافر عمل التزويد يدويًا لكل رأس عمل من صفحة **تفاصيل العمل** إذا كنت ترغب في ذلك.</span><span class="sxs-lookup"><span data-stu-id="b2233-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="b2233-378">عندما يقوم النظام بتعيين توافر عمل التزويد، يأخذ في الاعتبار أي مخزون موجود في الموقع قبل إكمال أي عمل.</span><span class="sxs-lookup"><span data-stu-id="b2233-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="b2233-379">يتم ربط كل قطة من عمل أمر المبيعات بعمل تزويد معين.</span><span class="sxs-lookup"><span data-stu-id="b2233-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="b2233-380">لا توجد وظيفة توافر أمر مبيعات مقابل.</span><span class="sxs-lookup"><span data-stu-id="b2233-380">There is no corresponding sales work availability functionality.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]