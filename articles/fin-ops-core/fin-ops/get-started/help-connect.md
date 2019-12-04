---
title: الاتصال بنظام التعليمات
description: يُوضح هذا الموضوع مكونات نظام التعليمات لتطبيقات Finance and Operations، ويقدم نظرة عامة حول كيفية توصيلها بالإضافة إلى ملخص حول كيفية إنشاء تعليمات مخصصة.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812570"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="4b5fd-103">الاتصال بنظام التعليمات</span><span class="sxs-lookup"><span data-stu-id="4b5fd-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b5fd-104">يُوضح هذا الموضوع مكونات نظام التعليمات لتطبيقات Finance and Operations، مثل Dynamics 365 Finance، وSupply Chain Management، وRetail، وTalent.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="4b5fd-105">ويقدم نظرة عامة حول كيفية توصيل هذه المكونات وملخصًا لكيفية إنشاء تعليمات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="4b5fd-106">بنية التعليمات</span><span class="sxs-lookup"><span data-stu-id="4b5fd-106">Help architecture</span></span>

<span data-ttu-id="4b5fd-107">يبين الرسم التوضيحي التالي أجزاء نظام التعليمات.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="4b5fd-108">يعمل نظام التعليمات في المنتج على سحب المقالات من https://docs.microsoft.com، وكذلك دلائل المهام المخزنة في "أداة تكوين عمليات الأعمال" في Lifecycle Services (LCS)‎.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="4b5fd-109">الميزات المدرجة في الرسم التخطيطي مع العلامة النجمية (\*) عبارة عن ميزات تم التخطيط لإصدارها، ولكنها غير متوفرة حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="4b5fd-110">[![بنية التعليمات](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="4b5fd-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="4b5fd-111">الاتصال بنظام التعليمات</span><span class="sxs-lookup"><span data-stu-id="4b5fd-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="4b5fd-112">في الوقت الحالي لا تتوفر علامة التبويب **دلائل المهام** في Dynamics 365 Talent أو في Retail.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="4b5fd-113">نحن نعمل حاليًا على تمكين هذه الوظيفة في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="4b5fd-114">تبقى دلائل المهام في تجربة "بدء الاستخدام" في Talent متوفرة لتغطية الوظائف الأساسية.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="4b5fd-115">كما تتوفر تعليمات إجرائية في الموقع docs.microsoft.com لكل من Retail وTalent.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="4b5fd-116">من خلال استخدام صفحة **معلمات النظام**، يتصل مسؤولو النظام بأجزاء نظام التعليمات لتطبيقها.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="4b5fd-117">[![نموذج محددات النظام مع إعدادات نظام التعليمات](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="4b5fd-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="4b5fd-118">في صفحة **محددات النظام‬**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="4b5fd-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b5fd-119">في المرة الأولى التي تفتح فيها علامة التبويب **تعليمات** يجب الاتصال بميزة Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="4b5fd-120">احرص على النقر فوق الارتباط الموجود في وسط النموذج، وانتظر الاتصال، ثم قم بإغلاق مربع الحوار، ثم انقر فوق **موافق** للوصول إلى صفحة **معلمات النظام**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="4b5fd-121">[![الاتصال بـ LCS](./media/connect-to-lcs-crop-1024x365.png "الاتصال بـ LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="4b5fd-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="4b5fd-122">تحديد مشروع Lifecycle Services المراد الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="4b5fd-123">تحديد مكتبات BPM (في المشروع المحدد) لاسترداد تسجيلات المهام منها.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="4b5fd-124">تعيين أمر العرض لمكتبات BPM.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="4b5fd-125">ويحدد هذا الترتيب الذي ستظهر به تسجيلات المهام من المكتبات في جزء **المساعدة**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="4b5fd-126">بعد أن تكمل هذه الخطوات، يمكنك فتح جزء **التعليمات** والنقر فوق علامة تبويب **دلائل المهام**. سترى الآن دلائل المهام التي تنطبق على الصفحة التي تعمل عليها حاليًا في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="4b5fd-127">إذا لم تعثر على دلائك المهام، فيمكنك إدخال كلمات أساسية لتنقية البحث.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="4b5fd-128">إظهار دلائل المهام المترجمة</span><span class="sxs-lookup"><span data-stu-id="4b5fd-128">Showing translated task guides</span></span>

