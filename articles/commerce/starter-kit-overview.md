---
title: نظرة عامة على مكتبة الوحدات
description: يقدم هذا الموضوع نظرة عامة على مكتبة الوحدات النمطية في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcb0c2317315308de51d8247d23a930f10c3de6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234283"
---
# <a name="module-library-overview"></a><span data-ttu-id="fdbd6-103">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="fdbd6-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fdbd6-104">يقدم هذا الموضوع نظرة عامة على مكتبة الوحدات النمطية في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="fdbd6-105">تُعد مكتبة الوحدات النمطية في Dynamics 365 Commerce مجموعة من الوحدات النمطية التي يمكن استخدامها لإنشاء موقع ويب خاص بالتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="fdbd6-106">تحتوي الوحدات النمطية على كل من جوانب واجهة المستخدم (UI) وجوانب السلوك الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="fdbd6-107">يمكن تطبيق النُسق على الوحدات النمطية في مكتبة الوحدات النمطية لتغيير شكلها وأسلوب عرضها.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="fdbd6-108">تستخدم السمات أوراق الأنماط المتتالية (CSS).</span><span class="sxs-lookup"><span data-stu-id="fdbd6-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="fdbd6-109">يتم تقديم نسق لموقع تجارة إلكترونية  وهمي يسمى "Fabrikam" كجزء من مكتبة الوحدات النمطية ويمكن استخدامه كمرجع.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="fdbd6-110">الوحدات النمطية لمكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="fdbd6-110">Module library modules</span></span>

<span data-ttu-id="fdbd6-111">أنواع الوحدات النمطية التالية متوفرة في مكتبة الوحدات النمطية:</span><span class="sxs-lookup"><span data-stu-id="fdbd6-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="fdbd6-112">**وحدة الحاوية النمطية** – تُعد وحدة الحاوية النمطية وحدة نمطية بسيطة تعمل كمضيف لوحدات نمطية أخرى.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="fdbd6-113">إنها تتحكم في تخطيط الوحدات النمطية الموجودة داخلها.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="fdbd6-114">**الوحدات النمطية للتسويق** – تتضمن وحدات التسويق كتلة المحتوى وكتلة النص ومشغل الفيديو والوحدات الدوراة.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="fdbd6-115">يمكن استخدام كل هذه الوحدات النمطية لإظهار المحتوى.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="fdbd6-116">يمكن وضعها في أية صفحة ويتم التحكم بها بواسطة البيانات من نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="fdbd6-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="fdbd6-117">**الوحدات النمطية للرأي والتذييل** – تظهر الوحدات النمطية للرأس والتذييل في رأس وتذييل كافة صفحات الموقع.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="fdbd6-118">يمكن تكوين هذه الوحدات النمطية كما تريد خلال الخصائص.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="fdbd6-119">**الوحدات النمطية للبحث** يمكن اكتشاف المنتجات باستخدام الوحدة النمطية للبحث في الرأس.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="fdbd6-120">تظهر نتائج البحث على صفحة نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-120">Search results appear on the search results page.</span></span> <span data-ttu-id="fdbd6-121">يمكن أيضًا اكتشاف المنتجات على صفحات الفئة، وهي عبارة عن صفحات مخصصة لكل فئة مدعومة في التدرج الهرمي للتنقل في القناة.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="fdbd6-122">بالإضافة إلى ذلك، يمكن استخدام الوحدات النمطية للمدقق للحصول على نتائج تصفية إضافية في صفحات نتائج البحث والفئات.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="fdbd6-123">**الوحدات النمطية لصفحة تفاصيل المنتج** – تستخدم صفحات تفاصيل المنتج عدة وحدات نمطية لإظهار معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="fdbd6-124">تتيح الوحدة النمطية لمربع الشراء للعملاء عرض المنتجات وإضافتهاا إلى سله التسوق.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="fdbd6-125">بينما تقوم الوحدات النمطية الأخرى، مثل وحدة نمطية للمواصفات التقنية، بإظهار تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="fdbd6-126">يمكن استخدام الوحدة النمطية للتقييمات والمراجعات لعرض المراجعات وتوفيرها.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="fdbd6-127">**‏‫الوحدة النمطية للشراء عبر الإنترنت والانتقاء في المتجر** - تتكامل الوحدة النمطية للشراء عبر الإنترنت والانتقاء في المتجر مع خرائط Bing.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="fdbd6-128">يمكن استخدامها للبحث عن المتاجر القريبة حيث يمكن للعملاء انتقاء المنتجات التي قاموا بشراءها.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="fdbd6-129">**الوحدات النمطية للشراء** – تتضمن الوحدات النمطية للشراء الوحدة النمطية لسلة التسوق، والتي يمكن استخدامها لإضافة أصناف إلى عربة التسوق.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="fdbd6-130">تقوم الوحدة النمطية للسحب بإظهار عنوان الشحن وخيارات التسليم وبطاقة الهدايا وبرنامج الولاء والمعلومات الخاصة ببطاقة الائتمان، بحيث يمكن معالجة الأمر.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="fdbd6-131">بعد إصدار الأمر، يمكن استخدام الوحدة النمطية لتأكيد الأمر لإظهار تفاصيل التأكيد.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="fdbd6-132">**الوحدات النمطية لإدارة الحساب** – تسمح الوحدة النمطية لتسجيل الدخول للعملاء بتسجيل الدخول إلى حساب موجود، وتتيح لهم الوحدة النمطية للتسجيل بإنشاء حساب جديد.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="fdbd6-133">بعد إنشاء حساب، يمكن استخدام الوحدة النمطية لسجل الأمر لعرض الأوامر الحديثة ويمكن استخدام الوحدة النمطية لتفاصيل الأمر لعرض تفاصيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="fdbd6-134">**الوحدة النمطية للتوصيات** – يتم عرض التوصيات باستخدام الوحدة النمطية لوضع محتوى المنتج.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="fdbd6-135">تدعم هذه الوحدة النمطية القوائم الحسابية والتحريرية التي يمكن إظهارها على أية صفحة.</span><span class="sxs-lookup"><span data-stu-id="fdbd6-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdbd6-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fdbd6-136">Additional resources</span></span>

[<span data-ttu-id="fdbd6-137">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="fdbd6-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fdbd6-138">وحدة مربع شراء</span><span class="sxs-lookup"><span data-stu-id="fdbd6-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fdbd6-139">وحدة سلة التسوق</span><span class="sxs-lookup"><span data-stu-id="fdbd6-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fdbd6-140">وحدة السداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="fdbd6-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fdbd6-141">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="fdbd6-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fdbd6-142">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="fdbd6-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fdbd6-143">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="fdbd6-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]