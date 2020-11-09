---
title: العمل باستخدام الأجزاء
description: يوضح هذا الموضوع سبب وقت وكيفية استخدام الأجزاء في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f1525610fb16edd5ff9ccefe0194f6f27b797b62
ms.sourcegitcommit: b063bf3a52f19baa11ddba31ef9313d58a0f610e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4019554"
---
# <a name="work-with-fragments"></a><span data-ttu-id="9001f-103">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="9001f-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="9001f-104">يوضح هذا الموضوع سبب وقت وكيفية استخدام الأجزاء في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9001f-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9001f-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="9001f-105">Overview</span></span>

<span data-ttu-id="9001f-106">تسمح الأجزاء بتجربة تأليف مركزية لتكوينات الوحدة النمطية التي يجب إعادة استخدامها في الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="9001f-107">على سبيل المثال، غالبًا ما يتم تكوين الرؤوس والتذييلات والشعارات كأجزاء، لأنه تتم مشاركتها عبر العديد من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="9001f-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="9001f-108">يمكنك اعتبار الأجزاء كصفحات ويب مصغرة يمكن إدراجها في صفحات أخرى على موقعك.</span><span class="sxs-lookup"><span data-stu-id="9001f-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="9001f-109">تحتوي الأجزاء على دورة حياة خاصة بها.</span><span class="sxs-lookup"><span data-stu-id="9001f-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="9001f-110">بمعنى آخر، يتم إنشاءها والإشارة إليها وتحديثها وحذفها ككيانات مستقلة في أدوات التأليف.</span><span class="sxs-lookup"><span data-stu-id="9001f-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="9001f-111">بعد تكوين الأجزاء، فإنه يمكن استخدامها أينما يمكن استخدام الوحدات النمطية في بنية الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="9001f-112">يمكن الإشارة إلى الأجزاء في الصفحات وفي التخطيطات وفي القوالب وفي أجزاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="9001f-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="9001f-113">يمكن أن تتداخل الأجزاء حتى عمق سبعة مستويات داخل أجزاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="9001f-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="9001f-114">على سبيل المثال، إذا كنت تريد ترقية الحدث الموسمي عبر العديد من الصفحات في الموقع الخاص بنا، فإنه يمكنك استخدام جزء.</span><span class="sxs-lookup"><span data-stu-id="9001f-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="9001f-115">إن الخطوة الأولى في عملية إنشاء جزء جديد هي تحديد نوع الوحدة النمطية التي ترغب في البدء منها.</span><span class="sxs-lookup"><span data-stu-id="9001f-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="9001f-116">على سبيل المثال، يمكنك إنشاء الجزء من الوحدة النمطية لجزء رئيسي.</span><span class="sxs-lookup"><span data-stu-id="9001f-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="9001f-117">يمكن إنشاء الأجزاء من أي نوع وحدة نمطية.</span><span class="sxs-lookup"><span data-stu-id="9001f-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="9001f-118">يمكنك حينها تكوين جزء الجزء الرئيسي بالمحتوى الترويجي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="9001f-119">يمكنك أيضًا تعريبها على النحو الذي تريده.</span><span class="sxs-lookup"><span data-stu-id="9001f-119">You can also localize it as you require.</span></span> <span data-ttu-id="9001f-120">يمكن بعد ذلك استهلاك جزء الجزء الرئيسي المستقل الجديد كوحدة نمطية مكونة مسبقًا في الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="9001f-121">يمكنك بسهوله اضافته إلى القوالب أو إلى صفحات معينة أو إلى أجزاء أخرى يمكن أن تحتوي على وحدات نمطية لجزء رئيسي.</span><span class="sxs-lookup"><span data-stu-id="9001f-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="9001f-122">تُعد كافة الأماكن التي تمت إضافة الجزء فيها مراجع إلى جزء الجزء الرئيسي المركزي الذي قمت بإنشاءه.</span><span class="sxs-lookup"><span data-stu-id="9001f-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="9001f-123">إذا قمت بنشر التغييرات إلى الجزء، ستظهر هذه التغييرات على الفور في كافة الأماكن التي يتم فيها الإشارة إلى الجزء عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="9001f-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="9001f-124">لذلك، توفر الأجزاء طريقة فعالة وقوية لإعادة استخدام تكوينات الوحدة النمطية وإدارتها مركزيًا على موقع ما.</span><span class="sxs-lookup"><span data-stu-id="9001f-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="9001f-125">وباستخدامها بفاعلية، فإنه يمكنك زيادة المرونة والمساعدة على تقليل التكلفة المقترنة بإدارة محتوى الموقع بشكل ملحوظ.</span><span class="sxs-lookup"><span data-stu-id="9001f-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="9001f-126">يبين الرسم التوضيحي التالي الكيفية التي يمكن بها استخدام الأجزاء لتأليف تكوينات وحدة نمطية مشتركة مركزيًا عبر موقع تجارة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9001f-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![رسم توضيحي يبين الكيفية التي يمكن بها استخدام الأجزاء لتأليف تكوينات وحدة نمطية مشتركة مركزيًا عبر موقع تجارة إلكترونية.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="9001f-128">إنشاء جزء</span><span class="sxs-lookup"><span data-stu-id="9001f-128">Create a fragment</span></span>