<span data-ttu-id="4b5fd-129">تم شحن دلائل المهام المترجمة لأول مرة في شهر مايو 2016 لمكتبة بدء الاستخدام والمكتبة الموحدة APQC.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="4b5fd-130">في تطبيقات Finance and Operations، لرؤية تعليمات دلائل المهام المترجمة، تأكد من اتصالك بمكتبة مايو.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="4b5fd-131">يمكن للمستخدم التحكم في اللغة التي يظهر بها دليل المهام بواسطة إعدادات اللغة ضمن**الخيارات** &gt; **التفضيلات**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="4b5fd-132">على الرغم من العدد الكبير من دلائل المهام التي تمت ترجمتها، إلا أن العميل لا يعرض الآن أسماء دلائل المهام المترجمة.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="4b5fd-133">علاوةً على ذلك، لا تتضمن مكتبة شهر مايو سوى دلائل المهام المترجمة التي تم إصدارها في شهر فبراير 2016.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="4b5fd-134">سوف نقوم بإصدار مكتبة محدثة تضم ترجمات إضافية.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="4b5fd-135">إذا كان دليل المهمة مترجمًا، فسيظهر نصه بلغتك المحددة عندما تفتحه.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="4b5fd-136">إذا لم يكن دليل المهمة مترجمًا بعد، فسيظهر بعض النص فقط (نصر عناصر التحكم) بلغتك المحددة عندما تفتحه.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="4b5fd-137">إنشاء التعليمات المخصصة</span><span class="sxs-lookup"><span data-stu-id="4b5fd-137">Creating custom help</span></span>

<span data-ttu-id="4b5fd-138">يمكنك استخدام أدلة المهام لإنشاء تعليمات مخصصة أو ربط موقع الويب بجزء التعليمات.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="4b5fd-139">إنشاء التعليمات المخصصة باستخدام أدلة المهام</span><span class="sxs-lookup"><span data-stu-id="4b5fd-139">Create custom help with task guides</span></span>

<span data-ttu-id="4b5fd-140">يمكنك إنشاء تعليمات مخصصة للتطبيق Finance وSupply Chain Management وRetail بإنشاء تسجيلات المهام التي تعكس عملية التنفيذ التي تقوم بها، وحفظها إلى مكتبة عمليات أعمال LCS.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="4b5fd-141">لا يمكنك إنشاء دلائل مهام مخصصة لتطبيق Talent.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="4b5fd-142">وبالنسبة للشركاء، إذا قمت بترقية مكتبة إلى مكتبة شركة وقمت بتضمينها في أحد حلول، فستتوفر للعملاء.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="4b5fd-143">يمكنك أيضًا إنشاء نسخة من المكتبة العمومية الموحدة APQC، ثم فتح نسختك وفتح تسجيلات المهام منها وتعديلها وحفظ التسجيلات مع تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="4b5fd-144">لمزيد من المعلومات، راجع [موارد مسجل المهام](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fd-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="4b5fd-145">الاتصال بموقع مخصص</span><span class="sxs-lookup"><span data-stu-id="4b5fd-145">Connect a custom site</span></span>

<span data-ttu-id="4b5fd-146">قامت Microsoft بتوفير مستند تقني وعينات من الأكواد التي توضح كيفية إنشاء وربط موقع تعليمات مخصص بجزء التعليمات.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="4b5fd-147">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="4b5fd-147">For more information, see:</span></span>

- [<span data-ttu-id="4b5fd-148">إنشاء تعليمات مخصصة لتطبيقات Finance and Operations (المستند التقني)</span><span class="sxs-lookup"><span data-stu-id="4b5fd-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="4b5fd-149">مستودع التعليمات المخصصة لـ GitHub</span><span class="sxs-lookup"><span data-stu-id="4b5fd-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="4b5fd-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4b5fd-150">Additional resources</span></span>

[<span data-ttu-id="4b5fd-151">نظام التعليمات</span><span class="sxs-lookup"><span data-stu-id="4b5fd-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="4b5fd-152">موارد مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="4b5fd-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="4b5fd-153">إنشاء الوثائق أو التدريب بمسجل المهام</span><span class="sxs-lookup"><span data-stu-id="4b5fd-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
