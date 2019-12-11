---
title: إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx/5xx
description: يوضح هذا الموضوع كيفية إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx و5xx باستخدام أدوات التأليف في Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697096"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="fbc35-103">إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="fbc35-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fbc35-104">يوضح هذا الموضوع كيفية إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx و5xx باستخدام أدوات التأليف في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbc35-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fbc35-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="fbc35-105">Overview</span></span>

<span data-ttu-id="fbc35-106">في حالة عدم نجاح أحد الطلبات، يقوم الخادم بإصدار استجابات خطأ رمز الحالة HTTP.</span><span class="sxs-lookup"><span data-stu-id="fbc35-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="fbc35-107">يتم التقاط رمز الحالة 404 وإرجاعه إذا لم يتم العثور علي الصفحة، ويتم التقاط رمز الحالة 500 وإرجاعه في حالة حدوث خطأ بالخادم.</span><span class="sxs-lookup"><span data-stu-id="fbc35-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="fbc35-108">في Dynamics 365 Commerce، يمكن لمستخدمي التطبيق بناء صفحات استجابة خطأ مخصصة لرمز الحالة التي تظهر للمستخدمين لاستجابات خطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="fbc35-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="fbc35-109">إنشاء صفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="fbc35-109">Build a status code error response page</span></span>

<span data-ttu-id="fbc35-110">لبدء إنشاء صفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fbc35-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="fbc35-111">في متصفح الويب المفضل لديك، سجّل الدخول إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbc35-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="fbc35-112">حدد الموقع الذي تريد إنشاء صفحة استجابة لخطأ رمز الحالة 4xx/5xx له.</span><span class="sxs-lookup"><span data-stu-id="fbc35-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="fbc35-113">إنشاء القالب</span><span class="sxs-lookup"><span data-stu-id="fbc35-113">Build the template</span></span>

<span data-ttu-id="fbc35-114">لإنشاء قالب لصفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fbc35-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="fbc35-115">انتقل إلي **قوالب \> قالب جديد**.</span><span class="sxs-lookup"><span data-stu-id="fbc35-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="fbc35-116">اسم القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="fbc35-116">Name the new template.</span></span>
1. <span data-ttu-id="fbc35-117">قم بإنشاء القالب، استنادًا إلى البنية التي تريدها لصفحة استجابة خطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="fbc35-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="fbc35-118">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="fbc35-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="fbc35-119">إنشاء صفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="fbc35-119">Build the status code error response page</span></span>

<span data-ttu-id="fbc35-120">لإنشاء صفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fbc35-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="fbc35-121">انتقل إلى **صفحات \> صفحة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="fbc35-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="fbc35-122">قم بتسمية صفحة استجابة خطأ رمز الحالة، ولكن **لا** تقم بتعيين حقل **URL**.</span><span class="sxs-lookup"><span data-stu-id="fbc35-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="fbc35-123">إنشاء الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fbc35-123">Build the page.</span></span>
1. <span data-ttu-id="fbc35-124">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="fbc35-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="fbc35-125">يمكنك إنشاء صفحات استجابة خطأ رمز حالة منفصلة لأخطاء رمز الحالة 4xx و 5xx.</span><span class="sxs-lookup"><span data-stu-id="fbc35-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="fbc35-126">بدلاً من ذلك، يمكنك استخدام صفحة استجابة خطأ رمز الحالة العامة لفئتي الخطأ.</span><span class="sxs-lookup"><span data-stu-id="fbc35-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="fbc35-127">قم بإعداد إعادة توجيه لصفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="fbc35-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="fbc35-128">لإعداد إعادة توجيه لصفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fbc35-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="fbc35-129">انتقل إلى **URLs \> جديد \> الاسم المستعار الجديد**، وحدد صفحة استجابة خطأ رمز الحالة التي قمت بإنشاءها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="fbc35-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="fbc35-130">في الحقل **الاسم المستعار** ، أدخل إما **الافتراضي-4xx** أو **الافتراضي-5xx**، وفقًا لصفحة استجابة خطأ رمز الحالة التي تقوم بإعداد إعادة توجيهها.</span><span class="sxs-lookup"><span data-stu-id="fbc35-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="fbc35-131">يتعين نشر هذه الأسماء المستعارة.</span><span class="sxs-lookup"><span data-stu-id="fbc35-131">These aliases must be published.</span></span> <span data-ttu-id="fbc35-132">وإلا، فلن تعمل إعادة التوجيه.</span><span class="sxs-lookup"><span data-stu-id="fbc35-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="fbc35-133">حدد **موافق** لتنفيذ الربط.</span><span class="sxs-lookup"><span data-stu-id="fbc35-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="fbc35-134">إذا كنت تستخدم صفحة استجابة واحدة لخطأ رمز الحالة لفئتي الخطأ، فكرر هذا الإجراء لربط اسم مستعار لفئة الخطأ الأخرى بالصفحة نفسها.</span><span class="sxs-lookup"><span data-stu-id="fbc35-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbc35-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fbc35-135">Additional resources</span></span>

[<span data-ttu-id="fbc35-136">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="fbc35-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="fbc35-137">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="fbc35-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="fbc35-138">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="fbc35-138">Create a page URL</span></span>](create-page-url.md)
