---
title: "الاتصال بنظام التعليمات"
description: "يصف هذا الموضوع مكونات نظام تعليمات تطبيق Microsoft Dynamics 365 for Finance and Operations، ويقدم لمحة عامة عن كيفية توصيلها بالإضافة إلى ملخص حول كيفية إنشاء تعليمات مخصصة."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: a27b21ffcde9bfbb7e6276ef35b2e48bd23af70d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="904c2-103">الاتصال بنظام التعليمات</span><span class="sxs-lookup"><span data-stu-id="904c2-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="904c2-104">يصف هذا الموضوع المكونات التي تشكّل نظام تعليمات Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="904c2-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="904c2-105">ويقدم نظرة عامة حول كيفية توصيل هذه المكونات وملخصًا لكيفية إنشاء تعليمات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="904c2-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="904c2-106">بنية التعليمات</span><span class="sxs-lookup"><span data-stu-id="904c2-106">Help architecture</span></span>
<span data-ttu-id="904c2-107">يبين الرسم التوضيحي التالي أجزاء نظام تعليمات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="904c2-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="904c2-108">يعمل نظام التعليمات في المنتج على سحب المقالات من موقع Finance and Operations الموجود على https://docs.microsoft.com، وكذلك من دلائل المهام المخزنة في "أداة تكوين عمليات الأعمال" في Lifecycle Services (LCS)‎.</span><span class="sxs-lookup"><span data-stu-id="904c2-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="904c2-109">الميزات المدرجة في الرسم التخطيطي مع العلامة النجمية (\*) عبارة عن ميزات تم التخطيط لإصدارها، ولكنها غير متوفرة حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="904c2-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="904c2-110">[![بنية التعليمات](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="904c2-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="904c2-111">الاتصال بنظام التعليمات</span><span class="sxs-lookup"><span data-stu-id="904c2-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="904c2-112">علامة التبويب **دلائل المهام** غير متوفرة بعد في كل من Microsoft Dynamics 365 for Talent وMicrosoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="904c2-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="904c2-113">نحن نعمل حاليًا على تمكين هذه الوظيفة في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="904c2-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="904c2-114">تبقى دلائل المهام في تجربة "بدء الاستخدام" في Talent متوفرة لتغطية الوظائف الأساسية.</span><span class="sxs-lookup"><span data-stu-id="904c2-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="904c2-115">تتوفر أيضًا تعليمات إجرائية في الموقع docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) لكل من Retail وTalent.</span><span class="sxs-lookup"><span data-stu-id="904c2-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="904c2-116">من خلال استخدام صفحة **معلمات النظام**، يتصل مسؤولو النظام بأجزاء نظام التعليمات لتطبيقها.</span><span class="sxs-lookup"><span data-stu-id="904c2-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="904c2-117">[![نموذج معلمات النظام مع إعدادات التعليمات](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) في صفحة **معلمات النظام**‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="904c2-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="904c2-118">في المرة الأولى التي تفتح فيها علامة التبويب **تعليمات** يجب الاتصال بميزة Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="904c2-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="904c2-119">احرص على النقر فوق الارتباط الموجود في وسط النموذج، وانتظر الاتصال، وقم بإغلاق مربع الحوار، ثم انقر فوق **موافق** للانتقال إلى صفحة **معلمات النظام**.[![الاتصال بـ LCS](./media/connect-to-lcs-crop-1024x365.png "الاتصال بـ LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="904c2-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="904c2-120">تحديد مشروع Lifecycle Services المراد الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="904c2-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="904c2-121">تحديد مكتبات BPM (في المشروع المحدد) لاسترداد تسجيلات المهام منها.</span><span class="sxs-lookup"><span data-stu-id="904c2-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="904c2-122">بالنسبة إلى Finance and Operations، ولمحتوى Microsoft، حدد المكتبة الموحدة APQC (فبراير 2017) الأحدث لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="904c2-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="904c2-123">بالنسبة إلى Retail، سنقوم بإصدار مكتبة في المستقبل القريب.</span><span class="sxs-lookup"><span data-stu-id="904c2-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="904c2-124">لا تحتاج إلى تحديد مكتبة لتطبيق Talent — يتم تأسيس الاتصال بالمكتبة الصحيحة بالنيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="904c2-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="904c2-125">تعيين أمر العرض لمكتبات BPM.</span><span class="sxs-lookup"><span data-stu-id="904c2-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="904c2-126">ويحدد هذا الترتيب الذي ستظهر به تسجيلات المهام من المكتبات في جزء **المساعدة**.</span><span class="sxs-lookup"><span data-stu-id="904c2-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="904c2-127">بعد أن تكمل هذه الخطوات، يمكنك فتح جزء **التعليمات** والنقر فوق علامة تبويب **دلائل المهام**. سترى الآن دلائل المهام التي تنطبق على الصفحة التي تعمل عليها حاليًا في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="904c2-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="904c2-128">إذا لم تعثر على دلائك المهام، فيمكنك إدخال كلمات أساسية لتنقية البحث.</span><span class="sxs-lookup"><span data-stu-id="904c2-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="904c2-129">إظهار دلائل المهام المترجمة</span><span class="sxs-lookup"><span data-stu-id="904c2-129">Showing translated task guides</span></span>

<span data-ttu-id="904c2-130">تم شحن دلائل المهام المترجمة لأول مرة في شهر مايو 2016 لمكتبة بدء الاستخدام والمكتبة الموحدة APQC.</span><span class="sxs-lookup"><span data-stu-id="904c2-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="904c2-131">في Finance and Operations، لرؤية تعليمات دلائل المهام المترجمة، تأكد من اتصالك بمكتبة مايو.</span><span class="sxs-lookup"><span data-stu-id="904c2-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="904c2-132">يمكن للمستخدم التحكم في اللغة التي يظهر بها دليل المهام بواسطة إعدادات اللغة ضمن**الخيارات** &gt; **التفضيلات**.</span><span class="sxs-lookup"><span data-stu-id="904c2-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="904c2-133">على الرغم من العدد الكبير من دلائل المهام التي تمت ترجمتها، إلا أن عميل Finance and Operations لا يعرض أسماء دلائل المهام المترجمة.</span><span class="sxs-lookup"><span data-stu-id="904c2-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="904c2-134">علاوةً على ذلك، لا تتضمن مكتبة شهر مايو سوى دلائل المهام المترجمة التي تم إصدارها في شهر فبراير 2016.</span><span class="sxs-lookup"><span data-stu-id="904c2-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="904c2-135">سوف نقوم بإصدار مكتبة محدثة تضم ترجمات إضافية.</span><span class="sxs-lookup"><span data-stu-id="904c2-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="904c2-136">إذا كان دليل المهمة مترجمًا، فسيظهر نصه بلغتك المحددة عندما تفتحه.</span><span class="sxs-lookup"><span data-stu-id="904c2-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="904c2-137">إذا لم يكن دليل المهمة مترجمًا بعد، فسيظهر بعض النص فقط (نصر عناصر التحكم) بلغتك المحددة عندما تفتحه.</span><span class="sxs-lookup"><span data-stu-id="904c2-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="904c2-138">إنشاء التعليمات المخصصة</span><span class="sxs-lookup"><span data-stu-id="904c2-138">Creating custom help</span></span>
<span data-ttu-id="904c2-139">يمكنك إنشاء تعليمات مخصصة لتطبيق Finance and Operations وRetail بإنشاء تسجيلات المهام التي تعكس التنفيذ، وحفظها إلى مكتبة عمليات أعمال LCS.</span><span class="sxs-lookup"><span data-stu-id="904c2-139">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="904c2-140">لا يمكنك إنشاء دلائل مهام مخصصة لتطبيق Talent.</span><span class="sxs-lookup"><span data-stu-id="904c2-140">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="904c2-141">وبالنسبة للشركاء، إذا قمت بترقية مكتبة إلى مكتبة شركة وقمت بتضمينها في أحد حلول، فستتوفر للعملاء.</span><span class="sxs-lookup"><span data-stu-id="904c2-141">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="904c2-142">يمكنك أيضًا إنشاء نسخة من المكتبة العمومية الموحدة APQC، ثم فتح نسختك وفتح تسجيلات المهام منها وتعديلها وحفظ التسجيلات مع تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="904c2-142">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="904c2-143">لمزيد من المعلومات، راجع [كيفية إنشاء تسجيل مهام لاستخدامه كوثيقة أو تدريب](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="904c2-143">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="904c2-144">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="904c2-144">See also</span></span>
--------

[<span data-ttu-id="904c2-145">نظرة عامة حول التعليمات</span><span class="sxs-lookup"><span data-stu-id="904c2-145">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="904c2-146">نظرة عامة حول مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="904c2-146">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="904c2-147">كيفية إنشاء تسجيل مهمة لاستخدامه كوثائق أو تدريب</span><span class="sxs-lookup"><span data-stu-id="904c2-147">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)




