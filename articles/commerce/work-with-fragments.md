---
title: العمل باستخدام الأجزاء
description: يوضح هذا الموضوع سبب وقت وكيفية استخدام الأجزاء في Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914690"
---
# <a name="work-with-fragments"></a><span data-ttu-id="58db9-103">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="58db9-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="58db9-104">يوضح هذا الموضوع سبب وقت وكيفية استخدام الأجزاء في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="58db9-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="58db9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="58db9-105">Overview</span></span>

<span data-ttu-id="58db9-106">تسمح الأجزاء بتجربة تأليف مركزية لتكوينات الوحدة النمطية التي يجب إعادة استخدامها في الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="58db9-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="58db9-107">على سبيل المثال، غالبًا ما يتم تكوين الرؤوس والتذييلات والشعارات كأجزاء، لأنه تتم مشاركتها عبر العديد من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="58db9-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="58db9-108">يمكنك اعتبار الأجزاء كصفحات ويب مصغرة يمكن إدراجها في صفحات أخرى على موقعك.</span><span class="sxs-lookup"><span data-stu-id="58db9-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="58db9-109">تحتوي الأجزاء على دورة حياة خاصة بها.</span><span class="sxs-lookup"><span data-stu-id="58db9-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="58db9-110">بمعنى آخر، يتم إنشاءها والإشارة إليها وتحديثها وحذفها ككيانات مستقلة في أدوات التأليف.</span><span class="sxs-lookup"><span data-stu-id="58db9-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="58db9-111">بعد تكوين الأجزاء، فإنه يمكن استخدامها أينما يمكن استخدام الوحدات النمطية في بنية الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="58db9-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="58db9-112">يمكن الإشارة إلى الأجزاء في الصفحات وفي التخطيطات وفي القوالب وفي أجزاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="58db9-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="58db9-113">يمكن أن تتداخل الأجزاء حتى عمق سبعة مستويات داخل أجزاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="58db9-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="58db9-114">على سبيل المثال، إذا كنت تريد ترقية الحدث الموسمي عبر العديد من الصفحات في الموقع الخاص بنا، فإنه يمكنك استخدام جزء.</span><span class="sxs-lookup"><span data-stu-id="58db9-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="58db9-115">إن الخطوة الأولى في عملية إنشاء جزء جديد هي تحديد نوع الوحدة النمطية التي ترغب في البدء منها.</span><span class="sxs-lookup"><span data-stu-id="58db9-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="58db9-116">على سبيل المثال، يمكنك إنشاء الجزء من الوحدة النمطية لجزء رئيسي.</span><span class="sxs-lookup"><span data-stu-id="58db9-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="58db9-117">يمكن إنشاء الأجزاء من أي نوع وحدة نمطية.</span><span class="sxs-lookup"><span data-stu-id="58db9-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="58db9-118">يمكنك حينها تكوين جزء الجزء الرئيسي بالمحتوى الترويجي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="58db9-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="58db9-119">يمكنك أيضًا تعريبها على النحو الذي تريده.</span><span class="sxs-lookup"><span data-stu-id="58db9-119">You can also localize it as you require.</span></span> <span data-ttu-id="58db9-120">يمكن بعد ذلك استهلاك جزء الجزء الرئيسي المستقل الجديد كوحدة نمطية مكونة مسبقًا في الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="58db9-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="58db9-121">يمكنك بسهوله اضافته إلى القوالب أو إلى صفحات معينة أو إلى أجزاء أخرى يمكن أن تحتوي على وحدات نمطية لجزء رئيسي.</span><span class="sxs-lookup"><span data-stu-id="58db9-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="58db9-122">تُعد كافة الأماكن التي تمت إضافة الجزء فيها مراجع إلى جزء الجزء الرئيسي المركزي الذي قمت بإنشاءه.</span><span class="sxs-lookup"><span data-stu-id="58db9-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="58db9-123">إذا قمت بنشر التغييرات إلى الجزء، ستظهر هذه التغييرات على الفور في كافة الأماكن التي يتم فيها الإشارة إلى الجزء عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="58db9-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="58db9-124">لذلك، توفر الأجزاء طريقة فعالة وقوية لإعادة استخدام تكوينات الوحدة النمطية وإدارتها مركزيًا على موقع ما.</span><span class="sxs-lookup"><span data-stu-id="58db9-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="58db9-125">وباستخدامها بفاعلية، فإنه يمكنك زيادة المرونة والمساعدة على تقليل التكلفة المقترنة بإدارة محتوى الموقع بشكل ملحوظ.</span><span class="sxs-lookup"><span data-stu-id="58db9-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="58db9-126">يبين الرسم التوضيحي التالي الكيفية التي يمكن بها استخدام الأجزاء لتأليف تكوينات وحدة نمطية مشتركة مركزيًا عبر موقع تجارة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="58db9-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![رسم توضيحي يبين الكيفية التي يمكن بها استخدام الأجزاء لتأليف تكوينات وحدة نمطية مشتركة مركزيًا عبر موقع تجارة إلكترونية.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="58db9-128">إنشاء جزء</span><span class="sxs-lookup"><span data-stu-id="58db9-128">Create a fragment</span></span>

<span data-ttu-id="58db9-129">يمكنك إما إنشاء جزء جديد أو حفظ تكوين وحدة نمطية موجود كجزء.</span><span class="sxs-lookup"><span data-stu-id="58db9-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="58db9-130">إنشاء جزء جديد</span><span class="sxs-lookup"><span data-stu-id="58db9-130">Create a new fragment</span></span>

<span data-ttu-id="58db9-131">لإنشاء جزء جديد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="58db9-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="58db9-132">في جزء التنقل على اليسار، حدد **الأجزاء**.</span><span class="sxs-lookup"><span data-stu-id="58db9-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="58db9-133">حدد **جزء صفحة جديد**.</span><span class="sxs-lookup"><span data-stu-id="58db9-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="58db9-134">يظهر مربع حوار يعرض كافة أنواع الوحدات النمطية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="58db9-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="58db9-135">كما ذكر سابقًا، يمكن إنشاء الأجزاء من أي نوع من أنواع الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="58db9-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="58db9-136">حدد نوع الوحدة النمطية للجزء الخاص بك، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="58db9-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="58db9-137">وعن طريق تحديد نوع وحدة الحاوية النمطية العامة، فإنه يمكنك الحصول على أعلى درجات المرونة عند ضرورة تحديث الجزء الخاص بك وتكوينه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="58db9-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="58db9-138">حفظ تكوين وحدة نمطية موجودة كجزء</span><span class="sxs-lookup"><span data-stu-id="58db9-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="58db9-139">لتحويل وحدة نمطية تم تكوينها مسبقًا إلى جزء قابل لإعادة الاستخدام، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="58db9-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="58db9-140">افتح صفحة أو قالب يحتوي على الوحدة النمطية التي تريد تحويلها إلى جزء.</span><span class="sxs-lookup"><span data-stu-id="58db9-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="58db9-141">في جزء المخطط التفصيلي الموجود على اليسار، حدد زر علامة الحذف (**...**) المجاور لاسم الوحدة النمطية، ثم حدد **حفظ كجزء**.</span><span class="sxs-lookup"><span data-stu-id="58db9-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="58db9-142">سوف يظهر مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="58db9-142">A dialog box appears.</span></span>
1. <span data-ttu-id="58db9-143">أدخل اسمًا وبيانات تعريف للجزء.</span><span class="sxs-lookup"><span data-stu-id="58db9-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="58db9-144">حدد **موافق** لحفظ تكوين الوحدة النمطية كجزء يمكن إضافته إلى الصفحات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="58db9-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="58db9-145">إضافة أجزاء إلى صفحة أو ازالتها أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="58db9-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="58db9-146">تصف الإجراءات التالية كيفية إضافة الأجزاء وإزالتها وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="58db9-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="58db9-147">إضافة جزء</span><span class="sxs-lookup"><span data-stu-id="58db9-147">Add a fragment</span></span>

<span data-ttu-id="58db9-148">لإضافة جزء إلى صفحة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="58db9-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="58db9-149">في جزء المخطط التفصيلي الموجود على اليسار، حدد حاوية أو فتحة يمكن إضافة وحدات نمطية تابعة إليها.</span><span class="sxs-lookup"><span data-stu-id="58db9-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="58db9-150">حدد زر علامة الحذف المجاور لاسم الحاوية أو الفتحة، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="58db9-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="58db9-151">سوف يظهر مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="58db9-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58db9-152">إذا كانت الحاوية أو الفتحة لا تدعم وحدات تابعة جديدة، فلن يكون خيار **إضافة جزء** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="58db9-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="58db9-153">في مربع الحوار، ابحث عن جزء وحدده لإضافته.</span><span class="sxs-lookup"><span data-stu-id="58db9-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="58db9-154">إذا لم يتم سرد الأجزاء المتوفرة، فقد تحتاج أولاً إلى إنشاء جزء من نوع الوحدة النمطية التي تدعمها الحاوية أو الفتحة المحددة.</span><span class="sxs-lookup"><span data-stu-id="58db9-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="58db9-155">حدد **موافق** لإضافة الجزء المحدد للحاوية أو الفتحة المحددة على الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="58db9-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="58db9-156">يتم تعريف الوحدات النمطية المسموح بها في حاوية أو فتحة بواسطة قالب الصفحة أو تعريفات الوحدات النمطية الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="58db9-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="58db9-157">إزالة جزء</span><span class="sxs-lookup"><span data-stu-id="58db9-157">Remove a fragment</span></span>

<span data-ttu-id="58db9-158">لإزالة جزء من فتحة أو حاوية على صفحة، فاتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="58db9-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="58db9-159">في جزء المخطط التفصيلي الموجود على اليسار، حدد زر علامة الحذف المجاور لاسم الجزء المراد إزالته، ثم حدد زر سلة المهملات.</span><span class="sxs-lookup"><span data-stu-id="58db9-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="58db9-160">عند مطالبتك بتأكيد رغبتك في إزالة الجزء، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="58db9-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="58db9-161">عندما تقوم بازالة جزء من صفحة، فإنك تزيل المرجع إليه فقط من تلك الصفحة.</span><span class="sxs-lookup"><span data-stu-id="58db9-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="58db9-162">**لا** تقم بحذف الجزء من الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="58db9-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="58db9-163">لحذف أجزاء من الموقع الخاص بك، فإنه يجب عليك استخدام واجهة مستخدم مفتش الجزء (UI).</span><span class="sxs-lookup"><span data-stu-id="58db9-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="58db9-164">يمكنك حذف أجزاء من موقع فقط إذا لم يكن مشار إليها حاليًا بواسطة أية صفحات أو قوالب أو أجزاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="58db9-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="58db9-165">تحرير جزء</span><span class="sxs-lookup"><span data-stu-id="58db9-165">Edit a fragment</span></span>

<span data-ttu-id="58db9-166">لتحرير أجزاء، يجب عليك استخدام واجهة مستخدم محرر الجزء.</span><span class="sxs-lookup"><span data-stu-id="58db9-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="58db9-167">يتم هذا القيد بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="58db9-167">This restriction is by design.</span></span> <span data-ttu-id="58db9-168">إنه يساعد على ضمان أن المؤلفين لا يخلطون بين عملية تحرير الوحدات النمطية لصفحة محددة مع عملية تحرير الأجزاء التي قد يتم مشاركتها عبر العديد من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="58db9-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="58db9-169">لتحرير جزء، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="58db9-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="58db9-170">في جزء التنقل على اليسار، حدد **الأجزاء**.</span><span class="sxs-lookup"><span data-stu-id="58db9-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="58db9-171">ضمن **أجزاء**، حدد الجزء المراد تحريره.</span><span class="sxs-lookup"><span data-stu-id="58db9-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="58db9-172">قم بتحرير خصائص وبنية الوحدة النمطية لجزء كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="58db9-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="58db9-173">تمثل العملية عملية تحرير الوحدات النمطية في طريقة عرض محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="58db9-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="58db9-174">يمكنك أيضًا تحرير جزء عن طريق تحديده في صفحة أو في قالب أو في جزء أصل، ثم تحديد **تحرير جزء** في جزء الخصائص الموجود على الجانب الأيمن.</span><span class="sxs-lookup"><span data-stu-id="58db9-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58db9-175">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="58db9-175">Additional resources</span></span>

[<span data-ttu-id="58db9-176">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="58db9-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="58db9-177">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="58db9-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="58db9-178">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="58db9-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="58db9-179">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="58db9-179">Work with publish groups</span></span>](publish-groups.md)