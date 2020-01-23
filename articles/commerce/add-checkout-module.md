---
title: الوحدة النمطية للسداد مع الخروج
description: يوضح هذا الموضوع كيفية إضافة الوحدة النمطية للسداد مع الخروج إلى صفحة، وتعيين الخصائص المطلوبة.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697073"
---
# <a name="checkout-module"></a><span data-ttu-id="576d9-103">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="576d9-103">Checkout module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="576d9-104">يوضح هذا الموضوع كيفية إضافة الوحدة النمطية للسداد مع الخروج إلى صفحة، وتعيين الخصائص المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="576d9-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="576d9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="576d9-105">Overview</span></span>

<span data-ttu-id="576d9-106">تُمثل الوحدة النمطية للسداد مع الخروج حاوية خاصة تستضيف كافة الوحدات المطلوبة لإنشاء أمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-106">A checkout module is a special container that hosts all the modules that are required to create an order.</span></span> <span data-ttu-id="576d9-107">ويُمكن أن تشمل الوحدة النمطية للسداد مع الخروج التي تُعالج عنوان الشحن وأساليب الشحن ومعلومات الفوترة وملخص الأمر والمعلومات الأخرى ذات الصلة بأمر العميل.</span><span class="sxs-lookup"><span data-stu-id="576d9-107">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to a customer order.</span></span> <span data-ttu-id="576d9-108">وهي توضح التدفق خطوة بخطوة الذي يستخدمه العميل لإدخال كافة المعلومات ذات الصلة لإجراء عملية شراء.</span><span class="sxs-lookup"><span data-stu-id="576d9-108">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span>

<span data-ttu-id="576d9-109">تعرض الوحدة النمطية للسداد مع الخروج البيانات بناءً على مُعرف سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="576d9-109">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="576d9-110">يتم حفظ مُعرف سلة التسوق كملف تعريف ارتباط للمستعرض.</span><span class="sxs-lookup"><span data-stu-id="576d9-110">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="576d9-111">ويُكون مُعرف سلة التسوق مطلوبًا لعرض المعلومات في الوحدة النمطية للسداد مع الخروج، مثل الأصناف في الأمر والمبلغ الإجمالي والخصومات.</span><span class="sxs-lookup"><span data-stu-id="576d9-111">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span>

## <a name="checkout-module-properties"></a><span data-ttu-id="576d9-112">خصائص الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="576d9-112">Checkout module properties</span></span>

<span data-ttu-id="576d9-113">وتستضيف الوحدة النمطية للسداد مع الخروج مجموعة من الوحدات داخلها.</span><span class="sxs-lookup"><span data-stu-id="576d9-113">A checkout module hosts a set of modules inside it.</span></span> <span data-ttu-id="576d9-114">وتسمح لك خاصية العرض بتحديد إذا ما كانت العناصر في الوحدة النمطية للسداد مع الخروج يجب أن تتناسب مع عرضها أو ملء الشاشة.</span><span class="sxs-lookup"><span data-stu-id="576d9-114">A width property lets you specify whether the items in the checkout module should fit the width of it or fill the screen.</span></span>

<span data-ttu-id="576d9-115">ويكون للوحدة النمطية للسداد مع الخروج فتحات متعددة، مثل فتحة **معلومات السداد مع الخروج** ، وفتحة **ملخص الأمر** وفتحة **وضع أمر**.</span><span class="sxs-lookup"><span data-stu-id="576d9-115">A checkout module has multiple slots, such as a **Checkout information** slot, an **Order summary** slot, and a **Place order** slot.</span></span> <span data-ttu-id="576d9-116">تدعم كل فتحة مجموعة من الوحدات التي سوف تظهر في تخطيط معين في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="576d9-116">Each slot supports a set of modules that will appear in a specific layout on the page.</span></span> <span data-ttu-id="576d9-117">على سبيل المثال، تحتوي فتحة **معلومات السداد مع الخروج** جميع الوحدات المطلوبة لتشغيل عملية سداد مع خروج، مثل الوحدات الخاصة بعنوان الشحن وطريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="576d9-117">For example, the **Checkout information** slot contains all the modules that are required to trigger a checkout, such as modules for the shipping address and payment method.</span></span> <span data-ttu-id="576d9-118">تعرض فتحة **ملخص الأمر** ملخص الأمر وتدعم إجراء وضع الأمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-118">The **Order summary** slot shows an order summary and supports the action for placing the order.</span></span> <span data-ttu-id="576d9-119">وتدعم أيضًا فتحة **وضع الأمر** الإجراء الخاص بوضع الأمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-119">The **Place order** slot also supports the action for placing the order.</span></span> <span data-ttu-id="576d9-120">يُمكن تحديد وحدات وضع الأمر في فتحتين لتحسين عملية وضع الأوامر من أنظمة أساسية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="576d9-120">Place order modules can be defined in two slots to optimize the process of placing orders from various platforms.</span></span>

