---
title: إضافة صفحة سياسة الخصوصية
description: يصف هذا الموضوع كيفية إضافة صفحة سياسة الخصوصية إلى موقعك في Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001313"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="35495-103">إضافة صفحة سياسة الخصوصية</span><span class="sxs-lookup"><span data-stu-id="35495-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35495-104">يصف هذا الموضوع كيفية إضافة صفحة سياسة الخصوصية إلى موقعك في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="35495-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35495-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="35495-105">Overview</span></span>

<span data-ttu-id="35495-106">يتضمن الالتزام بالخصوصية تدابير تنظيمية تُعلم مستخدمي الموقع بكيفية جمع بياناتهم ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="35495-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="35495-107">ويمكن للمستخدمين بعد ذلك أن يقرروا كيف يريدون معالجة بياناتهم الشخصية ويمكنهم اتخاذ الإجراءات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="35495-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="35495-108">راجع بيان خصوصية Microsoft في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="35495-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="35495-109">لمراجعة بيان خصوصية Microsoft أثناء تسجيل الدخول إلى أدوات تأليف Dynamics 365 Commerce ، حدد الزر **تعليمات** (**؟**) في الركن الأعلى الأيمن، ثم حدد **الخصوصية وملفات تعريف الارتباط**.</span><span class="sxs-lookup"><span data-stu-id="35495-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="35495-110">يتم فتح علامة تبويب جديدة تحتوي على رابط لـ [بيان خصوصية Microsoft](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="35495-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="35495-111">إنشاء صفحة سياسة الخصوصية لموقعك</span><span class="sxs-lookup"><span data-stu-id="35495-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="35495-112">في Dynamics 365 Commerce، هناك عده طرق لمنح مستخدمي موقعك الوصول إلى سياسة الخصوصية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="35495-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="35495-113">يوضح هذا القسم كيفية إنشاء صفحة سياسة الخصوصية ثم الرجوع إلى الصفحة باستخدام جزء التذييل.</span><span class="sxs-lookup"><span data-stu-id="35495-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="35495-114">الإرشادات التالية هي مثال يوضح كيفية إنشاء صفحة سياسة خصوصية عامة لموقع التجارة.</span><span class="sxs-lookup"><span data-stu-id="35495-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="35495-115">أنت مسؤول عن تصميم وتنفيذ حل صفحة سياسة الخصوصية الذي يلبي المتطلبات القانونية لشركتك.</span><span class="sxs-lookup"><span data-stu-id="35495-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="35495-116">للبدء، في أدوات التأليف، انتقل إلى الموقع الذي تريد إنشاء صفحة سياسة خصوصية له.</span><span class="sxs-lookup"><span data-stu-id="35495-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="35495-117">إنشاء قالب</span><span class="sxs-lookup"><span data-stu-id="35495-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="35495-118">إذا كان قد تم بالفعل إنشاء قالب يمكن استخدامه لصفحة سياسة الخصوصية، فانتقل إلى قسم [إنشاء سياسة الخصوصية](#build-a-privacy-policy-page)</span><span class="sxs-lookup"><span data-stu-id="35495-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="35495-119">لإنشاء قالب، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="35495-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="35495-120">انتقل إلي **قوالب \> قالب جديد**.</span><span class="sxs-lookup"><span data-stu-id="35495-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="35495-121">قم بإدخال اسم القالب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="35495-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="35495-122">في القالب، قم بإضافة أي وحدات مطلوبة إلى فتحات الصفحة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="35495-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="35495-123">للحصول على إرشادات، مرر مؤشر الماوس فوق علامات التعجب الحمراء.</span><span class="sxs-lookup"><span data-stu-id="35495-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="35495-124">على سبيل المثال، قد تتطلب فتحة **رأس HTML** الوحدة النمطية **النص الخارجي الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="35495-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="35495-125">في فتحة **النص الأساسي‏‎** ، أضف الوحدة النمطية **الصفحة الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="35495-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="35495-126">في الوحدة النمطية **الصفحة الافتراضية** ، قم بإضافة الفتحة **الرئيسية** ، أضف الوحدة النمطية **كتلة تنسيق المحتوى** .</span><span class="sxs-lookup"><span data-stu-id="35495-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="35495-127">في الوحدة النمطية **كتلة تنسيق المحتوى** ، أضف الوحدة النمطية **عنصر تنسيق المحتوى** .</span><span class="sxs-lookup"><span data-stu-id="35495-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="35495-128">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="35495-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="35495-129">إنشاء صفحة سياسة الخصوصية</span><span class="sxs-lookup"><span data-stu-id="35495-129">Build a privacy policy page</span></span>

<span data-ttu-id="35495-130">لإنشاء صفحة سياسة الخصوصية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="35495-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="35495-131">انتقل إلى **صفحات \> صفحة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="35495-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="35495-132">حدد القالب الخاص بصفحة سياسة الخصوصية.</span><span class="sxs-lookup"><span data-stu-id="35495-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="35495-133">قم بإدخال اسم الصفحة وعنوان URL، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="35495-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="35495-134">في الفتحة **الرئيسية** للصفحة، قم بإضافة الوحدة النمطية **كتلة تنسيق المحتوى** .</span><span class="sxs-lookup"><span data-stu-id="35495-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="35495-135">في الوحدة النمطية **كتلة تنسيق المحتوى** ، أضف الوحدة النمطية **عنصر تنسيق المحتوى** .</span><span class="sxs-lookup"><span data-stu-id="35495-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="35495-136">في جزء الخصائص للوحدة النمطية **كتلة تنسيق المحتوي** ، حدد **إضافة مصدر البيانات** ، ثم حدد **محتوي النص المنسق**.</span><span class="sxs-lookup"><span data-stu-id="35495-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="35495-137">في محرر النص المنسق، أدخل محتوى صفحة سياسة الخصوصية.</span><span class="sxs-lookup"><span data-stu-id="35495-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="35495-138">قم بتوسيع محرر النص المنسق إلى وضع ملء الشاشة كما تريد.</span><span class="sxs-lookup"><span data-stu-id="35495-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="35495-139">عند الانتهاء من إدخال المحتوى، حدد **معاينة** لمعاينة الصفحة في متصفح الويب.</span><span class="sxs-lookup"><span data-stu-id="35495-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="35495-140">أكمل أي إضافات متبقية إلى خصائص الصفحة والوحدة.</span><span class="sxs-lookup"><span data-stu-id="35495-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="35495-141">تحقق من صفحة سياسة الخصوصية في، ونشرها.</span><span class="sxs-lookup"><span data-stu-id="35495-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="35495-142">لنشر عنوان URL لصفحة سياسة الخصوصية، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="35495-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="35495-143">انتقل إلى **عناوين URL**، وحدد عنوان URL لصفحة سياسة الخصوصية.</span><span class="sxs-lookup"><span data-stu-id="35495-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="35495-144">نشر عنوان URL المحدد.</span><span class="sxs-lookup"><span data-stu-id="35495-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="35495-145">إنشاء رابط لصفحة سياسة الخصوصية في تذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="35495-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="35495-146">يمكنك إضافة رابط إلى صفحة سياسة الخصوصية إلى جزء.</span><span class="sxs-lookup"><span data-stu-id="35495-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="35495-147">وبهذه الطريقة، يمكنك مشاركة الرابط وتحديثه عبر صفحات مواقع متعددة من خلال الرجوع إلى الجزء.</span><span class="sxs-lookup"><span data-stu-id="35495-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="35495-148">يوضح هذا المثال كيفية إضافة ارتباط إلى صفحة سياسة الخصوصية إلى جزء من تذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35495-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="35495-149">لإضافة ارتباط إلى جزء تذييل الصفحة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="35495-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="35495-150">انتقل إلى **أجزاء الصفحة \> جزء صفحة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="35495-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="35495-151">حدد الوحدة النمطية **تذييل** ثم قم بإدخال اسم في الحقل **اسم جزء الصفحة** .</span><span class="sxs-lookup"><span data-stu-id="35495-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="35495-152">في فتحه **فئة التذييل** ، أضف الوحدة النمطية **عنصر التذييل** .</span><span class="sxs-lookup"><span data-stu-id="35495-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="35495-153">في جزء الخصائص على اليمين ، حدد **نص الارتباط**.</span><span class="sxs-lookup"><span data-stu-id="35495-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="35495-154">في مربع الحوار **نص الارتباط** ، أدخل نص الارتباط وهدف الارتباط الخاص بصفحة سياسة الخصوصية ، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="35495-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="35495-155">للحصول على عنوان URL الخاص لصفحة سياسة الخصوصية ، انتقل إلى **الصفحات** ، انتقل إلى صفحة سياسة الخصوصية، وانسخ عنوان URL من جزء الخصائص.</span><span class="sxs-lookup"><span data-stu-id="35495-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="35495-156">قم بحفظ جزء الصفحة، وإيداعه ونشره.</span><span class="sxs-lookup"><span data-stu-id="35495-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="35495-157">معاينة الجزء، واختبار الارتباط إلى صفحة سياسة الخصوصية.</span><span class="sxs-lookup"><span data-stu-id="35495-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="35495-158">يمكن الآن الرجوع إلى الجزء في قالب صفحات الموقع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="35495-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="35495-159">عندما تتم الإشارة إلى هذا الجزء في الوحدة المنطقية **تذييل** الخاصة بالقالب، سيظهر مرجع الارتباط في أي صفحات تم إنشاؤها باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="35495-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35495-160">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="35495-160">Additional resources</span></span>

[<span data-ttu-id="35495-161">‏‫نظرة عامة على التوافق</span><span class="sxs-lookup"><span data-stu-id="35495-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="35495-162">ميزات وقدرات إمكانية الوصول</span><span class="sxs-lookup"><span data-stu-id="35495-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="35495-163">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="35495-163">Cookie compliance</span></span>](cookie-compliance.md)
