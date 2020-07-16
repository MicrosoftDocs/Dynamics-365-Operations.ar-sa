---
title: توزيع البضائع المخطط
description: يصف هذا الموضوع توزيع البضائع المخطط المتقدم، حيث يتم توجيه كمية المخزون المطلوبة لأمر ما بشكل مستقيم من الاستلام أو الإنشاء إلى المساحة الخارجية الصحيحة أو ناحية الإعداد. ويتم توجيه كافة المخزون المتبقي من المصدر الوارد إلى موقع التخزين الصحيح خلال عملية الإبعاد العادية.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: ae805d9aac790a1a58478cf54d033ce758c5eca3
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530088"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="b762d-104">توزيع البضائع المخطط</span><span class="sxs-lookup"><span data-stu-id="b762d-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b762d-105">يصف هذا الموضوع توزيع البضائع المخطط المتقدم.</span><span class="sxs-lookup"><span data-stu-id="b762d-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="b762d-106">توزيع البضائع هو إحدى عمليات المستودع، حيث يتم توجيه كمية المخزون المطلوبة لأمر ما بشكل مستقيم من الاستلام أو الإنشاء إلى المساحة الخارجية الصحيحة أو ناحية الإعداد.</span><span class="sxs-lookup"><span data-stu-id="b762d-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="b762d-107">ويتم توجيه كافة المخزون المتبقي من المصدر الوارد إلى موقع التخزين الصحيح خلال عملية الإبعاد العادية.</span><span class="sxs-lookup"><span data-stu-id="b762d-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="b762d-108">يتيح توزيع البضائع للعاملين تخطي الإبعاد الوارد الانتقاء الصادر للمخزون الذي تم وضع علامة عليه بالفعل لأمر صادر.</span><span class="sxs-lookup"><span data-stu-id="b762d-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="b762d-109">لذلك، يتم تقليل عدد مرات لمس المخزون، قدر الإمكان.</span><span class="sxs-lookup"><span data-stu-id="b762d-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="b762d-110">بالإضافة إلى ذلك، بسبب وجود تفاعل أقل مع النظام، تزداد توفيرات الوقت والمساحة على أرضية صالة المستودع.</span><span class="sxs-lookup"><span data-stu-id="b762d-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="b762d-111">قبل تشغيل توزيع البضائع، يجب أن يقوم المستخدم بتكوين قالب توزيع بضائع جديد حيث يتم تحديد مصدر التوريد والمجموعات الأخرى من المتطلبات لتوزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="b762d-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="b762d-112">وبمجرد إنشاء الأمر الصادر، يجب وضع علامة على البند في مقابل أمر وارد يحتوي على نفس الصنف.</span><span class="sxs-lookup"><span data-stu-id="b762d-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="b762d-113">وفي وقت استلام الأمر الوارد، يقوم إعداد توزيع البضائع تلقائيا بتحديد الحاجة إلى توزيع البضائع وينشئ عمل الحركة للكمية المطلوبة، استنادا إلى إعداد توجيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="b762d-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="b762d-114">و**لا** يتم إلغاء تسجيل حركات المخزون عندما يتم إلغاء عمل توزيع البضائع، حتى في حالة تشغيل إعداد هذه الإمكانية في معلمات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="b762d-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="b762d-115">تشغيل ميزة توزيع البضائع المخططة</span><span class="sxs-lookup"><span data-stu-id="b762d-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="b762d-116">لكي تتمكن من استخدام توزيع البضائع المخطط، يجب تشغيل الميزة في النظام.</span><span class="sxs-lookup"><span data-stu-id="b762d-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="b762d-117">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b762d-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b762d-118">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b762d-119">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="b762d-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b762d-120">**اسم الميزة:** *توزيع البضائع المخطط*</span><span class="sxs-lookup"><span data-stu-id="b762d-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="b762d-121">الإعداد</span><span class="sxs-lookup"><span data-stu-id="b762d-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="b762d-122">إعادة إنشاء طرق ترحيل الحمل</span><span class="sxs-lookup"><span data-stu-id="b762d-122">Regenerate load posting methods</span></span>

