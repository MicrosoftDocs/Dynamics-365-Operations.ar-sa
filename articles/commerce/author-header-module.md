---
title: وحدة الرأس
description: يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055440"
---
# <a name="header-module"></a><span data-ttu-id="d96fc-103">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="d96fc-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d96fc-104">يتناول هذا الموضوع وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d96fc-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d96fc-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d96fc-105">Overview</span></span>

<span data-ttu-id="d96fc-106">في Dynamics 365 Commerce، يتم تكوين رأس الصفحة كجزء صفحة يتضمن الوحدات النمطية للرأس والشعار الترويجي والموافقة على ملفات تعريف الارتباط‬.</span><span class="sxs-lookup"><span data-stu-id="d96fc-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="d96fc-107">تتضمن وحدة الرأس شعار الموقع وارتباطات إلى التدرج الهرمي للتنقل وارتباطات إلى صفحات أخرى في الموقع ووحدة نمطية لأيقونة سلة التسوق ورمز قائمة الأمنيات وخيارات تسجيل الدخول وشريط البحث.</span><span class="sxs-lookup"><span data-stu-id="d96fc-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="d96fc-108">يتم تحسين وحدة الرأس بشكل تلقائي للجهاز الذي يتم عرض الموقع عليه (بمعنىً آخر لجهاز سطح المكتب أو جهاز محمول).</span><span class="sxs-lookup"><span data-stu-id="d96fc-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="d96fc-109">على سبيل المثال، على جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير* ).</span><span class="sxs-lookup"><span data-stu-id="d96fc-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu* ).</span></span>

<span data-ttu-id="d96fc-110">تعرض الصورة التالية مثالاً عن وحدة الرأس في صفحة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="d96fc-110">The following image shows an example of a header module on a home page.</span></span>

