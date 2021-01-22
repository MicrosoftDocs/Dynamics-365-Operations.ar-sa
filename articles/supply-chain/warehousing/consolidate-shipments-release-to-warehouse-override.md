---
title: دمج الشحنات عند تجاوز سياسة دمج الشحنات من صفحة الإصدار إلى المستودع
description: يقدم هذا الموضوع سيناريو يجب أن يتم فيه إصدار بند مبيعات واحد أو أكثر يدويا إلى المستودع من صفحة الإصدار إلى المستودع، ويجب تجاوز نهج دمج الشحنات المحدد بواسطة النظام قبل الإصدار.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 96f994e9f3440721105545f96d7d8475fcab2b6b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016783"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="68034-103">دمج الشحنات عند تجاوز سياسة دمج الشحنات من صفحة الإصدار إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="68034-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68034-104">يقدم هذا الموضوع سيناريو يجب أن يتم فيه إصدار بند مبيعات واحد أو أكثر يدويا إلى المستودع من صفحة **الإصدار إلى المستودع** ، ويجب تجاوز نهج دمج الشحنات المحدد بواسطة النظام قبل الإصدار.</span><span class="sxs-lookup"><span data-stu-id="68034-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="68034-105">قد يكون تجاوز نهج دمج الشحنات مطلوبًا، إذا كان الأمر، على سبيل المثال، الذي لم يتم دمجه عادة مع الشحنات المفتوحة يلزم دمجه مع شحنات مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="68034-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="68034-106">أثناء السيناريو، ستقوم بإنشاء مجموعة من أوامر المبيعات ثم تجاوز نهج دمج الشحنات الافتراضية قبل إصدار الأوامر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="68034-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="68034-107">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="68034-107">Make demo data available</span></span>

<span data-ttu-id="68034-108">يشير السيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="68034-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="68034-109">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="68034-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="68034-110">إعداد نُهج دمج الشحنات وعوامل تصفيه المنتجات</span><span class="sxs-lookup"><span data-stu-id="68034-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="68034-111">يفترض السيناريو الموضح هنا أنك قمت بالفعل بتشغيل الميزة، ونفذت التمرينات في [تكوين نهج دمج الشحنات](configure-shipment-consolidation-policies.md)، وإنشاء النهج والسجلات الأخرى التي تم وصفها هناك.</span><span class="sxs-lookup"><span data-stu-id="68034-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="68034-112">تأكد من تنفيذ تلك التمرينات قبل المتابعة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="68034-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="68034-113">إنشاء أوامر مبيعات لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="68034-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="68034-114">انتقل إلى **الحسابات المدينة \> أوامر المبيعات \> جميع أوامر المبيعات** وقم بإنشاء ثلاثة أوامر مبيعات متماثلة تتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="68034-114">Go to **Accounts receivable \> Orders \> All sales orders** , and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="68034-115">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="68034-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="68034-116">أضف بند أمر يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="68034-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="68034-117">**رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)</span><span class="sxs-lookup"><span data-stu-id="68034-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="68034-118">**الكمية:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="68034-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="68034-119">حدد **المخزون \> حجز** ، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="68034-119">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="68034-120">إصدار أوامر المبيعات من صفحة الإصدار إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="68034-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="68034-121">اتبع الخطوات التالية لتجاوز نهج دمج الشحنات أثناء الإصدار إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="68034-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="68034-122">انتقل إلى **إدارة المستودعات \> الإصدار إلى المستودع \> الإصدار إلى المستودع**.</span><span class="sxs-lookup"><span data-stu-id="68034-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="68034-123">في الجزء العلوي، حدد أمر المبيعات الأول الذي قمت بإنشائه لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="68034-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="68034-124">حدد **إضافة** لإضافة البند إلى الإصدار إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="68034-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="68034-125">لاحظ أنه تم تطبيق نهج دمج الشحنات *الافتراضي* في الجزء السفلي.</span><span class="sxs-lookup"><span data-stu-id="68034-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="68034-126">في الجزء السفلي، حدد **تحديد نهج دمج شحنات جديد**.</span><span class="sxs-lookup"><span data-stu-id="68034-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="68034-127">حدد نهجًا يسمح بالدمج مع الشحنات المفتوحة الأخرى لنفس النهج.</span><span class="sxs-lookup"><span data-stu-id="68034-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="68034-128">على سبيل المثال، حدد نهج *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="68034-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="68034-129">حدد **الإصدار إلى المستودع**.</span><span class="sxs-lookup"><span data-stu-id="68034-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="68034-130">حدد أمر المبيعات الثاني والثالث الذي قمت بإنشائه لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="68034-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="68034-131">حدد **إضافة** لإضافة البنود إلى الإصدار إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="68034-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="68034-132">لاحظ أنه تم تطبيق النهج *الافتراضي* في الجزء السفلي.</span><span class="sxs-lookup"><span data-stu-id="68034-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="68034-133">حدد البند الثاني، ثم في حقل **تحديد نهج دمج الشحنات الجديد** ، حدد نهج *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="68034-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="68034-134">حدد **الإصدار إلى المستودع** لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="68034-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="68034-135">التحقق من الشحنات</span><span class="sxs-lookup"><span data-stu-id="68034-135">Verify the shipments</span></span>

<span data-ttu-id="68034-136">ينبغي أن يتم إنشاء شحنتين:</span><span class="sxs-lookup"><span data-stu-id="68034-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="68034-137">تحتوي الشحنة الأولى على بندين وتم إنشاؤها باستخدام نهج دمج الشحنات *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="68034-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="68034-138">تحتوي الشحنة الثاني على بند واحد وتم إنشاؤها باستخدام نهج دمج الشحنات *الافتراضي*.</span><span class="sxs-lookup"><span data-stu-id="68034-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="68034-139">اتبع هذه الخطوات لمراجعة الشحنات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="68034-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="68034-140">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="68034-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="68034-141">ابحث عن الشحنة المطلوبة وحددها.</span><span class="sxs-lookup"><span data-stu-id="68034-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="68034-142">في حقل **نهج دمج الشحنات** ، رجع نهج الدمج الذي تم استخدامه عند إنشاء الشحنة.</span><span class="sxs-lookup"><span data-stu-id="68034-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68034-143">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="68034-143">Additional resources</span></span>

- [<span data-ttu-id="68034-144">سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="68034-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="68034-145">تكوين نُهج دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="68034-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)