---
title: ‏‫العمل باستخدام ملفات التجاوز في CSS .
description: يصف هذا الموضوع لماذا، ومتى، وكيفية استخدام ملفات التجاوز الخاصة بأوراق الأنماط المتتالية (CSS) في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409895"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="5c980-103">‏‫العمل باستخدام ملفات التجاوز في CSS .</span><span class="sxs-lookup"><span data-stu-id="5c980-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5c980-104">يصف هذا الموضوع لماذا، ومتى، وكيفية استخدام ملفات التجاوز الخاصة بأوراق الأنماط المتتالية (CSS) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5c980-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c980-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5c980-105">Overview</span></span>

<span data-ttu-id="5c980-106">يجب دائمًا معالجة أنماط الموقع الدائمة من خلال سمة الموقع.</span><span class="sxs-lookup"><span data-stu-id="5c980-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="5c980-107">توفر المظاهر إعدادات CSS وإعدادات النمط للوحدات النمطية في أي صفحة من موقعك.</span><span class="sxs-lookup"><span data-stu-id="5c980-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="5c980-108">يتم إنشاء السمات باستخدام مجموعة تطوير البرامج (SDK) الخاصة بـ Dynamics 365 Commerce عبر الإنترنت، ويتم نشرها على مواقع الويب الخاصة بك من خلال Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5c980-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5c980-109">تساعد قدرات تصحيح السمات وتكوينات واجهة الوحدة النمطية في SDK مطوري المواقع على إنشاء حزم تصميم موقع قابلة للتخصيص ومتماسكة.</span><span class="sxs-lookup"><span data-stu-id="5c980-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="5c980-110">عند نشر حزم التصميم هذه على موقع ما، يمكن لمؤلفي الموقع التركيز على إنشاء محتوى وتحريره ونشره بدلاً من تطوير الموقع.</span><span class="sxs-lookup"><span data-stu-id="5c980-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="5c980-111">بالنظر إلى دورة الحياة المعتادة للسمة، فإن الاعتماد على المطورين لإجراء تغييرات على النمط من خلال تدفقات نشر SDK و LCS قد يكون باهظ الثمن في بعض السيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="5c980-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="5c980-112">قد تبدو النماذج الأولية أو الإصلاحات العاجلة للموقع مرهقة إذا لم يتم تكوين SDK، أو إذا لم يكن لديك الوقت لانتظار نشر LCS.</span><span class="sxs-lookup"><span data-stu-id="5c980-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="5c980-113">في هذه السيناريوهات، يمكن ان تساعد ملفات التجاوز الخاصة بـ CSS .</span><span class="sxs-lookup"><span data-stu-id="5c980-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="5c980-114">في أدوات التأليف التجارة، يمكن للمستخدمين المصادق عليهم تحميل ملف CSS، ومعاينته، ثم تنشيطه لتجاوز سمة الموقع.</span><span class="sxs-lookup"><span data-stu-id="5c980-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="5c980-115">لا نحتاج إلى مصروفات زائدة‬ لنشر SDK أو LCS.</span><span class="sxs-lookup"><span data-stu-id="5c980-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="5c980-116">يمكن أن تكون التجاوزات المحددة في ملف التجاوز الخاص بـ CSS صغيرة مثل التغيير في نمط نص واحد أو واسعة النطاق مثل إصلاح العلامة التجارية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="5c980-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="5c980-117">قبل استخدام ملفات التجاوز الخاصة بـ CSS، يجب أن تكون علي علم بالقيود التالية:</span><span class="sxs-lookup"><span data-stu-id="5c980-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="5c980-118">يمكن فقط تنشيط ملف تجاوز CSS واحد فقط علي الموقع في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="5c980-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="5c980-119">لذا، يجب أن تكون كافة التجاوزات النشطة موجودة في ملف تجاوز واحد.</span><span class="sxs-lookup"><span data-stu-id="5c980-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="5c980-120">على الرغم من أنه يمكنك معاينة التجاوزات في أدوات تأليف التجارة، إلا أنه لا توجد ميزات مخصصة لتصحيح الأخطاء للمساعدة في تحديد أي أخطاء تقدمها التجاوزات.</span><span class="sxs-lookup"><span data-stu-id="5c980-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="5c980-121">وبعبارة أخرى، عند استخدام ملفات CSS للتجاوز، لا تملك نفس مجموعة الأدوات التي يوفرها SDK لوحدة التحقق من صحة الوحدة والتأليف.</span><span class="sxs-lookup"><span data-stu-id="5c980-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="5c980-122">ومع ذلك، توفر ملفات CSS للتجاوز طريقه سريعة لنموذج تصميم أو تطبيق إصلاح عاجل قبل تحديث سمه كامله تطوير ونشرها.</span><span class="sxs-lookup"><span data-stu-id="5c980-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="5c980-123">إنشاء ملف CSS للتجاوز</span><span class="sxs-lookup"><span data-stu-id="5c980-123">Create a CSS override file</span></span>

