---
title: توصيل تجربة وتحرير التباينات
description: يصف هذا الموضوع كيفيه توصيل تجربه في خدمه جهة خارجيه بـ Dynamics 365 Commerce، وكيفيه تحرير التباينات للتجربة.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4c9c9463162f21cdaf40f1c4ed6d5ae51e97cb88
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799073"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="e7116-103">توصيل تجربة وتحرير التباينات</span><span class="sxs-lookup"><span data-stu-id="e7116-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="e7116-104">يصف هذا الموضوع كيفية توصيل التجربة الخاصة بك في التجارة وإجراء تغييرات على التباينات الخاصة بك بحيث تتم محاذاتها مع الفرضية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e7116-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="e7116-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7116-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e7116-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="e7116-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="e7116-107">[![رحلة مستخدم التجارب - التوصيل والتحرير](./media/experimentation_connect_edit.svg)](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="e7116-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="e7116-108">بعد [اعداد التجربة](experimentation-setup.md)في أحدي الخدمات التابعة لجهة خارجية، ستقوم بتوصيل التجربة في Dynamics 365 Commerce وتحرير تباينات التجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="e7116-109">اعتبارات التخطيط</span><span class="sxs-lookup"><span data-stu-id="e7116-109">Planning considerations</span></span>

<span data-ttu-id="e7116-110">قبل ان تقوم بتوصيل تجربتك في التجارة، ستحتاج إلى اتخاذ بعض القرارات التي تؤثر علي طريقه أداره التجارة للمحتوي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e7116-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="e7116-111">تحديد نطاق التجربة الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="e7116-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="e7116-112">عند توصيل أحد التجارب، تتم مطالبتك بتحديد نطاق التجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="e7116-113">يتم تعريف التجارب كنطاق **جزئي** أو كنطاق **كامل**.</span><span class="sxs-lookup"><span data-stu-id="e7116-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="e7116-114">اختر **جزئي** إذا كنت تريد عقد تجربه علي جزء محدد من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e7116-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="e7116-115">إذا قمت بتحديد هذا الخيار، فيجب عليك تحديد الوحدات النمطية المضمنة في التجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="e7116-116">يتم مزامنة التغييرات التي يتم اجراؤها علي أجزاء الصفحة الافتراضية أو الجزء غير المرتبطة بالتجربة تلقائيا عبر التباينات.</span><span class="sxs-lookup"><span data-stu-id="e7116-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="e7116-117">اختر **كامل** إذا كنت تريد اجراء تجربه علي صفحه بأكملها أو جزء منها.</span><span class="sxs-lookup"><span data-stu-id="e7116-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="e7116-118">يتم إنشاء نسخ منفصلة من الصفحة أو الجزء الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="e7116-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="e7116-119">لن تحتاج إلى تحديد الوحدات النمطية المضمنة في التجربة لان سطح التحرير بأكمله متوفر للتغيير.</span><span class="sxs-lookup"><span data-stu-id="e7116-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="e7116-120">يمكنك إضافة أو حذف أو إعادة ترتيب الوحدات النمطية حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e7116-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="e7116-121">ومع ذلك، إذا تم اجراء إيه تغييرات علي الصفحة الافتراضية أو الجزء الذي تقترن به التجربة، فيجب مزامنة هذه التغييرات يدويا عبر كافة التباينات.</span><span class="sxs-lookup"><span data-stu-id="e7116-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="e7116-122">إذا قمت باقران التجربة الخاصة بك مع الصفحة التي تستخدم تخطيطًا، يمكنك فقط جعل نطاق التجربة **كامل**.</span><span class="sxs-lookup"><span data-stu-id="e7116-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="e7116-123">تحديد ما إذا كنت ترغب في الجدولة عند نشر التجربة الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="e7116-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="e7116-124">إذا أردت جدوله وقت نشر التجربة إلى موقعك المباشر، فتاكد من توفر المحتوي الذي ترغب في ربطه بالتجربة في مجموعه نشر *قبل* توصيل التجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="e7116-125">لمزيد من المعلومات حول نشر المجموعات، راجع [العمل مع مجموعات النشر](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e7116-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="e7116-126">توصيل التجربة</span><span class="sxs-lookup"><span data-stu-id="e7116-126">Connect your experiment</span></span>
<span data-ttu-id="e7116-127">لتوصيل تجربتك، ستقوم بتشغيل معالج **توصيل التجربة**.</span><span class="sxs-lookup"><span data-stu-id="e7116-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="e7116-128">يرشدك هذا المعالج عبر الخطوات المطلوبة لتوصيل التجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="e7116-129">عند إكمال المعالج ، يتم ربط التجربة وإنشاء التباينات التي تم إنشاؤها وتصبح جاهزه للتحرير.</span><span class="sxs-lookup"><span data-stu-id="e7116-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="e7116-130">لبدء الاتصال بتجربتك في منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e7116-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e7116-131">لبدء تشغيل معالج **تجربة الاتصال**، حدد **التجارب** في جزء التنقل الأيسر، ثم حدد **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="e7116-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="e7116-132">وبدلاً من ذلك، يمكنك الوصول إلى المعالج من صفحة أو من محرر الجزء عن طريق تحريره وتحديد **توصيل التجربة** على شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="e7116-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7116-133">يمكن توصيل صفحه بتجربة واحده فقط في المرة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="e7116-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="e7116-134">لتوصيل صفحه بتجربة مختلفه، قم أولا بحذف التجربة التي تتصل بها الصفحة حاليا.</span><span class="sxs-lookup"><span data-stu-id="e7116-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="e7116-135">اختر الصفحة أو الجزء الذي تريد تشغيل التجربة عليه.</span><span class="sxs-lookup"><span data-stu-id="e7116-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="e7116-136">قم بتعيين نطاق التجارب إلى **جزئي** أو **كامل**، استنادا إلى الخيار الذي قمت به في مقطع [تحديد نطاق التجربة](#determine-the-scope-of-your-experiment) أعلاه.</span><span class="sxs-lookup"><span data-stu-id="e7116-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="e7116-137">يجب تمكين علامة الميزة **التجربة علي الصفحات أو الأجزاء** إذا كنت ترغب في التجربة علي صفحه كامله أو جزء منها.</span><span class="sxs-lookup"><span data-stu-id="e7116-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="e7116-138">راجع [التجارب في موضوع Dynamics 365 Commerce](experimentation-overview.md) لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="e7116-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="e7116-139">في الخطوة الاخيره من المعالج، حدد **إنشاء التباينات وإنهاء المعالج**.</span><span class="sxs-lookup"><span data-stu-id="e7116-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="e7116-140">ويتم إنشاء التباينات للتجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="e7116-141">تحرير التباينات</span><span class="sxs-lookup"><span data-stu-id="e7116-141">Edit your variations</span></span>
<span data-ttu-id="e7116-142">عند إنهاء المعالج، يتم إنشاء التباينات لك.</span><span class="sxs-lookup"><span data-stu-id="e7116-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="e7116-143">بعد ذلك، ستقوم بتحرير التباينات بحيث تعكس الاختيارات التي تحتاجها للتحقق في الفرضية الخاص بالتجربة.</span><span class="sxs-lookup"><span data-stu-id="e7116-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="e7116-144">اختر أحد الإجراءات التالية التي تتوافق مع النطاق الذي اخترته لتجربتك في مقطع [تحديد نطاق التجربة الخاص بك](#determine-the-scope-of-your-experiment) أعلاه.</span><span class="sxs-lookup"><span data-stu-id="e7116-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="e7116-145">تحرير التباينات للتجارب ذات النطاق الجزئي</span><span class="sxs-lookup"><span data-stu-id="e7116-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="e7116-146">اتبع الخطوات التالية إذا قمت بتحديد نطاق التجربة الخاصة بك على **جزئي** في معالج **توصيل التجربه**.</span><span class="sxs-lookup"><span data-stu-id="e7116-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="e7116-147">في عرض المحرر، استخدم القائمة المنسدلة التباينات أسفل شريط الأوامر لتحرير كل تباين استنادا إلى الافتراض الأصلي.</span><span class="sxs-lookup"><span data-stu-id="e7116-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="e7116-148">وقد ترغب أيضا في إنشاء عنصر تحكم أو اختلاف أساسي عن طريق ترك أحد التباينات دون تغيير.</span><span class="sxs-lookup"><span data-stu-id="e7116-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="e7116-149">حدد الوحدة النمطية التي ستتم تجربتها، وحدد علامة القطع (...)، ثم حدد **أضافه للتجربة**.</span><span class="sxs-lookup"><span data-stu-id="e7116-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="e7116-150">تحرير التباينات للتجارب ذات النطاق الكامل</span><span class="sxs-lookup"><span data-stu-id="e7116-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="e7116-151">إذا قمت بتحديد نطاق التجربة الخاصة بك على **كامل** في معالج **توصيل التجربة**، بينما في عرض المحرر ، استخدم القائمة المنسدلة تباينات أسفل شريط الأوامر لتحرير كل تباين استنادا إلى الافتراض الأصلي.</span><span class="sxs-lookup"><span data-stu-id="e7116-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="e7116-152">في كلتا الحالتين، قد ترغب أيضا في إنشاء عنصر تحكم أو اختلاف أساسي عن طريق ترك أحد التباينات دون تغيير.</span><span class="sxs-lookup"><span data-stu-id="e7116-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="e7116-153">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="e7116-153">Previous step</span></span>
[<span data-ttu-id="e7116-154">إعداد تجربة</span><span class="sxs-lookup"><span data-stu-id="e7116-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="e7116-155">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="e7116-155">Next step</span></span>
[<span data-ttu-id="e7116-156">معاينه التجربة ونشرها</span><span class="sxs-lookup"><span data-stu-id="e7116-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]