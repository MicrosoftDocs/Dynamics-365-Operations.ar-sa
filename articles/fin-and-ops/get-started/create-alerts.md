---
title: "إنشاء قواعد تنبيه"
description: "يشمل هذا الموضوع معلومات حول التنبيهات ويوضح كيفية إنشاء قاعدة تنبيه بحيث يتم إعلامك بالأحداث مثل تاريخ يتم بلوغه أو تغييرًا محددًا يحدث."
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: cbf4917424e72a70a6d513b5daf45f6bf9cd57c7
ms.contentlocale: ar-sa
ms.lasthandoff: 12/18/2018

---

# <a name="create-alert-rules"></a><span data-ttu-id="71d4f-103">إنشاء قواعد تنبيه</span><span class="sxs-lookup"><span data-stu-id="71d4f-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="71d4f-104">بدء الاستخدام</span><span class="sxs-lookup"><span data-stu-id="71d4f-104">Getting started</span></span>

<span data-ttu-id="71d4f-105">قبل إعداد قاعدة تنبيه، قرر متى وفي أي مواقف تحتاج فيها إلى تلقي التنبيهات.</span><span class="sxs-lookup"><span data-stu-id="71d4f-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="71d4f-106">عندما تعرف الحدث الذي تريد إعلامك به، في Microsoft Dynamics 365 for Finance and Operations، ابحث عن الصحة التي توجد فيها البيانات التي تؤدي إلى ظهور هذا الحدث.</span><span class="sxs-lookup"><span data-stu-id="71d4f-106">When you know which event you want to be notified about, in Microsoft Dynamics 365 for Finance and Operations find the page where the data that causes that event appears.</span></span> <span data-ttu-id="71d4f-107">يمكن أن يكون الحدث تاريخًا يتم بلوغه أو تغييرًا محددًا يحدث.</span><span class="sxs-lookup"><span data-stu-id="71d4f-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="71d4f-108">لذلك، يجب البحث عن الصفحة التي يتم فيها تحديد التاريخ، أو الحقل الذي تظهر فيها هذه التغييرات أو السجل الجديد الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="71d4f-109">بعد أن تتوفر لديك هذه المعلومات، يمكنك إنشاء قاعدة التنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="71d4f-110">عندما تقوم بإنشاء قاعدة تنبيه، يمكنك تحديد المعايير التي يجب أن تتحقق قبل أن يتم تشغيل أحد التنبيهات.</span><span class="sxs-lookup"><span data-stu-id="71d4f-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="71d4f-111">ويمكنك التفكير في معايير تمثل حالة من التوافق بين حدوث حدث وتحقق شروط محددة.</span><span class="sxs-lookup"><span data-stu-id="71d4f-111">You can think of criteria as a match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="71d4f-112">وعند حدوث حدث معين، يبدأ النظام في إجراء فحص وفقًا للشروط التي تم إعدادها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="71d4f-112">When an event occurs, the system starts to perform a check according to the conditions that are set up in Finance and Operations.</span></span>

## <a name="events"></a><span data-ttu-id="71d4f-113">الأحداث</span><span class="sxs-lookup"><span data-stu-id="71d4f-113">Events</span></span>

<span data-ttu-id="71d4f-114">قد يكون الحدث الذي يقوم بتشغيل قاعدة تنبيه تاريخ يتم بلوغه أو تغييرًا محددًا يحدث.</span><span class="sxs-lookup"><span data-stu-id="71d4f-114">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="71d4f-115">يتم تحديد مشغلات الأحداث في علامة التبويب السريعة **تنبيهي عند** في مربع الحوار **إنشاء قاعدة تنبيه**.</span><span class="sxs-lookup"><span data-stu-id="71d4f-115">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="71d4f-116">تعتمد الأحداث المتوفرة لحقل محدد على المشغل الذي تم تحديده.</span><span class="sxs-lookup"><span data-stu-id="71d4f-116">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="71d4f-117">على سبيل المثال، إذا كنت تقوم بإعداد قاعدة تنبيه لحقل **تاريخ البدء**، تكون أحداث تواريخ الاستحقاق‬ مناسبة.</span><span class="sxs-lookup"><span data-stu-id="71d4f-117">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="71d4f-118">ولذلك، يكون نوع الحدث **مستحق في‬** متوفرًا لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="71d4f-118">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="71d4f-119">ومع ذلك، بالنسبة لحقل مثل **مركز التكلفة**، لا يكون حدث تاريخ الاستحقاق مناسبًا.</span><span class="sxs-lookup"><span data-stu-id="71d4f-119">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="71d4f-120">ولذلك، يكون نوع الحدث **مستحق في‬** غير متوفر.</span><span class="sxs-lookup"><span data-stu-id="71d4f-120">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="71d4f-121">بدلاً من ذلك، يكون نوع الحدث **تم تغييره** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="71d4f-121">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="71d4f-122">أنواع الحدث</span><span class="sxs-lookup"><span data-stu-id="71d4f-122">Event types</span></span>

