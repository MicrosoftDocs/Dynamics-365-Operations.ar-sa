---
title: توزيع البضائع المخطط
description: يصف هذا الموضوع توزيع البضائع المخطط المتقدم، حيث يتم توجيه كمية المخزون المطلوبة لأمر ما بشكل مستقيم من الاستلام أو الإنشاء إلى المساحة الخارجية الصحيحة أو ناحية الإعداد. ويتم توجيه كافة المخزون المتبقي من المصدر الوارد إلى موقع التخزين الصحيح خلال عملية الإبعاد العادية.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911238"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="d3f96-104">توزيع البضائع المخطط</span><span class="sxs-lookup"><span data-stu-id="d3f96-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3f96-105">يصف هذا الموضوع توزيع البضائع المخطط المتقدم.</span><span class="sxs-lookup"><span data-stu-id="d3f96-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="d3f96-106">توزيع البضائع هو إحدى عمليات المستودع، حيث يتم توجيه كمية المخزون المطلوبة لأمر ما بشكل مستقيم من الاستلام أو الإنشاء إلى المساحة الخارجية الصحيحة أو ناحية الإعداد.</span><span class="sxs-lookup"><span data-stu-id="d3f96-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="d3f96-107">ويتم توجيه كافة المخزون المتبقي من المصدر الوارد إلى موقع التخزين الصحيح خلال عملية الإبعاد العادية.</span><span class="sxs-lookup"><span data-stu-id="d3f96-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="d3f96-108">يتيح توزيع البضائع للعاملين تخطي الإبعاد الوارد الانتقاء الصادر للمخزون الذي تم وضع علامة عليه بالفعل لأمر صادر.</span><span class="sxs-lookup"><span data-stu-id="d3f96-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="d3f96-109">لذلك، يتم تقليل عدد مرات لمس المخزون، قدر الإمكان.</span><span class="sxs-lookup"><span data-stu-id="d3f96-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="d3f96-110">بالإضافة إلى ذلك، بسبب وجود تفاعل أقل مع النظام، تزداد توفيرات الوقت والمساحة على أرضية صالة المستودع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="d3f96-111">قبل تشغيل توزيع البضائع، يجب أن تقوم بتكوين قالب توزيع بضائع جديد حيث يتم تحديد مصدر التوريد والمجموعات الأخرى من المتطلبات لتوزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="d3f96-112">وبمجرد إنشاء الأمر الصادر، يجب وضع علامة على البند في مقابل أمر وارد يحتوي على نفس الصنف.</span><span class="sxs-lookup"><span data-stu-id="d3f96-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="d3f96-113">يمكنك تحديد حقل كود التوجيه على قالب توزيع البضائع، بطريقة مماثلة لإعداد التزويد وأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d3f96-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="d3f96-114">وفي وقت استلام الأمر الوارد، يقوم إعداد توزيع البضائع تلقائيا بتحديد الحاجة إلى توزيع البضائع وينشئ عمل الحركة للكمية المطلوبة، استنادا إلى إعداد توجيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="d3f96-115">و *لا* يتم إلغاء تسجيل حركات المخزون عندما يتم إلغاء عمل توزيع البضائع، حتى في حالة تشغيل إعداد هذه الإمكانية في معلمات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="d3f96-116">تشغيل ميزات توزيع البضائع المخططة</span><span class="sxs-lookup"><span data-stu-id="d3f96-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="d3f96-117">إذا لم يتضمن نظامك الميزات الموضحة في هذا الموضوع بالفعل، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) وقم بتشغيل الميزات التالية بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="d3f96-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="d3f96-118">*توزيع البضائع المخطط*</span><span class="sxs-lookup"><span data-stu-id="d3f96-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="d3f96-119">*قوالب توزيع البضائع مع توجيهات المواقع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="d3f96-120">تمكّن هذه الميزة تحديد حقل **كود التوجيه** على قالب توزيع البضائع، بما يشبه طريقة إعداد قوالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="d3f96-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="d3f96-121">يؤدي تمكين هذه الميزة إلى منعك من إضافة كود التوجيه على بنود قالب عمل توزيع البضائع لبند *الوضع*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="d3f96-122">ويضمن ذلك إمكانية تحديد موقع الوضع النهائي أثناء إنشاء العمل قبل وضع قوالب العمل في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="d3f96-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="d3f96-123">الإعداد</span><span class="sxs-lookup"><span data-stu-id="d3f96-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="d3f96-124">إعادة إنشاء طرق ترحيل الحمل</span><span class="sxs-lookup"><span data-stu-id="d3f96-124">Regenerate load posting methods</span></span>

