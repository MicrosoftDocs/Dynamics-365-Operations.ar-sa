---
title: وحدة الرأس
description: يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261434"
---
# <a name="header-module"></a><span data-ttu-id="29fc2-103">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="29fc2-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="29fc2-104">يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="29fc2-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="29fc2-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="29fc2-105">Overview</span></span>

<span data-ttu-id="29fc2-106">في Dynamics 365 Commerce، يتضمن رأس الصفحة وحدات متعددة، مثل وحدات الرأس وقائمة التنقل والبحث والشعار الترويجي والموافقة على ملف تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="29fc2-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="29fc2-107">تتضمن وحدة الرأس شعار الموقع وارتباطات إلى التدرج الهرمي للتنقل وارتباطات إلى صفحات أخرى في الموقع ورمز سلة التسوق ورمز قائمة الأمنيات وخيارات تسجيل الدخول وشريط البحث.</span><span class="sxs-lookup"><span data-stu-id="29fc2-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="29fc2-108">يتم تحسين وحدة الرأس بشكل تلقائي للجهاز الذي يتم عرض الموقع عليه (بمعنىً آخر لجهاز سطح المكتب أو جهاز محمول).</span><span class="sxs-lookup"><span data-stu-id="29fc2-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="29fc2-109">على سبيل المثال، علي جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير*).</span><span class="sxs-lookup"><span data-stu-id="29fc2-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="29fc2-110">خصائص وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="29fc2-110">Properties of a header module</span></span>