<span data-ttu-id="5c980-124">لإنشاء ملف CSS للتجاوز، يمكنك استخدام اي بيئة تطوير متكاملة (IDE) أو محرر نص أو محرر التعليمات البرمجية المصدر.</span><span class="sxs-lookup"><span data-stu-id="5c980-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="5c980-125">تتمثل الطريقة المعتادة في استخدام مصحح أخطاء الويب القياسية في المستعرض الخاص بك لتحديد محددات النمط والخصائص والقيم على موقعك الحالي.</span><span class="sxs-lookup"><span data-stu-id="5c980-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="5c980-126">تسمح لك معظم المستعرضات بتغيير القيم ومعاينتها في مصحح الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="5c980-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="5c980-127">بعد تحديد التغييرات التي تريد اجراؤها، يمكنك حفظها في ملف CSS الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5c980-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="5c980-128">تحميل ملف CSS للتجاوز</span><span class="sxs-lookup"><span data-stu-id="5c980-128">Upload a CSS override file</span></span>

<span data-ttu-id="5c980-129">لتحميل ملف CSS إلى موقعك في التجارة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5c980-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5c980-130">في أدوات التأليف، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5c980-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="5c980-131">في جزء التنقل على اليسار، حدد **التصميم**.</span><span class="sxs-lookup"><span data-stu-id="5c980-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c980-132">استنادًا إلى إصدار أدوات تأليف التجارة التي تستخدمها، قد تضطر إلى توسيع **الإعدادات** في جزء التنقل قبل ان تتمكن من تحديد **التصميم**.</span><span class="sxs-lookup"><span data-stu-id="5c980-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="5c980-133">في الجزء العلوي من جزء التصميم الرئيسي، حدد علامة التبويب **CSS للتجاوز**، إذا لم تكن محددة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="5c980-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="5c980-134">ضمن **ملفات CSS للتجاوز المتوفرة**، حدد **تحميل ملف CSS**.</span><span class="sxs-lookup"><span data-stu-id="5c980-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="5c980-135">يظهر إطار مستكشف الملفات.</span><span class="sxs-lookup"><span data-stu-id="5c980-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="5c980-136">في "مستكشف الملفات"، استعرض ملف CSS وحدده، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="5c980-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="5c980-137">يظهر ملف CSS الذي تم تحميله الآن ضمن **ملفات CSS للتجاوز المتوفرة**.</span><span class="sxs-lookup"><span data-stu-id="5c980-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="5c980-138">معاينة ملف CSS للتجاوز</span><span class="sxs-lookup"><span data-stu-id="5c980-138">Preview a CSS override file</span></span>

