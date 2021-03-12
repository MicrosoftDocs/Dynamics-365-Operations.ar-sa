---
title: العمل مع مجموعات النشر
description: يصف هذا الموضوع ميزة مجموعات النشر في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0a4f19af0cdf9c72add0ec18be84e36c807af9ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969866"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="18c75-103">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="18c75-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="18c75-104">يصف هذا الموضوع ميزة مجموعات النشر في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18c75-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="18c75-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="18c75-105">Overview</span></span>

<span data-ttu-id="18c75-106">يتم تحديث مواقع التجارة الإلكترونية باستمرار بمحتوي جديد على مدار العام.</span><span class="sxs-lookup"><span data-stu-id="18c75-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="18c75-107">وغالبًا ما يتم نشر التحديثات على دفعات حول أحداث التجارة الإلكترونية المزدحمة مثل العطلات أو حملات التسويق الموسمية أو عمليات الإطلاق الترويجية.</span><span class="sxs-lookup"><span data-stu-id="18c75-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="18c75-108">تتطلب هذه التحديثات غالبًا أن يتم تجهيز مجموعات محتوى موقع الويب (للأمثلة والصفحات والصور والأجزاء والقوالب) والتحقق من صحتها ونشرها بشكل متزامن في إجراء واحد.</span><span class="sxs-lookup"><span data-stu-id="18c75-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="18c75-109">توفر القدرة على تجميع الأصناف في المجموعات المنطقية التي تقوم بنشر الأصناف معًا، حيث تحتوي كل مجموعة على دورة الحياة الخاصة بها، وتوفر العديد من المزايا لمؤلفي الموقع.</span><span class="sxs-lookup"><span data-stu-id="18c75-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="18c75-110">في Commerce، تُعرف هذه المجموعات المنطقية باسم مجموعات النشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="18c75-111">إنها تسمح لمؤلفي الموقع بتعقب مجموعات من التحديثات على أنها كيانات قابلة للتكوين وقابلة للاختبار وقابلة للنشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="18c75-112">يمكن للمؤلفين معاينة التحديثات في مجموعة نشر مجمعة دون التأثير على موقع العرض المباشر أو مجموعات النشر المكتملة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="18c75-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="18c75-113">يمكن للمؤلفين بعد ذلك جدولة إجراء النشر لنشر كافة الأصناف الموجودة في مجموعة النشر في الوقت نفسه في موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="18c75-114">تُعد القدرة على تجميع التحديثات ومعاينتها وجدولتها للنشر مهمة للعديد من الشركات على مستوى المؤسسة التي تعمل على وضع إيرادات سنوية كبيرة عن المراحل الرئيسية لتحديث الموقع المستندة إلى الحدث.</span><span class="sxs-lookup"><span data-stu-id="18c75-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="18c75-115">يمكن للشركات تكبد تكاليف من لعمليات نشر المحتوى البطيء أو الذي تم إبطاله والتي لا تسير بسلاسة.</span><span class="sxs-lookup"><span data-stu-id="18c75-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="18c75-116">تساعد مجموعات النشر على ضمان أنه يتم تنظيم عمليات الإطلاق والتحقق من صحتها ونشرها في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="18c75-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="18c75-117">سواء كانت كبيرة أو صغيرة، تقدم مجموعات النشر توفر مجموعة أدوات قيمة تساعد المؤلفين على تنظيم وتبسيط مهام تحديث الموقع الجارية.</span><span class="sxs-lookup"><span data-stu-id="18c75-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="18c75-118">متى يتم استخدام مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="18c75-118">When to use publish groups</span></span>

