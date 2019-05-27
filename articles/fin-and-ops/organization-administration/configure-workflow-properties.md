---
title: تكوين خصائص سير العمل
description: يوضح هذا الموضوع كيفية تكوين مختلف خصائص لسير العمل.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
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
ms.openlocfilehash: 576ce368b2a8672aa39116eb0cc6e3d3f2a06bb3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571302"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="13362-103">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="13362-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13362-104">يوضح هذا الموضوع كيفية تكوين مختلف خصائص لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="13362-105">لتكوين خصائص سير العمل، افتح سير العمل في محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="13362-106">انقر فوق لوحة محرر سير العمل، ثم انقر **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="13362-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="13362-107">يمكنك استخدام الإجراءات التالية لتكوين مختلف خصائص سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="13362-108">تسمية سير العمل</span><span class="sxs-lookup"><span data-stu-id="13362-108">Name the workflow</span></span>

<span data-ttu-id="13362-109">اتبع الخطوات التالية لإدخال اسم لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="13362-110">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="13362-111">في الحقل **الاسم**، أدخل اسمًا فريدًا لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="13362-112">على سبيل المثال، إذا أنشأت سير عمل طلب شراء لكل بلد/منطقة تعمل فيها، فيمكنك تسمية سير عمل طلب الشراء **طلبات الشراء الخاصة بالدانمارك** أو **طلبات الشراء الخاصة بأسبانيا**.</span><span class="sxs-lookup"><span data-stu-id="13362-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="13362-113">تحديد مالك سير العمل</span><span class="sxs-lookup"><span data-stu-id="13362-113">Specify the workflow owner</span></span>

<span data-ttu-id="13362-114">يعد مالك سير العمل الشخص الذي يدير سير العمل هذا ويحافظ عليه.</span><span class="sxs-lookup"><span data-stu-id="13362-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="13362-115">اتبع الخطوات التالية لتحديد مالك سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="13362-116">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="13362-117">من قائمة **المالك**، حدد اسم الشخص الذي سيدير سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="13362-118">تحديد قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="13362-118">Select an email template</span></span>

<span data-ttu-id="13362-119">اتبع هذه الخطوات لتحديد قالب البريد الإلكتروني الذي يستخدم لإنشاء رسائل الإخطار الخاصة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="13362-120">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="13362-121">في قائمة **قالب البريد الإلكتروني لإخطارات سير العمل**، حدد القالب.</span><span class="sxs-lookup"><span data-stu-id="13362-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="13362-122">إدخال إرشادات للمستخدمين</span><span class="sxs-lookup"><span data-stu-id="13362-122">Enter instructions for users</span></span>

<span data-ttu-id="13362-123">يمكنك توفير إرشادات للمستخدمين الذين يرسلون المستندات للمعالجة والاعتماد.</span><span class="sxs-lookup"><span data-stu-id="13362-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="13362-124">كما يشار إلى هؤلاء المستخدمين باسم *المنشئين*.</span><span class="sxs-lookup"><span data-stu-id="13362-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="13362-125">على سبيل المثال، تقوم بإنشاء سير عمل طلب شراء، وتدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="13362-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="13362-126">سيتمكن عندئذٍ المستخدمون الذي يدخلون طلبات الشراء في صفحة **طلبات الشراء** من رؤية هذه الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="13362-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="13362-127">لعرض الإرشادات، ينقر المنشئ فوق الأيقونة في شريط رسائل سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="13362-128">اتبع الخطوات التالية لإدخال إرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="13362-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="13362-129">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="13362-130">في حقل **إرشادات الإرسال‬**، أدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="13362-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="13362-131">لتخصيص الإرشادات، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="13362-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="13362-132">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما تظهر الإرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="13362-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="13362-133">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="13362-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="13362-134">انقر في حقل **إرشادات الإرسال** لتحديد المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="13362-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="13362-135">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="13362-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="13362-136">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="13362-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="13362-137">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="13362-137">Click **Insert**.</span></span>

4. <span data-ttu-id="13362-138">لإضافة ترجمات الإرشادات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="13362-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="13362-139">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="13362-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="13362-140">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="13362-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="13362-141">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="13362-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="13362-142">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="13362-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="13362-143">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="13362-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="13362-144">للحصول على إرشادات حول كيفية إدخال عنصر نائب، راجع الخطوة رقم 3.</span><span class="sxs-lookup"><span data-stu-id="13362-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="13362-145">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="13362-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="13362-146">تحديد وقت وجوب استخدام سير العمل هذا</span><span class="sxs-lookup"><span data-stu-id="13362-146">Specify when this workflow is used</span></span>

