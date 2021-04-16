---
title: دمج الشحنات يدويًا باستخدام صفحة دمج الشحنات
description: يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع ثم دمجها لاحقًا باستخدام صفحة دمج الشحنات.
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
ms.openlocfilehash: e4e6dac1d1b4a304062e852526235eeee6579540
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840379"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="0b730-103">دمج الشحنات يدويًا باستخدام صفحة دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="0b730-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b730-104">يقدم هذا الموضوع سيناريو يتم فيه إصدار الأوامر المتعددة إلى المستودع ثم دمجها لاحقًا باستخدام صفحة **دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0b730-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="0b730-105">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="0b730-105">Make demo data available</span></span>

<span data-ttu-id="0b730-106">يشير السيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b730-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0b730-107">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="0b730-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="0b730-108">إعداد نُهج دمج الشحنات وعوامل تصفيه المنتجات</span><span class="sxs-lookup"><span data-stu-id="0b730-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="0b730-109">يفترض السيناريو الموضح هنا أنك قمت بالفعل بتشغيل الميزة، ونفذت التمرينات في [تكوين نهج دمج الشحنات](configure-shipment-consolidation-policies.md)، وإنشاء النهج والسجلات الأخرى التي تم وصفها هناك.</span><span class="sxs-lookup"><span data-stu-id="0b730-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="0b730-110">تأكد من تنفيذ تلك التمرينات قبل المتابعة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="0b730-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="0b730-111">إنشاء أوامر مبيعات لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="0b730-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="0b730-112">أبدا بإنشاء مجموعة من أوامر المبيعات التي يمكنك العمل بها.</span><span class="sxs-lookup"><span data-stu-id="0b730-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="0b730-113">يجب أن تعمل مع مستودع ممكّن لعمليات المستودع المتقدم (WMS).</span><span class="sxs-lookup"><span data-stu-id="0b730-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="0b730-114">يجب استخدام نفس المستودع لكل مجموعة من مجموعات الأوامر التالية، ما لم يتم ذكر مستودع مختلف بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="0b730-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="0b730-115">انتقال إلى **الحسابات المدينة \> الأوامر \> كافة أوامر المبيعات**، وقم بإنشاء مجموعة أوامر المبيعات التي لها الإعدادات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="0b730-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="0b730-116">إنشاء أوامر المبيعات 1 و2</span><span class="sxs-lookup"><span data-stu-id="0b730-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="0b730-117">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0b730-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b730-118">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0b730-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0b730-119">**الوعاء:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="0b730-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="0b730-120">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0b730-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b730-121">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="0b730-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b730-122">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b730-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b730-123">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="0b730-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="0b730-124">إنشاء أوامر المبيعات 3 و4</span><span class="sxs-lookup"><span data-stu-id="0b730-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="0b730-125">قم بإنشاء اثنين من أوامر المبيعات المتماثلة التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0b730-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b730-126">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0b730-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0b730-127">**الوعاء:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="0b730-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="0b730-128">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0b730-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b730-129">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="0b730-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b730-130">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b730-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b730-131">حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="0b730-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="0b730-132">إصدار الأوامر إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="0b730-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="0b730-133">اتبع الخطوات التالية لإصدار كل أمر مبيعات قمت بإنشائها لهذا السيناريو إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="0b730-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="0b730-134">انتقل إلى **الحسابات المدينة \> الأوامر‬ \> كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="0b730-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0b730-135">ابحث عن وحدد أمر المبيعات المُراد إصدارها.</span><span class="sxs-lookup"><span data-stu-id="0b730-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="0b730-136">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **الإجراءات \> إصدار إلى المستودع‬** لإصدار أمر المبيعات المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b730-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="0b730-137">كرر هذا الإجراء لكل أوامر المبيعات الأخرى التي قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="0b730-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="0b730-138">دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="0b730-138">Consolidate shipments</span></span>

1. <span data-ttu-id="0b730-139">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0b730-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="0b730-140">ابحث عن الشحنة التي تم إنشاؤها عند إصدار أمر المبيعات 1 إلى المستودع وقم بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="0b730-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="0b730-141">(يجب تعيين حقل **نهج دمج الشحنات** الخاص بها إلى *وعاء الأوامر*.)</span><span class="sxs-lookup"><span data-stu-id="0b730-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="0b730-142">في جزء الإجراءات، في علامة تبويب **الشحنات**، حدد **الشحنات \> دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0b730-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="0b730-143">التحقق من الشحنات المقترحة للدمج.</span><span class="sxs-lookup"><span data-stu-id="0b730-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="0b730-144">يجب اقتراح شحنة واحدة فقط لها نفس النهج لعملية الدمج.</span><span class="sxs-lookup"><span data-stu-id="0b730-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="0b730-145">أغلق صفحة **دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0b730-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="0b730-146">ابحث عن الشحنة التي تم إنشاؤها عند إصدار أمر المبيعات 3 إلى المستودع وقم بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="0b730-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="0b730-147">(يجب تعيين حقل **نهج دمج الشحنات** الخاص بها إلى *الافتراضي*.)</span><span class="sxs-lookup"><span data-stu-id="0b730-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="0b730-148">في جزء الإجراءات، في علامة تبويب **الشحنات**، حدد **الشحنات \> دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0b730-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="0b730-149">التحقق من عدم اقتراح أي شحنات للدمج.</span><span class="sxs-lookup"><span data-stu-id="0b730-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="0b730-150">حدد **إظهار عوامل التصفية**.</span><span class="sxs-lookup"><span data-stu-id="0b730-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="0b730-151">في جزء **عوامل التصفية** ، قم إزالة عاملة التصفية **رقم الأمر**، ثم قم بتحديد **تطبيق**</span><span class="sxs-lookup"><span data-stu-id="0b730-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="0b730-152">التحقق من الشحنات المقترحة للدمج.</span><span class="sxs-lookup"><span data-stu-id="0b730-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="0b730-153">يجب اقتراح شحنة واحدة فقط لها نفس النهج لعملية الدمج.</span><span class="sxs-lookup"><span data-stu-id="0b730-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b730-154">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0b730-154">Additional resources</span></span>

- [<span data-ttu-id="0b730-155">سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="0b730-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="0b730-156">تكوين نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="0b730-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]