<span data-ttu-id="18c75-119">يمكنك استخدام مجموعات النشر كلما كان يجب عليك تقسيم المستندات المتعددة ونشرها معًا.</span><span class="sxs-lookup"><span data-stu-id="18c75-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="18c75-120">على سبيل المثال، إذا كان موقع الويب الخاص بك يقوم بتحديث المحتوى كل موسم، فإنه يمكنك إنشاء مجموعات نشر لهذه الحركات التسويقية الموسمية.</span><span class="sxs-lookup"><span data-stu-id="18c75-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="18c75-121">قد تحتوي مجموعة نشر "التحديث الموسمي لفصل الخريف" على صور موسمية جديدة، وأجزاء تحتوى على رسائل تسويقية موسمية، وصفحات تشمل مجموعات المنتجات الموسمية، أو تحديثات موسمية أخرى لمواقع الويب.</span><span class="sxs-lookup"><span data-stu-id="18c75-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="18c75-122">تكمن ميزة مجموعات النشر في أنه يمكنك إظهار تحديثات متعددة في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="18c75-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="18c75-123">على سبيل المثال، بعد وقت قصير من التحديث لمجموعه نشر "التحديث الموسمي لفصل الخريف"، قد يكون هناك تحديث محتوى لعطلة نهاية أسبوع معينة.</span><span class="sxs-lookup"><span data-stu-id="18c75-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="18c75-124">في هذه الحالة، يمكنك إظهار محتوى لمجموعة نشر "التحديث الموسمي السنوي" في الوقت نفسه الذي تقوم فيه بعرض محتوى لمجموعة نشر "تحديث العطلات في فصل الخريف" اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="18c75-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="18c75-125">تحتوي كل مجموعة نشر على مجموعة فريدة خاصة بها من الصفحات والصور والأجزاء والقوالب وهكذا.</span><span class="sxs-lookup"><span data-stu-id="18c75-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="18c75-126">يمكنك عرض مجموعتي النشر هذه ومعاينتها والتحقق من صحتها بشكل مستقل ولكن على مخطط زمني متزامن.</span><span class="sxs-lookup"><span data-stu-id="18c75-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="18c75-127">ويمكن بعد ذلك جدولة كل مجموعة نشر للانتقال إلى العرض المباشر لموقعك في تواريخ وأوقات محددة.</span><span class="sxs-lookup"><span data-stu-id="18c75-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="18c75-128">تشغيل ميزة مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="18c75-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="18c75-129">تُعد ميزة مجموعات النشر اختيارية ويجب تشغيلها لموقعك.</span><span class="sxs-lookup"><span data-stu-id="18c75-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="18c75-130">لتشغيل ميزة مجموعات النشر لموقعك في أدوات تأليف Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="18c75-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="18c75-131">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="18c75-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="18c75-132">ضمن **إعدادات الموقع**، حدد **الميزات**.</span><span class="sxs-lookup"><span data-stu-id="18c75-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="18c75-133">قم بتعيين خيار **مجموعات النشر** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="18c75-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="18c75-134">إنشاء مجموعة نشر</span><span class="sxs-lookup"><span data-stu-id="18c75-134">Create a publish group</span></span>

<span data-ttu-id="18c75-135">لإنشاء مجموعة نشرلموقعك في أدوات تأليف Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="18c75-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="18c75-136">في جزء التنقل على اليسار، حدد **مجموعات النشر**.</span><span class="sxs-lookup"><span data-stu-id="18c75-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="18c75-137">في شريط الأوامر العلوي، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="18c75-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="18c75-138">في مربع الحوار **إنشاء مجموعة نشر**، ضمن **اسم مجموعة النشر**، أدخل اسمًا وصفيًا.</span><span class="sxs-lookup"><span data-stu-id="18c75-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="18c75-139">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="18c75-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="18c75-140">تعيين سياق تأليف مجموعة النشر</span><span class="sxs-lookup"><span data-stu-id="18c75-140">Set the publish group authoring context</span></span>

