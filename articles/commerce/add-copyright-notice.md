---
title: إضافة إشعار لحقوق النشر
description: يصف هذا الموضوع كيفية إضافة إشعار لحقوق النشر إلى موقع ويب e-Commerce.
author: psimolin
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: a2ed52dbd19508e07fcced92a7fad831180b1d1d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269580"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="d6cea-103">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="d6cea-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6cea-104">يصف هذا الموضوع كيفية إضافة إشعار لحقوق النشر إلى موقع ويب e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6cea-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d6cea-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="d6cea-105">Prerequisites</span></span>

<span data-ttu-id="d6cea-106">قبل أن تتمكن من إضافة إشعار حقوق النشر إلى موقعك، يجب أن يكون لديك الأصناف التالية:</span><span class="sxs-lookup"><span data-stu-id="d6cea-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="d6cea-107">قالب يتضمن جزء تذييل مشترك.</span><span class="sxs-lookup"><span data-stu-id="d6cea-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="d6cea-108">صحفة تستخدم هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d6cea-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="d6cea-109">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="d6cea-109">Add a copyright notice</span></span>

<span data-ttu-id="d6cea-110">لإضافة إشعار حقوق نشر إلى أسفل كل صفحة تستخدم قالبًا معينًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d6cea-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="d6cea-111">انتقل إلى **الأجزاء**، ثم حدد **جزء صفحة جديد**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="d6cea-112">في مربع الحوار، حدد الوحدة النمطية **لتذييل الصفحة** ، ثم قم بتسمية الجزء.</span><span class="sxs-lookup"><span data-stu-id="d6cea-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="d6cea-113">على سبيل المثال، ادخل **حقوق نشر تذييل الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="d6cea-114">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-114">Select **OK**.</span></span>
1. <span data-ttu-id="d6cea-115">في جزء التنقل، حدد زر علامة الحذف (**...**) بجوار **تذييل الصفحة**، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6cea-116">في مربع الحوار، حدد **فئة تذييل الصفحة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="d6cea-117">في جزء التنقل، حدد زر علامة الحذف بجوار **فئة التذييل**، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6cea-118">في مربع الحوار، حدد **كتلة نص**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="d6cea-119">في جزء التنقل، حدد **كتلة نص**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="d6cea-120">في جزء الخصائص الموجود على الجانب الأيمن، في حقل **الفقرة** ، قم بإضافة رسالة حقوق النشر الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d6cea-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="d6cea-121">على سبيل المثال، ادخل **(C) شركة الاتحاد للتصنيع 2019**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="d6cea-122">حدد **حفظ**، حدد **إنهاء التحرير**، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="d6cea-123">اذهب إلى **القوالب**، وحدد القالب، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="d6cea-124">تحت **المخطط التفصيلي للصفحة**، ثم بتوسيع **النص الأساسي**، ثم قم بتوسيع **الصفحة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="d6cea-125">حدد زر علامة الحذف الموجود بجوار **فتحة تذييل الصفحة**، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="d6cea-126">حدد الجزء الذي قمت بإنشائه سابقًا، ثم حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="d6cea-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="d6cea-127">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="d6cea-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="d6cea-128">يظهر التذييل الذي يحتوي على إشعار حقوق النشر تلقائيًا في أسفل كافة الصفحات التي تستخدم القالب المُحدد.</span><span class="sxs-lookup"><span data-stu-id="d6cea-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6cea-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d6cea-129">Additional resources</span></span>

[<span data-ttu-id="d6cea-130">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="d6cea-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d6cea-131">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="d6cea-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d6cea-132">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="d6cea-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d6cea-133">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="d6cea-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d6cea-134">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="d6cea-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d6cea-135">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="d6cea-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d6cea-136">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="d6cea-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

