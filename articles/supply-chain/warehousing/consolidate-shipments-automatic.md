---
title: دمج الشحنات عند إصدارها إلى المستودع باستخدام الإصدار التلقائي لأوامر المبيعات
description: يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع في نفس الإجراء الدوري الخاص بالإصدار إلى مستودع والذي يتم تنفيذه تلقائيًا.
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
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f4d095456435a3401daa173d79b80b81176a3c17
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987108"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="44254-103">دمج الشحنات عند إصدارها إلى المستودع باستخدام الإصدار التلقائي لأوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="44254-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44254-104">يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع في نفس الإجراء الدوري الخاص بالإصدار إلى مستودع والذي يتم تنفيذه تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="44254-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="44254-105">سيتم دمج الأوامر تلقائيا إلى الشحنات، استنادًا إلى القواعد التي تم تحديدها كنهج دمج الشحنات.</span><span class="sxs-lookup"><span data-stu-id="44254-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="44254-106">أثناء السيناريو، ستقوم بإنشاء مجموعات من أوامر المبيعات وإصدار كل مجموعة إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="44254-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="44254-107">ثم ستقوم بمراجعة الشحنات التي تم إنشاؤها أو تحديثها أثناء دمج الشحنات، استنادا إلى النُهج التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="44254-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="44254-108">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="44254-108">Make demo data available</span></span>

<span data-ttu-id="44254-109">يشير السيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="44254-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="44254-110">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="44254-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="44254-111">إعداد نُهج دمج الشحنات وعوامل تصفيه المنتجات</span><span class="sxs-lookup"><span data-stu-id="44254-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="44254-112">يفترض السيناريو الموضح هنا أنك قمت بالفعل بتشغيل الميزة، ونفذت التمرينات في [تكوين نهج دمج الشحنات](configure-shipment-consolidation-policies.md)، وإنشاء النهج والسجلات الأخرى التي تم وصفها هناك.</span><span class="sxs-lookup"><span data-stu-id="44254-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="44254-113">تأكد من تنفيذ تلك التمرينات قبل المتابعة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="44254-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="44254-114">إنشاء أوامر مبيعات لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="44254-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="44254-115">أبدا بإنشاء مجموعة من أوامر المبيعات التي يمكنك العمل بها.</span><span class="sxs-lookup"><span data-stu-id="44254-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="44254-116">يجب أن تعمل مع مستودع ممكّن لعمليات المستودع المتقدم (WMS).</span><span class="sxs-lookup"><span data-stu-id="44254-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="44254-117">يجب استخدام نفس المستودع لكل مجموعة من مجموعات الأوامر التالية، ما لم يتم ذكر مستودع مختلف بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="44254-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="44254-118">انتقال إلى **الحسابات المدينة \> الأوامر \> كافة أوامر المبيعات** ، وقم بإنشاء مجموعة أوامر المبيعات التي لها الإعدادات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="44254-118">Go to **Accounts receivable \> Orders \> All sales orders** , and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="44254-119">إنشاء مجموعة الأوامر 1</span><span class="sxs-lookup"><span data-stu-id="44254-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="44254-120">أمر المبيعات 1-1</span><span class="sxs-lookup"><span data-stu-id="44254-120">Sales order 1-1</span></span>

1. <span data-ttu-id="44254-121">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="44254-122">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="44254-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="44254-123">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="44254-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="44254-124">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-125">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-126">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="44254-127">أمر المبيعات 1-2</span><span class="sxs-lookup"><span data-stu-id="44254-127">Sales order 1-2</span></span>

1. <span data-ttu-id="44254-128">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="44254-129">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="44254-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="44254-130">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="44254-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="44254-131">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-132">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-133">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="44254-134">أمر المبيعات 1-3</span><span class="sxs-lookup"><span data-stu-id="44254-134">Sales order 1-3</span></span>

