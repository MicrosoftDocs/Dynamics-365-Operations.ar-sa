---
title: دمج الشحنات باستخدام منضدة عمل دمج الشحنات
description: يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع ثم دمجها إلى شحنات لاحقًا باستخدام منضدة عمل دمج الشحنات.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b1a2c9506b4444fc98a9e4f0389cbd69db4ce052
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383705"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="e82c0-103">دمج الشحنات باستخدام منضدة عمل دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="e82c0-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e82c0-104">يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع ثم دمجها إلى شحنات لاحقًا باستخدام منضدة عمل دمج الشحنات.</span><span class="sxs-lookup"><span data-stu-id="e82c0-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="e82c0-105">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="e82c0-105">Make demo data available</span></span>

<span data-ttu-id="e82c0-106">يشير السيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e82c0-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e82c0-107">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF**قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="e82c0-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="e82c0-108">إعداد نُهج دمج الشحنات وعوامل تصفيه المنتجات</span><span class="sxs-lookup"><span data-stu-id="e82c0-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="e82c0-109">يفترض السيناريو الموضح هنا أنك قمت بالفعل بتشغيل الميزة، ونفذت التمرينات في [تكوين نهج دمج الشحنات](configure-shipment-consolidation-policies.md)، وإنشاء النهج والسجلات الأخرى التي تم وصفها هناك.</span><span class="sxs-lookup"><span data-stu-id="e82c0-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="e82c0-110">تأكد من تنفيذ تلك التمرينات قبل المتابعة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e82c0-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="e82c0-111">تشغيل ميزة دمج الشحنات اليدوي</span><span class="sxs-lookup"><span data-stu-id="e82c0-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="e82c0-112">قبل أن تتمكن من استخدام ميزة *دمج الشحنات اليدوي*، يجب تشغيلها في النظام لديك.</span><span class="sxs-lookup"><span data-stu-id="e82c0-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="e82c0-113">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="e82c0-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e82c0-114">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e82c0-115">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="e82c0-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e82c0-116">**اسم الميزة:** *دمج الشحنات اليدوي*</span><span class="sxs-lookup"><span data-stu-id="e82c0-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="e82c0-117">كما ذكر في [تكوين نُهج دمج الشحنات](configure-shipment-consolidation-policies.md)، يجب عليك أيضا تشغيل ميزة *دمج الشحنات* قبل أن تتمكن من إنشاء النهج.</span><span class="sxs-lookup"><span data-stu-id="e82c0-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="e82c0-118">مع ذلك، يجب أن تكون قد أكملت هذه الخطوة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e82c0-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="e82c0-119">إنشاء أوامر مبيعات لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="e82c0-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="e82c0-120">أبدا بإنشاء مجموعة من أوامر المبيعات التي يمكنك العمل بها.</span><span class="sxs-lookup"><span data-stu-id="e82c0-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="e82c0-121">يجب أن تعمل مع مستودع ممكّن لعمليات المستودع المتقدم (WMS).</span><span class="sxs-lookup"><span data-stu-id="e82c0-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="e82c0-122">يجب استخدام نفس المستودع لكل مجموعة من مجموعات الأوامر التالية، ما لم يتم ذكر مستودع مختلف بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="e82c0-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="e82c0-123">انتقال إلى **الحسابات المدينة \> الأوامر \> كافة أوامر المبيعات**، وقم بإنشاء مجموعة أوامر المبيعات التي لها الإعدادات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="e82c0-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="e82c0-124">إنشاء مجموعة الأوامر 1</span><span class="sxs-lookup"><span data-stu-id="e82c0-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="e82c0-125">أوامر المبيعات 1-1 و 1-2</span><span class="sxs-lookup"><span data-stu-id="e82c0-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="e82c0-126">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-127">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e82c0-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e82c0-128">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e82c0-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e82c0-129">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-130">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-131">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-132">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="e82c0-133">أمر المبيعات 1-3</span><span class="sxs-lookup"><span data-stu-id="e82c0-133">Sales order 1-3</span></span>

