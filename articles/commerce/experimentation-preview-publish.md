---
title: معاينه التجربة ونشرها
description: يوضح هذا الموضوع كيفيه معاينه التجربة ونشرها من Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097106"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="1b395-103">معاينه التجربة ونشرها</span><span class="sxs-lookup"><span data-stu-id="1b395-103">Preview and publish an experiment</span></span>

<span data-ttu-id="1b395-104">يصف هذا الموضوع كيفيه معاينه التجربة الخاصة بك ونشرها في Dynamics 365 Commerce بعد قيامك [بتوصيل التجربة وتحرير التباينات الخاصة بك](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="1b395-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="1b395-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1b395-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1b395-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="1b395-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="1b395-107">[![رحلة مستخدم التجربة - المعاينه والنشر](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1b395-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="1b395-108">معاينه تباينات التجربة الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="1b395-108">Preview your experiment variations</span></span>
<span data-ttu-id="1b395-109">يمكنك معاينه التباينات الخاصة بك ومتابعه تحريرها حتى تبدو بالطريقة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="1b395-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="1b395-110">لمعاينة تباينات التجربة الخاصة بك في منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1b395-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1b395-111">من القائمة المنسدلة تباينات أسفل شريط الأوامر، حدد المحتوى الذي تريد معاينته.</span><span class="sxs-lookup"><span data-stu-id="1b395-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="1b395-112">في شريط الأوامر، حدد **معاينة**.</span><span class="sxs-lookup"><span data-stu-id="1b395-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="1b395-113">يتم عرض معاينه لما سيبدو عليه المحتوي عند نشره.</span><span class="sxs-lookup"><span data-stu-id="1b395-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="1b395-114">لمعاينة تباين مختلف، قم بتحديده من القائمة المنسدلة الخاصة بالتباين وحدد **معاينة** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="1b395-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="1b395-115">انشر تجربتك</span><span class="sxs-lookup"><span data-stu-id="1b395-115">Publish your experiment</span></span>
<span data-ttu-id="1b395-116">إذا كنت لا تستخدم مجموعه نشر لجدوله وقت وصول التجربة الخاصة بك وترغب في النشر علي الفور، حدد **نشر** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="1b395-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="1b395-117">سيتم نشر كافة الاختلافات التي تنتمي إلى التجربة.</span><span class="sxs-lookup"><span data-stu-id="1b395-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="1b395-118">إذا كانت الصفحة تحتوي علي URL غير منشور، يجب أولا نشر محدد موقع المعلومات (URL) أو لن يكون مرئيا لمستخدمي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1b395-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="1b395-119">للحصول على مزيد من التفاصيل، راجع [حفظ صفحة ومعاينتها ونشرها](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="1b395-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="1b395-120">استخدام مجموعات النشر للجدولة عندما يتم نشر التجربة الخاصة بك بشكل مباشر</span><span class="sxs-lookup"><span data-stu-id="1b395-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="1b395-121">يمكن جدوله الاختلافات التي تم إنشاؤها في منشئ المواقع للنشر باستخدام مجموعه النشر.</span><span class="sxs-lookup"><span data-stu-id="1b395-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="1b395-122">داخل مجموعة نشر، يمكنك توصيل صفحة أو جزء بتجربتك الخاصة عن طريق تحديد **تجارب** في جزء التنقل الأيسر.</span><span class="sxs-lookup"><span data-stu-id="1b395-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="1b395-123">يمكنك أيضًا القيام بذلك عن طريق تحديد **الصفحات** أو **الأجزاء** واتباع التعليمات في [توصيل تجربة وتحرير التباينات](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="1b395-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="1b395-124">للحصول على معلومات حول نشر المجموعات، راجع [العمل مع مجموعات النشر](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="1b395-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="1b395-125">عند استخدامك نشر مجموعات مع التجارب، هناك بعض الاعتبارات الهامه التي يجب ان تكون علي علم بها.</span><span class="sxs-lookup"><span data-stu-id="1b395-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="1b395-126">عندما تقوم باضافه صفحه أو جزء تم تشغيل تجربة عليه في مجموعه نشر، ستتم أزاله التجربة من الصفحة أو الجزء في مجموعه النشر.</span><span class="sxs-lookup"><span data-stu-id="1b395-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="1b395-127">لا تتوفر التجارب المتصلة بالصفحات الموجودة في موقع مباشر للصفحات الموجودة في نشر المجموعات والعكس بالعكس.</span><span class="sxs-lookup"><span data-stu-id="1b395-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="1b395-128">بالمثل، لا تتوفر الصفحات التي يتم تشغيل التجارب عليها في موقع مباشر لتجارب أخرى في مجموعات النشر والعكس.</span><span class="sxs-lookup"><span data-stu-id="1b395-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="1b395-129">عند نشر مجموعه نشر أو جدولتها، يتم نشر كافة المحتويات الموجودة في مجموعه النشر، بغض النظر عما إذا كان هناك تجربه مقترنة بمجموعه النشر.</span><span class="sxs-lookup"><span data-stu-id="1b395-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="1b395-130">ونظرا لاستمرار استمرار مجموعه النشر بعد نشرها إلى موقع مباشر ، ستستمر الاكسبيريمينتس في مجموعه النشر أيضا.</span><span class="sxs-lookup"><span data-stu-id="1b395-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="1b395-131">لذلك، لن تتمكن من اقران التجارب الأخرى بنفس الصفحة أو الجزء.</span><span class="sxs-lookup"><span data-stu-id="1b395-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="1b395-132">لتجنب هذا القيد، قم بحذف إيه مجموعات نشر تحتوي على تجارب مستمرة.</span><span class="sxs-lookup"><span data-stu-id="1b395-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="1b395-133">بالمثل، إذا كنت ترغب في حذف تجربه في موقع مباشر موجود أيضا في مجموعه نشر، فقم بحذفه من مجموعة النشر أولا.</span><span class="sxs-lookup"><span data-stu-id="1b395-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="1b395-134">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="1b395-134">Previous step</span></span>
[<span data-ttu-id="1b395-135">الاتصال بتجربة وتحريرها</span><span class="sxs-lookup"><span data-stu-id="1b395-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="1b395-136">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="1b395-136">Next step</span></span>
[<span data-ttu-id="1b395-137">تشغيل تجربة ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="1b395-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
