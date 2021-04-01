---
title: العمل باستخدام الوحدات النمطية
description: يوضح هذا الموضوع كيفية استخدام الوحدات النمطية ووقت استخدامها في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210889"
---
# <a name="work-with-modules"></a><span data-ttu-id="2f1e3-103">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f1e3-104">يوضح هذا الموضوع كيفية استخدام الوحدات النمطية ووقت استخدامها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2f1e3-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2f1e3-105">Overview</span></span>

<span data-ttu-id="2f1e3-106">تُعد الوحدات النمطية كتل إنشاء منطقية تتكون منها بنية الصفحة الخاصة بك، ويكون لها أغراض ونطاقات متعددة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="2f1e3-107">وتُعد بعض الوحدات النمطية حاويات عالية المستوى، والغرض الوحيد منها هو استيعاب وتنظيم الوحدات النمطية الأخرى (الوحدات النمطية التابعة).</span><span class="sxs-lookup"><span data-stu-id="2f1e3-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="2f1e3-108">ويكون للوحدات النمطية الأخرى، مثل الوحدة النمطية البسيطة لوضع صورة، غرض محدد جدًا.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="2f1e3-109">وتقع الوحدات النمطية الأخرى، مثل الوحدة النمطية الدوارة، في مكان ما بين هاتين الفئتين.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="2f1e3-110">بشكل افتراضي، يتضمن موقع Dynamics 365 Commerce مكتبة وحدات نمطية تسمح لك بتحقيق معظم سيناريوهات التجارة الإلكترونية الأساسية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="2f1e3-111">يجب أن تكون قادرًا على إنشاء موقع تجارة إلكترونية شامل فقط باستخدام هذه الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="2f1e3-112">ومع ذلك، قد تحتاج أيضًا إلى تخصيص هذه الوحدات النمطية أو إنشاء وحدات نمطية مخصصة وجديدة لاحتياجات محددة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="2f1e3-113">إذا كنت ترغب في إنشاء وحدات نمطية مخصصة، تتوفر مجموعة تطوير برامج تصميم الوحدة النمطية (SDK) لمساعدتك في إنشاء مكتبة وحدة نمطية مخصصة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="2f1e3-114">وحدات الحاوية النمطية والفتحات</span><span class="sxs-lookup"><span data-stu-id="2f1e3-114">Container modules and slots</span></span>

<span data-ttu-id="2f1e3-115">كما ذكر سابقًا، يتم تصميم بعض الوحدات النمطية للاحتفاظ بالوحدات النمطية التابعة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="2f1e3-116">تُعرف هذه الوحدات باسم *الحاويات*، وتسمح بالتسلسلات الهرمية للوحدات النمطية المتداخلة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="2f1e3-117">تتضمن وحدات الحاوية النمطية *الفتحات*.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-117">Container modules include *slots*.</span></span> <span data-ttu-id="2f1e3-118">تُستخدم الفتحات لمعالجة التخطيط والغرض من الوحدات النمطية التابعة في الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="2f1e3-119">وكمثال على الوحدة النمطية لحاوية الصفحة الأساسية (وحدة نمطية ذات مستوى أعلى لأي صفحة) التي تحدد عدة فتحات مهمة:</span><span class="sxs-lookup"><span data-stu-id="2f1e3-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="2f1e3-120">فتحة رأس</span><span class="sxs-lookup"><span data-stu-id="2f1e3-120">A header slot</span></span>
- <span data-ttu-id="2f1e3-121">فتحة رأس فرعي</span><span class="sxs-lookup"><span data-stu-id="2f1e3-121">A sub-header slot</span></span>
- <span data-ttu-id="2f1e3-122">فتحة رئيسية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-122">A main slot</span></span>
- <span data-ttu-id="2f1e3-123">فتحة تذييل</span><span class="sxs-lookup"><span data-stu-id="2f1e3-123">A footer slot</span></span>
- <span data-ttu-id="2f1e3-124">فتحة تذييل فرعي</span><span class="sxs-lookup"><span data-stu-id="2f1e3-124">A sub-footer slot</span></span>

