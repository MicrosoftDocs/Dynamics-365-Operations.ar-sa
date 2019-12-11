---
title: الوحدة النمطية للعنوان
description: يتناول هذا الموضوع الوحدات النمطية للعنوان ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697265"
---
# <a name="header-module"></a><span data-ttu-id="6c18b-103">الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="6c18b-103">Header module</span></span>

<span data-ttu-id="6c18b-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="6c18b-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="6c18b-105">يتناول هذا الموضوع الوحدات النمطية للعنوان ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c18b-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c18b-106">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6c18b-106">Overview</span></span>

<span data-ttu-id="6c18b-107">الوحدة النمطية للعنوان هي حاوية خاصة تُستخدم لاستضافة جميع الوحدات التي سيتم عرضها في عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c18b-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="6c18b-108">علي سبيل المثال، يمكن ان يتضمن شعار الموقع الخاص بك والارتباطات بالتدرج الهرمي للتنقل والارتباطات بالصفحات الأخرى علي الموقع وشريط البحث.</span><span class="sxs-lookup"><span data-stu-id="6c18b-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="6c18b-109">يتم تحسين الوحدة النمطية للعنوان تلقائيًا للجهاز الذي يتم عرض الموقع عليه (أي جهاز سطح المكتب أو جهاز المحمول).</span><span class="sxs-lookup"><span data-stu-id="6c18b-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="6c18b-110">علي سبيل المثال، علي جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير*).</span><span class="sxs-lookup"><span data-stu-id="6c18b-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="6c18b-111">خصائص العنوان</span><span class="sxs-lookup"><span data-stu-id="6c18b-111">Properties of a header</span></span>

<span data-ttu-id="6c18b-112">مثل معظم الحاويات، تدعم الوحدة النمطية للعنوان خصائص **العنوان** و **العرض** .</span><span class="sxs-lookup"><span data-stu-id="6c18b-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="6c18b-113">تحتوي الوحدة النمطية للعنوان علي عدة فتحات.</span><span class="sxs-lookup"><span data-stu-id="6c18b-113">A header module has multiple slots.</span></span> <span data-ttu-id="6c18b-114">على سبيل المثال، توجد فتحات لرسالة معلوماتية، وقائمة التنقل، والشعار، وشريط البحث، ورمز سلة التسوق، ورمز قائمة الأمنيات، ومعلومات الحساب.</span><span class="sxs-lookup"><span data-stu-id="6c18b-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="6c18b-115">تدعم كل فتحه مجموعة معينة من الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="6c18b-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="6c18b-116">الوحدات النمطية المتوفرة في الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="6c18b-116">Modules that are available in a header module</span></span>

