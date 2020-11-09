---
title: الوحدة النمطية للدفع
description: يتناول هذا الموضوع الوحدة النمطية للدفع ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055371"
---
# <a name="payment-module"></a><span data-ttu-id="92053-103">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="92053-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92053-104">يتناول هذا الموضوع الوحدة النمطية للدفع ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="92053-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="92053-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="92053-105">Overview</span></span>

<span data-ttu-id="92053-106">تتيح الوحدة النمطية للدفع للعملاء بتسديد قيمة الأوامر باستخدام بطاقة الائتمان أو بطاقة الخصم.</span><span class="sxs-lookup"><span data-stu-id="92053-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="92053-107">يتم توفير سلامة الدفع لهذه الوحدة النمطية باستخدام موصل دفع Dynamics 365 لـ Adyen‬.</span><span class="sxs-lookup"><span data-stu-id="92053-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="92053-108">للحصول على معلومات حول كيفية إعداد وتكوين موصل الدفع، راجع [موصل دفع Dynamics 365 لـ Adyen‬](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="92053-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="92053-109">تستضيف الوحدة النمطية للدفع معلومات الدفع التي يتم تقديمها عبر Adyen في اطار HTML مضمن (iframe).</span><span class="sxs-lookup"><span data-stu-id="92053-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="92053-110">تتفاعل الوحدة النمطية للدفع مع Commerce Scale Unit لاسترداد معلومات دفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="92053-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="92053-111">وكجزء من تفاعل Commerce Scale Unit، بإمكان الوحدة النمطية للدفع أن تسمح بتقديم معلومات عنوان الفوترة إما في iframe أو كوحدة نمطية منفصلة.</span><span class="sxs-lookup"><span data-stu-id="92053-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="92053-112">في نسق Fabrikam، يظهر عنوان الفوترة في وحدة نمطية منفصلة.</span><span class="sxs-lookup"><span data-stu-id="92053-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="92053-113">يسمح هذا الأسلوب بالحصول على مرونة أكبر في التنسيق، نظرًا لإمكانية عرض بنود العنوان بحيث تشبه بنود عنوان الشحن.</span><span class="sxs-lookup"><span data-stu-id="92053-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="92053-114">وتتيح أيضًا الوحدة النمطية للدفع للعملاء الذين سجلوا دخولهم بحفظ معلومات الدفع الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="92053-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="92053-115">تُحفظ معلومات الدفع وعنوان الفوترة وتتم إدارتها بواسطة موصل دفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="92053-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="92053-116">تغطي الوحدة النمطية للدفع مصاريف الأوامر التي لم تتم تغطيتها بواسطة نقاط الولاء أو بطاقة هدايا.</span><span class="sxs-lookup"><span data-stu-id="92053-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="92053-117">إذا تمت تغطية القيمة الإجمالية للأمر بواسطة نقاط الولاء أو أرصدة بطاقات الهدايا، فستكون الوحدة النمطية للدفع مخفية، وسيتمكن العميل من تسجيل الأمر من دونها.</span><span class="sxs-lookup"><span data-stu-id="92053-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="92053-118">يدعم أيضًا موصل دفع Adyen مصادقة العملاء القوية (SCA)</span><span class="sxs-lookup"><span data-stu-id="92053-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="92053-119">يتطلب جزء من التوجيه 2.0 لخدمات الدفع (PSD2.0) في الاتحاد الأوروبي أن تتم مصادقة المتسوقين عبر الإنترنت خارج تجربة التسوق الخاصة بهم عبر الإنترنت عندما يستخدمون طريقة دفع إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="92053-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="92053-120">اثناء سير مهام السداد مع الخروج، يُعاد توجيه العملاء إلى موقع البنك الذي يتعاملون معه.</span><span class="sxs-lookup"><span data-stu-id="92053-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="92053-121">وبعد المصادقة، يُعاد توجيههم إلى سير مهام السداد مع الخروج في Commerce.</span><span class="sxs-lookup"><span data-stu-id="92053-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="92053-122">أثناء عملية إعادة التوجيه هذه، سيستمر وجود المعلومات التي أدخلها العميل في سير مهام السداد مع تسجيل الخروج (على سبيل المثال، عنوان الشحن وخيارات التسليم ومعلومات بطاقة الهدايا ومعلومات الولاء).</span><span class="sxs-lookup"><span data-stu-id="92053-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="92053-123">قبل أن تتمكن من تشغيل هذه الميزة، يجب تكوين موصل الدفع لـ SCA في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="92053-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="92053-124">لمزيد من المعلومات، راجع [مصادقة العميل القوية باستخدام Adyen‎](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="92053-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

> [!NOTE]
> <span data-ttu-id="92053-125">بالنسبة لموصل المدفوعات Adyen، يمكن عرض الوحدة النمطية iframe في الوحدة النمطية للدفع فقط إذا قمت بإضافة عنوان Adyen URL إلى قائمة السماح الخاصة بموقعك.</span><span class="sxs-lookup"><span data-stu-id="92053-125">For the Adyen payment connector, the iframe module in the payment module can be rendered only if you add the Adyen URL to your site's allow list.</span></span> <span data-ttu-id="92053-126">لإكمال هذه الخطوة ، قم بإضافة **\*.adyen.com** إلى توجيهات **child-src** و **connect-src** و **img-src** و **script-src** و **style-src** الخاصة بسياسة أمان محتوى الموقع.</span><span class="sxs-lookup"><span data-stu-id="92053-126">To complete this step, add **\*.adyen.com** to the **child-src** , **connect-src** , **img-src** , **script-src** , and **style-src** directives of your site's content security policy.</span></span> <span data-ttu-id="92053-127">لمزيد من المعلومات، راجع [إدارة سياسة أمان المحتوى](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="92053-127">For more information, see [Manage Content Security Policy](manage-csp.md).</span></span> 

<span data-ttu-id="92053-128">يعرض الشكل التوضيحي التالي مثالاً عن وحدات بطاقة الهدايا ونقاط الولاء والدفع في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="92053-128">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![مثال عن وحدات بطاقة الهدايا والولاء والدفع في صفحة السداد مع الخروج](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="92053-130">خصائص الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="92053-130">Payment module properties</span></span>

| <span data-ttu-id="92053-131">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="92053-131">Property name</span></span> | <span data-ttu-id="92053-132">القيم</span><span class="sxs-lookup"><span data-stu-id="92053-132">Values</span></span> | <span data-ttu-id="92053-133">الوصف</span><span class="sxs-lookup"><span data-stu-id="92053-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="92053-134">العنوان</span><span class="sxs-lookup"><span data-stu-id="92053-134">Heading</span></span> | <span data-ttu-id="92053-135">نص العنوان</span><span class="sxs-lookup"><span data-stu-id="92053-135">Heading text</span></span> | <span data-ttu-id="92053-136">عنوان اختياري للوحدة النمطية للدفع.</span><span class="sxs-lookup"><span data-stu-id="92053-136">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="92053-137">ارتفاع iframe</span><span class="sxs-lookup"><span data-stu-id="92053-137">Height of the iframe</span></span> | <span data-ttu-id="92053-138">بكسل</span><span class="sxs-lookup"><span data-stu-id="92053-138">Pixels</span></span> | <span data-ttu-id="92053-139">ارتفاع iframe بالبكسل.</span><span class="sxs-lookup"><span data-stu-id="92053-139">The iframe height, in pixels.</span></span> <span data-ttu-id="92053-140">يمكن ضبط الارتفاع كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="92053-140">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="92053-141">إظهار عنوان الفاتورة</span><span class="sxs-lookup"><span data-stu-id="92053-141">Show billing address</span></span> | <span data-ttu-id="92053-142">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="92053-142">**True** or **False**</span></span> | <span data-ttu-id="92053-143">إذا تم تعيين هذه الخاصية إلى **صواب** ، سيتم تقديم عنوان الفاتورة بواسطة Adyen داخل iframe للوحدة النمطية للدفع.</span><span class="sxs-lookup"><span data-stu-id="92053-143">If this property is set to **True** , the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="92053-144">إذا تم تعيينها إلى **خطأ** ، فلن يتم عرض عنوان الفوترة بواسطة Adyen، وسيتعين على مستخدم Commerce تكوين وحدة نمطية لعرض عنوان الفوترة على صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="92053-144">If it's set to **False** , the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="92053-145">تجاوز نمط الدفع</span><span class="sxs-lookup"><span data-stu-id="92053-145">Payment style override</span></span> | <span data-ttu-id="92053-146">كود أوراق الأنماط المتتالية (CSS)</span><span class="sxs-lookup"><span data-stu-id="92053-146">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="92053-147">بسبب استضافة الوحدة النمطية للدفع في iframe، هناك إمكانية محدودة لتطبيق الأنماط.</span><span class="sxs-lookup"><span data-stu-id="92053-147">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="92053-148">يمكنك تطبيق بعض الأنماط باستخدام هذه الخاصية.</span><span class="sxs-lookup"><span data-stu-id="92053-148">You can achieve some styling by using this property.</span></span> <span data-ttu-id="92053-149">لتجاوز أنماط الموقع، يجب عليك لصق كود CSS كقيمة لهذه الخاصية.</span><span class="sxs-lookup"><span data-stu-id="92053-149">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="92053-150">لا تنطبق تجاوزات وأنماط CSS منشئ الموقع على هذه الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="92053-150">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="92053-151">عنوان الفوترة</span><span class="sxs-lookup"><span data-stu-id="92053-151">Billing address</span></span>

<span data-ttu-id="92053-152">تسمح الوحدة النمطية للدفع للعملاء بتوفير عنوان فوترة لمعلومات الدفع الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="92053-152">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="92053-153">كما تتيح لهم إمكانية استخدام عنوان الشحن كعنوان فوترة، لتسهيل وتسريع عملية السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="92053-153">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="92053-154">إذا تم تعيين خاصية **إظهار عنوان الفوترة** إلى **خطـ** ، فيجب تكوين وحدة الدفع على صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="92053-154">If the **Show billing address** property is set to **False** , the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="92053-155">إضافة وحدة نمطية للدفع إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="92053-155">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="92053-156">يمكن إضافة وحده نمطية للدفع فقط إلى وحدة نمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="92053-156">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="92053-157">لمزيد من المعلومات حول كيفية تكوين وحدة نمطية للدفع لصفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="92053-157">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92053-158">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="92053-158">Additional resources</span></span>

[<span data-ttu-id="92053-159">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="92053-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="92053-160">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="92053-160">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="92053-161">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="92053-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="92053-162">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="92053-162">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="92053-163">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="92053-163">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="92053-164">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="92053-164">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="92053-165">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="92053-165">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="92053-166">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="92053-166">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="92053-167">مصادقة العملاء القوية باستخدام Adyen</span><span class="sxs-lookup"><span data-stu-id="92053-167">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