<span data-ttu-id="2f1e3-125">يقوم مطور الوحدة النمطية بتحديد هذه الفتحات وتحديد الوحدات النمطية التابعة وعدد الوحدات النمطية التابعة التي يمكن وضعها مباشره داخلها.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="2f1e3-126">على سبيل المثال، قد تدعم فتحة الرأس وحدة نمطية واحدة فقط لنوع **الوحدة النمطية للرأس**، بينما قد تدعم فتحة النص الأصلي عدد غير محدود من الوحدات النمطية من أي نوع (باستثناء الوحدات النمطية الأخرى لحاويات الصفحة).</span><span class="sxs-lookup"><span data-stu-id="2f1e3-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="2f1e3-127">في أدوات التأليف، لا يضطر مؤلفو الصفحة إلى معرفة أي الوحدات النمطية يمكن وضعها في كل فتحة مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="2f1e3-128">عند يحدد مؤلفو الصفحة فتحة ثم يحاولون تحديد وحدة نمطية لإضافتها إليها، فإنها تظهر طريقة عرض تمت تصفيتها لأنواع الوحدة النمطية التي يتم تدعيمها لتلك الفتحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="2f1e3-129">وحدات المحتوى النمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-129">Content modules</span></span>

<span data-ttu-id="2f1e3-130">تحتوي وحدات المحتوى النمطية على عناصر وسائط ومحتوى، مثل النص (على سبيل المثال، العناوين الرئيسيةوالفقرات والارتباطات) أو مراجع الأصول (على سبيل المثال، صور وفيديو وملفات بتنسيق PDF).</span><span class="sxs-lookup"><span data-stu-id="2f1e3-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="2f1e3-131">تتضمن أنواع وحدات المحتوى النموذجية وحدات كتلة المحتوى وكتلة النص والشعار الترويجي‬.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="2f1e3-132">يمكن أن تحتوي الوحدات النمطية الثلاثة هذه على نص أو وسائط، ولا تتطلب أية وحدات نمطية تابعة لجعل شيء ما مرئيًا على صفحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="2f1e3-133">تتضمن معظم الصفحات النموذجية واليومية وأنشطة تأليف المحتوى وحدات محتوى نمطية، لأن هذه الوحدات النمطية تحدد بشكل أساسي المحتوى الفعلي الذي يتم عرضه في وحدات الحاوية النمطية الأصل.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="2f1e3-134">تتوفر العديد من وحدات المحتوى النمطية، وعادة ما تكون هذه الوحدات النمطية هي الأجزاء الأخيرة التي ستضيفها إلى التسلسل الهرمي للصفحة في الوحدات النمطية المتداخلة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="2f1e3-135">يبين الرسم التوضيحي التالي كيفية تداخل الوحدات النمطية داخل فتحات الوحدة النمطية للحاوية الأصل.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![تداخل الوحدات النمطية](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="2f1e3-137">إضافة الوحدات النمطية أو إزالتها</span><span class="sxs-lookup"><span data-stu-id="2f1e3-137">Add or remove modules</span></span>

<span data-ttu-id="2f1e3-138">تصف الإجراءات التالية كيفية إضافة الوحدات النمطية وإزالتها.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="2f1e3-139">إضافة وحدة نمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-139">Add a module</span></span>

<span data-ttu-id="2f1e3-140">لإضافة وحدة نمطية إلى فتحة أو حاوية على صفحة، فاتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-141">في جزء المخطط التفصيلي إلى اليمين أو مباشرةً في اللوحة الرئيسية، حدد حاوية أو فتحة يمكن إضافة وحدة نمطية تابعة إليها.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f1e3-142">يقوم مصمم الوحدة النمطية بتحديد قائمة بأنواع الوحدات النمطية التي يمكن إضافتها إلى فتحة وحدة نمطية معينة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="2f1e3-143">يمكن لمؤلفي القوالب بعد ذلك تحسين خيارات الوحدة النمطية المسموح بها للمساعدة على ضمان تحسين محرك البحث المتناسق (SEO) وكفاءة التأليف لكافة الصفحات التي يتم إنشاؤها من قالب معين.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="2f1e3-144">عند إضافة وحدة نمطية إلى فتحة، تتم تصفية مربع الحوار **إضافة وحدة نمطية** تلقائيًا بحيث يعرض الوحدات النمطية التي يتم دعمها في الحاوية أو الفتحة المحددة فقط.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="2f1e3-145">تتحدد قائمة الوحدات النمطية المسموح بها من خلال تعريف قالب الصفحة أو الوحدة النمطية للحاوية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="2f1e3-146">إذا كنت تستخدم جزء المخطط التفصيلي، فحدد علامة القطع (**...**) إلى جانب اسم الوحدة، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="2f1e3-147">إذا كنت تستخدم عناصر التحكم مباشرة داخل اللوحة، فحدد رمز علامة الجمع ( **+**) في فتحة فارغة أو مجاورة للوحدة المحددة حاليًا، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f1e3-148">إذا كانت الحاوية أو الفتحة لا تدعم وحدات تابعة جديدة، فلن يكون خيار **إضافة وحدة نمطية** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="2f1e3-149">في مربع الحوار **إضافة وحدة نمطية**، حدد وحدة نمطية لإضافتها إلى صفحتك.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="2f1e3-150">**كتلة المحتوى** هي نوع وحدة جيد للمبتدئين لاستخدامها.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="2f1e3-151">حدد **موافق** لإضافة الوحدة النمطية المحددة للحاوية أو الفتحة المحددة على الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="2f1e3-152">إزالة وحدة نمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-152">Remove a module</span></span>

