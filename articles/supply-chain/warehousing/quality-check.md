---
title: فحص الجودة
description: يوفر هذا الموضوع معلومات حول ميزة فحص الجودة. تسمح هذه الميزة للعاملين في المستودع بإجراء عمليات عشوائية سريعة لفحص الجودة أثناء استلام الأصناف في منطقة الرصيف الداخلية.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 60d566e3ef1fa4bc0cea960f7c75094f51823550
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838216"
---
# <a name="quality-check"></a><span data-ttu-id="b59b4-104">فحص الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b59b4-105">تسمح ميزة *فحص الجودة* للعاملين في المستودع بإجراء عمليات عشوائية سريعة لفحص الجودة أثناء استلام الأصناف في منطقة المساحة الداخلية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="b59b4-106">تعتبر عمليات الفحص العشوائية هذه مفيدة عند قيام العاملين بفحص التعبئة أو الأجزاء الأخرى التي يسهل التعرف عليها في أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="b59b4-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="b59b4-107">تقوم الميزة بإرشاد العاملين لإلقاء نظرة سريعة لمعرفة ما إذا كان هناك أي شيء يوجد به خلل أو تلف واضح قبل وضع المخزون في مكانه المناسب.</span><span class="sxs-lookup"><span data-stu-id="b59b4-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="b59b4-108">هذه الميزة عبارة عن بديل لعملية فحص الجودة القياسية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="b59b4-109">وهي تقدم المزيد من المرونة إلى جانب معالجة أسرع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="b59b4-110">عند استخدام هذه الميزة، يحدث الفحص عند الوصول وفحص الجودة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="b59b4-111">عند وصول شحنة، يقوم عامل المستودع بتسجيل الوصول.</span><span class="sxs-lookup"><span data-stu-id="b59b4-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="b59b4-112">يقوم العامل أيضًا بمسح لوحة الترخيص لتسجيل الموقع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="b59b4-113">يجري العامل عملية فحص جودة سريعة ويسجل ل النتيجة (نجح أو فشل) للوحة الترخيص هذه.</span><span class="sxs-lookup"><span data-stu-id="b59b4-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="b59b4-114">يحدث أحد الأمور التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="b59b4-115">إذا نجحت عملية فحص الجودة، يتم قبول لوحة الترخيص وإرشادها إلى موقع استلام، كالمعتاد.</span><span class="sxs-lookup"><span data-stu-id="b59b4-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="b59b4-116">إذا فشلت عملية فحص الجودة، يتم رفض لوحة الترخيص، ويُعاد توجيه عمل التخزين إلى موقع بديل لمزيد من الفحص.</span><span class="sxs-lookup"><span data-stu-id="b59b4-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="b59b4-117">يتم إنشاء أمر جودة جديد.</span><span class="sxs-lookup"><span data-stu-id="b59b4-117">A new quality order is created.</span></span> <span data-ttu-id="b59b4-118">لعرض أمر الجودة الذي تم إنشاؤه من عملية الفحص الفاشلة، انتقل إلى **إدارة المخزون \> المهام الدورية \> إدارة الجودة \> أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="b59b4-119">يمكن أيضًا إعداد هذه العملية بحيث يتم تحويل جميع لوحات الترخيص التي تم إجراء مسح لها إلى موقع فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="b59b4-120">تشغيل ميزة فحص الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="b59b4-121">قبل أن تتمكن من استخدام ميزة *فحص الجودة*، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="b59b4-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b59b4-122">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b59b4-123">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b59b4-124">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="b59b4-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b59b4-125">**اسم الميزة:** *فحص الجودة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="b59b4-126">إعداد الميزة السيناريو المثال</span><span class="sxs-lookup"><span data-stu-id="b59b4-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="b59b4-127">يوفر هذا القسم إرشادات ومثال يوضح كيفيه إعداد ميزة *فحص الجودة* وتجهيز عينة البيانات للسيناريو المثال الذي يتم توفيره لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="b59b4-128">جعل بيانات العينة متاحة</span><span class="sxs-lookup"><span data-stu-id="b59b4-128">Make sample data available</span></span>

