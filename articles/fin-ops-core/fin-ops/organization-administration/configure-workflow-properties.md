---
title: تكوين خصائص سير العمل
description: يوضح هذا الموضوع كيفية تكوين مختلف خصائص لسير العمل.
author: sericks007
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268448049955170b8eb9e64cbd50416565a041b1
ms.sourcegitcommit: 561d06c2a74602dfaa40334d8afac5053aebc055
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/07/2020
ms.locfileid: "3541099"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="5aca3-103">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="5aca3-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aca3-104">يوضح هذا الموضوع كيفية تكوين مختلف خصائص لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="5aca3-105">لتكوين خصائص سير العمل، افتح سير العمل في محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="5aca3-106">انقر فوق لوحة محرر سير العمل، ثم انقر **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="5aca3-107">يمكنك استخدام الإجراءات التالية لتكوين مختلف خصائص سير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="5aca3-108">تسمية سير العمل</span><span class="sxs-lookup"><span data-stu-id="5aca3-108">Name the workflow</span></span>

<span data-ttu-id="5aca3-109">اتبع الخطوات التالية لإدخال اسم لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="5aca3-110">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5aca3-111">في الحقل **الاسم**، أدخل اسمًا فريدًا لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="5aca3-112">على سبيل المثال، إذا أنشأت سير عمل طلب شراء لكل بلد/منطقة تعمل فيها، فيمكنك تسمية سير عمل طلب الشراء **طلبات الشراء الخاصة بالدانمارك** أو **طلبات الشراء الخاصة بأسبانيا**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="5aca3-113">تحديد مالك سير العمل</span><span class="sxs-lookup"><span data-stu-id="5aca3-113">Specify the workflow owner</span></span>

<span data-ttu-id="5aca3-114">يعد مالك سير العمل الشخص الذي يدير سير العمل هذا ويحافظ عليه.</span><span class="sxs-lookup"><span data-stu-id="5aca3-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="5aca3-115">اتبع الخطوات التالية لتحديد مالك سير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="5aca3-116">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5aca3-117">من قائمة **المالك**، حدد اسم الشخص الذي سيدير سير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="5aca3-118">تحديد قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="5aca3-118">Select an email template</span></span>

<span data-ttu-id="5aca3-119">اتبع هذه الخطوات لتحديد قالب البريد الإلكتروني الذي يستخدم لإنشاء رسائل الإخطار الخاصة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="5aca3-120">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5aca3-121">في قائمة **قالب البريد الإلكتروني لإخطارات سير العمل**، حدد القالب.</span><span class="sxs-lookup"><span data-stu-id="5aca3-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="5aca3-122">إدخال إرشادات للمستخدمين</span><span class="sxs-lookup"><span data-stu-id="5aca3-122">Enter instructions for users</span></span>

<span data-ttu-id="5aca3-123">يمكنك توفير إرشادات للمستخدمين الذين يرسلون المستندات للمعالجة والاعتماد.</span><span class="sxs-lookup"><span data-stu-id="5aca3-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="5aca3-124">كما يشار إلى هؤلاء المستخدمين باسم *المنشئين*.</span><span class="sxs-lookup"><span data-stu-id="5aca3-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="5aca3-125">على سبيل المثال، تقوم بإنشاء سير عمل طلب شراء، وتدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="5aca3-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="5aca3-126">سيتمكن عندئذٍ المستخدمون الذي يدخلون طلبات الشراء في صفحة **طلبات الشراء** من رؤية هذه الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="5aca3-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="5aca3-127">لعرض الإرشادات، ينقر المنشئ فوق الأيقونة في شريط رسائل سير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="5aca3-128">اتبع الخطوات التالية لإدخال إرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="5aca3-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="5aca3-129">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5aca3-130">في حقل **إرشادات الإرسال‬**، أدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="5aca3-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="5aca3-131">لتخصيص الإرشادات، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="5aca3-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="5aca3-132">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما تظهر الإرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="5aca3-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="5aca3-133">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="5aca3-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="5aca3-134">انقر في حقل **إرشادات الإرسال** لتحديد المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="5aca3-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5aca3-135">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5aca3-136">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="5aca3-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5aca3-137">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-137">Click **Insert**.</span></span>