<span data-ttu-id="5c980-139">لمعاينة ملف CSS للتجاوز قبل جعله نشطًا علي موقعك المباشر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5c980-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="5c980-140">في جزء التنقل علي اليسار، حدد **تصميم**، ثم في علامة التبويب ملفات **CSS للتجاوز**، ضمن **ملفات CSS للتجاوز المتوفرة**، ابحث عن ملف CSS الذي تريد معاينته.</span><span class="sxs-lookup"><span data-stu-id="5c980-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="5c980-141">بجوار اسم ملف CSS، حدد **معاينه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="5c980-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="5c980-142">في مربع الحوار **حدد عنوان URL**، حدد عنوان URL الخاص بالموقع الذي ترغب في رؤية التجاوز المطبق عليه، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c980-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="5c980-143">إذا كان هناك العديد من المتغيرات لعنوان URL المحدد، فحدد المتغير المطلوب في مربع الحوار **معاينة التغييرات** التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="5c980-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="5c980-144">يتم فتح علامة تبويب أو نافذة مستعرض جديدة، حيث يمكنك التحقق من صحة تجاوزات النمط الخاصة بك مقابل موقعك.</span><span class="sxs-lookup"><span data-stu-id="5c980-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="5c980-145">يمكنك بعد ذلك مشاركة عنوان URL مع مستخدمي التجارة المعتمدين الآخرين للمراجعة والتعليقات.</span><span class="sxs-lookup"><span data-stu-id="5c980-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="5c980-146">قم بتنشيط ملف CSS للتجاوز على موقع العرض المباشر الخاص بك</span><span class="sxs-lookup"><span data-stu-id="5c980-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="5c980-147">بعد معاينة ملف CSS للتجاوز واعتماده، يمكنك تنشيطه على موقع العرض المباشر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5c980-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="5c980-148">يمكن فقط تنشيط ملف CSS للتجاوز واحد فقط علي موقعك في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="5c980-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="5c980-149">إذا قمت بتنشيط ملف تجاوز جديد، يتم إلغاء تنشيط ملف التجاوز السابق.</span><span class="sxs-lookup"><span data-stu-id="5c980-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="5c980-150">لذا، تأكد من أن كافة التجاوزات المطلوبة موجودة في ملف CSS للتجاوز واحد.</span><span class="sxs-lookup"><span data-stu-id="5c980-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="5c980-151">لتنشيط ملف CSS للتجاوز، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5c980-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="5c980-152">في جزء التنقل علي اليسار، حدد **تصميم**، ثم في علامة التبويب ملفات **CSS للتجاوز**، ضمن **ملفات CSS للتجاوز المتوفرة**، ابحث عن ملف CSS الذي تريد تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="5c980-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="5c980-153">ضمن اسم ملف CSS، حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="5c980-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="5c980-154">يصبح ملف التجاوز نشطًا على الفور في موقع العرض المباشر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5c980-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="5c980-155">إلغاء تنشيط ملف CSS للتجاوز على موقع العرض المباشر الخاص بك</span><span class="sxs-lookup"><span data-stu-id="5c980-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="5c980-156">لإلغاء تنشيط CSS ملف تجاوز علي موقعك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5c980-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="5c980-157">في جزء التنقل علي اليسار، حدد **تصميم**، ثم في علامة التبويب ملفات **CSS للتجاوز**، ضمن **ملفات CSS للتجاوز المتوفرة**، ابحث عن ملف CSS الذي تريد إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="5c980-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="5c980-158">ضمن اسم ملف CSS، حدد **إلغاء التنشيط**.</span><span class="sxs-lookup"><span data-stu-id="5c980-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="5c980-159">يصبح ملف التجاوز غير نشط على الفور في موقع العرض المباشر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5c980-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="5c980-160">للوصول إلى خيارات ملفات CSS للتجاوز الإضافية، حدد علامة القطع (**...**) بجوار اسم ملف CSS .</span><span class="sxs-lookup"><span data-stu-id="5c980-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="5c980-161">تعتبر خيارات **التنزيل**، و **إعادة التسمية**، و **الاستبدال** مفيدة للتغييرات السريعة على ملف CSS للتجاوز الموجود.</span><span class="sxs-lookup"><span data-stu-id="5c980-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c980-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5c980-162">Additional resources</span></span>

[<span data-ttu-id="5c980-163">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="5c980-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5c980-164">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="5c980-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5c980-165">استخدام الإعدادات المسبقة للأنماط</span><span class="sxs-lookup"><span data-stu-id="5c980-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="5c980-166">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="5c980-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5c980-167">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="5c980-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5c980-168">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="5c980-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5c980-169">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="5c980-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5c980-170">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="5c980-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
