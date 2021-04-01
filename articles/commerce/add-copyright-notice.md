---
title: إضافة إشعار لحقوق النشر
description: يصف هذا الموضوع كيفية إضافة إشعار لحقوق النشر إلى موقع ويب e-Commerce.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206357"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="3b941-103">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="3b941-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b941-104">يصف هذا الموضوع كيفية إضافة إشعار لحقوق النشر إلى موقع ويب e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b941-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b941-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="3b941-105">Prerequisites</span></span>

<span data-ttu-id="3b941-106">قبل أن تتمكن من إضافة إشعار حقوق النشر إلى موقعك، يجب أن يكون لديك الأصناف التالية:</span><span class="sxs-lookup"><span data-stu-id="3b941-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="3b941-107">قالب يتضمن جزء تذييل مشترك.</span><span class="sxs-lookup"><span data-stu-id="3b941-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="3b941-108">صحفة تستخدم هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="3b941-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="3b941-109">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="3b941-109">Add a copyright notice</span></span>

<span data-ttu-id="3b941-110">لإضافة إشعار حقوق نشر إلى أسفل كل صفحة تستخدم قالبًا معينًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3b941-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="3b941-111">انتقل إلى **الأجزاء**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="3b941-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="3b941-112">في مربع الحوار **جزء جديد**، حدد وحدة **التذييل** واسم الجزء.</span><span class="sxs-lookup"><span data-stu-id="3b941-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="3b941-113">على سبيل المثال، ادخل **حقوق نشر تذييل الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="3b941-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="3b941-114">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3b941-114">Select **OK**.</span></span>
1. <span data-ttu-id="3b941-115">في جزء التنقل، حدد زر علامة الحذف (**...**) بجوار **تذييل الصفحة**، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="3b941-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3b941-116">في مربع الحوار، حدد **فئة تذييل الصفحة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3b941-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b941-117">في جزء التنقل، حدد زر علامة الحذف بجوار **فئة التذييل**، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="3b941-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3b941-118">في مربع الحوار، حدد **كتلة نص**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3b941-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b941-119">في جزء التنقل، حدد **كتلة نص**.</span><span class="sxs-lookup"><span data-stu-id="3b941-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="3b941-120">في جزء الخصائص الموجود على الجانب الأيمن، في حقل **الفقرة** ، قم بإضافة رسالة حقوق النشر الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3b941-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="3b941-121">على سبيل المثال، ادخل **(C) شركة الاتحاد للتصنيع 2019**.</span><span class="sxs-lookup"><span data-stu-id="3b941-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="3b941-122">حدد **حفظ**، حدد **إنهاء التحرير**، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="3b941-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="3b941-123">اذهب إلى **القوالب**، وحدد القالب، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="3b941-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="3b941-124">تحت **المخطط التفصيلي للصفحة**، ثم بتوسيع **النص الأساسي**، ثم قم بتوسيع **الصفحة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="3b941-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="3b941-125">حدد زر علامة الحذف الموجود بجوار **فتحة تذييل الصفحة**، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="3b941-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="3b941-126">حدد الجزء الذي قمت بإنشائه سابقًا، ثم حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="3b941-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="3b941-127">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="3b941-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3b941-128">يظهر التذييل الذي يحتوي على إشعار حقوق النشر تلقائيًا في أسفل كافة الصفحات التي تستخدم القالب المُحدد.</span><span class="sxs-lookup"><span data-stu-id="3b941-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b941-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3b941-129">Additional resources</span></span>

[<span data-ttu-id="3b941-130">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="3b941-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3b941-131">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="3b941-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3b941-132">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="3b941-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3b941-133">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="3b941-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3b941-134">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="3b941-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3b941-135">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="3b941-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3b941-136">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="3b941-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]