---
title: الوحدة النمطية لتذييل الصفحة
description: يغطي هذا الموضوع الوحدات النمطية لتذييل الصفحة وكيفية تأليفها في Dynamics 365 Commerce.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979937"
---
# <a name="footer-module"></a><span data-ttu-id="2b085-103">الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2b085-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b085-104">يغطي هذا الموضوع الوحدات النمطية لتذييل الصفحات ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2b085-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b085-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2b085-105">Overview</span></span>

<span data-ttu-id="2b085-106">الوحدة النمطية لتذييل الصفحة هي حاوية خاصة تُستخدم لاستضافة الوحدات النمطية التي تظهر في تذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b085-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="2b085-107">على سبيل المثال، يمكن أن تتضمن ارتباطات إلى العديد من الصفحات عبر الموقع، مثل صفحات **اتصل بنا** و **سياسات المتجر** .</span><span class="sxs-lookup"><span data-stu-id="2b085-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="2b085-108">تعرض الصورة التالية مثالاً عن وحدة تذييل في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="2b085-108">The following image shows an example of a footer module on a site page.</span></span>

![مثال عن وحدة تذييل](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="2b085-110">خصائص الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2b085-110">Footer module properties</span></span> 

<span data-ttu-id="2b085-111">مثل معظم الحاويات، تدعم وحدة التذييل خصائص الرأس والعرض.</span><span class="sxs-lookup"><span data-stu-id="2b085-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="2b085-112">كما أنه يدعم إضافة الوحدات النمطية لفئات التذييل المتعددة.</span><span class="sxs-lookup"><span data-stu-id="2b085-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="2b085-113">يتم عرض كل وحده نمطيه للفئة التي تتم إضافتها كعمود في الوحدة النمطية لتذييل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b085-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="2b085-114">الوحدات النمطية المتوفرة في الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2b085-114">Modules available in a footer module</span></span>

<span data-ttu-id="2b085-115">**عناصر تذييل الصفحة** – يمكن أن تحتوي الوحدة النمطية لعناصر التذييل على عنوان وصوره وارتباط.</span><span class="sxs-lookup"><span data-stu-id="2b085-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="2b085-116">يمكن استخدام العنوان بمفرده أو مع الصور والارتباط.</span><span class="sxs-lookup"><span data-stu-id="2b085-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="2b085-117">يمكن تكوين كل ارتباط في التذييل بحيث يحتوي على نص فقط (على سبيل المثال، ارتباطات "اتصل بنا" و "الخصوصية")، أو بحيث يحتوي على كل من نص وصورة (على سبيل المثال، ارتباطات الوسائط الاجتماعية).</span><span class="sxs-lookup"><span data-stu-id="2b085-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="2b085-118">**العودة إلى الأعلى** - توفر الوحدة النمطية العودة إلى الأعلى ارتباطًا للتنقل السريع إلى أعلي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b085-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="2b085-119">الوجهة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2b085-119">A destination is required.</span></span> <span data-ttu-id="2b085-120">القيمة الافتراضية للوجهة هي \#، التي تأخذ المستخدم إلى أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b085-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="2b085-121">إنشاء وحدة نمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="2b085-121">Create a footer module</span></span>

1. <span data-ttu-id="2b085-122">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="2b085-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2b085-123">في مربع الحوار **جزء جديد**، حدد وحدة **الحاوية**، وأدخل اسمًا للجزء، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b085-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2b085-124">في فتحة **الحاوية الافتراضية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2b085-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b085-125">في مربع الحوار **إضافة وحدة**، حدد وحدة **فئة التذييل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b085-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b085-126">في فتحة **فئة التذييل‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2b085-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b085-127">في مربع الحوار **إضافة وحدة**، حدد وحدة **عنصر التذييل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b085-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b085-128">حدد فتحة **عنصر التذييل**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتكوين العنوان والارتباط ونص الارتباط والصورة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="2b085-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="2b085-129">لإضافة المزيد من عناصر التذييل، كرر الخطوات من 5 إلى 7 لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="2b085-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="2b085-130">لإضافة ارتباط ‬‏‫"العودة إلى الأعلى" إلى التذييل، حدد علامة القطع (**‎...**) في فتحة **فئة التذييل**، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2b085-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b085-131">في مربع الحوار **إضافة وحدة**، حدد الوحدة ‬‏‫**العودة إلى الأعلى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b085-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b085-132">حدد فتحة **العودة إلى الأعلى**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتكوين النص وخصائص أخرى للوحدة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="2b085-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="2b085-133">حدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="2b085-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2b085-134">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="2b085-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2b085-135">في فتحة **التذييل** في وحدة **الصفحة الافتراضية**، أضف جزء التذييل الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="2b085-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="2b085-136">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="2b085-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2b085-137">من خلال إضافة جزء إلى قوالب الصفحة، فإنك تساعد في ضمان عرض التذييل على كل صفحة.</span><span class="sxs-lookup"><span data-stu-id="2b085-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b085-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2b085-138">Additional resources</span></span>

[<span data-ttu-id="2b085-139">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2b085-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2b085-140">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="2b085-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2b085-141">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="2b085-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2b085-142">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="2b085-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2b085-143">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="2b085-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2b085-144">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="2b085-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2b085-145">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="2b085-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2b085-146">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="2b085-146">Footer module</span></span>](author-footer-module.md)
