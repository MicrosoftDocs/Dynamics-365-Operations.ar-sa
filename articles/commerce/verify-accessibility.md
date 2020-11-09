---
title: التحقق من إمكانية الوصول إلى محتوى الصفحة
description: يصف هذا الموضوع كيفية التحقق من إمكانية الوصول إلى محتوى الصفحة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fc3dca673510e1636f497bb7d5c295bebe025677
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015093"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="0f237-103">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="0f237-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0f237-104">يصف هذا الموضوع كيفية التحقق من إمكانية الوصول إلى محتوى الصفحة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f237-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0f237-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="0f237-105">Overview</span></span>

<span data-ttu-id="0f237-106">عند الانتهاء من تغيير صفحة، فإنه يجب عليك التأكد من إمكانية الوصول إلى المحتوى لكل شخص على الويب.</span><span class="sxs-lookup"><span data-stu-id="0f237-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="0f237-107">في أدوات التأليف الخاصة بـ Commerce، يمكنك بسهولة التحقق من إمكانية الوصول إلى محتوى الصفحة باستخدام خدمة [Microsoft Accessibility Insights](https://accessibilityinsights.io/) المتكاملة.</span><span class="sxs-lookup"><span data-stu-id="0f237-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="0f237-108">تتحقق هذه الخدمة من محتوى الصفحة الخاص بك بالمقارنة مع أحدث إرشادات [إمكانية الوصول التي وضعتها جمعية شبكة الإنترنت العالمية (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="0f237-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="0f237-109">يجب تشغيل دمج [Microsoft Accessibility Insights](https://accessibilityinsights.io/) على مستوى المستأجر أو الموقع قبل أن تتمكن من استخدامه.</span><span class="sxs-lookup"><span data-stu-id="0f237-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="0f237-110">تشغيل Microsoft Accessibility Insights لكافة المواقع في المستأجر الخاص بك</span><span class="sxs-lookup"><span data-stu-id="0f237-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="0f237-111">لتشغيل تكامل [Microsoft Accessibility Insights](https://accessibilityinsights.io/) لكافة مواقع Commerce في المستأجر الخاص بك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0f237-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="0f237-112">للوصول إلى إعدادات المستأجر، فإنه يجب أن تقوم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="0f237-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="0f237-113">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="0f237-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="0f237-114">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="0f237-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="0f237-115">ضمن **إعدادات المستأجر** ، حدد **الميزات**.</span><span class="sxs-lookup"><span data-stu-id="0f237-115">Under **Tenant Settings** , select **Features**.</span></span>
1. <span data-ttu-id="0f237-116">قم بتعيين خيار **التحقق من إمكانية الوصول** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0f237-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="0f237-117">تشغيل Microsoft Accessibility Insights لموقع واحد</span><span class="sxs-lookup"><span data-stu-id="0f237-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="0f237-118">لتشغيل تكامل [Microsoft Accessibility Insights](https://accessibilityinsights.io/) لموقع Commerce واحد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0f237-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="0f237-119">تحت **المواقع** ، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="0f237-119">Under **Sites** , select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0f237-120">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="0f237-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="0f237-121">ضمن **إعدادات الموقع** ، حدد **الميزات**.</span><span class="sxs-lookup"><span data-stu-id="0f237-121">Under **Site Settings** , select **Features**.</span></span>
1. <span data-ttu-id="0f237-122">قم بتعيين خيار **التحقق من إمكانية الوصول** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0f237-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="0f237-123">التحقق من إمكانية الوصول إلى المحتوى على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="0f237-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="0f237-124">لاستخدام خدمة [Microsoft Accessibility Insights](https://accessibilityinsights.io/) المتكاملة لفحص محتوى الصفحة الرئيسية في Commerce والتحقق من صحته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0f237-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0f237-125">تحت **المواقع** ، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="0f237-125">Under **Sites** , select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0f237-126">في جزء التنقل الأيسر، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="0f237-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="0f237-127">ابحث عن الصفحة الرئيسية وحددها لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0f237-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0f237-128">في شريط الأوامر، حدد **التحقق من إمكانية الوصول**.</span><span class="sxs-lookup"><span data-stu-id="0f237-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="0f237-129">تظهر صفحة **التحقق من إمكانية الوصول**.</span><span class="sxs-lookup"><span data-stu-id="0f237-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="0f237-130">بعد اكتمال الفحص، راجع محتويات التقرير.</span><span class="sxs-lookup"><span data-stu-id="0f237-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="0f237-131">إذا فشلت أية عمليات فحص، حدد كل عنصر تحقق تم فشله لتوسيعه بحيث يمكنك عرض مزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="0f237-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="0f237-132">لإغلاق التقرير بعد الانتهاء من مراجعته، قم بالتمرير إلى أسفل الصفحة **التحقق من إمكانية الوصول** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0f237-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f237-133">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0f237-133">Additional resources</span></span>

[<span data-ttu-id="0f237-134">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="0f237-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0f237-135">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="0f237-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0f237-136">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="0f237-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0f237-137">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="0f237-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0f237-138">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="0f237-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0f237-139">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="0f237-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0f237-140">إثراء الصفحة المتنقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="0f237-140">Enrich a category landing page</span></span>](enrich-category-page.md)
