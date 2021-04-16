---
title: إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx/5xx
description: يوضح هذا الموضوع كيفية إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx و5xx باستخدام أدوات التأليف في Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799627"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="e72cc-103">إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="e72cc-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e72cc-104">يوضح هذا الموضوع كيفية إنشاء صفحات استجابة مخصصة لأخطاء رمز الحالة 4xx و5xx باستخدام أدوات التأليف في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e72cc-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e72cc-105">في حالة عدم نجاح أحد الطلبات، يقوم الخادم بإصدار استجابات خطأ رمز الحالة HTTP.</span><span class="sxs-lookup"><span data-stu-id="e72cc-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="e72cc-106">يتم التقاط رمز الحالة 404 وإرجاعه إذا لم يتم العثور علي الصفحة، ويتم التقاط رمز الحالة 500 وإرجاعه في حالة حدوث خطأ بالخادم.</span><span class="sxs-lookup"><span data-stu-id="e72cc-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="e72cc-107">في Dynamics 365 Commerce، يمكن لمستخدمي التطبيق بناء صفحات استجابة خطأ مخصصة لرمز الحالة التي تظهر للمستخدمين لاستجابات خطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="e72cc-108">إنشاء صفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="e72cc-108">Build a status code error response page</span></span>

<span data-ttu-id="e72cc-109">لبدء إنشاء صفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e72cc-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="e72cc-110">في متصفح الويب المفضل لديك، سجّل الدخول إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e72cc-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="e72cc-111">حدد الموقع الذي تريد إنشاء صفحة استجابة لخطأ رمز الحالة 4xx/5xx له.</span><span class="sxs-lookup"><span data-stu-id="e72cc-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="e72cc-112">إنشاء القالب</span><span class="sxs-lookup"><span data-stu-id="e72cc-112">Build the template</span></span>

<span data-ttu-id="e72cc-113">لإنشاء قالب لصفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e72cc-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="e72cc-114">انتقل إلى **القوالب**.</span><span class="sxs-lookup"><span data-stu-id="e72cc-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="e72cc-115">حدد **جديد**، لإنشاء قالب صفحة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="e72cc-116">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل اسمًا لقالب جديد، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e72cc-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="e72cc-117">قم بإنشاء القالب، استنادًا إلى البنية التي تريدها لصفحة استجابة خطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="e72cc-118">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="e72cc-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="e72cc-119">إنشاء صفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="e72cc-119">Build the status code error response page</span></span>

<span data-ttu-id="e72cc-120">لإنشاء صفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e72cc-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="e72cc-121">انتقل إلى **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="e72cc-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="e72cc-122">حدد **جديد** لإنشاء صفحة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="e72cc-123">في مربع الحوار **اختيار قالب**، حدد أحد القوالب، ثم، تحت **اسم الصفحة**، أدخل اسمًا لصفحة الاستجابة لخطأ رمز الحالة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="e72cc-124">اترك حقل **عنوان URL للصفحة** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="e72cc-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="e72cc-125">إنشاء الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-125">Build the page.</span></span>
1. <span data-ttu-id="e72cc-126">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="e72cc-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="e72cc-127">يمكنك إنشاء صفحات استجابة خطأ رمز حالة منفصلة لأخطاء رمز الحالة 4xx و 5xx.</span><span class="sxs-lookup"><span data-stu-id="e72cc-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="e72cc-128">بدلاً من ذلك، يمكنك استخدام صفحة استجابة خطأ رمز الحالة العامة لفئتي الخطأ.</span><span class="sxs-lookup"><span data-stu-id="e72cc-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="e72cc-129">قم بإعداد إعادة توجيه لصفحة استجابة خطأ رمز الحالة</span><span class="sxs-lookup"><span data-stu-id="e72cc-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="e72cc-130">لإعداد إعادة توجيه لصفحة استجابة خطأ رمز الحالة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e72cc-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="e72cc-131">انتقل إلى **URLs \> جديد \> الاسم المستعار الجديد**، وحدد صفحة استجابة خطأ رمز الحالة التي قمت بإنشاءها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="e72cc-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="e72cc-132">في الحقل **الاسم المستعار** ، أدخل إما **الافتراضي-4xx** أو **الافتراضي-5xx**، وفقًا لصفحة استجابة خطأ رمز الحالة التي تقوم بإعداد إعادة توجيهها.</span><span class="sxs-lookup"><span data-stu-id="e72cc-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="e72cc-133">يتعين نشر هذه الأسماء المستعارة.</span><span class="sxs-lookup"><span data-stu-id="e72cc-133">These aliases must be published.</span></span> <span data-ttu-id="e72cc-134">وإلا، فلن تعمل إعادة التوجيه.</span><span class="sxs-lookup"><span data-stu-id="e72cc-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="e72cc-135">حدد **موافق** لتنفيذ الربط.</span><span class="sxs-lookup"><span data-stu-id="e72cc-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="e72cc-136">إذا كنت تستخدم صفحة استجابة واحدة لخطأ رمز الحالة لفئتي الخطأ، فكرر هذا الإجراء لربط اسم مستعار لفئة الخطأ الأخرى بالصفحة نفسها.</span><span class="sxs-lookup"><span data-stu-id="e72cc-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e72cc-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e72cc-137">Additional resources</span></span>

[<span data-ttu-id="e72cc-138">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="e72cc-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="e72cc-139">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="e72cc-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e72cc-140">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="e72cc-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
