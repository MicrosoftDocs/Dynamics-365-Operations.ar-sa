---
title: تكوين خصائص سير العمل
description: يوضح هذا الموضوع كيفية تكوين مختلف خصائص لسير العمل.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40118f329a676ffb30870eb882d127e3eb258599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566957"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="3496a-103">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="3496a-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3496a-104">يوضح هذا الموضوع كيفية تكوين مختلف خصائص لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="3496a-105">لتكوين خصائص سير العمل، افتح سير العمل في محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="3496a-106">انقر فوق لوحة محرر سير العمل، ثم انقر **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="3496a-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3496a-107">يمكنك استخدام الإجراءات التالية لتكوين مختلف خصائص سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="3496a-108">تسمية سير العمل</span><span class="sxs-lookup"><span data-stu-id="3496a-108">Name the workflow</span></span>

<span data-ttu-id="3496a-109">اتبع الخطوات التالية لإدخال اسم لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="3496a-110">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3496a-111">في الحقل **الاسم**، أدخل اسمًا فريدًا لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="3496a-112">على سبيل المثال، إذا أنشأت سير عمل طلب شراء لكل بلد/منطقة تعمل فيها، فيمكنك تسمية سير عمل طلب الشراء **طلبات الشراء الخاصة بالدانمارك** أو **طلبات الشراء الخاصة بأسبانيا**.</span><span class="sxs-lookup"><span data-stu-id="3496a-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="3496a-113">تحديد مالك سير العمل</span><span class="sxs-lookup"><span data-stu-id="3496a-113">Specify the workflow owner</span></span>

<span data-ttu-id="3496a-114">يعد مالك سير العمل الشخص الذي يدير سير العمل هذا ويحافظ عليه.</span><span class="sxs-lookup"><span data-stu-id="3496a-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="3496a-115">اتبع الخطوات التالية لتحديد مالك سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="3496a-116">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3496a-117">من قائمة **المالك**، حدد اسم الشخص الذي سيدير سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="3496a-118">تحديد قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="3496a-118">Select an email template</span></span>

<span data-ttu-id="3496a-119">اتبع هذه الخطوات لتحديد قالب البريد الإلكتروني الذي يستخدم لإنشاء رسائل الإخطار الخاصة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="3496a-120">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3496a-121">في قائمة **قالب البريد الإلكتروني لإخطارات سير العمل**، حدد القالب.</span><span class="sxs-lookup"><span data-stu-id="3496a-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="3496a-122">إدخال إرشادات للمستخدمين</span><span class="sxs-lookup"><span data-stu-id="3496a-122">Enter instructions for users</span></span>

<span data-ttu-id="3496a-123">يمكنك توفير إرشادات للمستخدمين الذين يرسلون المستندات للمعالجة والاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3496a-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="3496a-124">كما يشار إلى هؤلاء المستخدمين باسم *المنشئين*.</span><span class="sxs-lookup"><span data-stu-id="3496a-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="3496a-125">على سبيل المثال، تقوم بإنشاء سير عمل طلب شراء، وتدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="3496a-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="3496a-126">سيتمكن عندئذٍ المستخدمون الذي يدخلون طلبات الشراء في صفحة **طلبات الشراء** من رؤية هذه الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="3496a-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="3496a-127">لعرض الإرشادات، ينقر المنشئ فوق الأيقونة في شريط رسائل سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="3496a-128">اتبع الخطوات التالية لإدخال إرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3496a-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="3496a-129">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3496a-130">في حقل **إرشادات الإرسال‬**، أدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="3496a-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="3496a-131">لتخصيص الإرشادات، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="3496a-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="3496a-132">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما تظهر الإرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3496a-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="3496a-133">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="3496a-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="3496a-134">انقر في حقل **إرشادات الإرسال** لتحديد المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="3496a-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3496a-135">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="3496a-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3496a-136">في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="3496a-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3496a-137">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="3496a-137">Click **Insert**.</span></span>

