---
title: إضافة شعار
description: يوضح هذا الموضوع كيفية إضافة شعار إلى موقعك في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797589"
---
# <a name="add-a-logo"></a><span data-ttu-id="7af27-103">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="7af27-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7af27-104">يوضح هذا الموضوع كيفية إضافة شعار إلى موقعك في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7af27-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7af27-105">عند إنشاء موقعك، من بين الأشياء الأولى التي ربما ستقوم بها هي إضافة شعار شركتك أو علامتك التجارية إلى رأس الموقع.</span><span class="sxs-lookup"><span data-stu-id="7af27-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="7af27-106">توفر مكتبة الوحدات النمطية في Dynamics 365 Commerce عبر الإنترنت وحدة تجعل هذه المهمة سهلة.</span><span class="sxs-lookup"><span data-stu-id="7af27-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="7af27-107">يمكنك إضافة شعار مباشرة إلى قالب أو تخطيط أو صفحة.</span><span class="sxs-lookup"><span data-stu-id="7af27-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="7af27-108">بهذه الطريقة، يمكنك بسهولة تغيير الشعار الذي يظهر على صفحات أو مجموعات محددة من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="7af27-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="7af27-109">ومع ذلك، يغطي هذا الموضوع السيناريو الأكثر شيوعًا، حيث تضيف شعارك إلى جزء من الرأس يمكن إعادة استخدامه عبر جميع صفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="7af27-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7af27-110">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="7af27-110">Prerequisites</span></span>

<span data-ttu-id="7af27-111">قبل أن تتمكن من إضافة شعار إلى جميع صفحات موقعك، ينبغي عليك إكمال هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="7af27-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="7af27-112">قم بتحميل الشعار إلى مكتبة الوسائط.</span><span class="sxs-lookup"><span data-stu-id="7af27-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="7af27-113">إنشاء جزء الرأس.</span><span class="sxs-lookup"><span data-stu-id="7af27-113">Create a header fragment.</span></span> <span data-ttu-id="7af27-114">لمزيد من المعلومات حول كيفية إنشاء الأجزاء واستخدامها، راجع [العمل مع الأجزاء](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="7af27-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="7af27-115">قم بتضمين جزء الرأس في القالب الذي تستخدمه صفحات موقعك لتخطيطها وخيارات الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="7af27-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="7af27-116">لمزيد من المعلومات حول القوالب، راجع [العمل مع القوالب](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="7af27-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="7af27-117">إضافة شعار إلى جزء الرأس</span><span class="sxs-lookup"><span data-stu-id="7af27-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="7af27-118">لإضافة شعار إلى جزء الرأس لموقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="7af27-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="7af27-119">في جزء التنقل على اليسار، حدد **الأجزاء**.</span><span class="sxs-lookup"><span data-stu-id="7af27-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="7af27-120">حدد جزء الرأس الذي أنشأته، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="7af27-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="7af27-121">قم بتوسيع وحدة الرأس.</span><span class="sxs-lookup"><span data-stu-id="7af27-121">Expand the header module.</span></span>
1. <span data-ttu-id="7af27-122">في جزء الخصائص لوحدة الرأس، قدم صورة وارتباطًا للشعار.</span><span class="sxs-lookup"><span data-stu-id="7af27-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="7af27-123">احفظ جزء الرأس ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="7af27-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="7af27-124">بعد نشر جزء الرأس المحدّث، سوف تُظهر جميع صفحات الموقع التي تستخدم القالب الذي يحتوي على جزء الرأس شعارك.</span><span class="sxs-lookup"><span data-stu-id="7af27-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7af27-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7af27-125">Additional resources</span></span>

[<span data-ttu-id="7af27-126">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="7af27-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="7af27-127">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="7af27-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="7af27-128">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="7af27-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7af27-129">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="7af27-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7af27-130">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="7af27-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="7af27-131">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="7af27-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="7af27-132">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="7af27-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