### <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="576d9-121">الوحدات التي يُمكن استخدامها في الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="576d9-121">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="576d9-122">**عنوان الشحن** - تتيح هذه الوحدة للعميل إضافة أو تحديد عنوان الشحن لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="576d9-122">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="576d9-123">إذا قام العميل بتسجيل الدخول، فسوف يتم عرض أي عناوين تم حفظها مسبقًا لهذا العميل.</span><span class="sxs-lookup"><span data-stu-id="576d9-123">If the customer is signed in, any addresses that were previously saved for that customer are shown.</span></span> <span data-ttu-id="576d9-124">يمكن للعميل عندئذ الاختيار من بين هذه العناوين.</span><span class="sxs-lookup"><span data-stu-id="576d9-124">The customer can then select among those addresses.</span></span> <span data-ttu-id="576d9-125">ويُمكن للعميل أيضًا إضافة عنوان جديد.</span><span class="sxs-lookup"><span data-stu-id="576d9-125">The customer can also add a new address.</span></span> <span data-ttu-id="576d9-126">يتم استخدام عنوان الشحن لكافة الأصناف في الأمر الذي يتطلب الشحن.</span><span class="sxs-lookup"><span data-stu-id="576d9-126">The shipping address is used for all the items in the order that require shipping.</span></span> <span data-ttu-id="576d9-127">ولا يُمكن تخصيصه لأصناف البنود الفردية.</span><span class="sxs-lookup"><span data-stu-id="576d9-127">It can't be customized for individual line items.</span></span> <span data-ttu-id="576d9-128">يتم تحديد تنسيقات عناوين الشحن لكل بلد أو منطقة، ويتم فرض القواعد الخاصة بالبلد/المنطقة بواسطة هذه الوحدة.</span><span class="sxs-lookup"><span data-stu-id="576d9-128">Shipping address formats are defined for each country or region, and the country/region-specific rules are enforced by this module.</span></span> <span data-ttu-id="576d9-129">وعلى الرغم من أن هذه الوحدة لا توفر ميزة التحقق من صحة العنوان، إلا أنه يُمكن تطبيق ميزة التحقق من صحة العنوان من خلال التخصيص.</span><span class="sxs-lookup"><span data-stu-id="576d9-129">Although this module doesn't provide address validation, address validation can be implemented through customization.</span></span> <span data-ttu-id="576d9-130">إذا كان الأمر يشتمل فقط الأصناف التي سوف يتم انتقاؤها في المتجر، فمن ثم يتم إخفاء هذه الوحدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="576d9-130">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>
- <span data-ttu-id="576d9-131">**خيارات التسليم** - وتتيح هذه الوحدة للعميل تحديد خيار التسليم لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="576d9-131">**Delivery options** – This module lets a customer select a delivery option for an order.</span></span> <span data-ttu-id="576d9-132">وتعتمد خيارات التسليم علي عنوان الشحن.</span><span class="sxs-lookup"><span data-stu-id="576d9-132">Delivery options are based on the shipping address.</span></span> <span data-ttu-id="576d9-133">وفي حالة تغيير عنوان الشحن، يتعين استرداد خيارات التسليم مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="576d9-133">If the shipping address is changed, the delivery options must be retrieved again.</span></span> <span data-ttu-id="576d9-134">إذا كان الأمر يشتمل فقط الأصناف التي سوف يتم انتقاؤها في المتجر، فمن ثم يتم إخفاء هذه الوحدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="576d9-134">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>
- <span data-ttu-id="576d9-135">**حاوية قسم السداد مع الخروج** - تُمثل هذه حاوية يُمكنك وضع وحدات متعددة داخلها لإنشاء قسم داخل تدفق السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="576d9-135">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="576d9-136">على سبيل المثال، يُمكنك وضع كافة الوحدات المرتبطة بالدفع داخل هذه الحاوية لجعلها تظهر كقسم واحد.</span><span class="sxs-lookup"><span data-stu-id="576d9-136">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="576d9-137">تؤثر هذه الوحدة فقط على تخطيط التدفق.</span><span class="sxs-lookup"><span data-stu-id="576d9-137">This module affects only the layout of the flow.</span></span>
- <span data-ttu-id="576d9-138">**بطاقة الهدايا**- تتيح هذه الوحدة للعميل الدفع لأحد الأوامر باستخدام بطاقة هدايا.</span><span class="sxs-lookup"><span data-stu-id="576d9-138">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="576d9-139">فهو يدعم فقط بطاقات الهدايا من Microsoft Dynamics 365 Commerce فقط.</span><span class="sxs-lookup"><span data-stu-id="576d9-139">It supports only Microsoft Dynamics 365 Commerce gift cards.</span></span> <span data-ttu-id="576d9-140">ويُمكن استخدام بطاقة هدايا واحدة أو أكثر لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="576d9-140">One or more gift cards can be applied to an order.</span></span> <span data-ttu-id="576d9-141">إذا لم يُغطي رصيد بطاقة الهدايا المبلغ في سلة التسوق، فيُمكن دمج بطاقة الهدايا مع طريقة دفع أخرى.</span><span class="sxs-lookup"><span data-stu-id="576d9-141">If the balance of the gift card doesn't cover the amount in the cart, the gift card can be combined with another payment method.</span></span> <span data-ttu-id="576d9-142">ولا يُمكن استرجاع بطاقات الهدايا إلا إذا قام العميل بتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="576d9-142">Gift cards can be redeemed only if the customer is signed in.</span></span>
- <span data-ttu-id="576d9-143">**نقاط الولاء** - تسمح هذه الوحدة للعميل بدفع في مقابل أمر باستخدام نقاط الولاء.</span><span class="sxs-lookup"><span data-stu-id="576d9-143">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="576d9-144">وتوفر ملخصًا للنقاط المتاحة والنقاط منتهية الصلاحية، كما تتيح للعميل تحديد عدد النقاط المطلوب استردادها.</span><span class="sxs-lookup"><span data-stu-id="576d9-144">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="576d9-145">إذا لم يقم العميل بتسجيل الدخول أو إذا لم يكن عضوًا في برنامج الولاء، أو إذا كان المبلغ  الإجمالي في سلة التسوق هو 0 (صفر)، فمن ثم يتم إخفاء هذه الوحدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="576d9-145">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>
- <span data-ttu-id="576d9-146">**بطاقة الائتمان**- تتيح هذه الوحدة للعميل الدفع لأحد الأوامر باستخدام بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="576d9-146">**Credit card** – This module lets a customer pay for an order by using a credit card.</span></span> <span data-ttu-id="576d9-147">إذا كان إجمالي المبلغ في سلة التسوق مُغطى من خلال نقاط الولاء أو بطاقة هدايا أو إذا كان 0 (صفر)، يتم إخفاء هذه الوحدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="576d9-147">If the total amount in the cart is covered by loyalty points or a gift card, or if it's 0 (zero), this module is automatically hidden.</span></span> <span data-ttu-id="576d9-148">يتم توفير تكامل بطاقة الائتمان بواسطة موصل دفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="576d9-148">Credit card integration is provided by the Adyen payment connector.</span></span> <span data-ttu-id="576d9-149">لمزيد من المعلومات حول كيفية استخدام هذا الموصل، راجع [موصل دفع Ayden](https://).</span><span class="sxs-lookup"><span data-stu-id="576d9-149">For more information about how to use this connector, see [Adyen payment connector](https://).</span></span>
- <span data-ttu-id="576d9-150">**عنوان الفوترة** - تتيح هذه الوحدة للعميل تقديم معلومات الفوترة.</span><span class="sxs-lookup"><span data-stu-id="576d9-150">**Billing address** – This module lets a customer provide billing information.</span></span> <span data-ttu-id="576d9-151">تتم مُعالجة هذه المعلومات مع معلومات بطاقة الائتمان بواسطة Adyen.</span><span class="sxs-lookup"><span data-stu-id="576d9-151">This information is processed, together with the credit card information, by Adyen.</span></span> <span data-ttu-id="576d9-152">وتتضمن هذه الوحدة خيارًا يسمح للعملاء باستخدام عنوان الفوترة الخاص بهم كعنوان الشحن.</span><span class="sxs-lookup"><span data-stu-id="576d9-152">This module includes an option that lets customers use their billing address as the shipping address.</span></span>
- <span data-ttu-id="576d9-153">**معلومات الاتصال**- تُتيح هذه الوحدة للعميل إضافة أو تغيير معلومات الاتصال (عنوان البريد الإلكتروني) لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="576d9-153">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>
- <span data-ttu-id="576d9-154">**وضع أمر** - تتيح هذه الوحدة للعميل وضع أمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-154">**Place order** – This module lets a customer place an order.</span></span>
- <span data-ttu-id="576d9-155">**كتلة تنسيق المحتوى** - تحتوي هذه الوحدة على أي مُراسلات يتم التحكم فيها بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="576d9-155">**Content rich block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="576d9-156">على سبيل المثال، قد يحتوي على رسالة تنص على، "للمشاكل الخاصة بطلبك، يُرجى الاتصال بالرقم التالي 1-800- شركة الاتحاد للتصنيع."</span><span class="sxs-lookup"><span data-stu-id="576d9-156">For example, it might contain a message that states, "For issues with your order, please contact 1-800-FABRIKAM."</span></span> 
- <span data-ttu-id="576d9-157">**ملخص الأمر** - تعرض هذه الوحدة تصنيف تكلفة الأمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-157">**Order summary** – This module shows the cost breakdown of an order.</span></span>
- <span data-ttu-id="576d9-158">**أصناف بند الأمر** - تعرض هذه الوحدة ملخص للأصناف التي سوف يتم تضمينها في أمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-158">**Order line items** – This module shows a summary of the items that will be included in an order.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="576d9-159">تفاعل خادم Retail</span><span class="sxs-lookup"><span data-stu-id="576d9-159">Retail server interaction</span></span>

