---
title: تطبيق إعدادات المخزون
description: يتناول هذا الموضوع إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fc81c190806a0bdb50569f526589cfa1808ce0c
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417428"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="150fc-103">تطبيق إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="150fc-103">Apply inventory settings</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="150fc-104">يتناول هذا الموضوع إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="150fc-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="150fc-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="150fc-105">Overview</span></span>

<span data-ttu-id="150fc-106">تحدد إعدادات المخزون ما إذا كان ينبغي فحص المخزون قبل إضافة المنتجات إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="150fc-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="150fc-107">وهي تحدد أيضًا رسائل ترويج البضائع المرتبطة بالمخزون، مثل "في المخزون" و "بقي عدد قليل فقط."</span><span class="sxs-lookup"><span data-stu-id="150fc-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="150fc-108">وتضمن هذه الإعدادات عدم إمكانية شراء منتج عندما ينفد من المخزون.</span><span class="sxs-lookup"><span data-stu-id="150fc-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="150fc-109">يوفر Dynamics 365 Commerce تقديرات عن التوفر الفعلي للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="150fc-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="150fc-110">للحصول على معلومات حول كيفية حساب التوفر الفعلي، راجع [حساب توفر المخزون لقنوات البيع بالتجزئة](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="150fc-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="150fc-111">في منشئ الموقع في Commerce، يمكن تعريف حدود ونطاقات المخزون لمنتج أو فئة.</span><span class="sxs-lookup"><span data-stu-id="150fc-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="150fc-112">وهي تحدد ما إذا كان من الممكن تصنيف المخزون في حالة "في المخزون" أو "نفد من المخزون" أو "مخزون قليل".</span><span class="sxs-lookup"><span data-stu-id="150fc-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="150fc-113">للاطلاع على التفاصيل، راجع [تكوين المخازن المؤقتة للمخزون ومستويات المخزون](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="150fc-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="150fc-114">إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="150fc-114">Inventory settings</span></span>

<span data-ttu-id="150fc-115">في Commerce، يتم تعريف إعدادات المخزون في **إعدادات الموقع \> الملحقات \> إدارة المخزون** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="150fc-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="150fc-116">هناك أربعة إعدادات للمخزون، أحدها أصبح قديمًا ومهملاً:</span><span class="sxs-lookup"><span data-stu-id="150fc-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="150fc-117">**تمكين فحص المخزون على التطبيق** – يقوم هذا الإعداد بتشغيل عملية فحص مخزون المنتج.</span><span class="sxs-lookup"><span data-stu-id="150fc-117">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="150fc-118">ستقوم عندئذٍ الوحدات‬ النمطية لصندوق الشراء‬ وسلة التسوق والانتقاء في المتجر‬ الصندوق بفحص مخزون المنتجات، وستسمح بإضافة منتج إلى سلة التسوق فقط إذا توفر المخزون.</span><span class="sxs-lookup"><span data-stu-id="150fc-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="150fc-119">**مستوى المخزون استنادًا إلى** – يحدد هذا الإعداد كيفية حساب مستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="150fc-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="150fc-120">القيم المتوفرة هي **الإجمالي المتوفر** و**الفعلي المتوفر** و**حد النفاد من المخزون**.</span><span class="sxs-lookup"><span data-stu-id="150fc-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="150fc-121">في Commerce، يمكن تعريف حدود ونطاقات المخزون لكل منتج أو فئة.</span><span class="sxs-lookup"><span data-stu-id="150fc-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="150fc-122">تقوم واجهات API للمخزون بإرجاع معلومات عن مخزون المنتج للخاصيتين **الإجمالي المتوفر** و**الفعلي المتوفر**.</span><span class="sxs-lookup"><span data-stu-id="150fc-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="150fc-123">يقرر بائع التجزئة ما إذا كان يجب استخدام قيمة **الإجمالي المتوفر** و**الفعلي المتوفر** لتحديد جرد المخزون والنطاقات المناظر للحالتين "في المخزون" و"نفد من المخزون".</span><span class="sxs-lookup"><span data-stu-id="150fc-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="150fc-124">قيمة **حد النفاد من المخزون** لإعداد **مستوى المخزون استنادًا إلى** هي قيمة قديمة ومهمة.</span><span class="sxs-lookup"><span data-stu-id="150fc-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="150fc-125">عند تحديد هذه القيمة، يتم تحديد جرد المخزون من نتائج قيمة **الإجمالي المتوفر**، ولكن يتم تعريف الحد بواسطة الإعداد الرقمي **حد النفاد من المخزون** الذي سيرد وصفه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="150fc-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="150fc-126">ينطبق إعداد الحد هذا على كافة المنتجات في موقع تجارة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="150fc-126">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="150fc-127">إذا كان المخزون أقل من رقم الحد، فسيُعتبر المنتج على أنه نفد من المخزون.</span><span class="sxs-lookup"><span data-stu-id="150fc-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="150fc-128">بخلاف ذلك، سيُعتبر على أنه في المخزون.</span><span class="sxs-lookup"><span data-stu-id="150fc-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="150fc-129">تعتبر قدرات قيمة **حد النفاد من المخزون** محدودة، ولا ننصح باستخدامها في الإصدار 10.0.12 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="150fc-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="150fc-130">**نطاقات المخزون** – يحدد هذا الإعداد نطاقات المخزون التي تظهر رسائلها على وحدات الموقع.</span><span class="sxs-lookup"><span data-stu-id="150fc-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="150fc-131">ينطبق هذا الإعداد فقط عندما تكون قيمة **الإجمالي المتوفر** أو قيمة **الفعلي المتوفر** محددة للإعداد **مستوى المخزون استنادًا إلى‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="150fc-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="150fc-132">القيم المتوفرة هي **الكل** و**مخزون قليل ونفد من المخزون** و**نفد من المخزون**.</span><span class="sxs-lookup"><span data-stu-id="150fc-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="150fc-133">عند تحديد **الكل**، ستظهر رسائل لجميع نطاقات المخزون، من الحالة "في المخزون" (الرسالة "متوفر") إلى "نفد من المخزون" (الرسالة "نفد من المخزون").</span><span class="sxs-lookup"><span data-stu-id="150fc-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="150fc-134">عند تحديد **مخزون قليل ونفد من المخزون‬‏‫**، ستظهر رسائل لجميع نطاقات المخزون باستثناء الحالة "في المخزون" (الرسالة "متوفر").</span><span class="sxs-lookup"><span data-stu-id="150fc-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="150fc-135">عند تحديد **نفد من المخزون**، ستظهر الرسالة "نفد من المخزون" فقط.</span><span class="sxs-lookup"><span data-stu-id="150fc-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="150fc-136">**حد النفاد من المخزون** – سيصبح الإعداد الرقمي القديم ساري المفعول فقط عند تحديد قيمة **حد النفاد من المخزون** للإعداد **مستوى المخزون استنادًا إلى**.</span><span class="sxs-lookup"><span data-stu-id="150fc-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="150fc-137">الوحدات النمطية التي تستخدم إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="150fc-137">Modules that use inventory settings</span></span>

<span data-ttu-id="150fc-138">تستخدم الوحدات النمطية صندوق الشراء وقائمة الأمنيات وسلة التسوق وأيقونة سلة التسوق إعدادات المخزون لإظهار نطاقات المخزون ورسائله.</span><span class="sxs-lookup"><span data-stu-id="150fc-138">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="150fc-139">تعرض الصورة التالية مثالاً لصفحة تفاصيل المنتج (PDP) التي تعرض رسالة التوفر في المخزون ("متوفر").</span><span class="sxs-lookup"><span data-stu-id="150fc-139">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![مثال عن وحدة PDP تتضمن رسالة التوفر "في المخزون"](./media/pdp-InStock.png)

<span data-ttu-id="150fc-141">تعرض الصورة التالية مثالاً لصفحة تفاصيل المنتج (PDP) التي تعرض الرسالة "نفد من المخزون".</span><span class="sxs-lookup"><span data-stu-id="150fc-141">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![مثال عن وحدة PDP تتضمن رسالة "نفد من المخزون"](./media/pdp-outofstock.png)

<span data-ttu-id="150fc-143">تعرض الصورة التالية مثالاً لسلة توسق تعرض رسالة التوفر في المخزون ("متوفر").‬</span><span class="sxs-lookup"><span data-stu-id="150fc-143">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![مثال عن وحدة سلة تسوق تتضمن رسالة التوفر "في المخزون"](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="150fc-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="150fc-145">Additional resources</span></span>

[<span data-ttu-id="150fc-146">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="150fc-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="150fc-147">تكوين المخازن المؤقتة للمخزون ومستويات المخزون</span><span class="sxs-lookup"><span data-stu-id="150fc-147">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="150fc-148">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="150fc-148">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="150fc-149">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="150fc-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="150fc-150">صفحات ووحدات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="150fc-150">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="150fc-151">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="150fc-151">Store selector module</span></span>](store-selector.md)
