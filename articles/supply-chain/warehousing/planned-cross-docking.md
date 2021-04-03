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
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556256"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="7d585-104">توزيع البضائع المخطط</span><span class="sxs-lookup"><span data-stu-id="7d585-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d585-105">يصف هذا الموضوع توزيع البضائع المخطط المتقدم.</span><span class="sxs-lookup"><span data-stu-id="7d585-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="7d585-106">توزيع البضائع هو إحدى عمليات المستودع، حيث يتم توجيه كمية المخزون المطلوبة لأمر ما بشكل مستقيم من الاستلام أو الإنشاء إلى المساحة الخارجية الصحيحة أو ناحية الإعداد.</span><span class="sxs-lookup"><span data-stu-id="7d585-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="7d585-107">ويتم توجيه كافة المخزون المتبقي من المصدر الوارد إلى موقع التخزين الصحيح خلال عملية الإبعاد العادية.</span><span class="sxs-lookup"><span data-stu-id="7d585-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="7d585-108">يتيح توزيع البضائع للعاملين تخطي الإبعاد الوارد الانتقاء الصادر للمخزون الذي تم وضع علامة عليه بالفعل لأمر صادر.</span><span class="sxs-lookup"><span data-stu-id="7d585-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="7d585-109">لذلك، يتم تقليل عدد مرات لمس المخزون، قدر الإمكان.</span><span class="sxs-lookup"><span data-stu-id="7d585-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="7d585-110">بالإضافة إلى ذلك، بسبب وجود تفاعل أقل مع النظام، تزداد توفيرات الوقت والمساحة على أرضية صالة المستودع.</span><span class="sxs-lookup"><span data-stu-id="7d585-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="7d585-111">قبل تشغيل توزيع البضائع، يجب أن يقوم المستخدم بتكوين قالب توزيع بضائع جديد حيث يتم تحديد مصدر التوريد والمجموعات الأخرى من المتطلبات لتوزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="7d585-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="7d585-112">وبمجرد إنشاء الأمر الصادر، يجب وضع علامة على البند في مقابل أمر وارد يحتوي على نفس الصنف.</span><span class="sxs-lookup"><span data-stu-id="7d585-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="7d585-113">وفي وقت استلام الأمر الوارد، يقوم إعداد توزيع البضائع تلقائيا بتحديد الحاجة إلى توزيع البضائع وينشئ عمل الحركة للكمية المطلوبة، استنادا إلى إعداد توجيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="7d585-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="7d585-114">و **لا** يتم إلغاء تسجيل حركات المخزون عندما يتم إلغاء عمل توزيع البضائع، حتى في حالة تشغيل إعداد هذه الإمكانية في معلمات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="7d585-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="7d585-115">تشغيل ميزات توزيع البضائع المخططة</span><span class="sxs-lookup"><span data-stu-id="7d585-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="7d585-116">إذا لم يتضمن نظامك الميزات الموضحة في هذا الموضوع بالفعل، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) وقم بتشغيل الميزات التالية بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="7d585-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="7d585-117">*توزيع البضائع المخطط*</span><span class="sxs-lookup"><span data-stu-id="7d585-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="7d585-118">*قوالب توزيع البضائع مع توجيهات المواقع*</span><span class="sxs-lookup"><span data-stu-id="7d585-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="7d585-119">الإعداد</span><span class="sxs-lookup"><span data-stu-id="7d585-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="7d585-120">إعادة إنشاء طرق ترحيل الحمل</span><span class="sxs-lookup"><span data-stu-id="7d585-120">Regenerate load posting methods</span></span>