<span data-ttu-id="b59b4-129">للعمل عبر [السيناريو المثال](#example-scenario) باستخدام عينات البيانات والسجلات المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span><span class="sxs-lookup"><span data-stu-id="b59b4-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b59b4-130">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="b59b4-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="b59b4-131">قالب فحص الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-131">Quality check template</span></span>

<span data-ttu-id="b59b4-132">يحدد قالب فحص الجودة قواعد إجراء عمليات فحص جودة عشوائية سريعة عند الاستلام.</span><span class="sxs-lookup"><span data-stu-id="b59b4-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="b59b4-133">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> قالب فحص الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="b59b4-134">حدد **جديد** لإضافة قالب إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="b59b4-135">عيّن القيم التالية لتعريف القالب الجديد:</span><span class="sxs-lookup"><span data-stu-id="b59b4-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="b59b4-136">**اسم قالب فحص الجودة:** *فحص الأرصفة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="b59b4-137">أدخل اسمًا يحدد السياسات المطبقة لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="b59b4-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="b59b4-138">**سياسة القبول:** *مطالبة المستخدم*</span><span class="sxs-lookup"><span data-stu-id="b59b4-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="b59b4-139">حدد ما إذا كان يجب أن تتم مطالبة المستخدمين بقبول جودة المخزون أو رفضها أثناء قيامهم بمعالجة العمل، أو ما إذا كان يجب رفض الجودة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b59b4-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="b59b4-140">الخيارات المتوفرة هي *رفض تلقائي* و *مطالبة المستخدم*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="b59b4-141">**سياسة معالجة الجودة:** *إنشاء أمر الجودة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="b59b4-142">حدد السياسة التي ينبغي اتباعها عند رفض جودة المخزون</span><span class="sxs-lookup"><span data-stu-id="b59b4-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="b59b4-143">وتتوفر الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-143">The following options are available:</span></span>

        - <span data-ttu-id="b59b4-144">*إنشاء العمل فقط* - أنشئ العمل فقط لتسهيل حركة المخزون.</span><span class="sxs-lookup"><span data-stu-id="b59b4-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="b59b4-145">*إنشاء أمر الجودة* – إنشاء أمر الجودة لتسهيل اختبارات الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="b59b4-146">**مجموعه الاختبار:** *الحاوية*</span><span class="sxs-lookup"><span data-stu-id="b59b4-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="b59b4-147">حدد مجموعة الاختبار التي يجب استخدامها في أمر الجودة الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="b59b4-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="b59b4-148">يتم إعداد مجموعات الاختبار في وحدة **إدارة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="b59b4-149">اترك الخيار **اختبار تحديد القدرة‬** متوقفًا عن التشغيل لمجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b59b4-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="b59b4-150">يحدد هذا الخيار ما إذا كان سيتم إتلاف العينة كجزء من الاختبارات في مجموعة الاختبارات.</span><span class="sxs-lookup"><span data-stu-id="b59b4-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="b59b4-151">إذا تم استخدام اختبار تحديد القدرة، فسيقوم النظام بإنشاء حركة مخزون عند إنشاء أمر جودة لأحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="b59b4-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="b59b4-152">وتتنبأ حركة المخزون الجديدة بخفض المخزون لكمية الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b59b4-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="b59b4-153">يحدث انخفاض المخزون عند إكمال أمر الجودة من خلال خطوة التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="b59b4-154">يتم تحديد العمليات المخزنية كأمر جودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="b59b4-155">فئة العمل – فحص الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-155">Work class – Quality check</span></span>

<span data-ttu-id="b59b4-156">تُستخدم فئات العمل لتوجيه و/أو الحد من نوع بنود أوامر العمل التي يستطيع عاملو مستودع معالجتها على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="b59b4-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="b59b4-157">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b59b4-158">حدد **جديد** لإنشاء فئة عمل.</span><span class="sxs-lookup"><span data-stu-id="b59b4-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="b59b4-159">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="b59b4-160">**معرف فئة العمل:** *فحص QC*</span><span class="sxs-lookup"><span data-stu-id="b59b4-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="b59b4-161">أدخل اسمًا يحدد فئة العمل.</span><span class="sxs-lookup"><span data-stu-id="b59b4-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="b59b4-162">**الوصف:** *فحص QC*</span><span class="sxs-lookup"><span data-stu-id="b59b4-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="b59b4-163">أدخل وصفًا قصيرًا يشير إلى سبب استخدام فئة العمل.</span><span class="sxs-lookup"><span data-stu-id="b59b4-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="b59b4-164">**نوع أمر العمل:** *الجودة في فحص الجودة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="b59b4-165">حدد نوع أمر العمل الذي يتم إنشاؤه بواسطة فئة العمل.</span><span class="sxs-lookup"><span data-stu-id="b59b4-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="b59b4-166">عند إعداد عمل التحكم في الجودة، حدد دائمًا *الجودة في فحص الجودة*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="b59b4-167">على علامة التبويب السريعة **أنواع مواقع التخزين الصالحة**، اترك الحقل **نوع الموقع** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b59b4-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="b59b4-168">إذا قمت بتحديد نوع الموقع، فأنت تحدد المواقع التي يمكن وضع الأصناف فيها بعد انتقائها.</span><span class="sxs-lookup"><span data-stu-id="b59b4-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="b59b4-169">يُستخدم هذا الحقل عندما يحاول توجيه موقع حل الموقع أو عندما يحدد عامل مستودع الموقع لعنصر قائمة الجهاز المحمول يدوياً.</span><span class="sxs-lookup"><span data-stu-id="b59b4-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="b59b4-170">لمزيد من المعلومات حول فئات العمل وكيفية إنشائها، راجع [إنشاء فئة عمل](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="b59b4-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="b59b4-171">قالب العمل</span><span class="sxs-lookup"><span data-stu-id="b59b4-171">Work template</span></span>

<span data-ttu-id="b59b4-172">تتيح لك قوالب العمل تحديد عمليات العمل التي يجب القيام بها في المستودع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="b59b4-173">تتكون عمليات عمل المستودع عادةً من زوج من الإجراءات: عامل مستودع يقوم بانتقاء المخزون الفعلي في موقع واحد، ثم يضع المخزون المستلم في موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="b59b4-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="b59b4-174">يحدد قالب العمل الخاص بفحص الجودة عمليات العمل لإجراء عمليات فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="b59b4-175">أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="b59b4-175">Purchase orders</span></span>

1. <span data-ttu-id="b59b4-176">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b59b4-177">في الرأس، قم بتعيين الحقل **نوع أمر العمل** إلى *أوامر الشراء*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="b59b4-178">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b59b4-179">حدد قالب عمل ينبغي أن يتضمن خطوة فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="b59b4-180">في القسم **نظرة عامة**، في الحقل **قالب العمل**، حدد *إيصال أمر الشراء 51*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="b59b4-181">في القسم **تفاصيل قالب العمل**، لاحظ وجود بندين في الشبكة: بند *انتقاء* وبند *تخزين*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="b59b4-182">في القسم **تفاصيل قالب العمل**، حدد **جديد** لإضافة صف للتحكم في الجودة بالشبكة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="b59b4-183">لاحظ أن **رقم البند** للبند الجديد معين إلى *3*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="b59b4-184">في البند الجديد، قم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-184">On the new line, set the following values.</span></span> <span data-ttu-id="b59b4-185">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="b59b4-186">**نوع العمل:** *فحص الجودة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="b59b4-187">**معرف فئة العمل:** *شراء*</span><span class="sxs-lookup"><span data-stu-id="b59b4-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="b59b4-188">**اسم قالب فحص الجودة:** *فحص الأرصفة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="b59b4-189">حدد المعرّف الفريد لفئة العمل.</span><span class="sxs-lookup"><span data-stu-id="b59b4-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="b59b4-190">تستخدم هذه القيمة لتكوين عناصر القائمة بالجهاز المحمول وأنواع العمل التي يمكن معالجتها بواسطة تلك العناصر في القائمة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="b59b4-191">في جزء الإجراءات، حدد **حفظ** لحفظ عملك حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="b59b4-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="b59b4-192">تتلقى رسالة إخبارية تفيد بما يلي: "غير صالح - يجب أن يأتي فحص الجودة مباشرةً بعد الانتقاء"</span><span class="sxs-lookup"><span data-stu-id="b59b4-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="b59b4-193">وبالتالي، يجب تغيير قيمة **رقم البند** للبند الذي أضفته.</span><span class="sxs-lookup"><span data-stu-id="b59b4-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="b59b4-194">اتبع الخطوات التالية لتغيير قيمة **رقم البند** للبند الجديد:</span><span class="sxs-lookup"><span data-stu-id="b59b4-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="b59b4-195">في القسم **تفاصيل قالب العمل**، حدد البند حيث تم تعيين الحقل **نوع العمل** إلى *فحص الجودة*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="b59b4-196">حدد الزر **تحريك لأعلى** أو **تحريك لأسفل** لتحريك بند *فحص الجودة* لوضعه بعد بند *الانتقاء*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="b59b4-197">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="b59b4-198">الجودة في فحص الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-198">Quality in quality check</span></span>

<span data-ttu-id="b59b4-199">بعد ذلك، أنشئ قالب عمل لفحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="b59b4-200">في رأس الصفحة **قوالب العمل**، قم بتغيير قيمة الحقل **نوع أمر العمل** إلى *الجودة في فحص الجودة*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="b59b4-201">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة في القسم **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="b59b4-202">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b59b4-203">**قالب العمل:** *فحص الجودة 51*</span><span class="sxs-lookup"><span data-stu-id="b59b4-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="b59b4-204">أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="b59b4-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="b59b4-205">**وصف قالب العمل:** *فحص الجودة 51*</span><span class="sxs-lookup"><span data-stu-id="b59b4-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="b59b4-206">في جزء الإجراءات، حدد **حفظ** لإتاحة القسم **تفاصيل قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="b59b4-207">بينما لا يزال القالب الجديد محددًا في القسم **نظرة عامة**، حدد **جديد** في القسم **تفاصيل قالب العمل** لإضافة صف جديد إلى الشبكة هنا.</span><span class="sxs-lookup"><span data-stu-id="b59b4-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="b59b4-208">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b59b4-209">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="b59b4-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b59b4-210">**معرف فئة العمل:** *فحص QC*</span><span class="sxs-lookup"><span data-stu-id="b59b4-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="b59b4-211">حدد اسم [فئة العمل](#work-class) التي أنشأتها سابقًا لعمل فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="b59b4-212">في قسم **تفاصيل قالب العمل**، حدد **جديد** لإضافة صف جديد.</span><span class="sxs-lookup"><span data-stu-id="b59b4-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="b59b4-213">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b59b4-214">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="b59b4-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b59b4-215">**معرف فئة العمل:** *فحص QC*</span><span class="sxs-lookup"><span data-stu-id="b59b4-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="b59b4-216">حدد اسم [فئة العمل](#work-class) التي أنشأتها سابقًا لعمل فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="b59b4-217">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="b59b4-218">لمزيد من المعلومات حول قوالب العمل، راجع [مراقبة عمل المستودع باستخدام قوالب العمل والتوجيهات المتعلقة بالموقع](control-warehouse-location-directives.md).</span><span class="sxs-lookup"><span data-stu-id="b59b4-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="b59b4-219">توجيه الموقع – حالات فشل الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-219">Location directive – Quality failures</span></span>

<span data-ttu-id="b59b4-220">توجيهات الموقع هي القواعد التي تساعد في تحديد انتقاء ووضع مواقع لحركة المخزون.</span><span class="sxs-lookup"><span data-stu-id="b59b4-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="b59b4-221">على سبيل المثال، في حركة أمر مبيعات، يحدد توجيه الموقع أين سيتم انتقاء الأصناف وأين سيتم وضع الأصناف المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="b59b4-222">يجب تكوين قاعدة توجيه الموقع لتحديد كيفية التعامل مع عمليات فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="b59b4-223">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b59b4-224">في الجزء الأيمن، قم بتعيين حقل **نوع أمر العمل**  إلى *أوامر الشراء* للعمل باستخدام توجيهات المواقع من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="b59b4-225">في جزء الإجراءات، حدد **جديد** لإنشاء توجيه الموقع لعمليات فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="b59b4-226">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="b59b4-227">**الرقم التسلسلي:** قبول القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b59b4-228">**الاسم:** *51 إلى الجودة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="b59b4-229">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية</span><span class="sxs-lookup"><span data-stu-id="b59b4-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="b59b4-230">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="b59b4-231">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="b59b4-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b59b4-232">**الموقع:** *5*</span><span class="sxs-lookup"><span data-stu-id="b59b4-232">**Site:** *5*</span></span>
    - <span data-ttu-id="b59b4-233">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b59b4-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b59b4-234">في جزء الإجراءات، حدد **حفظ** لحفظ التوجيه وجعل علامة التبويب السريعة **البنود** متاحة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b59b4-235">في علامة التبويب السريعة **السطور**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b59b4-236">في البند الجديد، قم بتعيين القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-236">On the new line, set the following values.</span></span> <span data-ttu-id="b59b4-237">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="b59b4-238">**من الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="b59b4-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="b59b4-239">**إلى الكمية:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="b59b4-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="b59b4-240">في جزء الإجراءات، حدد **حفظ** لحفظ البند الجديد وجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="b59b4-241">بينما لا يزال البند الجديد محددًا في علامة التبويب السريعة **البنود**، حدد **جديد** على علامة التبويب السريعة **إجراءات توجيه الموقع** لإضافة صف إلى الشبكة هناك، بحيث يمكنك إعداد إجراء للبند.</span><span class="sxs-lookup"><span data-stu-id="b59b4-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="b59b4-242">في الصف الجديد، قم بتعيين الحقل **الاسم** إلى *الجودة*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="b59b4-243">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="b59b4-244">في جزء الإجراءات، حدد **حفظ** لإتاحة الزر **تحرير الاستعلام** في علامة التبويب السريعة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="b59b4-245">بينما لا يزال البند الذي أضفته محددًا على علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **تحرير الاستعلام** لفتح مربع حوار حيث يمكنك تحرير الاستعلام للإجراء.</span><span class="sxs-lookup"><span data-stu-id="b59b4-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="b59b4-246">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة صف إلى الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="b59b4-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="b59b4-247">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b59b4-248">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="b59b4-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b59b4-249">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="b59b4-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b59b4-250">**الحقل:** *الموقع*</span><span class="sxs-lookup"><span data-stu-id="b59b4-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="b59b4-251">**المعايير:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="b59b4-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="b59b4-252">يعتبر *QMS* موقع مستودع للجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="b59b4-253">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b59b4-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="b59b4-254">يجب تغيير تسلسل توجيهات مواقع أمر الشراء الموجودة للمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="b59b4-255">احفظ توجيه الموقع الجديد *51 إلى الجودة* وقم بتحديث الصفحة، وحدد توجيه الموقع في القائمة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="b59b4-256">ثم استخدم الزرين **تحريك لأعلى** و **تحريك لأسفل** على جزء الإجراءات لوضع توجيه الموقع للمستودع *51* بالترتيب التالي.</span><span class="sxs-lookup"><span data-stu-id="b59b4-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="b59b4-257">(قبل أن تحدد **تحريك لأعلى** أو **تحريك لأسفل**، يجب أن تحدد توجيه موقع في القائمة.)</span><span class="sxs-lookup"><span data-stu-id="b59b4-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="b59b4-258">51 إلى الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-258">51 To Quality</span></span>
    2. <span data-ttu-id="b59b4-259">51 أمر شراء مباشر</span><span class="sxs-lookup"><span data-stu-id="b59b4-259">51 PO Direct</span></span>
    3. <span data-ttu-id="b59b4-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="b59b4-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="b59b4-261">أصناف قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="b59b4-261">Mobile device menu items</span></span>

<span data-ttu-id="b59b4-262">قم بتكوين عنصر قائمة بحيث يمكن للأجهزة المحمولة إجراء وظيفة **فحص الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="b59b4-263">تخزين الشراء</span><span class="sxs-lookup"><span data-stu-id="b59b4-263">Purchase putaway</span></span>

1. <span data-ttu-id="b59b4-264">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b59b4-265">في القائمة، حدد عنصر القائمة **تخزين الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="b59b4-266">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b59b4-267">في القسم **فئات العمل**، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b59b4-268">في الصف الجديد، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b59b4-269">**معرف فئة العمل:** *فحص QC*</span><span class="sxs-lookup"><span data-stu-id="b59b4-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="b59b4-270">أدخل اسم [فئة العمل](#work-class) التي أنشأتها سابقًا لعمل فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="b59b4-271">**نوع أمر العمل:** *الجودة في فحص الجودة*</span><span class="sxs-lookup"><span data-stu-id="b59b4-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="b59b4-272">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="b59b4-273">استلام بند أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="b59b4-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="b59b4-274">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b59b4-275">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b59b4-276">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="b59b4-277">**اسم عنصر القائمة:** *استلام سطر أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="b59b4-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="b59b4-278">**العنوان:** *استلام سطر أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="b59b4-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="b59b4-279">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="b59b4-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="b59b4-280">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="b59b4-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="b59b4-281">في علامة التبويب السريعة **عام**، عيّن القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="b59b4-282">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="b59b4-283">**عملية إنشاء العمل:** *استلام بند أمر الشراء وتخزينه*</span><span class="sxs-lookup"><span data-stu-id="b59b4-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="b59b4-284">**إنشاء لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="b59b4-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="b59b4-285">**قالب العمل:** *إيصال أمر الشراء 51*</span><span class="sxs-lookup"><span data-stu-id="b59b4-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="b59b4-286">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="b59b4-287">إضافة عنصر القائمة إلى قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="b59b4-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="b59b4-288">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="b59b4-289">في الجزء الأيمن، حدد القائمة **وارد**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="b59b4-290">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b59b4-291">في العمود **القوائم المتوفرة وعناصر القائمة**، حدد عنصر القائمة **استلام بند أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="b59b4-292">حدد زر السهم الأيمن لنقل **استلام بند أمر الشراء** إلى العمود **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="b59b4-293">في العمود **بنية القائمة**، حدد **استلام بند أمر الشراء**، ثم حدد زر السهم لأعلى أو زر السهم لأسفل لنقل عنصر القائمة إلى الموضع المطلوب على قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="b59b4-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="b59b4-294">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="b59b4-295">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="b59b4-295">Example scenario</span></span>

<span data-ttu-id="b59b4-296">بعد جعل كافة عينات البيانات التي تم وصفها سابقًا متوفرة ثم إعدادها، يمكنك العمل عبر هذا السيناريو لتجربة ميزة *فحص الجودة*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="b59b4-297">تفترض القيم التي يتم عرضها في هذا السيناريو أنك تعمل مع بيانات العرض التوضيحي القياسية، وأنك حددت الكيان القانوني **USMF**، وأنك أعددت عينات السجلات التي ورد وصفها سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="b59b4-298">يعمل هذا السيناريو أيضًا كمثال يوضح كيفية استخدام الميزة في إعداد الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b59b4-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b59b4-299">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="b59b4-299">Create a purchase order</span></span>

1. <span data-ttu-id="b59b4-300">انتقل إلى **التدبير والتوريد \> أوامر الشراء \> كل أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b59b4-301">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b59b4-302">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b59b4-303">**حساب المورّد:** *104*</span><span class="sxs-lookup"><span data-stu-id="b59b4-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="b59b4-304">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b59b4-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b59b4-305">حدد **موافق** لإغلاق مربع الحوار وفتح أمر الشراء الجديد.</span><span class="sxs-lookup"><span data-stu-id="b59b4-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="b59b4-306">على علامة التبويب السريعة **بنود أمر المبيعات**، تحتوي الشبكة على بند جديد فارغ.</span><span class="sxs-lookup"><span data-stu-id="b59b4-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="b59b4-307">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b59b4-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="b59b4-308">**رقم الصنف:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="b59b4-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="b59b4-309">**الكمية:** *3*</span><span class="sxs-lookup"><span data-stu-id="b59b4-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="b59b4-310">**الوحدة:** *PL*</span><span class="sxs-lookup"><span data-stu-id="b59b4-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="b59b4-311">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="b59b4-312">معالجة استلام فحص الجودة</span><span class="sxs-lookup"><span data-stu-id="b59b4-312">Process quality check receiving</span></span>

<span data-ttu-id="b59b4-313">بعد إنشاء أمر الشراء، يمكن استلامه باستخدام عنصر القائمة **استلام بند أمر الشراء** وكذلك وظيفة ميزة *فحص الجودة*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="b59b4-314">استلام البالته 1</span><span class="sxs-lookup"><span data-stu-id="b59b4-314">Receive pallet 1</span></span>

1. <span data-ttu-id="b59b4-315">سجل الدخول إلى تطبيق إدارة المستودع للأجهزة المحمولة كمستخدم ممكّن للمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-315">Sign in to the Warehouse Management mobile app as a user for warehouse *51*.</span></span> <span data-ttu-id="b59b4-316">(قم بإدخال *51* كمعرف المستخدم و *1* ككلمة مرور.)</span><span class="sxs-lookup"><span data-stu-id="b59b4-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="b59b4-317">انتقل إلى **وارد \> استلام بند أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="b59b4-318">في حقل **‎PONUM**، أدخل رقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b59b4-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="b59b4-319">أكد رقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b59b4-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="b59b4-320">في الحقل **رقم البند**، أدخل رقم بند أمر الشراء الذي يجري استلامه.</span><span class="sxs-lookup"><span data-stu-id="b59b4-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="b59b4-321">بسبب وجود بند واحد فقط في هذا السيناريو، ستقوم بإدخال *1* في الحقل **رقم البند** لكل خطوة استلام.</span><span class="sxs-lookup"><span data-stu-id="b59b4-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="b59b4-322">أكد رقم البند.</span><span class="sxs-lookup"><span data-stu-id="b59b4-322">Confirm the line number.</span></span>
1. <span data-ttu-id="b59b4-323">في حقل **‏‫الكمية**، أدخل الكمية المراد استلامها.</span><span class="sxs-lookup"><span data-stu-id="b59b4-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="b59b4-324">لأن أمر الشراء يتعلق بثلاث باليتات (*PL*) في هذا السيناريو، وهناك ثلاث خطوات استلام، ستدخل *1* في حقل **الكمية** لكل خطوة استلام.</span><span class="sxs-lookup"><span data-stu-id="b59b4-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="b59b4-325">قم بتأكيد الكمية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-325">Confirm the quantity.</span></span>

    <span data-ttu-id="b59b4-326">تظهر صفحة **فحص الجودة** التي لا تتضمن حقول إدخال.</span><span class="sxs-lookup"><span data-stu-id="b59b4-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="b59b4-327">تحتوي هذه الصفحة فقط على زر التأكيد (علامة اختيار) في الأسفل وزر القائمة (**≡**) في الأعلى.</span><span class="sxs-lookup"><span data-stu-id="b59b4-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="b59b4-328">(يُشار إلى زر القائمة أحيانًا على أنه هامبورجير‬‏‫ أو زر هامبورجير‬‏‫). لتسريع عملية فحص الجودة، عندما تجتاز الباليته فحص الجودة، يقوم المستخدم فقط بتأكيد صفحة **فحص الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="b59b4-329">![صفحة فحص الجودة](media/quality-check.png "صفحة فحص الجودة")</span><span class="sxs-lookup"><span data-stu-id="b59b4-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="b59b4-330">حدد زر التأكيد لاجتياز فحص الجودة للبالته 1 من البند 1.</span><span class="sxs-lookup"><span data-stu-id="b59b4-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="b59b4-331">تظهر صفحة **أوامر الشراء: تخزين** التي تعرض تفاصيل عمل التخزين:</span><span class="sxs-lookup"><span data-stu-id="b59b4-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="b59b4-332">**LOC:** الموقع الذي حدده النظام</span><span class="sxs-lookup"><span data-stu-id="b59b4-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="b59b4-333">هذا الموقع هو موقع التخزين المعين لاستلام أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b59b4-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="b59b4-334">**LP:** معرف لوحة الترخيص التي أنشأها النظام</span><span class="sxs-lookup"><span data-stu-id="b59b4-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="b59b4-335">**الصنف:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="b59b4-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="b59b4-336">**الكمية** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="b59b4-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="b59b4-337">يظهر أيضًا وصف الصنف.</span><span class="sxs-lookup"><span data-stu-id="b59b4-337">The item description is also shown.</span></span>

1. <span data-ttu-id="b59b4-338">قم بتأكيد عمل التخزين.</span><span class="sxs-lookup"><span data-stu-id="b59b4-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="b59b4-339">في صفحة **المهمة** لاستلام بند أمر الشراء، تتلقي رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b59b4-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b59b4-340">يتوفر الحقل **رقم البند** بحيث يمكنك بدء استلام البالته التالية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="b59b4-341">استلام البالته 2</span><span class="sxs-lookup"><span data-stu-id="b59b4-341">Receive pallet 2</span></span>

<span data-ttu-id="b59b4-342">بالنسبة لهذا السيناريو، سيتم رفض البالته 2.</span><span class="sxs-lookup"><span data-stu-id="b59b4-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="b59b4-343">في الحقل **رقم البند**، أدخل *1*، وأكد رقم البند.</span><span class="sxs-lookup"><span data-stu-id="b59b4-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="b59b4-344">يتوفر الآن حقل **الكمية‏‎**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-344">The **QTY** field is now available.</span></span> <span data-ttu-id="b59b4-345">ادخل *1*، وقم بتأكيد الكمية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="b59b4-346">تظهر صفحة **فحص الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-346">The **Quality check** page appears.</span></span> <span data-ttu-id="b59b4-347">بالنسبة لهذا الإيصال، سيتم رفض البالته للجودة، وسيتم وضعها في موقع *QMS*.</span><span class="sxs-lookup"><span data-stu-id="b59b4-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="b59b4-348">حدد زر القائمة (**≡**) في أعلى الصفحة، ثم في القائمة، حدد **رفض**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="b59b4-349">في صفحة **المهمة** التي تظهر، أدخل **QMS** كموقع *تخزين* لإرسال البالته إليه لإجراء المزيد من الفحص.</span><span class="sxs-lookup"><span data-stu-id="b59b4-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="b59b4-350">تظهر صفحة **الجودة في فحص الجودة: تخزين** التي تعرض تفاصيل عمل التخزين:</span><span class="sxs-lookup"><span data-stu-id="b59b4-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="b59b4-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="b59b4-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="b59b4-352">هذا الموقع هو موقع التخزين المعين لأمر الشراء المرفوض.</span><span class="sxs-lookup"><span data-stu-id="b59b4-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="b59b4-353">**LP:** معرف لوحة الترخيص التي أنشأها النظام</span><span class="sxs-lookup"><span data-stu-id="b59b4-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="b59b4-354">**الصنف:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="b59b4-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="b59b4-355">**الكمية** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="b59b4-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="b59b4-356">يظهر أيضًا وصف الصنف.</span><span class="sxs-lookup"><span data-stu-id="b59b4-356">The item description is also shown.</span></span>

1. <span data-ttu-id="b59b4-357">قم بتأكيد عمل التخزين.</span><span class="sxs-lookup"><span data-stu-id="b59b4-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="b59b4-358">في صفحة **المهمة** لاستلام بند أمر الشراء، تتلقي رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b59b4-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b59b4-359">يتوفر الحقل **رقم البند** بحيث يمكنك بدء استلام البالته التالية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="b59b4-360">لقد أكملت الآن عملية فحص الجودة وأنشأت أمر الجودة للبالته المرفوضة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="b59b4-361">لعرض الأمر الذي تم إنشاؤه، انتقل إلى **إدارة المخزون \> المهام الدورية \> إدارة الجودة \> أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="b59b4-362">يمكن الآن معالجة اختبار أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="b59b4-363">لم تتم تغطية اختبار الجودة في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="b59b4-364">لمزيد من المعلومات حول إدارة الجودة، راجع [نظرة عامة على إدارة الجودة](../inventory/enable-quality-management.md).</span><span class="sxs-lookup"><span data-stu-id="b59b4-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="b59b4-365">استلام البالته 3</span><span class="sxs-lookup"><span data-stu-id="b59b4-365">Receive pallet 3</span></span>

<span data-ttu-id="b59b4-366">بالنسبة لهذا السيناريو، سيتم قبول البالته 3.</span><span class="sxs-lookup"><span data-stu-id="b59b4-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="b59b4-367">في الحقل **رقم البند**، أدخل *1*، وأكد رقم البند.</span><span class="sxs-lookup"><span data-stu-id="b59b4-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="b59b4-368">يتوفر الآن حقل **الكمية‏‎**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-368">The **QTY** field is now available.</span></span> <span data-ttu-id="b59b4-369">ادخل *1*، وقم بتأكيد الكمية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="b59b4-370">تظهر صفحة **فحص الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b59b4-370">The **Quality check** page appears.</span></span> <span data-ttu-id="b59b4-371">بالنسبة لهذا الإيصال، سيتم قبول البالته للجودة، وسيتم وضعها في موقع تخزين مجمع.</span><span class="sxs-lookup"><span data-stu-id="b59b4-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="b59b4-372">حدد زر التأكيد لاجتياز فحص الجودة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="b59b4-373">تظهر صفحة **أوامر الشراء: تخزين** التي تعرض تفاصيل عمل التخزين:</span><span class="sxs-lookup"><span data-stu-id="b59b4-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="b59b4-374">**LOC:** الموقع الذي حدده النظام</span><span class="sxs-lookup"><span data-stu-id="b59b4-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="b59b4-375">هذا الموقع هو موقع التخزين المعين لاستلام أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b59b4-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="b59b4-376">**LP:** معرف لوحة الترخيص التي أنشأها النظام</span><span class="sxs-lookup"><span data-stu-id="b59b4-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="b59b4-377">**الصنف:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="b59b4-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="b59b4-378">**الكمية** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="b59b4-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="b59b4-379">يظهر أيضًا وصف الصنف.</span><span class="sxs-lookup"><span data-stu-id="b59b4-379">The item description is also shown.</span></span>

1. <span data-ttu-id="b59b4-380">قم بتأكيد عمل التخزين.</span><span class="sxs-lookup"><span data-stu-id="b59b4-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="b59b4-381">في صفحة **المهمة** لاستلام بند أمر الشراء، تتلقي رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b59b4-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b59b4-382">يتوفر الحقل **رقم البند** بحيث يمكنك بدء استلام البالته التالية.</span><span class="sxs-lookup"><span data-stu-id="b59b4-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="b59b4-383">حدد زر القائمة (**≡**) في أعلى الصفحة، ثم في القائمة، حدد **إلغاء** للرجوع إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="b59b4-384">يمكنك الآن إغلاق تطبيق الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="b59b4-384">You can now close the mobile app.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]