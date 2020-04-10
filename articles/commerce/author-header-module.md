---
title: وحدة الرأس
description: يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025638"
---
# <a name="header-module"></a><span data-ttu-id="1d668-103">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="1d668-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1d668-104">يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1d668-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d668-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1d668-105">Overview</span></span>

<span data-ttu-id="1d668-106">في Dynamics 365 Commerce، يتضمن رأس الصفحة وحدات متعددة، مثل وحدات الرأس وقائمة التنقل والبحث والشعار الترويجي والموافقة على ملف تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="1d668-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="1d668-107">تتضمن وحدة الرأس شعار الموقع وارتباطات إلى التدرج الهرمي للتنقل وارتباطات إلى صفحات أخرى في الموقع ورمز سلة التسوق ورمز قائمة الأمنيات وخيارات تسجيل الدخول وشريط البحث.</span><span class="sxs-lookup"><span data-stu-id="1d668-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="1d668-108">يتم تحسين وحدة الرأس بشكل تلقائي للجهاز الذي يتم عرض الموقع عليه (بمعنىً آخر لجهاز سطح المكتب أو جهاز محمول).</span><span class="sxs-lookup"><span data-stu-id="1d668-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="1d668-109">علي سبيل المثال، علي جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير*).</span><span class="sxs-lookup"><span data-stu-id="1d668-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="1d668-110">خصائص وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="1d668-110">Properties of a header module</span></span>

<span data-ttu-id="1d668-111">تدعم وحدة الرأس خصائص **صورة الشعار** و**ارتباط الشعار** و**ارتباطات حسابي**.</span><span class="sxs-lookup"><span data-stu-id="1d668-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="1d668-112">تُستخدم خصائص **صورة الشعار** و**ارتباط الشعار** لتعريف شعار على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1d668-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="1d668-113">لمزيد من المعلومات، راجع [إضافة شعار](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="1d668-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="1d668-114">يمكن استخدام الخاصية **ارتباطات حسابي** لتحديد صفحات الحساب التي يريد مالك الموقع عرض ارتباطات سريعة لها في الرأس.</span><span class="sxs-lookup"><span data-stu-id="1d668-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="1d668-115">الوحدات النمطية المتوفرة في الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="1d668-115">Modules that are available in a header module</span></span>

<span data-ttu-id="1d668-116">يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:</span><span class="sxs-lookup"><span data-stu-id="1d668-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="1d668-117">**قائمه التنقل** – تمثل قائمه التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة.</span><span class="sxs-lookup"><span data-stu-id="1d668-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="1d668-118">يمكن تكوين التدرج الهرمي للتنقل في القناة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1d668-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1d668-119">تتضمن قائمة التنقل خاصية **مصدر‏‎ التنقل** التي تُستخدم لتحديد عناصر قائمة التنقل Retail Server وعناصر القائمة الثابتة كمصدر.</span><span class="sxs-lookup"><span data-stu-id="1d668-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="1d668-120">إذا تم تحديد عناصر قائمة ثابتة كمصدر، فيمكن توفير ارتباطات نسبية إلى الصفحات الأخرى في الموقع.</span><span class="sxs-lookup"><span data-stu-id="1d668-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="1d668-121">تظهر العناصر المكونة بعد ذلك كتنقل عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1d668-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="1d668-122">**بحث** – تسمح وحدة البحث للمستخدمين بإدخال مصطلحات البحث للبحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="1d668-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="1d668-123">يجب توفير عنوان URL لصفحة البحث الافتراضية ومحددات استعلام البحث في **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="1d668-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="1d668-124">تتضمن وحدة البحث خصائص تتيح لك منع زر البحث أو التسمية كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="1d668-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="1d668-125">وتدعم أيضًا وحدة البحث خيارات الاقتراح التلقائي، مثل نتائج البحث عن منتج وكلمة أساسية وفئة.</span><span class="sxs-lookup"><span data-stu-id="1d668-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="1d668-126">إنشاء وحدة رأس لصفحة</span><span class="sxs-lookup"><span data-stu-id="1d668-126">Create a header module for a page</span></span>

<span data-ttu-id="1d668-127">لإنشاء وحدة نمطية للعنوان، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="1d668-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="1d668-128">أنشئ جزءًا يسمى **جزء الرأس**، وأضف إليه وحدة حاوية.</span><span class="sxs-lookup"><span data-stu-id="1d668-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="1d668-129">في جزء الخاصية لوحدة الحاوية، عيّن خاصية **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="1d668-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1d668-130">أضف وحدة الشعار الترويجي ووحدة الموافقة على ملفات تعريف شعار الارتباط إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="1d668-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="1d668-131">أضف وحدة حاوية أخرى إلى الجزء، وعيّن خاصية **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="1d668-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1d668-132">أضف وحدة رأس إلى وحدة الحاوية الثانية.</span><span class="sxs-lookup"><span data-stu-id="1d668-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="1d668-133">في فتحة **قائمة التنقل** في وحدة الرأس، أضف وحدة قائمة تنقل.</span><span class="sxs-lookup"><span data-stu-id="1d668-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="1d668-134">في جزء الخصائص لوحدة قائمة التنقل، قم بتكوين خصائص وحدة قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="1d668-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="1d668-135">في فتحة **البحث** في وحدة الرأس، أضف وحدة بحث.</span><span class="sxs-lookup"><span data-stu-id="1d668-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="1d668-136">في جزء الخصائص لوحدة البحث، قم بتكوين خصائص وحدة البحث.</span><span class="sxs-lookup"><span data-stu-id="1d668-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="1d668-137">احفظ جزء الصفحة ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="1d668-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="1d668-138">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="1d668-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="1d668-139">في الفتحة **الرئيسية** للصفحة الافتراضية، أضف جزء صفحة الرأس الذي يحتوي على وحدة الرأس إلى الرأس.</span><span class="sxs-lookup"><span data-stu-id="1d668-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="1d668-140">احفظ القالب ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="1d668-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d668-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1d668-141">Additional resources</span></span>

[<span data-ttu-id="1d668-142">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="1d668-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1d668-143">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="1d668-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1d668-144">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="1d668-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1d668-145">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="1d668-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1d668-146">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="1d668-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1d668-147">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="1d668-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1d668-148">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="1d668-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1d668-149">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="1d668-149">Footer module</span></span>](author-footer-module.md)