<span data-ttu-id="71d4f-123">يمكن أن تحدث ثلاثة أنواع من الأحداث:</span><span class="sxs-lookup"><span data-stu-id="71d4f-123">Three types of events can occur:</span></span>

- <span data-ttu-id="71d4f-124">**أحداث إنشاء-نوع وحذف-نوع‬** - تشغل هذه الأحداث أحد التنبيهات عندما يتم إنشاء سجل أو حذفه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-124">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="71d4f-125">**أحداث من نوع التحديث** - تشغل هذه الأحداث أحد التنبيهات عندما تتغير البيانات الموجودة في حقل معين.</span><span class="sxs-lookup"><span data-stu-id="71d4f-125">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="71d4f-126">**أحداث من نوع تاريخ الاستحقاق** - تشغل هذه الأحداث أحد التنبيهات عندما تصل إلى تاريخ.</span><span class="sxs-lookup"><span data-stu-id="71d4f-126">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="71d4f-127">يمكن للتغييرات التي تحدث أن تبدأ من قِبل مستخدم.</span><span class="sxs-lookup"><span data-stu-id="71d4f-127">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="71d4f-128">على سبيل المثال، يقوم مستخدم بتغيير تاريخ التسليم لأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="71d4f-128">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="71d4f-129">بدلاً من ذلك، يمكن أن تحدث التغييرات كجزء من عملية.</span><span class="sxs-lookup"><span data-stu-id="71d4f-129">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="71d4f-130">على سبيل المثال، يتغير الحقل **حالة** في صفحة لإظهار دورة حياة العديد من العمليات في النظام.</span><span class="sxs-lookup"><span data-stu-id="71d4f-130">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="71d4f-131">الحالات</span><span class="sxs-lookup"><span data-stu-id="71d4f-131">Conditions</span></span>

<span data-ttu-id="71d4f-132">في علامة التبويب السريعة **التنبيه عن** في مربع الحوار **إنشاء قاعدة تنبيه‬**، يمكنك استخدام الشروط للتحكم عندما يتم تنبيهك بشأن أحداث.</span><span class="sxs-lookup"><span data-stu-id="71d4f-132">On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="71d4f-133">على سبيل المثال، يمكنك تحديد أن النظام يجب أن يقوم بتنبيهك عندما تتغير حالة أوامر الشراء، ولكن فقط إذا كانت الحالة تتطابق مع مجموعة معينة من الشروط.</span><span class="sxs-lookup"><span data-stu-id="71d4f-133">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="71d4f-134">بشكل خاص، أنت تريد أن تتلقى تنبيهًا عندما يتم تعيين حالة أمر الشراء إلى **مُستَلم**.</span><span class="sxs-lookup"><span data-stu-id="71d4f-134">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="71d4f-135">هذا التغيير في الحالة هو الحدث الذي يشغل التنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-135">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="71d4f-136">بعد ذلك، يجب أن تحدد أوامر الشراء التي ترغب في أن يتم تنبيهك إليها.</span><span class="sxs-lookup"><span data-stu-id="71d4f-136">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="71d4f-137">على سبيل المثال، يمكنك تحديد أحد الخيارات التالية.</span><span class="sxs-lookup"><span data-stu-id="71d4f-137">For example, you can select one of the following options.</span></span> <span data-ttu-id="71d4f-138">تحديد هذه الخيارات شروط قاعدة التنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-138">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="71d4f-139">**السجل الحالي المحدد** -تتلقى تنبيهًا عندما تتغير حالة أمر شراء محدد إلى **مُستَلم‬**.</span><span class="sxs-lookup"><span data-stu-id="71d4f-139">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="71d4f-140">**جميع السجلات** - تتلقى تحذيرًا عند تغيير حالة أمر شراء لصنف في طريقة عرض الصفحة النشطة.</span><span class="sxs-lookup"><span data-stu-id="71d4f-140">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="71d4f-141">يمكنك استخدام التصفية المتقدمة المتوفرة على الصفحة لإنشاء قواعد لمجموعة معينة من السجلات.</span><span class="sxs-lookup"><span data-stu-id="71d4f-141">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="71d4f-142">على سبيل المثال، يمكنك إنشاء تنبيه يتم تشغيله لجميع أوامر الشراء للعملاء في مجموعة عملاء محددة.</span><span class="sxs-lookup"><span data-stu-id="71d4f-142">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="71d4f-143">انتهاء صلاحية القاعدة</span><span class="sxs-lookup"><span data-stu-id="71d4f-143">Expiry of rule</span></span>

