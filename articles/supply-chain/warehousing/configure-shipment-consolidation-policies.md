---
title: تكوين نُهج دمج الشحنات
description: يوضح هذا الموضوع كيفية إعداد نُهج دمج الشحنات الافتراضية والمخصصة.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: adb88bbd29a89a1d18d7fd4781c2541ffb4e721f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421712"
---
# <a name="configure-shipment-consolidation-policies"></a><span data-ttu-id="920a0-103">تكوين نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="920a0-103">Configure shipment consolidation policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="920a0-104">تسمح عملية دمج الشحنات التي تستخدم نُهج دمج الشحنات بالدمج التلقائي للشحنات أثناء الإصدار التلقائي واليدوي إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="920a0-104">The shipment consolidation process that uses shipment consolidation policies allows for automated shipment consolidation during automated and manual release to the warehouse.</span></span> <span data-ttu-id="920a0-105">بعد تشغيل هذه الميزة، يجب تكوين النهج الأولي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="920a0-105">After you turn on this feature, you must configure your initial policies.</span></span> <span data-ttu-id="920a0-106">إذا لم يتم تكوين أي نهج، سيقوم كل بند مبيعات بإنشاء شحنة منفصلة تحتوي على بند تحميل واحد.</span><span class="sxs-lookup"><span data-stu-id="920a0-106">If no policies are configured, each sales line will generate a separate shipment that has a single load line.</span></span>

<span data-ttu-id="920a0-107">توضح السيناريوهات الواردة في هذا الموضوع كيفية إعداد نُهج دمج الشحنات الافتراضية والمخصصة.</span><span class="sxs-lookup"><span data-stu-id="920a0-107">The scenarios that are presented in this topic show how to set up default and custom shipment consolidation policies.</span></span>

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a><span data-ttu-id="920a0-108">تشغيل ميزة نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="920a0-108">Turn on the Shipment consolidation policies feature</span></span>

