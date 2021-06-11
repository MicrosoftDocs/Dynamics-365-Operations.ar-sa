---
title: دمج الشحنات عن طريق الإصدار إلى المستودع من منضدة عمل تخطيط الحمل
description: يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع في نفس الحمل ثم دمجه تلقائيًا إلى شحنات
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 30824bf1c8e84bab08b6885ee812ed5e3e9937bb
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117171"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="03349-103">دمج الشحنات عن طريق الإصدار إلى المستودع من منضدة عمل تخطيط الحمل</span><span class="sxs-lookup"><span data-stu-id="03349-103">Consolidate shipments by releasing to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03349-104">يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع في نفس الحمل ثم دمجه تلقائيًا إلى شحنات</span><span class="sxs-lookup"><span data-stu-id="03349-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="03349-105">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="03349-105">Make demo data available</span></span>

<span data-ttu-id="03349-106">يشير السيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="03349-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="03349-107">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="03349-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="03349-108">إعداد نُهج دمج الشحنات وعوامل تصفيه المنتجات</span><span class="sxs-lookup"><span data-stu-id="03349-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="03349-109">يفترض السيناريو الموضح هنا أنك قمت بالفعل بتشغيل الميزة، ونفذت التمرينات في [تكوين نهج دمج الشحنات](configure-shipment-consolidation-policies.md)، وإنشاء النهج والسجلات الأخرى التي تم وصفها هناك.</span><span class="sxs-lookup"><span data-stu-id="03349-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="03349-110">تأكد من تنفيذ تلك التمرينات قبل المتابعة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="03349-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="03349-111">إنشاء أوامر مبيعات لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="03349-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="03349-112">أبدا بإنشاء مجموعة من أوامر المبيعات التي يمكنك العمل بها.</span><span class="sxs-lookup"><span data-stu-id="03349-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="03349-113">يجب أن تعمل مع مستودع ممكّن لعمليات المستودع المتقدم (WMS).</span><span class="sxs-lookup"><span data-stu-id="03349-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="03349-114">يجب استخدام نفس المستودع لكل مجموعة من مجموعات الأوامر التالية، ما لم يتم ذكر مستودع مختلف بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="03349-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="03349-115">انتقال إلى **الحسابات المدينة \> الأوامر \> كافة أوامر المبيعات**، وقم بإنشاء مجموعة أوامر المبيعات التي لها الإعدادات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="03349-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="03349-116">إنشاء مجموعة الأوامر 1</span><span class="sxs-lookup"><span data-stu-id="03349-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="03349-117">أمر المبيعات 1-1</span><span class="sxs-lookup"><span data-stu-id="03349-117">Sales order 1-1</span></span>

1. <span data-ttu-id="03349-118">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="03349-119">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="03349-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="03349-120">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="03349-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="03349-121">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-122">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-123">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-124">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="03349-125">أمر المبيعات 1-2</span><span class="sxs-lookup"><span data-stu-id="03349-125">Sales order 1-2</span></span>

1. <span data-ttu-id="03349-126">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="03349-127">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="03349-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="03349-128">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="03349-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="03349-129">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-130">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-131">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-132">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="03349-133">أمر المبيعات 1-3</span><span class="sxs-lookup"><span data-stu-id="03349-133">Sales order 1-3</span></span>

