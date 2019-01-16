---
title: "مسجل المهام وتعليمات Retail Modern POS (MPOS) وCloud POS"
description: "يصف هذا الموضوع كيفية استخدام مسجل المهام في نقطة بيع التجزئة الحديثة ونقطة بيع المجموعة."
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: a74a1275f08e3dba60a1002a102e143eb37fcd9a
ms.contentlocale: ar-sa
ms.lasthandoff: 01/04/2019

---

# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="7ac62-103">مسجل المهام وتعليمات Retail Modern POS (MPOS) وCloud POS</span><span class="sxs-lookup"><span data-stu-id="7ac62-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7ac62-104">يصف هذا الموضوع كيفية استخدام مسجل المهام في نقطة بيع التجزئة الحديثة ونقطة بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="7ac62-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="7ac62-105">Overview</span></span>

<span data-ttu-id="7ac62-106">يُعتبر مسجل المهام في Retail Modern POS أو Cloud POS حلاً جديدًا تم بناؤه مع التركيز على الاستجابة العالية.</span><span class="sxs-lookup"><span data-stu-id="7ac62-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="7ac62-107">إنه يوفر واجهة برمجة تطبيقات مرنة (API) مرنة لقابلية التوسعة والتكامل السلس مع عملاء لديهم تسجيلات لعمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="7ac62-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="7ac62-108">بالإضافة إلى ذلك، تم تقديم تكامل مسجل المهام مع أداة تكوين عمليات الأعمال (BPM) على Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)).</span><span class="sxs-lookup"><span data-stu-id="7ac62-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="7ac62-109">لذلك، سيتمكن المستخدمون من متابعة إنتاج رسومات تخطيطية لعمليات الأعمال من التسجيلات إلى تحليل تطبيقاتهم وتصميمها.</span><span class="sxs-lookup"><span data-stu-id="7ac62-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="7ac62-110">الهندسة</span><span class="sxs-lookup"><span data-stu-id="7ac62-110">Architecture</span></span>

<span data-ttu-id="7ac62-111">باستطاعة مسجل المهام تسجيل إجراءات المستخدم في العميل بنفس الدقة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="7ac62-112">تم تجهيز كل عنصر تحكم لإعلام مسجل المهام عن تنفيذ إجراء من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7ac62-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="7ac62-113">يقوم عنصر التحكم بإعلام مسجل المهام بوقوع حدث ما، ويقوم بتمرير كافة المعلومات ذات الصلة حول إجراء المستخدم المناظر في الوقت الحقيقي.</span><span class="sxs-lookup"><span data-stu-id="7ac62-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="7ac62-114">من خلال هذه المعلومات، يستطيع مسجل المهام التقاط نوع إجراء المستخدم (مثل النقر فوق الزر أو إدخال قيمة، أو التنقل) وأي بيانات مرتبطة بإجراء المستخدم (مثل قيمة بيانات الإدخال أو سياق النموذج أو سياق السجل).</span><span class="sxs-lookup"><span data-stu-id="7ac62-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="7ac62-115">يلتزم مسجل المهام بالمعلومات مع تفاصيل كافية للمساعدة في ضمان قيام تشغيل التسجيل بتنفيذ الإجراءات المسجلة تمامًا كما نفذها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7ac62-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="7ac62-116">(لم يتم بعد تطبيق ميزة التشغيل في نقطة بيع التجزئة الحديثة أو نقطة بيع المجموعة.)</span><span class="sxs-lookup"><span data-stu-id="7ac62-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="7ac62-117">التكوين الأساسي</span><span class="sxs-lookup"><span data-stu-id="7ac62-117">Basic configuration</span></span>

<span data-ttu-id="7ac62-118">لتمكين تسجيل المهام في نقطة البيع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7ac62-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="7ac62-119">انقر فوق **البيع بالتجزئة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **السجلات‬**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-119">Click **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="7ac62-120">انقر فوق السجل لتمكين تسجيل المهام.</span><span class="sxs-lookup"><span data-stu-id="7ac62-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="7ac62-121">على علامة التبويب **سجل**، على علامة التبويب السريعة **عام**، عيّن الخيار **تمكين تسجيل المهام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="7ac62-122">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-122">Click **Save**.</span></span>
5. <span data-ttu-id="7ac62-123">انتقل إلى **البيع بالتجزئة** &gt; **تكنولوجيا معلومات البيع بالتجزئة** &gt; **جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-123">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="7ac62-124">حدد الوظيفة **سجلات (1090)**، ثم انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="7ac62-125">إنشاء تسجيل</span><span class="sxs-lookup"><span data-stu-id="7ac62-125">Create a recording</span></span>

