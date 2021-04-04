---
title: تكوين تجربة التعليمات لتطبيقات Finance and Operations
description: يوفر هذا الموضوع معلومات حول مكونات نظام التعليمات لبعض تطبيقات Microsoft Dynamics 365. كما يوضح كيفية توصيل هذه التطبيقات وتوفير ملخص لعملية إنشاء تعليمات مخصصة.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 467cce5a80dc7577647e82c8652c8a7adc67a498
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565918"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="bf231-104">تكوين تجربة التعليمات لتطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bf231-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf231-105">في هذا الموضوع، ستجد نظرة عامة على مكونات نظام التعليمات لتطبيقات Finance and Operations، مثل Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Commerce وDynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bf231-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bf231-106">يوضح الموضوع أيضًا كيفية توصيل هذه التطبيقات ويوفر ملخصًا لعملية إنشاء تعليمات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="bf231-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="bf231-107">بنية التعليمات</span><span class="sxs-lookup"><span data-stu-id="bf231-107">Help architecture</span></span>

<span data-ttu-id="bf231-108">تشمل تطبيقات Finance and Operations نظرات تصورية ومواضيع أخرى يتم نشرها على موقع [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="bf231-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="bf231-109">يمكن بعد ذلك الوصول إلى هذا المحتوى من خلال جزء **التعليمات** داخل المنتج.</span><span class="sxs-lookup"><span data-stu-id="bf231-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="bf231-110">يبين الرسم التوضيحي التالي أجزاء نظام التعليمات.</span><span class="sxs-lookup"><span data-stu-id="bf231-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="bf231-111">[![بنية التعليمات](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="bf231-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="bf231-112">يقوم نظام التعليمات داخل المنتج بسحب المقالات من docs.microsoft.com ومواقع ويب الأخرى المتصلة.</span><span class="sxs-lookup"><span data-stu-id="bf231-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="bf231-113">كما يسحب أيضًا أدلة المهام التي يتم تخزينها في ‏‫أداة تكوين عمليات الأعمال (BPM)‬ في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bf231-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="bf231-114">إضافة دلائل المهام</span><span class="sxs-lookup"><span data-stu-id="bf231-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="bf231-115">في الوقت الحالي لا تتوفر علامة التبويب **دلائل المهام** في Human Resources أو Commerce.</span><span class="sxs-lookup"><span data-stu-id="bf231-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="bf231-116">مع ذلك، تظل دلائل المهام في تجربة "بدء الاستخدام" في Human Resources متاحة لتغطية الوظائف الأساسية.</span><span class="sxs-lookup"><span data-stu-id="bf231-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="bf231-117">فيما يتعلق بكل من Human Resources وCommerce، تتوفر تعليمات إجرائية على موقع [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="bf231-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="bf231-118">في صفحة **معلمات النظام**، يمكن لمسؤولي النظام تكوين الوصول إلى مكتبات دلائل المهام ذات الصلة لأي عملية تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="bf231-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="bf231-119">لتكوين التعليمات، يجب أن تسجل الدخول باستخدام حساب في المستأجر نفسه الذي تم فيه نشر التطبيق.</span><span class="sxs-lookup"><span data-stu-id="bf231-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="bf231-120">لا يمكن الاتصال بمكتبة LCS من مثيل تطبيق قيد التشغيل على محرك أقراص ثابت محلي ظاهري (VHD).</span><span class="sxs-lookup"><span data-stu-id="bf231-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="bf231-121">[![نموذج محددات النظام مع إعدادات نظام التعليمات](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="bf231-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="bf231-122">لتكوين دلائل مهام لأحد الحلول، اتبع الخطوات التالية في صفحة **معلمات النظام**.</span><span class="sxs-lookup"><span data-stu-id="bf231-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf231-123">في المرة الأولى التي تفتح فيها علامة التبويب **تعليمات** يجب الاتصال بميزة Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="bf231-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="bf231-124">احرص على تحديد الارتباط الموجود في وسط النموذج، وانتظر الاتصال، ثم قم بإغلاق مربع الحوار، ثم حدد **موافق** للوصول إلى صفحة **معلمات النظام**.</span><span class="sxs-lookup"><span data-stu-id="bf231-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="bf231-125">[![الاتصال بـ LCS](./media/connect-to-lcs-crop-1024x365.png "الاتصال بـ LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="bf231-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="bf231-126">تحديد مشروع Lifecycle Services المراد الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="bf231-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="bf231-127">تحديد مكتبات BPM (في المشروع المحدد) لاسترداد تسجيلات المهام منها.</span><span class="sxs-lookup"><span data-stu-id="bf231-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="bf231-128">تعيين أمر العرض لمكتبات BPM.</span><span class="sxs-lookup"><span data-stu-id="bf231-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="bf231-129">ويحدد ترتيب العرض الترتيب الذي ستظهر به تسجيلات المهام من المكتبات في جزء **المساعدة**.</span><span class="sxs-lookup"><span data-stu-id="bf231-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="bf231-130">بعد أن تكمل هذه الخطوات، يمكنك فتح جزء **التعليمات** وتحديد علامة تبويب **دلائل المهام**. سترى الآن دلائل المهام التي تنطبق على الصفحة التي تعمل عليها حاليًا في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bf231-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="bf231-131">إذا لم تعثر على دلائك المهام، فيمكنك إدخال كلمات أساسية لتنقية البحث.</span><span class="sxs-lookup"><span data-stu-id="bf231-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="bf231-132">إظهار دلائل المهام المترجمة</span><span class="sxs-lookup"><span data-stu-id="bf231-132">Showing translated task guides</span></span>

<span data-ttu-id="bf231-133">تم إصدار دلائل المهام المترجمة لأول مرة في شهر مايو 2016 لمكتبة بدء الاستخدام والمكتبة الموحدة APQC.</span><span class="sxs-lookup"><span data-stu-id="bf231-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="bf231-134">لرؤية تعليمات دلائل المهام المترجمة، تأكد من اتصال حل Dynamics 365 بمكتبة مايو 2016.</span><span class="sxs-lookup"><span data-stu-id="bf231-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="bf231-135">يمكن للمستخدمين تغيير اللغة التي يظهر بها دليل المهام بواسطة تغيير إعدادات اللغة ضمن **الخيارات** &gt; **التفضيلات**.</span><span class="sxs-lookup"><span data-stu-id="bf231-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="bf231-136">على الرغم من ترجمة العديد من دلائل المهام، إلا أن العميل لا يعرض الآن أسماء دلائل المهام المترجمة.</span><span class="sxs-lookup"><span data-stu-id="bf231-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="bf231-137">علاوةً على ذلك، في مكتبة شهر مايو، تتوفر الترجمات فقط لدلائل المهام المترجمة التي تم إصدارها في شهر فبراير 2016.</span><span class="sxs-lookup"><span data-stu-id="bf231-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="bf231-138">سوف تصدر Microsoft مكتبة محدثة تشمل الترجمات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="bf231-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="bf231-139">إذا كان دليل المهمة مترجمًا، فسيظهر نصه بلغتك المحددة عندما تفتحه.</span><span class="sxs-lookup"><span data-stu-id="bf231-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="bf231-140">إذا لم يكن دليل المهمة مترجمًا بعد، فسيظهر بعض النص فقط (نصر عناصر التحكم) بلغتك المحددة عندما تفتحه.</span><span class="sxs-lookup"><span data-stu-id="bf231-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="bf231-141">إضافة تعليمات مخصصة</span><span class="sxs-lookup"><span data-stu-id="bf231-141">Adding custom Help</span></span>

<span data-ttu-id="bf231-142">يمكنك استخدام أدلة المهام لإنشاء تعليمات مخصصة أو يمكنك ربط موقع الويب لتعليمات مخصصة بجزء **التعليمات**.</span><span class="sxs-lookup"><span data-stu-id="bf231-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="bf231-143">إنشاء تعليمات مخصصة باستخدام دلائل المهام</span><span class="sxs-lookup"><span data-stu-id="bf231-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="bf231-144">يمكنك إنشاء تعليمات مخصصة للتطبيقات المدعومة عن طريق إنشاء تسجيلات المهام التي تعكس التنفيذ ثم حفظها إلى مكتبة عملية أعمال في LCS.</span><span class="sxs-lookup"><span data-stu-id="bf231-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="bf231-145">لا يمكنك إنشاء دلائل مهام مخصصة لـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bf231-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="bf231-146">إذا كنت شريكًا، وقمت بترقية مكتبة إلى مكتبة شركة وقمت بتضمينها في أحد حلول، فستتوفر للعملاء الخاصين بك.</span><span class="sxs-lookup"><span data-stu-id="bf231-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="bf231-147">يمكنك أيضًا إنشاء نسخة من المكتبة العمومية الموحدة APQC، ثم فتح تسجيلات المهام في النسخة وتحريرها وحفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="bf231-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="bf231-148">لمزيد من المعلومات، راجع [موارد مسجل المهام](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="bf231-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="bf231-149">الاتصال بموقع تعليمات مخصص</span><span class="sxs-lookup"><span data-stu-id="bf231-149">Connect a custom Help site</span></span>

<span data-ttu-id="bf231-150">نادرًا ما يتم استخدام تطبيقات Finance and Operations في نموذج جاهز لها.</span><span class="sxs-lookup"><span data-stu-id="bf231-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="bf231-151">بدلا من ذلك، يتم تخصيص الحل وتوسيعه لملائمة احتياجات المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="bf231-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="bf231-152">يمكنك أيضا تخصيص تجربة التعليمات وتوسيعها.</span><span class="sxs-lookup"><span data-stu-id="bf231-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="bf231-153">على سبيل المثال، يمكنك إضافة تعليمات مخصصة إلى جزء **تعليمات** داخل المنتج.</span><span class="sxs-lookup"><span data-stu-id="bf231-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="bf231-154">قامت Microsoft بتوفير مجموعة أدوات تساعدك في نشر التعليمات المخصصة وتوصيلها بجزء **التعليمات**.</span><span class="sxs-lookup"><span data-stu-id="bf231-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="bf231-155">للحصول على معلومات حول كيفية إعداد حل تعليمات مخصص متصل جزء **التعليمات**، راجع [نظرة عامة حول التعليمات المخصصة](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bf231-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="bf231-156">إذا كنت ترغب في التعاون مع Microsoft بشأن الأدوات والعمليات الخاصة بتخصيص التعليمات، فقم بملء النموذج في [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback)</span><span class="sxs-lookup"><span data-stu-id="bf231-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="bf231-157">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="bf231-157">See also</span></span>

[<span data-ttu-id="bf231-158">نظام التعليمات</span><span class="sxs-lookup"><span data-stu-id="bf231-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="bf231-159">نظرة عامة حول التعليمات المخصصة</span><span class="sxs-lookup"><span data-stu-id="bf231-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="bf231-160">موارد مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="bf231-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="bf231-161">إنشاء الوثائق أو التدريب بمسجل المهام</span><span class="sxs-lookup"><span data-stu-id="bf231-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="bf231-162">مستودع GitHub للتعليمات المخصصة</span><span class="sxs-lookup"><span data-stu-id="bf231-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]