<span data-ttu-id="7d585-121">يتم تنفيذ توزيع البضائع المخطط كطريقه لترحيل الحمل.</span><span class="sxs-lookup"><span data-stu-id="7d585-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="7d585-122">بعد تشغيل الميزة، يجب إعادة إنشاء الأساليب.</span><span class="sxs-lookup"><span data-stu-id="7d585-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="7d585-123">انتقل إلى **إدارة المستودعات \> الإعداد \> طرق ترحيل الحمل**.</span><span class="sxs-lookup"><span data-stu-id="7d585-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="7d585-124">في جزء الإجراءات، حدد **طرق إعادة الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="7d585-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="7d585-125">عند اكتمال إعادة الإنشاء، يجب أن تشاهد أسلوب له **اسم أسلوب** بالقيمة *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="7d585-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="7d585-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d585-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="7d585-127">إنشاء قالب توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="7d585-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="7d585-128">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> قوالب توزيع البضائع**.</span><span class="sxs-lookup"><span data-stu-id="7d585-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="7d585-129">في جزء الإجراءات، حدد **جديد** لإنشاء قالب.</span><span class="sxs-lookup"><span data-stu-id="7d585-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="7d585-130">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="7d585-131">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="7d585-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="7d585-132">يحدد هذا الحقل الترتيب الذي يتم تقييم القوالب باستخدامه.</span><span class="sxs-lookup"><span data-stu-id="7d585-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="7d585-133">**معرف قالب توزيع البضائع:** *51*</span><span class="sxs-lookup"><span data-stu-id="7d585-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="7d585-134">**الوصف:** *المستودع 51*</span><span class="sxs-lookup"><span data-stu-id="7d585-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="7d585-135">**سياسة إصدار الطلب:** *قبل إيصال التوريد*</span><span class="sxs-lookup"><span data-stu-id="7d585-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="7d585-136">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="7d585-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="7d585-137">يتحكم الإعداد الموجود في علامة التبويب السريعة **التخطيط** في كيفية عمل القالب.</span><span class="sxs-lookup"><span data-stu-id="7d585-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="7d585-138">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-138">Set the following values:</span></span>

    - <span data-ttu-id="7d585-139">**متطلبات الطلب:** *بلا*</span><span class="sxs-lookup"><span data-stu-id="7d585-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="7d585-140">يحدد هذا الحقل متطلبات مخزون الطلب.</span><span class="sxs-lookup"><span data-stu-id="7d585-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="7d585-141">إذا كان يجب ربط الطلب بالتوريد قبل الإصدار، فحدد *وضع علامة*.</span><span class="sxs-lookup"><span data-stu-id="7d585-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="7d585-142">إذا كان يجب حجز الطلب مقابل التوريد قبل الإصدار، فحدد *حجز الأمر*.</span><span class="sxs-lookup"><span data-stu-id="7d585-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="7d585-143">**نوع تحديد الموقع:** *مواقع الشحنة*</span><span class="sxs-lookup"><span data-stu-id="7d585-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="7d585-144">يحدد هذا الحقل ما إذا كان يجب أن يستخدم عمل توزيع البضائع مواقع مرحلية/مواقع حمل من الشحنة، أو ما إذا كان يجب عليه استخدام توجيهات المواقع للعثور على مواقع مرحلية/مواقع حمل خاصة به.</span><span class="sxs-lookup"><span data-stu-id="7d585-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="7d585-145">**قالب العمل:** – اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="7d585-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="7d585-146">يحدد هذا الحقل قالب العمل الذي ينبغي استخدامه عند إنشاء عمل توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="7d585-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="7d585-147">**إعادة التحقق عند استلام التوريد:** *لا*</span><span class="sxs-lookup"><span data-stu-id="7d585-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="7d585-148">يحدد هذا الخيار ما إذا كان يجب إعادة التحقق من التوريد أثناء الاستلام أم لا.</span><span class="sxs-lookup"><span data-stu-id="7d585-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="7d585-149">إذا تم تعيين هذا الخيار على *نعم*، فعندئذ يتم تحديد كل من أقصى إطار زمني ونطاق أيام انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="7d585-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="7d585-150">**كود التوجيه** اترك هذا الحقل فارغًا</span><span class="sxs-lookup"><span data-stu-id="7d585-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="7d585-151">يتيح هذا الخيار للنظام استخدام توجيهات الموقع للمساعدة في تحديد أفضل مكان لنقل مخزون توزيع البضائع إليه.</span><span class="sxs-lookup"><span data-stu-id="7d585-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="7d585-152">يمكنك إعداده عن طريق تعيين رمز توجيهي لكل قالب توزيع البضائع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="7d585-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="7d585-153">يحدد كل رمز توجيه توجيهًا فريدًا للموقع.</span><span class="sxs-lookup"><span data-stu-id="7d585-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="7d585-154">**إطار زمن التحقق من الصحة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="7d585-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="7d585-155">يحدد هذا الخيار ما إذا كان يجب تقييم الحد الأقصى للإطار الزمني عند تحديد مصدر توريد.</span><span class="sxs-lookup"><span data-stu-id="7d585-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="7d585-156">إذا تم تعيين هذا الخيار على *نعم*، ستتوفر الحقول التي ترتبط بالحد الأقصى والأدنى للإطارات الزمنية.</span><span class="sxs-lookup"><span data-stu-id="7d585-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="7d585-157">**أقصى إطار زمني:** *5*</span><span class="sxs-lookup"><span data-stu-id="7d585-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="7d585-158">يحدد هذا الحقل أقصى فترة بين وصول التوريد ومغادرة الطلب.</span><span class="sxs-lookup"><span data-stu-id="7d585-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="7d585-159">**وحدة أقصى إطار زمني:** *الأيام*</span><span class="sxs-lookup"><span data-stu-id="7d585-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="7d585-160">**أدنى إطار زمني:** *0*</span><span class="sxs-lookup"><span data-stu-id="7d585-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="7d585-161">يحدد هذا الحقل أدنى فترة بين وصول التوريد ومغادرة الطلب.</span><span class="sxs-lookup"><span data-stu-id="7d585-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="7d585-162">**وحدة أدنى إطار زمني:** *الأيام*</span><span class="sxs-lookup"><span data-stu-id="7d585-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="7d585-163">**نطاق أيام انتهاء الصلاحية:** *0*</span><span class="sxs-lookup"><span data-stu-id="7d585-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="7d585-164">*معيار تاريخ ‏‫‏‫ما تنتهي صلاحيته أولاً يصرف أولاً (FEFO):* يحدد هذا الحقل أقصى عدد للأيام بين تاريخ انتهاء صلاحية دفعة ما تنتهي صلاحيته أولا الموجودة حاليًا في المستودع والدفعة التي يتم استلامها.</span><span class="sxs-lookup"><span data-stu-id="7d585-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="7d585-165">في علامة التبويب السريعة **مصادر التوريد**، حدد أنواع التوريد الصالحة لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="7d585-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="7d585-166">حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="7d585-167">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="7d585-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="7d585-168">**مصدر التوريد:** *أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="7d585-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="7d585-169">إنشاء درجة عمل</span><span class="sxs-lookup"><span data-stu-id="7d585-169">Create a work class</span></span>

