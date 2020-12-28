---
title: إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx/5xx
description: يوضح هذا الموضوع كيفية إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx و5xx باستخدام أدوات التأليف في Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409861"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="28aef-103">إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="28aef-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="28aef-104">يوضح هذا الموضوع كيفية إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx و5xx باستخدام أدوات التأليف في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="28aef-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="28aef-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="28aef-105">Overview</span></span>

<span data-ttu-id="28aef-106">في حالة عدم نجاح أحد الطلبات، يقوم الخادم بإصدار استجابات خطأ رمز الحالة HTTP.</span><span class="sxs-lookup"><span data-stu-id="28aef-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="28aef-107">يتم التقاط رمز الحالة 404 وإرجاعه إذا لم يتم العثور علي الصفحة، ويتم التقاط رمز الحالة 500 وإرجاعه في حالة حدوث خطأ بالخادم.</span><span class="sxs-lookup"><span data-stu-id="28aef-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="28aef-108">في Dynamics 365 Commerce، يمكن لمستخدمي التطبيق بناء صفحات استجابة خطأ مخصصة لرمز الحالة التي تظهر للمستخدمين لاستجابات خطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="28aef-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="28aef-109">إنشاء صفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="28aef-109">Build a status code error response page</span></span>

<span data-ttu-id="28aef-110">لبدء إنشاء صفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="28aef-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="28aef-111">في متصفح الويب المفضل لديك، سجّل الدخول إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="28aef-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="28aef-112">حدد الموقع الذي تريد إنشاء صفحة استجابة لخطأ رمز الحالة 4xx/5xx له.</span><span class="sxs-lookup"><span data-stu-id="28aef-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="28aef-113">إنشاء القالب</span><span class="sxs-lookup"><span data-stu-id="28aef-113">Build the template</span></span>

<span data-ttu-id="28aef-114">لإنشاء قالب لصفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="28aef-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="28aef-115">انتقل إلى **القوالب**.</span><span class="sxs-lookup"><span data-stu-id="28aef-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="28aef-116">حدد **جديد**، لإنشاء قالب صفحة.</span><span class="sxs-lookup"><span data-stu-id="28aef-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="28aef-117">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل اسمًا لقالب جديد، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="28aef-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="28aef-118">قم بإنشاء القالب، استنادًا إلى البنية التي تريدها لصفحة استجابة خطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="28aef-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="28aef-119">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="28aef-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="28aef-120">إنشاء صفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="28aef-120">Build the status code error response page</span></span>

<span data-ttu-id="28aef-121">لإنشاء صفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="28aef-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="28aef-122">انتقل إلى **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="28aef-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="28aef-123">حدد **جديد** لإنشاء صفحة.</span><span class="sxs-lookup"><span data-stu-id="28aef-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="28aef-124">في مربع الحوار **اختيار قالب**، حدد أحد القوالب، ثم، تحت **اسم الصفحة**، أدخل اسمًا لصفحة الاستجابة لخطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="28aef-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="28aef-125">اترك حقل **عنوان URL للصفحة** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="28aef-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="28aef-126">إنشاء الصفحة.</span><span class="sxs-lookup"><span data-stu-id="28aef-126">Build the page.</span></span>
1. <span data-ttu-id="28aef-127">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="28aef-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="28aef-128">يمكنك إنشاء صفحات استجابة خطأ رمز حالة منفصلة لأخطاء رمز الحالة 4xx و 5xx.</span><span class="sxs-lookup"><span data-stu-id="28aef-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="28aef-129">بدلاً من ذلك، يمكنك استخدام صفحة استجابة خطأ رمز الحالة العامة لفئتي الخطأ.</span><span class="sxs-lookup"><span data-stu-id="28aef-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="28aef-130">قم بإعداد إعادة توجيه لصفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="28aef-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="28aef-131">لإعداد إعادة توجيه لصفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="28aef-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="28aef-132">انتقل إلى **URLs \> جديد \> الاسم المستعار الجديد**، وحدد صفحة استجابة خطأ رمز الحالة التي قمت بإنشاءها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="28aef-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="28aef-133">في الحقل **الاسم المستعار** ، أدخل إما **الافتراضي-4xx** أو **الافتراضي-5xx**، وفقًا لصفحة استجابة خطأ رمز الحالة التي تقوم بإعداد إعادة توجيهها.</span><span class="sxs-lookup"><span data-stu-id="28aef-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="28aef-134">يتعين نشر هذه الأسماء المستعارة.</span><span class="sxs-lookup"><span data-stu-id="28aef-134">These aliases must be published.</span></span> <span data-ttu-id="28aef-135">وإلا، فلن تعمل إعادة التوجيه.</span><span class="sxs-lookup"><span data-stu-id="28aef-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="28aef-136">حدد **موافق** لتنفيذ الربط.</span><span class="sxs-lookup"><span data-stu-id="28aef-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="28aef-137">إذا كنت تستخدم صفحة استجابة واحدة لخطأ رمز الحالة لفئتي الخطأ، فكرر هذا الإجراء لربط اسم مستعار لفئة الخطأ الأخرى بالصفحة نفسها.</span><span class="sxs-lookup"><span data-stu-id="28aef-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28aef-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="28aef-138">Additional resources</span></span>

[<span data-ttu-id="28aef-139">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="28aef-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="28aef-140">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="28aef-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="28aef-141">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="28aef-141">Create a page URL</span></span>](create-page-url.md)
