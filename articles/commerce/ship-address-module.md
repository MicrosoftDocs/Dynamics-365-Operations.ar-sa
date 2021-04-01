---
title: الوحدة النمطية لعنوان الشحن
description: يتناول هذا الموضوع الوحدة النمطية لعنوان الشحن ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234403"
---
# <a name="shipping-address-module"></a><span data-ttu-id="3b347-103">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="3b347-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b347-104">يصف هذا الموضوع الوحدة النمطية لعنوان الشحن ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b347-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3b347-105">تسمح الوحدة النمطية لعنوان الشحن للعملاء بإضافة أو تحديد عنوان الشحن لأحد الأوامر أثناء سير مهام السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="3b347-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="3b347-106">إذا قام العميل بتسجيل الدخول، فسوف يتم عرض أي عناوين تم حفظها في وقت سابق لهذا العميل، ويمكن للعميل الاختيار من بينها.</span><span class="sxs-lookup"><span data-stu-id="3b347-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="3b347-107">ويُمكن للعميل أيضًا إضافة عنوان جديد.</span><span class="sxs-lookup"><span data-stu-id="3b347-107">The customer can also add a new address.</span></span> <span data-ttu-id="3b347-108">يتم استخدام الوحدة النمطية لعنوان الشحن لكافة الأصناف في الأمر التي تتطلب الشحن.</span><span class="sxs-lookup"><span data-stu-id="3b347-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="3b347-109">يمكن تحديد تنسيقات عناوين الشحن في مركز Commerce الرئيسي لكل بلد أو منطقة، وعندئذ تقوم الوحدة النمطية لعنوان الشحن بفرض القواعد الخاصة بالبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="3b347-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="3b347-110">عندما يقوم العملاء بإدخال عنوان شحن أثناء سير مهام السداد مع الخروج، يمكنهم حفظ العنوان كعنوان رئيسي.</span><span class="sxs-lookup"><span data-stu-id="3b347-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="3b347-111">يظهر هذا الخيار فقط إذا سجل العميل دخوله.</span><span class="sxs-lookup"><span data-stu-id="3b347-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="3b347-112">وعلى الرغم من أن الوحدة النمطية لعنوان الشحن لا توفر ميزة التحقق من صحة العنوان، إلا أنه يُمكن تطبيق هذه الميزة من خلال التخصيص.</span><span class="sxs-lookup"><span data-stu-id="3b347-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="3b347-113">يبين الشكل التوضيحي التالي مثالاُ عن وحدة عنوان شحن جديدة في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="3b347-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![مثال عن الوحدة النمطية لعنوان الشحن على صفحة السداد مع الخروج](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="3b347-115">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="3b347-115">Module properties</span></span>

| <span data-ttu-id="3b347-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="3b347-116">Property name</span></span> | <span data-ttu-id="3b347-117">القيم</span><span class="sxs-lookup"><span data-stu-id="3b347-117">Values</span></span> | <span data-ttu-id="3b347-118">الوصف</span><span class="sxs-lookup"><span data-stu-id="3b347-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3b347-119">العنوان</span><span class="sxs-lookup"><span data-stu-id="3b347-119">Heading</span></span> | <span data-ttu-id="3b347-120">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="3b347-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3b347-121">عنوان اختياري للوحدة النمطية لعنوان الشحن.</span><span class="sxs-lookup"><span data-stu-id="3b347-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="3b347-122">إظهار نوع العنوان</span><span class="sxs-lookup"><span data-stu-id="3b347-122">Show address type</span></span> | <span data-ttu-id="3b347-123">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="3b347-123">**True** or **False**</span></span> | <span data-ttu-id="3b347-124">إذا تم تعيين هذه الخاصية الاختيارية إلى **صواب**، فسيظهر نوع عنوان مثل **المنزل** أو **العمل**.</span><span class="sxs-lookup"><span data-stu-id="3b347-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="3b347-125">إذا لم يتم تحديد نوع عنوان، سيتم حفظ العنوان تلقائيًا **النوع**=**غير ذلك**.</span><span class="sxs-lookup"><span data-stu-id="3b347-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="3b347-126">تمكين الاقتراح التلقائي</span><span class="sxs-lookup"><span data-stu-id="3b347-126">Enable auto suggestion</span></span>| <span data-ttu-id="3b347-127">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="3b347-127">**True** or **False**</span></span> | <span data-ttu-id="3b347-128">إذا تم تعيين هذه الخاصية الاختيارية على **True**، سيتم توفير اقتراحات العناوين التلقائية.</span><span class="sxs-lookup"><span data-stu-id="3b347-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="3b347-129">يتم تشغيل هذه الاقتراحات بواسطة خرائط Bing.</span><span class="sxs-lookup"><span data-stu-id="3b347-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="3b347-130">للحصول على معلومات حول كيفية إعداد تكامل خرائط Bing للموقع الخاص بك، راجع [الوحدة النمطية لمحدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="3b347-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="3b347-131">تتوفر هذه الميزة اعتبارًا من إصدار Commerce رقم 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="3b347-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="3b347-132">خيارات الاقتراح التلقائي</span><span class="sxs-lookup"><span data-stu-id="3b347-132">Auto suggest options</span></span>| <span data-ttu-id="3b347-133">رقم A</span><span class="sxs-lookup"><span data-stu-id="3b347-133">A number</span></span>| <span data-ttu-id="3b347-134">في حالة تمكين اقتراحات العنوان التلقائي، يمكنك تحديد خيارات إضافية، مثل الحد الأقصى لعدد الاقتراحات التي يجب توفيرها.</span><span class="sxs-lookup"><span data-stu-id="3b347-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="3b347-135">إضافة الوحدة النمطية لعنوان الشحن إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="3b347-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="3b347-136">يمكن إضافة وحدة نمطية لعنوان الشحن فقط إلى وحدة نمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="3b347-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="3b347-137">لمزيد من المعلومات حول كيفية تكوين الوحدة النمطية لعنوان الشحن وإضافتها إلى صفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="3b347-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b347-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3b347-138">Additional resources</span></span>

[<span data-ttu-id="3b347-139">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="3b347-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3b347-140">الوحدة النمطية لرمز عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="3b347-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3b347-141">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="3b347-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3b347-142">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="3b347-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="3b347-143">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="3b347-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3b347-144">الوحدة النمطية لمعلومات الاستلام</span><span class="sxs-lookup"><span data-stu-id="3b347-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="3b347-145">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="3b347-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3b347-146">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="3b347-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="3b347-147">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="3b347-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]