---
title: الوحدة النمطية لتذييل الصفحة
description: يغطي هذا الموضوع الوحدات النمطية لتذييل الصفحة وكيفية تأليفها في Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e81617979a945274500c9f4ceaa8078d8dfd79e8
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686684"
---
# <a name="footer-module"></a><span data-ttu-id="f141a-103">الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="f141a-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="f141a-104">يغطي هذا الموضوع الوحدات النمطية لتذييل الصفحات ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f141a-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f141a-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="f141a-105">Overview</span></span>

<span data-ttu-id="f141a-106">الوحدة النمطية لتذييل الصفحة هي حاوية خاصة تُستخدم لاستضافة الوحدات النمطية التي تظهر في تذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f141a-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="f141a-107">علي سبيل المثال، يمكن أن تتضمن ارتباطات إلى العديد من الصفحات عبر الموقع، مثل صفحات **اتصل بنا** و **سياسات المتجر** .</span><span class="sxs-lookup"><span data-stu-id="f141a-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="f141a-108">تعرض الصورة التالية مثالاً عن وحدة تذييل في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="f141a-108">The following image shows an example of a footer module on a site page.</span></span>

![مثال عن وحدة تذييل](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="f141a-110">خصائص الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="f141a-110">Footer module properties</span></span> 

<span data-ttu-id="f141a-111">مثل معظم الحاويات، تدعم وحدة التذييل خصائص الرأس والعرض.</span><span class="sxs-lookup"><span data-stu-id="f141a-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="f141a-112">كما أنه يدعم إضافة الوحدات النمطية لفئات التذييل المتعددة.</span><span class="sxs-lookup"><span data-stu-id="f141a-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="f141a-113">يتم عرض كل وحده نمطيه للفئة التي تتم إضافتها كعمود في الوحدة النمطية لتذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f141a-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="f141a-114">الوحدات النمطية المتوفرة في الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="f141a-114">Modules available in a footer module</span></span>

<span data-ttu-id="f141a-115">**عناصر تذييل الصفحة** – يمكن أن تحتوي الوحدة النمطية لعناصر التذييل علي عنوان وصوره وارتباط.</span><span class="sxs-lookup"><span data-stu-id="f141a-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="f141a-116">يمكن استخدام العنوان بمفرده أو مع الصور والارتباط.</span><span class="sxs-lookup"><span data-stu-id="f141a-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="f141a-117">يمكن تكوين كل ارتباط في التذييل بحيث يحتوي على نص فقط (علي سبيل المثال، ارتباطات "اتصل بنا" و "الخصوصية")، أو بحيث يحتوي علي كل من نص وصورة (علي سبيل المثال، ارتباطات الوسائط الاجتماعية).</span><span class="sxs-lookup"><span data-stu-id="f141a-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="f141a-118">**العودة إلى الأعلى** - توفر الوحدة النمطية العودة إلى الأعلى ارتباطًا للتنقل السريع إلى أعلي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f141a-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="f141a-119">الوجهة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f141a-119">A destination is required.</span></span> <span data-ttu-id="f141a-120">القيمة الافتراضية للوجهة هي \#، التي تأخذ المستخدم إلى أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f141a-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="f141a-121">إنشاء وحدة نمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="f141a-121">Create a footer module</span></span>

1. <span data-ttu-id="f141a-122">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="f141a-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f141a-123">في مربع الحوار **جزء الصفحة الجديد**، حدد وحدة **الحاوية**، وأدخل اسمًا لجزء الصفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f141a-123">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f141a-124">في فتحة **الحاوية الافتراضية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="f141a-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f141a-125">في مربع الحوار **إضافة وحدة**، حدد وحدة **فئة التذييل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f141a-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f141a-126">في فتحة **فئة التذييل‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="f141a-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f141a-127">في مربع الحوار **إضافة وحدة**، حدد وحدة **عنصر التذييل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f141a-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f141a-128">حدد فتحة **عنصر التذييل**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتكوين العنوان والارتباط ونص الارتباط والصورة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="f141a-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="f141a-129">لإضافة المزيد من عناصر التذييل، كرر الخطوات من 5 إلى 7 لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="f141a-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="f141a-130">لإضافة ارتباط ‬‏‫"العودة إلى الأعلى" إلى التذييل، حدد علامة القطع (**‎...**) في فتحة **فئة التذييل**، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="f141a-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f141a-131">في مربع الحوار **إضافة وحدة**، حدد الوحدة ‬‏‫**العودة إلى الأعلى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f141a-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f141a-132">حدد فتحة **العودة إلى الأعلى**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتكوين النص وخصائص أخرى للوحدة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="f141a-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="f141a-133">حدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="f141a-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f141a-134">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="f141a-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f141a-135">في فتحة **التذييل** في وحدة **الصفحة الافتراضية**، أضف جزء التذييل الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="f141a-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f141a-136">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="f141a-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f141a-137">بإضافة جزء الصفحة إلى قوالب الصفحة، فإنك تساعد في ضمان عرض تذييل الصفحة في كل صفحة.</span><span class="sxs-lookup"><span data-stu-id="f141a-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f141a-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f141a-138">Additional resources</span></span>

[<span data-ttu-id="f141a-139">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="f141a-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f141a-140">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="f141a-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f141a-141">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="f141a-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f141a-142">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="f141a-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f141a-143">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="f141a-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f141a-144">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="f141a-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f141a-145">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="f141a-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f141a-146">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="f141a-146">Footer module</span></span>](author-footer-module.md)
