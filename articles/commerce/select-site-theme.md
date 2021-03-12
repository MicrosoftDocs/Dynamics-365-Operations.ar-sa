---
title: تحديد سمة الموقع
description: يصف هذا الموضوع كيفية تعيين أو تغيير سمة خاصة بموقعك في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982381"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="da1c9-103">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="da1c9-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da1c9-104">يصف هذا الموضوع كيفية تعيين أو تغيير سمة خاصة بموقعك في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da1c9-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da1c9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="da1c9-105">Overview</span></span>

<span data-ttu-id="da1c9-106">يتم تحديد تخطيط الموقع ونمطه (على سبيل المثال، الخطوط والأحجام والألوان) بواسطة السمة التي تحددها ويتم تطبيقها على الموقع.</span><span class="sxs-lookup"><span data-stu-id="da1c9-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="da1c9-107">يتم إنشاء السمة ونشرها من قبل مطور يعمل في شركتك.</span><span class="sxs-lookup"><span data-stu-id="da1c9-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="da1c9-108">للحصول على نظرة عامة حول السمات، راجع [نظرة عامة حول السمات](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="da1c9-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="da1c9-109">لمزيد من المعلومات حول كيفية إنشاء السمات ونشرها، راجع [إنشاء سمة جديدة](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="da1c9-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="da1c9-110">بشكل افتراضي، عندما تقوم بإنشاء موقع للمرة الأولى، فإنه يستخدم سمة تُسمى **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="da1c9-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="da1c9-111">يتم توفير هذا النسق الافتراضي كجزء من مكتبة الوحدات النمطية في Commerce.</span><span class="sxs-lookup"><span data-stu-id="da1c9-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="da1c9-112">بعد قيامك بتوزيع سمات إضافية للموقع الخاص بك، فإنه يمكنك تكوين الموقع بحيث يستخدم إحدى السمتين بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="da1c9-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="da1c9-113">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="da1c9-113">Select the site theme</span></span>

<span data-ttu-id="da1c9-114">لتحديد السمة المطبقة على موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="da1c9-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="da1c9-115">في بيئة التأليف الخاصة بالموقع، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="da1c9-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="da1c9-116">انتقل إلى **إدارة الموقع** \> **قابلية التوسعة**.</span><span class="sxs-lookup"><span data-stu-id="da1c9-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="da1c9-117">ضمن **السمة**، حدد سمة من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="da1c9-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="da1c9-118">لتطبيق السمة المحددة على الموقع الخاص بك، حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="da1c9-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="da1c9-119">يتم نشر السمة التي تحددها على موقعك بمجرد تحديد **حفظ ونشر** في الصفحة **قابلية التوسعة**.</span><span class="sxs-lookup"><span data-stu-id="da1c9-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="da1c9-120">لمعاينة سمة على موقعك قبل تطبيقها، يمكنك استخدام بيئة التطوير أو وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="da1c9-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da1c9-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="da1c9-121">Additional resources</span></span>

[<span data-ttu-id="da1c9-122">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="da1c9-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="da1c9-123">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="da1c9-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="da1c9-124">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="da1c9-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="da1c9-125">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="da1c9-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="da1c9-126">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="da1c9-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="da1c9-127">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="da1c9-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="da1c9-128">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="da1c9-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="da1c9-129">نظرة عامة على النُسق</span><span class="sxs-lookup"><span data-stu-id="da1c9-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="da1c9-130">إنشاء سمة جديدة</span><span class="sxs-lookup"><span data-stu-id="da1c9-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