<span data-ttu-id="9001f-129">يمكنك إما إنشاء جزء جديد أو حفظ تكوين وحدة نمطية موجود كجزء.</span><span class="sxs-lookup"><span data-stu-id="9001f-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="9001f-130">حفظ تكوين وحدة نمطية موجودة كجزء</span><span class="sxs-lookup"><span data-stu-id="9001f-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="9001f-131">لتحويل وحدة نمطية تم تكوينها مسبقًا إلى جزء قابل لإعادة الاستخدام في منشئ مواقع Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9001f-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9001f-132">افتح صفحة أو قالب يحتوي على الوحدة النمطية التي تريد تحويلها إلى جزء.</span><span class="sxs-lookup"><span data-stu-id="9001f-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="9001f-133">في جزء المخطط التفصيلي الموجود إلى اليمين أو مباشرة في أداة إنشاء الصفحة المرئية، حدد الوحدة النمطية التي تم تكوينها في السابق.</span><span class="sxs-lookup"><span data-stu-id="9001f-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="9001f-134">حدد علامة القطع ( **...** ) إلى جانب اسم الوحدة في جزء المخطط التفصيلي أو في شريط أدوات أداة إنشاء الصفحة المرئية.</span><span class="sxs-lookup"><span data-stu-id="9001f-134">Select the ellipsis ( **...** ) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="9001f-135">حدد **مشاركه كجزء**.</span><span class="sxs-lookup"><span data-stu-id="9001f-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="9001f-136">في مربع الحوار **حفظ كجزء** ، ادخل اسمًا لهذا الجزء.</span><span class="sxs-lookup"><span data-stu-id="9001f-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="9001f-137">حدد **موافق** لحفظ تكوين الوحدة النمطية كجزء يمكن إضافته إلى الصفحات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="9001f-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="9001f-138">إنشاء جزء جديد</span><span class="sxs-lookup"><span data-stu-id="9001f-138">Create a new fragment</span></span>

<span data-ttu-id="9001f-139">لإنشاء جزء جديد في منشئ موقع التجارة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9001f-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9001f-140">في جزء التنقل على اليسار، حدد **الأجزاء**.</span><span class="sxs-lookup"><span data-stu-id="9001f-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9001f-141">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9001f-141">Select **New**.</span></span> <span data-ttu-id="9001f-142">يظهر مربع حوار **جزء جديد** يعرض كافة أنواع الوحدات النمطية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="9001f-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="9001f-143">كما ذكر سابقًا، يمكن إنشاء الأجزاء من أي نوع من أنواع الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="9001f-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="9001f-144">حدد نوع الوحدة النمطية لجزء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="9001f-145">وعن طريق تحديد نوع وحدة الحاوية النمطية العامة، فإنه يمكنك الحصول على أعلى درجات المرونة عند ضرورة تحديث الجزء الخاص بك وتكوينه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="9001f-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="9001f-146">إضافة أجزاء إلى صفحة أو ازالتها أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="9001f-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="9001f-147">تصف الإجراءات التالية كيفية إضافة الأجزاء وإزالتها وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="9001f-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="9001f-148">إضافة جزء</span><span class="sxs-lookup"><span data-stu-id="9001f-148">Add a fragment</span></span>

