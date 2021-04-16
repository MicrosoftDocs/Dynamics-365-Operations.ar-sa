---
title: العمل مع مجموعات النشر
description: يصف هذا الموضوع ميزة مجموعات النشر في Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 15ac04721e440dcd7c0f8984c14e86aa0f68963e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792305"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="94315-103">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="94315-103">Work with publish groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94315-104">يصف هذا الموضوع ميزة مجموعات النشر في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="94315-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="94315-105">يتم تحديث مواقع التجارة الإلكترونية باستمرار بمحتوي جديد على مدار العام.</span><span class="sxs-lookup"><span data-stu-id="94315-105">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="94315-106">وغالبًا ما يتم نشر التحديثات على دفعات حول أحداث التجارة الإلكترونية المزدحمة مثل العطلات أو حملات التسويق الموسمية أو عمليات الإطلاق الترويجية.</span><span class="sxs-lookup"><span data-stu-id="94315-106">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="94315-107">تتطلب هذه التحديثات غالبًا أن يتم تجهيز مجموعات محتوى موقع الويب (للأمثلة والصفحات والصور والأجزاء والقوالب) والتحقق من صحتها ونشرها بشكل متزامن في إجراء واحد.</span><span class="sxs-lookup"><span data-stu-id="94315-107">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="94315-108">توفر القدرة على تجميع الأصناف في المجموعات المنطقية التي تقوم بنشر الأصناف معًا، حيث تحتوي كل مجموعة على دورة الحياة الخاصة بها، وتوفر العديد من المزايا لمؤلفي الموقع.</span><span class="sxs-lookup"><span data-stu-id="94315-108">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="94315-109">في Commerce، تُعرف هذه المجموعات المنطقية باسم مجموعات النشر.</span><span class="sxs-lookup"><span data-stu-id="94315-109">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="94315-110">إنها تسمح لمؤلفي الموقع بتعقب مجموعات من التحديثات على أنها كيانات قابلة للتكوين وقابلة للاختبار وقابلة للنشر.</span><span class="sxs-lookup"><span data-stu-id="94315-110">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="94315-111">يمكن للمؤلفين معاينة التحديثات في مجموعة نشر مجمعة دون التأثير على موقع العرض المباشر أو مجموعات النشر المكتملة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="94315-111">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="94315-112">يمكن للمؤلفين بعد ذلك جدولة إجراء النشر لنشر كافة الأصناف الموجودة في مجموعة النشر في الوقت نفسه في موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="94315-112">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="94315-113">تُعد القدرة على تجميع التحديثات ومعاينتها وجدولتها للنشر مهمة للعديد من الشركات على مستوى المؤسسة التي تعمل على وضع إيرادات سنوية كبيرة عن المراحل الرئيسية لتحديث الموقع المستندة إلى الحدث.</span><span class="sxs-lookup"><span data-stu-id="94315-113">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="94315-114">يمكن للشركات تكبد تكاليف من لعمليات نشر المحتوى البطيء أو الذي تم إبطاله والتي لا تسير بسلاسة.</span><span class="sxs-lookup"><span data-stu-id="94315-114">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="94315-115">تساعد مجموعات النشر على ضمان أنه يتم تنظيم عمليات الإطلاق والتحقق من صحتها ونشرها في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="94315-115">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="94315-116">سواء كانت كبيرة أو صغيرة، تقدم مجموعات النشر توفر مجموعة أدوات قيمة تساعد المؤلفين على تنظيم وتبسيط مهام تحديث الموقع الجارية.</span><span class="sxs-lookup"><span data-stu-id="94315-116">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="94315-117">متى يتم استخدام مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="94315-117">When to use publish groups</span></span>

