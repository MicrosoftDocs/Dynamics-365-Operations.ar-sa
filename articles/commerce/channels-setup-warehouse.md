---
title: إعداد مستودع
description: يصف هذا الموضوع كيفية إعداد مستودع لاستخدامه مع قناة جديدة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800485"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="8f4b5-103">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="8f4b5-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f4b5-104">يصف هذا الموضوع كيفية إعداد مستودع لاستخدامه مع قناة جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8f4b5-105">تحتاج كل قناة تجارية إلى مستودع مكوّن يرتبط بها.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="8f4b5-106">توفر الإجراءات التالية الحد الأدنى من التكوين المطلوب لإعداد مستودع لقناة تجارية.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="8f4b5-107">لمزيد من المعلومات حول إعداد المستودع، راجع [نظرة عامة حول إدارة المستودعات](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="8f4b5-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="8f4b5-108">تكوين موقع مستودع</span><span class="sxs-lookup"><span data-stu-id="8f4b5-108">Configure a warehouse site</span></span>

<span data-ttu-id="8f4b5-109">قبل إعداد مستودع، يجب تكوين موقع مستودع.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="8f4b5-110">لتكوين موقع مستودع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="8f4b5-111">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="8f4b5-112">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8f4b5-113">في حقل **الموقع**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="8f4b5-114">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="8f4b5-115">في القسم **عام**، قم بتعيين **المنطقة الزمنية** المناسبة.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="8f4b5-116">في حقل **العناوين**، أدخل عنوانًا.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="8f4b5-117">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8f4b5-118">تعرض الصورة التالية مثالاً لموقع مستودع.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-118">The following image shows an example warehouse site.</span></span>

![مثال عن موقع مستودع](media/warehouse-site.png)

## <a name="set-up-a-warehouse&quot;></a><span data-ttu-id=&quot;8f4b5-120&quot;>إعداد مستودع</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-120&quot;>Set up a warehouse</span></span>

<span data-ttu-id=&quot;8f4b5-121&quot;>لإعداد مستودع، اتبع هذه الخطوات.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-121&quot;>To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id=&quot;8f4b5-122&quot;>في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المستودعات**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-122&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id=&quot;8f4b5-123&quot;>في جزء الإجراءات، حدد **جديد**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-123&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;8f4b5-124&quot;>في حقل **المستودع**، أدخل قيمة.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-124&quot;>In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id=&quot;8f4b5-125&quot;>إذا كان هذا عبارة عن تعيين 1:1 لمتجر، فيمكنك استخدام اسم المتجر أو اسم مركز توزيع إقليمي.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-125&quot;>If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id=&quot;8f4b5-126&quot;>في حقل **الاسم**، أدخل قيمة.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-126&quot;>In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id=&quot;8f4b5-127&quot;>في القائمة المنسدلة **الموقع**، حدد موقع المستودع الذي تم إنشاؤها في وقت سابق.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-127&quot;>In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id=&quot;8f4b5-128&quot;>في حقل **النوع**، حدد **افتراضي**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-128&quot;>In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id=&quot;8f4b5-129&quot;>إذا أردت تعيين **مخزن فحص‬**، فستحتاج أولاً إلى اتباع هذه الخطوات لإنشاء مستودع إضافي حيث تم تعيين **النوع** إلى **العزل**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-129&quot;>If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id=&quot;8f4b5-130&quot;>إذا أردت تعيين **مخزن بضاعة بالطريق‬‬**، فستحتاج أولاً إلى اتباع هذه الخطوات لإنشاء مستودع إضافي حيث تم تعيين **النوع** إلى **عابر‬**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-130&quot;>If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id=&quot;8f4b5-131&quot;>في جزء الإجراءات، حدد **حفظ**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-131&quot;>On the action pane, select **Save**.</span></span>

## <a name=&quot;set-up-inventory-aisles&quot;></a><span data-ttu-id=&quot;8f4b5-132&quot;>إعداد ممرات المخزون</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-132&quot;>Set up inventory aisles</span></span>

<span data-ttu-id=&quot;8f4b5-133&quot;>لإعداد ممرات المخزون، اتبع هذه الخطوات:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-133&quot;>To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id=&quot;8f4b5-134&quot;>في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> إعداد الموقع \> ممرات المخزون**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-134&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id=&quot;8f4b5-135&quot;>في جزء الإجراءات، حدد **جديد**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-135&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;8f4b5-136&quot;>في القائمة المنسدلة **المستودع**، حدد المستودع الذي تم إنشاؤها في وقت سابق.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f4b5-136&quot;>In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id=&quot;8f4b5-137&quot;>في حقل **الممر**، أدخل اسمًا (على سبيل المثال، &quot;Def").</span><span class="sxs-lookup"><span data-stu-id="8f4b5-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="8f4b5-138">في حقل **الاسم**، أدخل اسمًا (على سبيل المثال، "ممر افتراضي").</span><span class="sxs-lookup"><span data-stu-id="8f4b5-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="8f4b5-139">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="8f4b5-140">إعداد مواقع مخزون المستودع</span><span class="sxs-lookup"><span data-stu-id="8f4b5-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="8f4b5-141">لإعداد مواقع مخزون المستودع للمخزون القياسي والتالف والمرتجع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="8f4b5-142">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="8f4b5-143">حدد المستودع الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="8f4b5-144">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="8f4b5-145">في جزء الإجراءات، حدد **المستودع**، ثم حدد **موقع المخزون**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="8f4b5-146">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-146">On the action pane, select **New**.</span></span> <span data-ttu-id="8f4b5-147">يجب أن تكون القائمة المنسدلة **المستودع** معينة بشكل افتراضي إلى مستودعك الجديد.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="8f4b5-148">في مربع **الممر**، أدخل اسم الممر الذي قمت بتحديده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="8f4b5-149">قم بتعيين **التحديث اليدوي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="8f4b5-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="8f4b5-150">في مربع **الموقع**، أدخل اسم المستودع.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="8f4b5-151">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="8f4b5-152">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="8f4b5-153">يجب أن تكون القائمة المنسدلة **المستودع** معينة بشكل افتراضي إلى مستودعك الجديد.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="8f4b5-154">في مربع **الممر**، أدخل اسم الممر الذي قمت بتحديده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="8f4b5-155">قم بتعيين **التحديث اليدوي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="8f4b5-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="8f4b5-156">في مربع **الموقع**، أدخل "تالف".</span><span class="sxs-lookup"><span data-stu-id="8f4b5-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="8f4b5-157">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="8f4b5-158">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="8f4b5-159">يجب أن تكون القائمة المنسدلة **المستودع** معينة بشكل افتراضي إلى مستودعك الجديد.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="8f4b5-160">في مربع **الممر**، أدخل اسم الممر الذي قمت بتحديده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="8f4b5-161">قم بتعيين **التحديث اليدوي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="8f4b5-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="8f4b5-162">في مربع **الموقع**، أدخل "مرتجعات".</span><span class="sxs-lookup"><span data-stu-id="8f4b5-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="8f4b5-163">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="8f4b5-164">تعرض الصورة التالية إعداد موقع مخزون مستودع سان فرانسيسكو.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![مثال عن إعداد موقع المخزون](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="8f4b5-166">إكمال إعداد المخزون</span><span class="sxs-lookup"><span data-stu-id="8f4b5-166">Complete warehouse setup</span></span>

<span data-ttu-id="8f4b5-167">لإكمال إعداد المخزون، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="8f4b5-168">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="8f4b5-169">حدد المستودع الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="8f4b5-170">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="8f4b5-171">ضمن **إدارة المخزون والمستودعات**:</span><span class="sxs-lookup"><span data-stu-id="8f4b5-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="8f4b5-172">قم بتعيين **موقع الاستلام الافتراضي** إلى الموقع الافتراضي الذي تم إنشاؤه أعلاه.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="8f4b5-173">قم بتعيين **موقع الإصدار الافتراضي** إلى الموقع الافتراضي الذي تم إنشاؤه أعلاه.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="8f4b5-174">ضمن قسم **العناوين**، أدخل عنوان المستودع.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="8f4b5-175">ضمن قسم **البيع بالتجزئة**:</span><span class="sxs-lookup"><span data-stu-id="8f4b5-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="8f4b5-176">في المربع **موقع الإرجاع الافتراضي**، أدخل موقع المرتجعات الذي تم إنشاؤه في السابق.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="8f4b5-177">قم بتعيين **المتجر** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="8f4b5-178">قم بتعيين **الوزن** إلى **1.00**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="8f4b5-179">في المربع **أبعاد المخزون**، أدخل الموقع الافتراضي الذي تم إنشاؤه في السابق.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="8f4b5-180">في قسم **المستودع**، قم بتعيين **مخزون سالب مادي‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="8f4b5-181">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8f4b5-182">تعرض الصورة التالية تفاصيل المستودع الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="8f4b5-182">The following image shows details for a configured warehouse.</span></span>

![مثال عن مستودع مكوّن](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="8f4b5-184">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8f4b5-184">Additional resources</span></span>

[<span data-ttu-id="8f4b5-185">نظرة عامة على إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="8f4b5-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="8f4b5-186">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="8f4b5-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8f4b5-187">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="8f4b5-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="8f4b5-188">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8f4b5-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="8f4b5-189">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8f4b5-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="8f4b5-190">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="8f4b5-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