1. <span data-ttu-id="7d585-170">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="7d585-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="7d585-171">في جزء الإجراءات، حدد **جديد** لإنشاء فئة عمل.</span><span class="sxs-lookup"><span data-stu-id="7d585-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="7d585-172">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-172">Set the following values:</span></span>

    - <span data-ttu-id="7d585-173">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="7d585-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="7d585-174">**الوصف:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="7d585-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="7d585-175">**نوع أمر العمل:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="7d585-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="7d585-176">إنشاء قالب عمل</span><span class="sxs-lookup"><span data-stu-id="7d585-176">Create a work template</span></span>

1. <span data-ttu-id="7d585-177">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="7d585-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="7d585-178">قم بتعيين حقل **نوع أمر العمل** إلى *توزيع البضائع*.</span><span class="sxs-lookup"><span data-stu-id="7d585-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="7d585-179">في جزء الإجراءات، حدد **جديد** لإضافة سطر إلى علامة تبويب **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="7d585-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="7d585-180">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7d585-181">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="7d585-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="7d585-182">**قالب العمل:** *توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="7d585-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="7d585-183">**وصف قالب العمل:** *توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="7d585-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="7d585-184">حدد **حفظ** لجعل علامة التبويب السريعة **تفاصيل قالب العمل** متاحة.</span><span class="sxs-lookup"><span data-stu-id="7d585-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="7d585-185">في علامة التبويب السريعة **تفاصيل قالب العمل**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="7d585-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="7d585-186">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7d585-187">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="7d585-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="7d585-188">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="7d585-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="7d585-189">حدد **جديد** لإضافة سطر آخر، ثم قم بتعيين القيم التالية عليه:</span><span class="sxs-lookup"><span data-stu-id="7d585-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="7d585-190">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="7d585-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="7d585-191">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="7d585-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="7d585-192">حدد **حفظ**، وتأكد من أنه تم تحديد خانة الاختيار **صالح** لقالب *توزيع البضائع 51*.</span><span class="sxs-lookup"><span data-stu-id="7d585-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="7d585-193">يجب أن تكون معرفات فئة العمل لأنواع عمل *الانتقاء* و *الوضع* متطابقة.</span><span class="sxs-lookup"><span data-stu-id="7d585-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="7d585-194">إنشاء توجيات الموقع</span><span class="sxs-lookup"><span data-stu-id="7d585-194">Create location directives</span></span>