<span data-ttu-id="d3f96-125">يتم تنفيذ توزيع البضائع المخطط كطريقه لترحيل الحمل.</span><span class="sxs-lookup"><span data-stu-id="d3f96-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="d3f96-126">بعد تشغيل الميزة، يجب إعادة إنشاء الأساليب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="d3f96-127">انتقل إلى **إدارة المستودعات \> الإعداد \> طرق ترحيل الحمل**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="d3f96-128">في جزء الإجراءات، حدد **طرق إعادة الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d3f96-129">عند اكتمال إعادة الإنشاء، يجب أن تشاهد أسلوب له **اسم أسلوب** بالقيمة *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="d3f96-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="d3f96-131">إنشاء قالب توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="d3f96-132">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> قوالب توزيع البضائع**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="d3f96-133">في جزء الإجراءات، حدد **جديد** لإنشاء قالب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="d3f96-134">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="d3f96-135">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="d3f96-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="d3f96-136">يحدد هذا الحقل الترتيب الذي يتم تقييم القوالب باستخدامه.</span><span class="sxs-lookup"><span data-stu-id="d3f96-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="d3f96-137">**معرف قالب توزيع البضائع:** *51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="d3f96-138">**الوصف:** *المستودع 51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="d3f96-139">**سياسة إصدار الطلب:** *قبل إيصال التوريد*</span><span class="sxs-lookup"><span data-stu-id="d3f96-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="d3f96-140">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d3f96-141">يتحكم الإعداد الموجود في علامة التبويب السريعة **التخطيط** في كيفية عمل القالب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="d3f96-142">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-142">Set the following values:</span></span>

    - <span data-ttu-id="d3f96-143">**متطلبات الطلب:** *بلا*</span><span class="sxs-lookup"><span data-stu-id="d3f96-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="d3f96-144">يحدد هذا الحقل متطلبات مخزون الطلب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="d3f96-145">إذا كان يجب ربط الطلب بالتوريد قبل الإصدار، فحدد *وضع علامة*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="d3f96-146">إذا كان يجب حجز الطلب مقابل التوريد قبل الإصدار، فحدد *حجز الأمر*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="d3f96-147">**نوع تحديد الموقع:** *مواقع الشحنة*</span><span class="sxs-lookup"><span data-stu-id="d3f96-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="d3f96-148">يحدد هذا الحقل ما إذا كان يجب أن يستخدم عمل توزيع البضائع مواقع مرحلية/مواقع حمل من الشحنة، أو ما إذا كان يجب عليه استخدام توجيهات المواقع للعثور على مواقع مرحلية/مواقع حمل خاصة به.</span><span class="sxs-lookup"><span data-stu-id="d3f96-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="d3f96-149">**قالب العمل:** – اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="d3f96-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="d3f96-150">يحدد هذا الحقل قالب العمل الذي ينبغي استخدامه عند إنشاء عمل توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="d3f96-151">**إعادة التحقق عند استلام التوريد:** *لا*</span><span class="sxs-lookup"><span data-stu-id="d3f96-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="d3f96-152">يحدد هذا الخيار ما إذا كان يجب إعادة التحقق من التوريد أثناء الاستلام أم لا.</span><span class="sxs-lookup"><span data-stu-id="d3f96-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="d3f96-153">إذا تم تعيين هذا الخيار على *نعم*، فعندئذ يتم تحديد كل من أقصى إطار زمني ونطاق أيام انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="d3f96-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="d3f96-154">**كود التوجيه:** اترك هذا الحقل فارغًا</span><span class="sxs-lookup"><span data-stu-id="d3f96-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="d3f96-155">يتم تمكين هذا الخيار بواسطة ميزة *قوالب توزيع البضائع باستخدام توجيهات المواقع*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="d3f96-156">يستخدم النظام توجيهات الموقع للمساعدة في تحديد أفضل مكان لنقل مخزون توزيع البضائع إليه.</span><span class="sxs-lookup"><span data-stu-id="d3f96-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="d3f96-157">يمكنك إعداده عن طريق تعيين رمز توجيهي لكل قالب توزيع البضائع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="d3f96-158">إذا تم تعيين كود توجيه، سيقوم النظام بالبحث عن توجيهات الموقع حسب كود التوجيه عند إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="d3f96-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="d3f96-159">وبهذه الطريقة، يمكنك تحديد توجيهات الموقع التي يتم استخدامها لقالب معين لتوزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="d3f96-160">**إطار زمن التحقق من الصحة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="d3f96-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="d3f96-161">يحدد هذا الخيار ما إذا كان يجب تقييم الحد الأقصى للإطار الزمني عند تحديد مصدر توريد.</span><span class="sxs-lookup"><span data-stu-id="d3f96-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="d3f96-162">إذا تم تعيين هذا الخيار على *نعم*، ستتوفر الحقول التي ترتبط بالحد الأقصى والأدنى للإطارات الزمنية.</span><span class="sxs-lookup"><span data-stu-id="d3f96-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="d3f96-163">**أقصى إطار زمني:** *5*</span><span class="sxs-lookup"><span data-stu-id="d3f96-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="d3f96-164">يحدد هذا الحقل أقصى فترة بين وصول التوريد ومغادرة الطلب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d3f96-165">**وحدة أقصى إطار زمني:** *الأيام*</span><span class="sxs-lookup"><span data-stu-id="d3f96-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d3f96-166">**أدنى إطار زمني:** *0*</span><span class="sxs-lookup"><span data-stu-id="d3f96-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="d3f96-167">يحدد هذا الحقل أدنى فترة بين وصول التوريد ومغادرة الطلب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d3f96-168">**وحدة أدنى إطار زمني:** *الأيام*</span><span class="sxs-lookup"><span data-stu-id="d3f96-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d3f96-169">**نطاق أيام انتهاء الصلاحية:** *0*</span><span class="sxs-lookup"><span data-stu-id="d3f96-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="d3f96-170">*معيار تاريخ ‏‫‏‫ما تنتهي صلاحيته أولاً يصرف أولاً (FEFO):* يحدد هذا الحقل أقصى عدد للأيام بين تاريخ انتهاء صلاحية دفعة ما تنتهي صلاحيته أولا الموجودة حاليًا في المستودع والدفعة التي يتم استلامها.</span><span class="sxs-lookup"><span data-stu-id="d3f96-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="d3f96-171">في علامة التبويب السريعة **مصادر التوريد**، حدد أنواع التوريد الصالحة لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="d3f96-172">حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d3f96-173">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="d3f96-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d3f96-174">**مصدر التوريد:** *أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="d3f96-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="d3f96-175">إنشاء درجة عمل</span><span class="sxs-lookup"><span data-stu-id="d3f96-175">Create a work class</span></span>