<span data-ttu-id="6c18b-117">يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:</span><span class="sxs-lookup"><span data-stu-id="6c18b-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="6c18b-118">**قائمه التنقل** – تمثل قائمه التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6c18b-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="6c18b-119">يمكن تكوين التدرج الهرمي للتنقل في القناة في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="6c18b-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="6c18b-120">تظهر العناصر المكونة بعد ذلك كتنقل عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c18b-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="6c18b-121">بالإضافة إلى ذلك، يمكن تكوين ارتباطات التنقل الثابت، ويمكن توفير ارتباطات نسبيه للصفحات الأخرى الموجودة في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6c18b-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="6c18b-122">يمكن محاذاة العنوان نفسه إلى اليسار أو اليمين أو الوسط.</span><span class="sxs-lookup"><span data-stu-id="6c18b-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="6c18b-123">**رمز سلة التسوق** – يعد رمز السلة أحد الرموز الخاصة التي تمثل السلة.</span><span class="sxs-lookup"><span data-stu-id="6c18b-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="6c18b-124">يظهر في العنوان ويشير إلى عدد العناصر في السلة.</span><span class="sxs-lookup"><span data-stu-id="6c18b-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="6c18b-125">يجب أن يرافق أي رابط لصفحة السلة رمز السلة، بحيث يمكن إعادة توجيه العملاء إلى صفحة سلة التسوق عندما يتفاعلون مع الرمز.</span><span class="sxs-lookup"><span data-stu-id="6c18b-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="6c18b-126">**رمز قائمة الأمنيات** – يتم عرض رمز قائمه الأمنيات في عنوان الصفحة ويشير إلى عدد الأصناف التي تمت إضافتها إلى قائمة الجهات الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="6c18b-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="6c18b-127">يجب أن يرافق أي رابط لصفحة قائمة الأمنيات هذا الرمز، بحيث يمكن إعادة توجيه العملاء إلى صفحة قائمة الأمنيات عندما يتفاعلون مع الرمز.</span><span class="sxs-lookup"><span data-stu-id="6c18b-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="6c18b-128">**الوحدة النمطية تسجيل الدخول** – يتم عرض الوحدة النمطية لتسجيل الدخول في العنوان.</span><span class="sxs-lookup"><span data-stu-id="6c18b-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="6c18b-129">يتيح للعملاء إما تسجيل الدخول إلى حسابهم أو التسجيل للحصول على حساب.</span><span class="sxs-lookup"><span data-stu-id="6c18b-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="6c18b-130">إذا تم تسجيل دخول العميل بالفعل، يمكن تكوين الوحدة النمطية لإظهار الارتباطات إلى صفحة الحساب، أو صفحة سجل الأمر ، أو أي صفحة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6c18b-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="6c18b-131">**الوحدة النمطية للشعار** – تعرض هذه الوحدة النمطية الشعار الذي يمثل بائع التجزئة والعلامة التجارية.</span><span class="sxs-lookup"><span data-stu-id="6c18b-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="6c18b-132">إنها صورة لها ارتباط.</span><span class="sxs-lookup"><span data-stu-id="6c18b-132">It's an image that has a link.</span></span> <span data-ttu-id="6c18b-133">عادةً ما يتم تكوين الارتباط بحيث يحتوي على إعادة توجيه إلى الصفحة الرئيسية، وبالتالي، يمكن للعملاء العودة بسرعة إلى الصفحة الرئيسية من أي صفحة على الموقع.</span><span class="sxs-lookup"><span data-stu-id="6c18b-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="6c18b-134">**التنبيه** – يظهر التنبيه في العنوان ويستخدم لعرض رسالة مضمنة تنطبق علي كافة صفحات الموقع.</span><span class="sxs-lookup"><span data-stu-id="6c18b-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="6c18b-135">علي سبيل المثال، قد يُظهر التنبيه رسالة مثل "ينتهي البيع السنوي في غضون يومين".</span><span class="sxs-lookup"><span data-stu-id="6c18b-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="6c18b-136">**شريط البحث** – يتيح شريط البحث للمستخدمين إدخال مصطلحات البحث حتى يمكنهم البحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="6c18b-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="6c18b-137">يجب تكوين الوحدة النمطية باستخدام عنوان URL لصفحة نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="6c18b-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="6c18b-138">يمكن تكوين مُعلمة سلسلة استعلام (وتكون القيمة الافتراضية **"q"**).</span><span class="sxs-lookup"><span data-stu-id="6c18b-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="6c18b-139">يحتوي شريط البحث على فتحة اقتراح تلقائي حيث يجب إضافة الوحدة النمطية اقتراح تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6c18b-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="6c18b-140">**اقتراح تلقائي** – تعرض الوحدة النمطية للاقتراح التلقائي النتائج المقترحة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6c18b-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="6c18b-141">يمكن أن تكون هذه النتائج كلمات رئيسية، أو منتجات، أو فئات يتم العثور فيها على مصطلح البحث.</span><span class="sxs-lookup"><span data-stu-id="6c18b-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="6c18b-142">إنشاء وحدة نمطية لرأس</span><span class="sxs-lookup"><span data-stu-id="6c18b-142">Create a header module</span></span>

<span data-ttu-id="6c18b-143">لإنشاء وحدة نمطية للعنوان، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="6c18b-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="6c18b-144">إنشاء جزء صفحة يتضمن الوحدة النمطية للعنوان.</span><span class="sxs-lookup"><span data-stu-id="6c18b-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="6c18b-145">إضافة وحدات نمطية إلى فتحات في الوحدة النمطية للعنوان.</span><span class="sxs-lookup"><span data-stu-id="6c18b-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="6c18b-146">تحديث الإعدادات لكل وحدة نمطية.</span><span class="sxs-lookup"><span data-stu-id="6c18b-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="6c18b-147">قم بحفظ جزء الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c18b-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="6c18b-148">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="6c18b-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="6c18b-149">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="6c18b-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="6c18b-150">في الصفحة الافتراضية، أضف جزء الصفحة الذي يحتوي على وحدة العنوان إلى العنوان في الفتحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="6c18b-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="6c18b-151">قم بحفظ القالب.</span><span class="sxs-lookup"><span data-stu-id="6c18b-151">Save the template.</span></span> 
1. <span data-ttu-id="6c18b-152">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="6c18b-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c18b-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6c18b-153">Additional resources</span></span>

[<span data-ttu-id="6c18b-154">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="6c18b-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6c18b-155">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="6c18b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6c18b-156">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="6c18b-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6c18b-157">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="6c18b-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6c18b-158">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="6c18b-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6c18b-159">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="6c18b-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6c18b-160">الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="6c18b-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6c18b-161">الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="6c18b-161">Footer module</span></span>](author-footer-module.md)