> [!IMPORTANT]
> <span data-ttu-id="920a0-109">في [السيناريو الأول](#scenario-1) الموضح في هذا الموضوع، ستقوم أولا بإعداد مستودع بحيث يستخدم ميزة دمج الشحنات السابقة.</span><span class="sxs-lookup"><span data-stu-id="920a0-109">In the [first scenario](#scenario-1) that is described in this topic, you will first set up a warehouse so that it uses the earlier shipment consolidation feature.</span></span> <span data-ttu-id="920a0-110">وبعد ذلك ستقوم بإتاحة نُهج دمج الشحنات.</span><span class="sxs-lookup"><span data-stu-id="920a0-110">You will then make shipment consolidation policies available.</span></span> <span data-ttu-id="920a0-111">بهذه الطريقة، يمكنك تجربة كيف يعمل سيناريو الترقية.</span><span class="sxs-lookup"><span data-stu-id="920a0-111">In this way, you can experience how the upgrade scenario works.</span></span> <span data-ttu-id="920a0-112">إذا كنت تخطط لاستخدام بيئة بيانات العرض التوضيحي للانتقال عبر السيناريو الأول، فلا تقم بتشغيل الميزة قبل تنفيذ السيناريو.</span><span class="sxs-lookup"><span data-stu-id="920a0-112">If you plan to use a demo data environment to go through the first scenario, don't turn on the feature before you do the scenario.</span></span>

<span data-ttu-id="920a0-113">قبل أن تتمكن من استخدام ميزة *نُهج دمج الشحنات*، يجب تشغيلها في النظام لديك.</span><span class="sxs-lookup"><span data-stu-id="920a0-113">Before you can use the *Shipment consolidation policies* feature, you must turn it on in your system.</span></span> <span data-ttu-id="920a0-114">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="920a0-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="920a0-115">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="920a0-116">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="920a0-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="920a0-117">**اسم الميزة:** *دمج الشحنات*</span><span class="sxs-lookup"><span data-stu-id="920a0-117">**Feature name:** *Consolidate shipment*</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="920a0-118">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="920a0-118">Make demo data available</span></span>

<span data-ttu-id="920a0-119">يشير كل سيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="920a0-119">Each scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="920a0-120">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="920a0-120">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><span data-ttu-id="920a0-121"><a name="scenario-1">السيناريو 1: تكوين نهج دمج الشحنات الافتراضي</a></span><span class="sxs-lookup"><span data-stu-id="920a0-121"><a name="scenario-1"></a>Scenario 1: Configure default shipment consolidation policies</span></span>

<span data-ttu-id="920a0-122">يوجد حالتان يجب فيهما أن تقوم بتكوين عدد أدنى من النهج الافتراضية بعد تشغيل ميزة *نُهج دمج الشحنات*:</span><span class="sxs-lookup"><span data-stu-id="920a0-122">There are two situations where you must configure the minimum number of default policies after you turn on the *Shipment consolidation policies* feature:</span></span>

- <span data-ttu-id="920a0-123">أنت تقوم بترقية بيئة تحتوي بالفعل على البيانات.</span><span class="sxs-lookup"><span data-stu-id="920a0-123">You're upgrading an environment that already contains data.</span></span>
- <span data-ttu-id="920a0-124">أن تقوم بإعداد بيئة جديدة تمامًا.</span><span class="sxs-lookup"><span data-stu-id="920a0-124">You're setting up a completely new environment.</span></span>

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a><span data-ttu-id="920a0-125">ترقيه بيئة تم بالفعل تكوين المستودعات لها للدمج عبر الأوامر</span><span class="sxs-lookup"><span data-stu-id="920a0-125">Upgrade an environment where warehouses are already configured for cross-order consolidation</span></span>

<span data-ttu-id="920a0-126">عند بدء هذا الإجراء، يجب إيقاف تشغيل ميزة *نهج دمج الشحنات*، لمحاكاة بيئة تم فيها بالفعل استخدام ميزة الدمج الأساسي عبر الأوامر.</span><span class="sxs-lookup"><span data-stu-id="920a0-126">When you start this procedure, the *Shipment consolidation policies* feature should be turned off, to simulate an environment where the basic cross-order consolidation feature was already used.</span></span> <span data-ttu-id="920a0-127">ستستخدم بعد ذلك إدارة الميزات لتشغيل الميزة، لكي تتمكن من معرفة كيفية إعداد نُهج دمج الشحنات بعد الترقية.</span><span class="sxs-lookup"><span data-stu-id="920a0-127">You will then use feature management to turn on the feature, so that you can learn how to set up shipment consolidation policies after the upgrade.</span></span>

<span data-ttu-id="920a0-128">اتبع هذه الخطوات لإعداد نُهج دمج الشحنات الافتراضية في بيئة تم فيها بالفعل تكوين المستودعات للدمج عبر الأوامر.</span><span class="sxs-lookup"><span data-stu-id="920a0-128">Follow these steps to set up default shipment consolidation policies in an environment where warehouses have already been configured for cross-order consolidation.</span></span>

1. <span data-ttu-id="920a0-129">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-129">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="920a0-130">في القائمة، ابحث عن سجل المستودع المطلوب وافتحه (على سبيل المثال، المستودع *24* في بيانات العرض التوضيحي **USMF**).</span><span class="sxs-lookup"><span data-stu-id="920a0-130">In the list, find and open the desired warehouse record (for example, warehouse *24* in the **USMF** demo data).</span></span>
1. <span data-ttu-id="920a0-131">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="920a0-131">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="920a0-132">في علامة التبويب السريعة **المستودع**، قم بتعيين خيار **دمج الشحنات عند الإصدار إلى المستودع** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-132">On the **Warehouse** FastTab, set the **Consolidate shipment at release to warehouse** option to *Yes*.</span></span>
1. <span data-ttu-id="920a0-133">كرر الخطوات من 2 إلى 4 لكافة المستودعات الأخرى التي يكون الدمج مطلوبًا فيها.</span><span class="sxs-lookup"><span data-stu-id="920a0-133">Repeat steps 2 through 4 for all other warehouses where consolidation is required.</span></span>
1. <span data-ttu-id="920a0-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-134">Close the page.</span></span>
1. <span data-ttu-id="920a0-135">استخدم [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل ميزة *نُهج دمج الشحنات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-135">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the *Shipment consolidation policies* feature.</span></span> <span data-ttu-id="920a0-136">في مساحة عمل **إدارة الميزات**، يتم تسمية الميزة باسم *الشحنة المدمجة*.</span><span class="sxs-lookup"><span data-stu-id="920a0-136">In the **Feature management** workspace, the feature is named *Consolidate shipment*.</span></span>
1. <span data-ttu-id="920a0-137">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-137">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span> <span data-ttu-id="920a0-138">قد تضطر إلى تحديث المستعرض الخاص بك لرؤية عنصر قائمة **نُهج دمج الشحنات** الجديدة بعد تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="920a0-138">You might have to refresh your browser to see the new **Shipment consolidation policies** menu item after you turn on the feature.</span></span>
1. <span data-ttu-id="920a0-139">في جزء الإجراءات، حدد **إنشاء إعداد افتراضي** لإنشاء النُهج التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-139">On the Action Pane, select **Create default setup** to create the following policies:</span></span>

    - <span data-ttu-id="920a0-140">نهج **CrossOrder** لنوع نهج *أوامر المبيعات* (بشرط أن يكون لديك على الأقل مستودع واحد تم إعداده لاستخدام ميزة الدمج السابقة)</span><span class="sxs-lookup"><span data-stu-id="920a0-140">A **CrossOrder** policy for the *Sales orders* policy type (provided that you have at least one warehouse that is set up to use the earlier consolidation feature)</span></span>
    - <span data-ttu-id="920a0-141">نهج **افتراضي** لنوع نهج *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="920a0-141">A **Default** policy for the *Sales orders* policy type</span></span>
    - <span data-ttu-id="920a0-142">نهج **افتراضي** لنوع نهج *إصدار التحويل*</span><span class="sxs-lookup"><span data-stu-id="920a0-142">A **Default** policy for the *Transfer issue* policy type</span></span>
    - <span data-ttu-id="920a0-143">نهج **CrossOrder** لنوع نهج *إصدار التحويل* (بشرط أن يكون لديك على الأقل مستودع واحد تم إعداده لاستخدام ميزة الدمج السابقة)</span><span class="sxs-lookup"><span data-stu-id="920a0-143">A **CrossOrder** policy for the *Transfer issue* policy type (provided you have at least one warehouse that is set up to use the earlier consolidation feature)</span></span>

    > [!NOTE]
    > - <span data-ttu-id="920a0-144">يأخذ كل من نهجي **CrossOrder** في الاعتبار نفس مجموعة الحقول مثل المنطق السابق، باستثناء الحقل الخاص برقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="920a0-144">Both **CrossOrder** policies consider the same set of fields as the earlier logic, except for the field for the order number.</span></span> <span data-ttu-id="920a0-145">(يتم استخدام هذا الحقل لدمج البنود في الشحنات استنادا إلى عوامل مثل المستودع ووضع نقل التسليم والعنوان.)</span><span class="sxs-lookup"><span data-stu-id="920a0-145">(That field is used to consolidate lines into shipments, based on factors such as the warehouse, transportation mode of delivery, and address.)</span></span>
    > - <span data-ttu-id="920a0-146">يأخذ كل من نهجي **الافتراضي** في الاعتبار نفس مجموعة الحقول مثل المنطق السابق، مع تضمين الحقل الخاص برقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="920a0-146">Both **Default** policies consider the same set of fields as the earlier logic, including the field for the order number.</span></span> <span data-ttu-id="920a0-147">(يتم استخدام هذا الحقل لدمج البنود في الشحنات استنادا إلى عوامل مثل رقم الأمر والمستودع ووضع نقل التسليم والعنوان.)</span><span class="sxs-lookup"><span data-stu-id="920a0-147">(That field is used to consolidate lines into shipments, based on factors such as the order number, warehouse, transportation mode of delivery, and address.)</span></span>

1. <span data-ttu-id="920a0-148">حدد نهج **CrossOrder** لـ *أوامر المبيعات*، ثم في جزء الإجراءات، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="920a0-148">Select the **CrossOrder** policy for the *Sales orders* policy type, and then, on the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="920a0-149">في مربع الحوار محرر الاستعلام، لاحظ أين تم تعيين خيار **دمج الشحنة عند الإصدار إلى المستودع** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-149">In the query editor dialog box, notice that warehouses where the **Consolidate shipment at release to warehouse** option is set to *Yes* are listed.</span></span> <span data-ttu-id="920a0-150">بالتالي، يتم تضمينها في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="920a0-150">Therefore, they are included in the query.</span></span>

### <a name="create-default-policies-for-a-new-environment"></a><span data-ttu-id="920a0-151">إنشاء نُهج افتراضية لبيئة جديدة</span><span class="sxs-lookup"><span data-stu-id="920a0-151">Create default policies for a new environment</span></span>

<span data-ttu-id="920a0-152">اتبع هذه الخطوات لإعداد نُهج دمج الشحنات الافتراضية في بيئة جديدة تمامًا.</span><span class="sxs-lookup"><span data-stu-id="920a0-152">Follow these steps to set up default shipment consolidation policies in a brand-new environment.</span></span>

1. <span data-ttu-id="920a0-153">استخدم [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل ميزة *نُهج دمج الشحنات* إذا لم يكن قد تم تشغيلها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="920a0-153">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the *Shipment consolidation policies* feature, if you haven't already turned it on.</span></span> <span data-ttu-id="920a0-154">في مساحة عمل **إدارة الميزات**، يتم تسمية الميزة باسم *الشحنة المدمجة*.</span><span class="sxs-lookup"><span data-stu-id="920a0-154">In the **Feature management** workspace, the feature is named *Consolidate shipment*.</span></span>
1. <span data-ttu-id="920a0-155">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-155">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-156">في جزء الإجراءات، حدد **إنشاء إعداد افتراضي** لإنشاء النُهج التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-156">On the Action Pane, select **Create default setup** to create the following policies:</span></span>

    - <span data-ttu-id="920a0-157">نهج **افتراضي** لنوع نهج *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="920a0-157">A **Default** policy for the *Sales orders* policy type</span></span>
    - <span data-ttu-id="920a0-158">نهج **افتراضي** لنوع نهج *إصدار التحويل*</span><span class="sxs-lookup"><span data-stu-id="920a0-158">A **Default** policy for the *Transfer issue* policy type</span></span>

    > [!NOTE]
    > <span data-ttu-id="920a0-159">يأخذ كل من نهجي **الافتراضي** في الاعتبار نفس مجموعة الحقول مثل المنطق السابق، مع تضمين الحقل الخاص برقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="920a0-159">Both **Default** policies consider the same set of fields as the earlier logic, including the field for the order number.</span></span> <span data-ttu-id="920a0-160">(يتم استخدام هذا الحقل لدمج البنود في الشحنات استنادا إلى عوامل مثل رقم الأمر والمستودع ووضع نقل التسليم والعنوان.)</span><span class="sxs-lookup"><span data-stu-id="920a0-160">(That field is used to consolidate lines into shipments, based on factors such as the order number, warehouse, transportation mode of delivery, and address.)</span></span>

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a><span data-ttu-id="920a0-161">السيناريو 2: تكوين نهج دمج الشحنات المخصصة</span><span class="sxs-lookup"><span data-stu-id="920a0-161">Scenario 2: Configure custom shipment consolidation policies</span></span>

<span data-ttu-id="920a0-162">يوضح هذا السيناريو كيفية إعداد نُهج دمج الشحنات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="920a0-162">This scenario shows how to set up custom shipment consolidation policies.</span></span> <span data-ttu-id="920a0-163">يمكن للنهج المخصصة دعم متطلبات الأعمال المعقدة حيث تعتمد عملية دمج الشحنات على العديد من الشروط.</span><span class="sxs-lookup"><span data-stu-id="920a0-163">Custom policies can support complex business requirements where shipment consolidation depends on several conditions.</span></span> <span data-ttu-id="920a0-164">ويوجد مع كل مثال نهج سيرد لاحقا في هذا السيناريو وصفًا مختصرًا لحالة العمل.</span><span class="sxs-lookup"><span data-stu-id="920a0-164">For each example policy later in this scenario, a short description of the business case is included.</span></span> <span data-ttu-id="920a0-165">يجب إعداد هذه الأمثلة بشكل متسلسل يضمن تقييم الاستعلامات بشكل يشبه الهرم.</span><span class="sxs-lookup"><span data-stu-id="920a0-165">These example policies should be set up in a sequence that ensures a pyramid-like evaluation of the queries.</span></span> <span data-ttu-id="920a0-166">(بمعنى آخر، يجب تقييم النُهج التي تتضمن معظم الشروط على أنها صاحبة الأولوية الأعلى.)</span><span class="sxs-lookup"><span data-stu-id="920a0-166">(In other words, the policies that have the most conditions should be evaluated as having the highest priority.)</span></span>

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a><span data-ttu-id="920a0-167">تشغيل الميزة وتحضير البيانات الرئيسية لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="920a0-167">Turn on the feature and prepare master data for this scenario</span></span>

<span data-ttu-id="920a0-168">قبل أن تتمكن من التنقل عبر التمرينات في هذا السيناريو، يجب عليك تشغيل الميزة وإعداد البيانات الرئيسية المطلوبة لإجراء التصفية، كما هو موضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="920a0-168">Before you can go through the exercises in this scenario, you must turn on the feature and prepare the master data that is required to do the filtering, as described in the following subsections.</span></span> <span data-ttu-id="920a0-169">(يتم تطبيق هذه المتطلبات الأساسية أيضًا على السيناريوهات المدرجة في [أمثلة سيناريوهات لكيفية استخدام نُهج دمج الشحنات](#example-scenarios).)</span><span class="sxs-lookup"><span data-stu-id="920a0-169">(These prerequisites also apply to the scenarios listed in [Example scenarios of how to use shipment consolidation policies](#example-scenarios).)</span></span>

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a><span data-ttu-id="920a0-170">تشغيل الميزة وإنشاء النُهج الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="920a0-170">Turn on the feature and create the default policies</span></span>

<span data-ttu-id="920a0-171">استخدم إدارة الميزات لتشغيل الميزة، إذا لم تكن قد قمت بتشغيلها بالفعل، وقم بإنشاء نُهج الدمج الافتراضية الموضحة في [السيناريو 1](#scenario-1).</span><span class="sxs-lookup"><span data-stu-id="920a0-171">Use feature management to turn on the feature, if you haven't already turned it on, and create the default consolidation polices that are described in [scenario 1](#scenario-1).</span></span>

#### <a name="create-two-new-product-filter-codes"></a><span data-ttu-id="920a0-172">إنشاء ترميزين جديدين لتصفية المنتج</span><span class="sxs-lookup"><span data-stu-id="920a0-172">Create two new product filter codes</span></span>

1. <span data-ttu-id="920a0-173">انتقل إلى **إدارة المستودعات \> إعداد \> عوامل تصفية المنتج \> عوامل تصفية المنتج**، ثم أضف اثنين من عوامل تصفية المنتجات:</span><span class="sxs-lookup"><span data-stu-id="920a0-173">Go to **Warehouse management \> Setup \> Product filters \> Product filters**, and add two product filters:</span></span>

    - <span data-ttu-id="920a0-174">عامل تصفية المنتج 1:</span><span class="sxs-lookup"><span data-stu-id="920a0-174">Product filter 1:</span></span>

        - <span data-ttu-id="920a0-175">**ترميز عامل التصفية:** *قابل للاشتعال*</span><span class="sxs-lookup"><span data-stu-id="920a0-175">**Filter code:** *Flammable*</span></span>
        - <span data-ttu-id="920a0-176">**عنوان عامل التصفية:** *الرمز 4*</span><span class="sxs-lookup"><span data-stu-id="920a0-176">**Filter title:** *Code 4*</span></span>

    - <span data-ttu-id="920a0-177">عامل تصفية المنتج 2:</span><span class="sxs-lookup"><span data-stu-id="920a0-177">Product filter 2:</span></span>

        - <span data-ttu-id="920a0-178">**ترميز عام التصفية:** *متفجر*</span><span class="sxs-lookup"><span data-stu-id="920a0-178">**Filter code:** *Explosive*</span></span>
        - <span data-ttu-id="920a0-179">**عنوان عامل التصفية:** *الرمز 4*</span><span class="sxs-lookup"><span data-stu-id="920a0-179">**Filter title:** *Code 4*</span></span>

1. <span data-ttu-id="920a0-180">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-180">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="920a0-181">افتح المنتج الذي يحتوي على رقم الصنف *M9200*.</span><span class="sxs-lookup"><span data-stu-id="920a0-181">Open the product that has item number *M9200*.</span></span> <span data-ttu-id="920a0-182">(يجب تمكين المنتج الذي قمت بتحديده لعمليات \[WMS\] للمستودع المتقدم، وتم تمكين هذا المنتج مسبقًا لعمليات WMS في بيانات العرض التوضيحي **USMF**.)</span><span class="sxs-lookup"><span data-stu-id="920a0-182">(The product that you select must be enabled for advanced warehouse \[WMS\] processes, and this product is pre-enabled for WMS processes in the **USMF** demo data.)</span></span>
1. <span data-ttu-id="920a0-183">في علامة التبويب السريعة **المستودع**، قم بتعيين حقل **الرمز 4** إلى *قابل للاشتعال*.</span><span class="sxs-lookup"><span data-stu-id="920a0-183">On the **Warehouse** FastTab, set the **Code 4** field to *Flammable*.</span></span>
1. <span data-ttu-id="920a0-184">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-184">Close the page.</span></span>
1. <span data-ttu-id="920a0-185">افتح المنتج الذي يحتوي على رقم الصنف *M9201*.</span><span class="sxs-lookup"><span data-stu-id="920a0-185">Open the product that has item number *M9201*.</span></span> <span data-ttu-id="920a0-186">(تم تمكين هذا المنتج أيضًا بشكل مسبق لعمليات WMS في بيانات العرض التوضيحي **USMF**.)</span><span class="sxs-lookup"><span data-stu-id="920a0-186">(This product is also pre-enabled for WMS processes in the in the **USMF** demo data.)</span></span>
1. <span data-ttu-id="920a0-187">في علامة التبويب السريعة **المستودع**، قم بتعيين حقل **الرمز 4** إلى *متفجر*.</span><span class="sxs-lookup"><span data-stu-id="920a0-187">On the **Warehouse** FastTab, set the **Code 4** field to *Explosive*.</span></span>
1. <span data-ttu-id="920a0-188">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-188">Close the page.</span></span>

#### <a name="create-a-new-transportation-mode-of-delivery"></a><span data-ttu-id="920a0-189">قم بإنشاء وضع نقل جديد للتسليم.</span><span class="sxs-lookup"><span data-stu-id="920a0-189">Create a new transportation mode of delivery</span></span>

1. <span data-ttu-id="920a0-190">انتقل إلى **إدارة النقل \> الإعداد \> شركات النقل \> الوضع**.</span><span class="sxs-lookup"><span data-stu-id="920a0-190">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="920a0-191">قم بإنشاء وضع النقل الذي سيتم استخدامه في استعلامات الدمج، وقم بتسميته *Airways*.</span><span class="sxs-lookup"><span data-stu-id="920a0-191">Create a transportation mode that will be used in consolidation queries, and name it *Airways*.</span></span>
1. <span data-ttu-id="920a0-192">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل‬‬ \> شركات الشحن‬‬**.</span><span class="sxs-lookup"><span data-stu-id="920a0-192">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="920a0-193">قم بإنشاء شركة نقل تتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-193">Create a carrier that has the following settings:</span></span>

    - <span data-ttu-id="920a0-194">**شركه الشحن:** *Airways*</span><span class="sxs-lookup"><span data-stu-id="920a0-194">**Shipping carrier:** *Airways*</span></span>
    - <span data-ttu-id="920a0-195">**الاسم:** *Airways*</span><span class="sxs-lookup"><span data-stu-id="920a0-195">**Name:** *Airways*</span></span>
    - <span data-ttu-id="920a0-196">**الوضع:** *Airways*</span><span class="sxs-lookup"><span data-stu-id="920a0-196">**Mode:** *Airways*</span></span>

1. <span data-ttu-id="920a0-197">في علامة التبويب السريعة **الخدمات** لشركه النقل الجديدة، قم بإضافة صف يحتوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-197">On the **Services** FastTab for the new carrier, add a row that has the following settings:</span></span>

    - <span data-ttu-id="920a0-198">**خدمة شركة النقل:** *Air*</span><span class="sxs-lookup"><span data-stu-id="920a0-198">**Carrier service:** *Air*</span></span>
    - <span data-ttu-id="920a0-199">**وسيلة النقل:** *Air*</span><span class="sxs-lookup"><span data-stu-id="920a0-199">**Transportation method:** *Air*</span></span>

1. <span data-ttu-id="920a0-200">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="920a0-200">On the Action Pane, select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="920a0-201">عند حفظ شركة النقل الجديدة، يتم تعيين حقل **وضع التسليم** للصف الجديد في شبكة **الخدمات** تلقائيا إلى *Airwa-Air*.</span><span class="sxs-lookup"><span data-stu-id="920a0-201">When you save the new carrier, the **Mode of delivery** field for the new row in the **Services** grid is automatically set to *Airwa-Air*.</span></span> <span data-ttu-id="920a0-202">عند استخدام وضع التسليم *Airwa-Air* لأمر المبيعات، سيتم استخدام وضع النقل *Airways* للشحنات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="920a0-202">When you use the *Airwa-Air* mode of delivery for a sales order, the *Airways* transportation mode will be used for related shipments.</span></span>

#### <a name="create-an-order-pool"></a><span data-ttu-id="920a0-203">إنشاء وعاء أوامر</span><span class="sxs-lookup"><span data-stu-id="920a0-203">Create an order pool</span></span>

1. <span data-ttu-id="920a0-204">انتقل إلى **المبيعات والتسويق \> الإعداد \> أوامر المبيعات \> أوعية الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="920a0-204">Go to **Sales and marketing \> Setup \> Sales orders \> Order pools**.</span></span>
1. <span data-ttu-id="920a0-205">قم بإنشاء وعاء أوامر سيتم استخدامه مع استعلام الدمج.</span><span class="sxs-lookup"><span data-stu-id="920a0-205">Create an order pool that will be used for the consolidation query.</span></span> <span data-ttu-id="920a0-206">يجب أن يتضمن وعاء الأوامر هذا الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-206">This order pool should have the following settings:</span></span>

    - <span data-ttu-id="920a0-207">**الوعاء:** أدخل عددًا صحيحًا غير مستخدم بالفعل من قبل أي وعاء آخر.</span><span class="sxs-lookup"><span data-stu-id="920a0-207">**Pool:** Enter an integer that isn't already used by any other pool.</span></span>
    - <span data-ttu-id="920a0-208">**الاسم:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="920a0-208">**Name:** *ShipCons*</span></span>

1. <span data-ttu-id="920a0-209">انتقل إلى **المبيعات والتسويق \> العملاء \> جميع العملاء‬**.</span><span class="sxs-lookup"><span data-stu-id="920a0-209">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="920a0-210">افتح العميل الذي يتضمن رقم الحساب *US-003*.</span><span class="sxs-lookup"><span data-stu-id="920a0-210">Open the customer that has account number *US-003*.</span></span>
1. <span data-ttu-id="920a0-211">في علامة التبويب السريعة **‬‏‫إعدادات أوامر المبيعات الافتراضية‬‏‫**، قم بتعيين حقل **وعاء أوامر المبيعات** إلى وعاء الأوامر الذي قمت بإنشائه لتوك.</span><span class="sxs-lookup"><span data-stu-id="920a0-211">On the **Sales order defaults** FastTab, set the **Sales order pool** field to the order pool that you just created.</span></span>
1. <span data-ttu-id="920a0-212">قم بإغلاق الصفحة، ثم قم بتكرار الخطوتين 4 و 5 للعميل الذي له رقم حساب *004*.</span><span class="sxs-lookup"><span data-stu-id="920a0-212">Close the page, and then repeat the steps 4 and 5 for the customer that has account number *US-004*.</span></span>

### <a name="create-example-policy-1"></a><span data-ttu-id="920a0-213">إنشاء مثال للنهج 1</span><span class="sxs-lookup"><span data-stu-id="920a0-213">Create example policy 1</span></span>

<span data-ttu-id="920a0-214">في هذا المثال، ستقوم بإنشاء نهج *العميل + الوضع* الذي يمكن استخدامه لحالة الأعمال التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-214">In this example, you will create a *Customer+Mode* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="920a0-215">سيقوم النهج بالاستعلام عن حساب عميل محدد (*US-001*) ووضع تسليم محدد (*Airwa-Air*).</span><span class="sxs-lookup"><span data-stu-id="920a0-215">The policy will query for a specific customer account (*US-001*) and a specific mode of delivery (*Airwa-Air*).</span></span>
- <span data-ttu-id="920a0-216">يتم إيقاف تشغيل الدمج مع الشحنات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-216">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="920a0-217">ويتم إجراء الدمج حسب معرف الأمر.</span><span class="sxs-lookup"><span data-stu-id="920a0-217">Consolidation is done per order ID.</span></span> <span data-ttu-id="920a0-218">(بمعنى آخر، ستكون هناك شحنات منفصلة لكل أمر، ومستودع، وهكذا.)</span><span class="sxs-lookup"><span data-stu-id="920a0-218">(In other words, there will be separate shipments per order, warehouse, and so on.)</span></span>

<span data-ttu-id="920a0-219">اتبع الخطوات التالية لإنشاء نهج دمج الشحنات لحالة الأعمال هذه.</span><span class="sxs-lookup"><span data-stu-id="920a0-219">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="920a0-220">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-220">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-221">قم بتعيين حقل **نوع النهج** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-221">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="920a0-222">في جزء الإجراءات، حدد **جديد** لإنشاء نهج بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-222">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="920a0-223">**اسم النهج:** *CustomerMode*</span><span class="sxs-lookup"><span data-stu-id="920a0-223">**Policy name:** *CustomerMode*</span></span>
    - <span data-ttu-id="920a0-224">**وصف النهج:** *حساب العميل ووضع التسليم*</span><span class="sxs-lookup"><span data-stu-id="920a0-224">**Policy description:** *Customer account and mode of delivery*</span></span>

1. <span data-ttu-id="920a0-225">اترك خيار **دمج مع الشحنات المفتوحة** معينًا إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="920a0-225">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="920a0-226">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="920a0-226">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="920a0-227">في علامة التبويب السريعة **حقول الدمج**، في قائمة **الحقول المتبقية**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل** إلى *وضع التسليم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-227">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="920a0-228">حدد زر **إضافة** ![سهم لليمين](media/forward-button.png) لنقل الحقل إلى قائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-228">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="920a0-229">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="920a0-229">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="920a0-230">في مربع الحوار محرر الاستعلام، ضمن علامة التبويب **النطاق**، في الشبكة، ابحث عن الصف الذي تم فيه تعيين حقل **الحقل** إلى *حساب العميل*، وقم بتعيين حقل **المعايير** لهذا الصف إلى *US-001*.</span><span class="sxs-lookup"><span data-stu-id="920a0-230">In the query editor dialog box, on the **Range** tab, in the grid, find the row where the **Field** field is set to *Customer account*, and set the **Criteria** field for that row to *US-001*.</span></span>
1. <span data-ttu-id="920a0-231">حدد **إضافة** لإضافة صف يتضمن الإعدادات التالية للشبكة:</span><span class="sxs-lookup"><span data-stu-id="920a0-231">Select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="920a0-232">**الجدول:** *بنود الأمر*</span><span class="sxs-lookup"><span data-stu-id="920a0-232">**Table:** *Order lines*</span></span>
    - <span data-ttu-id="920a0-233">**الجدول المشتق:** *بنود الأمر*</span><span class="sxs-lookup"><span data-stu-id="920a0-233">**Derived table:** *Order lines*</span></span>
    - <span data-ttu-id="920a0-234">**الحقل:** *وضع التسليم*</span><span class="sxs-lookup"><span data-stu-id="920a0-234">**Field:** *Mode of delivery*</span></span>
    - <span data-ttu-id="920a0-235">**المعايير:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="920a0-235">**Criteria:** *Airwa-Air*</span></span>

1. <span data-ttu-id="920a0-236">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="920a0-236">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="920a0-237">في حالة الأعمال هذه، لن يتم دمج سطور الأوامر الخاصة بالعميل *US-001* التي تستخدم وضع التسليم *Airwa-Air* عبر الأوامر.</span><span class="sxs-lookup"><span data-stu-id="920a0-237">For this business case, order lines for customer *US-001* that use the *Airwa-Air* mode of delivery won't be consolidated across orders.</span></span> <span data-ttu-id="920a0-238">يتم تخصيص هذا النهج لاستخدامه أولا في التسلسل، في الحالات التي يتم فيها دمج الشحنات لكافة أوضاع التسليم الأخرى لهذا العميل.</span><span class="sxs-lookup"><span data-stu-id="920a0-238">This policy is intended to be used first in a sequence, in cases where shipments for all other modes of delivery are consolidated for this customer.</span></span>

### <a name="create-example-policy-2"></a><span data-ttu-id="920a0-239">إنشاء مثال للنهج 2</span><span class="sxs-lookup"><span data-stu-id="920a0-239">Create example policy 2</span></span>

<span data-ttu-id="920a0-240">في هذا المثال، ستقوم بإنشاء نهج *البضائع الخطرة* الذي يمكن استخدامه لحالة الأعمال التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-240">In this example, you will create a *Hazardous goods* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="920a0-241">سيقوم النهج بالاستعلام عن رمز تصفية محدد (*خطر*) ووضع تسليم محدد (*Airwa-Air*).</span><span class="sxs-lookup"><span data-stu-id="920a0-241">The policy will query for a specific filter code (*hazardous*) and a specific mode of delivery (*Airwa-Air*).</span></span>
- <span data-ttu-id="920a0-242">يتم تشغيل الدمج مع الشحنات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-242">Consolidation with open shipments is turned on.</span></span>
- <span data-ttu-id="920a0-243">ويتم إجراء الدمج عبر الأوامر المشتركة.</span><span class="sxs-lookup"><span data-stu-id="920a0-243">Consolidation is done across orders.</span></span> <span data-ttu-id="920a0-244">(بمعنى آخر، ستكون هناك شحنات منفصلة لكل حساب ومستودع وهكذا، ولكن فقط داخل مجموعة الأصناف المحددة في الاستعلام.)</span><span class="sxs-lookup"><span data-stu-id="920a0-244">(In other words, there will be separate shipments per account, warehouse, and so on, but only within the item group that is specified in the query.)</span></span>

<span data-ttu-id="920a0-245">اتبع الخطوات التالية لإنشاء نهج دمج الشحنات لحالة الأعمال هذه.</span><span class="sxs-lookup"><span data-stu-id="920a0-245">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="920a0-246">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-246">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-247">قم بتعيين حقل **نوع النهج** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-247">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="920a0-248">في جزء الإجراءات، حدد **جديد** لإنشاء نهج بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-248">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="920a0-249">**اسم النهج:** *نوع الصنف*</span><span class="sxs-lookup"><span data-stu-id="920a0-249">**Policy name:** *Item type*</span></span>
    - <span data-ttu-id="920a0-250">**وصف النهج:** *دمج نفس نوع الصنف عبر الأوامر*</span><span class="sxs-lookup"><span data-stu-id="920a0-250">**Policy description:** *Consolidate the same type of item across orders*</span></span>

1. <span data-ttu-id="920a0-251">قم بتعيين خيار **دمج مع الشحنات المفتوحة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-251">Set the **Consolidate with open shipments** option to *Yes*.</span></span>
1. <span data-ttu-id="920a0-252">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="920a0-252">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="920a0-253">في علامة التبويب السريعة **حقول الدمج**، في قائمة **الحقول المتبقية**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل** إلى *وضع التسليم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-253">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="920a0-254">حدد زر **إضافة** ![سهم لليمين](media/forward-button.png) لنقل الحقل إلى قائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-254">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="920a0-255">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="920a0-255">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="920a0-256">في مربع الحوار محرر الاستعلام، في علامة تبويب **عمليات الانضمام**، قم بتوسيع وتحديد **الجداول \> تحميل التفاصيل** في الشجرة.</span><span class="sxs-lookup"><span data-stu-id="920a0-256">In the query editor dialog box, on the **Joins** tab, expand and select **Tables \> Load details** in the tree.</span></span>
1. <span data-ttu-id="920a0-257">حدد **إضافة انضمام جدول**.</span><span class="sxs-lookup"><span data-stu-id="920a0-257">Select **Add table join**.</span></span>
1. <span data-ttu-id="920a0-258">في شبكة العلاقات التي تظهر، ابحث عن وحدد الصف الذي تم فيه تعيين حقل **العلاقة** إلى *رقم صنف المستودع (رقم الصنف)*، ثم حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="920a0-258">In the grid of relations that appears, find and select the row where the **Relation** field is set to *Warehouse item number (Item number)*, and then select **Select**.</span></span> 
1. <span data-ttu-id="920a0-259">في علامة تبويب **النطاق**، حدد **إضافة** لإضافة صف يتضمن الإعدادات التالية للشبكة:</span><span class="sxs-lookup"><span data-stu-id="920a0-259">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="920a0-260">**الجدول:** *رقم صنف المستودع*</span><span class="sxs-lookup"><span data-stu-id="920a0-260">**Table:** *Warehouse item number*</span></span>
    - <span data-ttu-id="920a0-261">**الجدول المشتق:** *رقم صنف المستودع*</span><span class="sxs-lookup"><span data-stu-id="920a0-261">**Derived table:** *Warehouse item number*</span></span>
    - <span data-ttu-id="920a0-262">**الحقل:** *الرمز 4*</span><span class="sxs-lookup"><span data-stu-id="920a0-262">**Field:** *Code 4*</span></span>
    - <span data-ttu-id="920a0-263">**المعايير:** *قابل للاشتعال*</span><span class="sxs-lookup"><span data-stu-id="920a0-263">**Criteria:** *Flammable*</span></span>

1. <span data-ttu-id="920a0-264">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="920a0-264">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="920a0-265">في حالة الأعمال هذه، سيتم دمج كافة بنود الأوامر التي تحتوي الأصناف فيها على رمز تصفية محدد (أي، رمز التصفية الذي تم تعيين حقل **الرمز 4** فيه إلى *قابل للاشتعال*) مع الأصناف الأخرى بنفس نوع عبر الأوامر.</span><span class="sxs-lookup"><span data-stu-id="920a0-265">For this business case, all order lines where items have a specific filter code (that is, the filter code where the **Code 4** field is set to *Flammable*) will be consolidated with other items of the same type across orders.</span></span> <span data-ttu-id="920a0-266">إذا كان هناك شحنة مفتوحة لنفس الحساب والمستودع ومجموعة الأصناف، فسيتم إلحاق البنود الجديدة بها.</span><span class="sxs-lookup"><span data-stu-id="920a0-266">If there is an open shipment for the same account, warehouse, and group of items, the new lines will be attached to it.</span></span>

### <a name="create-example-policy-3"></a><span data-ttu-id="920a0-267">إنشاء مثال للنهج 3</span><span class="sxs-lookup"><span data-stu-id="920a0-267">Create example policy 3</span></span>

<span data-ttu-id="920a0-268">في هذا المثال، ستقوم بإنشاء نهج *متطلبات العملاء* الذي يمكن استخدامه لحالة الأعمال التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-268">In this example, you will create a *Customers' requirements* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="920a0-269">سيقوم النهج بالاستعلام عن حساب عميل محدد.</span><span class="sxs-lookup"><span data-stu-id="920a0-269">The policy will query for a specific customer account.</span></span>
- <span data-ttu-id="920a0-270">يتم تشغيل الدمج مع الشحنات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-270">Consolidation with open shipments is turned on.</span></span>
- <span data-ttu-id="920a0-271">ويتم إجراء الدمج عبر الأوامر ولكنه يستند إلى طلبات العميل.</span><span class="sxs-lookup"><span data-stu-id="920a0-271">Consolidation is done across orders but is based on customer requisitions.</span></span> <span data-ttu-id="920a0-272">(بمعنى آخر، سيتم تجميع الأوامر المتعددة إلى شحنات، استنادًا إلى نفس رقم طلب العميل والمستودع.)</span><span class="sxs-lookup"><span data-stu-id="920a0-272">(In other words, multiple orders will be grouped into shipments, based on the same customer requisition number and warehouse.)</span></span>

<span data-ttu-id="920a0-273">اتبع الخطوات التالية لإنشاء نهج دمج الشحنات لحالة الأعمال هذه.</span><span class="sxs-lookup"><span data-stu-id="920a0-273">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="920a0-274">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-274">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-275">قم بتعيين حقل **نوع النهج** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-275">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="920a0-276">في جزء الإجراءات، حدد **جديد** لإنشاء نهج بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-276">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="920a0-277">**اسم النهج:** *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="920a0-277">**Policy name:** *CustomerOrderNo*</span></span>
    - <span data-ttu-id="920a0-278">**وصف النهج:** *دمج البنود استنادا إلى أمر شراء العميل*</span><span class="sxs-lookup"><span data-stu-id="920a0-278">**Policy description:** *Consolidate lines based on customer PO*</span></span>

1. <span data-ttu-id="920a0-279">قم بتعيين خيار **دمج مع الشحنات المفتوحة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-279">Set the **Consolidate with open shipments** option to *Yes*.</span></span>
1. <span data-ttu-id="920a0-280">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="920a0-280">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="920a0-281">في علامة التبويب السريعة **حقول الدمج**، في قائمة **الحقول المتبقية**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل** إلى *طلب العميل*.</span><span class="sxs-lookup"><span data-stu-id="920a0-281">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Customer requisition*.</span></span>
1. <span data-ttu-id="920a0-282">حدد زر **إضافة** ![سهم لليمين](media/forward-button.png) لنقل الحقل إلى قائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-282">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="920a0-283">في قائمة **الحقول المتبقية**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل** إلى *وضع التسليم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-283">In the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="920a0-284">حدد زر **إضافة** ![سهم لليمين](media/forward-button.png) لنقل الحقل إلى قائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-284">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="920a0-285">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="920a0-285">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="920a0-286">في مربع الحوار محرر الاستعلام، ضمن علامة التبويب **النطاق**، ابحث عن الصف الذي تم فيه تعيين حقل **الحقل** إلى *حساب العميل*، وقم بتعيين حقل **المعايير** لهذا الصف إلى *US-001*.</span><span class="sxs-lookup"><span data-stu-id="920a0-286">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Customer account*, and set the **Criteria** field for that row to *US-001*.</span></span>
1. <span data-ttu-id="920a0-287">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="920a0-287">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="920a0-288">في حالة الأعمال هذه، سيتم دمج كافة بنود الأوامر التي يكون لأوامر المبيعات فيها نفس رقم طلب العميل في شحنة واحدة، بغض النظر عن رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="920a0-288">For this business case, all order lines where sales orders have the same customer requisition number will be consolidated into one shipment, regardless of the sales order number.</span></span> <span data-ttu-id="920a0-289">(يتم استخدام رقم طلب العميل كرقم \[PO\] لأمر شراء العميل.) إذا كان هناك شحنة مفتوحة لنفس الحساب والمستودع وطلب العميل، فسيتم إلحاق البنود الجديدة بها.</span><span class="sxs-lookup"><span data-stu-id="920a0-289">(The customer requisition number is used as the customer's purchase order \[PO\] number.) If there is an open shipment for the same account, warehouse, and customer requisition, the new lines will be attached to it.</span></span> <span data-ttu-id="920a0-290">يمكن استخدام هذا النهج إذا كان العميل يقوم بإرسال بنود أوامر إضافية لها نفس رقم أمر الشراء عدة مرات خلال يوم معين ويرغب في تجميع كافة البنود في شحنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="920a0-290">This policy can be used if the customer sends additional order lines that have the same PO number several times during a day and wants all the lines to be grouped into one shipment.</span></span> <span data-ttu-id="920a0-291">(بمعنى آخر، سيكون هناك بوليصة شحن واحدة وإيصال تعبئة واحد.)</span><span class="sxs-lookup"><span data-stu-id="920a0-291">(In other words, there will be one bill of lading and one packing slip.)</span></span>

### <a name="create-example-policy-4"></a><span data-ttu-id="920a0-292">إنشاء مثال للنهج 4</span><span class="sxs-lookup"><span data-stu-id="920a0-292">Create example policy 4</span></span>

<span data-ttu-id="920a0-293">في هذا المثال، ستقوم بإنشاء نهج *سماح العملاء بالدمج* الذي يمكن استخدامه لحالة الأعمال التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-293">In this example, you will create a *Customers allowing consolidation* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="920a0-294">سيقوم النهج بالاستعلام عن وعاء أوامر محدد لتحديد العملاء الذين يقبلون الشحنات المدمجة.</span><span class="sxs-lookup"><span data-stu-id="920a0-294">The policy will query for a specific order pool to identify customers who accept consolidated shipments.</span></span>
- <span data-ttu-id="920a0-295">يتم إيقاف تشغيل الدمج مع الشحنات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-295">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="920a0-296">تتم عملية الدمج عبر الأوامر باستخدام الحقول المحددة بواسطة نهج CrossOrder الافتراضي (لاستنساخ خانة اختيار **دمج الشحنات عند الإصدار إلى المستودع** السابقة).</span><span class="sxs-lookup"><span data-stu-id="920a0-296">Consolidation is done across orders using the fields selected by default CrossOrder policy (to replicate the previous **Consolidate shipment at release to warehouse** check box).</span></span>

- <span data-ttu-id="920a0-297">يمكنك تجاوز القاعدة في أمر المبيعات من خلال تحديد وعاء أوامر مختلف.</span><span class="sxs-lookup"><span data-stu-id="920a0-297">You can override the rule on a sales order by selecting a different order pool.</span></span>

<span data-ttu-id="920a0-298">اتبع الخطوات التالية لإنشاء نهج دمج الشحنات لحالة الأعمال هذه.</span><span class="sxs-lookup"><span data-stu-id="920a0-298">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="920a0-299">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-299">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-300">قم بتعيين حقل **نوع النهج** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-300">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="920a0-301">في جزء الإجراءات، حدد **جديد** لإنشاء نهج بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-301">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="920a0-302">**اسم النهج:** *وعاء الأوامر*</span><span class="sxs-lookup"><span data-stu-id="920a0-302">**Policy name:** *Order pool*</span></span>
    - <span data-ttu-id="920a0-303">**وصف النهج:** *دمج عبر الأوامر استنادًا إلى وعاء الأوامر*</span><span class="sxs-lookup"><span data-stu-id="920a0-303">**Policy description:** *Consolidate across orders based on order pool*</span></span>

1. <span data-ttu-id="920a0-304">اترك خيار **دمج مع الشحنات المفتوحة** معينًا إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="920a0-304">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="920a0-305">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="920a0-305">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="920a0-306">في علامة التبويب السريعة **حقول الدمج**، في قائمة **الحقول المتبقية**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل** إلى *وضع التسليم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-306">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="920a0-307">حدد زر **إضافة** ![سهم لليمين](media/forward-button.png) لنقل الحقل إلى قائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-307">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="920a0-308">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="920a0-308">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="920a0-309">في مربع حوار محرر الاستعلام، في علامة تبويب **النطاق**، حدد **إضافة** لإضافة صف يتضمن الإعدادات التالية للشبكة:</span><span class="sxs-lookup"><span data-stu-id="920a0-309">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="920a0-310">**الجدول:** *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="920a0-310">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="920a0-311">**الجدول المشتق:** *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="920a0-311">**Derived table:** *Sales orders*</span></span>
    - <span data-ttu-id="920a0-312">**الحقل:** *الوعاء*</span><span class="sxs-lookup"><span data-stu-id="920a0-312">**Field:** *Pool*</span></span>
    - <span data-ttu-id="920a0-313">**المعايير:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="920a0-313">**Criteria:** *ShipCons*</span></span>

1. <span data-ttu-id="920a0-314">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="920a0-314">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="920a0-315">في حالة الأعمال هذه، سيتم دمج كافة بنود الأوامر التي تنتمي فيها أوامر المبيعات إلى نفس وعاء الأوامر في شحنة واحدة عبر أوامر المبيعات لنفس الحساب والمستودع ووضع النقل الخاص بالتسليم.</span><span class="sxs-lookup"><span data-stu-id="920a0-315">For this business case, all order lines where sales orders belong to the same order pool will be consolidated into one shipment across sales orders for the same account, warehouse, and transportation mode of delivery.</span></span> <span data-ttu-id="920a0-316">وبدلا من وعاء الأوامر، يمكنك استخدام أي حقل آخر لتمييز مجموعة من العملاء واستخدام رأس أمر المبيعات بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="920a0-316">Instead of the order pool, you can use any other field to distinguish a group of customers and use the sales order header by default.</span></span> <span data-ttu-id="920a0-317">يمكنك استخدام هذا الأسلوب إذا كان العميل، وليس المستودع، يقوم بتوجيه الحاجة إلى الدمج.</span><span class="sxs-lookup"><span data-stu-id="920a0-317">You can use this approach if the customer, not the warehouse, is driving the need for consolidation.</span></span> <span data-ttu-id="920a0-318">(في منطق الدمج السابق، ساهم المستودع في توجيه الحاجة إلى الدمج.)</span><span class="sxs-lookup"><span data-stu-id="920a0-318">(In the earlier consolidation logic, the warehouse drove the need for consolidation.)</span></span>

### <a name="create-example-policy-5"></a><span data-ttu-id="920a0-319">إنشاء مثال للنهج 5</span><span class="sxs-lookup"><span data-stu-id="920a0-319">Create example policy 5</span></span>

<span data-ttu-id="920a0-320">في هذا المثال، ستقوم بإنشاء نهج *سماح المستودعات بالدمج* الذي يمكن استخدامه لحالة الأعمال التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-320">In this example, you will create a *Warehouses allowing consolidation* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="920a0-321">سيقوم النهج بالاستعلام عن وعاء أوامر محدد لتحديد المستودعات التي يمكنها دمج الشحنات.</span><span class="sxs-lookup"><span data-stu-id="920a0-321">The policy will query for a specific order pool to identify warehouses that can consolidate shipments.</span></span>
- <span data-ttu-id="920a0-322">يتم إيقاف تشغيل الدمج مع الشحنات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="920a0-322">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="920a0-323">تتم عملية الدمج عبر الأوامر باستخدام الحقول المحددة بواسطة نهج CrossOrder الافتراضي (لاستنساخ خانة اختيار **دمج الشحنات عند الإصدار إلى المستودع** السابقة).</span><span class="sxs-lookup"><span data-stu-id="920a0-323">Consolidation is done across orders using the fields selected by default CrossOrder policy (to replicate the previous **Consolidate shipment at release to warehouse** check box).</span></span>

<span data-ttu-id="920a0-324">عادة، يمكن معالجة حالة الأعمال هذه باستخدام النُهج الافتراضية التي قمت بإنشائها في [السيناريو 1](#scenario-1).</span><span class="sxs-lookup"><span data-stu-id="920a0-324">Typically, this business case can be addressed by using the default policies that you created in [scenario 1](#scenario-1).</span></span> <span data-ttu-id="920a0-325">ومع ذلك، يمكنك أيضًا إنشاء سياسات مشابهة يدويًا باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="920a0-325">However, you can also manually create similar policies by following these steps.</span></span>

1. <span data-ttu-id="920a0-326">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-326">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-327">قم بتعيين حقل **نوع النهج** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-327">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="920a0-328">في جزء الإجراءات، حدد **جديد** لإنشاء نهج بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="920a0-328">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="920a0-329">**اسم النهج:** *عبر الأوامر*</span><span class="sxs-lookup"><span data-stu-id="920a0-329">**Policy name:** *Cross-order*</span></span>
    - <span data-ttu-id="920a0-330">**وصف النهج:** *دمج عبر الأوامر لمستودعات محددة*</span><span class="sxs-lookup"><span data-stu-id="920a0-330">**Policy description:** *Cross-order consolidation for specific warehouses*</span></span>

1. <span data-ttu-id="920a0-331">اترك خيار **دمج مع الشحنات المفتوحة** معينًا إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="920a0-331">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="920a0-332">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="920a0-332">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="920a0-333">في علامة التبويب السريعة **حقول الدمج**، في حقل **الحقول المتبقية**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل** إلى *وضع التسليم*.</span><span class="sxs-lookup"><span data-stu-id="920a0-333">On the **Consolidation fields** FastTab, in the **Remaining fields** field, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="920a0-334">حدد زر **إضافة** ![سهم لليمين](media/forward-button.png) لنقل الحقل إلى قائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="920a0-334">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="920a0-335">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="920a0-335">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="920a0-336">في مربع الحوار محرر الاستعلام، ضمن علامة التبويب **النطاق**، ابحث عن الصف الذي تم فيه تعيين حقل **الحقل** إلى *المستودع*، وقم بتعيين حقل **المعايير** لهذا الصف إلى *61, 63*.</span><span class="sxs-lookup"><span data-stu-id="920a0-336">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Warehouse*, and set the **Criteria** field for that row to *61, 63*.</span></span>
1. <span data-ttu-id="920a0-337">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="920a0-337">Select **OK** to close the dialog box.</span></span>

### <a name="set-the-order"></a><span data-ttu-id="920a0-338">تعيين الأمر</span><span class="sxs-lookup"><span data-stu-id="920a0-338">Set the order</span></span>

<span data-ttu-id="920a0-339">والآن بعد إنشاء كافة النُهج، يجب عليك إنشاء الأمر الذي سيتم تطبيقها فيه.</span><span class="sxs-lookup"><span data-stu-id="920a0-339">Now that you've created all your policies, you must establish the order that they will be applied in.</span></span> <span data-ttu-id="920a0-340">لاستخدام أسلوب يشبه الهرم، بحيث يتم تقييم النهج التي تتضمن معظم الشروط باعتبارها صاحبة أعلى أولوية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="920a0-340">To use a pyramid-like approach, where the policies that have the most conditions are evaluated as having the highest priority, follow these steps.</span></span>

1. <span data-ttu-id="920a0-341">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="920a0-341">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="920a0-342">قم بتعيين حقل **نوع النهج** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="920a0-342">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="920a0-343">حدد كل نهج مسرود في العمود الأيمن، ثم استخدم الزرين **تحريك لأعلى** و **تحريك لأسفل** في جزء الإجراءات لترتيب النهج بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="920a0-343">Select each policy that is listed in the left column, and then use the **Move up** and **Move down** buttons on the Action Pane to arrange the policies in the following order:</span></span>

    1. <span data-ttu-id="920a0-344">CustomerMode</span><span class="sxs-lookup"><span data-stu-id="920a0-344">CustomerMode</span></span>
    1. <span data-ttu-id="920a0-345">نوع الصنف</span><span class="sxs-lookup"><span data-stu-id="920a0-345">Item type</span></span>
    1. <span data-ttu-id="920a0-346">CustomerOrderNo</span><span class="sxs-lookup"><span data-stu-id="920a0-346">CustomerOrderNo</span></span>
    1. <span data-ttu-id="920a0-347">وعاء الأوامر</span><span class="sxs-lookup"><span data-stu-id="920a0-347">Order pool</span></span>
    1. <span data-ttu-id="920a0-348">عبر الأوامر</span><span class="sxs-lookup"><span data-stu-id="920a0-348">Cross-order</span></span>
    1. <span data-ttu-id="920a0-349">الإعداد الافتراضي</span><span class="sxs-lookup"><span data-stu-id="920a0-349">Default</span></span>

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a><span data-ttu-id="920a0-350">سيناريوهات أمثلة لكيفية استخدام نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="920a0-350">Example scenarios of how to use shipment consolidation policies</span></span>

<span data-ttu-id="920a0-351">توضح السيناريوهات التالية كيفية استخدام نُهج دمج الشحنات التي قمت بإنشائها أثناء قراءة هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="920a0-351">The following scenarios illustrate how you could use the shipment consolidation policies that you created while reading this topic.</span></span> <span data-ttu-id="920a0-352">يتناول معك كل سيناريو عملية دمج الشحنات التي تستخدم نُهج دمج الشحنات أثناء الإصدار التلقائي واليدوي إلى المستودع:</span><span class="sxs-lookup"><span data-stu-id="920a0-352">Each scenario walks you through a shipment consolidation process that uses shipment consolidation policies during automated or manual release to the warehouse:</span></span>

- <span data-ttu-id="920a0-353">السيناريو 1: [دمج الشحنات عند إصدارها إلى المستودع باستخدام الإصدار التلقائي لأوامر المبيعات](../warehousing/consolidate-shipments-automatic.md)</span><span class="sxs-lookup"><span data-stu-id="920a0-353">Scenario 1: [Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders](../warehousing/consolidate-shipments-automatic.md)</span></span>
- <span data-ttu-id="920a0-354">السيناريو 2: [دمج الشحنات عند تجاوز نهج دمج الشحنات من صفحة الإصدار إلى المستودع](../warehousing/consolidate-shipments-release-to-warehouse-override.md)</span><span class="sxs-lookup"><span data-stu-id="920a0-354">Scenario 2: [Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page](../warehousing/consolidate-shipments-release-to-warehouse-override.md)</span></span>
- <span data-ttu-id="920a0-355">السيناريو 3: [دمج الشحنات باستخدام الإصدار إلى المستودع من منضدة عمل تخطيط الحمل](../warehousing/consolidate-shipments-load-planning-workbench.md)</span><span class="sxs-lookup"><span data-stu-id="920a0-355">Scenario 3: [Consolidate shipments by using Release to warehouse from the load planning workbench](../warehousing/consolidate-shipments-load-planning-workbench.md)</span></span>
- <span data-ttu-id="920a0-356">السيناريو 4: [دمج الشحنات باستخدام منضدة عمل دمج الشحنات](../warehousing/consolidate-shipments-manual-workbench.md)</span><span class="sxs-lookup"><span data-stu-id="920a0-356">Scenario 4: [Consolidate shipments by using the shipment consolidation workbench](../warehousing/consolidate-shipments-manual-workbench.md)</span></span>
- <span data-ttu-id="920a0-357">السيناريو 5: [دمج الشحنات يدويًا باستخدام صفحة دمج الشحنات](../warehousing/consolidate-shipments-manual-form.md)</span><span class="sxs-lookup"><span data-stu-id="920a0-357">Scenario 5: [Consolidate shipments manually by using the Consolidate shipments page](../warehousing/consolidate-shipments-manual-form.md)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="920a0-358">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="920a0-358">Additional resources</span></span>

- [<span data-ttu-id="920a0-359">سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="920a0-359">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