<span data-ttu-id="576d9-160">يتم تخزين معظم معلومات السداد مع الخروج، مثل عنوان الشحن وطريقة الشحن في سلة التسوق ومُعالجتها كجزء من الأمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-160">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="576d9-161">والاستثناء الوحيد هو معلومات بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="576d9-161">The only exception is the credit card information.</span></span> <span data-ttu-id="576d9-162">تتم مُعالجة هذه المعلومات مُباشرة باستخدام موصل دفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="576d9-162">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="576d9-163">يتم تخويل الدفع ولكن لا يتم قيده.</span><span class="sxs-lookup"><span data-stu-id="576d9-163">The payment is authorized but isn't charged.</span></span>

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a><span data-ttu-id="576d9-164">إضافة الوحدة النمطية للسداد مع الخروج إلى صفحة جديدة وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="576d9-164">Add a checkout module to a new page and set the required properties</span></span>

<span data-ttu-id="576d9-165">لإضافة الوحدة النمطية للسداد مع الخروج إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="576d9-165">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="576d9-166">انتقل إلى **جزء\> جزء جديد** ، وقم بتسمية الجزء الجديد **جزء السداد مع الخروج**.</span><span class="sxs-lookup"><span data-stu-id="576d9-166">Go to **Fragment \> New Fragment**, and name the new fragment **Checkout fragment**.</span></span>
1. <span data-ttu-id="576d9-167">إضافة الوحدة النمطية للسداد مع الخروج إلى الجزء.</span><span class="sxs-lookup"><span data-stu-id="576d9-167">Add a checkout module to the fragment.</span></span>
1. <span data-ttu-id="576d9-168">إضافة عنوان إلى الوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="576d9-168">Add a heading to the checkout module.</span></span>
1. <span data-ttu-id="576d9-169">في فتحة **معلومات السداد مع الخروج** ، أضف وحدات عنوان الشحن وخيارات التسليم وحاوية قسم السداد مع الخروج ومعلومات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="576d9-169">In the **Checkout information** slot, add shipping address, delivery options, checkout section container, and contact information modules.</span></span> <span data-ttu-id="576d9-170">يجب أن يوجد الآن أربعة مقاطع في فتحة **معلومات السداد مع الخروج**.</span><span class="sxs-lookup"><span data-stu-id="576d9-170">There should now be four sections in the **Checkout information** slot.</span></span>
1. <span data-ttu-id="576d9-171">في وحدة حاوية قسم الخروج مع السداد، قم بإضافة وحدات بطاقة الهدايا ونقاط الولاء وبطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="576d9-171">In the checkout section container module, add gift card, loyalty points, and credit card modules.</span></span> <span data-ttu-id="576d9-172">وبهذه الطريقة، فسوف تتأكد من ظهور جميع أساليب الدفع في أحد الأقسام.</span><span class="sxs-lookup"><span data-stu-id="576d9-172">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="576d9-173">في فتحة **ملخص الأمر** ، قم بإضافة وحدات ملخص الأمر ووضع الأمر وكتلة تنسيق المحتوى.</span><span class="sxs-lookup"><span data-stu-id="576d9-173">In the **Order summary** slot, add order summary, place order, and content rich block modules.</span></span>
1. <span data-ttu-id="576d9-174">في وحدة كتلة تنسيق المحتوى، قم بإضافة النص التالي: **للاستفسارات الخاصة بطلبك،، اتصل بالرقم التالي 1-800- شركة الاتحاد للتصنيع.**</span><span class="sxs-lookup"><span data-stu-id="576d9-174">In the content rich block module, add the following text: **For questions about your order, contact 1-800-FABRIKAM.**</span></span>
1. <span data-ttu-id="576d9-175">في فتحة **وضع أمر** ، قم بإضافة وحدة وضع أمر.</span><span class="sxs-lookup"><span data-stu-id="576d9-175">In the **Place order** slot, add a place order module.</span></span>
1. <span data-ttu-id="576d9-176">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="576d9-176">Select **Save**.</span></span> <span data-ttu-id="576d9-177">قد لا يتم عرض بعض الوحدات في المعاينة، لأنها لا تحتوي على سياق سلة تسوق.</span><span class="sxs-lookup"><span data-stu-id="576d9-177">Some modules might not be rendered in the preview, because they don't have a cart context.</span></span>
1. <span data-ttu-id="576d9-178">قم بإيداع الجزء ونشره.</span><span class="sxs-lookup"><span data-stu-id="576d9-178">Check the fragment in, and publish it.</span></span>
1. <span data-ttu-id="576d9-179">قم بإنشاء قالب يستخدم جزء السداد مع الخروج جديد.</span><span class="sxs-lookup"><span data-stu-id="576d9-179">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="576d9-180">قم بإنشاء صفحة السداد مع الخروج التي تستخدم القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="576d9-180">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="576d9-181">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="576d9-181">Additional resources</span></span>

[<span data-ttu-id="576d9-182">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="576d9-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="576d9-183">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="576d9-183">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="576d9-184">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="576d9-184">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="576d9-185">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="576d9-185">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="576d9-186">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="576d9-186">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="576d9-187">الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="576d9-187">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="576d9-188">الوحدة النمطية لتذييل الصفحة</span><span class="sxs-lookup"><span data-stu-id="576d9-188">Footer module</span></span>](author-footer-module.md)