1. <span data-ttu-id="d3f96-176">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d3f96-177">في جزء الإجراءات، حدد **جديد** لإنشاء فئة عمل.</span><span class="sxs-lookup"><span data-stu-id="d3f96-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="d3f96-178">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-178">Set the following values:</span></span>

    - <span data-ttu-id="d3f96-179">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d3f96-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d3f96-180">**الوصف:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="d3f96-181">**نوع أمر العمل:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="d3f96-182">إنشاء قالب عمل</span><span class="sxs-lookup"><span data-stu-id="d3f96-182">Create a work template</span></span>

1. <span data-ttu-id="d3f96-183">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d3f96-184">قم بتعيين حقل **نوع أمر العمل** إلى *توزيع البضائع*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d3f96-185">في جزء الإجراءات، حدد **جديد** لإضافة سطر إلى علامة تبويب **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="d3f96-186">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-187">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="d3f96-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d3f96-188">**قالب العمل:** *توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="d3f96-189">**وصف قالب العمل:** *توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="d3f96-190">حدد **حفظ** لجعل علامة التبويب السريعة **تفاصيل قالب العمل** متاحة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d3f96-191">في علامة التبويب السريعة **تفاصيل قالب العمل**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f96-192">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-193">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="d3f96-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d3f96-194">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d3f96-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d3f96-195">حدد **جديد** لإضافة سطر آخر، ثم قم بتعيين القيم التالية عليه:</span><span class="sxs-lookup"><span data-stu-id="d3f96-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="d3f96-196">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d3f96-197">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d3f96-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d3f96-198">حدد **حفظ**، وتأكد من أنه تم تحديد خانة الاختيار **صالح** لقالب *توزيع البضائع 51*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="d3f96-199">يجب أن تكون معرفات فئة العمل لأنواع عمل *الانتقاء* و *الوضع* متطابقة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="d3f96-200">إنشاء توجيات الموقع</span><span class="sxs-lookup"><span data-stu-id="d3f96-200">Create location directives</span></span>

