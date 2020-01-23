---
title: إضافة شعار
description: يوضح هذا الموضوع كيفية إضافة شعار إلى موقعك في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914604"
---
# <a name="add-a-logo"></a><span data-ttu-id="f6617-103">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="f6617-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f6617-104">يوضح هذا الموضوع كيفية إضافة شعار إلى موقعك في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6617-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f6617-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="f6617-105">Overview</span></span>

<span data-ttu-id="f6617-106">عند إنشاء موقعك، من بين الأشياء الأولى التي ربما ستقوم بها هي إضافة شعار شركتك أو علامتك التجارية إلى رأس الموقع.</span><span class="sxs-lookup"><span data-stu-id="f6617-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="f6617-107">توفر مجموعة أدوات بدء تشغيل Dynamics 365 Commerce عبر الإنترنت وحدة تجعل هذه المهمة سهلة.</span><span class="sxs-lookup"><span data-stu-id="f6617-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="f6617-108">يمكنك إضافة شعار مباشرة إلى قالب أو تخطيط أو صفحة.</span><span class="sxs-lookup"><span data-stu-id="f6617-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="f6617-109">بهذه الطريقة، يمكنك بسهولة تغيير الشعار الذي يظهر على صفحات أو مجموعات محددة من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="f6617-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="f6617-110">ومع ذلك، يغطي هذا الموضوع السيناريو الأكثر شيوعًا، حيث تضيف شعارك إلى جزء من الرأس يمكن إعادة استخدامه عبر جميع صفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="f6617-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f6617-111">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="f6617-111">Prerequisites</span></span>

<span data-ttu-id="f6617-112">قبل أن تتمكن من إضافة شعار إلى جميع صفحات موقعك، ينبغي عليك إكمال هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="f6617-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="f6617-113">قم بتحميل شعارك على مدير الأصول الرقمية، والذي يمكنك الوصول إليه من صفحة **الأصول** .</span><span class="sxs-lookup"><span data-stu-id="f6617-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="f6617-114">إنشاء جزء الرأس.</span><span class="sxs-lookup"><span data-stu-id="f6617-114">Create a header fragment.</span></span> <span data-ttu-id="f6617-115">لمزيد من المعلومات حول كيفية إنشاء الأجزاء واستخدامها ، راجع [العمل مع الأجزاء](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="f6617-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="f6617-116">قم بتضمين جزء الرأس في القالب الذي تستخدمه صفحات موقعك لتخطيطها وخيارات الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="f6617-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="f6617-117">لمزيد من المعلومات حول القوالب، راجع [العمل مع القوالب](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f6617-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="f6617-118">إضافة شعار إلى جزء الرأس</span><span class="sxs-lookup"><span data-stu-id="f6617-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="f6617-119">لإضافة شعار إلى جزء الرأس لموقعك ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f6617-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="f6617-120">في جزء التنقل علي اليسار، حدد **الأجزاء**، ثم حدد جزء الرأس الذي قمت بإنشاءه.</span><span class="sxs-lookup"><span data-stu-id="f6617-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="f6617-121">حدد **سحب**.</span><span class="sxs-lookup"><span data-stu-id="f6617-121">Select **Check out**.</span></span>
3. <span data-ttu-id="f6617-122">قم بتوسيع فتحة **الرأس** وفتحة **الشعار** .</span><span class="sxs-lookup"><span data-stu-id="f6617-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="f6617-123">تحديد زر علامة الحذف (**...**) للفتحة **الشعار** ، ثم حدد **‏‫إضافة وحدة نمطية‬**.</span><span class="sxs-lookup"><span data-stu-id="f6617-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="f6617-124">حدد الوحدة النمطية للشعار.</span><span class="sxs-lookup"><span data-stu-id="f6617-124">Select the logo module.</span></span>
6. <span data-ttu-id="f6617-125">في جزء الخصائص على اليمين، قم بتكوين وحدة الشعار بحيث تظهر شعارك.</span><span class="sxs-lookup"><span data-stu-id="f6617-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="f6617-126">قم بحفظ جزء العنوان، وإيداعه ونشره.</span><span class="sxs-lookup"><span data-stu-id="f6617-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="f6617-127">بعد نشر جزء الرأس المحدّث، سوف تُظهر جميع صفحات الموقع التي تستخدم القالب الذي يحتوي على جزء الرأس شعارك.</span><span class="sxs-lookup"><span data-stu-id="f6617-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6617-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f6617-128">Additional resources</span></span>

[<span data-ttu-id="f6617-129">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="f6617-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f6617-130">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="f6617-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f6617-131">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="f6617-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f6617-132">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="f6617-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f6617-133">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="f6617-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f6617-134">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="f6617-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f6617-135">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="f6617-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