<span data-ttu-id="18c75-141">في Commerce، يكون سياق التأليف الافتراضي هو سياق موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="18c75-142">يكون سياق تأليف موقع العرض المباشر هو طريقة العرض الافتراضية حيث يمكنك العرض والقيام بالتغييرات مباشرة على موقع الويب الخاص بك دون استخدام جروب نشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="18c75-143">وإنه يمثل أحدث التحديثات المباشرة للإصدار المنشور لموقعك.</span><span class="sxs-lookup"><span data-stu-id="18c75-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="18c75-144">إذا كان عنصر تحكم السياق ضمن **مجموعات النشر** في جزء التنقل الأيسر يعرض اسم **موقع العرض المباشر**، فإنك تعمل في سياق تأليف موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="18c75-145">إن **موقع العرض المباشر** هو الاسم الافتراضي لعنصر تحكم السياق.</span><span class="sxs-lookup"><span data-stu-id="18c75-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="18c75-146">وإلا، يعرض عنصر تحكم السياق اسم مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="18c75-147">للعمل في مجموعة نشر، فإنه يجب عليك التبديل إلى سياق تأليف مجموعة النشر له.</span><span class="sxs-lookup"><span data-stu-id="18c75-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="18c75-148">لتعيين سياق مجموعة النشر، اتبع إحدى الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="18c75-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="18c75-149">في جزء التنقل الأيسر، حدد عنصر تحكم السياق مباشرة ضمن **مجموعات النشر**، ثم حدد اسم مجموعة النشر في قائمة الخيارات التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="18c75-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="18c75-150">تتم إعادة تسمية عنصر تحكم السياق ويعرض مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="18c75-151">في جزء التنقل الأيسر، حدد **مجموعات النشر**، ثم ضمن **مجموعات النشر**، حدد اسم مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="18c75-152">تتم إعادة تسمية عنصر تحكم السياق ويعرض مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="18c75-153">بعد تعيين سياق تأليف مجموعة النشر، فإنك تعمل في سياق مجموعة النشر عند تقوم بمعاينة محتوى الموقع وتحريره.</span><span class="sxs-lookup"><span data-stu-id="18c75-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="18c75-154">للرجوع إلى سياق تأليف موقع العرض المباشر الافتراضي، حدد عنصر تحكم السياق، ثم حدد **موقع العرض المباشر**.</span><span class="sxs-lookup"><span data-stu-id="18c75-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="18c75-155">إضافة صفحات أو أصناف أخرى إلى مجموعة نشر</span><span class="sxs-lookup"><span data-stu-id="18c75-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="18c75-156">بعد أن تقوم بتحديد سياق تأليف مجموعة نشر، ويعرض عنصر تحكم السياق في جزء التنقل الأيسر اسمه، فإنه يمكنك إنشاء محتوى تمامًا كما تفعل في سياق موقع العرض المباشر الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="18c75-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="18c75-157">يمكنك أيضًا إضافة الصفحات الموجودة أو الأصناف الأخرى من مجموعات النشر الأخرى، أو من سياق موقع العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="18c75-158">لنسخ الصفحات الموجودة إلى مجموعة نشر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="18c75-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="18c75-159">حدد سياق التأليف المراد النسخ منه، ثم في جزء التنقل الأيسر، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="18c75-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="18c75-160">حدد الصفحة التي تريد إضافتها إلى مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="18c75-161">في شريط الأوامر، حدد **نسخ إلى مجموعة النشر**.</span><span class="sxs-lookup"><span data-stu-id="18c75-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="18c75-162">في مربع الحوار **تحديد مجموعة نشر**، حدد مجموعة النشر المراد إضافة الصفحة إليها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="18c75-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="18c75-163">يمكنك استخدام الخطوات الأساسية نفسها لإنشاء صفحات المنتج المخصصة وعناوين Url والقوالب والتخطيطات والأجزاء وأصول المكتبة الوسائط ، أو لإضافة أصناف موجودة من هذه الأنواع إلى مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="18c75-164">التحقق من صحة مجموعة نشر</span><span class="sxs-lookup"><span data-stu-id="18c75-164">Validate a publish group</span></span>

<span data-ttu-id="18c75-165">للتأكد من أن كافة التبعيات في محتوى مجموعة النشر مستوفاه، ومن أنه يتم النجاح في كافة عمليات التحقق من الصحة، فإنه يمكنك التحقق للتعرف على أية مشكلات يجب معالجتها قبل جدولة إجراء نشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="18c75-166">للتحقق من صحة مجموعة النشر الخاصة بك قبل أن تقوم بجدولتها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="18c75-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="18c75-167">في جزء التنقل على اليسار، حدد **مجموعات النشر**.</span><span class="sxs-lookup"><span data-stu-id="18c75-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="18c75-168">حدد مجموعة النشر للتحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="18c75-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="18c75-169">في شريط الأوامر العلوي، حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="18c75-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="18c75-170">يتم تشغيل التحقق من الصحة على كل المحتوى الموجود في مجموعة النشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="18c75-171">سيتم عرض أية مشكلات ستمنع إجراء نشر ناجح في مربع الإخطار الذي يظهر في الجزء العلوي الأيمن.</span><span class="sxs-lookup"><span data-stu-id="18c75-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="18c75-172">يتم دائمًا تشغيل التحقق من الصحة تلقائيًا عند جدولة مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="18c75-173">ومع ذلك، يكون الزر **التحقق من الصحة** الموجود في شريط الأوامر مفيدًا لأنه يساعد في تحديد المشكلات التي يجب إصلاحها قبل محاولة جدولة مجموعة نشر للعرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="18c75-174">جدولة مجموعة نشر للعرض المباشر</span><span class="sxs-lookup"><span data-stu-id="18c75-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="18c75-175">لجدولة مجموعة نشر للعرض المباشر في موقعك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="18c75-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="18c75-176">في جزء التنقل على اليسار، حدد **مجموعات النشر**.</span><span class="sxs-lookup"><span data-stu-id="18c75-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="18c75-177">ضمن **مجموعات النشر**، حدد مجموعة النشر المراد جدولتها.</span><span class="sxs-lookup"><span data-stu-id="18c75-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="18c75-178">في شريط الأوامر العلوي، حدد **تحرير الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="18c75-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="18c75-179">يظهر مربع الحوار **تحرير الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="18c75-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="18c75-180">حدد التاريخ والوقت الذي يجب أن يتم فيه عرض مجموعة النشر عرضًا مباشرًا، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="18c75-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="18c75-181">لإلغاء جدولة مجموعة نشر، اتبع الخطوات نفسها، ولكن حدد **إلغاء جدولة مجموعة نشر** في مربع الحوار **تحرير جدول**.</span><span class="sxs-lookup"><span data-stu-id="18c75-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="18c75-182">قد تستغرق مجموعات النشر الكبيرة للغاية مدة تصل إلى دقيقة أو دقيقتين ليتم نشرها عند وصول الوقت المجدول.</span><span class="sxs-lookup"><span data-stu-id="18c75-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="18c75-183">تأكد من ألا يكون إجراء النشر فوريًا، وأنه سيتم نشر مجموعات نشر أصغر بشكل أسرع.</span><span class="sxs-lookup"><span data-stu-id="18c75-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="18c75-184">الأسئلة المتداولة عن مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="18c75-184">Publish groups FAQ</span></span>