<span data-ttu-id="94315-118">يمكنك استخدام مجموعات النشر كلما كان يجب عليك تقسيم المستندات المتعددة ونشرها معًا.</span><span class="sxs-lookup"><span data-stu-id="94315-118">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="94315-119">على سبيل المثال، إذا كان موقع الويب الخاص بك يقوم بتحديث المحتوى كل موسم، فإنه يمكنك إنشاء مجموعات نشر لهذه الحركات التسويقية الموسمية.</span><span class="sxs-lookup"><span data-stu-id="94315-119">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="94315-120">قد تحتوي مجموعة نشر "التحديث الموسمي لفصل الخريف" على صور موسمية جديدة، وأجزاء تحتوى على رسائل تسويقية موسمية، وصفحات تشمل مجموعات المنتجات الموسمية، أو تحديثات موسمية أخرى لمواقع الويب.</span><span class="sxs-lookup"><span data-stu-id="94315-120">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="94315-121">تكمن ميزة مجموعات النشر في أنه يمكنك إظهار تحديثات متعددة في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="94315-121">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="94315-122">على سبيل المثال، بعد وقت قصير من التحديث لمجموعه نشر "التحديث الموسمي لفصل الخريف"، قد يكون هناك تحديث محتوى لعطلة نهاية أسبوع معينة.</span><span class="sxs-lookup"><span data-stu-id="94315-122">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="94315-123">في هذه الحالة، يمكنك إظهار محتوى لمجموعة نشر "التحديث الموسمي السنوي" في الوقت نفسه الذي تقوم فيه بعرض محتوى لمجموعة نشر "تحديث العطلات في فصل الخريف" اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="94315-123">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="94315-124">تحتوي كل مجموعة نشر على مجموعة فريدة خاصة بها من الصفحات والصور والأجزاء والقوالب وهكذا.</span><span class="sxs-lookup"><span data-stu-id="94315-124">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="94315-125">يمكنك عرض مجموعتي النشر هذه ومعاينتها والتحقق من صحتها بشكل مستقل ولكن على مخطط زمني متزامن.</span><span class="sxs-lookup"><span data-stu-id="94315-125">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="94315-126">ويمكن بعد ذلك جدولة كل مجموعة نشر للانتقال إلى العرض المباشر لموقعك في تواريخ وأوقات محددة.</span><span class="sxs-lookup"><span data-stu-id="94315-126">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="94315-127">تشغيل ميزة مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="94315-127">Turn on the publish groups feature</span></span>

<span data-ttu-id="94315-128">تُعد ميزة مجموعات النشر اختيارية ويجب تشغيلها لموقعك.</span><span class="sxs-lookup"><span data-stu-id="94315-128">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="94315-129">لتشغيل ميزة مجموعات النشر لموقعك في أدوات تأليف Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="94315-129">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="94315-130">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="94315-130">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="94315-131">ضمن **إعدادات الموقع**، حدد **الميزات**.</span><span class="sxs-lookup"><span data-stu-id="94315-131">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="94315-132">قم بتعيين خيار **مجموعات النشر** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="94315-132">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="94315-133">إنشاء مجموعة نشر</span><span class="sxs-lookup"><span data-stu-id="94315-133">Create a publish group</span></span>

<span data-ttu-id="94315-134">لإنشاء مجموعة نشرلموقعك في أدوات تأليف Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="94315-134">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="94315-135">في جزء التنقل على اليسار، حدد **مجموعات النشر**.</span><span class="sxs-lookup"><span data-stu-id="94315-135">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="94315-136">في شريط الأوامر العلوي، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="94315-136">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="94315-137">في مربع الحوار **إنشاء مجموعة نشر**، ضمن **اسم مجموعة النشر**، أدخل اسمًا وصفيًا.</span><span class="sxs-lookup"><span data-stu-id="94315-137">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="94315-138">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94315-138">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="94315-139">تعيين سياق تأليف مجموعة النشر</span><span class="sxs-lookup"><span data-stu-id="94315-139">Set the publish group authoring context</span></span>