<span data-ttu-id="7ac62-126">اتبع هذه الخطوات لإنشاء تسجيل جديد باستخدام مسجل المهام.</span><span class="sxs-lookup"><span data-stu-id="7ac62-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="7ac62-127">ابدأ تشغيل نقطة بيع التجزئة الحديثة أو نقطة بيع المجموعة، وسجل دخولك.</span><span class="sxs-lookup"><span data-stu-id="7ac62-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="7ac62-128">في صفحة **الإعدادات**، في المقطع **مسجل المهام** ، انقر فوق **فتح مسجل المهام**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="7ac62-129">يظهر جزء **مسجل المهام**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="7ac62-130">يمكنك النقر فوق الزر **إغلاق** (**X**) في الزاوية العلوية اليسرى لإغلاق جزء **مسجل المهام** قبل بدء تسجيل جديد.</span><span class="sxs-lookup"><span data-stu-id="7ac62-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="7ac62-131">لإعادة فتح الجزء، كرر الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="7ac62-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="7ac62-132">[![جزء مسجل المهام](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="7ac62-133">أدخل اسمًا ووصفًا للتسجيل، ثم انقر فوق **البدء‬**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="7ac62-134">تبدأ جلسة التسجيل بمجرد النقر فوق **البدء‬**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ac62-135">إذا نقرت فوق الزر **إغلاق‏‎** (**X**) في الزاوية العلوية اليسرى بينما يكون التسجيل قيد التقدم، فسيتم إغلاق الجزء **مسجل المهام** ولكن من دون إنهاء جلسة التسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="7ac62-136">لإعادة فتح جزء مسجل المهام، انقر فوق الزر **تعليمات** (علامة استفهام) في الجزء العلوي من الشاشة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="7ac62-137">[![علامة استفهام](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="7ac62-138">بعد النقر فوق **البدء**، يدخل مسجل المهام في وضع التسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="7ac62-139">يعرض جزء **مسجل المهام** المعلومات وعناصر التحكم المرتبطة بعملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="7ac62-140">نفّذ الإجراءات التي تريد تنفيذها في واجهة المستخدم في نقطة بيع التجزئة الحديثة أو نقطة بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="7ac62-141">لإنهاء جلسة التسجيل، انقر فوق **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="7ac62-142">خيارات التنزيل</span><span class="sxs-lookup"><span data-stu-id="7ac62-142">Download options</span></span>

<span data-ttu-id="7ac62-143">بعد أن تقوم بإنهاء جلسة التسجيل، يظهر الكثير من الخيارات، بحيث يمكنك تنزيل التسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="7ac62-144">[![خيارات التنزيل](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="7ac62-145">حفظ إلى هذا الكمبيوتر الشخصي</span><span class="sxs-lookup"><span data-stu-id="7ac62-145">Save to this PC</span></span>

<span data-ttu-id="7ac62-146">يمكنك استخدام حزمة التسجيل لتشغيل دليل مهام أو المحافظة على التسجيل أو تحرير التعليقات التوضيحية في التسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="7ac62-147">(لم يتم بعد تطبيق هذه الميزة في نقطة بيع التجزئة الحديثة أو نقطة بيع المجموعة.)</span><span class="sxs-lookup"><span data-stu-id="7ac62-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="7ac62-148">تصدير كمستند Word</span><span class="sxs-lookup"><span data-stu-id="7ac62-148">Export as Word document</span></span>

<span data-ttu-id="7ac62-149">يمكنك حفظ التسجيل كمستند Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="7ac62-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="7ac62-150">سوف يحتوي المستند على الخطوات المسجلة ولقطات الشاشة التي تم التقاطها.</span><span class="sxs-lookup"><span data-stu-id="7ac62-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="7ac62-151">حفظ كتسجيل مطور</span><span class="sxs-lookup"><span data-stu-id="7ac62-151">Save as developer recording</span></span>

<span data-ttu-id="7ac62-152">سيكون ملف التسجيل الأولي مفيدًا لسيناريوهات المطور مثل إنشاء كود الاختبار.</span><span class="sxs-lookup"><span data-stu-id="7ac62-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="7ac62-153">(لم يتم بعد تطبيق هذه الميزة.)</span><span class="sxs-lookup"><span data-stu-id="7ac62-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="7ac62-154">عناصر التحكم الخاصة بالتسجيل</span><span class="sxs-lookup"><span data-stu-id="7ac62-154">Recording controls</span></span>

<span data-ttu-id="7ac62-155">[![عناصر التحكم الخاصة بالتسجيل](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="7ac62-156">إيقاف</span><span class="sxs-lookup"><span data-stu-id="7ac62-156">Stop</span></span>

<span data-ttu-id="7ac62-157">انقر فوق **إيقاف** لإنهاء جلسة التسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="7ac62-158">لاحظ أنه لا يمكنك إعادة تشغيل جلسة عمل بعد إنهائها.</span><span class="sxs-lookup"><span data-stu-id="7ac62-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="7ac62-159">لذلك، تأكد من إكمال التسجيل قبل إنهائه.</span><span class="sxs-lookup"><span data-stu-id="7ac62-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="7ac62-160">توقف مؤقت</span><span class="sxs-lookup"><span data-stu-id="7ac62-160">Pause</span></span>

<span data-ttu-id="7ac62-161">انقر فوق **إيقاف مؤقت** لإيقاف جلسة التسجيل مؤقتًا ومتابعة العملية.</span><span class="sxs-lookup"><span data-stu-id="7ac62-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="7ac62-162">لا يتم تسجيل الخطوات التي تقوم بتنفيذها بعد النقر فوق **إيقاف مؤقت**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="7ac62-163">متابعة</span><span class="sxs-lookup"><span data-stu-id="7ac62-163">Continue</span></span>

<span data-ttu-id="7ac62-164">لاستئناف جلسة التسجيل بعد إيقافها مؤقتًا، انقر فوق **متابعة**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="7ac62-165">التقاط لقطات الشاشة</span><span class="sxs-lookup"><span data-stu-id="7ac62-165">Capture screenshots</span></span>

<span data-ttu-id="7ac62-166">باستطاعة مسجل المهام التقاط لقطات الشاشة‬ لواجهة مستخدم نقطة البيع الحديثة للبيع بالتجزئة بينما تقوم بتسجيل عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="7ac62-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="7ac62-167">لتشغيل ميزة التقاط لقطات الشاشة‬، عيّن الخيار **التقاط لقطات الشاشة‬** إلى **نعم**، ثم قم بالتسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="7ac62-168">بمجرد اكتمال التسجيل، انقر فوق **إيقاف** وقم بتنزيل مستند Word.</span><span class="sxs-lookup"><span data-stu-id="7ac62-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="7ac62-169">سوف يحتوي المستند على الخطوات بلقطات الشاشة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="7ac62-170">وظيفة التقاط لقطات الشاشة‬ غير مدعومة في نقطة بيع المجموعة‬.</span><span class="sxs-lookup"><span data-stu-id="7ac62-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="7ac62-171">بدء المهمة وإنهاء المهمة</span><span class="sxs-lookup"><span data-stu-id="7ac62-171">Start task and End task</span></span>

<span data-ttu-id="7ac62-172">يمكنك تحديد بداية ونهاية مجموعة من الخطوات المجمعة باستخدام الزرين **بدء المهمة‬** و**إنهاء** **المهمة**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="7ac62-173">انقر فوق **بدء المهمة** لإضافة خطوة "بدء المهمة"، ثم قم بتنفيذ الخطوات التي يجب تضمينها في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="7ac62-174">بعد الانتهاء من تنفيذ الخطوات للمجموعة، انقر فوق **إنهاء المهمة**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="7ac62-175">تساعدك المهام في تنظيم إجراءاتك.</span><span class="sxs-lookup"><span data-stu-id="7ac62-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="7ac62-176">ويمكن تضمين المهام ضمن مهام أخرى.</span><span class="sxs-lookup"><span data-stu-id="7ac62-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="7ac62-177">بهذه الطريقة، يمكن تنظيم عمليات الأعمال الطويلة جدًا والبالغة التعقيد بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="7ac62-178">إضافة تعليقات توضيحية</span><span class="sxs-lookup"><span data-stu-id="7ac62-178">Adding annotations</span></span>

<span data-ttu-id="7ac62-179">التعليق التوضيحي هو النص الإضافي الذي تضيفه إلى إحدى الخطوات في تسجيل.</span><span class="sxs-lookup"><span data-stu-id="7ac62-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="7ac62-180">على سبيل المثال، يمكنك استخدام التعليقات التوضيحية لتقديم سياق إضافي أو إرشادات إضافية للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="7ac62-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="7ac62-181">يمكنك إضافة التعليقات التوضيحية قبل خطوة أو بعدها.</span><span class="sxs-lookup"><span data-stu-id="7ac62-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="7ac62-182">يمكنك إضافة تعليق توضيحي لأي خطوة عن طريق النقر فوق الزر **تحرير** (رمز القلم) إلى يسار الخطوة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="7ac62-183">[![الزر "تحرير" لخطوة](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="7ac62-184">النصوص والملاحظات</span><span class="sxs-lookup"><span data-stu-id="7ac62-184">Texts and notes</span></span>

<span data-ttu-id="7ac62-185">يمكنك استخدام الحقلين **نصوص** و**ملاحظات** لإضافة النص الذي يجب إقرانه بإحدى الخطوات في دليل مهام.</span><span class="sxs-lookup"><span data-stu-id="7ac62-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="7ac62-186">[![حقول النصوص والملاحظات](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="7ac62-187">النص</span><span class="sxs-lookup"><span data-stu-id="7ac62-187">Text</span></span>

<span data-ttu-id="7ac62-188">يظهر النص الذي تدخله في حقل **النص** *فوق* نص الخطوة في دليل المهام.</span><span class="sxs-lookup"><span data-stu-id="7ac62-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="7ac62-189">يُعتبر هذا الموقع مناسبًا للنص الذي تريد أن يقرأه المستخدم قبل أن يكمل الخطوة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="7ac62-190">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="7ac62-190">Notes</span></span>

<span data-ttu-id="7ac62-191">يظهر النص الذي تدخله في حقل **الملاحظات** *تحت* نص الخطوة في دليل المهام.</span><span class="sxs-lookup"><span data-stu-id="7ac62-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="7ac62-192">لقراءة نص الملاحظة، يجب على المستخدم توسيع نص الخطوة في النافذة المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="7ac62-193">يُعتبر هذا الموقع مناسبًا لمواد القراءة الاختيارية أو المعلومات الأخرى التي قد تكون مفيدة للمستخدم، ولكن المستخدم لا يحتاجها لإكمال الإجراء.</span><span class="sxs-lookup"><span data-stu-id="7ac62-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="7ac62-194">نظام التعليمات في نقطة البيع الحديثة للبيع بالتجزئة ونقطة بيع المجموعة</span><span class="sxs-lookup"><span data-stu-id="7ac62-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="7ac62-195">لإظهار تسجيلات المهام المخصصة الخاصة بك في جزء المساعدة في نقطة البيع الحديثة للبيع بالتجزئة ونقطة بيع المجموعة بحيث يمكن عرضها كنص، يجب عليك حفظ تسجيلات المهام إلى مكتبة BPM، ثم تحديث محددات نظام التعليمات‬ بحيث تشير إلى مكتبة BPM.</span><span class="sxs-lookup"><span data-stu-id="7ac62-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="7ac62-196">لمزيد من المعلومات، راجع [الاتصال بنظام التعليمات](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="7ac62-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="7ac62-197">يبحث نظام تعليمات نقطة البيع الحديثة للبيع بالتجزئة ونقطة بيع المجموعة‬ في LCS في‬ الوقت الحقيقي.</span><span class="sxs-lookup"><span data-stu-id="7ac62-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="7ac62-198">وهو يبحث عبر كافة مكتبات BPM التي تم تحديدها في محددات نظام تعليمات Microsoft Dynamics 365 for Retail ويعرض النتائج ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="7ac62-198">It searches across all the BPM libraries that are selected in the Microsoft Dynamics 365 for Retail Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="7ac62-199">للوصول إلى القائمة **تعليمات**، انقر فوق الزر **تعليمات** (علامة الاستفهام) في الجزء العلوي من الشاشة، ثم اكتب اسم عمليتك في مربع البحث واضغط الزر بحث.</span><span class="sxs-lookup"><span data-stu-id="7ac62-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="7ac62-200">[![الزر تعليمات](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ac62-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="7ac62-201">عندما تنقر فوق دليل مهام في نتائج البحث، يمكنك عرض الخطوات كموضوع تعليمات أو تصدير الخطوات إلى مستند Word.</span><span class="sxs-lookup"><span data-stu-id="7ac62-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="7ac62-202">لن يعرض نظام التعليمات في نقطة البيع الحديثة للبيع بالتجزئة ونقطة بيع المجموعة‬ دلائل المهام وفقًا للنموذج الذي تعمل عليه أو العملية التي تعمل على تنفيذها.</span><span class="sxs-lookup"><span data-stu-id="7ac62-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="7ac62-203">يجب عليك كتابة اسم العملية في مربع البحث والنقر فوق **بحث**.</span><span class="sxs-lookup"><span data-stu-id="7ac62-203">You have to type the process name in the search box and then click **Search**.</span></span>

