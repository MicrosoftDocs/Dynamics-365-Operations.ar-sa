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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885468"
---
# <a name="header-module"></a><span data-ttu-id="6370c-103">وحدة نمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="6370c-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6370c-104">يتناول هذا الموضوع الوحدات النمطية للعنوان ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6370c-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6370c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6370c-105">Overview</span></span>

<span data-ttu-id="6370c-106">الوحدة النمطية للعنوان هي حاوية خاصة تُستخدم لاستضافة جميع الوحدات التي سيتم عرضها في عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6370c-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="6370c-107">علي سبيل المثال، يمكن ان يتضمن شعار الموقع الخاص بك والارتباطات بالتدرج الهرمي للتنقل والارتباطات بالصفحات الأخرى علي الموقع وشريط البحث.</span><span class="sxs-lookup"><span data-stu-id="6370c-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="6370c-108">يتم تحسين الوحدة النمطية للعنوان تلقائيًا للجهاز الذي يتم عرض الموقع عليه (أي جهاز سطح المكتب أو جهاز المحمول).</span><span class="sxs-lookup"><span data-stu-id="6370c-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="6370c-109">علي سبيل المثال، علي جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير*).</span><span class="sxs-lookup"><span data-stu-id="6370c-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="6370c-110">خصائص العنوان</span><span class="sxs-lookup"><span data-stu-id="6370c-110">Properties of a header</span></span>

<span data-ttu-id="6370c-111">مثل معظم الحاويات، تدعم الوحدة النمطية للعنوان خصائص **العنوان** و **العرض** .</span><span class="sxs-lookup"><span data-stu-id="6370c-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="6370c-112">تحتوي الوحدة النمطية للعنوان علي عدة فتحات.</span><span class="sxs-lookup"><span data-stu-id="6370c-112">A header module has multiple slots.</span></span> <span data-ttu-id="6370c-113">على سبيل المثال، توجد فتحات لرسالة معلوماتية، وقائمة التنقل، والشعار، وشريط البحث، ورمز سلة التسوق، ورمز قائمة الأمنيات، ومعلومات الحساب.</span><span class="sxs-lookup"><span data-stu-id="6370c-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="6370c-114">تدعم كل فتحه مجموعة معينة من الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="6370c-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="6370c-115">الوحدات النمطية المتوفرة في الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="6370c-115">Modules that are available in a header module</span></span>