1. <span data-ttu-id="d3f96-201">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d3f96-202">في الجزء الأيسر، قم بتعيين حقل **نوع أمر العمل** إلى *توزيع البضائع*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d3f96-203">في جزء الإجراءات، حدد **جديد**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="d3f96-204">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="d3f96-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d3f96-205">**الاسم:** *إيداع توزيع البضائع 51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="d3f96-206">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d3f96-207">**الموقع:** *5*</span><span class="sxs-lookup"><span data-stu-id="d3f96-207">**Site:** *5*</span></span>
    - <span data-ttu-id="d3f96-208">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d3f96-209">حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d3f96-210">في علامة التبويب السريعة **السطور**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f96-211">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-212">**من الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="d3f96-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d3f96-213">**إلى الكمية:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d3f96-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="d3f96-214">حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d3f96-215">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f96-216">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-217">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="d3f96-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="d3f96-218">**استخدام الموقع الثابت:** *المواقع الثابتة وغير الثابتة*</span><span class="sxs-lookup"><span data-stu-id="d3f96-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="d3f96-219">حدد **حفظ** لتجعل زر **تحرير الاستعلام** في شريط أدوات **لإجراءات توجيه الموقع** متاحًا.</span><span class="sxs-lookup"><span data-stu-id="d3f96-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="d3f96-220">حدد **تحرير الاستعلام** لفتح محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="d3f96-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="d3f96-221">من علامة التبويب **النطاق**، تأكد من تكوين السطرين التاليين:</span><span class="sxs-lookup"><span data-stu-id="d3f96-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="d3f96-222">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="d3f96-222">Line 1:</span></span>

        - <span data-ttu-id="d3f96-223">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d3f96-224">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d3f96-225">**الحقل:** *المستودع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="d3f96-226">**المعايير:** *51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="d3f96-227">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="d3f96-227">Line 2:</span></span>

        - <span data-ttu-id="d3f96-228">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d3f96-229">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d3f96-230">**الحقل:** *الموقع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="d3f96-231">**المعايير:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="d3f96-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="d3f96-232">حدد **موافق** لإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="d3f96-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d3f96-233">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="d3f96-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d3f96-234">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d3f96-235">في قائمة أصناف القائمة الموجودة في الجزء الأيمن، حدد **إبعاد الشراء**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="d3f96-236">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-236">Select **Edit**.</span></span>
1. <span data-ttu-id="d3f96-237">في علامة التبويب السريعة **فئات العمل**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f96-238">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-239">**معرف فئة العمل:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d3f96-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d3f96-240">**نوع أمر العمل:** *توزيع البضائع*</span><span class="sxs-lookup"><span data-stu-id="d3f96-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="d3f96-241">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d3f96-242">سيناريو</span><span class="sxs-lookup"><span data-stu-id="d3f96-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d3f96-243">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="d3f96-243">Create a purchase order</span></span>

<span data-ttu-id="d3f96-244">اتبع الخطوات التالية لإنشاء أمر شراء كمصدر للتوريد.</span><span class="sxs-lookup"><span data-stu-id="d3f96-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="d3f96-245">انتقل إلى **التدبير والتوريد \> أوامر الشراء \> كل أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d3f96-246">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d3f96-247">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d3f96-248">**حساب المورّد:** *104*</span><span class="sxs-lookup"><span data-stu-id="d3f96-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d3f96-249">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d3f96-250">حدد **موافق**، وقم بتدوين رقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="d3f96-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="d3f96-251">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d3f96-252">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-253">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d3f96-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d3f96-254">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="d3f96-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="d3f96-255">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="d3f96-255">Create a sales order</span></span>

