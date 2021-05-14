---
title: تطبيق إعدادات المخزون
description: يتناول هذا الموضوع إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
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
ms.openlocfilehash: dd3db0039525c18521ad6a42b2f281976b7b236a
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937400"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="2113e-103">تطبيق إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="2113e-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2113e-104">يتناول هذا الموضوع إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2113e-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2113e-105">تحدد إعدادات المخزون ما إذا كان ينبغي فحص المخزون قبل إضافة المنتجات إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="2113e-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="2113e-106">وهي تحدد أيضًا رسائل ترويج البضائع المرتبطة بالمخزون، مثل "في المخزون" و "بقي عدد قليل فقط."</span><span class="sxs-lookup"><span data-stu-id="2113e-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="2113e-107">وتضمن هذه الإعدادات عدم إمكانية شراء منتج عندما ينفد من المخزون.</span><span class="sxs-lookup"><span data-stu-id="2113e-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="2113e-108">يوفر Dynamics 365 Commerce تقديرات عن التوفر الفعلي للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="2113e-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="2113e-109">للحصول على معلومات حول كيفية حساب التوفر الفعلي، راجع [حساب توفر المخزون لقنوات البيع بالتجزئة](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="2113e-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="2113e-110">في منشئ الموقع في Commerce، يمكن تعريف حدود ونطاقات المخزون لمنتج أو فئة.</span><span class="sxs-lookup"><span data-stu-id="2113e-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="2113e-111">وهي تحدد ما إذا كان من الممكن تصنيف المخزون في حالة "في المخزون" أو "نفد من المخزون" أو "مخزون قليل".</span><span class="sxs-lookup"><span data-stu-id="2113e-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="2113e-112">للاطلاع على التفاصيل، راجع [تكوين المخازن المؤقتة للمخزون ومستويات المخزون](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2113e-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2113e-113">يتوفر دعم حدود ونطاقات في Dynamics 365 Commerce الإصدار 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="2113e-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="2113e-114">إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="2113e-114">Inventory settings</span></span>

<span data-ttu-id="2113e-115">في Commerce، يتم تعريف إعدادات المخزون في **إعدادات الموقع \> الملحقات \> إدارة المخزون** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="2113e-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="2113e-116">هناك خمسة إعدادات للمخزون، أحدها أصبح قديمًا ومهملاً:</span><span class="sxs-lookup"><span data-stu-id="2113e-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="2113e-117">**تمكين فحص المخزون على التطبيق** – يقوم هذا الإعداد بتشغيل فحص مخزون المنتج.</span><span class="sxs-lookup"><span data-stu-id="2113e-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="2113e-118">ستقوم عندئذٍ الوحدات‬ النمطية لصندوق الشراء‬ وسلة التسوق والانتقاء في المتجر‬ الصندوق بفحص مخزون المنتجات، وستسمح بإضافة منتج إلى سلة التسوق فقط إذا توفر المخزون.</span><span class="sxs-lookup"><span data-stu-id="2113e-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="2113e-119">**مستوى المخزون استنادًا إلى** – يحدد هذا الإعداد كيفية حساب مستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="2113e-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="2113e-120">القيم المتوفرة هي **الإجمالي المتوفر** و **الفعلي المتوفر** و **حد النفاد من المخزون**.</span><span class="sxs-lookup"><span data-stu-id="2113e-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="2113e-121">في Commerce، يمكن تعريف حدود ونطاقات المخزون لكل منتج أو فئة.</span><span class="sxs-lookup"><span data-stu-id="2113e-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="2113e-122">تقوم واجهات API للمخزون بإرجاع معلومات عن مخزون المنتج للخاصيتين **الإجمالي المتوفر** و **الفعلي المتوفر**.</span><span class="sxs-lookup"><span data-stu-id="2113e-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="2113e-123">يقرر بائع التجزئة ما إذا كان يجب استخدام قيمة **الإجمالي المتوفر** و **الفعلي المتوفر** لتحديد جرد المخزون والنطاقات المناظر للحالتين "في المخزون" و"نفد من المخزون".</span><span class="sxs-lookup"><span data-stu-id="2113e-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="2113e-124">قيمة **حد النفاد من المخزون** لإعداد **مستوى المخزون استنادًا إلى** هي قيمة قديمة ومهمة.</span><span class="sxs-lookup"><span data-stu-id="2113e-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="2113e-125">عند تحديد هذه القيمة، يتم تحديد جرد المخزون من نتائج قيمة **الإجمالي المتوفر**، ولكن يتم تعريف الحد بواسطة الإعداد الرقمي **حد النفاد من المخزون** الذي سيرد وصفه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="2113e-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="2113e-126">ينطبق إعداد الحد هذا على كافة المنتجات في موقع تجارة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2113e-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="2113e-127">إذا كان المخزون أقل من رقم الحد، فسيُعتبر المنتج على أنه نفد من المخزون.</span><span class="sxs-lookup"><span data-stu-id="2113e-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="2113e-128">بخلاف ذلك، سيُعتبر على أنه في المخزون.</span><span class="sxs-lookup"><span data-stu-id="2113e-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="2113e-129">تعتبر قدرات قيمة **حد النفاد من المخزون** محدودة، ولا ننصح باستخدامها في الإصدار 10.0.12 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="2113e-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="2113e-130">**مستوى المخزون لمستودعات متعددة** – يتيح هذا الإعداد حساب مستوى المخزون مقابل المستودع الافتراضي أو المستودعات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="2113e-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="2113e-131">سيحسب خيار **على أساس المستودع الفردي** مستويات المخزون على أساس المستودع الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="2113e-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="2113e-132">بدلاً من ذلك، يمكن أن يشير موقع التجارة الإلكترونية إلى مستودعات متعددة لتسهيل التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="2113e-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="2113e-133">في هذه الحالة، يتم استخدام خيار **على أساس التجميع لمخازن الشحن والاستلام** للإشارة إلى توافر المخزون.</span><span class="sxs-lookup"><span data-stu-id="2113e-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="2113e-134">على سبيل المثال، عندما يشتري أحد العملاء صنفًا ويحدد "الشحن" كوضع التسليم، يمكن شحن الصنف من أي مستودع في مجموعة التنفيذ التي تحتوي على مخزون متاح.</span><span class="sxs-lookup"><span data-stu-id="2113e-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="2113e-135">ستعرض صفحة تفاصيل المنتج (PDP) رسالة "متوفر" للشحن إذا كان هناك مخزون في أي مستودع شحن متوفر في مجموعة التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="2113e-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="2113e-136">يتوفر إعداد **مستوى المخزون لمستودعات متعددة** اعتبارًا من إصدار Commerce رقم 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="2113e-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="2113e-137">إذا كنت تقوم بالتحديث من إصدار قديم من Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2113e-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="2113e-138">للاطلاع على التعليمات، راجع [تحديثات مكتبة الوحدات وSDK](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="2113e-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="2113e-139">**نطاقات المخزون** – يحدد هذا الإعداد نطاقات المخزون التي تظهر رسائلها على وحدات الموقع.</span><span class="sxs-lookup"><span data-stu-id="2113e-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="2113e-140">ينطبق هذا الإعداد فقط عندما تكون قيمة **الإجمالي المتوفر** أو قيمة **الفعلي المتوفر** محددة للإعداد **مستوى المخزون استنادًا إلى‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="2113e-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="2113e-141">القيم المتوفرة هي **الكل** و **مخزون قليل ونفد من المخزون** و **نفد من المخزون**.</span><span class="sxs-lookup"><span data-stu-id="2113e-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="2113e-142">عند تحديد **الكل**، ستظهر رسائل لجميع نطاقات المخزون، من الحالة "في المخزون" (الرسالة "متوفر") إلى "نفد من المخزون" (الرسالة "نفد من المخزون").</span><span class="sxs-lookup"><span data-stu-id="2113e-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="2113e-143">عند تحديد **مخزون قليل ونفد من المخزون‬‏‫**، ستظهر رسائل لجميع نطاقات المخزون باستثناء الحالة "في المخزون" (الرسالة "متوفر").</span><span class="sxs-lookup"><span data-stu-id="2113e-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="2113e-144">عند تحديد **نفد من المخزون**، ستظهر الرسالة "نفد من المخزون" فقط.</span><span class="sxs-lookup"><span data-stu-id="2113e-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="2113e-145">**حد النفاد من المخزون** – سيصبح الإعداد الرقمي القديم ساري المفعول فقط عند تحديد قيمة **حد النفاد من المخزون** للإعداد **مستوى المخزون استنادًا إلى**.</span><span class="sxs-lookup"><span data-stu-id="2113e-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="2113e-146">تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="2113e-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="2113e-147">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2113e-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="2113e-148">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="2113e-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="2113e-149">الوحدات النمطية التي تستخدم إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="2113e-149">Modules that use inventory settings</span></span>

<span data-ttu-id="2113e-150">تستخدم الوحدات النمطية صندوق الشراء وقائمة الأمنيات وسلة التسوق وأيقونة سلة التسوق إعدادات المخزون لإظهار نطاقات المخزون ورسائله.</span><span class="sxs-lookup"><span data-stu-id="2113e-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="2113e-151">في المثال الموضح في الرسم التوضيحي التالي، تعرض PDP رسالة في المخزن ("متوفرة").</span><span class="sxs-lookup"><span data-stu-id="2113e-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![مثال عن وحدة PDP تتضمن رسالة التوفر "في المخزون"](./media/pdp-InStock.png)

<span data-ttu-id="2113e-153">في المثال الموضح في الرسم التوضيحي التالي، تعرض PDP رسالة "نفاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="2113e-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![مثال عن وحدة PDP تتضمن رسالة "نفد من المخزون"](./media/pdp-outofstock.png)

<span data-ttu-id="2113e-155&quot;>في المثال الموضح في الرسم التوضيحي التالي، تعرض عربة التسوق رسالة في المخزن (&quot;متوفرة").</span><span class="sxs-lookup"><span data-stu-id="2113e-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![مثال عن وحدة سلة تسوق تتضمن رسالة التوفر "في المخزون"](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="2113e-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2113e-157">Additional resources</span></span>

[<span data-ttu-id="2113e-158">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2113e-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2113e-159">تكوين المخازن المؤقتة للمخزون ومستويات المخزون</span><span class="sxs-lookup"><span data-stu-id="2113e-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="2113e-160">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="2113e-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2113e-161">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="2113e-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2113e-162">صفحات ووحدات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="2113e-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="2113e-163">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="2113e-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="2113e-164">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2113e-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