<span data-ttu-id="29fc2-111">تدعم وحدة الرأس خصائص **صورة الشعار** و**ارتباط الشعار** و**ارتباطات حسابي**.</span><span class="sxs-lookup"><span data-stu-id="29fc2-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="29fc2-112">تُستخدم خصائص **صورة الشعار** و**ارتباط الشعار** لتعريف شعار على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="29fc2-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="29fc2-113">لمزيد من المعلومات، راجع [إضافة شعار](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="29fc2-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="29fc2-114">يمكن استخدام الخاصية **ارتباطات حسابي** لتحديد صفحات الحساب التي يريد مالك الموقع عرض ارتباطات سريعة لها في الرأس.</span><span class="sxs-lookup"><span data-stu-id="29fc2-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="29fc2-115">الوحدات النمطية المتوفرة في الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="29fc2-115">Modules that are available in a header module</span></span>

<span data-ttu-id="29fc2-116">يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:</span><span class="sxs-lookup"><span data-stu-id="29fc2-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="29fc2-117">**قائمة التنقل** – تمثل قائمة التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة.</span><span class="sxs-lookup"><span data-stu-id="29fc2-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="29fc2-118">يمكن تكوين التدرج الهرمي للتنقل في القناة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="29fc2-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="29fc2-119">تتضمن قائمة التنقل خاصية **مصدر‏‎ التنقل** التي تُستخدم لتحديد عناصر قائمة التنقل Retail Server وعناصر القائمة الثابتة كمصدر.</span><span class="sxs-lookup"><span data-stu-id="29fc2-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="29fc2-120">إذا تم تحديد عناصر قائمة ثابتة كمصدر، فيمكن توفير ارتباطات نسبية إلى الصفحات الأخرى في الموقع.</span><span class="sxs-lookup"><span data-stu-id="29fc2-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="29fc2-121">تظهر العناصر المكونة بعد ذلك كتنقل عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="29fc2-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="29fc2-122">**بحث** – تسمح وحدة البحث للمستخدمين بإدخال مصطلحات البحث للبحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="29fc2-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="29fc2-123">يجب توفير عنوان URL لصفحة البحث الافتراضية ومحددات استعلام البحث في **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="29fc2-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="29fc2-124">تتضمن وحدة البحث خصائص تتيح لك منع زر البحث أو التسمية كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="29fc2-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="29fc2-125">وتدعم أيضًا وحدة البحث خيارات الاقتراح التلقائي، مثل نتائج البحث عن منتج وكلمة أساسية وفئة.</span><span class="sxs-lookup"><span data-stu-id="29fc2-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="29fc2-126">**أيقونة سلة التسوق** - تمثل وحدة أيقونة سلة التسوق أيقونة سلة التسوق، التي تعرض عدد الأصناف في سلة التسوق في أي وقت محدد.</span><span class="sxs-lookup"><span data-stu-id="29fc2-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="29fc2-127">لمزيد من المعلومات، راجع‏‎ [وحدة أيقونة سلة التسوق](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="29fc2-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="29fc2-128">إنشاء وحدة رأس لصفحة</span><span class="sxs-lookup"><span data-stu-id="29fc2-128">Create a header module for a page</span></span>

<span data-ttu-id="29fc2-129">لإنشاء وحدة نمطية للعنوان، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="29fc2-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="29fc2-130">أنشئ جزءًا يسمى **جزء الرأس**، وأضف إليه وحدة حاوية.</span><span class="sxs-lookup"><span data-stu-id="29fc2-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="29fc2-131">في جزء الخاصية لوحدة الحاوية، عيّن خاصية **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="29fc2-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="29fc2-132">أضف وحدة الشعار الترويجي ووحدة الموافقة على ملفات تعريف الارتباط إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="29fc2-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="29fc2-133">أضف وحدة حاوية أخرى إلى الجزء، وعيّن خاصية **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="29fc2-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="29fc2-134">أضف وحدة رأس إلى وحدة الحاوية الثانية.</span><span class="sxs-lookup"><span data-stu-id="29fc2-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="29fc2-135">في فتحة **قائمة التنقل** في وحدة الرأس، أضف وحدة قائمة تنقل.</span><span class="sxs-lookup"><span data-stu-id="29fc2-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="29fc2-136">في جزء الخصائص لوحدة قائمة التنقل، قم بتكوين خصائص وحدة قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="29fc2-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="29fc2-137">في فتحة **البحث** في وحدة الرأس، أضف وحدة بحث.</span><span class="sxs-lookup"><span data-stu-id="29fc2-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="29fc2-138">في جزء الخصائص لوحدة البحث، قم بتكوين خصائص وحدة البحث.</span><span class="sxs-lookup"><span data-stu-id="29fc2-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="29fc2-139">في فتحة **وحدة أيقونة سلة التسوق** لوحة الرأس، أضف وحدة أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="29fc2-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="29fc2-140">في جزء الخصائص لوحدة أيقونة سلة التسوق، قم بتكوين وحدة أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="29fc2-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="29fc2-141">إذا أردت أن تعرض أيقونة سلة التسوق سلة تسوق صغيرة عند تمرير الماوس فوقها، فحدد **صواب** من اجل **إظهار سلة التسوق الصغيرة**.</span><span class="sxs-lookup"><span data-stu-id="29fc2-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="29fc2-142">احفظ جزء الصفحة ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="29fc2-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="29fc2-143">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="29fc2-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="29fc2-144">في الفتحة **الرئيسية** للصفحة الافتراضية، أضف جزء صفحة الرأس الذي يحتوي على وحدة الرأس إلى الرأس.</span><span class="sxs-lookup"><span data-stu-id="29fc2-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="29fc2-145">احفظ القالب ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="29fc2-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29fc2-146">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="29fc2-146">Additional resources</span></span>

[<span data-ttu-id="29fc2-147">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="29fc2-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="29fc2-148">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="29fc2-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="29fc2-149">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="29fc2-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="29fc2-150">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="29fc2-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="29fc2-151">الوحدة النمطية لأيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="29fc2-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="29fc2-152">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="29fc2-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="29fc2-153">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="29fc2-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="29fc2-154">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="29fc2-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="29fc2-155">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="29fc2-155">Footer module</span></span>](author-footer-module.md)