<span data-ttu-id="13362-147">يمكنك إنشاء مهام سير عمل متعددة تستند إلى النوع نفسه.</span><span class="sxs-lookup"><span data-stu-id="13362-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="13362-148">على سبيل المثال، يمكنك إنشاء سير عمل طلب شراء لكل بلد/منطقة تعمل فيها، مثل طلبات الشراء الخاصة بالدانمارك وطلبات الشراء الخاصة بأسبانيا.</span><span class="sxs-lookup"><span data-stu-id="13362-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="13362-149">في حالة توفّر عمليات سير عمل متعددة تستند إلى النوع نفسه، يجب تحديد وقت استخدام كل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="13362-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="13362-150">بالنسبة إلى المثال السابق، يمكنك تحديد الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="13362-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="13362-151">يتم استخدام طلبات الشراء الخاصة بالدانمارك في الحالة التالية: البلد/المنطقة = DK.</span><span class="sxs-lookup"><span data-stu-id="13362-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="13362-152">يتم استخدام طلبات الشراء الخاصة بأسبانيا في الحالة التالية: البلد/المنطقة = ES.</span><span class="sxs-lookup"><span data-stu-id="13362-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="13362-153">اتبع الخطوات التالية لتحديد متى ينبغي استخدام سير العمل الذي تقوم بتكوينه.</span><span class="sxs-lookup"><span data-stu-id="13362-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="13362-154">في الجزء الأيمن، انقر فوق **التنشيط**.</span><span class="sxs-lookup"><span data-stu-id="13362-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="13362-155">حدد خانة الاختيار **تعيين شروط تشغيل سير العمل هذا‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="13362-156">انقر فوق **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="13362-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="13362-157">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="13362-157">Enter a condition.</span></span>
5. <span data-ttu-id="13362-158">أدخل أية شروط إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="13362-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="13362-159">للتأكد من تعيين الشروط التي قمت بإدخالها بشكل صحيح، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="13362-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="13362-160">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="13362-160">Click **Test**.</span></span>
    2. <span data-ttu-id="13362-161">في صفحة **اختبار حالة سير العمل**، في الناحية **التحقق من صحة الشرط‬**، حدد سجلاً.</span><span class="sxs-lookup"><span data-stu-id="13362-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="13362-162">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="13362-162">Click **Test**.</span></span> <span data-ttu-id="13362-163">سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.</span><span class="sxs-lookup"><span data-stu-id="13362-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="13362-164">على سبيل المثال، إذا كنت تقوم بإنشاء سير عمل طلب شراء لأسبانيا، فستعرض الناحية **التحقق من صحة الشرط‬** في الصفحة قائمة بطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="13362-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="13362-165">وعند النقر فوق **اختبار**، سيقوم النظام بتقييم طلب الشراء المحدد لتحديد ما إذا كان البلد/المنطقة هو ES أم لا.</span><span class="sxs-lookup"><span data-stu-id="13362-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="13362-166">انقر فوق **موافق** أو **إلغاء الأمر** للرجوع إلى الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="13362-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="13362-167">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="13362-167">Specify when notifications are sent</span></span>

