---
title: إعداد مستودع
description: يصف هذا الموضوع كيفية إعداد مستودع لاستخدامه مع قناة جديدة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9ba12876a8c8f841733d8ec49c33e900211c4ab4
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057846"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="72ac0-103">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="72ac0-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="72ac0-104">يصف هذا الموضوع كيفية إعداد مستودع لاستخدامه مع قناة جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="72ac0-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="72ac0-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="72ac0-105">Overview</span></span>

<span data-ttu-id="72ac0-106">تحتاج كل قناة تجارية إلى مستودع مكوّن يرتبط بها.</span><span class="sxs-lookup"><span data-stu-id="72ac0-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="72ac0-107">توفر الإجراءات التالية الحد الأدنى من التكوين المطلوب لإعداد مستودع لقناة تجارية.</span><span class="sxs-lookup"><span data-stu-id="72ac0-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="72ac0-108">لمزيد من المعلومات حول إعداد المستودع، راجع [نظرة عامة حول إدارة المستودعات](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span><span class="sxs-lookup"><span data-stu-id="72ac0-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="72ac0-109">تكوين موقع مستودع</span><span class="sxs-lookup"><span data-stu-id="72ac0-109">Configure a warehouse site</span></span>

<span data-ttu-id="72ac0-110">قبل إعداد مستودع، يجب تكوين موقع مستودع.</span><span class="sxs-lookup"><span data-stu-id="72ac0-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="72ac0-111">لتكوين موقع مستودع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="72ac0-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="72ac0-112">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="72ac0-113">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="72ac0-114">في حقل **الموقع**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="72ac0-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="72ac0-115">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="72ac0-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="72ac0-116">في القسم **عام**، قم بتعيين **المنطقة الزمنية** المناسبة.</span><span class="sxs-lookup"><span data-stu-id="72ac0-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="72ac0-117">في حقل **العناوين**، أدخل عنوانًا.</span><span class="sxs-lookup"><span data-stu-id="72ac0-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="72ac0-118">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="72ac0-119">تعرض الصورة التالية مثالاً لموقع مستودع.</span><span class="sxs-lookup"><span data-stu-id="72ac0-119">The following image shows an example warehouse site.</span></span>

![مثال عن موقع مستودع](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="72ac0-121">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="72ac0-121">Set up a warehouse</span></span>

<span data-ttu-id="72ac0-122">لإعداد مستودع، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="72ac0-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="72ac0-123">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="72ac0-124">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="72ac0-125">في حقل **المستودع**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="72ac0-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="72ac0-126">إذا كان هذا عبارة عن تعيين 1:1 لمتجر، فيمكنك استخدام اسم المتجر أو اسم مركز توزيع إقليمي.</span><span class="sxs-lookup"><span data-stu-id="72ac0-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="72ac0-127">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="72ac0-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="72ac0-128">في القائمة المنسدلة **الموقع**، حدد موقع المستودع الذي تم إنشاؤها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="72ac0-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="72ac0-129">في حقل **النوع**، حدد **افتراضي**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="72ac0-130">إذا أردت تعيين **مخزن فحص‬**، فستحتاج أولاً إلى اتباع هذه الخطوات لإنشاء مستودع إضافي حيث تم تعيين **النوع** إلى **العزل**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="72ac0-131">إذا أردت تعيين **مخزن بضاعة بالطريق‬‬**، فستحتاج أولاً إلى اتباع هذه الخطوات لإنشاء مستودع إضافي حيث تم تعيين **النوع** إلى **عابر‬**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="72ac0-132">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="72ac0-133">إعداد ممرات المخزون</span><span class="sxs-lookup"><span data-stu-id="72ac0-133">Set up inventory aisles</span></span>

<span data-ttu-id="72ac0-134">لإعداد ممرات المخزون، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="72ac0-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="72ac0-135">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> إعداد الموقع \> ممرات المخزون**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="72ac0-136">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="72ac0-137">في القائمة المنسدلة **المستودع**، حدد المستودع الذي تم إنشاؤها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="72ac0-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="72ac0-138">في حقل **الممر**، أدخل اسمًا (على سبيل المثال، "Def").</span><span class="sxs-lookup"><span data-stu-id="72ac0-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="72ac0-139">في حقل **الاسم**، أدخل اسمًا (على سبيل المثال، "ممر افتراضي").</span><span class="sxs-lookup"><span data-stu-id="72ac0-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="72ac0-140">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="72ac0-141">إعداد مواقع مخزون المستودع</span><span class="sxs-lookup"><span data-stu-id="72ac0-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="72ac0-142">لإعداد مواقع مخزون المستودع للمخزون القياسي والتالف والمرتجع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="72ac0-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="72ac0-143">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="72ac0-144">حدد المستودع الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="72ac0-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="72ac0-145">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="72ac0-146">في جزء الإجراءات، حدد **المستودع**، ثم حدد **موقع المخزون**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="72ac0-147">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-147">On the action pane, select **New**.</span></span> <span data-ttu-id="72ac0-148">يجب أن تكون القائمة المنسدلة **المستودع** معينة بشكل افتراضي إلى مستودعك الجديد.</span><span class="sxs-lookup"><span data-stu-id="72ac0-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="72ac0-149">في مربع **الممر**، أدخل اسم الممر الذي قمت بتحديده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="72ac0-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="72ac0-150">قم بتعيين **التحديث اليدوي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="72ac0-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="72ac0-151">في مربع **الموقع**، أدخل اسم المستودع.</span><span class="sxs-lookup"><span data-stu-id="72ac0-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="72ac0-152">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="72ac0-153">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="72ac0-154">يجب أن تكون القائمة المنسدلة **المستودع** معينة بشكل افتراضي إلى مستودعك الجديد.</span><span class="sxs-lookup"><span data-stu-id="72ac0-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="72ac0-155">في مربع **الممر**، أدخل اسم الممر الذي قمت بتحديده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="72ac0-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="72ac0-156">قم بتعيين **التحديث اليدوي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="72ac0-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="72ac0-157">في مربع **الموقع**، أدخل "تالف".</span><span class="sxs-lookup"><span data-stu-id="72ac0-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="72ac0-158">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="72ac0-159">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="72ac0-160">يجب أن تكون القائمة المنسدلة **المستودع** معينة بشكل افتراضي إلى مستودعك الجديد.</span><span class="sxs-lookup"><span data-stu-id="72ac0-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="72ac0-161">في مربع **الممر**، أدخل اسم الممر الذي قمت بتحديده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="72ac0-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="72ac0-162">قم بتعيين **التحديث اليدوي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="72ac0-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="72ac0-163">في مربع **الموقع**، أدخل "مرتجعات".</span><span class="sxs-lookup"><span data-stu-id="72ac0-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="72ac0-164">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="72ac0-165">تعرض الصورة التالية إعداد موقع مخزون مستودع سان فرانسيسكو.</span><span class="sxs-lookup"><span data-stu-id="72ac0-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![مثال عن إعداد موقع المخزون](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="72ac0-167">إكمال إعداد المخزون</span><span class="sxs-lookup"><span data-stu-id="72ac0-167">Complete warehouse setup</span></span>

<span data-ttu-id="72ac0-168">لإكمال إعداد المخزون، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="72ac0-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="72ac0-169">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="72ac0-170">حدد المستودع الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="72ac0-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="72ac0-171">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="72ac0-172">ضمن **إدارة المخزون والمستودعات**:</span><span class="sxs-lookup"><span data-stu-id="72ac0-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="72ac0-173">قم بتعيين **موقع الاستلام الافتراضي** إلى الموقع الافتراضي الذي تم إنشاؤه أعلاه.</span><span class="sxs-lookup"><span data-stu-id="72ac0-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="72ac0-174">قم بتعيين **موقع الإصدار الافتراضي** إلى الموقع الافتراضي الذي تم إنشاؤه أعلاه.</span><span class="sxs-lookup"><span data-stu-id="72ac0-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="72ac0-175">ضمن قسم **العناوين**، أدخل عنوان المستودع.</span><span class="sxs-lookup"><span data-stu-id="72ac0-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="72ac0-176">ضمن قسم **البيع بالتجزئة**:</span><span class="sxs-lookup"><span data-stu-id="72ac0-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="72ac0-177">في المربع **موقع الإرجاع الافتراضي**، أدخل موقع المرتجعات الذي تم إنشاؤه في السابق.</span><span class="sxs-lookup"><span data-stu-id="72ac0-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="72ac0-178">قم بتعيين **المتجر** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="72ac0-179">قم بتعيين **الوزن** إلى **1.00**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="72ac0-180">في المربع **أبعاد المخزون**، أدخل الموقع الافتراضي الذي تم إنشاؤه في السابق.</span><span class="sxs-lookup"><span data-stu-id="72ac0-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="72ac0-181">في قسم **المستودع**، قم بتعيين **مخزون سالب مادي‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="72ac0-182">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72ac0-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="72ac0-183">تعرض الصورة التالية تفاصيل المستودع الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="72ac0-183">The following image shows details for a configured warehouse.</span></span>

![مثال عن مستودع مكوّن](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="72ac0-185">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="72ac0-185">Additional resources</span></span>

[<span data-ttu-id="72ac0-186">نظرة عامة على إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="72ac0-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="72ac0-187">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="72ac0-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="72ac0-188">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="72ac0-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="72ac0-189">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="72ac0-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="72ac0-190">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="72ac0-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="72ac0-191">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="72ac0-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





