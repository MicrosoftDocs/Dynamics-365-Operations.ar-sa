---
title: إخطارات تنفيذ الموجة
description: يصف هذا الموضوع إخطارات تنفيذ الموجة ويشرح كيفية إعدادها.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 47f270b5fff37e8e231d8a9c4a011172df3d9385
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271367"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="0a39b-103">إخطارات تنفيذ الموجة</span><span class="sxs-lookup"><span data-stu-id="0a39b-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a39b-104">تستخدم ميزة *إخطارت تنفيذ الموجة* أحداث العمل ومركز العمل لتقديم الإخطارات المتعلقة بتنفيذ الموجة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="0a39b-105">يتيح لك تحديد أنواع الأحداث التي تنشئ الإشعارات والمستودعات التي تنشئها والمستخدمين الذين يستلمونها.</span><span class="sxs-lookup"><span data-stu-id="0a39b-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="0a39b-106">يشير الزر **إظهار الرسائل** (رمز الجرس) الموجود على الجانب الأيمن من شريط التنقل إلى وقت توفر رسالة مركز الإجراءات للمستخدم الحالي.</span><span class="sxs-lookup"><span data-stu-id="0a39b-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="0a39b-107">يمكن للمستخدم تحديد الزر **إظهار الرسائل** لفتح مركز الإجراء ومراجعه الرسائل.</span><span class="sxs-lookup"><span data-stu-id="0a39b-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="0a39b-108">يتم إجراء أحداث الاعمال عند تشغيل عمليات الاعمال.</span><span class="sxs-lookup"><span data-stu-id="0a39b-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="0a39b-109">تتكون عمليات الأعمال من مهام.</span><span class="sxs-lookup"><span data-stu-id="0a39b-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="0a39b-110">أثناء عملية الأعمال، يقوم المستخدمون الذين يشاركون فيها بتنفيذ إجراءات العمل لإكمال تلك المهام.</span><span class="sxs-lookup"><span data-stu-id="0a39b-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="0a39b-111">توفر أحداث العمل آلية تتيح للأنظمة الخارجية تلقي الإخطارات من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a39b-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="0a39b-112">وبهذه الطريقة، يمكن للانظمه تنفيذ إجراءات العمل كاستجابة لاحداث العمل.</span><span class="sxs-lookup"><span data-stu-id="0a39b-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="0a39b-113">لمزيد من المعلومات، راجع [نظرة عامة على أحداث الأعمال](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="0a39b-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="0a39b-114">تشغيل ميزة إخطارات تنفيذ الموجات</span><span class="sxs-lookup"><span data-stu-id="0a39b-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="0a39b-115">قبل أن تتمكن من استخدام ميزة *إخطارات تنفيذ الموجات*، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="0a39b-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="0a39b-116">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="0a39b-117">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="0a39b-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0a39b-118">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="0a39b-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0a39b-119">**اسم الميزة:** *إخطارات تنفيذ الموجات*</span><span class="sxs-lookup"><span data-stu-id="0a39b-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="0a39b-120">السيناريو: إرسال إخطارات تنفيذ دفعه الموجه إلى مركز الإجراء</span><span class="sxs-lookup"><span data-stu-id="0a39b-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="0a39b-121">يوضح هذا السيناريو التدفق الشامل لإرسال إعلامات حول أخطاء تنفيذ دفعة الموجة إلى دور معين عبر مركز الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0a39b-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="0a39b-122">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="0a39b-122">Make demo data available</span></span>

<span data-ttu-id="0a39b-123">لاتباع هذا السيناريو، يجب تثبيت بيانات العرض التوضيحي، ويجب تحديد الكيان القانوني **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="0a39b-124">التأكد من تشغيل الأمواج في وضع الدفعة</span><span class="sxs-lookup"><span data-stu-id="0a39b-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="0a39b-125">انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="0a39b-126">في علامة التبويب السريع **معالجة الموجات**، قم بتعيين خيار **معالجة موجات في دفعة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="0a39b-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="0a39b-127">إذا كنت ترغب في تعطيل إخطارات تنفيذ دفعة الموجة، فقم بتعيين خيار **تعطيل إخطارات دفعات معالجة الموجات** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="0a39b-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="0a39b-128">تكوين سياسة الإخطار بالموجة</span><span class="sxs-lookup"><span data-stu-id="0a39b-128">Configure a wave notification policy</span></span>

<span data-ttu-id="0a39b-129">تحدد سياسات اعلام الموجات أنواع الاعلامات التي يتم إرسالها والمستخدمين الذين تم اعلامهم.</span><span class="sxs-lookup"><span data-stu-id="0a39b-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="0a39b-130">انتقل إلى **إدارة المستودعات \> إعداد \> الموجات \> سياسات إخطارات الموجات**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="0a39b-131">انشئ سجلاً ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a39b-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="0a39b-132">**سياسة إخطارات الموجات:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="0a39b-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="0a39b-133">**الوصف:** *خطأ دفعة موجة المستودع 24*</span><span class="sxs-lookup"><span data-stu-id="0a39b-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="0a39b-134">**إرسال الإخطار:** *الخطأ فقط*</span><span class="sxs-lookup"><span data-stu-id="0a39b-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="0a39b-135">**إلى الدور:** *مسؤول النظام*</span><span class="sxs-lookup"><span data-stu-id="0a39b-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="0a39b-136">نظرًا لأن هذا السيناريو يستخدم بيانات العرض التوضيحي، يتم تحديد دور *مسؤول النظام* من أجل البساطة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="0a39b-137">لذلك، نظرا لأنك قمت بتسجيل الدخول كمستخدم مسؤول نظام، ستتلقى الاعلامات.</span><span class="sxs-lookup"><span data-stu-id="0a39b-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="0a39b-138">ومع ذلك، من الناحية العملية، يجب عليك عادةً تحديد دور أكثر تحديدًا للإبلاغ عن أخطاء تنفيذ دفعة الموجة، مثل *مدير المستودع*.</span><span class="sxs-lookup"><span data-stu-id="0a39b-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="0a39b-139">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="0a39b-140">قم بتكوين قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-140">Configure a wave template</span></span>

<span data-ttu-id="0a39b-141">تتيح لك القوالب الموجهة ربط مثيلات معينة من أساليب الموجة إلى قوالب تسمية الموجة المقابلة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="0a39b-142">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="0a39b-143">في جزء القائمة، قم بتعيين حقل **نوع قالب الموجة** إلى *الشحن*، ثم حدد قالب الموجة *الإعداد الافتراضي لشحن 24* للمستودع 24.</span><span class="sxs-lookup"><span data-stu-id="0a39b-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="0a39b-144">على علامة التبويب السريعةة **عام**، قم بتعيين حقل **سياسة إخطارات الموجات** إلى *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="0a39b-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="0a39b-145">تكوين قالب عمل</span><span class="sxs-lookup"><span data-stu-id="0a39b-145">Configure a work template</span></span>

<span data-ttu-id="0a39b-146">يتم استخدام قوالب العمل اثناء تنفيذ الموجه لإنشاء عمل.</span><span class="sxs-lookup"><span data-stu-id="0a39b-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="0a39b-147">بالنسبة لهذا السيناريو، يجب ان يقوم تنفيذ الموجه بتشغيل خطا.</span><span class="sxs-lookup"><span data-stu-id="0a39b-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="0a39b-148">من خلال تعيين استعلام قالب العمل لاستخدام مستودع غير موجود، سوف تتأكد من فشل تنفيذ الموجة، وبالتالي ترسل إخطارًا.</span><span class="sxs-lookup"><span data-stu-id="0a39b-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="0a39b-149">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="0a39b-150">في جزء القائمة، قم بتعيين حقل **نوع قالب العمل** إلى *أوامر المبيعات*، ثم حدد قالب عمل *مرحلة SO رقم 24* للمستودع 24.</span><span class="sxs-lookup"><span data-stu-id="0a39b-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="0a39b-151">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="0a39b-152">في مربع الحوار محرر الاستعلام، في علامة التبويب **النطاق**، قم بتحرير الصف التالي (أو إضافته إذا لم يكن موجودًا):</span><span class="sxs-lookup"><span data-stu-id="0a39b-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="0a39b-153">**الجدول:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a39b-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="0a39b-154">**الجدول المشتق:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a39b-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="0a39b-155">**الحقل:** *المستودع*</span><span class="sxs-lookup"><span data-stu-id="0a39b-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="0a39b-156">**المعايير:** قم بتغيير القيمة من *24* إلى *خطأ*.</span><span class="sxs-lookup"><span data-stu-id="0a39b-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="0a39b-157">حدد **موافق** وقم بتأكيد التغيير.</span><span class="sxs-lookup"><span data-stu-id="0a39b-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="0a39b-158">إنشاء أمر مبيعات وإصداره للمستودع</span><span class="sxs-lookup"><span data-stu-id="0a39b-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="0a39b-159">انتقل إلى **المبيعات والتسويق \> أمر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="0a39b-160">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a39b-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="0a39b-161">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0a39b-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0a39b-162">**المستودع:** *24*</span><span class="sxs-lookup"><span data-stu-id="0a39b-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="0a39b-163">على علامة التبويب السريعة **بنود أمر المبيعات**، أضف بند أمر مبيعات يحتوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a39b-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="0a39b-164">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a39b-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="0a39b-165">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a39b-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a39b-166">هذه الأصناف والكميات هي أمثلة فقط.</span><span class="sxs-lookup"><span data-stu-id="0a39b-166">These items and quantities are only examples.</span></span> <span data-ttu-id="0a39b-167">يجب أن يحتوي المستودع المحدد على مخزون كافٍ.</span><span class="sxs-lookup"><span data-stu-id="0a39b-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="0a39b-168">بينما لا يزال البند الجديد محددًا في علامة التبويب السريع **بنود أمر المبيعات**، حدد **المخزون \> الحجز** على شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="0a39b-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="0a39b-169">في صفحة **الحجز**، في جزء الإجراءات، حدد **حجز لوط**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="0a39b-170">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-170">Then close the page.</span></span>
1. <span data-ttu-id="0a39b-171">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="0a39b-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="0a39b-172">إخطارات من تنفيذ وظيفة دفعة الموجة</span><span class="sxs-lookup"><span data-stu-id="0a39b-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="0a39b-173">اعتمادًا على إعداد أحداث عملك، ستتلقى في النهاية إخطارًا حول فشل تنفيذ الموجة.</span><span class="sxs-lookup"><span data-stu-id="0a39b-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="0a39b-174">ستكون رسالة مركز الإجراءات مشابهة للمثال التالي وستتضمن ارتباطًا بالموجة التي فشلت.</span><span class="sxs-lookup"><span data-stu-id="0a39b-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="0a39b-175">**حدث خطأ أثناء تنفيذ الموجة**</span><span class="sxs-lookup"><span data-stu-id="0a39b-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="0a39b-176">حدث خطأ أثناء تنفيذ الموجة USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="0a39b-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="0a39b-177">الرسائل الأخيرة: لم يتم إنشاء أي عمل للموجة USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="0a39b-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="0a39b-178">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="0a39b-178">**STATUS**</span></span>  
> <span data-ttu-id="0a39b-179">نشط</span><span class="sxs-lookup"><span data-stu-id="0a39b-179">Active</span></span>
>
> <span data-ttu-id="0a39b-180">فتح تفاصيل الموجة</span><span class="sxs-lookup"><span data-stu-id="0a39b-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