1. <span data-ttu-id="e82c0-134">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-135">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e82c0-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e82c0-136">**وضع التسليم:** *10*</span><span class="sxs-lookup"><span data-stu-id="e82c0-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="e82c0-137">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-138">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-139">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-140">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="e82c0-141">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-142">**رقم الصنف:** *A0002* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-143">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="e82c0-144">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e82c0-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e82c0-145">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="e82c0-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="e82c0-146">إنشاء مجموعة الأوامر 2</span><span class="sxs-lookup"><span data-stu-id="e82c0-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="e82c0-147">أوامر المبيعات 2-1 و 2-2</span><span class="sxs-lookup"><span data-stu-id="e82c0-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="e82c0-148">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-149">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="e82c0-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="e82c0-150">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e82c0-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e82c0-151">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-152">**رقم الصنف:** *M9200* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *قابل للاشتعال*)</span><span class="sxs-lookup"><span data-stu-id="e82c0-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="e82c0-153">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-154">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="e82c0-155">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-156">**رقم الصنف:** *M9201* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *متفجر*)</span><span class="sxs-lookup"><span data-stu-id="e82c0-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="e82c0-157">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="e82c0-158">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e82c0-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e82c0-159">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="e82c0-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="e82c0-160">إنشاء مجموعة الأوامر 3</span><span class="sxs-lookup"><span data-stu-id="e82c0-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="e82c0-161">أوامر المبيعات 3-1 و 3-2</span><span class="sxs-lookup"><span data-stu-id="e82c0-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="e82c0-162">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-163">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e82c0-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e82c0-164">**طلب العميل:** *1*</span><span class="sxs-lookup"><span data-stu-id="e82c0-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="e82c0-165">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-166">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-167">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-168">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="e82c0-169">أوامر المبيعات 3-3 و 3-4</span><span class="sxs-lookup"><span data-stu-id="e82c0-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="e82c0-170">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-171">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e82c0-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e82c0-172">**طلب العميل:** *2*</span><span class="sxs-lookup"><span data-stu-id="e82c0-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="e82c0-173">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-174">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-175">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-176">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="e82c0-177">إنشاء مجموعة الأوامر 4</span><span class="sxs-lookup"><span data-stu-id="e82c0-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="e82c0-178">أوامر المبيعات 4-1 و 4-2</span><span class="sxs-lookup"><span data-stu-id="e82c0-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="e82c0-179">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-180">**حساب العميل:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="e82c0-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="e82c0-181">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-182">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-183">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-184">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="e82c0-185">أوامر المبيعات 4-3 و 4-4</span><span class="sxs-lookup"><span data-stu-id="e82c0-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="e82c0-186">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-187">**حساب العميل:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="e82c0-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="e82c0-188">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-189">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-190">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-191">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="e82c0-192">أوامر المبيعات 4-5 و 4-6</span><span class="sxs-lookup"><span data-stu-id="e82c0-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="e82c0-193">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-194">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e82c0-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e82c0-195">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="e82c0-195">**Site:** *6*</span></span>
    - <span data-ttu-id="e82c0-196">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="e82c0-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e82c0-197">**الوعاء:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="e82c0-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="e82c0-198">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-199">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-200">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-201">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="e82c0-202">أوامر المبيعات 4-7 و 4-8</span><span class="sxs-lookup"><span data-stu-id="e82c0-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="e82c0-203">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e82c0-204">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e82c0-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e82c0-205">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="e82c0-205">**Site:** *6*</span></span>
    - <span data-ttu-id="e82c0-206">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="e82c0-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e82c0-207">**الوعاء:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="e82c0-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="e82c0-208">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e82c0-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e82c0-209">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="e82c0-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e82c0-210">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e82c0-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e82c0-211">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="e82c0-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="e82c0-212">إصدار الأوامر إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="e82c0-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="e82c0-213">اتبع الخطوات التالية لإصدار كل أمر مبيعات قمت بإنشائها لهذا السيناريو إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="e82c0-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="e82c0-214">انتقل إلى **الحسابات المدينة \> الأوامر‬ \> كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e82c0-215">ابحث عن وحدد أمر المبيعات المُراد إصدارها.</span><span class="sxs-lookup"><span data-stu-id="e82c0-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="e82c0-216">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **الإجراءات \> إصدار إلى المستودع‬** لإصدار أمر المبيعات المحدد.</span><span class="sxs-lookup"><span data-stu-id="e82c0-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="e82c0-217">كرر هذا الإجراء لكل أوامر المبيعات الأخرى التي قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e82c0-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="e82c0-218">دمج الشحنات باستخدام منضدة عمل دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="e82c0-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="e82c0-219">انتقل إلى **إدارة المستودعات \> الإصدار إلى المستودع \> منضدة عمل دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="e82c0-220">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e82c0-221">في مربع حوار محرر الاستعلام، في علامة تبويب **النطاق**، حدد **إضافة** لإضافة صف يتضمن الإعدادات التالية للشبكة:</span><span class="sxs-lookup"><span data-stu-id="e82c0-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="e82c0-222">**الجدول:** *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="e82c0-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="e82c0-223">**الحقل:** *أمر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="e82c0-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="e82c0-224">**المعايير:** أدخل قائمة مفصولة بفواصل بأرقام أوامر المبيعات لكل مجموعة أوامر قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e82c0-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="e82c0-225">حدد **موافق** لحفظ الاستعلام الخاص بك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="e82c0-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="e82c0-226">في جزء الإجراءات‬، حدد **دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="e82c0-227">حدد جميع الشحنات، ثم، في جزء الإجراءات، حدد علامة **دمج**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="e82c0-228">التحقق من الشحنات</span><span class="sxs-lookup"><span data-stu-id="e82c0-228">Verify the shipments</span></span>