1. <span data-ttu-id="03349-134">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="03349-135">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="03349-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="03349-136">**وضع التسليم:** *10*</span><span class="sxs-lookup"><span data-stu-id="03349-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="03349-137">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-138">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-139">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-140">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="03349-141">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-142">**رقم الصنف:** *A0002* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-143">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="03349-144">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="03349-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="03349-145">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="03349-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="03349-146">إنشاء مجموعة الأوامر 2</span><span class="sxs-lookup"><span data-stu-id="03349-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="03349-147">أوامر المبيعات 2-1 و 2-2</span><span class="sxs-lookup"><span data-stu-id="03349-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="03349-148">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-149">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="03349-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="03349-150">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-151">**رقم الصنف:** *M9200* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *قابل للاشتعال*)</span><span class="sxs-lookup"><span data-stu-id="03349-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="03349-152">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-153">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="03349-154">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-155">**رقم الصنف:** *M9201* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *متفجر*)</span><span class="sxs-lookup"><span data-stu-id="03349-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="03349-156">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="03349-157">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="03349-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="03349-158">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="03349-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="03349-159">إنشاء مجموعة الأوامر 3</span><span class="sxs-lookup"><span data-stu-id="03349-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="03349-160">أوامر المبيعات 3-1 و 3-2</span><span class="sxs-lookup"><span data-stu-id="03349-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="03349-161">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-162">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="03349-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="03349-163">**طلب العميل:** *1*</span><span class="sxs-lookup"><span data-stu-id="03349-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="03349-164">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-165">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-166">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-167">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="03349-168">أوامر المبيعات 3-3 و 3-4</span><span class="sxs-lookup"><span data-stu-id="03349-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="03349-169">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-170">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="03349-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="03349-171">**طلب العميل:** *2*</span><span class="sxs-lookup"><span data-stu-id="03349-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="03349-172">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-173">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-174">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-175">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="03349-176">إنشاء مجموعة الأوامر 4</span><span class="sxs-lookup"><span data-stu-id="03349-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="03349-177">أوامر المبيعات 4-1 و 4-2</span><span class="sxs-lookup"><span data-stu-id="03349-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="03349-178">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-179">**حساب العميل:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="03349-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="03349-180">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-181">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-182">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-183">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="03349-184">أوامر المبيعات 4-3 و 4-4</span><span class="sxs-lookup"><span data-stu-id="03349-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="03349-185">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-186">**حساب العميل:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="03349-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="03349-187">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-188">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-189">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-190">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="03349-191">أوامر المبيعات 4-5 و 4-6</span><span class="sxs-lookup"><span data-stu-id="03349-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="03349-192">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-193">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="03349-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="03349-194">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="03349-194">**Site:** *6*</span></span>
    - <span data-ttu-id="03349-195">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="03349-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="03349-196">**الوعاء:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="03349-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="03349-197">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-198">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-199">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-200">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="03349-201">أوامر المبيعات 4-7 و 4-8</span><span class="sxs-lookup"><span data-stu-id="03349-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="03349-202">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="03349-203">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="03349-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="03349-204">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="03349-204">**Site:** *6*</span></span>
    - <span data-ttu-id="03349-205">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="03349-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="03349-206">**الوعاء:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="03349-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="03349-207">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="03349-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="03349-208">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="03349-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="03349-209">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="03349-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="03349-210">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="03349-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="03349-211">استخدام منضدة عمل تخطيط الحمل لإنشاء أحمال وإصدارها إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="03349-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="03349-212">اتبع الخطوات التالية لإنشاء حمل لكل مجموعة أوامر قمت بإنشائها لهذا السيناريو ثم قم بإصدارها إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="03349-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="03349-213">انتقل إلى **إدارة المستودعات \> الأحمال \> منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="03349-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="03349-214">من علامة التبويب **بنود المبيعات**، ابحث عن كافة بنود أمر البيعات وحددها من إحدى مجموعات الأوامر التي قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="03349-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="03349-215">في جزء الإجراءات، ضمن علامة التبويب **العرض والطلب**، حدد **إضافة \> إلى حمل جديد** لإضافة بنود الأمر المحدد إلى حمل جديد.</span><span class="sxs-lookup"><span data-stu-id="03349-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="03349-216">في مربع الحوار **تعيين قالب الحمل**، في حقل **معرف قالب الحمل**، حدد قالب حمل، مثل *قالب حمل قياسي*.</span><span class="sxs-lookup"><span data-stu-id="03349-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="03349-217">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="03349-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="03349-218">في قسم **الأحمال**، ابحث عن الحمل الذي أنشأته للتو وحدده.</span><span class="sxs-lookup"><span data-stu-id="03349-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="03349-219">حدد **الإصدار \> الإصدار إلى المستودع** لإصدار الحمل المحدد إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="03349-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="03349-220">كرر هذا الإجراء لمجموعات الأوامر الثلاثة الأخرى التي قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="03349-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="03349-221">التحقق من الشحنات</span><span class="sxs-lookup"><span data-stu-id="03349-221">Verify the shipments</span></span>