<span data-ttu-id="71d4f-144">في علامة التبويب **‏‫التنبيه حتى‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد المدة التي يجب أن تكون قاعدة التنبيه نشطة خلالها.</span><span class="sxs-lookup"><span data-stu-id="71d4f-144">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="71d4f-145">محتويات التنبيهات</span><span class="sxs-lookup"><span data-stu-id="71d4f-145">Alert contents</span></span>

<span data-ttu-id="71d4f-146">في علامة التبويب السريعة **التنبيه باستخدام** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد نص الموضوع ونص الرسالة التي يجب أن تستخدمها رسائل التنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-146">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="71d4f-147">معرّف المستخدم</span><span class="sxs-lookup"><span data-stu-id="71d4f-147">User ID</span></span>

<span data-ttu-id="71d4f-148">في علامة التبويب السريعة **‏‫التنبيه باستخدام‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد المستخدم الذي يجب أن يتلقى رسائل التنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-148">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="71d4f-149">بشكل افتراضي، يتم تحديد معرف المستخدم الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="71d4f-149">By default, your user ID is selected.</span></span> <span data-ttu-id="71d4f-150">يتم تقييد هذا الخيار على مسؤولي المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="71d4f-150">This option is restricted to organization administrators.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="71d4f-151">إنشاء قاعدة تنبيه</span><span class="sxs-lookup"><span data-stu-id="71d4f-151">Create an alert rule</span></span>

1. <span data-ttu-id="71d4f-152">افتح الصفحة التي تحتوي على البيانات المطلوب مراقبتها.</span><span class="sxs-lookup"><span data-stu-id="71d4f-152">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="71d4f-153">في جزء الإجراءات، في علامة التبويب **خيارات**، في المجموعة **مشاركة**، حدد **إنشاء قاعدة تنبيه**.</span><span class="sxs-lookup"><span data-stu-id="71d4f-153">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="71d4f-154">في مربع الحوار **إنشاء قاعدة تنبيه**، في الحقل **حقل**، حدد الحقل المطلوب مراقبته.</span><span class="sxs-lookup"><span data-stu-id="71d4f-154">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="71d4f-155">في الحقل **حدث**، حدد نوع الحدث.</span><span class="sxs-lookup"><span data-stu-id="71d4f-155">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="71d4f-156">في علامة التبويب السريعة **‏‫التنبيه عن‬**، حدد أحد الخيارات.</span><span class="sxs-lookup"><span data-stu-id="71d4f-156">On the **Alert me for** FastTab, select an option.</span></span>
6. <span data-ttu-id="71d4f-157">إذا كان يجب أن تكون القاعدة غير نشطة في تاريخ معين، في علامة التبويب السريعة **التنبيه حتى‬**، فحدد تاريخ انتهاء.</span><span class="sxs-lookup"><span data-stu-id="71d4f-157">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="71d4f-158">في علامة التبويب السريعة **التنبيه باستخدام** في الحقل **موضوع**، اقبل عنوان الموضوع الافتراضي لرسالة البريد الإلكتروني أو أدخل موضوعًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="71d4f-158">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="71d4f-159">يتم استخدام النص كعنوان للموضوع لرسالة البريد الإلكتروني التي تتلقاها عند تشغيل تنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-159">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span>
8. <span data-ttu-id="71d4f-160">في الحقل **رسالة**، أدخل رسالة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="71d4f-160">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="71d4f-161">يتم استخدام النص كرسالة تتلقاها عند تشغيل تنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-161">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="71d4f-162">حدد **موافق** لحفظ الإعدادات وإنشاء قاعدة التنبيه.</span><span class="sxs-lookup"><span data-stu-id="71d4f-162">Select **OK** to save the settings and create the alert rule.</span></span>