<span data-ttu-id="13362-168">عندما إرسال مستند للمعالجة، يتم إنشاء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="13362-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="13362-169">ويمكنك إرسال إخطارات إلى المستخدمين عند بدء مثيلات سير العمل التي تستند إلى سير العمل أو عند إكمالها أو إلغائها أو إيقافها نظرًا لحدوث خطأ.</span><span class="sxs-lookup"><span data-stu-id="13362-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="13362-170">اتبع الخطوات التالية لتحديد أوقات إرسال الإخطارات.</span><span class="sxs-lookup"><span data-stu-id="13362-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="13362-171">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="13362-172">حدد خانة الاختيار لكل حدث من المفترض أن يؤدي إلى تشغيل الإخطارات‬:</span><span class="sxs-lookup"><span data-stu-id="13362-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="13362-173">**تم البدء** — إرسال إخطارات عند بدء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="13362-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="13362-174">**متوقف** — إرسال إخطارات عند توقف مثيل سير عمل نظرًا لحدوث خطأ.</span><span class="sxs-lookup"><span data-stu-id="13362-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="13362-175">**مكتمل** — إرسال إخطارات عند اكتمال مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="13362-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="13362-176">**غير قابل للاسترداد‬** — إرسال إخطارات عند توقف مثيل سير عمل نظرًا لحدوث خطأ غير قابل للاسترداد‬.</span><span class="sxs-lookup"><span data-stu-id="13362-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="13362-177">**تم الإنهاء‬** — إرسال إخطارات عند إنهاء مثيل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="13362-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="13362-178">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="13362-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="13362-179">في علامة التبويب **نص الإخطار‬**، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="13362-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="13362-180">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="13362-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="13362-181">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر النص للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="13362-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="13362-182">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="13362-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="13362-183">انقر داخل الحقل لتحديد المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="13362-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="13362-184">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="13362-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="13362-185">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="13362-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="13362-186">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="13362-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="13362-187">عنصر نائب شائع **نص الإعلام** يجب تضمينه هو "الملاحظات الأخيرة: %Workflow.Last note%"، وهو يعرض تعليقات من الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="13362-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="13362-188">لإضافة ترجمات النص، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="13362-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="13362-189">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="13362-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="13362-190">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="13362-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="13362-191">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="13362-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="13362-192">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="13362-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="13362-193">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="13362-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="13362-194">للحصول على إرشادات حول كيفية إدخال عنصر نائب، راجع الخطوة رقم 5.</span><span class="sxs-lookup"><span data-stu-id="13362-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="13362-195">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="13362-195">Click **Close**.</span></span>

7. <span data-ttu-id="13362-196">في علامة تبويب **المستلم**، استخدم الخيارات التالية لتحديد الشخص الذي سيتلقى الإخطارات.</span><span class="sxs-lookup"><span data-stu-id="13362-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="13362-197">خيار</span><span class="sxs-lookup"><span data-stu-id="13362-197">Option</span></span></th>
    <th><span data-ttu-id="13362-198">يتم إرسال الإخطارات إلى هؤلاء المستخدمين</span><span class="sxs-lookup"><span data-stu-id="13362-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="13362-199">لإرسال الإخطارات، اتبع الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="13362-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="13362-200">المشارك</span><span class="sxs-lookup"><span data-stu-id="13362-200">Participant</span></span></td>
    <td><span data-ttu-id="13362-201">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="13362-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="13362-202">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>المشترك</strong>.</span><span class="sxs-lookup"><span data-stu-id="13362-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="13362-203">في علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="13362-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="13362-204">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="13362-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="13362-205">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="13362-205">Workflow user</span></span></td>
    <td><span data-ttu-id="13362-206">المستخدمون المشاركون في سير العمل هذا</span><span class="sxs-lookup"><span data-stu-id="13362-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="13362-207">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>مستخدم سير العمل</strong>.</span><span class="sxs-lookup"><span data-stu-id="13362-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="13362-208">في علامة تبويب <strong>مستخدم سير العمل</strong>، في قائمة <strong>مستخدم سير العمل</strong>، حدد أحد المشاركين في سير العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="13362-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="13362-209">المستخدم</span><span class="sxs-lookup"><span data-stu-id="13362-209">User</span></span></td>
    <td><span data-ttu-id="13362-210">مستخدمو Finance and Operations معينون</span><span class="sxs-lookup"><span data-stu-id="13362-210">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="13362-211">في علامة تبويب <strong>المستلم</strong>، انقر فوق <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="13362-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="13362-212">في علامة تبويب <strong>المستخدم</strong>، تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع مستخدمي Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13362-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="13362-213">حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="13362-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="13362-214">كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="13362-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="13362-215">أدخل تعليقات حول التغييرات التي قمت بها في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13362-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="13362-216">لإدخال تعليقات حول التغييرات التي قمت بها في سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="13362-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="13362-217">في الجزء الأيمن، انقر فوق **الملاحظات**.</span><span class="sxs-lookup"><span data-stu-id="13362-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="13362-218">في الحقل **إدخال التعليقات الخاصة بسير العمل‬**، أدخل تعليقاتك.</span><span class="sxs-lookup"><span data-stu-id="13362-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="13362-219">راجع تعليقاتك.</span><span class="sxs-lookup"><span data-stu-id="13362-219">Review your comments.</span></span> <span data-ttu-id="13362-220">بعد إضافة التعليقات، لا يمكنك تعديلها.</span><span class="sxs-lookup"><span data-stu-id="13362-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="13362-221">انقر فوق **إضافة** لإضافة التعليقات إلى ناحية **سجل التعليقات‬**.</span><span class="sxs-lookup"><span data-stu-id="13362-221">Click **Add** to add your comments to the **Comment history** area.</span></span>