<span data-ttu-id="94315-140">في Commerce، يكون سياق التأليف الافتراضي هو سياق موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="94315-140">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="94315-141">يكون سياق تأليف موقع العرض المباشر هو طريقة العرض الافتراضية حيث يمكنك العرض والقيام بالتغييرات مباشرة على موقع الويب الخاص بك دون استخدام جروب نشر.</span><span class="sxs-lookup"><span data-stu-id="94315-141">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="94315-142">وإنه يمثل أحدث التحديثات المباشرة للإصدار المنشور لموقعك.</span><span class="sxs-lookup"><span data-stu-id="94315-142">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="94315-143">إذا كان عنصر تحكم السياق ضمن **مجموعات النشر** في جزء التنقل الأيسر يعرض اسم **موقع العرض المباشر**، فإنك تعمل في سياق تأليف موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="94315-143">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="94315-144">إن **موقع العرض المباشر** هو الاسم الافتراضي لعنصر تحكم السياق.</span><span class="sxs-lookup"><span data-stu-id="94315-144">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="94315-145">وإلا، يعرض عنصر تحكم السياق اسم مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="94315-145">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="94315-146">للعمل في مجموعة نشر، فإنه يجب عليك التبديل إلى سياق تأليف مجموعة النشر له.</span><span class="sxs-lookup"><span data-stu-id="94315-146">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="94315-147">لتعيين سياق مجموعة النشر، اتبع إحدى الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="94315-147">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="94315-148">في جزء التنقل الأيسر، حدد عنصر تحكم السياق مباشرة ضمن **مجموعات النشر**، ثم حدد اسم مجموعة النشر في قائمة الخيارات التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="94315-148">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="94315-149">تتم إعادة تسمية عنصر تحكم السياق ويعرض مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="94315-149">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="94315-150">في جزء التنقل الأيسر، حدد **مجموعات النشر**، ثم ضمن **مجموعات النشر**، حدد اسم مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="94315-150">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="94315-151">تتم إعادة تسمية عنصر تحكم السياق ويعرض مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="94315-151">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="94315-152">بعد تعيين سياق تأليف مجموعة النشر، فإنك تعمل في سياق مجموعة النشر عند تقوم بمعاينة محتوى الموقع وتحريره.</span><span class="sxs-lookup"><span data-stu-id="94315-152">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="94315-153">للرجوع إلى سياق تأليف موقع العرض المباشر الافتراضي، حدد عنصر تحكم السياق، ثم حدد **موقع العرض المباشر**.</span><span class="sxs-lookup"><span data-stu-id="94315-153">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="94315-154">إضافة صفحات أو أصناف أخرى إلى مجموعة نشر</span><span class="sxs-lookup"><span data-stu-id="94315-154">Add pages or other items to a publish group</span></span>

<span data-ttu-id="94315-155">بعد أن تقوم بتحديد سياق تأليف مجموعة نشر، ويعرض عنصر تحكم السياق في جزء التنقل الأيسر اسمه، فإنه يمكنك إنشاء محتوى تمامًا كما تفعل في سياق موقع العرض المباشر الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="94315-155">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="94315-156">يمكنك أيضًا إضافة الصفحات الموجودة أو الأصناف الأخرى من مجموعات النشر الأخرى، أو من سياق موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="94315-156">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="94315-157">لنسخ الصفحات الموجودة إلى مجموعة نشر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="94315-157">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="94315-158">حدد سياق التأليف المراد النسخ منه، ثم في جزء التنقل الأيسر، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="94315-158">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="94315-159">حدد الصفحة التي تريد إضافتها إلى مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="94315-159">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="94315-160">في شريط الأوامر، حدد **نسخ إلى مجموعة النشر**.</span><span class="sxs-lookup"><span data-stu-id="94315-160">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="94315-161">في مربع الحوار **تحديد مجموعة نشر**، حدد مجموعة النشر المراد إضافة الصفحة إليها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94315-161">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="94315-162">يمكنك استخدام الخطوات الأساسية نفسها لإنشاء صفحات المنتج المخصصة وعناوين Url والقوالب والتخطيطات والأجزاء وأصول المكتبة الوسائط ، أو لإضافة أصناف موجودة من هذه الأنواع إلى مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="94315-162">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="94315-163">التحقق من صحة مجموعة نشر</span><span class="sxs-lookup"><span data-stu-id="94315-163">Validate a publish group</span></span>