<span data-ttu-id="9001f-149">لإضافة جزء إلى صفحة في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9001f-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9001f-150">في جزء المخطط التفصيلي إلى اليمين أو مباشرةً في أداة إنشاء الصفحة المرئية، حدد حاوية أو فتحة يمكن إضافة وحدات نمطية تابعة إليها.</span><span class="sxs-lookup"><span data-stu-id="9001f-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="9001f-151">حدد علامة القطع ( **...** ) إلى جانب اسم الفتحة أو الحاوية.</span><span class="sxs-lookup"><span data-stu-id="9001f-151">Select the ellipsis ( **...** ) next to the name of the container or slot.</span></span>  <span data-ttu-id="9001f-152">أو إذا كنت تستخدم أداة إنشاء الصفحة المرئية، فحدد رمز علامة الجمع ( **+** ).</span><span class="sxs-lookup"><span data-stu-id="9001f-152">Alternately, if using visual page builder, select the plus symbol ( **+** ).</span></span>  
1. <span data-ttu-id="9001f-153">حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="9001f-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="9001f-154">إذا كانت الحاوية أو الفتحة لا تدعم وحدات تابعة جديدة، فلن يكون خيار **إضافة جزء** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="9001f-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="9001f-155">في مربع الحوار **تحديد جزء** ، ابحث عن جزء وحدده لإضافته.</span><span class="sxs-lookup"><span data-stu-id="9001f-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="9001f-156">إذا لم يتم سرد الأجزاء المتوفرة، فقد تحتاج أولاً إلى إنشاء جزء من نوع الوحدة النمطية التي تدعمها الحاوية أو الفتحة المحددة.</span><span class="sxs-lookup"><span data-stu-id="9001f-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="9001f-157">حدد الجزء المطلوب لإضافته إلى الحاوية أو الفتحة على الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="9001f-158">يتم تعريف الوحدات النمطية المسموح بها في حاوية أو فتحة بواسطة قالب الصفحة أو تعريفات الوحدات النمطية الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="9001f-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="9001f-159">إزالة جزء</span><span class="sxs-lookup"><span data-stu-id="9001f-159">Remove a fragment</span></span>

<span data-ttu-id="9001f-160">لإزالة جزء من فتحة أو حاوية في صفحة في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9001f-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9001f-161">في جزء المخطط التفصيلي إلى اليمين، حدد علامة القطع ( **...** ) إلى جانب اسم الجزء المراد إزالته، ثم حدد رمز سلة المهملات.</span><span class="sxs-lookup"><span data-stu-id="9001f-161">In the outline pane on the left, select the ellipsis ( **...** ) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="9001f-162">بدلاً من ذلك، يمكنك تحديد الجزء الموجود في أداة إنشاء الصفحة المرئية وتحديد رمز سلة المهملات في شريط أدوات الجزء.</span><span class="sxs-lookup"><span data-stu-id="9001f-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="9001f-163">عند مطالبتك بتأكيد رغبتك في إزالة الجزء، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9001f-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9001f-164">عندما تقوم بازالة جزء من صفحة، فإنك تزيل المرجع إليه فقط من تلك الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9001f-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="9001f-165">**لا** تقم بحذف الجزء من الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9001f-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="9001f-166">لحذف أجزاء من الموقع الخاص بك، فإنه يجب عليك استخدام واجهة مستخدم مفتش الجزء (UI).</span><span class="sxs-lookup"><span data-stu-id="9001f-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="9001f-167">يمكنك حذف أجزاء من موقع فقط إذا لم يكن مشار إليها حاليًا بواسطة أية صفحات أو قوالب أو أجزاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="9001f-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="9001f-168">تحرير جزء</span><span class="sxs-lookup"><span data-stu-id="9001f-168">Edit a fragment</span></span>

<span data-ttu-id="9001f-169">لتحرير أجزاء، يجب عليك استخدام واجهة مستخدم محرر الجزء.</span><span class="sxs-lookup"><span data-stu-id="9001f-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="9001f-170">يتم هذا القيد بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="9001f-170">This restriction is by design.</span></span> <span data-ttu-id="9001f-171">إنه يساعد على ضمان أن المؤلفين لا يخلطون بين عملية تحرير الوحدات النمطية لصفحة محددة مع عملية تحرير الأجزاء التي قد يتم مشاركتها عبر العديد من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="9001f-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="9001f-172">لتحرير جزء في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9001f-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9001f-173">في جزء التنقل على اليسار، حدد **الأجزاء**.</span><span class="sxs-lookup"><span data-stu-id="9001f-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9001f-174">ضمن **أجزاء** ، حدد الجزء المراد تحريره.</span><span class="sxs-lookup"><span data-stu-id="9001f-174">Under **Fragments** , select the fragment to edit.</span></span>
1. <span data-ttu-id="9001f-175">قم بتحرير خصائص وبنية الوحدة النمطية لجزء كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="9001f-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="9001f-176">تمثل العملية عملية تحرير الوحدات النمطية في طريقة عرض محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9001f-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="9001f-177">يمكنك أيضًا تحرير جزء عن طريق تحديده في صفحة أو في قالب أو في جزء أصل، ثم تحديد **تحرير جزء** في جزء الخصائص الموجود على الجانب الأيمن.</span><span class="sxs-lookup"><span data-stu-id="9001f-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9001f-178">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9001f-178">Additional resources</span></span>

[<span data-ttu-id="9001f-179">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="9001f-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9001f-180">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="9001f-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="9001f-181">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="9001f-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="9001f-182">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="9001f-182">Work with publish groups</span></span>](publish-groups.md)
