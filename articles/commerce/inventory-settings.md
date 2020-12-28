---
title: تطبيق إعدادات المخزون
description: يتناول هذا الموضوع إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: dfa8b2bdc03e3698feda26932db757421097140d
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517054"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="1116c-103">تطبيق إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="1116c-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1116c-104">يتناول هذا الموضوع إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1116c-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1116c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1116c-105">Overview</span></span>

<span data-ttu-id="1116c-106">تحدد إعدادات المخزون ما إذا كان ينبغي فحص المخزون قبل إضافة المنتجات إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="1116c-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="1116c-107">وهي تحدد أيضًا رسائل ترويج البضائع المرتبطة بالمخزون، مثل "في المخزون" و "بقي عدد قليل فقط."</span><span class="sxs-lookup"><span data-stu-id="1116c-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="1116c-108">وتضمن هذه الإعدادات عدم إمكانية شراء منتج عندما ينفد من المخزون.</span><span class="sxs-lookup"><span data-stu-id="1116c-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="1116c-109">يوفر Dynamics 365 Commerce تقديرات عن التوفر الفعلي للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="1116c-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="1116c-110">للحصول على معلومات حول كيفية حساب التوفر الفعلي، راجع [حساب توفر المخزون لقنوات البيع بالتجزئة](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="1116c-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="1116c-111">في منشئ الموقع في Commerce، يمكن تعريف حدود ونطاقات المخزون لمنتج أو فئة.</span><span class="sxs-lookup"><span data-stu-id="1116c-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="1116c-112">وهي تحدد ما إذا كان من الممكن تصنيف المخزون في حالة "في المخزون" أو "نفد من المخزون" أو "مخزون قليل".</span><span class="sxs-lookup"><span data-stu-id="1116c-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="1116c-113">للاطلاع على التفاصيل، راجع [تكوين المخازن المؤقتة للمخزون ومستويات المخزون](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1116c-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1116c-114">يتوفر دعم حدود ونطاقات في Dynamics 365 Commerce الإصدار 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="1116c-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="1116c-115">إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="1116c-115">Inventory settings</span></span>

<span data-ttu-id="1116c-116">في Commerce، يتم تعريف إعدادات المخزون في **إعدادات الموقع \> الملحقات \> إدارة المخزون** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="1116c-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="1116c-117">هناك أربعة إعدادات للمخزون، أحدها أصبح قديمًا ومهملاً:</span><span class="sxs-lookup"><span data-stu-id="1116c-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="1116c-118">**تمكين فحص المخزون على التطبيق** – يقوم هذا الإعداد بتشغيل فحص مخزون المنتج.</span><span class="sxs-lookup"><span data-stu-id="1116c-118">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="1116c-119">ستقوم عندئذٍ الوحدات‬ النمطية لصندوق الشراء‬ وسلة التسوق والانتقاء في المتجر‬ الصندوق بفحص مخزون المنتجات، وستسمح بإضافة منتج إلى سلة التسوق فقط إذا توفر المخزون.</span><span class="sxs-lookup"><span data-stu-id="1116c-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="1116c-120">**مستوى المخزون استنادًا إلى** – يحدد هذا الإعداد كيفية حساب مستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="1116c-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="1116c-121">القيم المتوفرة هي **الإجمالي المتوفر** و **الفعلي المتوفر** و **حد النفاد من المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1116c-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="1116c-122">في Commerce، يمكن تعريف حدود ونطاقات المخزون لكل منتج أو فئة.</span><span class="sxs-lookup"><span data-stu-id="1116c-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="1116c-123">تقوم واجهات API للمخزون بإرجاع معلومات عن مخزون المنتج للخاصيتين **الإجمالي المتوفر** و **الفعلي المتوفر**.</span><span class="sxs-lookup"><span data-stu-id="1116c-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="1116c-124">يقرر بائع التجزئة ما إذا كان يجب استخدام قيمة **الإجمالي المتوفر** و **الفعلي المتوفر** لتحديد جرد المخزون والنطاقات المناظر للحالتين "في المخزون" و"نفد من المخزون".</span><span class="sxs-lookup"><span data-stu-id="1116c-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="1116c-125">قيمة **حد النفاد من المخزون** لإعداد **مستوى المخزون استنادًا إلى** هي قيمة قديمة ومهمة.</span><span class="sxs-lookup"><span data-stu-id="1116c-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="1116c-126">عند تحديد هذه القيمة، يتم تحديد جرد المخزون من نتائج قيمة **الإجمالي المتوفر**، ولكن يتم تعريف الحد بواسطة الإعداد الرقمي **حد النفاد من المخزون** الذي سيرد وصفه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="1116c-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="1116c-127">ينطبق إعداد الحد هذا على كافة المنتجات في موقع تجارة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1116c-127">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="1116c-128">إذا كان المخزون أقل من رقم الحد، فسيُعتبر المنتج على أنه نفد من المخزون.</span><span class="sxs-lookup"><span data-stu-id="1116c-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="1116c-129">بخلاف ذلك، سيُعتبر على أنه في المخزون.</span><span class="sxs-lookup"><span data-stu-id="1116c-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="1116c-130">تعتبر قدرات قيمة **حد النفاد من المخزون** محدودة، ولا ننصح باستخدامها في الإصدار 10.0.12 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="1116c-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="1116c-131">**نطاقات المخزون** – يحدد هذا الإعداد نطاقات المخزون التي تظهر رسائلها على وحدات الموقع.</span><span class="sxs-lookup"><span data-stu-id="1116c-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="1116c-132">ينطبق هذا الإعداد فقط عندما تكون قيمة **الإجمالي المتوفر** أو قيمة **الفعلي المتوفر** محددة للإعداد **مستوى المخزون استنادًا إلى‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="1116c-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="1116c-133">القيم المتوفرة هي **الكل** و **مخزون قليل ونفد من المخزون** و **نفد من المخزون**.</span><span class="sxs-lookup"><span data-stu-id="1116c-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="1116c-134">عند تحديد **الكل**، ستظهر رسائل لجميع نطاقات المخزون، من الحالة "في المخزون" (الرسالة "متوفر") إلى "نفد من المخزون" (الرسالة "نفد من المخزون").</span><span class="sxs-lookup"><span data-stu-id="1116c-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="1116c-135">عند تحديد **مخزون قليل ونفد من المخزون‬‏‫**، ستظهر رسائل لجميع نطاقات المخزون باستثناء الحالة "في المخزون" (الرسالة "متوفر").</span><span class="sxs-lookup"><span data-stu-id="1116c-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="1116c-136">عند تحديد **نفد من المخزون**، ستظهر الرسالة "نفد من المخزون" فقط.</span><span class="sxs-lookup"><span data-stu-id="1116c-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="1116c-137">**حد النفاد من المخزون** – سيصبح الإعداد الرقمي القديم ساري المفعول فقط عند تحديد قيمة **حد النفاد من المخزون** للإعداد **مستوى المخزون استنادًا إلى**.</span><span class="sxs-lookup"><span data-stu-id="1116c-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="1116c-138">تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="1116c-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="1116c-139">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="1116c-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1116c-140">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="1116c-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="1116c-141">الوحدات النمطية التي تستخدم إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="1116c-141">Modules that use inventory settings</span></span>

<span data-ttu-id="1116c-142">تستخدم الوحدات النمطية صندوق الشراء وقائمة الأمنيات وسلة التسوق وأيقونة سلة التسوق إعدادات المخزون لإظهار نطاقات المخزون ورسائله.</span><span class="sxs-lookup"><span data-stu-id="1116c-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="1116c-143">تعرض الصورة التالية مثالاً لصفحة تفاصيل المنتج (PDP) التي تعرض رسالة التوفر في المخزون ("متوفر").</span><span class="sxs-lookup"><span data-stu-id="1116c-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![مثال عن وحدة PDP تتضمن رسالة التوفر "في المخزون"](./media/pdp-InStock.png)

<span data-ttu-id="1116c-145">تعرض الصورة التالية مثالاً لصفحة تفاصيل المنتج (PDP) التي تعرض الرسالة "نفد من المخزون".</span><span class="sxs-lookup"><span data-stu-id="1116c-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![مثال عن وحدة PDP تتضمن رسالة "نفد من المخزون"](./media/pdp-outofstock.png)

<span data-ttu-id="1116c-147">تعرض الصورة التالية مثالاً لسلة توسق تعرض رسالة التوفر في المخزون ("متوفر").‬</span><span class="sxs-lookup"><span data-stu-id="1116c-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![مثال عن وحدة سلة تسوق تتضمن رسالة التوفر "في المخزون"](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="1116c-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1116c-149">Additional resources</span></span>

[<span data-ttu-id="1116c-150">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="1116c-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1116c-151">تكوين المخازن المؤقتة للمخزون ومستويات المخزون</span><span class="sxs-lookup"><span data-stu-id="1116c-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="1116c-152">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="1116c-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1116c-153">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="1116c-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1116c-154">صفحات ووحدات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="1116c-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="1116c-155">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="1116c-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="1116c-156">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="1116c-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
