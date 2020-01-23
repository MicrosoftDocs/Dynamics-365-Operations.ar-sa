---
title: إضافة إشعار لحقوق النشر
description: يصف هذا الموضوع كيفية إضافة إشعار لحقوق النشر إلى موقع ويب e-Commerce.
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914552"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="ce724-103">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="ce724-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ce724-104">يصف هذا الموضوع كيفية إضافة إشعار لحقوق النشر إلى موقع ويب e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="ce724-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ce724-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ce724-105">Prerequisites</span></span>

<span data-ttu-id="ce724-106">قبل أن تتمكن من إضافة إشعار حقوق النشر إلى موقعك، يجب أن يكون لديك الأصناف التالية:</span><span class="sxs-lookup"><span data-stu-id="ce724-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="ce724-107">قالب يتضمن جزء تذييل مشترك.</span><span class="sxs-lookup"><span data-stu-id="ce724-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="ce724-108">صحفة تستخدم هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="ce724-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="ce724-109">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="ce724-109">Add a copyright notice</span></span>

<span data-ttu-id="ce724-110">لإضافة إشعار حقوق نشر إلى أسفل كل صفحة تستخدم قالبًا معينًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ce724-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="ce724-111">انتقل إلى **الأجزاء**، ثم حدد **جزء صفحة جديد**.</span><span class="sxs-lookup"><span data-stu-id="ce724-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ce724-112">في مربع الحوار، حدد الوحدة النمطية **لتذييل الصفحة** ، ثم قم بتسمية الجزء.</span><span class="sxs-lookup"><span data-stu-id="ce724-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="ce724-113">على سبيل المثال، ادخل **حقوق نشر تذييل الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="ce724-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="ce724-114">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ce724-114">Select **OK**.</span></span>
1. <span data-ttu-id="ce724-115">في جزء التنقل، حدد زر علامة الحذف (**...**) بجوار **تذييل الصفحة**، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="ce724-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ce724-116">في مربع الحوار، حدد **فئة تذييل الصفحة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ce724-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="ce724-117">في جزء التنقل، حدد زر علامة الحذف بجوار **فئة التذييل**، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="ce724-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ce724-118">في مربع الحوار، حدد **عنصر كتلة منسقة للمحتوى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ce724-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="ce724-119">في جزء التنقل، حدد **عنصر كتلة تنسيق المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="ce724-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="ce724-120">في جزء الخصائص الموجود على الجانب الأيمن، في حقل **الفقرة** ، قم بإضافة رسالة حقوق النشر الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="ce724-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="ce724-121">على سبيل المثال، ادخل **(C) شركة الاتحاد للتصنيع 2019**.</span><span class="sxs-lookup"><span data-stu-id="ce724-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="ce724-122">حدد **حفظ**، ثم حدد **إيداع**، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="ce724-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="ce724-123">انتقل إلى **القوالب**، حدد القالب، ثم حدد **السحب**.</span><span class="sxs-lookup"><span data-stu-id="ce724-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="ce724-124">تحت **المخطط التفصيلي للصفحة**، ثم بتوسيع **النص الأصلي**، ثم قم بتوسيع **الصفحة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="ce724-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="ce724-125">حدد زر علامة الحذف الموجود بجوار **فتحة تذييل الصفحة**، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="ce724-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="ce724-126">حدد الجزء الذي قمت بإنشائه سابقًا، ثم حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="ce724-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="ce724-127">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="ce724-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="ce724-128">يظهر التذييل الذي يحتوي على إشعار حقوق النشر تلقائيًا في أسفل كافة الصفحات التي تستخدم القالب المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ce724-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce724-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ce724-129">Additional resources</span></span>

[<span data-ttu-id="ce724-130">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="ce724-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ce724-131">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="ce724-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ce724-132">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="ce724-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="ce724-133">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="ce724-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ce724-134">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="ce724-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="ce724-135">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="ce724-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="ce724-136">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ce724-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