<span data-ttu-id="94315-164">للتأكد من أن كافة التبعيات في محتوى مجموعة النشر مستوفاه، ومن أنه يتم النجاح في كافة عمليات التحقق من الصحة، فإنه يمكنك التحقق للتعرف على أية مشكلات يجب معالجتها قبل جدولة إجراء نشر.</span><span class="sxs-lookup"><span data-stu-id="94315-164">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="94315-165">للتحقق من صحة مجموعة النشر الخاصة بك قبل أن تقوم بجدولتها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="94315-165">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="94315-166">في جزء التنقل على اليسار، حدد **مجموعات النشر**.</span><span class="sxs-lookup"><span data-stu-id="94315-166">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="94315-167">حدد مجموعة النشر للتحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="94315-167">Select the publish group to validate.</span></span>
1. <span data-ttu-id="94315-168">في شريط الأوامر العلوي، حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="94315-168">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="94315-169">يتم تشغيل التحقق من الصحة على كل المحتوى الموجود في مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="94315-169">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="94315-170">سيتم عرض أية مشكلات ستمنع إجراء نشر ناجح في مربع الإخطار الذي يظهر في الجزء العلوي الأيمن.</span><span class="sxs-lookup"><span data-stu-id="94315-170">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="94315-171">يتم دائمًا تشغيل التحقق من الصحة تلقائيًا عند جدولة مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="94315-171">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="94315-172">ومع ذلك، يكون الزر **التحقق من الصحة** الموجود في شريط الأوامر مفيدًا لأنه يساعد في تحديد المشكلات التي يجب إصلاحها قبل محاولة جدولة مجموعة نشر للعرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="94315-172">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="94315-173">جدولة مجموعة نشر للعرض المباشر</span><span class="sxs-lookup"><span data-stu-id="94315-173">Schedule a publish group to go live</span></span>

<span data-ttu-id="94315-174">لجدولة مجموعة نشر للعرض المباشر في موقعك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="94315-174">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="94315-175">في جزء التنقل على اليسار، حدد **مجموعات النشر**.</span><span class="sxs-lookup"><span data-stu-id="94315-175">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="94315-176">ضمن **مجموعات النشر**، حدد مجموعة النشر المراد جدولتها.</span><span class="sxs-lookup"><span data-stu-id="94315-176">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="94315-177">في شريط الأوامر العلوي، حدد **تحرير الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="94315-177">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="94315-178">يظهر مربع الحوار **تحرير الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="94315-178">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="94315-179">حدد التاريخ والوقت الذي يجب أن يتم فيه عرض مجموعة النشر عرضًا مباشرًا، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94315-179">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="94315-180">لإلغاء جدولة مجموعة نشر، اتبع الخطوات نفسها، ولكن حدد **إلغاء جدولة مجموعة نشر** في مربع الحوار **تحرير جدول**.</span><span class="sxs-lookup"><span data-stu-id="94315-180">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="94315-181">قد تستغرق مجموعات النشر الكبيرة للغاية مدة تصل إلى دقيقة أو دقيقتين ليتم نشرها عند وصول الوقت المجدول.</span><span class="sxs-lookup"><span data-stu-id="94315-181">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="94315-182">تأكد من ألا يكون إجراء النشر فوريًا، وأنه سيتم نشر مجموعات نشر أصغر بشكل أسرع.</span><span class="sxs-lookup"><span data-stu-id="94315-182">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="94315-183">الأسئلة المتداولة عن مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="94315-183">Publish groups FAQ</span></span>