1. <span data-ttu-id="7d585-195">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="7d585-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="7d585-196">في الجزء الأيسر، قم بتعيين حقل **نوع أمر العمل** إلى *توزيع البضائع*.</span><span class="sxs-lookup"><span data-stu-id="7d585-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="7d585-197">في جزء الإجراءات، حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="7d585-198">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="7d585-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="7d585-199">**الاسم:** *إيداع توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="7d585-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="7d585-200">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="7d585-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="7d585-201">**الموقع:** *5*</span><span class="sxs-lookup"><span data-stu-id="7d585-201">**Site:** *5*</span></span>
    - <span data-ttu-id="7d585-202">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="7d585-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="7d585-203">حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.</span><span class="sxs-lookup"><span data-stu-id="7d585-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="7d585-204">في علامة التبويب السريعة **السطور**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="7d585-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="7d585-205">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7d585-206">**من الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="7d585-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="7d585-207">**إلى الكمية:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="7d585-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="7d585-208">حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="7d585-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="7d585-209">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="7d585-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="7d585-210">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7d585-211">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="7d585-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="7d585-212">**استخدام الموقع الثابت:** *المواقع الثابتة وغير الثابتة*</span><span class="sxs-lookup"><span data-stu-id="7d585-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="7d585-213">حدد **حفظ** لتجعل زر **تحرير الاستعلام** في شريط أدوات **لإجراءات توجيه الموقع** متاحًا.</span><span class="sxs-lookup"><span data-stu-id="7d585-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="7d585-214">حدد **تحرير الاستعلام** لفتح محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="7d585-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="7d585-215">من علامة التبويب **النطاق**، تأكد من تكوين السطرين التاليين:</span><span class="sxs-lookup"><span data-stu-id="7d585-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="7d585-216">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="7d585-216">Line 1:</span></span>

        - <span data-ttu-id="7d585-217">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="7d585-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="7d585-218">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="7d585-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="7d585-219">**الحقل:** *المستودع*</span><span class="sxs-lookup"><span data-stu-id="7d585-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="7d585-220">**المعايير:** *51*</span><span class="sxs-lookup"><span data-stu-id="7d585-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="7d585-221">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="7d585-221">Line 2:</span></span>

        - <span data-ttu-id="7d585-222">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="7d585-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="7d585-223">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="7d585-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="7d585-224">**الحقل:** *الموقع*</span><span class="sxs-lookup"><span data-stu-id="7d585-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="7d585-225">**المعايير:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="7d585-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="7d585-226">حدد **موافق** لإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="7d585-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="7d585-227">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="7d585-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="7d585-228">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="7d585-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="7d585-229">في قائمة أصناف القائمة الموجودة في الجزء الأيمن، حدد **إبعاد الشراء**.</span><span class="sxs-lookup"><span data-stu-id="7d585-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="7d585-230">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="7d585-230">Select **Edit**.</span></span>
1. <span data-ttu-id="7d585-231">في علامة التبويب السريعة **فئات العمل**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="7d585-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="7d585-232">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7d585-233">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="7d585-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="7d585-234">**نوع أمر العمل:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="7d585-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="7d585-235">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7d585-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="7d585-236">سيناريو</span><span class="sxs-lookup"><span data-stu-id="7d585-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="7d585-237">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="7d585-237">Create a purchase order</span></span>

<span data-ttu-id="7d585-238">اتبع الخطوات التالية لإنشاء أمر شراء كمصدر للتوريد.</span><span class="sxs-lookup"><span data-stu-id="7d585-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="7d585-239">انتقل إلى **التدبير والتوريد \> أوامر الشراء \> كل أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="7d585-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="7d585-240">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7d585-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7d585-241">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7d585-242">**حساب المورّد:** *104*</span><span class="sxs-lookup"><span data-stu-id="7d585-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="7d585-243">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="7d585-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="7d585-244">حدد **موافق**، وقم بتدوين رقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="7d585-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="7d585-245">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="7d585-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="7d585-246">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="7d585-247">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="7d585-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="7d585-248">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="7d585-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="7d585-249">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="7d585-249">Create a sales order</span></span>