4. <span data-ttu-id="5aca3-138">لإضافة ترجمات الإرشادات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5aca3-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="5aca3-139">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="5aca3-140">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5aca3-141">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="5aca3-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="5aca3-142">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="5aca3-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5aca3-143">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="5aca3-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="5aca3-144">للحصول على إرشادات حول كيفية إدخال عنصر نائب، راجع الخطوة رقم 3.</span><span class="sxs-lookup"><span data-stu-id="5aca3-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="5aca3-145">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="5aca3-146">تحديد متى يتم استخدام سير العمل هذا من خلال شروط التنشيط</span><span class="sxs-lookup"><span data-stu-id="5aca3-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="5aca3-147">يمكنك إنشاء مهام سير عمل متعددة تستند إلى نوع سير العمل نفسه.</span><span class="sxs-lookup"><span data-stu-id="5aca3-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="5aca3-148">في حالة توفّر عمليات سير عمل متعددة تستند إلى النوع نفسه، يجب تحديد وقت استخدام كل سير عمل باستخدام شروط التنشيط.</span><span class="sxs-lookup"><span data-stu-id="5aca3-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="5aca3-149">في حال عدم استيفاء شروط التنشيط، يتم استخدام سير العمل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="5aca3-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="5aca3-150">بطريقة مماثلة، في حال تم تحديد تكوين سير عمل واحد فقط لنوع سير العمل، سيتم عندئذٍ استخدام تكوين سير العمل هذا بغض النظر عن شروط التنشيط.</span><span class="sxs-lookup"><span data-stu-id="5aca3-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="5aca3-151">على سبيل المثال، يمكنك إنشاء سير عمل طلب شراء لكل بلد/منطقة تعمل فيها، مثل طلبات الشراء الخاصة بالدانمارك وطلبات الشراء الخاصة بأسبانيا، مع الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="5aca3-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="5aca3-152">يتم استخدام طلبات الشراء الخاصة بالدانمارك في الحالة التالية: البلد/المنطقة = DK.</span><span class="sxs-lookup"><span data-stu-id="5aca3-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="5aca3-153">يتم استخدام طلبات الشراء الخاصة بأسبانيا في الحالة التالية: البلد/المنطقة = ES.</span><span class="sxs-lookup"><span data-stu-id="5aca3-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="5aca3-154">اتبع الخطوات التالية لتحديد متى ينبغي استخدام سير العمل الذي تقوم بتكوينه.</span><span class="sxs-lookup"><span data-stu-id="5aca3-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="5aca3-155">في الجزء الأيمن، انقر فوق **التنشيط**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="5aca3-156">حدد خانة الاختيار **تعيين شروط تشغيل سير العمل هذا‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="5aca3-157">انقر فوق **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="5aca3-158">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="5aca3-158">Enter a condition.</span></span>
5. <span data-ttu-id="5aca3-159">أدخل أية شروط إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5aca3-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="5aca3-160">قم بتشغيل سير العمل مع بعض السجلات الهدف للتحقق من أن الشرط يتضمن ويستبعد السجلات بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="5aca3-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="5aca3-161">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="5aca3-161">Specify when notifications are sent</span></span>

<span data-ttu-id="5aca3-162">عندما إرسال مستند للمعالجة، يتم إنشاء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="5aca3-163">ويمكنك إرسال إخطارات إلى المستخدمين عند بدء مثيلات سير العمل التي تستند إلى سير العمل أو عند إكمالها أو إلغائها أو إيقافها نظرًا لحدوث خطأ.</span><span class="sxs-lookup"><span data-stu-id="5aca3-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="5aca3-164">اتبع الخطوات التالية لتحديد أوقات إرسال الإخطارات.</span><span class="sxs-lookup"><span data-stu-id="5aca3-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="5aca3-165">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="5aca3-166">حدد خانة الاختيار لكل حدث من المفترض أن يؤدي إلى تشغيل الإخطارات‬:</span><span class="sxs-lookup"><span data-stu-id="5aca3-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="5aca3-167">**تم البدء** — إرسال إخطارات عند بدء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="5aca3-168">**متوقف** — إرسال إخطارات عند توقف مثيل سير عمل نظرًا لحدوث خطأ.</span><span class="sxs-lookup"><span data-stu-id="5aca3-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="5aca3-169">**مكتمل** — إرسال إخطارات عند اكتمال مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="5aca3-170">**غير قابل للاسترداد‬** — إرسال إخطارات عند توقف مثيل سير عمل نظرًا لحدوث خطأ غير قابل للاسترداد‬.</span><span class="sxs-lookup"><span data-stu-id="5aca3-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="5aca3-171">**تم الإنهاء‬** — إرسال إخطارات عند إنهاء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="5aca3-172">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="5aca3-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="5aca3-173">في علامة التبويب **نص الإخطار‬**، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="5aca3-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="5aca3-174">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="5aca3-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="5aca3-175">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر النص للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="5aca3-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="5aca3-176">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="5aca3-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="5aca3-177">انقر داخل الحقل لتحديد المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="5aca3-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5aca3-178">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5aca3-179">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="5aca3-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5aca3-180">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="5aca3-181">عنصر نائب شائع **نص الإعلام** يجب تضمينه هو "الملاحظات الأخيرة: %Workflow.Last note%"، وهو يعرض تعليقات من الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="5aca3-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="5aca3-182">لإضافة ترجمات النص، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5aca3-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="5aca3-183">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="5aca3-184">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="5aca3-185">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="5aca3-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="5aca3-186">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="5aca3-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5aca3-187">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="5aca3-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="5aca3-188">للحصول على إرشادات حول كيفية إدخال عنصر نائب، راجع الخطوة رقم 5.</span><span class="sxs-lookup"><span data-stu-id="5aca3-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="5aca3-189">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-189">Click **Close**.</span></span>