1. <span data-ttu-id="44254-135">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="44254-136">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="44254-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="44254-137">**وضع التسليم:** *10*</span><span class="sxs-lookup"><span data-stu-id="44254-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="44254-138">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-139">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-140">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="44254-141">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-142">**رقم الصنف:** *A0002* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-143">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="44254-144">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="44254-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="44254-145">إنشاء مجموعة الأوامر 2</span><span class="sxs-lookup"><span data-stu-id="44254-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="44254-146">أوامر المبيعات 2-1 و 2-2</span><span class="sxs-lookup"><span data-stu-id="44254-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="44254-147">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="44254-148">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="44254-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="44254-149">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-150">**رقم الصنف:** *M9200* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *قابل للاشتعال* )</span><span class="sxs-lookup"><span data-stu-id="44254-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable* )</span></span>
    - <span data-ttu-id="44254-151">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="44254-152">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-153">**رقم الصنف:** *M9201* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *متفجر* )</span><span class="sxs-lookup"><span data-stu-id="44254-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive* )</span></span>
    - <span data-ttu-id="44254-154">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="44254-155">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="44254-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="44254-156">إنشاء مجموعة الأوامر 3</span><span class="sxs-lookup"><span data-stu-id="44254-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="44254-157">أمر المبيعات 3-1</span><span class="sxs-lookup"><span data-stu-id="44254-157">Sales order 3-1</span></span>

1. <span data-ttu-id="44254-158">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="44254-159">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="44254-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="44254-160">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-161">**رقم الصنف:** *M9200* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *قابل للاشتعال* )</span><span class="sxs-lookup"><span data-stu-id="44254-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable* )</span></span>
    - <span data-ttu-id="44254-162">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="44254-163">أضف بند أمر ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-164">**رقم الصنف:** *M9201* (العنصر الذي تم فيه تعيين عامل تصفية **الرمز 4** إلى *متفجر* )</span><span class="sxs-lookup"><span data-stu-id="44254-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive* )</span></span>
    - <span data-ttu-id="44254-165">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="44254-166">**وضع التسليم:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="44254-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="44254-167">يكون هذا الأمر مطابقًا للأمرين اللذين قمت بإنشائهما لمجموعة الأوامر رقم 2.</span><span class="sxs-lookup"><span data-stu-id="44254-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="44254-168">ومع ذلك، يتم إدراجها كمجموعة أوامر خاصة بها لأنك ستقوم بتحريرها بشكل منفصل لاحقًا في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="44254-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="44254-169">إنشاء مجموعة الأوامر 4</span><span class="sxs-lookup"><span data-stu-id="44254-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="44254-170">أمر المبيعات 4-1</span><span class="sxs-lookup"><span data-stu-id="44254-170">Sales order 4-1</span></span>

1. <span data-ttu-id="44254-171">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="44254-172">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="44254-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="44254-173">**طلب العميل:** *1*</span><span class="sxs-lookup"><span data-stu-id="44254-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="44254-174">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-175">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-176">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="44254-177">إنشاء مجموعة الأوامر 5</span><span class="sxs-lookup"><span data-stu-id="44254-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="44254-178">أوامر المبيعات 5-1 و 5-2</span><span class="sxs-lookup"><span data-stu-id="44254-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="44254-179">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="44254-180">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="44254-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="44254-181">**طلب العميل:** *2*</span><span class="sxs-lookup"><span data-stu-id="44254-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="44254-182">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-183">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-184">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="44254-185">أمر المبيعات 5-3</span><span class="sxs-lookup"><span data-stu-id="44254-185">Sales order 5-3</span></span>