<span data-ttu-id="2f1e3-153">لإزالة وحدة نمطية من فتحة أو حاوية على صفحة، فاتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-154">في جزء المخطط التفصيلي إلى اليمين، حدد علامة القطع (**...**) إلى جانب اسم الوحدة النمطية المراد إزالتها، ثم حدد رمز سلة المهملات.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="2f1e3-155">بدلاً من ذلك، يمكنك تحديد رمز سلة المهملات في اللوحة على شريط أدوات وحدة نمطية محددة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="2f1e3-156">عند مطالبتك بتأكيد رغبتك في إزالة الوحدة النمطية، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="2f1e3-157">نقل وحدة نمطية إلى موضع جديد</span><span class="sxs-lookup"><span data-stu-id="2f1e3-157">Move a module to a new position</span></span>

<span data-ttu-id="2f1e3-158">لنقل وحدة نمطية إلى موضع جديد في صفحتك، استخدم أي واحدة من الطرق التالية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="2f1e3-159">نقل وحدة نمطية باستخدام جزء المخطط التفصيلي</span><span class="sxs-lookup"><span data-stu-id="2f1e3-159">Move a module using the outline pane</span></span>

<span data-ttu-id="2f1e3-160">لنقل وحدة نمطية باستخدام جزء المخطط التفصيلي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-161">حدد واستمر في الضغط على الوحدة النمطية التي تريد نقلها في جزء المخطط التفصيلي، ثم اسحب الوحدة النمطية إلى موضع جديد في المخطط التفصيلي.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="2f1e3-162">يشير الخط الأزرق في المخطط التفصيلي وعلى اللوحة إلى المكان الذي يمكن وضع الوحدة النمطية فيه.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="2f1e3-163">حرر الوحدة النمطية لإسقاطها في الموضع الجديد.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="2f1e3-164">نقل وحدة نمطية مباشرة داخل اللوحة</span><span class="sxs-lookup"><span data-stu-id="2f1e3-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="2f1e3-165">لنقل وحدة نمطية مباشرة داخل اللوحة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-166">حدد الوحدة النمطية التي ترغب في نقلها في اللوحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="2f1e3-167">حدد رمز سهم يشير إلى الأعلى أو إلى الأسفل في شريط أدوات الوحدة النمطية، ثم اسحب السهم إلى موضع جديد على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="2f1e3-168">يشير الخط الأزرق في المخطط التفصيلي وعلى اللوحة إلى المكان الذي يمكن وضع الوحدة النمطية فيه.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="2f1e3-169">إذا تعذر نقل وحدة نمطية إلى الأعلى أو إلى الأسفل، سيكون رمز السهم رماديًا.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="2f1e3-170">حرر الوحدة النمطية لإسقاطها في الموضع الجديد.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="2f1e3-171">نقل وحدة نمطية باستخدام قائمة علامة القطع</span><span class="sxs-lookup"><span data-stu-id="2f1e3-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="2f1e3-172">لنقل وحدة نمطية باستخدام قائمة علامة القطع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-173">حدد وحدة نمطية في المخطط التفصيلي أو اللوحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="2f1e3-174">حدد علامة القطع (**...**) إلى جانب اسم الوحدة في جزء المخطط التفصيلي، أو في شريط أدوات الوحدة النمطية في اللوحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="2f1e3-175">إذا كان من الممكن نقل الوحدة النمطية لأعلى أو لأسفل داخل الحاوية أو الفتحة، فسترى خيارات **تحريك لأعلى** أو **تحريك لأسفل**.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="2f1e3-176">حدد خيار التحريك المطلوب لنقل الوحدة النمطية لأعلى أو لأسفل بالنسبة إلى مثيلاتها.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="2f1e3-177">تكوين وحدات نمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-177">Configure modules</span></span>