<span data-ttu-id="d3f96-256">اتبع الخطوات التالية لإنشاء أمر مبيعات كمصدر للطلب.</span><span class="sxs-lookup"><span data-stu-id="d3f96-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="d3f96-257">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d3f96-258">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d3f96-259">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d3f96-260">**حساب العميل:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d3f96-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d3f96-261">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="d3f96-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d3f96-262">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-262">Select **OK**.</span></span>
1. <span data-ttu-id="d3f96-263">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d3f96-264">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d3f96-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="d3f96-265">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d3f96-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d3f96-266">**الكمية:** *3*</span><span class="sxs-lookup"><span data-stu-id="d3f96-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="d3f96-267">إنشاء توزيع البضائع المخطط</span><span class="sxs-lookup"><span data-stu-id="d3f96-267">Create planned cross-docking</span></span>

<span data-ttu-id="d3f96-268">اتبع هذه الخطوات لإنشاء توزيع البضائع المخطط من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d3f96-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="d3f96-269">في صفحة **تفاصيل أمر المبيعات** لأمر المبيعات الذي قمت بإنشائه الآن، في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **الإصدار للمستودع**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d3f96-270">يقوم إجراء الإصدار إلى المستودع بإنشاء شحنة وبند حمل لسطر أمر المبيعات، ويحاول تخصيص المخزون.</span><span class="sxs-lookup"><span data-stu-id="d3f96-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="d3f96-271">ستتلقى رسالة معلوماتية.</span><span class="sxs-lookup"><span data-stu-id="d3f96-271">You receive an informational message.</span></span> <span data-ttu-id="d3f96-272">ستتلقى أيضًا رسالة التحذير التالية: "لم يتم إنشاء عمل للموجة XXXX.</span><span class="sxs-lookup"><span data-stu-id="d3f96-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="d3f96-273">راجع سجل محفوظات إنشاء العمل للحصول على التفاصيل."</span><span class="sxs-lookup"><span data-stu-id="d3f96-273">See the work creation history log for details."</span></span> <span data-ttu-id="d3f96-274">هذا السلوك متوقع، نظرا لعدم وجود مخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="d3f96-275">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المستودع**، حدد **تفاصيل الشحنة**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="d3f96-276">تظهر صفحة **تفاصيل الشحنة** وتظهر الشحنة التي تم إنشاؤها لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d3f96-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="d3f96-277">في علامة التبويب السريعة **بنود الحمل**، لاحظ أن حقل **كمية توزيع البضائع المخطط** قد تم تعيينه إلى *3*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="d3f96-278">ونظرا لأنه لا يتوفر مخزون في المستودع، ولكن سيصل مصدر التوريد الصالح خلال الإطار الزمني المحدد في قالب توزيع البضائع، فقد تم إنشاء كمية توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="d3f96-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="d3f96-279">في علامة التبويب السريعة **بنود الحمل**، حدد **توزيع البضائع المخطط** لعرض تفاصيل توزيع البضائع التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="d3f96-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="d3f96-280">معالجة توزيع البضائع</span><span class="sxs-lookup"><span data-stu-id="d3f96-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="d3f96-281">استلام أمر الشراء في تطبيق المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="d3f96-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="d3f96-282">سيستلم النظام الكمية 5 من أمر الشراء إلى موقع الاستلام ويقوم بإنشاء نوعين من العمل.</span><span class="sxs-lookup"><span data-stu-id="d3f96-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="d3f96-283">يحتوي معرف العمل الأول الذي تم إنشاؤه على **نوع أمر عمل** بقيمة *توزيع البضائع* ويتم ربطه بأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d3f96-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="d3f96-284">وهو يتضمن الكمية 3 ويتم توجيهها إلى موقع الشحن النهائي لكي يمكن شحنها فورا.</span><span class="sxs-lookup"><span data-stu-id="d3f96-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="d3f96-285">يحتوي معرف العمل الثاني الذي تم إنشاؤه على **نوع أمر عمل** بقيمة *أوامر الشراء* ويتم ربطه بأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d3f96-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="d3f96-286">ويحتوي على الكمية المتبقية 2 والتي لم يتم توزيعها ويتم توجيهها إلى الإبعاد للتخزين.</span><span class="sxs-lookup"><span data-stu-id="d3f96-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="d3f96-287">سجل الدخول إلى الجهاز المحمول كمستخدم في المستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="d3f96-288">الانتقال إلى **الوارد \> استلام الشراء**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="d3f96-289">في حقل **رقم أمر الشراء**، أدخل رقم أمر الشراء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d3f96-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="d3f96-290">في حقل **كمية**، أدخل *5*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="d3f96-291">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-291">Select **OK**.</span></span>
1. <span data-ttu-id="d3f96-292">في الصفحة التالية، قم بتعيين حقل **الصنف** إلى *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="d3f96-293">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-293">Select **OK**.</span></span>
1. <span data-ttu-id="d3f96-294">في الصفحة التالية، قم بتأكيد **رقم أمر الشراء** و **الصنف** و **الكمية** بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="d3f96-295">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="d3f96-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d3f96-296">حدد **إلغاء** للخروج.</span><span class="sxs-lookup"><span data-stu-id="d3f96-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="d3f96-297">الإبعاد لتوزيع البضائع والتجميع</span><span class="sxs-lookup"><span data-stu-id="d3f96-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="d3f96-298">حاليًا، يتضمن كل من معرفي العمل نفس لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="d3f96-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="d3f96-299">لإكمال الخطوات التالية، يجب الحصول على معرف العمل ومعرف لوحة الترخيص المستهدفة.</span><span class="sxs-lookup"><span data-stu-id="d3f96-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="d3f96-300">يمكنك الحصول على هذه المعلومات من تفاصيل العمل الخاصة بسطر أمر الشراء وسطر أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="d3f96-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="d3f96-301">وبدلا من ذلك، يمكن الانتقال إلى **إدارة المستودع \> العمل \> تفاصيل العمل** وقم بالتصفية للعمل الذي تكون قيمة **المستودع** له *51*.</span><span class="sxs-lookup"><span data-stu-id="d3f96-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="d3f96-302">على الجهاز المحمول، انتقل إلى **الوارد \> إبعاد الشراء**، ثم أدخل لوحة الترخيص المستهدفة من العمل.</span><span class="sxs-lookup"><span data-stu-id="d3f96-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="d3f96-303">في حقل **المعرف**، أدخل معرف لوحة الترخيص الهدف من تفاصيل العمل.</span><span class="sxs-lookup"><span data-stu-id="d3f96-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="d3f96-304">تظهر صفحة انتقاء توزيع البضائع موقع الانتقاء (*RECV*) ولوحة الترخيص الهدف (*لوحة الترخيص*) والصنف (*A0001*) والكمية (*3*).</span><span class="sxs-lookup"><span data-stu-id="d3f96-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="d3f96-305">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-305">Select **OK**.</span></span>
1. <span data-ttu-id="d3f96-306">في حقل **لوحة الترخيص الهدف**، أدخل لوح الترخيص الهدف لمعرف لوحة الترخيص الذي يجب وضعه (توزيعه) إلى موقع الشحن.</span><span class="sxs-lookup"><span data-stu-id="d3f96-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="d3f96-307">يمكنك تحديد أي معرف لوحة الترخيص من اختيارك.</span><span class="sxs-lookup"><span data-stu-id="d3f96-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="d3f96-308">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-308">Select **OK**.</span></span>
1. <span data-ttu-id="d3f96-309">في الصفحة التالية في حقل **المعرف**، أدخل معرف لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="d3f96-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="d3f96-310">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-310">Select **OK**.</span></span>
1. <span data-ttu-id="d3f96-311">قم بتأكيد العمل لانتقاء باقي الكمية 2، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="d3f96-312">في الصفحة التالية، حدد **تم** لإنهاء عملية الانتقاء وبدء عملية الإبعاد.</span><span class="sxs-lookup"><span data-stu-id="d3f96-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="d3f96-313">يعرض لك تطبيق الأجهزة المحمولة المكان ولوحة الترخيص لوضع الصنف فيه.</span><span class="sxs-lookup"><span data-stu-id="d3f96-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="d3f96-314">قم بتأكيد **وضع** التخزين المجمع بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="d3f96-315">في الصفحة التالية، قم بتأكيد **وضع** توزيع البضائع بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3f96-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="d3f96-316">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="d3f96-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d3f96-317">حدد **إلغاء** للخروج.</span><span class="sxs-lookup"><span data-stu-id="d3f96-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="d3f96-318">يبين الرسم التوضيحي التالي كيف يظهر عمل توزيع البضائع المكتمل في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3f96-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d3f96-319">![اكتمال عمل توزيع البضائع](media/PlannedCrossDockingWork.png "اكتمال عمل توزيع البضائع")</span><span class="sxs-lookup"><span data-stu-id="d3f96-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]