1. <span data-ttu-id="44254-186">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="44254-187">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="44254-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="44254-188">**طلب العميل:** *1*</span><span class="sxs-lookup"><span data-stu-id="44254-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="44254-189">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-190">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-191">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="44254-192">إنشاء مجموعة الأوامر 6</span><span class="sxs-lookup"><span data-stu-id="44254-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="44254-193">أوامر المبيعات 6-1 و 6-2</span><span class="sxs-lookup"><span data-stu-id="44254-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="44254-194">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="44254-195">**حساب العميل:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="44254-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="44254-196">**طلب العميل:** *2*</span><span class="sxs-lookup"><span data-stu-id="44254-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="44254-197">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-198">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-199">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="44254-200">أوامر المبيعات 6-3 و 6-4</span><span class="sxs-lookup"><span data-stu-id="44254-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="44254-201">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="44254-202">**حساب العميل:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="44254-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="44254-203">**طلب العميل:** *1*</span><span class="sxs-lookup"><span data-stu-id="44254-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="44254-204">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-205">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-206">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="44254-207">أوامر المبيعات 6-5 و 6-6</span><span class="sxs-lookup"><span data-stu-id="44254-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="44254-208">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="44254-209">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="44254-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="44254-210">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="44254-210">**Site:** *6*</span></span>
    - <span data-ttu-id="44254-211">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="44254-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="44254-212">**الوعاء:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="44254-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="44254-213">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-214">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-215">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="44254-216">أوامر المبيعات 6-7 و 6-8</span><span class="sxs-lookup"><span data-stu-id="44254-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="44254-217">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="44254-218">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="44254-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="44254-219">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="44254-219">**Site:** *6*</span></span>
    - <span data-ttu-id="44254-220">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="44254-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="44254-221">**الوعاء:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="44254-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="44254-222">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="44254-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="44254-223">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="44254-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="44254-224">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="44254-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="44254-225">الإصدار التلقائي لأوامر المبيعات إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="44254-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="44254-226">مع كل مجموعة من أوامر المبيات التي قمت بإنشائها سابقًا، ستقوم بإكمال إجراء للإصدار التلقائي إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="44254-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="44254-227">في كل حالة، ستعمل خلال [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) الذي تم توفيره هنا.</span><span class="sxs-lookup"><span data-stu-id="44254-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="44254-228">إجراء الإصدار إلى المستودع الأساسي</span><span class="sxs-lookup"><span data-stu-id="44254-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="44254-229">بالنسبة لكل مجموعة من أوامر المبيعات التي قمت بإنشائها سابقصا، ستقوم بإكمال الإجراءات الثلاثة الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="44254-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="44254-230">تحديث قالب الموجة الذي سيتم استخدامه أثناء التحرير</span><span class="sxs-lookup"><span data-stu-id="44254-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="44254-231">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة** .</span><span class="sxs-lookup"><span data-stu-id="44254-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates** .</span></span>
1. <span data-ttu-id="44254-232">قم بتعيين حقل **نوع قالب الموجة** إلى *الشحن* .</span><span class="sxs-lookup"><span data-stu-id="44254-232">Set the **Wave template type** field to *Shipping* .</span></span>
1. <span data-ttu-id="44254-233">ابحث عن وحدد قالب الموجة المرتبط بالمستودع الذي قمت باستخدامه في مجموعات الأوامر التي قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="44254-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="44254-234">على سبيل المثال، إذا استخدمت المستودع *24* ، فحدد قالب الموجة **افتراضي الشحن 24** .</span><span class="sxs-lookup"><span data-stu-id="44254-234">For example, if you used warehouse *24* , select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="44254-235">إذا استخدمت المستودع *61* ، فحدد قالب الموجة **الشحن 61** .</span><span class="sxs-lookup"><span data-stu-id="44254-235">If you used warehouse *61* , select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="44254-236">في جزء الإجراءات، حدد **تحرير** .</span><span class="sxs-lookup"><span data-stu-id="44254-236">On the Action Pane, select **Edit** .</span></span>
1. <span data-ttu-id="44254-237">قم بتعيين الخيار **معالجة الموجة عند الإصدار إلى المستودع** إلى *لا* .</span><span class="sxs-lookup"><span data-stu-id="44254-237">Set the **Process wave at release to warehouse** option to *No* .</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="44254-238">الإصدار إلى مستودع</span><span class="sxs-lookup"><span data-stu-id="44254-238">Release to the warehouse</span></span>