<span data-ttu-id="6370c-116">يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:</span><span class="sxs-lookup"><span data-stu-id="6370c-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="6370c-117">**قائمه التنقل** – تمثل قائمه التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6370c-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="6370c-118">يمكن تكوين التدرج الهرمي للتنقل في القناة في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="6370c-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="6370c-119">تظهر العناصر المكونة بعد ذلك كتنقل عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6370c-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="6370c-120">بالإضافة إلى ذلك، يمكن تكوين ارتباطات التنقل الثابت، ويمكن توفير ارتباطات نسبيه للصفحات الأخرى الموجودة في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6370c-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="6370c-121">يمكن محاذاة العنوان نفسه إلى اليسار أو اليمين أو الوسط.</span><span class="sxs-lookup"><span data-stu-id="6370c-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="6370c-122">**رمز سلة التسوق** – يعد رمز السلة أحد الرموز الخاصة التي تمثل السلة.</span><span class="sxs-lookup"><span data-stu-id="6370c-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="6370c-123">يظهر في العنوان ويشير إلى عدد العناصر في السلة.</span><span class="sxs-lookup"><span data-stu-id="6370c-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="6370c-124">يجب أن يرافق أي رابط لصفحة السلة رمز السلة، بحيث يمكن إعادة توجيه العملاء إلى صفحة سلة التسوق عندما يتفاعلون مع الرمز.</span><span class="sxs-lookup"><span data-stu-id="6370c-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="6370c-125">**رمز قائمة الأمنيات** – يتم عرض رمز قائمه الأمنيات في عنوان الصفحة ويشير إلى عدد الأصناف التي تمت إضافتها إلى قائمة الجهات الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="6370c-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="6370c-126">يجب أن يرافق أي رابط لصفحة قائمة الأمنيات هذا الرمز، بحيث يمكن إعادة توجيه العملاء إلى صفحة قائمة الأمنيات عندما يتفاعلون مع الرمز.</span><span class="sxs-lookup"><span data-stu-id="6370c-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="6370c-127">**الوحدة النمطية تسجيل الدخول** – يتم عرض الوحدة النمطية لتسجيل الدخول في العنوان.</span><span class="sxs-lookup"><span data-stu-id="6370c-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="6370c-128">يتيح للعملاء إما تسجيل الدخول إلى حسابهم أو التسجيل للحصول على حساب.</span><span class="sxs-lookup"><span data-stu-id="6370c-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="6370c-129">إذا تم تسجيل دخول العميل بالفعل، يمكن تكوين الوحدة النمطية لإظهار الارتباطات إلى صفحة الحساب، أو صفحة سجل الأمر ، أو أي صفحة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6370c-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="6370c-130">**الوحدة النمطية للشعار** – تعرض هذه الوحدة النمطية الشعار الذي يمثل بائع التجزئة والعلامة التجارية.</span><span class="sxs-lookup"><span data-stu-id="6370c-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="6370c-131">إنها صورة لها ارتباط.</span><span class="sxs-lookup"><span data-stu-id="6370c-131">It's an image that has a link.</span></span> <span data-ttu-id="6370c-132">عادةً ما يتم تكوين الارتباط بحيث يحتوي على إعادة توجيه إلى الصفحة الرئيسية، وبالتالي، يمكن للعملاء العودة بسرعة إلى الصفحة الرئيسية من أي صفحة على الموقع.</span><span class="sxs-lookup"><span data-stu-id="6370c-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="6370c-133">**التنبيه** – يظهر التنبيه في العنوان ويستخدم لعرض رسالة مضمنة تنطبق علي كافة صفحات الموقع.</span><span class="sxs-lookup"><span data-stu-id="6370c-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="6370c-134">علي سبيل المثال، قد يُظهر التنبيه رسالة مثل "ينتهي البيع السنوي في غضون يومين".</span><span class="sxs-lookup"><span data-stu-id="6370c-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="6370c-135">**شريط البحث** – يتيح شريط البحث للمستخدمين إدخال مصطلحات البحث حتى يمكنهم البحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="6370c-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="6370c-136">يجب تكوين الوحدة النمطية باستخدام عنوان URL لصفحة نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="6370c-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="6370c-137">يمكن تكوين مُعلمة سلسلة استعلام (وتكون القيمة الافتراضية **"q"**).</span><span class="sxs-lookup"><span data-stu-id="6370c-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="6370c-138">يحتوي شريط البحث على فتحة اقتراح تلقائي حيث يجب إضافة الوحدة النمطية اقتراح تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6370c-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="6370c-139">**اقتراح تلقائي** – تعرض الوحدة النمطية للاقتراح التلقائي النتائج المقترحة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6370c-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="6370c-140">يمكن أن تكون هذه النتائج كلمات رئيسية، أو منتجات، أو فئات يتم العثور فيها على مصطلح البحث.</span><span class="sxs-lookup"><span data-stu-id="6370c-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="6370c-141">إنشاء وحدة نمطية لرأس</span><span class="sxs-lookup"><span data-stu-id="6370c-141">Create a header module</span></span>

<span data-ttu-id="6370c-142">لإنشاء وحدة نمطية للعنوان، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="6370c-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="6370c-143">إنشاء جزء صفحة يتضمن الوحدة النمطية للعنوان.</span><span class="sxs-lookup"><span data-stu-id="6370c-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="6370c-144">إضافة وحدات نمطية إلى فتحات في الوحدة النمطية للعنوان.</span><span class="sxs-lookup"><span data-stu-id="6370c-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="6370c-145">تحديث الإعدادات لكل وحدة نمطية.</span><span class="sxs-lookup"><span data-stu-id="6370c-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="6370c-146">قم بحفظ جزء الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6370c-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="6370c-147">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="6370c-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="6370c-148">للمساعدة في ضمان ظهور عنوان في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.</span><span class="sxs-lookup"><span data-stu-id="6370c-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="6370c-149">في الصفحة الافتراضية، أضف جزء الصفحة الذي يحتوي على وحدة العنوان إلى العنوان في الفتحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="6370c-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="6370c-150">قم بحفظ القالب.</span><span class="sxs-lookup"><span data-stu-id="6370c-150">Save the template.</span></span> 
1. <span data-ttu-id="6370c-151">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="6370c-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6370c-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6370c-152">Additional resources</span></span>

[<span data-ttu-id="6370c-153">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="6370c-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6370c-154">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="6370c-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6370c-155">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="6370c-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6370c-156">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="6370c-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6370c-157">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="6370c-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6370c-158">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="6370c-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6370c-159">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="6370c-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6370c-160">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="6370c-160">Footer module</span></span>](author-footer-module.md)