![مثال عن وحدة رأس](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="d96fc-112">خصائص وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="d96fc-112">Properties of a header module</span></span>

<span data-ttu-id="d96fc-113">تدعم وحدة الرأس خصائص **صورة الشعار** و **ارتباط الشعار** و **ارتباطات حسابي**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-113">A header module supports **Logo image** , **Logo link** , and **My account links** properties.</span></span> 

<span data-ttu-id="d96fc-114">تُستخدم خصائص **صورة الشعار** و **ارتباط الشعار** لتعريف شعار على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d96fc-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="d96fc-115">لمزيد من المعلومات، راجع [إضافة شعار](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="d96fc-116">يمكن استخدام الخاصية **ارتباطات حسابي** لتحديد صفحات الحساب التي يريد مالك الموقع عرض ارتباطات سريعة لها في الرأس.</span><span class="sxs-lookup"><span data-stu-id="d96fc-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="d96fc-117">الوحدات النمطية المتوفرة في الوحدة النمطية للرأس</span><span class="sxs-lookup"><span data-stu-id="d96fc-117">Modules that are available within a header module</span></span>

<span data-ttu-id="d96fc-118">يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:</span><span class="sxs-lookup"><span data-stu-id="d96fc-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="d96fc-119">**قائمة التنقل** – تمثل قائمة التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة.</span><span class="sxs-lookup"><span data-stu-id="d96fc-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="d96fc-120">لمزيد من المعلومات، راجع [الوحدة النمطية لقائمة التنقل](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="d96fc-121">**بحث** – تسمح وحدة البحث للمستخدمين بإدخال مصطلحات البحث للبحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="d96fc-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="d96fc-122">يجب توفير عنوان URL لصفحة البحث الافتراضية ومحددات استعلام البحث في **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="d96fc-123">تتضمن وحدة البحث خصائص تتيح لك منع زر البحث أو التسمية كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="d96fc-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="d96fc-124">وتدعم أيضًا وحدة البحث خيارات الاقتراح التلقائي، مثل نتائج البحث عن منتج وكلمة أساسية وفئة.</span><span class="sxs-lookup"><span data-stu-id="d96fc-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="d96fc-125">**أيقونة سلة التسوق** - تمثل وحدة أيقونة سلة التسوق أيقونة سلة التسوق، التي تعرض عدد الأصناف في سلة التسوق في أي وقت محدد.</span><span class="sxs-lookup"><span data-stu-id="d96fc-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="d96fc-126">لمزيد من المعلومات، راجع‏‎ [وحدة أيقونة سلة التسوق](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="d96fc-127">**محدد الموقع** - تتيح الوحدة النمطية لمحدد الموقع للمستخدمين استعراض المواقع المختلفة المعرفة مسبقًا، استنادًا إلى السوق والمناطق والإعدادات المحلية.</span><span class="sxs-lookup"><span data-stu-id="d96fc-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="d96fc-128">لمزيد من المعلومات، راجع‏‎ [الوحدة النمطية لمحدد الموقع](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="d96fc-129">**محدد المتجر** - يمكن تضمين الوحدة النمطية لمحدد المتجر في فتحة محدد المتجر الخاصة بالوحدة النمطية لرأس.</span><span class="sxs-lookup"><span data-stu-id="d96fc-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="d96fc-130">تتيح للمستخدمين استعراض المتاجر القريبة والبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="d96fc-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="d96fc-131">كما يمكن للمستخدمين تحديد المتجر المفضل.</span><span class="sxs-lookup"><span data-stu-id="d96fc-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="d96fc-132">سيتم بعد ذلك إظهار ذلك المتجر في الرأس.</span><span class="sxs-lookup"><span data-stu-id="d96fc-132">That store will then be shown in the header.</span></span> <span data-ttu-id="d96fc-133">عند تضمين الوحدة النمطية لمحدد المتجر في الوحدة النمطية للرأس، فإنه يجب تعيين الخاصية **وضع** على **البحث عن المتاجر**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="d96fc-134">لمزيد من المعلومات، راجع‏‎ [الوحدة النمطية لمحدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="d96fc-135">يتوفر دعم استخدام الوحدة النمطية لأيقونة عربة التسوق في الوحدات النمطية للرأس في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="d96fc-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="d96fc-136">يتوفر دعم استخدام الوحدة النمطية لمحدد الموقع في الوحدات النمطية للرأس في Dynamics 365 Commerce الإصدار 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="d96fc-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="d96fc-137">يتوفر دعم استخدام الوحدة النمطية لمحدد المتجر في الوحدات النمطية للرأس في Dynamics 365 Commerce الإصدار 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="d96fc-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="d96fc-138">إنشاء جزء رأس لصفحة</span><span class="sxs-lookup"><span data-stu-id="d96fc-138">Create a header fragment for a page</span></span>

<span data-ttu-id="d96fc-139">لإنشاء جزء رأس، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d96fc-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="d96fc-140">انتقل إلى **الأجزاء** ، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="d96fc-140">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d96fc-141">في مربع الحوار **جزء جديد** ، حدد وحدة **الحاوية** ، وأدخل اسمًا للجزء، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d96fc-142">حدد فتحة **الحاوية الافتراضية** ، ثم في جزء الخصائص الموجود إلى اليمين، قم بتعيين خاصية **العرض** إلى **ملء الشاشة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="d96fc-143">في فتحة **الحاوية الافتراضية‬‬‏‫** ، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-143">In the **Default container** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d96fc-144">في مربع الحوار **إضافة وحدة** ، حدد الوحدات النمطية **الموافقة على ملفات تعريف الارتباط** و **الرأس** و **الشعار الترويجي** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-144">In the **Add Module** dialog box, select the **Cookie consent** , **Header** , and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="d96fc-145">في جزء الخصائص في الوحدة النمطية **الشعار الترويجي** ، حدد **إضافة رسالة** ، ثم حدد **الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-145">In the properties pane of the **Promo banner** module, select **Add Message** , and then select **Message**.</span></span>
1. <span data-ttu-id="d96fc-146">في مربع الحوار **الرسالة** ، أضف النص والارتباطات للمحتوى الترويجي، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="d96fc-147">في جزء الخصائص في الوحدة النمطية **الموافقة على ملفات تعريف الارتباط** ، أضف وكوّن نصًا وارتباطًا إلى صفحة خصوصية الموقع.</span><span class="sxs-lookup"><span data-stu-id="d96fc-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="d96fc-148">في فتحة **قائمة التنقل** لوحدة الرأس، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-148">In the **Navigation menu** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d96fc-149">في مربع الحوار **إضافة وحدة** ، حدد وحدة **قائمة التنقل** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d96fc-150">في جزء الخصائص في الوحدة النمطية لقائمة التنقل، ضمن **المصدر لقائمة التنقل** ، حدد **Retail Server**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-150">In the property pane for the navigation menu module, under **Source for navigation menu** , select **Retail Server**.</span></span>
1. <span data-ttu-id="d96fc-151">في جزء الخصائص في الوحدة النمطية لقائمة التنقل، ضمن **عناصر القائمة الثابتة** ، حدد **إضافة عنصر قائمة** ، ثم حدد **عنصر قائمة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-151">In the property pane for the navigation menu module, under **Static menu items** , select **Add Menu item** , and then select **Menu item**.</span></span> 
1. <span data-ttu-id="d96fc-152">في مربع الحوار **عنصر القائمة** ، ضمن **نص عنصر القائمة** ، أدخل "جهة اتصال".</span><span class="sxs-lookup"><span data-stu-id="d96fc-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="d96fc-153">في مربع الحوار **عنصر القائمة** ، ضمن **هدف ارتباط عنصر القائمة** ، حدد **إضافة ارتباط**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="d96fc-154">في مربع الحوار **إضافة ارتباط** ،حدد عنوان URL لصفحة "جهة الاتصال" في الموقع، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="d96fc-155">في مربع الحوار **عنصر القائمة‬‏‫** حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="d96fc-156">في فتحة **البحث** لوحدة الرأس، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-156">In the **Search** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d96fc-157">في مربع الحوار **إضافة وحدة** ، حدد وحدة ‬‏‫ **البحث‬** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d96fc-158">في جزء الخصائص لوحدة البحث، قم بتكوين الخصائص وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d96fc-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="d96fc-159">في فتحة **أيقونة سلة التسوق** لوحدة الرأس، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-159">In the **Cart icon** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d96fc-160">في مربع الحوار **إضافة وحدة** ، حدد وحدة ‬‏‫ **أيقونة سلة التسوق‬** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d96fc-161">في جزء الخصائص لوحدة أيقونة سلة التسوق، قم بتكوين الخصائص وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d96fc-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="d96fc-162">إذا أردت أن تعرض أيقونة سلة التسوق ملخصًا لسلة التسوق (تُعرف أيضًا بسلة التسوق الصغيرة) عند قيام المستخدم بتمرير الماوس فوقها، فحدد **إظهار سلة التسوق الصغيرة**.</span><span class="sxs-lookup"><span data-stu-id="d96fc-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="d96fc-163">حدد **حفظ** ، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="d96fc-163">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="d96fc-164">للمساعدة في ضمان ظهور الرأس في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="d96fc-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="d96fc-165">في فتحة **الرأس** في وحدة **الصفحة الافتراضية** ، أضف جزء التذييل الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="d96fc-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="d96fc-166">حدد **حفظ** ، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="d96fc-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d96fc-167">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d96fc-167">Additional resources</span></span>

[<span data-ttu-id="d96fc-168">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="d96fc-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d96fc-169">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="d96fc-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d96fc-170">الوحدة النمطية لرمز عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="d96fc-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d96fc-171">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="d96fc-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="d96fc-172">الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="d96fc-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="d96fc-173">الموافقة على ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="d96fc-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="d96fc-174">وحدة التذييلات‬</span><span class="sxs-lookup"><span data-stu-id="d96fc-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="d96fc-175">الوحدة النمطية لمحدد الموقع</span><span class="sxs-lookup"><span data-stu-id="d96fc-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="d96fc-176">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="d96fc-176">Store selector module</span></span>](store-selector.md)
