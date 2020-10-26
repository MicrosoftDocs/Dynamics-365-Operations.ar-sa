---
title: معاينه التجربة ونشرها
description: يوضح هذا الموضوع كيفيه معاينه التجربة ونشرها من Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930133"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="782f0-103">معاينه التجربة ونشرها</span><span class="sxs-lookup"><span data-stu-id="782f0-103">Preview and publish an experiment</span></span>

<span data-ttu-id="782f0-104">يصف هذا الموضوع كيفيه معاينه التجربة الخاصة بك ونشرها في Dynamics 365 Commerce بعد قيامك [بتوصيل التجربة وتحرير التباينات الخاصة بك](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="782f0-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="782f0-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="782f0-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="782f0-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="782f0-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="782f0-107">[![رحلة مستخدم التجربة - المعاينه والنشر](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="782f0-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="782f0-108">معاينه تباينات التجربة الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="782f0-108">Preview your experiment variations</span></span>
<span data-ttu-id="782f0-109">يمكنك معاينه التباينات الخاصة بك ومتابعه تحريرها حتى تبدو بالطريقة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="782f0-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="782f0-110">في منشئ الموقع، استخدم القائمة المنسدلة تباينات أسفل شريط الأوامر لتحديد المحتوي الذي تريد معاينته.</span><span class="sxs-lookup"><span data-stu-id="782f0-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="782f0-111">حدد **معاينه** في الشريط العلوي.</span><span class="sxs-lookup"><span data-stu-id="782f0-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="782f0-112">يتم عرض معاينه لما سيبدو عليه المحتوي عند نشره.</span><span class="sxs-lookup"><span data-stu-id="782f0-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="782f0-113">لمعاينه تباين مختلف، قم بتحديده من القائمة المنسدلة الخاصة بالتباين وحدد **معاينه** مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="782f0-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="782f0-114">انشر تجربتك</span><span class="sxs-lookup"><span data-stu-id="782f0-114">Publish your experiment</span></span>
<span data-ttu-id="782f0-115">إذا كنت لا تستخدم مجموعه نشر لجدوله وقت وصول التجربة الخاصة بك وترغب في النشر علي الفور، حدد **نشر** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="782f0-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="782f0-116">سيتم نشر كافة الاختلافات التي تنتمي إلى التجربة.</span><span class="sxs-lookup"><span data-stu-id="782f0-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="782f0-117">إذا كانت الصفحة تحتوي علي URL غير منشور، يجب أولا نشر محدد موقع المعلومات (URL) أو لن يكون مرئيا لمستخدمي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="782f0-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="782f0-118">للحصول على مزيد من التفاصيل، راجع [حفظ صفحة ومعاينتها ونشرها](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="782f0-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="782f0-119">استخدام مجموعات النشر للجدولة عندما يتم نشر التجربة الخاصة بك بشكل مباشر</span><span class="sxs-lookup"><span data-stu-id="782f0-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="782f0-120">يمكن جدوله الاختلافات التي تم إنشاؤها في منشئ المواقع للنشر باستخدام مجموعه النشر.</span><span class="sxs-lookup"><span data-stu-id="782f0-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="782f0-121">داخل مجموعه نشر، يمكنك توصيل صفحه أو جزء بالتجربة الخاصة بك عن طريق الانتقال إلى علامة التبويب **التجارب** أو علامة التبويب **الصفحات** أو **الأجزاء** . لمزيد من المعلومات، راجع [الاتصال بتجربة وتحرير موضوع التباينات](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="782f0-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="782f0-122">للحصول على معلومات حول نشر المجموعات، راجع [العمل مع مجموعات النشر](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="782f0-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="782f0-123">عند استخدامك نشر مجموعات مع التجارب، هناك بعض الاعتبارات الهامه التي يجب ان تكون علي علم بها.</span><span class="sxs-lookup"><span data-stu-id="782f0-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="782f0-124">عندما تقوم باضافه صفحه أو جزء تم تشغيل تجربة عليه في مجموعه نشر، ستتم أزاله التجربة من الصفحة أو الجزء في مجموعه النشر.</span><span class="sxs-lookup"><span data-stu-id="782f0-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="782f0-125">لا تتوفر التجارب المتصلة بالصفحات الموجودة في موقع مباشر للصفحات الموجودة في نشر المجموعات والعكس بالعكس.</span><span class="sxs-lookup"><span data-stu-id="782f0-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="782f0-126">بالمثل، لا تتوفر الصفحات التي يتم تشغيل التجارب عليها في موقع مباشر لتجارب أخرى في مجموعات النشر والعكس.</span><span class="sxs-lookup"><span data-stu-id="782f0-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="782f0-127">عند نشر مجموعه نشر أو جدولتها، يتم نشر كافة المحتويات الموجودة في مجموعه النشر، بغض النظر عما إذا كان هناك تجربه مقترنة بمجموعه النشر.</span><span class="sxs-lookup"><span data-stu-id="782f0-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="782f0-128">ونظرا لاستمرار استمرار مجموعه النشر بعد نشرها إلى موقع مباشر ، ستستمر الاكسبيريمينتس في مجموعه النشر أيضا.</span><span class="sxs-lookup"><span data-stu-id="782f0-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="782f0-129">لذلك، لن تتمكن من اقران التجارب الأخرى بنفس الصفحة أو الجزء.</span><span class="sxs-lookup"><span data-stu-id="782f0-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="782f0-130">لتجنب هذا القيد، قم بحذف إيه مجموعات نشر تحتوي على تجارب مستمرة.</span><span class="sxs-lookup"><span data-stu-id="782f0-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="782f0-131">بالمثل، إذا كنت ترغب في حذف تجربه في موقع مباشر موجود أيضا في مجموعه نشر، فقم بحذفه من مجموعة النشر أولا.</span><span class="sxs-lookup"><span data-stu-id="782f0-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="782f0-132">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="782f0-132">Previous step</span></span>
[<span data-ttu-id="782f0-133">الاتصال بتجربة وتحريرها</span><span class="sxs-lookup"><span data-stu-id="782f0-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="782f0-134">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="782f0-134">Next step</span></span>
[<span data-ttu-id="782f0-135">تشغيل تجربة ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="782f0-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
