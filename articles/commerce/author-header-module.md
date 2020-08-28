---
title: وحدة الرأس
description: يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686612"
---
# <a name="header-module"></a><span data-ttu-id="019f9-103">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="019f9-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="019f9-104">يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="019f9-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="019f9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="019f9-105">Overview</span></span>

<span data-ttu-id="019f9-106">في Dynamics 365 Commerce، يتضمن رأس الصفحة وحدات متعددة، مثل وحدات الرأس وقائمة التنقل والبحث والشعار الترويجي والموافقة على ملف تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="019f9-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="019f9-107">تتضمن وحدة الرأس شعار الموقع وارتباطات إلى التدرج الهرمي للتنقل وارتباطات إلى صفحات أخرى في الموقع ورمز سلة التسوق ورمز قائمة الأمنيات وخيارات تسجيل الدخول وشريط البحث.</span><span class="sxs-lookup"><span data-stu-id="019f9-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="019f9-108">يتم تحسين وحدة الرأس بشكل تلقائي للجهاز الذي يتم عرض الموقع عليه (بمعنىً آخر لجهاز سطح المكتب أو جهاز محمول).</span><span class="sxs-lookup"><span data-stu-id="019f9-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="019f9-109">على سبيل المثال، علي جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير*).</span><span class="sxs-lookup"><span data-stu-id="019f9-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="019f9-110">تعرض الصورة التالية مثالاً عن وحدة الرأس في صفحة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="019f9-110">The following image shows an example of a header module on a home page.</span></span>

![مثال عن وحدة رأس](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="019f9-112">خصائص وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="019f9-112">Properties of a header module</span></span>

<span data-ttu-id="019f9-113">تدعم وحدة الرأس خصائص **صورة الشعار** و**ارتباط الشعار** و**ارتباطات حسابي**.</span><span class="sxs-lookup"><span data-stu-id="019f9-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="019f9-114">تُستخدم خصائص **صورة الشعار** و**ارتباط الشعار** لتعريف شعار على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="019f9-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="019f9-115">لمزيد من المعلومات، راجع [إضافة شعار](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="019f9-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="019f9-116">يمكن استخدام الخاصية **ارتباطات حسابي** لتحديد صفحات الحساب التي يريد مالك الموقع عرض ارتباطات سريعة لها في الرأس.</span><span class="sxs-lookup"><span data-stu-id="019f9-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="019f9-117">الوحدات النمطية المتوفرة في الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="019f9-117">Modules that are available in a header module</span></span>

<span data-ttu-id="019f9-118">يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:</span><span class="sxs-lookup"><span data-stu-id="019f9-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="019f9-119">**قائمة التنقل** – تمثل قائمة التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة.</span><span class="sxs-lookup"><span data-stu-id="019f9-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="019f9-120">يمكن تكوين التدرج الهرمي للتنقل في القناة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="019f9-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="019f9-121">تتضمن قائمة التنقل خاصية **مصدر‏‎ التنقل** التي تُستخدم لتحديد عناصر قائمة التنقل Retail Server وعناصر القائمة الثابتة كمصدر.</span><span class="sxs-lookup"><span data-stu-id="019f9-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="019f9-122">إذا تم تحديد عناصر قائمة ثابتة كمصدر، فيمكن توفير ارتباطات نسبية إلى الصفحات الأخرى في الموقع.</span><span class="sxs-lookup"><span data-stu-id="019f9-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="019f9-123">تظهر العناصر المكونة بعد ذلك كتنقل عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="019f9-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="019f9-124">**بحث** – تسمح وحدة البحث للمستخدمين بإدخال مصطلحات البحث للبحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="019f9-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="019f9-125">يجب توفير عنوان URL لصفحة البحث الافتراضية ومحددات استعلام البحث في **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="019f9-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="019f9-126">تتضمن وحدة البحث خصائص تتيح لك منع زر البحث أو التسمية كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="019f9-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="019f9-127">وتدعم أيضًا وحدة البحث خيارات الاقتراح التلقائي، مثل نتائج البحث عن منتج وكلمة أساسية وفئة.</span><span class="sxs-lookup"><span data-stu-id="019f9-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="019f9-128">**أيقونة سلة التسوق** - تمثل وحدة أيقونة سلة التسوق أيقونة سلة التسوق، التي تعرض عدد الأصناف في سلة التسوق في أي وقت محدد.</span><span class="sxs-lookup"><span data-stu-id="019f9-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="019f9-129">لمزيد من المعلومات، راجع‏‎ [وحدة أيقونة سلة التسوق](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="019f9-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="019f9-130">إنشاء وحدة رأس لصفحة</span><span class="sxs-lookup"><span data-stu-id="019f9-130">Create a header module for a page</span></span>

<span data-ttu-id="019f9-131">لإنشاء وحدة نمطية للعنوان، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="019f9-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="019f9-132">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="019f9-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="019f9-133">في مربع الحوار **جزء الصفحة الجديد**، حدد وحدة **الحاوية**، وأدخل اسمًا لجزء الصفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-134">حدد فتحة **الحاوية الافتراضية**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتعيين خاصية **العرض** إلى **ملء الحاوية‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="019f9-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="019f9-135">في فتحة **الحاوية الافتراضية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="019f9-136">في مربع الحوار **إضافة وحدة**، حدد وحدة **الشعار الترويجي**‬ ووحدة **الموافقة على ملفات تعريف الارتباط**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-137">في فتحة **الحاوية الافتراضية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="019f9-138">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-139">حدد فتحة **الحاوية**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتعيين خاصية **العرض** إلى **ملء الحاوية‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="019f9-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="019f9-140">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="019f9-141">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الرأس‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-142">في فتحة **قائمة التنقل** لوحدة الرأس، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="019f9-143">في مربع الحوار **إضافة وحدة**، حدد وحدة **قائمة التنقل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-144">في جزء الخصائص لوحدة قائمة التنقل، قم بتكوين الخصائص وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="019f9-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="019f9-145">في فتحة **البحث** لوحدة الرأس، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="019f9-146">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**البحث‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-147">في جزء الخصائص لوحدة البحث، قم بتكوين الخصائص وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="019f9-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="019f9-148">في فتحة **أيقونة سلة التسوق** لوحدة الرأس، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="019f9-149">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**أيقونة سلة التسوق‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="019f9-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="019f9-150">في جزء الخصائص لوحدة أيقونة سلة التسوق، قم بتكوين الخصائص وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="019f9-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="019f9-151">إذا أردت أن تعرض أيقونة سلة التسوق ملخصًا لسلة التسوق (تُعرف أيضًا بسلة التسوق الصغيرة) عند قيام المستخدم بتمرير الماوس فوقها، فحدد **إظهار سلة التسوق الصغيرة**.</span><span class="sxs-lookup"><span data-stu-id="019f9-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="019f9-152">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="019f9-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="019f9-153">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="019f9-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="019f9-154">في فتحة **الرأس** في وحدة **الصفحة الافتراضية**، أضف جزء التذييل الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="019f9-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="019f9-155">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="019f9-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="019f9-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="019f9-156">Additional resources</span></span>

[<span data-ttu-id="019f9-157">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="019f9-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="019f9-158">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="019f9-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="019f9-159">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="019f9-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="019f9-160">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="019f9-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="019f9-161">الوحدة النمطية لأيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="019f9-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="019f9-162">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="019f9-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="019f9-163">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="019f9-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="019f9-164">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="019f9-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="019f9-165">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="019f9-165">Footer module</span></span>](author-footer-module.md)