<span data-ttu-id="7d585-250">اتبع الخطوات التالية لإنشاء أمر مبيعات كمصدر للطلب.</span><span class="sxs-lookup"><span data-stu-id="7d585-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="7d585-251">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="7d585-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7d585-252">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7d585-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7d585-253">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7d585-254">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="7d585-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="7d585-255">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="7d585-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="7d585-256">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-256">Select **OK**.</span></span>
1. <span data-ttu-id="7d585-257">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="7d585-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="7d585-258">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="7d585-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="7d585-259">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="7d585-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="7d585-260">**الكمية:** *3*</span><span class="sxs-lookup"><span data-stu-id="7d585-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="7d585-261">إنشاء توزيع البضائع المخطط</span><span class="sxs-lookup"><span data-stu-id="7d585-261">Create planned cross-docking</span></span>

<span data-ttu-id="7d585-262">اتبع هذه الخطوات لإنشاء توزيع البضائع المخطط من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d585-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="7d585-263">في صفحة **تفاصيل أمر المبيعات** لأمر المبيعات الذي قمت بإنشائه الآن، في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **الإصدار للمستودع**.</span><span class="sxs-lookup"><span data-stu-id="7d585-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="7d585-264">يقوم إجراء الإصدار إلى المستودع بإنشاء شحنة وبند حمل لسطر أمر المبيعات، ويحاول تخصيص المخزون.</span><span class="sxs-lookup"><span data-stu-id="7d585-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="7d585-265">ستتلقى رسالة معلوماتية.</span><span class="sxs-lookup"><span data-stu-id="7d585-265">You receive an informational message.</span></span> <span data-ttu-id="7d585-266">ستتلقى أيضًا رسالة التحذير التالية: "لم يتم إنشاء عمل للموجة XXXX.</span><span class="sxs-lookup"><span data-stu-id="7d585-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="7d585-267">راجع سجل محفوظات إنشاء العمل للحصول على التفاصيل."</span><span class="sxs-lookup"><span data-stu-id="7d585-267">See the work creation history log for details."</span></span> <span data-ttu-id="7d585-268">هذا السلوك متوقع، نظرا لعدم وجود مخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="7d585-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="7d585-269">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المستودع**، حدد **تفاصيل الشحنة**.</span><span class="sxs-lookup"><span data-stu-id="7d585-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="7d585-270">تظهر صفحة **تفاصيل الشحنة** وتظهر الشحنة التي تم إنشاؤها لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d585-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="7d585-271">في علامة التبويب السريعة **بنود الحمل**، لاحظ أن حقل **كمية توزيع البضائع المخطط** قد تم تعيينه إلى *3*.</span><span class="sxs-lookup"><span data-stu-id="7d585-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="7d585-272">ونظرا لأنه لا يتوفر مخزون في المستودع، ولكن سيصل مصدر التوريد الصالح خلال الإطار الزمني المحدد في قالب توزيع البضائع، فقد تم إنشاء كمية توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="7d585-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="7d585-273">في علامة التبويب السريعة **بنود الحمل**، حدد **توزيع البضائع المخطط** لعرض تفاصيل توزيع البضائع التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="7d585-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="7d585-274">معالجة توزيع البضائع</span><span class="sxs-lookup"><span data-stu-id="7d585-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="7d585-275">استلام أمر الشراء في تطبيق المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="7d585-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="7d585-276">سيستلم النظام الكمية 5 من أمر الشراء إلى موقع الاستلام ويقوم بإنشاء نوعين من العمل.</span><span class="sxs-lookup"><span data-stu-id="7d585-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="7d585-277">يحتوي معرف العمل الأول الذي تم إنشاؤه على **نوع أمر عمل** بقيمة *توزيع البضائع* ويتم ربطه بأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d585-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="7d585-278">وهو يتضمن الكمية 3 ويتم توجيهها إلى موقع الشحن النهائي لكي يمكن شحنها فورا.</span><span class="sxs-lookup"><span data-stu-id="7d585-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="7d585-279">يحتوي معرف العمل الثاني الذي تم إنشاؤه على **نوع أمر عمل** بقيمة *أوامر الشراء* ويتم ربطه بأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="7d585-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="7d585-280">ويحتوي على الكمية المتبقية 2 والتي لم يتم توزيعها ويتم توجيهها إلى الإبعاد للتخزين.</span><span class="sxs-lookup"><span data-stu-id="7d585-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="7d585-281">سجل الدخول إلى الجهاز المحمول كمستخدم في المستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="7d585-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="7d585-282">الانتقال إلى **الوارد \> استلام الشراء**.</span><span class="sxs-lookup"><span data-stu-id="7d585-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="7d585-283">في حقل **رقم أمر الشراء**، أدخل رقم أمر الشراء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="7d585-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="7d585-284">في حقل **كمية**، أدخل *5*.</span><span class="sxs-lookup"><span data-stu-id="7d585-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="7d585-285">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-285">Select **OK**.</span></span>
1. <span data-ttu-id="7d585-286">في الصفحة التالية، قم بتعيين حقل **الصنف** إلى *A0001*.</span><span class="sxs-lookup"><span data-stu-id="7d585-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="7d585-287">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-287">Select **OK**.</span></span>
1. <span data-ttu-id="7d585-288">في الصفحة التالية، قم بتأكيد **رقم أمر الشراء** و **الصنف** و **الكمية** بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="7d585-289">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="7d585-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="7d585-290">حدد **إلغاء** للخروج.</span><span class="sxs-lookup"><span data-stu-id="7d585-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="7d585-291">الإبعاد لتوزيع البضائع والتجميع</span><span class="sxs-lookup"><span data-stu-id="7d585-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="7d585-292">حاليًا، يتضمن كل من معرفي العمل نفس لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="7d585-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="7d585-293">لإكمال الخطوات التالية، يجب الحصول على معرف العمل ومعرف لوحة الترخيص المستهدفة.</span><span class="sxs-lookup"><span data-stu-id="7d585-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="7d585-294">يمكنك الحصول على هذه المعلومات من تفاصيل العمل الخاصة بسطر أمر الشراء وسطر أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="7d585-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="7d585-295">وبدلا من ذلك، يمكن الانتقال إلى **إدارة المستودع \> العمل \> تفاصيل العمل** وقم بالتصفية للعمل الذي تكون قيمة **المستودع** له *51*.</span><span class="sxs-lookup"><span data-stu-id="7d585-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="7d585-296">على الجهاز المحمول، انتقل إلى **الوارد \> إبعاد الشراء**، ثم أدخل لوحة الترخيص المستهدفة من العمل.</span><span class="sxs-lookup"><span data-stu-id="7d585-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="7d585-297">في حقل **المعرف**، أدخل معرف لوحة الترخيص الهدف من تفاصيل العمل.</span><span class="sxs-lookup"><span data-stu-id="7d585-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="7d585-298">تظهر صفحة انتقاء توزيع البضائع موقع الانتقاء (*RECV*) ولوحة الترخيص الهدف (*لوحة الترخيص*) والصنف (*A0001*) والكمية (*3*).</span><span class="sxs-lookup"><span data-stu-id="7d585-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="7d585-299">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-299">Select **OK**.</span></span>
1. <span data-ttu-id="7d585-300">في حقل **لوحة الترخيص الهدف**، أدخل لوح الترخيص الهدف لمعرف لوحة الترخيص الذي يجب وضعه (توزيعه) إلى موقع الشحن.</span><span class="sxs-lookup"><span data-stu-id="7d585-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="7d585-301">يمكنك تحديد أي معرف لوحة الترخيص من اختيارك.</span><span class="sxs-lookup"><span data-stu-id="7d585-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="7d585-302">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-302">Select **OK**.</span></span>
1. <span data-ttu-id="7d585-303">في الصفحة التالية في حقل **المعرف**، أدخل معرف لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="7d585-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="7d585-304">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-304">Select **OK**.</span></span>
1. <span data-ttu-id="7d585-305">قم بتأكيد العمل لانتقاء باقي الكمية 2، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="7d585-306">في الصفحة التالية، حدد **تم** لإنهاء عملية الانتقاء وبدء عملية الإبعاد.</span><span class="sxs-lookup"><span data-stu-id="7d585-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="7d585-307">يعرض لك تطبيق الأجهزة المحمولة المكان ولوحة الترخيص لوضع الصنف فيه.</span><span class="sxs-lookup"><span data-stu-id="7d585-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="7d585-308">قم بتأكيد **وضع** التخزين المجمع بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="7d585-309">في الصفحة التالية، قم بتأكيد **وضع** توزيع البضائع بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7d585-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="7d585-310">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="7d585-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="7d585-311">حدد **إلغاء** للخروج.</span><span class="sxs-lookup"><span data-stu-id="7d585-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="7d585-312">يبين الرسم التوضيحي التالي كيف يظهر عمل توزيع البضائع المكتمل في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7d585-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="7d585-313">![اكتمال عمل توزيع البضائع](media/PlannedCrossDockingWork.png "اكتمال عمل توزيع البضائع")</span><span class="sxs-lookup"><span data-stu-id="7d585-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]