<span data-ttu-id="b762d-123">يتم تنفيذ توزيع البضائع المخطط كطريقه لترحيل الحمل.</span><span class="sxs-lookup"><span data-stu-id="b762d-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="b762d-124">بعد تشغيل الميزة، يجب إعادة إنشاء الأساليب.</span><span class="sxs-lookup"><span data-stu-id="b762d-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="b762d-125">انتقل إلى **إدارة المستودعات \> الإعداد \> طرق ترحيل الحمل**.</span><span class="sxs-lookup"><span data-stu-id="b762d-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="b762d-126">في جزء الإجراءات، حدد **طرق إعادة الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="b762d-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="b762d-127">عند اكتمال إعادة الإنشاء، يجب أن تشاهد أسلوب له **اسم أسلوب** بالقيمة *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="b762d-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="b762d-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b762d-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="b762d-129">إنشاء قالب توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="b762d-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="b762d-130">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> قوالب توزيع البضائع**.</span><span class="sxs-lookup"><span data-stu-id="b762d-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="b762d-131">في جزء الإجراءات، حدد **جديد** لإنشاء قالب.</span><span class="sxs-lookup"><span data-stu-id="b762d-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="b762d-132">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="b762d-133">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="b762d-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="b762d-134">يحدد هذا الحقل الترتيب الذي يتم تقييم القوالب باستخدامه.</span><span class="sxs-lookup"><span data-stu-id="b762d-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="b762d-135">**معرف قالب توزيع البضائع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b762d-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="b762d-136">**الوصف:** *المستودع 51*</span><span class="sxs-lookup"><span data-stu-id="b762d-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="b762d-137">**سياسة إصدار الطلب:** *قبل إيصال التوريد*</span><span class="sxs-lookup"><span data-stu-id="b762d-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="b762d-138">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b762d-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b762d-139">يتحكم الإعداد الموجود في علامة التبويب السريعة **التخطيط** في كيفية عمل القالب.</span><span class="sxs-lookup"><span data-stu-id="b762d-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="b762d-140">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-140">Set the following values:</span></span>

    - <span data-ttu-id="b762d-141">**متطلبات الطلب:** *بلا*</span><span class="sxs-lookup"><span data-stu-id="b762d-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="b762d-142">يحدد هذا الحقل متطلبات مخزون الطلب.</span><span class="sxs-lookup"><span data-stu-id="b762d-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="b762d-143">إذا كان يجب ربط الطلب بالتوريد قبل الإصدار، فحدد *وضع علامة*.</span><span class="sxs-lookup"><span data-stu-id="b762d-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="b762d-144">إذا كان يجب حجز الطلب مقابل التوريد قبل الإصدار، فحدد *حجز الأمر*.</span><span class="sxs-lookup"><span data-stu-id="b762d-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="b762d-145">**نوع تحديد الموقع:** *مواقع الشحنة*</span><span class="sxs-lookup"><span data-stu-id="b762d-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="b762d-146">يحدد هذا الحقل ما إذا كان يجب أن يستخدم عمل توزيع البضائع مواقع مرحلية/مواقع حمل من الشحنة، أو ما إذا كان يجب عليه استخدام توجيهات المواقع للعثور على مواقع مرحلية/مواقع حمل خاصة به.</span><span class="sxs-lookup"><span data-stu-id="b762d-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="b762d-147">**قالب العمل:** – اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b762d-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="b762d-148">يحدد هذا الحقل قالب العمل الذي ينبغي استخدامه عند إنشاء عمل توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="b762d-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="b762d-149">**إعادة التحقق عند استلام التوريد:** *لا*</span><span class="sxs-lookup"><span data-stu-id="b762d-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="b762d-150">يحدد هذا الخيار ما إذا كان يجب إعادة التحقق من التوريد أثناء الاستلام أم لا.</span><span class="sxs-lookup"><span data-stu-id="b762d-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="b762d-151">إذا تم تعيين هذا الخيار على *نعم*، فعندئذ يتم تحديد كل من أقصى إطار زمني ونطاق أيام انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="b762d-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="b762d-152">**إطار زمن التحقق من الصحة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="b762d-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="b762d-153">يحدد هذا الخيار ما إذا كان يجب تقييم الحد الأقصى للإطار الزمني عند تحديد مصدر توريد.</span><span class="sxs-lookup"><span data-stu-id="b762d-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="b762d-154">إذا تم تعيين هذا الخيار على *نعم*، ستتوفر الحقول التي ترتبط بالحد الأقصى والأدنى للإطارات الزمنية.</span><span class="sxs-lookup"><span data-stu-id="b762d-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="b762d-155">**أقصى إطار زمني:** *5*</span><span class="sxs-lookup"><span data-stu-id="b762d-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="b762d-156">يحدد هذا الحقل أقصى فترة بين وصول التوريد ومغادرة الطلب.</span><span class="sxs-lookup"><span data-stu-id="b762d-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b762d-157">**وحدة أقصى إطار زمني:** *الأيام*</span><span class="sxs-lookup"><span data-stu-id="b762d-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b762d-158">**أدنى إطار زمني:** *0*</span><span class="sxs-lookup"><span data-stu-id="b762d-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="b762d-159">يحدد هذا الحقل أدنى فترة بين وصول التوريد ومغادرة الطلب.</span><span class="sxs-lookup"><span data-stu-id="b762d-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b762d-160">**وحدة أدنى إطار زمني:** *الأيام*</span><span class="sxs-lookup"><span data-stu-id="b762d-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b762d-161">**نطاق أيام انتهاء الصلاحية:** *0*</span><span class="sxs-lookup"><span data-stu-id="b762d-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="b762d-162">*معيار تاريخ ‏‫‏‫ما تنتهي صلاحيته أولاً يصرف أولاً (FEFO):* يحدد هذا الحقل أقصى عدد للأيام بين تاريخ انتهاء صلاحية دفعة ما تنتهي صلاحيته أولا الموجودة حاليًا في المستودع والدفعة التي يتم استلامها.</span><span class="sxs-lookup"><span data-stu-id="b762d-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="b762d-163">في علامة التبويب السريعة **مصادر التوريد**، حدد أنواع التوريد الصالحة لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="b762d-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="b762d-164">حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="b762d-165">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="b762d-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b762d-166">**مصدر التوريد:** *أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="b762d-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="b762d-167">إنشاء درجة عمل</span><span class="sxs-lookup"><span data-stu-id="b762d-167">Create a work class</span></span>