7. <span data-ttu-id="5aca3-190">في علامة تبويب **المستلم**، استخدم الخيارات التالية لتحديد الشخص الذي سيتلقى الإخطارات.</span><span class="sxs-lookup"><span data-stu-id="5aca3-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5aca3-191">خيار</span><span class="sxs-lookup"><span data-stu-id="5aca3-191">Option</span></span></th>
    <th><span data-ttu-id="5aca3-192">يتم إرسال الإخطارات إلى هؤلاء المستخدمين</span><span class="sxs-lookup"><span data-stu-id="5aca3-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="5aca3-193">لإرسال الإخطارات، اتبع الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="5aca3-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5aca3-194">المشارك</span><span class="sxs-lookup"><span data-stu-id="5aca3-194">Participant</span></span></td>
    <td><span data-ttu-id="5aca3-195">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="5aca3-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5aca3-196">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>المشترك</strong>.</span><span class="sxs-lookup"><span data-stu-id="5aca3-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="5aca3-197">في علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="5aca3-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="5aca3-198">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="5aca3-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5aca3-199">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="5aca3-199">Workflow user</span></span></td>
    <td><span data-ttu-id="5aca3-200">المستخدمون المشاركون في سير العمل هذا</span><span class="sxs-lookup"><span data-stu-id="5aca3-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5aca3-201">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>مستخدم سير العمل</strong>.</span><span class="sxs-lookup"><span data-stu-id="5aca3-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="5aca3-202">في علامة تبويب <strong>مستخدم سير العمل</strong>، في قائمة <strong>مستخدم سير العمل</strong>، حدد أحد المشاركين في سير العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="5aca3-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5aca3-203">المستخدم</span><span class="sxs-lookup"><span data-stu-id="5aca3-203">User</span></span></td>
    <td><span data-ttu-id="5aca3-204">مستخدمون محددون</span><span class="sxs-lookup"><span data-stu-id="5aca3-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5aca3-205">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="5aca3-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="5aca3-206">على علامة تبويب <strong>المستخدم</strong>، تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="5aca3-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5aca3-207">حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="5aca3-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="5aca3-208">كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="5aca3-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="5aca3-209">أدخل تعليقات حول التغييرات التي قمت بها في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="5aca3-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="5aca3-210">لإدخال تعليقات حول التغييرات التي قمت بها في سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5aca3-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="5aca3-211">في الجزء الأيمن، انقر فوق **الملاحظات**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="5aca3-212">في الحقل **إدخال التعليقات الخاصة بسير العمل‬**، أدخل تعليقاتك.</span><span class="sxs-lookup"><span data-stu-id="5aca3-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="5aca3-213">راجع تعليقاتك.</span><span class="sxs-lookup"><span data-stu-id="5aca3-213">Review your comments.</span></span> <span data-ttu-id="5aca3-214">بعد إضافة التعليقات، لا يمكنك تعديلها.</span><span class="sxs-lookup"><span data-stu-id="5aca3-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="5aca3-215">انقر فوق **إضافة** لإضافة التعليقات إلى ناحية **سجل التعليقات‬**.</span><span class="sxs-lookup"><span data-stu-id="5aca3-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
