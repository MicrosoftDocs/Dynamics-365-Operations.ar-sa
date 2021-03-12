---
title: جدولة قدرة حمل العمل
description: يشرح هذا الموضوع كيفية إعداد وجدولة قدرة حمل العمل للعاملين في مستودع أو لأحد المستودعات بكامل.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8db243949b2aeee0a8263276234d439652905449
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965567"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="0449d-103">جدولة قدرة حمل العمل</span><span class="sxs-lookup"><span data-stu-id="0449d-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0449d-104">يمكنك جدولة قدرة حمل العمل للمستودعات، ويمكنك توقع أحمال العمل الحالية والمستقبلية للعاملين في المستودعات الفردية.</span><span class="sxs-lookup"><span data-stu-id="0449d-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="0449d-105">يمكنك توقع حمل العمل للمستودع بالكامل، أو توقع حمل العمل بشكل منفصل لأحمال العمل الداخلية والخارجية.</span><span class="sxs-lookup"><span data-stu-id="0449d-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="0449d-106">لتوقع ناتج حمل العمل للمستودعات المحددة، يجب أن تتوفر بيانات الجدولة الرئيسية لتلك المستودعات.</span><span class="sxs-lookup"><span data-stu-id="0449d-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="0449d-107">لمزيد من المعلومات، راجع [نظرة عامة على الخطط الرئيسية](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="0449d-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="0449d-108">جدولة أحمال العمل وعرضها لمستودع</span><span class="sxs-lookup"><span data-stu-id="0449d-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="0449d-109">لجدولة قدرة حمل العمل لمستودع، يجب إنشاء إعداد حمل عمل لمستودع واحد أو أكثر، ثم إقران إعداد حمل العمل بخطة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="0449d-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="0449d-110">في إعداد قدرة حمل العمل، يمكنك تعريف حدود الوزن والحجم للحركات الداخلية والخارجية.</span><span class="sxs-lookup"><span data-stu-id="0449d-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="0449d-111">يمكنك أيضًا إنشاء أكثر من إعداد لكل مستودع وإقران الإعداد بالخطط الرئيسية الفردية.</span><span class="sxs-lookup"><span data-stu-id="0449d-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="0449d-112">على سبيل المثال، يمكنك استخدام هذا الأسلوب لاستيعاب التغيرات الموسمية في العاملين.</span><span class="sxs-lookup"><span data-stu-id="0449d-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="0449d-113">إذا كان العاملون في المستودع يعملون مع الحركات لأحمال العمل الداخلية والخارجية، يمكنك تكوين إعداد قدرة المستودع بحيث يتم توقع حمل العمل في عرض مجمع.</span><span class="sxs-lookup"><span data-stu-id="0449d-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="0449d-114">لجدولة أحمال عمل المستودعات وعرضها، يجب استكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="0449d-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="0449d-115">إنشاء إعداد قدرة حمل عمل وتعريف حدود قدرة حمل العمل لمستودع واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="0449d-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="0449d-116">إقران إعداد قدرة حمل العمل بخطة رئيسية لإنشاء توقعات أحمال عمل وتحديد طول فترة سريان تلك التوقعات.</span><span class="sxs-lookup"><span data-stu-id="0449d-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="0449d-117">إنشاء إعداد قدرة حمل عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="0449d-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="0449d-118">حدد **إدارة المخزون** \> **الإعداد** \> **مراقبة المستودع** \> **قدرة حمل العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="0449d-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="0449d-119">في جزء الإجراءات، حدد **جديد** لإنشاء إعداد قدرة حمل عمل.</span><span class="sxs-lookup"><span data-stu-id="0449d-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="0449d-120">في علامة التبويب الجديد **المستودعات**، حدد **جديد**، ثم أدخل القيم في البند لإقران المستودع بإعداد قدرة حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="0449d-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="0449d-121">حدد خانة الاختيار **حمل العمل الداخلي والخارجي المجمع‬** إذا كان تقرير **قدرة حمل العمل** يجب أن يظهر حمل العمل الإجمالي للحركات الواردة والصادرة في طريقة عرض واحدة.</span><span class="sxs-lookup"><span data-stu-id="0449d-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="0449d-122">في علامة التبويب السريعة **أنواع الحركات**، حدد أنواع الحركات الداخلية والخارجية التي ينطبق عليها حدود حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="0449d-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0449d-123">يجب تحديد نوع حركة واحد على الأقل لكل من حمل العمل الداخلي وحمل العمل الخارجي.</span><span class="sxs-lookup"><span data-stu-id="0449d-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="0449d-124">تحديد الحدود للحجم أو الوزن</span><span class="sxs-lookup"><span data-stu-id="0449d-124">Define limits for volume or weight</span></span>

<span data-ttu-id="0449d-125">يمكنك إعداد حدود الحجم أو الوزن، تبعًا للقيد ذي الصلة بعاملي المستودع.</span><span class="sxs-lookup"><span data-stu-id="0449d-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="0449d-126">يتم تضمين الحدود التي تحددها في توقع قدرة حمل العمل التي يمكن عرضها في تقرير **قدرة حمل العمل**.</span><span class="sxs-lookup"><span data-stu-id="0449d-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="0449d-127">لتوقع المعلومات حول حجم ووزن الأصناف، يجب تحديد نوع الحجم القياسي لأحد أصناف المخزون ووزن أحد أصناف المخزون لكل المنتجات.</span><span class="sxs-lookup"><span data-stu-id="0449d-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="0449d-128">تتوفر الحقول المطلوبة في مجموعات الحقول التالية في علامة التبويب السريعة **إدارة المخزون** في صفحة **تفاصيل المنتج الذي تم إصداره‬**:</span><span class="sxs-lookup"><span data-stu-id="0449d-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="0449d-129">معالجة</span><span class="sxs-lookup"><span data-stu-id="0449d-129">Handling</span></span>
- <span data-ttu-id="0449d-130">أبعاد فعلية</span><span class="sxs-lookup"><span data-stu-id="0449d-130">Physical dimensions</span></span>
- <span data-ttu-id="0449d-131">قياسات الوزن</span><span class="sxs-lookup"><span data-stu-id="0449d-131">Weight measurements</span></span>

<span data-ttu-id="0449d-132">في حالة عدم تحديد هذه المعلومات بشكل صحيح، ستتلقى رسالة عند إنشاء تقرير **قدرة حمل العمل**.</span><span class="sxs-lookup"><span data-stu-id="0449d-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="0449d-133">من التقرير، يمكنك بعد ذلك التنقل لأسفل لتحديد المعلومات المفقودة التي تكون مطلوب من أجل توقع حمل العمل المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="0449d-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="0449d-134">إقران إعداد قدرة حمل عمل بخطة رئيسية</span><span class="sxs-lookup"><span data-stu-id="0449d-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="0449d-135">حدد **إدارة المخزون** \> **دوري** \> **جدولة حمل العمل**.</span><span class="sxs-lookup"><span data-stu-id="0449d-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="0449d-136">في حقل **الخطة الرئيسية**، حدد الخطة الرئيسية المطلوب استخدامها لتوقعات حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="0449d-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="0449d-137">في حقل **عدد الأيام**، حدد عدد الأيام التي يغطيها توقع حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="0449d-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="0449d-138">في حقل **حمل العمل**، حدد إعداد حمل العمل لإقرانه بالخطة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="0449d-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="0449d-139">عرض حمل العمل</span><span class="sxs-lookup"><span data-stu-id="0449d-139">View workload capacity</span></span>

1. <span data-ttu-id="0449d-140">حدد **إدارة المخزون** \> **الاستعلامات والتقارير** \> **تقارير المخزون الفعلي‬** \> **قدرة حمل العمل**.</span><span class="sxs-lookup"><span data-stu-id="0449d-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="0449d-141">في حقل **عدد الأعمدة**، حدد عدد الأعمدة المطلوب عرضه في التقرير.</span><span class="sxs-lookup"><span data-stu-id="0449d-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="0449d-142">في حقل **نوع الأمر**، حدد **مخطط ومؤكد‬**، أو **المخطط**، أو **مؤكد** للإشارة إلى نوع الأوامر المراد توقعها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="0449d-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="0449d-143">في حقل **نوع الحمل**، حدد نوع الحمل المطلوب تحديده في حالة ضرورة توقع قدرة حمل العمل للحجم والوزن.</span><span class="sxs-lookup"><span data-stu-id="0449d-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="0449d-144">في حقل **قدرة حمل العمل**، حدد إعداد قدرة حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="0449d-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