4. <span data-ttu-id="3496a-138">لإضافة ترجمات الإرشادات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="3496a-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="3496a-139">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="3496a-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="3496a-140">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="3496a-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3496a-141">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="3496a-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="3496a-142">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="3496a-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3496a-143">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="3496a-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="3496a-144">للحصول على إرشادات حول كيفية إدخال عنصر نائب، راجع الخطوة رقم 3.</span><span class="sxs-lookup"><span data-stu-id="3496a-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="3496a-145">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="3496a-145">Click **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="3496a-146">لا يمكن أضافه العناصر النائبة باستخدام copy و لصق لأنه لم يتم لصق معلومات الهدف بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="3496a-146">Placeholders cannot be added using copy and paste because the target information is not pasted in correctly.</span></span> <span data-ttu-id="3496a-147">استخدم الواجهة لأضافه عناصر نائبه.</span><span class="sxs-lookup"><span data-stu-id="3496a-147">Use the interface to add placeholders.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="3496a-148">تحديد متى يتم استخدام سير العمل هذا من خلال شروط التنشيط</span><span class="sxs-lookup"><span data-stu-id="3496a-148">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="3496a-149">يمكنك إنشاء مهام سير عمل متعددة تستند إلى نوع سير العمل نفسه.</span><span class="sxs-lookup"><span data-stu-id="3496a-149">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="3496a-150">في حالة توفّر عمليات سير عمل متعددة تستند إلى النوع نفسه، يجب تحديد وقت استخدام كل سير عمل باستخدام شروط التنشيط.</span><span class="sxs-lookup"><span data-stu-id="3496a-150">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="3496a-151">في حال عدم استيفاء شروط التنشيط، يتم استخدام سير العمل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="3496a-151">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="3496a-152">بطريقة مماثلة، في حال تم تحديد تكوين سير عمل واحد فقط لنوع سير العمل، سيتم عندئذٍ استخدام تكوين سير العمل هذا بغض النظر عن شروط التنشيط.</span><span class="sxs-lookup"><span data-stu-id="3496a-152">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="3496a-153">على سبيل المثال، يمكنك إنشاء سير عمل طلب شراء لكل بلد/منطقة تعمل فيها، مثل طلبات الشراء الخاصة بالدانمارك وطلبات الشراء الخاصة بأسبانيا، مع الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="3496a-153">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="3496a-154">يتم استخدام طلبات الشراء الخاصة بالدانمارك في الحالة التالية: البلد/المنطقة = DK.</span><span class="sxs-lookup"><span data-stu-id="3496a-154">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="3496a-155">يتم استخدام طلبات الشراء الخاصة بأسبانيا في الحالة التالية: البلد/المنطقة = ES.</span><span class="sxs-lookup"><span data-stu-id="3496a-155">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="3496a-156">اتبع الخطوات التالية لتحديد متى ينبغي استخدام سير العمل الذي تقوم بتكوينه.</span><span class="sxs-lookup"><span data-stu-id="3496a-156">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="3496a-157">في الجزء الأيمن، انقر فوق **التنشيط**.</span><span class="sxs-lookup"><span data-stu-id="3496a-157">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="3496a-158">حدد خانة الاختيار **تعيين شروط تشغيل سير العمل هذا‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-158">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="3496a-159">انقر فوق **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="3496a-159">Click **Add condition**.</span></span>
4. <span data-ttu-id="3496a-160">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="3496a-160">Enter a condition.</span></span>
5. <span data-ttu-id="3496a-161">أدخل أية شروط إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3496a-161">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="3496a-162">قم بتشغيل سير العمل مع بعض السجلات الهدف للتحقق من أن الشرط يتضمن ويستبعد السجلات بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="3496a-162">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="3496a-163">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="3496a-163">Specify when notifications are sent</span></span>

<span data-ttu-id="3496a-164">عندما إرسال مستند للمعالجة، يتم إنشاء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-164">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="3496a-165">ويمكنك إرسال إخطارات إلى المستخدمين عند بدء مثيلات سير العمل التي تستند إلى سير العمل أو عند إكمالها أو إلغائها أو إيقافها نظرًا لحدوث خطأ.</span><span class="sxs-lookup"><span data-stu-id="3496a-165">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="3496a-166">اتبع الخطوات التالية لتحديد أوقات إرسال الإخطارات.</span><span class="sxs-lookup"><span data-stu-id="3496a-166">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="3496a-167">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-167">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="3496a-168">حدد خانة الاختيار لكل حدث من المفترض أن يؤدي إلى تشغيل الإخطارات‬:</span><span class="sxs-lookup"><span data-stu-id="3496a-168">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="3496a-169">**تم البدء** — إرسال إخطارات عند بدء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-169">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="3496a-170">**متوقف** — إرسال إخطارات عند توقف مثيل سير عمل نظرًا لحدوث خطأ.</span><span class="sxs-lookup"><span data-stu-id="3496a-170">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="3496a-171">**مكتمل** — إرسال إخطارات عند اكتمال مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-171">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="3496a-172">**غير قابل للاسترداد‬** — إرسال إخطارات عند توقف مثيل سير عمل نظرًا لحدوث خطأ غير قابل للاسترداد‬.</span><span class="sxs-lookup"><span data-stu-id="3496a-172">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="3496a-173">**تم الإنهاء‬** — إرسال إخطارات عند إنهاء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-173">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="3496a-174">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="3496a-174">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="3496a-175">في علامة التبويب **نص الإخطار‬**، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="3496a-175">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="3496a-176">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="3496a-176">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="3496a-177">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر النص للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3496a-177">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="3496a-178">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="3496a-178">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="3496a-179">انقر داخل الحقل لتحديد المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="3496a-179">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3496a-180">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="3496a-180">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3496a-181">في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="3496a-181">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3496a-182">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="3496a-182">Click **Insert**.</span></span>
    5. <span data-ttu-id="3496a-183">عنصر نائب شائع **نص الإعلام** يجب تضمينه هو "الملاحظات الأخيرة: %Workflow.Last note%"، وهو يعرض تعليقات من الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="3496a-183">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="3496a-184">لإضافة ترجمات النص، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="3496a-184">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="3496a-185">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="3496a-185">Click **Translations**.</span></span>
    2. <span data-ttu-id="3496a-186">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="3496a-186">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="3496a-187">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="3496a-187">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="3496a-188">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="3496a-188">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3496a-189">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="3496a-189">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="3496a-190">للحصول على إرشادات حول كيفية إدخال عنصر نائب، راجع الخطوة رقم 5.</span><span class="sxs-lookup"><span data-stu-id="3496a-190">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="3496a-191">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="3496a-191">Click **Close**.</span></span>