<span data-ttu-id="94315-184">**كم عدد الأصناف التي يمكن أن تكون موجودة في مجموعة نشر ؟**</span><span class="sxs-lookup"><span data-stu-id="94315-184">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="94315-185">حاليًا، هناك حد 2,000 من الأصناف لكل مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="94315-185">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="94315-186">لاحظ أن مجموعات النشر الكبيرة للغاية قد تستغرق عدة دقائق ليتم نشرها عند وصول الوقت المجدول.</span><span class="sxs-lookup"><span data-stu-id="94315-186">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="94315-187">**هل مجموعات النشر مثل كود "فروع" في مصطلحات تطوير البرامج ؟**</span><span class="sxs-lookup"><span data-stu-id="94315-187">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="94315-188">نعم ولا.</span><span class="sxs-lookup"><span data-stu-id="94315-188">Yes and no.</span></span> <span data-ttu-id="94315-189">يمكن اعتبار مجموعات النشر من الإصدارات المتشعبة لموقعك.</span><span class="sxs-lookup"><span data-stu-id="94315-189">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="94315-190">وبهذه الطريقة، فإنها تتصرف مثل الفروع.</span><span class="sxs-lookup"><span data-stu-id="94315-190">In that way, they do act like branches.</span></span> <span data-ttu-id="94315-191">ومع ذلك، لا يوجد مفهوم دمج على مستوى الأصناف الفردية.</span><span class="sxs-lookup"><span data-stu-id="94315-191">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="94315-192">يتم استبدال الصنف الذي يتم نشره أخيرًا بالصنف الذي كان موجودًا مسبقًا، ودائمًا ما يحل إجراء النشر الأحدث محل إجراءات النشر السابقة.</span><span class="sxs-lookup"><span data-stu-id="94315-192">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="94315-193">**هل يمكنني جدوله مجموعتي نشر للعرض المباشر في نفس الوقت ؟**</span><span class="sxs-lookup"><span data-stu-id="94315-193">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="94315-194">الرقم</span><span class="sxs-lookup"><span data-stu-id="94315-194">No.</span></span> <span data-ttu-id="94315-195">لأسباب تتعلق بالأداء والتعارض، سيجبرك النظام على تنظيم مجموعات نشر مجدولة لمدة خمس دقائق على الأقل.</span><span class="sxs-lookup"><span data-stu-id="94315-195">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="94315-196">**هل يمكنني استخدام مجموعات نشر لجدولة أصناف مكتب الدعم متعدد الاتجاهات، مثل الخصومات وتحديثات المنتج ؟**</span><span class="sxs-lookup"><span data-stu-id="94315-196">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="94315-197">حاليًا، تدعم ميزة مجموعات النشر محتوى موقع ويب فقط.</span><span class="sxs-lookup"><span data-stu-id="94315-197">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="94315-198">ومع ذلك، تدرك Microsoft أن التكامل مع سيناريوهات الترويج لمكاتب الدعم يمكن أن يكون مفيدًا للتنسيق والأتمتة بعمليات إطلاق حملة متعددة الاتجاهات.</span><span class="sxs-lookup"><span data-stu-id="94315-198">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94315-199">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="94315-199">Additional resources</span></span>

[<span data-ttu-id="94315-200">طرق إضافة المحتوى</span><span class="sxs-lookup"><span data-stu-id="94315-200">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="94315-201">مصطلحات نموذج الصفحة</span><span class="sxs-lookup"><span data-stu-id="94315-201">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="94315-202">حالات المستند ودورة الحياة</span><span class="sxs-lookup"><span data-stu-id="94315-202">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="94315-203">تمكين المشاركة عبر القنوات واستخدامها</span><span class="sxs-lookup"><span data-stu-id="94315-203">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="94315-204">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="94315-204">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="94315-205">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="94315-205">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="94315-206">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="94315-206">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="94315-207">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="94315-207">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
