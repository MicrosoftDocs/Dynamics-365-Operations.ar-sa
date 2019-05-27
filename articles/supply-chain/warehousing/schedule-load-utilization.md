---
title: جدولة استغلال الحِمل
description: يشرح هذا الموضوع كيفية إعداد وجدولة التحميل لمستودع.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15f3735f79671ac41789d39a5473722a5f35fde0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564822"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="41bcb-103">جدولة استغلال الحِمل</span><span class="sxs-lookup"><span data-stu-id="41bcb-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="41bcb-104">يمكنك جدولة استغلال الحِمل‬ لأنواع الموقع المحددة، ويمكنك أيضًا توقع استغلال الأحمال الحالية والمستقبلية.</span><span class="sxs-lookup"><span data-stu-id="41bcb-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="41bcb-105">ويمكنك توقع الحِمل لواحد أو أكثر من المواقع، لوحدات الحِمل (المستودع أو المنطقة)، أو لمجموعة مكونة من المنطقة والمستودع.</span><span class="sxs-lookup"><span data-stu-id="41bcb-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="41bcb-106">جدولة حِمل مستودع أو موقع وعرضه</span><span class="sxs-lookup"><span data-stu-id="41bcb-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="41bcb-107">لجدولة الحِمل للمواقع أو المستودعات أو المناطق، يتوجب عليك إنشاء إعداد لاستخدام المساحة وإقرانها بالخطة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="41bcb-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="41bcb-108">في إعداد استخدام المساحة، يمكنك استخدام أنواع المواقع، مثل **موقع المجموعة** و **موقع انتقاء**، لتحديد كيف ينبغي توقع استخدام المساحة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="41bcb-109">كما يتوجب عليك أيضًا تحديد وضع حِمل التخزين، مثل **المنطقة**.</span><span class="sxs-lookup"><span data-stu-id="41bcb-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="41bcb-110">ويبنى توقع الاستخدام المستقبلي للمساحة على المعلومات المحسوبة على الخطة الرئيسية المقترنة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="41bcb-111">وتتنبا الخطة الرئيسية بتخطيط الموارد للأوامر الواردة والصادرة للإنتاج والعمليات.</span><span class="sxs-lookup"><span data-stu-id="41bcb-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="41bcb-112">ويبنى توقع المساحة المتوفرة على العلاقة بين إعداد استخدام المساحة والخطة الرئيسية المحددة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="41bcb-113">باستخدام وضع تحميل التخزين الذي قمت بتحديده في إعداد استخدام المساحة، يمكنك تحديد ما إذا كان الحِمل ينبغي أن يتم توقعه لكل مستودع أو منطقة، أو ما إذا كانت التوقعات ينبغي أن تتضمن معلومات حول كل من المستودعات والمناطق.</span><span class="sxs-lookup"><span data-stu-id="41bcb-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="41bcb-114">يمكنك أيضًا تحديد ما إذا كانت المواقع المحظورة ينبغي أن يتم استبعادها من حساب استغلال الحِمل أم لا.</span><span class="sxs-lookup"><span data-stu-id="41bcb-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="41bcb-115">يمكنك توقع استخدام المساحة عن طريق إنشاء تقرير **استغلال حمل المستودع**.</span><span class="sxs-lookup"><span data-stu-id="41bcb-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="41bcb-116">عندما تقوم بإنشاء هذا التقرير، يمكنك تحديد ما إذا كان استغلال الحِمل ينبغي توقعه لكل موقع أو عبر المواقع أو لوحدة الحِمل المحددة، مثل المنطقة أو المستودع.</span><span class="sxs-lookup"><span data-stu-id="41bcb-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="41bcb-117">إنشاء إعداد استخدام المساحة لمستودع</span><span class="sxs-lookup"><span data-stu-id="41bcb-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="41bcb-118">حدد **إدارة المخزون** \> **الإعداد** \> **مراقبة المستودع** \> **استخدام المساحة**.</span><span class="sxs-lookup"><span data-stu-id="41bcb-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="41bcb-119">حدد **جديد** لإنشاء إعداد استخدام مساحة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="41bcb-120">حدد معرفًا واسمًا للإعداد الجديد.</span><span class="sxs-lookup"><span data-stu-id="41bcb-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="41bcb-121">في الحقل **وضع تحميل التخزين**، حدد ما إذا كانت النظرة العامة لاستخدام المساحة ينبغي أن تظهر المعلومات حسب المستودع أو المنطقة أو المستودع والمنطقة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="41bcb-122">قم بتعيين خيار **‏‫استبعاد المواقع المحظورة‬** على **نعم** لاستبعاد مواقع المخزون المحظورة من حساب المساحة المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="41bcb-123">ويمكنك حظر موقع مخزون للإدخال والإخراج عن طريق تحديد سبب حظر للموقع في حقل **تم تأمين الإدخال** أو **تم تأمين الإخراج** في علامة التبويب السريعة **أخرى** في صفحة **مواقع المخزون**.</span><span class="sxs-lookup"><span data-stu-id="41bcb-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="41bcb-124">في علامة التبويب السريعة **نوع الموقع**، حدد أنواع المواقع المراد تضمينها في حساب استخدام المساحة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="41bcb-125">يجب عليك تحديد نوع موقع واحد على الأقل للتوقع.</span><span class="sxs-lookup"><span data-stu-id="41bcb-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="41bcb-126">إقران إعداد استخدام مساحة بخطة رئيسية</span><span class="sxs-lookup"><span data-stu-id="41bcb-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="41bcb-127">حدد **إدارة المخزون** \> **مهام دورية** \> **جدولة استغلال الحمل**.</span><span class="sxs-lookup"><span data-stu-id="41bcb-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="41bcb-128">في الحقل **الخطة الرئيسية**، حدد خطة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="41bcb-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="41bcb-129">في الحقل **عدد الأيام**، حدد عدد الأيام المراد تضمينها في توقع أحمال العمل الحالية والمستقبلية.</span><span class="sxs-lookup"><span data-stu-id="41bcb-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="41bcb-130">في الحقل **استخدام المساحة**، حدد إعداد استخدام المساحة المراد استخدامه لتوقع أحمال العمل الحالية والمستقبلية.</span><span class="sxs-lookup"><span data-stu-id="41bcb-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="41bcb-131">تحديد توقع استخدام الحِمل وعرض المعلومات</span><span class="sxs-lookup"><span data-stu-id="41bcb-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="41bcb-132">حدد **إدارة المخزون** \> **الاستعلامات والتقارير** \> **تقارير المخزون الفعلي‬** \> **استغلال حمل المستودع**.</span><span class="sxs-lookup"><span data-stu-id="41bcb-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="41bcb-133">في الحقل **إظهار حسب**، حدد مستوى توقع استخدام المساحة:</span><span class="sxs-lookup"><span data-stu-id="41bcb-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="41bcb-134">**الموقع** – توقع استخدام المساحة لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="41bcb-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="41bcb-135">ويكون هذا التوقع مفيدًا، إذا كنت تريد عرض جميع المستودعات لأحد المواقع حتى تتمكن من موازنة استخدام المساحة بين المستودعات.</span><span class="sxs-lookup"><span data-stu-id="41bcb-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="41bcb-136">**وحدة الحمل** – توقع استخدام المساحة للمناطق أو المستودعات.</span><span class="sxs-lookup"><span data-stu-id="41bcb-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="41bcb-137">بعد ذلك يتم توقع المساحة المتوفرة طبقاً للقيمة التي قمت بتحديدها في الحقل **وضع تحميل التخزين** في صفحة **استخدام المساحة** عندما قمت بإنشاء إعداد استخدام المساحة.</span><span class="sxs-lookup"><span data-stu-id="41bcb-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="41bcb-138">اتبع إحدى الخطوات التالية، استناداً إلى القيمة التي قمت بتحديدها في الخطوة السابقة:</span><span class="sxs-lookup"><span data-stu-id="41bcb-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="41bcb-139">إذا قمت بتحديد **الموقع** في حقل **إظهار حسب**، يكون حقل **الموقع** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="41bcb-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="41bcb-140">حدد واحدًا أو أكثر من المواقع التي تريد تضمينها في التوقع.</span><span class="sxs-lookup"><span data-stu-id="41bcb-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="41bcb-141">إذا قمت بتحديد **وحدة الحمل** في حقل **إظهار حسب**، يكون حقل **وحدة الحمل** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="41bcb-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="41bcb-142">حدد وحدة الحِمل.</span><span class="sxs-lookup"><span data-stu-id="41bcb-142">Select the load unit.</span></span>

4. <span data-ttu-id="41bcb-143">في حقل **نوع الحمل**، حدد **الحجم** أو **الوزن** للإشارة إلى الوحدة التشغيلية للمستودع التي تريد توقع المساحة لها.</span><span class="sxs-lookup"><span data-stu-id="41bcb-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="41bcb-144">في الحقل **إعداد استخدام المساحة**، حدد إعداد استخدام المساحة الذي يجب أن يستند إليه التوقع.</span><span class="sxs-lookup"><span data-stu-id="41bcb-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