7. <span data-ttu-id="3496a-192">في علامة تبويب **المستلم**، استخدم الخيارات التالية لتحديد الشخص الذي سيتلقى الإخطارات.</span><span class="sxs-lookup"><span data-stu-id="3496a-192">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3496a-193">خيار</span><span class="sxs-lookup"><span data-stu-id="3496a-193">Option</span></span></th>
    <th><span data-ttu-id="3496a-194">يتم إرسال الإخطارات إلى هؤلاء المستخدمين</span><span class="sxs-lookup"><span data-stu-id="3496a-194">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="3496a-195">لإرسال الإخطارات، اتبع الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="3496a-195">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3496a-196">المشارك</span><span class="sxs-lookup"><span data-stu-id="3496a-196">Participant</span></span></td>
    <td><span data-ttu-id="3496a-197">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="3496a-197">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3496a-198">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>المشترك</strong>.</span><span class="sxs-lookup"><span data-stu-id="3496a-198">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="3496a-199">في علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="3496a-199">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="3496a-200">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="3496a-200">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3496a-201">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="3496a-201">Workflow user</span></span></td>
    <td><span data-ttu-id="3496a-202">المستخدمون المشاركون في سير العمل هذا</span><span class="sxs-lookup"><span data-stu-id="3496a-202">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3496a-203">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>مستخدم سير العمل</strong>.</span><span class="sxs-lookup"><span data-stu-id="3496a-203">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="3496a-204">في علامة تبويب <strong>مستخدم سير العمل</strong>، في قائمة <strong>مستخدم سير العمل</strong>، حدد أحد المشاركين في سير العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="3496a-204">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3496a-205">المستخدم</span><span class="sxs-lookup"><span data-stu-id="3496a-205">User</span></span></td>
    <td><span data-ttu-id="3496a-206">مستخدمون محددون</span><span class="sxs-lookup"><span data-stu-id="3496a-206">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3496a-207">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="3496a-207">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="3496a-208">على علامة تبويب <strong>المستخدم</strong>، تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3496a-208">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3496a-209">حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="3496a-209">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="3496a-210">كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="3496a-210">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="3496a-211">أدخل تعليقات حول التغييرات التي قمت بها في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3496a-211">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="3496a-212">لإدخال تعليقات حول التغييرات التي قمت بها في سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3496a-212">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="3496a-213">في الجزء الأيمن، انقر فوق **الملاحظات**.</span><span class="sxs-lookup"><span data-stu-id="3496a-213">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="3496a-214">في الحقل **إدخال التعليقات الخاصة بسير العمل‬**، أدخل تعليقاتك.</span><span class="sxs-lookup"><span data-stu-id="3496a-214">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="3496a-215">راجع تعليقاتك.</span><span class="sxs-lookup"><span data-stu-id="3496a-215">Review your comments.</span></span> <span data-ttu-id="3496a-216">بعد إضافة التعليقات، لا يمكنك تعديلها.</span><span class="sxs-lookup"><span data-stu-id="3496a-216">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="3496a-217">انقر فوق **إضافة** لإضافة التعليقات إلى ناحية **سجل التعليقات‬**.</span><span class="sxs-lookup"><span data-stu-id="3496a-217">Click **Add** to add your comments to the **Comment history** area.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]