1. <span data-ttu-id="44254-239">انتقل إلى **إدارة المستودعات \> الإصدار إلى المستودع \> الإصدار التلقائي لأوامر المبيعات** .</span><span class="sxs-lookup"><span data-stu-id="44254-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders** .</span></span>
1. <span data-ttu-id="44254-240">تعيين حقل **الكمية المراد إصدارها** إلى *الكل* .</span><span class="sxs-lookup"><span data-stu-id="44254-240">Set the **Quantity to release** field to *All* .</span></span>
1. <span data-ttu-id="44254-241">في علامة التبويب السريعة **السجلات المطلوب تضمينها** ، حدد **عامل التصفية** لفتح مربع حوار الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="44254-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="44254-242">في علامة تبويب **النطاق** ، حدد **إضافة** لإضافة صف يتضمن الإعدادات التالية للشبكة:</span><span class="sxs-lookup"><span data-stu-id="44254-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="44254-243">**الجدول:** *أمر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="44254-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="44254-244">**الجدول المشتق:** *أمر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="44254-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="44254-245">**الحقل:** *أمر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="44254-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="44254-246">**المعايير:** أدخل قائمة مفصولة بفواصل بأرقام أوامر المبيعات من مجموعة الأمر المرغوبة.</span><span class="sxs-lookup"><span data-stu-id="44254-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="44254-247">حدد **موافق** لحفظ الاستعلام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="44254-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="44254-248">حدد **موافق** لبدء إجراء *الإصدار التلقائي إلى المستودع* .</span><span class="sxs-lookup"><span data-stu-id="44254-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="44254-249">مراجعة الشحنة التي تم إنشاؤها أو تحديثها</span><span class="sxs-lookup"><span data-stu-id="44254-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="44254-250">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات** .</span><span class="sxs-lookup"><span data-stu-id="44254-250">Go to **Warehouse management \> Shipments \> All shipments** .</span></span>
1. <span data-ttu-id="44254-251">ابحث عن الشحنة المطلوبة وحددها.</span><span class="sxs-lookup"><span data-stu-id="44254-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="44254-252">إذا تم استخدام نهج دمج عند إنشاء الشحنة أو تحديثها، فيجب أن تراه في حقل **نهج دمج الشحنات** .</span><span class="sxs-lookup"><span data-stu-id="44254-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="44254-253">إصدار أوامر المبيعات من مجموعة الأوامر 1</span><span class="sxs-lookup"><span data-stu-id="44254-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="44254-254">اتبع [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) لإصدار أوامر المبيعات من مجموعة الأوامر 1.</span><span class="sxs-lookup"><span data-stu-id="44254-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="44254-255">وعندما تنتهي من ذلك، ينبغي أن ترى أنه تم إنشاء شحنتين:</span><span class="sxs-lookup"><span data-stu-id="44254-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="44254-256">تحتوي الشحنة الأولى على ثلاثة بنود وتم إنشاؤها باستخدام نهج دمج الشحنات *CustomerMode* .</span><span class="sxs-lookup"><span data-stu-id="44254-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="44254-257">تم إنشاء الشحنة الثانية، والتي لا تستخدم وضع نقل التسليم *Airways* ، باستخدام نهج دمج الشحنات *CustomerOrderNo* .</span><span class="sxs-lookup"><span data-stu-id="44254-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="44254-258">إصدار أوامر المبيعات من مجموعة الأوامر 2</span><span class="sxs-lookup"><span data-stu-id="44254-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="44254-259">اتبع [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) لإصدار أوامر المبيعات من مجموعة الأوامر 2.</span><span class="sxs-lookup"><span data-stu-id="44254-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="44254-260">وعندما تنتهي من ذلك، ينبغي أن ترى أنه تم إنشاء ثلاث شحنات:</span><span class="sxs-lookup"><span data-stu-id="44254-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="44254-261">تحتوي الشحنة الأولى على أصناف *قابلة للاشتعال* .</span><span class="sxs-lookup"><span data-stu-id="44254-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="44254-262">ويحتوي كل من الشحنتين الأخرتين على بند واحد يتضمن الصنف *متفجر* .</span><span class="sxs-lookup"><span data-stu-id="44254-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="44254-263">إصدار أوامر المبيعات من مجموعة الأوامر 3</span><span class="sxs-lookup"><span data-stu-id="44254-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="44254-264">اتبع [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) لإصدار أوامر المبيعات من مجموعة الأوامر 3.</span><span class="sxs-lookup"><span data-stu-id="44254-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="44254-265">وعند الانتهاء، ينبغي أن ترى أن الإجراءات التالية قد حدثت:</span><span class="sxs-lookup"><span data-stu-id="44254-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="44254-266">تم تحديث شحنة واحدة موجودة (الشحنة التي تم إنشاؤها عندما تم إصدار مجموعة الأوامر 2 إلى المستودع).</span><span class="sxs-lookup"><span data-stu-id="44254-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="44254-267">تمت إضافة سطر يحتوي على الصنف *قابل للاشتعال* .</span><span class="sxs-lookup"><span data-stu-id="44254-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="44254-268">تم إنشاء شحنة جديدة تحتوي على الصنف *متفجر* .</span><span class="sxs-lookup"><span data-stu-id="44254-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="44254-269">إصدار أوامر المبيعات من مجموعة الأوامر 4</span><span class="sxs-lookup"><span data-stu-id="44254-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="44254-270">اتبع [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) لإصدار أوامر المبيعات من مجموعة الأوامر 4.</span><span class="sxs-lookup"><span data-stu-id="44254-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="44254-271">وعندما تنتهي من ذلك، ينبغي أن ترى أنه تم تحديث شحنة واحدة موجودة (في المكان الذي تم فيه تعيين حقل **طلب العميل** إلى *1* ).</span><span class="sxs-lookup"><span data-stu-id="44254-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1* ) was updated.</span></span> <span data-ttu-id="44254-272">تمت إضافة سطر جديد إليه.</span><span class="sxs-lookup"><span data-stu-id="44254-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="44254-273">إصدار أوامر المبيعات من مجموعة الأوامر 5</span><span class="sxs-lookup"><span data-stu-id="44254-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="44254-274">اتبع [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) لإصدار أوامر المبيعات من مجموعة الأوامر 5.</span><span class="sxs-lookup"><span data-stu-id="44254-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="44254-275">وعند الانتهاء، ينبغي أن ترى أن الإجراءات التالية قد حدثت:</span><span class="sxs-lookup"><span data-stu-id="44254-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="44254-276">تم تحديث شحنة واحدة موجودة (في المكان الذي تم فيه تعيين حقل **طلب العميل** إلى *1* ).</span><span class="sxs-lookup"><span data-stu-id="44254-276">One existing shipment (where the **Customer requisition** field is set to *1* ) was updated.</span></span> <span data-ttu-id="44254-277">تمت إضافة بند من أمر المبيعات 5-3 إليه (في المكان الذي تم فيه تعيين حقل **طلب العميل** إلى *1* ).</span><span class="sxs-lookup"><span data-stu-id="44254-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1* ) was added to it.</span></span>
- <span data-ttu-id="44254-278">تم إنشاء شحنة جديدة، في المكان الذي تم فيه تجميع البنود من أوامر المبيعات 5-1 و 5-2 في شحنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="44254-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="44254-279">إصدار أوامر المبيعات من مجموعة الأوامر 6</span><span class="sxs-lookup"><span data-stu-id="44254-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="44254-280">اتبع [إجراء الإصدار إلى المستودع الأساسي](#release-procedure) لإصدار أوامر المبيعات من مجموعة الأوامر 6.</span><span class="sxs-lookup"><span data-stu-id="44254-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="44254-281">وعندما تنتهي من ذلك، ينبغي أن ترى أنه تم إنشاء أربعة شحنات:</span><span class="sxs-lookup"><span data-stu-id="44254-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="44254-282">يتم تجميع البنود من الأمرين للعميل *US-003* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر* .</span><span class="sxs-lookup"><span data-stu-id="44254-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="44254-283">يتم تجميع البنود من الأمرين للعميل *US-004* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر* .</span><span class="sxs-lookup"><span data-stu-id="44254-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="44254-284">يتم تجميع البنود من أوامر المبيعات 6-5 و 6-6 للعميل *US-007* في شحنة واحدة باستخدام نهج دمج الشحنات *وعاء الأوامر* .</span><span class="sxs-lookup"><span data-stu-id="44254-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="44254-285">يتم تجميع البنود من أوامر المبيعات 6-7 و 6-8 للعميل *US-007* في شحنة واحدة باستخدام نهج دمج الشحنات *CrossOrder* .</span><span class="sxs-lookup"><span data-stu-id="44254-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44254-286">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="44254-286">Additional resources</span></span>

- [<span data-ttu-id="44254-287">سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="44254-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="44254-288">تكوين نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="44254-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