<span data-ttu-id="03349-222">يتيح لك الإجراء التالي التحقق من الشحنات التي تم إنشاؤها أو تحديثها كنتيجة لدمج الشحنات.</span><span class="sxs-lookup"><span data-stu-id="03349-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="03349-223">استخدمه لمراجعة كل مجموعة أوامر قمت بإنشائها لهذا السيناريو، ثم قم بمراجعة الأقسام الفرعية التي تليها للتأكد من حصولك على النتائج المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="03349-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="03349-224">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="03349-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="03349-225">ابحث عن الشحنة المطلوبة وحددها.</span><span class="sxs-lookup"><span data-stu-id="03349-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="03349-226">إذا تم استخدام نهج دمج عند إنشاء الشحنة أو تحديثها، فيجب أن تراه في حقل **نهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="03349-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="03349-227">إصدار مجموعة الأوامر 1 في حمل واحد</span><span class="sxs-lookup"><span data-stu-id="03349-227">Release order set 1 in one load</span></span>

<span data-ttu-id="03349-228">ينبغي أن يتم إنشاء شحنتين:</span><span class="sxs-lookup"><span data-stu-id="03349-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="03349-229">تحتوي الشحنة الأولى على ثلاثة بنود وتم إنشاؤها باستخدام نهج دمج الشحنات *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="03349-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="03349-230">تم إنشاء الشحنة الثانية، والتي لا تستخدم وضع نقل التسليم *Airways*، باستخدام نهج دمج الشحنات *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="03349-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="03349-231">إصدار مجموعة الأوامر 2 في حمل واحد</span><span class="sxs-lookup"><span data-stu-id="03349-231">Release order set 2 in one load</span></span>

<span data-ttu-id="03349-232">ينبغي أن يتم إنشاء ثلاث شحنات:</span><span class="sxs-lookup"><span data-stu-id="03349-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="03349-233">تحتوي الشحنة الأولى على أصناف *قابلة للاشتعال*.</span><span class="sxs-lookup"><span data-stu-id="03349-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="03349-234">ويحتوي كل من الشحنتين الأخرتين على بند واحد يتضمن الصنف *متفجر*.</span><span class="sxs-lookup"><span data-stu-id="03349-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="03349-235">إصدار مجموعة الأوامر 3 في حمل واحد</span><span class="sxs-lookup"><span data-stu-id="03349-235">Release order set 3 in one load</span></span>

<span data-ttu-id="03349-236">ينبغي أن يتم إنشاء شحنتين:</span><span class="sxs-lookup"><span data-stu-id="03349-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="03349-237">تحتوي الشحنة الأولى على بنود أمر من أمر المبيعات الذي تم تعيين حقل **طلب العميل** له إلى *1*.</span><span class="sxs-lookup"><span data-stu-id="03349-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="03349-238">تحتوي الشحنة الثانية على بنود أمر من أمر المبيعات الذي تم تعيين حقل **طلب العميل** له إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="03349-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="03349-239">إصدار مجموعة الأوامر 4 في حمل واحد</span><span class="sxs-lookup"><span data-stu-id="03349-239">Release order set 4 in one load</span></span>

<span data-ttu-id="03349-240">ينبغي أن يتم إنشاء أربع شحنات:</span><span class="sxs-lookup"><span data-stu-id="03349-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="03349-241">يتم تجميع البنود من الأمرين لحساب العميل *US-003* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="03349-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="03349-242">يتم تجميع البنود من الأمرين لحساب العميل *US-004* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="03349-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="03349-243">يتم تجميع البنود من أوامر المبيعات 4-5 و 4-6 لحساب العميل *US-007* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="03349-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="03349-244">يتم تجميع البنود من أوامر المبيعات 4-7 و 4-8 لحساب العميل *US-007* في شحنة واحدة باستخدام نهج دمج الشحنات *‎CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="03349-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03349-245">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="03349-245">Additional resources</span></span>

- [<span data-ttu-id="03349-246">سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="03349-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="03349-247">تكوين نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="03349-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]