<span data-ttu-id="2f1e3-178">تصف الإجراءات التالية كيفية تكوين الوحدات النمطية الخاصة بالمحتوى والحاوية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="2f1e3-179">تكوين وحدة محتوى نمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-179">Configure a content module</span></span>

<span data-ttu-id="2f1e3-180">لتكوين وحدة محتوى نمطية على صفحة ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-181">في جزء المخطط التفصيلي إلى اليمين، قم بتوسيع الشجرة وحدد أي وحدة محتوى (على سبيل المثال، **كتلة المحتوى**).</span><span class="sxs-lookup"><span data-stu-id="2f1e3-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="2f1e3-182">أو، يمكنك تحديد الوحدة النمطية في اللوحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="2f1e3-183">في جزء خصائص الوحدة النمطية إلى اليمين، أدخل الخصائص لأي من عناصر تحكم الوحدة النمطية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="2f1e3-184">حدد **حفظ** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="2f1e3-185">كما سيؤدي ذلك إلى تحديث لوحه المعاينة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="2f1e3-186">تحرير خصائص نص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-186">Edit module text properties</span></span>

<span data-ttu-id="2f1e3-187">يمكن تحرير خصائص نص الوحدة النمطية التي ليست للقراءة فقط مباشرةً في اللوحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="2f1e3-188">لتحرير خصائص نص الوحدة النمطية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-189">حدد عنصر تحكم النص في اللوحة، ثم ضع المؤشر في المكان الذي تريد تحرير النص فيه.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="2f1e3-190">أدخل محتوى النص.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-190">Enter your text content.</span></span>
1. <span data-ttu-id="2f1e3-191">حدد أي مكان خارج محتوى النص لمتابعة تحرير المحتوى الآخر.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="2f1e3-192">تحديد صورة مضمنة</span><span class="sxs-lookup"><span data-stu-id="2f1e3-192">Inline image selection</span></span>

<span data-ttu-id="2f1e3-193">يمكن تغيير صور الوحدة النمطية التي ليست للقراءة فقط مباشرةً من اللوحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="2f1e3-194">لاختيار صورة جديدة لوحدة نمطية للمحتوى،، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-195">في اللوحة، انقر نقرًا مزدوجًا فوق الصورة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="2f1e3-196">سيؤدي ذلك إلى إظهار نافذة منتقي الوسائط.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="2f1e3-197">ابحث عن صورة جديدة تريد استخدامها وحددها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="2f1e3-198">يتم الآن عرض الصورة الجديدة في اللوحة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="2f1e3-199">تكوين وحدة حاوية نمطية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-199">Configure a container module</span></span>

<span data-ttu-id="2f1e3-200">لتكوين وحدة حاوية نمطية على صفحة ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="2f1e3-201">حدد وحدة حاوية نمطية على الصفحة الخاصة بك (على سبيل المثال، وحدة نمطية دوارة أو بسيطة).</span><span class="sxs-lookup"><span data-stu-id="2f1e3-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="2f1e3-202">في جزء الخصائص الموجود على اليمين، قم بتوسيع عناصر التحكم المتداخلة عن طريق تحديد الرؤوس وتعيين أية قيم تحكم مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="2f1e3-203">في جزء المخطط التفصيلي الموجود على اليسار، حدد زر علامة الحذف المجاور لاسم إما الحاوية أو أيه فتحات داخل الحاوية، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="2f1e3-204">ثم قم بإضافة الوحدات النمطية التابعة إلى الحاوية المحددة.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="2f1e3-205">لمزيد من المعلومات، راجع إجراء [التعامل مع الوحدات](#add-a-module) السابق في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="2f1e3-206">في حالة وجود وحدات نمطية تابعة متعددة كتابعات في الحاوية الأصل، فإنه يمكنك تغيير ترتيب العرض في الحاوية الأصل.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="2f1e3-207">حدد زر علامة الحذف للوحدة النمطية، ثم استخدم الزرين السهم لأعلى ولأسفل.</span><span class="sxs-lookup"><span data-stu-id="2f1e3-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f1e3-208">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2f1e3-208">Additional resources</span></span>

[<span data-ttu-id="2f1e3-209">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="2f1e3-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2f1e3-210">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="2f1e3-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="2f1e3-211">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="2f1e3-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="2f1e3-212">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="2f1e3-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2f1e3-213">إضافة وحدة حاوية إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="2f1e3-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="2f1e3-214">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="2f1e3-214">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]