1. <span data-ttu-id="b762d-168">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="b762d-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b762d-169">في جزء الإجراءات، حدد **جديد** لإنشاء فئة عمل.</span><span class="sxs-lookup"><span data-stu-id="b762d-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="b762d-170">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-170">Set the following values:</span></span>

    - <span data-ttu-id="b762d-171">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b762d-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b762d-172">**الوصف:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="b762d-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="b762d-173">**نوع أمر العمل:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="b762d-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="b762d-174">إنشاء قالب عمل</span><span class="sxs-lookup"><span data-stu-id="b762d-174">Create a work template</span></span>

1. <span data-ttu-id="b762d-175">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="b762d-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b762d-176">قم بتعيين حقل **نوع أمر العمل** إلى *توزيع البضائع*.</span><span class="sxs-lookup"><span data-stu-id="b762d-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b762d-177">في جزء الإجراءات، حدد **جديد** لإضافة سطر إلى علامة تبويب **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="b762d-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="b762d-178">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b762d-179">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="b762d-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b762d-180">**قالب العمل:** *توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="b762d-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="b762d-181">**وصف قالب العمل:** *توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="b762d-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="b762d-182">حدد **حفظ** لجعل علامة التبويب السريعة **تفاصيل قالب العمل** متاحة.</span><span class="sxs-lookup"><span data-stu-id="b762d-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b762d-183">في علامة التبويب السريعة **تفاصيل قالب العمل**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b762d-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b762d-184">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b762d-185">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="b762d-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b762d-186">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b762d-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b762d-187">حدد **جديد** لإضافة سطر آخر، ثم قم بتعيين القيم التالية عليه:</span><span class="sxs-lookup"><span data-stu-id="b762d-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="b762d-188">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="b762d-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b762d-189">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b762d-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b762d-190">حدد **حفظ**، وتأكد من أنه تم تحديد خانة الاختيار **صالح** لقالب *توزيع البضائع 51*.</span><span class="sxs-lookup"><span data-stu-id="b762d-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="b762d-191">يجب أن تكون معرفات فئة العمل لأنواع عمل *الانتقاء* و*الوضع* متطابقة.</span><span class="sxs-lookup"><span data-stu-id="b762d-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="b762d-192">إنشاء توجيات الموقع</span><span class="sxs-lookup"><span data-stu-id="b762d-192">Create location directives</span></span>

