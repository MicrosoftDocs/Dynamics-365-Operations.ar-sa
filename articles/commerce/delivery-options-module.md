---
title: الوحدة النمطية لخيارات التسليم
description: يتناول هذا الموضوع الوحدات النمطية لخيارات التسليم ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e55ce327e2c8ab714eb5e2fa14b3830b9171688
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020669"
---
# <a name="delivery-options-module"></a><span data-ttu-id="1263a-103">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="1263a-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1263a-104">يتناول هذا الموضوع الوحدات النمطية لخيارات التسليم ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1263a-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1263a-105">تتيح الوحدات النمطية لخيارات التسليم للعملاء تحديد وضع التسليم مثل الشحن أو الاستلام لطلباتهم عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="1263a-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="1263a-106">عنوان الشحن مطلوب لتحديد طريقة التسليم.</span><span class="sxs-lookup"><span data-stu-id="1263a-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="1263a-107">إذا تغيّر عنوان الشحن، فيجب البحث عن خيارات التسليم مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="1263a-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="1263a-108">إذا تضمن الأمر أصنافًا سيتم استلامها في المتجر فقط، فسيتم إخفاء هذه الوحدة النمطية بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="1263a-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="1263a-109">للحصول على معلومات حول كيفية تكوين أوضاع التسليم، راجع [إعداد القناة عبر الإنترنت](channel-setup-online.md) و[إعداد أوضاع التسليم](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="1263a-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="1263a-110">بإمكان كل وضع تسليم أن يكون لديهم تكلفة مرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="1263a-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="1263a-111">للحصول على معلومات حول كيفية تكوين التكاليف لمتجر عبر الإنترنت، راجع [التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="1263a-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="1263a-112">في الإصدار 10.0.13 من Commerce، تم تحديث خيارات التسليم لدعم الميزتين **تكاليف الرأس من دون توزيع** و **الشحن كتكلفة البنود**.</span><span class="sxs-lookup"><span data-stu-id="1263a-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="1263a-113">إذا تم إيقاف تشغيل التوزيع، فإن المتوقع هو أن سير عمل التجارة الإلكترونية لن يسمح بوضع تسليم مختلط للأصناف في سلة التسوق (أي تحديد بعض الأصناف للشحن وأصناف أخرى للاستلام).</span><span class="sxs-lookup"><span data-stu-id="1263a-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="1263a-114">تتطلب ميزة **تكاليف الرأس من دون توزيع** تشغيل العلامة **تمكين المعالجة المستمرة لوضع التسليم في القناة** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1263a-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="1263a-115">عند تشغيل علامة الميزة هذه، سيتم تطبيق تكاليف الشحن على مستوى الرأس أو على مستوى البند، بحسب التكوين في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1263a-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="1263a-116">يدعم نسق Fabrikam وضع تسليم مختلطًا، حيث تم تحديد بعض الأصناف للشحن وأصناف أخرى للاستلام.‬</span><span class="sxs-lookup"><span data-stu-id="1263a-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="1263a-117">في هذا الوضع، سيتم توزيع تكاليف الشحن على كافة الأصناف المحددة لاستخدام الشحن كوضع تسليم.</span><span class="sxs-lookup"><span data-stu-id="1263a-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="1263a-118">لكي يعمل وضع التسليم المختلط، يجب عليك أولاً تكوين الميزة **تكاليف الرأس مع توزيع** في مركز Commerce الرئيسي</span><span class="sxs-lookup"><span data-stu-id="1263a-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="1263a-119">لمزيد من المعلومات حول هذا التكوين، راجع [توزيع تكاليف الرأس لمطابقة بنود المبيعات](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="1263a-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="1263a-120">إذا انطبقت تكاليف الشحن على الأصناف، فيمكن عرضها في بند سلة التسوق لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="1263a-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="1263a-121">تتطلب هذه الوظيفة تشغيل الخاصية **إظهار تكاليف الشحن على البند‬** للوحدة النمطية لسلة التسوق والوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="1263a-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="1263a-122">لمزيد من المعلومات، راجع [الوحدة النمطية لسلة التسوق](add-cart-module.md) و[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md) .</span><span class="sxs-lookup"><span data-stu-id="1263a-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="1263a-123">يبين الشكل التوضيحي التالي مثالاُ عن وحدة خيارات التسليم في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="1263a-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![مثال عن الوحدة النمطية لخيارات التسليم على صفحة السداد مع الخروج](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="1263a-125">خصائص الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="1263a-125">Delivery options module properties</span></span>