<span data-ttu-id="e82c0-229">يتيح لك الإجراء التالي التحقق من الشحنات التي تم إنشاؤها أو تحديثها كنتيجة لدمج الشحنات.</span><span class="sxs-lookup"><span data-stu-id="e82c0-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="e82c0-230">استخدمه لمراجعة كل مجموعة أوامر قمت بإنشائها لهذا السيناريو، ثم قم بمراجعة الأقسام الفرعية التي تليها للتأكد من حصولك على النتائج المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="e82c0-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="e82c0-231">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="e82c0-232">ابحث عن الشحنة المطلوبة وحددها.</span><span class="sxs-lookup"><span data-stu-id="e82c0-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="e82c0-233">إذا تم استخدام نهج دمج عند إنشاء الشحنة أو تحديثها، فيجب أن تراه في حقل **نهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="e82c0-234">الشحنات المرتبطة لمجموعة الأوامر 1</span><span class="sxs-lookup"><span data-stu-id="e82c0-234">Related shipments for order set 1</span></span>

<span data-ttu-id="e82c0-235">ينبغي أن يتم إنشاء شحنتين:</span><span class="sxs-lookup"><span data-stu-id="e82c0-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="e82c0-236">تحتوي الشحنة الأولى على ثلاثة بنود وتم إنشاؤها باستخدام نهج دمج الشحنات *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="e82c0-237">تم إنشاء الشحنة الثانية، والتي لا تستخدم وضع نقل التسليم *Airways*، باستخدام نهج دمج الشحنات *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="e82c0-238">الشحنات المرتبطة لمجموعة الأوامر 2</span><span class="sxs-lookup"><span data-stu-id="e82c0-238">Related shipments for order set 2</span></span>

<span data-ttu-id="e82c0-239">ينبغي أن يتم إنشاء ثلاث شحنات:</span><span class="sxs-lookup"><span data-stu-id="e82c0-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="e82c0-240">تحتوي الشحنة الأولى على أصناف *قابلة للاشتعال*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="e82c0-241">ويحتوي كل من الشحنتين الأخرتين على بند واحد يتضمن الصنف *متفجر*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="e82c0-242">الشحنات المرتبطة لمجموعة الأوامر 3</span><span class="sxs-lookup"><span data-stu-id="e82c0-242">Related shipments for order set 3</span></span>

<span data-ttu-id="e82c0-243">ينبغي أن يتم إنشاء شحنتين:</span><span class="sxs-lookup"><span data-stu-id="e82c0-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="e82c0-244">تحتوي الشحنة الأولى على بنود أمر من أمر المبيعات الذي تم تعيين حقل **طلب العميل** له إلى *1*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="e82c0-245">تحتوي الشحنة الثانية على بنود أمر من أمر المبيعات الذي تم تعيين حقل **طلب العميل** له إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="e82c0-246">الشحنات المرتبطة لمجموعة الأوامر 4</span><span class="sxs-lookup"><span data-stu-id="e82c0-246">Related shipments for order set 4</span></span>

<span data-ttu-id="e82c0-247">ينبغي أن يتم إنشاء أربع شحنات:</span><span class="sxs-lookup"><span data-stu-id="e82c0-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="e82c0-248">يتم تجميع البنود من الأمرين للعميل *US-003* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e82c0-249">يتم تجميع البنود من الأمرين للعميل *US-004* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e82c0-250">يتم تجميع البنود من أوامر المبيعات 4-5 و 4-6 للعميل *US-007* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e82c0-251">يتم تجميع البنود من أوامر المبيعات 4-7 و 4-8 للعميل *US-007* في شحنة واحدة باستخدام نهج دمج الشحنات *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="e82c0-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e82c0-252">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e82c0-252">Additional resources</span></span>

- [<span data-ttu-id="e82c0-253">سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="e82c0-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="e82c0-254">تكوين نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="e82c0-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
