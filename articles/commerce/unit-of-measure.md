---
title: تطبيق إعدادات وحدة القياس
description: يغطي هذا الموضوع إعدادات وحدة القياس ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022364"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="f6cb2-103">تطبيق إعدادات وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="f6cb2-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f6cb2-104">يغطي هذا الموضوع إعدادات وحدة القياس ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f6cb2-105">يمكن بيع المنتج في وحدات مختلفة، مثل "كل" و"زوج" و"دستة".</span><span class="sxs-lookup"><span data-stu-id="f6cb2-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="f6cb2-106">في مقر Commerce، يمكن تعريف وحدة قياس البيع حسب المنتج وعرضها على موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="f6cb2-107">على سبيل المثال، إذا قام بائع تجزئة ببيع منتج ما بشكل فردي أو بالعشرات، فيمكن عرض وحدات القياس المتاحة مع معلومات المنتج الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="f6cb2-108">في المثال الموضح في الرسم التوضيحي التالي، يتم بيع وحدة قياس مقدارها **ea** تم تكوين (كل) لمنتج في Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![مثال على منتج تم تكوينه باستخدام وحدة قياس في Commerce headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="f6cb2-110">يتوفر دعم لتطبيق وإظهار وحدة القياس اعتبارًا من إصدار Commerce رقم 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="f6cb2-111">إعدادات وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="f6cb2-111">Unit of measure settings</span></span>

<span data-ttu-id="f6cb2-112">يتم تحديد إعدادات عرض وحدة القياس في منشئ موقع Commerce، في **إعدادات الموقع \> الأبعاد \> عرض وحدة القياس للمنتجات**.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="f6cb2-113">هناك ثلاثة إعدادات مدعومة:</span><span class="sxs-lookup"><span data-stu-id="f6cb2-113">There are three supported settings:</span></span>

- <span data-ttu-id="f6cb2-114">**عدم العرض** – عند تحديد هذا الإعداد، لن يعرض موقع التجارة الإلكترونية وحدة قياس المنتج.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="f6cb2-115">هذا السلوك هو السلوك الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="f6cb2-116">**عرض في تجربة شراء المنتج** – عند تحديد هذا الإعداد، يتم عرض وحدة القياس في صفحات تفاصيل المنتج، وعربة التسوق، والسداد، وسجل الطلبات، وصفحات تفاصيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="f6cb2-117">**عرض في تصفح المنتج وتجربة الشراء** – عند تحديد هذا الإعداد، يتم عرض وحدة القياس على صفحات تجربة شراء المنتج وأيضًا أثناء تجربة تصفح المنتج.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="f6cb2-118">كجزء من هذا السلوك، يتم عرض وحدات القياس في نتائج البحث ووحدات تجميع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6cb2-119">تتوفر إعدادات عرض وحدة القياس اعتبارًا من إصدار Commerce رقم 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="f6cb2-120">إذا كنت تقوم بالتحديث من إصدار قديم من Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f6cb2-121">للاطلاع على التعليمات، راجع [تحديثات مكتبة الوحدات وSDK](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="f6cb2-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="f6cb2-122">الوحدات التي تستخدم إعدادات وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="f6cb2-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="f6cb2-123">تشمل الوحدات التي تستخدم إعدادات وحدة القياس صندوق الشراء، وقائمة الرغبات، والعربة، وأيقونة عربة التسوق، وحاوية نتائج البحث، ومجموعة المنتجات، والسداد، ووحدات تفاصيل الطلب.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="f6cb2-124">في المثال الموضح في الرسم التوضيحي التالي، تعرض صفحة تفاصيل المنتج (PDP) وحدة القياس (**ea**) لمنتج.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![مثال على PDP يعرض وحدة القياس](./media/Productunit-PDP.png)

<span data-ttu-id="f6cb2-126">في المثال الموضح في الرسم التوضيحي التالي، تعرض وحدة تجميع المنتج وحدة القياس (**ea**) للمنتج.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![مثال على وحدة تجميع المنتج التي تعرض وحدة القياس](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="f6cb2-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f6cb2-128">Additional resources</span></span>

[<span data-ttu-id="f6cb2-129">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="f6cb2-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f6cb2-130">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="f6cb2-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f6cb2-131">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="f6cb2-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f6cb2-132">الصفحات والوحدات النمطية لإدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="f6cb2-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="f6cb2-133">تحديثات SDK ومكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="f6cb2-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