<span data-ttu-id="18c75-185">**كم عدد الأصناف التي يمكن أن تكون موجودة في مجموعة نشر ؟**</span><span class="sxs-lookup"><span data-stu-id="18c75-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="18c75-186">حاليًا، هناك حد 2,000 من الأصناف لكل مجموعة نشر.</span><span class="sxs-lookup"><span data-stu-id="18c75-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="18c75-187">لاحظ أن مجموعات النشر الكبيرة للغاية قد تستغرق عدة دقائق ليتم نشرها عند وصول الوقت المجدول.</span><span class="sxs-lookup"><span data-stu-id="18c75-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="18c75-188">**هل مجموعات النشر مثل كود "فروع" في مصطلحات تطوير البرامج ؟**</span><span class="sxs-lookup"><span data-stu-id="18c75-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="18c75-189">نعم ولا.</span><span class="sxs-lookup"><span data-stu-id="18c75-189">Yes and no.</span></span> <span data-ttu-id="18c75-190">يمكن اعتبار مجموعات النشر من الإصدارات المتشعبة لموقعك.</span><span class="sxs-lookup"><span data-stu-id="18c75-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="18c75-191">وبهذه الطريقة، فإنها تتصرف مثل الفروع.</span><span class="sxs-lookup"><span data-stu-id="18c75-191">In that way, they do act like branches.</span></span> <span data-ttu-id="18c75-192">ومع ذلك، لا يوجد مفهوم دمج على مستوى الأصناف الفردية.</span><span class="sxs-lookup"><span data-stu-id="18c75-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="18c75-193">يتم استبدال الصنف الذي يتم نشره أخيرًا بالصنف الذي كان موجودًا مسبقًا، ودائمًا ما يحل إجراء النشر الأحدث محل إجراءات النشر السابقة.</span><span class="sxs-lookup"><span data-stu-id="18c75-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="18c75-194">**هل يمكنني جدوله مجموعتي نشر للعرض المباشر في نفس الوقت ؟**</span><span class="sxs-lookup"><span data-stu-id="18c75-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="18c75-195">الرقم</span><span class="sxs-lookup"><span data-stu-id="18c75-195">No.</span></span> <span data-ttu-id="18c75-196">لأسباب تتعلق بالأداء والتعارض، سيجبرك النظام على تنظيم مجموعات نشر مجدولة لمدة خمس دقائق على الأقل.</span><span class="sxs-lookup"><span data-stu-id="18c75-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="18c75-197">**هل يمكنني استخدام مجموعات نشر لجدولة أصناف مكتب الدعم متعدد الاتجاهات، مثل الخصومات وتحديثات المنتج ؟**</span><span class="sxs-lookup"><span data-stu-id="18c75-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="18c75-198">حاليًا، تدعم ميزة مجموعات النشر محتوى موقع ويب فقط.</span><span class="sxs-lookup"><span data-stu-id="18c75-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="18c75-199">ومع ذلك، تدرك Microsoft أن التكامل مع سيناريوهات الترويج لمكاتب الدعم يمكن أن يكون مفيدًا للتنسيق والأتمتة بعمليات إطلاق حملة متعددة الاتجاهات.</span><span class="sxs-lookup"><span data-stu-id="18c75-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18c75-200">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="18c75-200">Additional resources</span></span>

[<span data-ttu-id="18c75-201">طرق إضافة المحتوى</span><span class="sxs-lookup"><span data-stu-id="18c75-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="18c75-202">مصطلحات نموذج الصفحة</span><span class="sxs-lookup"><span data-stu-id="18c75-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="18c75-203">حالات المستند ودورة الحياة</span><span class="sxs-lookup"><span data-stu-id="18c75-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="18c75-204">تمكين المشاركة عبر القنوات واستخدامها</span><span class="sxs-lookup"><span data-stu-id="18c75-204">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="18c75-205">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="18c75-205">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="18c75-206">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="18c75-206">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="18c75-207">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="18c75-207">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="18c75-208">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="18c75-208">Customize site navigation</span></span>](customize-site-navigation.md)
