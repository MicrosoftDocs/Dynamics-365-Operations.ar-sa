---
title: العمل باستخدام الوحدات النمطية
description: يوضح هذا الموضوع كيفية استخدام الوحدات النمطية ووقت استخدامها في Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025869"
---
# <a name="work-with-modules"></a><span data-ttu-id="79c93-103">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-103">Work with modules</span></span>

<span data-ttu-id="79c93-104">يوضح هذا الموضوع كيفية استخدام الوحدات النمطية ووقت استخدامها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="79c93-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="79c93-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="79c93-105">Overview</span></span>

<span data-ttu-id="79c93-106">تُعد الوحدات النمطية كتل إنشاء منطقية تتكون منها بنية الصفحة الخاصة بك، ويكون لها أغراض ونطاقات متعددة.</span><span class="sxs-lookup"><span data-stu-id="79c93-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="79c93-107">وتُعد بعض الوحدات النمطية حاويات عالية المستوى، والغرض الوحيد منها هو استيعاب وتنظيم الوحدات النمطية الأخرى (الوحدات النمطية التابعة).</span><span class="sxs-lookup"><span data-stu-id="79c93-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="79c93-108">ويكون للوحدات النمطية الأخرى، مثل الوحدة النمطية البسيطة لوضع صورة، غرض محدد جدًا.</span><span class="sxs-lookup"><span data-stu-id="79c93-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="79c93-109">وتقع الوحدات النمطية الأخرى، مثل الوحدة النمطية الدوارة، في مكان ما بين هاتين الفئتين.</span><span class="sxs-lookup"><span data-stu-id="79c93-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="79c93-110">بشكل افتراضي، يتضمن موقع Dynamics 365 Commerce الخاص بك مكتبة الوحدة النمطية لأدوات البداية التي تسمح لك بتحقيق معظم سيناريوهات التجارة الإكترونية الأساسية.</span><span class="sxs-lookup"><span data-stu-id="79c93-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="79c93-111">يجب أن تكون قادرًا على إنشاء موقع تجارة إلكترونية شامل فقط باستخدام هذه الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="79c93-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="79c93-112">ومع ذلك، قد تحتاج أيضًا إلى تخصيص هذه الوحدات النمطية أو إنشاء وحدات نمطية مخصصة وجديدة لاحتياجات محددة.</span><span class="sxs-lookup"><span data-stu-id="79c93-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="79c93-113">إذا كنت ترغب في إنشاء وحدات نمطية مخصصة، تتوفر مجموعة تطوير برامج تصميم الوحدة النمطية (SDK) لمساعدتك في إنشاء مكتبة وحدة نمطية مخصصة.</span><span class="sxs-lookup"><span data-stu-id="79c93-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="79c93-114">وحدات الحاوية النمطية والفتحات</span><span class="sxs-lookup"><span data-stu-id="79c93-114">Container modules and slots</span></span>

<span data-ttu-id="79c93-115">كما ذكر سابقًا، يتم تصميم بعض الوحدات النمطية للاحتفاظ بالوحدات النمطية التابعة.</span><span class="sxs-lookup"><span data-stu-id="79c93-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="79c93-116">تُعرف هذه الوحدات باسم *الحاويات*، وتسمح بالتسلسلات الهرمية للوحدات النمطية المتداخلة.</span><span class="sxs-lookup"><span data-stu-id="79c93-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="79c93-117">تتضمن وحدات الحاوية النمطية *الفتحات*.</span><span class="sxs-lookup"><span data-stu-id="79c93-117">Container modules include *slots*.</span></span> <span data-ttu-id="79c93-118">تُستخدم الفتحات لمعالجة التخطيط والغرض من الوحدات النمطية التابعة في الحاوية.</span><span class="sxs-lookup"><span data-stu-id="79c93-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="79c93-119">وكمثال على الوحدة النمطية لحاوية الصفحة الأساسية (وحدة نمطية ذات مستوى أعلى لأي صفحة) التي تحدد عدة فتحات مهمة:</span><span class="sxs-lookup"><span data-stu-id="79c93-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="79c93-120">فتحة رأس</span><span class="sxs-lookup"><span data-stu-id="79c93-120">A header slot</span></span>
- <span data-ttu-id="79c93-121">فتحة نص أصلي</span><span class="sxs-lookup"><span data-stu-id="79c93-121">A body slot</span></span>
- <span data-ttu-id="79c93-122">فتحة تذييل</span><span class="sxs-lookup"><span data-stu-id="79c93-122">A footer slot</span></span>

