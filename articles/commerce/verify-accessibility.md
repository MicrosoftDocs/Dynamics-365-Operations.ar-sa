---
title: التحقق من إمكانية الوصول إلى محتوى الصفحة
description: يصف هذا الموضوع كيفية التحقق من إمكانية الوصول إلى محتوى الصفحة في Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791621"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="e3379-103">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="e3379-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3379-104">يصف هذا الموضوع كيفية التحقق من إمكانية الوصول إلى محتوى الصفحة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3379-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e3379-105">عند الانتهاء من تغيير صفحة، فإنه يجب عليك التأكد من إمكانية الوصول إلى المحتوى لكل شخص على الويب.</span><span class="sxs-lookup"><span data-stu-id="e3379-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="e3379-106">في أدوات التأليف الخاصة بـ Commerce، يمكنك بسهولة التحقق من إمكانية الوصول إلى محتوى الصفحة باستخدام خدمة [Microsoft Accessibility Insights](https://accessibilityinsights.io/) المتكاملة.</span><span class="sxs-lookup"><span data-stu-id="e3379-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="e3379-107">تتحقق هذه الخدمة من محتوى الصفحة الخاص بك بالمقارنة مع أحدث إرشادات [إمكانية الوصول التي وضعتها جمعية شبكة الإنترنت العالمية (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="e3379-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="e3379-108">يجب تشغيل دمج [Microsoft Accessibility Insights](https://accessibilityinsights.io/) على مستوى المستأجر أو الموقع قبل أن تتمكن من استخدامه.</span><span class="sxs-lookup"><span data-stu-id="e3379-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="e3379-109">تشغيل Microsoft Accessibility Insights لكافة المواقع في المستأجر الخاص بك</span><span class="sxs-lookup"><span data-stu-id="e3379-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="e3379-110">لتشغيل تكامل [Microsoft Accessibility Insights](https://accessibilityinsights.io/) لكافة مواقع Commerce في المستأجر الخاص بك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e3379-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="e3379-111">للوصول إلى إعدادات المستأجر، فإنه يجب أن تقوم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="e3379-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="e3379-112">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="e3379-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="e3379-113">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="e3379-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="e3379-114">ضمن **إعدادات المستأجر**، حدد **الميزات**.</span><span class="sxs-lookup"><span data-stu-id="e3379-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="e3379-115">قم بتعيين خيار **التحقق من إمكانية الوصول** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="e3379-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="e3379-116">تشغيل Microsoft Accessibility Insights لموقع واحد</span><span class="sxs-lookup"><span data-stu-id="e3379-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="e3379-117">لتشغيل تكامل [Microsoft Accessibility Insights](https://accessibilityinsights.io/) لموقع Commerce واحد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e3379-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="e3379-118">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="e3379-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e3379-119">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="e3379-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="e3379-120">ضمن **إعدادات الموقع**، حدد **الميزات**.</span><span class="sxs-lookup"><span data-stu-id="e3379-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="e3379-121">قم بتعيين خيار **التحقق من إمكانية الوصول** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="e3379-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="e3379-122">التحقق من إمكانية الوصول إلى المحتوى على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="e3379-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="e3379-123">لاستخدام خدمة [Microsoft Accessibility Insights](https://accessibilityinsights.io/) المتكاملة لفحص محتوى الصفحة الرئيسية في Commerce والتحقق من صحته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e3379-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e3379-124">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="e3379-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e3379-125">في جزء التنقل الأيسر، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="e3379-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="e3379-126">ابحث عن الصفحة الرئيسية وحددها لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e3379-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="e3379-127">في شريط الأوامر، حدد **التحقق من إمكانية الوصول**.</span><span class="sxs-lookup"><span data-stu-id="e3379-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="e3379-128">تظهر صفحة **التحقق من إمكانية الوصول**.</span><span class="sxs-lookup"><span data-stu-id="e3379-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="e3379-129">بعد اكتمال الفحص، راجع محتويات التقرير.</span><span class="sxs-lookup"><span data-stu-id="e3379-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="e3379-130">إذا فشلت أية عمليات فحص، حدد كل عنصر تحقق تم فشله لتوسيعه بحيث يمكنك عرض مزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="e3379-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="e3379-131">لإغلاق التقرير بعد الانتهاء من مراجعته، قم بالتمرير إلى أسفل الصفحة **التحقق من إمكانية الوصول**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e3379-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3379-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e3379-132">Additional resources</span></span>

[<span data-ttu-id="e3379-133">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="e3379-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e3379-134">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="e3379-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e3379-135">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="e3379-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e3379-136">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="e3379-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e3379-137">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="e3379-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e3379-138">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="e3379-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e3379-139">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="e3379-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e3379-140">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="e3379-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
