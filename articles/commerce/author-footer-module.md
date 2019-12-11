---
title: الوحدة النمطية لتذييل الصفحة
description: يغطي هذا الموضوع الوحدات النمطية لتذييل الصفحة وكيفية تأليفها في Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697303"
---
# <a name="footer-module"></a><span data-ttu-id="2a613-103">الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2a613-103">Footer module</span></span>  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2a613-104">يغطي هذا الموضوع الوحدات النمطية لتذييل الصفحات ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2a613-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2a613-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2a613-105">Overview</span></span>

<span data-ttu-id="2a613-106">الوحدة النمطية لتذييل الصفحة هي حاوية خاصة تُستخدم لاستضافة الوحدات النمطية التي تظهر في تذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2a613-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="2a613-107">علي سبيل المثال، يمكن أن تتضمن ارتباطات إلى العديد من الصفحات عبر الموقع، مثل صفحات **اتصل بنا** و **سياسات المتجر** .</span><span class="sxs-lookup"><span data-stu-id="2a613-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="2a613-108">خصائص الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2a613-108">Footer module properties</span></span> 

<span data-ttu-id="2a613-109">مثل معظم الحاويات، تدعم الوحدة النمطية لتذييل الصفحة خصائص العنوان والعرض.</span><span class="sxs-lookup"><span data-stu-id="2a613-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="2a613-110">كما أنه يدعم إضافة الوحدات النمطية لفئات التذييل المتعددة.</span><span class="sxs-lookup"><span data-stu-id="2a613-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="2a613-111">يتم عرض كل وحده نمطيه للفئة التي تتم إضافتها كعمود في الوحدة النمطية لتذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2a613-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="2a613-112">الوحدات النمطية المتوفرة في الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2a613-112">Modules available in a footer module</span></span>

<span data-ttu-id="2a613-113">**عناصر تذييل الصفحة** – يمكن أن تحتوي الوحدة النمطية لعناصر التذييل علي عنوان وصوره وارتباط.</span><span class="sxs-lookup"><span data-stu-id="2a613-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="2a613-114">يمكن استخدام العنوان بمفرده أو مع الصور والارتباط.</span><span class="sxs-lookup"><span data-stu-id="2a613-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="2a613-115">يمكن تكوين كل ارتباط في التذييل بحيث يحتوي على نص فقط (علي سبيل المثال، ارتباطات "اتصل بنا" و "الخصوصية")، أو بحيث يحتوي علي كل من نص وصورة (علي سبيل المثال، ارتباطات الوسائط الاجتماعية).</span><span class="sxs-lookup"><span data-stu-id="2a613-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="2a613-116">**العودة إلى الأعلى** - توفر الوحدة النمطية العودة إلى الأعلى ارتباطًا للتنقل السريع إلى أعلي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2a613-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="2a613-117">الوجهة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2a613-117">A destination is required.</span></span> <span data-ttu-id="2a613-118">القيمة الافتراضية للوجهة هي #، والتي تأخذ المستخدم إلى أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2a613-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="2a613-119">مؤلف الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2a613-119">Author a footer module</span></span>

1. <span data-ttu-id="2a613-120">في جزء التنقل، حدد **أجزاء**، ثم حدد **جزء صفحة جديد**.</span><span class="sxs-lookup"><span data-stu-id="2a613-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="2a613-121">في مربع الحوار **جزء الصفحة الجديد** ، حدد الوحدة النمطية لتذييل الصفحة، وأدخل اسمًا لجزء الصفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2a613-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2a613-122">في شجرة المخطط التفصيلي، حدد زر علامة الحذف (**...**) للوحدة النمطية لتذييل الصفحة، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="2a613-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a613-123">في مربع الحوار **إضافة وحدة نمطية** ، حدد الوحدة النمطية لفئة تذييل الصفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2a613-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="2a613-124">في شجرة المخطط التفصيلي، حدد زر علامة الحذف للوحدة النمطية لفئة تذييل الصفحة، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="2a613-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a613-125">في مربع الحوار **إضافة وحدة نمطية** ، حدد الوحدة النمطية لعنصر تذييل الصفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2a613-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="2a613-126">في شجره المخطط التفصيلي، حدد الوحدة النمطية لعنصر التذييل.</span><span class="sxs-lookup"><span data-stu-id="2a613-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="2a613-127">بعد ذلك، في جزء الخصائص الموجود علي اليمين، قم بتكوين العنوان وارتباط ونص الارتباط والصورة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="2a613-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="2a613-128">لإضافة المزيد من عناصر التذييل، كرر الخطوات من 5 إلى 7.</span><span class="sxs-lookup"><span data-stu-id="2a613-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="2a613-129">لإضافة ارتباط "‬‏‫العودة إلى الأعلى" للتذييل الخاص بك، حدد زر علامة الحذف للوحدة النمطية لفئة تذييل الصفحة، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="2a613-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a613-130">في مربع الحوار **إضافة وحدة نمطية** ، حدد الوحدة النمطية ‬‏‫العودة إلى الأعلى، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2a613-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="2a613-131">في شجرة المخطط التفصيلي، حدد الوحدة النمطية ‬‏‫العودة إلى الأعلى.</span><span class="sxs-lookup"><span data-stu-id="2a613-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="2a613-132">وبعد ذلك، في جزء الخصائص الموجود علي اليمين، قم بتكوين الوحدة النمطية ‬‏‫العودة إلى الأعلى على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="2a613-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="2a613-133">قم بحفظ جزء الصفحة، وإيداعه ونشره.</span><span class="sxs-lookup"><span data-stu-id="2a613-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="2a613-134">في كل قالب صفحة تم إنشاؤه للموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2a613-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="2a613-135">في الفتحة **الرئيسية** للصفحة الافتراضية، في الوحدة النمطية لتذييل الصفحة، أضف جزء التذييل الذي قمت بإنشاءه.</span><span class="sxs-lookup"><span data-stu-id="2a613-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="2a613-136">قم بحفظ القالب، وإيداعه ونشره.</span><span class="sxs-lookup"><span data-stu-id="2a613-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="2a613-137">بإضافة جزء الصفحة إلى قوالب الصفحة، فإنك تساعد في ضمان عرض تذييل الصفحة في كل صفحة.</span><span class="sxs-lookup"><span data-stu-id="2a613-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a613-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2a613-138">Additional resources</span></span>

[<span data-ttu-id="2a613-139">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="2a613-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2a613-140">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="2a613-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2a613-141">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="2a613-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2a613-142">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="2a613-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2a613-143">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="2a613-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2a613-144">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="2a613-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2a613-145">الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="2a613-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2a613-146">الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2a613-146">Footer module</span></span>](author-footer-module.md)