<span data-ttu-id="79c93-123">يقوم مطور الوحدة النمطية بتحديد هذه الفتحات وتحديد الوحدات النمطية التابعة وعدد الوحدات النمطية التابعة التي يمكن وضعها مباشره داخلها.</span><span class="sxs-lookup"><span data-stu-id="79c93-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="79c93-124">على سبيل المثال، قد تدعم فتحة الرأس وحدة نمطية واحدة فقط لنوع **الوحدة النمطية للرأس**، بينما قد تدعم فتحة النص الأصلي عدد غير محدود من الوحدات النمطية من أي نوع (باستثناء الوحدات النمطية الأخرى لحاويات الصفحة).</span><span class="sxs-lookup"><span data-stu-id="79c93-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="79c93-125">في أدوات التأليف، لا يضطر مؤلفو الصفحة إلى معرفة أي الوحدات النمطية يمكن وضعها في كل فتحة مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="79c93-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="79c93-126">عند يحدد مؤلفو الصفحة فتحة ثم يحاولون تحديد وحدة نمطية لإضافتها إليها، فإنها تظهر طريقة عرض تمت تصفيتها لأنواع الوحدة النمطية التي يتم تدعيمها لتلك الفتحة.</span><span class="sxs-lookup"><span data-stu-id="79c93-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="79c93-127">وحدات المحتوى النمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-127">Content modules</span></span>

