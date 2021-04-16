---
title: تحديد سمة الموقع
description: يصف هذا الموضوع كيفية تعيين أو تغيير سمة خاصة بموقعك في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794057"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="7f17a-103">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="7f17a-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f17a-104">يصف هذا الموضوع كيفية تعيين أو تغيير سمة خاصة بموقعك في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f17a-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f17a-105">يتم تحديد تخطيط الموقع ونمطه (على سبيل المثال، الخطوط والأحجام والألوان) بواسطة السمة التي تحددها ويتم تطبيقها على الموقع.</span><span class="sxs-lookup"><span data-stu-id="7f17a-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="7f17a-106">يتم إنشاء السمة ونشرها من قبل مطور يعمل في شركتك.</span><span class="sxs-lookup"><span data-stu-id="7f17a-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="7f17a-107">للحصول على نظرة عامة حول السمات، راجع [نظرة عامة حول السمات](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="7f17a-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="7f17a-108">لمزيد من المعلومات حول كيفية إنشاء السمات ونشرها، راجع [إنشاء سمة جديدة](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="7f17a-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="7f17a-109">بشكل افتراضي، عندما تقوم بإنشاء موقع للمرة الأولى، فإنه يستخدم سمة تُسمى **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="7f17a-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="7f17a-110">يتم توفير هذا النسق الافتراضي كجزء من مكتبة الوحدات النمطية في Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f17a-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="7f17a-111">بعد قيامك بتوزيع سمات إضافية للموقع الخاص بك، فإنه يمكنك تكوين الموقع بحيث يستخدم إحدى السمتين بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="7f17a-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="7f17a-112">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="7f17a-112">Select the site theme</span></span>

<span data-ttu-id="7f17a-113">لتحديد السمة المطبقة على موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="7f17a-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="7f17a-114">في بيئة التأليف الخاصة بالموقع، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="7f17a-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="7f17a-115">انتقل إلى **إدارة الموقع** \> **قابلية التوسعة**.</span><span class="sxs-lookup"><span data-stu-id="7f17a-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="7f17a-116">ضمن **السمة**، حدد سمة من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="7f17a-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="7f17a-117">لتطبيق السمة المحددة على الموقع الخاص بك، حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="7f17a-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="7f17a-118">يتم نشر السمة التي تحددها على موقعك بمجرد تحديد **حفظ ونشر** في الصفحة **قابلية التوسعة**.</span><span class="sxs-lookup"><span data-stu-id="7f17a-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="7f17a-119">لمعاينة سمة على موقعك قبل تطبيقها، يمكنك استخدام بيئة التطوير أو وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="7f17a-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f17a-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7f17a-120">Additional resources</span></span>

[<span data-ttu-id="7f17a-121">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="7f17a-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="7f17a-122">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="7f17a-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="7f17a-123">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="7f17a-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7f17a-124">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="7f17a-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7f17a-125">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="7f17a-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="7f17a-126">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="7f17a-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="7f17a-127">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="7f17a-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="7f17a-128">نظرة عامة على النُسق</span><span class="sxs-lookup"><span data-stu-id="7f17a-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="7f17a-129">إنشاء سمة جديدة</span><span class="sxs-lookup"><span data-stu-id="7f17a-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