1. <span data-ttu-id="b762d-193">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b762d-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b762d-194">في الجزء الأيسر، قم بتعيين حقل **نوع أمر العمل** إلى *توزيع البضائع*.</span><span class="sxs-lookup"><span data-stu-id="b762d-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b762d-195">في جزء الإجراءات، حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="b762d-196">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="b762d-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b762d-197">**الاسم:** *إيداع توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="b762d-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="b762d-198">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="b762d-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b762d-199">**الموقع:** *5*</span><span class="sxs-lookup"><span data-stu-id="b762d-199">**Site:** *5*</span></span>
    - <span data-ttu-id="b762d-200">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b762d-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b762d-201">حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.</span><span class="sxs-lookup"><span data-stu-id="b762d-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b762d-202">في علامة التبويب السريعة **السطور**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b762d-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b762d-203">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b762d-204">**من الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="b762d-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="b762d-205">**إلى الكمية:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="b762d-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="b762d-206">حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="b762d-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b762d-207">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b762d-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b762d-208">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b762d-209">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b762d-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="b762d-210">**استخدام الموقع الثابت:** *المواقع الثابتة وغير الثابتة*</span><span class="sxs-lookup"><span data-stu-id="b762d-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="b762d-211">حدد **حفظ** لتجعل زر **تحرير الاستعلام** في شريط أدوات **لإجراءات توجيه الموقع** متاحًا.</span><span class="sxs-lookup"><span data-stu-id="b762d-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="b762d-212">حدد **تحرير الاستعلام** لفتح محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="b762d-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="b762d-213">من علامة التبويب **النطاق**، تأكد من تكوين السطرين التاليين:</span><span class="sxs-lookup"><span data-stu-id="b762d-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="b762d-214">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="b762d-214">Line 1:</span></span>

        - <span data-ttu-id="b762d-215">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="b762d-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b762d-216">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="b762d-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b762d-217">**الحقل:** *المستودع*</span><span class="sxs-lookup"><span data-stu-id="b762d-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="b762d-218">**المعايير:** *51*</span><span class="sxs-lookup"><span data-stu-id="b762d-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="b762d-219">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="b762d-219">Line 2:</span></span>

        - <span data-ttu-id="b762d-220">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="b762d-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b762d-221">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="b762d-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b762d-222">**الحقل:** *الموقع*</span><span class="sxs-lookup"><span data-stu-id="b762d-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="b762d-223">**المعايير:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b762d-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="b762d-224">حدد **موافق** لإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="b762d-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b762d-225">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="b762d-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b762d-226">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="b762d-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b762d-227">في قائمة أصناف القائمة الموجودة في الجزء الأيمن، حدد **إبعاد الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b762d-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="b762d-228">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b762d-228">Select **Edit**.</span></span>
1. <span data-ttu-id="b762d-229">في علامة التبويب السريعة **فئات العمل**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b762d-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b762d-230">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b762d-231">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b762d-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b762d-232">**نوع أمر العمل:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="b762d-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="b762d-233">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b762d-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b762d-234">سيناريو</span><span class="sxs-lookup"><span data-stu-id="b762d-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b762d-235">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="b762d-235">Create a purchase order</span></span>

<span data-ttu-id="b762d-236">اتبع الخطوات التالية لإنشاء أمر شراء كمصدر للتوريد.</span><span class="sxs-lookup"><span data-stu-id="b762d-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="b762d-237">انتقل إلى **التدبير والتوريد \> أوامر الشراء \> كل أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b762d-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b762d-238">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b762d-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b762d-239">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b762d-240">**حساب المورّد:** *104*</span><span class="sxs-lookup"><span data-stu-id="b762d-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="b762d-241">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b762d-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b762d-242">حدد **موافق**، وقم بتدوين رقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="b762d-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="b762d-243">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b762d-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b762d-244">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="b762d-245">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b762d-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b762d-246">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="b762d-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="b762d-247">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="b762d-247">Create a sales order</span></span>

<span data-ttu-id="b762d-248">اتبع الخطوات التالية لإنشاء أمر مبيعات كمصدر للطلب.</span><span class="sxs-lookup"><span data-stu-id="b762d-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="b762d-249">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="b762d-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b762d-250">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b762d-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b762d-251">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b762d-252">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b762d-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="b762d-253">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="b762d-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b762d-254">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-254">Select **OK**.</span></span>
1. <span data-ttu-id="b762d-255">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b762d-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b762d-256">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="b762d-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="b762d-257">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b762d-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b762d-258">**الكمية:** *3*</span><span class="sxs-lookup"><span data-stu-id="b762d-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="b762d-259">إنشاء توزيع البضائع المخطط</span><span class="sxs-lookup"><span data-stu-id="b762d-259">Create planned cross-docking</span></span>