<span data-ttu-id="79c93-128">تحتوي وحدات المحتوى النمطية على عناصر وسائط ومحتوى، مثل النص (على سبيل المثال، العناوين الرئيسيةوالفقرات والارتباطات) أو مراجع الأصول (على سبيل المثال، صور وفيديو وملفات بتنسيق PDF).</span><span class="sxs-lookup"><span data-stu-id="79c93-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="79c93-129">ومن أمثلة أنواع وحدات المحتوى النمطية **جزء رئيسي**، و**ميزة**، و**شعار**.</span><span class="sxs-lookup"><span data-stu-id="79c93-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="79c93-130">يمكن أن تحتوي الوحدات النمطية الثلاثة هذه على نص أو وسائط، ولا تتطلب أية وحدات نمطية تابعة لجعل شيء ما مرئيًا على صفحة.</span><span class="sxs-lookup"><span data-stu-id="79c93-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="79c93-131">تتضمن معظم الصفحات النموذجية واليومية وأنشطة تأليف المحتوى وحدات محتوى نمطية، لأن هذه الوحدات النمطية تحدد بشكل أساسي المحتوى الفعلي الذي يتم عرضه في وحدات الحاوية النمطية الأصل.</span><span class="sxs-lookup"><span data-stu-id="79c93-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="79c93-132">تتوفر العديد من وحدات المحتوى النمطية، وعادة ما تكون هذه الوحدات النمطية هي الأجزاء الأخيرة التي ستضيفها إلى التسلسل الهرمي للصفحة في الوحدات النمطية المتداخلة.</span><span class="sxs-lookup"><span data-stu-id="79c93-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="79c93-133">يبين الرسم التوضيحي التالي كيفية تداخل الوحدات النمطية داخل فتحات الوحدة النمطية للحاوية الأصل.</span><span class="sxs-lookup"><span data-stu-id="79c93-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![تداخل الوحدات النمطية](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="79c93-135">إضافة الوحدات النمطية أو إزالتها</span><span class="sxs-lookup"><span data-stu-id="79c93-135">Add or remove modules</span></span>

<span data-ttu-id="79c93-136">تصف الإجراءات التالية كيفية إضافة الوحدات النمطية وإزالتها.</span><span class="sxs-lookup"><span data-stu-id="79c93-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="79c93-137">إضافة وحدة نمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-137">Add a module</span></span>

<span data-ttu-id="79c93-138">لإضافة وحدة نمطية إلى فتحة أو حاوية على صفحة، فاتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="79c93-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="79c93-139">في جزء المخطط التفصيلي الموجود على اليسار، حدد حاوية أو فتحة يمكن إضافة وحدة نمطية تابعة إليها.</span><span class="sxs-lookup"><span data-stu-id="79c93-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79c93-140">يقوم مصمم الوحدة النمطية بتحديد قائمة بأنواع الوحدات النمطية التي يمكن إضافتها إلى فتحة وحدة نمطية معينة.</span><span class="sxs-lookup"><span data-stu-id="79c93-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="79c93-141">يمكن لمؤلفي القوالب بعد ذلك تحسين خيارات الوحدة النمطية المسموح بها للمساعدة على ضمان تحسين محرك البحث المتناسق (SEO) وكفاءة التأليف لكافة الصفحات التي يتم إنشاؤها من قالب معين.</span><span class="sxs-lookup"><span data-stu-id="79c93-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="79c93-142">حدد زر علامة الحذف (**...**) للوحدة النمطية، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="79c93-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="79c93-143">يظهر مربع الحوار **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="79c93-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="79c93-144">تتم تصفية مربع الحوار هذا تلقائيًا بحيث يعرض الوحدات النمطية التي يتم دعمها في الحاوية أو الفتحة المحددة فقط.</span><span class="sxs-lookup"><span data-stu-id="79c93-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="79c93-145">يتم تحديد قائمة بالوحدات النمطية عن طريق تعريف قالب الصفحة أو الوحدة النمطية للحاوية.</span><span class="sxs-lookup"><span data-stu-id="79c93-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79c93-146">إذا كانت الحاوية أو الفتحة لا تدعم وحدات تابعة جديدة، فلن يكون خيار **إضافة وحدة نمطية** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="79c93-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="79c93-147">في مربع الحوار، ابحث عن وحدة نمطية وحددها لإضافتها إلى الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="79c93-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="79c93-148">تُعد **الميزة** و**جزء رئيسي** أنواعًا جيدة من الوحدات النمطية للمبتدئين للعمل بها.</span><span class="sxs-lookup"><span data-stu-id="79c93-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="79c93-149">حدد **موافق** لإضافة الوحدة النمطية المحددة للحاوية أو الفتحة المحددة على الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="79c93-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="79c93-150">إزالة وحدة نمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-150">Remove a module</span></span>

<span data-ttu-id="79c93-151">لإزالة وحدة نمطية من فتحة أو حاوية على صفحة، فاتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="79c93-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="79c93-152">في جزء المخطط التفصيلي الموجود على اليسار، حدد زر علامة الحذف المجاور لاسم الوحدة النمطية المراد إزالتها، ثم حدد زر سلة المهملات.</span><span class="sxs-lookup"><span data-stu-id="79c93-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="79c93-153">عند مطالبتك بتأكيد رغبتك في إزالة الوحدة النمطية، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="79c93-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="79c93-154">تكوين وحدات نمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-154">Configure modules</span></span>

<span data-ttu-id="79c93-155">تصف الإجراءات التالية كيفية تكوين الوحدات النمطية الخاصة بالمحتوى والحاوية.</span><span class="sxs-lookup"><span data-stu-id="79c93-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="79c93-156">تكوين وحدة محتوى نمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-156">Configure a content module</span></span>

<span data-ttu-id="79c93-157">لتكوين وحدة محتوى نمطية على صفحة ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="79c93-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="79c93-158">في جزء المخطط التفصيلي الموجود على اليسار، قم بتوسيع الشجرة وحدد أي وحدة محتوى (على سبيل المثال، **ميزة** أو **جزء رئيسي** أو **شعار**).</span><span class="sxs-lookup"><span data-stu-id="79c93-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="79c93-159">في جزء الخصائص الموجود علي اليسار ، ابحث عن عناصر تحكم محتويات وإعدادات الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="79c93-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="79c93-160">أدخل الخصائص لأي من عناصر تحكم الوحدة النمطية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="79c93-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="79c93-161">حدد **حفظ** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="79c93-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="79c93-162">كما سيؤدي ذلك إلى تحديث لوحه المعاينة.</span><span class="sxs-lookup"><span data-stu-id="79c93-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="79c93-163">تكوين وحدة حاوية نمطية</span><span class="sxs-lookup"><span data-stu-id="79c93-163">Configure a container module</span></span>

<span data-ttu-id="79c93-164">لتكوين وحدة حاوية نمطية على صفحة ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="79c93-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="79c93-165">حدد وحدة حاوية نمطية على الصفحة الخاصة بك (على سبيل المثال، وحدة نمطية دوارة أو بسيطة).</span><span class="sxs-lookup"><span data-stu-id="79c93-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="79c93-166">في جزء الخصائص الموجود على اليمين، قم بتوسيع عناصر التحكم المتداخلة عن طريق تحديد الرؤوس وتعيين أية قيم تحكم مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="79c93-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="79c93-167">في جزء المخطط التفصيلي الموجود على اليسار، حدد زر علامة الحذف المجاور لاسم إما الحاوية أو أيه فتحات داخل الحاوية، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="79c93-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="79c93-168">ثم قم بإضافة الوحدات النمطية التابعة إلى الحاوية المحددة.</span><span class="sxs-lookup"><span data-stu-id="79c93-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="79c93-169">لمزيد من المعلومات، راجع إجراء [التعامل مع الوحدات](#add-a-module) السابق في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="79c93-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="79c93-170">في حالة وجود وحدات نمطية تابعة متعددة كتابعات في الحاوية الأصل، فإنه يمكنك تغيير ترتيب العرض في الحاوية الأصل.</span><span class="sxs-lookup"><span data-stu-id="79c93-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="79c93-171">حدد زر علامة الحذف للوحدة النمطية، ثم استخدم الزرين السهم لأعلى ولأسفل.</span><span class="sxs-lookup"><span data-stu-id="79c93-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79c93-172">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="79c93-172">Additional resources</span></span>

[<span data-ttu-id="79c93-173">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="79c93-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="79c93-174">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="79c93-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="79c93-175">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="79c93-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="79c93-176">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="79c93-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="79c93-177">إضافة وحدة حاوية إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="79c93-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="79c93-178">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="79c93-178">Work with publish groups</span></span>](publish-groups.md)