| <span data-ttu-id="1263a-126">الخاصية</span><span class="sxs-lookup"><span data-stu-id="1263a-126">Property</span></span> | <span data-ttu-id="1263a-127">القيم</span><span class="sxs-lookup"><span data-stu-id="1263a-127">Values</span></span> | <span data-ttu-id="1263a-128">الوصف</span><span class="sxs-lookup"><span data-stu-id="1263a-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="1263a-129">العنوان</span><span class="sxs-lookup"><span data-stu-id="1263a-129">Heading</span></span> | <span data-ttu-id="1263a-130">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="1263a-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1263a-131">عنوان اختياري للوحدة النمطية لخيارات التسليم.</span><span class="sxs-lookup"><span data-stu-id="1263a-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="1263a-132">اسم فئة CSS مخصصة</span><span class="sxs-lookup"><span data-stu-id="1263a-132">Custom CSS class name</span></span> | <span data-ttu-id="1263a-133">النص</span><span class="sxs-lookup"><span data-stu-id="1263a-133">Text</span></span> | <span data-ttu-id="1263a-134">اسم فئة أوراق الأنماط المتتالية (CSS) المخصصة التي سيتم استخدامها لتقديم هذه الوحدة النمطية، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="1263a-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="1263a-135">خيار تصفية طريقة التسليم</span><span class="sxs-lookup"><span data-stu-id="1263a-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="1263a-136">**عدم التصفية** أو **أوضاع غير خاصة بالشحن**</span><span class="sxs-lookup"><span data-stu-id="1263a-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="1263a-137">قيمة تحدد ما إذا كان يجب على الوحدة النمطية لخيارات التسليم تصفية كافة أوضاع التسليم غير الخاصة بالشحن.</span><span class="sxs-lookup"><span data-stu-id="1263a-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="1263a-138">تحديد خيار التسليم تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="1263a-138">Auto select a delivery option</span></span> | <span data-ttu-id="1263a-139">**عدم التصفية** أو **تحديد خيار التسليم التلقائي وإظهار الملخص** أو **تحديد خيار التسليم التلقائي وعدم إظهار الملخص**</span><span class="sxs-lookup"><span data-stu-id="1263a-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="1263a-140">تطبق هذه الخاصية تلقائيًا خيار التسليم الأول المتاح للخروج دون مطالبة المستخدم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="1263a-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="1263a-141">يجب استخدامه فقط إذا كان هناك خيار تسليم واحد متاح.</span><span class="sxs-lookup"><span data-stu-id="1263a-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="1263a-142">يتم دعم هذه الخاصية اعتبارًا من إصدار Commerce رقم 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="1263a-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="1263a-143">إضافة الوحدة النمطية لخيارات التسليم إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="1263a-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="1263a-144">يمكن إضافة وحدة نمطية لخيارات التسليم فقط إلى وحدة نمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="1263a-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="1263a-145">لمزيد من المعلومات حول كيفية تكوين الوحدة النمطية لخيارات التسليم وإضافتها إلى صفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1263a-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1263a-146">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1263a-146">Additional resources</span></span>

[<span data-ttu-id="1263a-147">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="1263a-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1263a-148">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="1263a-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1263a-149">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="1263a-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1263a-150">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="1263a-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="1263a-151">الوحدة النمطية لمعلومات الاستلام</span><span class="sxs-lookup"><span data-stu-id="1263a-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="1263a-152">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="1263a-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1263a-153">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="1263a-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="1263a-154">إعداد قناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="1263a-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="1263a-155">التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="1263a-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="1263a-156">توزيع تكاليف الرأس لمطابقة بنود المبيعات</span><span class="sxs-lookup"><span data-stu-id="1263a-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="1263a-157">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="1263a-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