<span data-ttu-id="b762d-260">اتبع هذه الخطوات لإنشاء توزيع البضائع المخطط من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b762d-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="b762d-261">في صفحة **تفاصيل أمر المبيعات** لأمر المبيعات الذي قمت بإنشائه الآن، في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **الإصدار للمستودع**.</span><span class="sxs-lookup"><span data-stu-id="b762d-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b762d-262">يقوم إجراء الإصدار إلى المستودع بإنشاء شحنة وبند حمل لسطر أمر المبيعات، ويحاول تخصيص المخزون.</span><span class="sxs-lookup"><span data-stu-id="b762d-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="b762d-263">ستتلقى رسالة معلوماتية.</span><span class="sxs-lookup"><span data-stu-id="b762d-263">You receive an informational message.</span></span> <span data-ttu-id="b762d-264">ستتلقى أيضًا رسالة التحذير التالية: "لم يتم إنشاء عمل للموجة XXXX.</span><span class="sxs-lookup"><span data-stu-id="b762d-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="b762d-265">راجع سجل محفوظات إنشاء العمل للحصول على التفاصيل."</span><span class="sxs-lookup"><span data-stu-id="b762d-265">See the work creation history log for details."</span></span> <span data-ttu-id="b762d-266">هذا السلوك متوقع، نظرا لعدم وجود مخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="b762d-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="b762d-267">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المستودع**، حدد **تفاصيل الشحنة**.</span><span class="sxs-lookup"><span data-stu-id="b762d-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="b762d-268">تظهر صفحة **تفاصيل الشحنة** وتظهر الشحنة التي تم إنشاؤها لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b762d-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="b762d-269">في علامة التبويب السريعة **بنود الحمل**، لاحظ أن حقل **كمية توزيع البضائع المخطط** قد تم تعيينه إلى *3*.</span><span class="sxs-lookup"><span data-stu-id="b762d-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="b762d-270">ونظرا لأنه لا يتوفر مخزون في المستودع، ولكن سيصل مصدر التوريد الصالح خلال الإطار الزمني المحدد في قالب توزيع البضائع، فقد تم إنشاء كمية توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="b762d-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="b762d-271">في علامة التبويب السريعة **بنود الحمل**، حدد **توزيع البضائع المخطط** لعرض تفاصيل توزيع البضائع التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b762d-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="b762d-272">معالجة توزيع البضائع</span><span class="sxs-lookup"><span data-stu-id="b762d-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="b762d-273">استلام أمر الشراء في تطبيق المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="b762d-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="b762d-274">سيستلم النظام الكمية 5 من أمر الشراء إلى موقع الاستلام ويقوم بإنشاء نوعين من العمل.</span><span class="sxs-lookup"><span data-stu-id="b762d-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="b762d-275">يحتوي معرف العمل الأول الذي تم إنشاؤه على **نوع أمر عمل** بقيمة *توزيع البضائع* ويتم ربطه بأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b762d-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="b762d-276">وهو يتضمن الكمية 3 ويتم توجيهها إلى موقع الشحن النهائي لكي يمكن شحنها فورا.</span><span class="sxs-lookup"><span data-stu-id="b762d-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="b762d-277">يحتوي معرف العمل الثاني الذي تم إنشاؤه على **نوع أمر عمل** بقيمة *أوامر الشراء* ويتم ربطه بأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b762d-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="b762d-278">ويحتوي على الكمية المتبقية 2 والتي لم يتم توزيعها ويتم توجيهها إلى الإبعاد للتخزين.</span><span class="sxs-lookup"><span data-stu-id="b762d-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="b762d-279">سجل الدخول إلى الجهاز المحمول كمستخدم في المستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="b762d-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="b762d-280">الانتقال إلى **الوارد \> استلام الشراء**.</span><span class="sxs-lookup"><span data-stu-id="b762d-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="b762d-281">في حقل **رقم أمر الشراء**، أدخل رقم أمر الشراء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b762d-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="b762d-282">في حقل **كمية**، أدخل *5*.</span><span class="sxs-lookup"><span data-stu-id="b762d-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="b762d-283">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-283">Select **OK**.</span></span>
1. <span data-ttu-id="b762d-284">في الصفحة التالية، قم بتعيين حقل **الصنف**إلى *A0001*.</span><span class="sxs-lookup"><span data-stu-id="b762d-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="b762d-285">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-285">Select **OK**.</span></span>
1. <span data-ttu-id="b762d-286">في الصفحة التالية، قم بتأكيد **رقم أمر الشراء** و**الصنف** و**الكمية** بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="b762d-287">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b762d-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b762d-288">حدد **إلغاء** للخروج.</span><span class="sxs-lookup"><span data-stu-id="b762d-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="b762d-289">الإبعاد لتوزيع البضائع والتجميع</span><span class="sxs-lookup"><span data-stu-id="b762d-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="b762d-290">حاليًا، يتضمن كل من معرفي العمل نفس لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="b762d-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="b762d-291">لإكمال الخطوات التالية، يجب الحصول على معرف العمل ومعرف لوحة الترخيص المستهدفة.</span><span class="sxs-lookup"><span data-stu-id="b762d-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="b762d-292">يمكنك الحصول على هذه المعلومات من تفاصيل العمل الخاصة بسطر أمر الشراء وسطر أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="b762d-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="b762d-293">وبدلا من ذلك، يمكن الانتقال إلى **إدارة المستودع \> العمل \> تفاصيل العمل** وقم بالتصفية للعمل الذي تكون قيمة **المستودع** له *51*.</span><span class="sxs-lookup"><span data-stu-id="b762d-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="b762d-294">على الجهاز المحمول، انتقل إلى **الوارد \> إبعاد الشراء**، ثم أدخل لوحة الترخيص المستهدفة من العمل.</span><span class="sxs-lookup"><span data-stu-id="b762d-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="b762d-295">في حقل **المعرف**، أدخل معرف لوحة الترخيص الهدف من تفاصيل العمل.</span><span class="sxs-lookup"><span data-stu-id="b762d-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="b762d-296">تظهر صفحة انتقاء توزيع البضائع موقع الانتقاء (*RECV*) ولوحة الترخيص الهدف (*لوحة الترخيص*) والصنف (*A0001*) والكمية (*3*).</span><span class="sxs-lookup"><span data-stu-id="b762d-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="b762d-297">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-297">Select **OK**.</span></span>
1. <span data-ttu-id="b762d-298">في حقل **لوحة الترخيص الهدف**، أدخل لوح الترخيص الهدف لمعرف لوحة الترخيص الذي يجب وضعه (توزيعه) إلى موقع الشحن.</span><span class="sxs-lookup"><span data-stu-id="b762d-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="b762d-299">يمكنك تحديد أي معرف لوحة الترخيص من اختيارك.</span><span class="sxs-lookup"><span data-stu-id="b762d-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="b762d-300">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-300">Select **OK**.</span></span>
1. <span data-ttu-id="b762d-301">في الصفحة التالية في حقل **المعرف**، أدخل معرف لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="b762d-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="b762d-302">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-302">Select **OK**.</span></span>
1. <span data-ttu-id="b762d-303">قم بتأكيد العمل لانتقاء باقي الكمية 2، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="b762d-304">في الصفحة التالية، حدد **تم** لإنهاء عملية الانتقاء وبدء عملية الإبعاد.</span><span class="sxs-lookup"><span data-stu-id="b762d-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="b762d-305">يعرض لك تطبيق الأجهزة المحمولة المكان ولوحة الترخيص لوضع الصنف فيه.</span><span class="sxs-lookup"><span data-stu-id="b762d-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="b762d-306">قم بتأكيد **وضع** التخزين المجمع بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="b762d-307">في الصفحة التالية، قم بتأكيد **وضع** توزيع البضائع بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b762d-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="b762d-308">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="b762d-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b762d-309">حدد **إلغاء** للخروج.</span><span class="sxs-lookup"><span data-stu-id="b762d-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="b762d-310">يبين الرسم التوضيحي التالي كيف يظهر عمل توزيع البضائع المكتمل في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b762d-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b762d-311">![اكتمال عمل توزيع البضائع](media/PlannedCrossDockingWork.png "اكتمال عمل توزيع البضائع")</span><span class="sxs-lookup"><span data-stu-id="b762d-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
