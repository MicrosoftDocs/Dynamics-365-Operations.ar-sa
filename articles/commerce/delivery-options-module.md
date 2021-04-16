---
title: الوحدة النمطية لخيارات التسليم
description: يتناول هذا الموضوع الوحدات النمطية لخيارات التسليم ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/05/2020
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
ms.openlocfilehash: f97dcd42e22e319d9af7cbf57fce7c10d8565d04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801967"
---
# <a name="delivery-options-module"></a><span data-ttu-id="dad05-103">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="dad05-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dad05-104">يتناول هذا الموضوع الوحدات النمطية لخيارات التسليم ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dad05-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dad05-105">تتيح الوحدات النمطية لخيارات التسليم للعملاء تحديد وضع التسليم مثل الشحن أو الاستلام لطلباتهم عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="dad05-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="dad05-106">عنوان الشحن مطلوب لتحديد طريقة التسليم.</span><span class="sxs-lookup"><span data-stu-id="dad05-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="dad05-107">إذا تغيّر عنوان الشحن، فيجب البحث عن خيارات التسليم مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="dad05-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="dad05-108">إذا تضمن الأمر أصنافًا سيتم استلامها في المتجر فقط، فسيتم إخفاء هذه الوحدة النمطية بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="dad05-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="dad05-109">للحصول على معلومات حول كيفية تكوين أوضاع التسليم، راجع [إعداد القناة عبر الإنترنت](channel-setup-online.md) و[إعداد أوضاع التسليم](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="dad05-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="dad05-110">بإمكان كل وضع تسليم أن يكون لديهم تكلفة مرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="dad05-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="dad05-111">للحصول على معلومات حول كيفية تكوين التكاليف لمتجر عبر الإنترنت، راجع [التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="dad05-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="dad05-112">في الإصدار 10.0.13 من Commerce، تم تحديث خيارات التسليم لدعم الميزتين **تكاليف الرأس من دون توزيع** و **الشحن كتكلفة البنود**.</span><span class="sxs-lookup"><span data-stu-id="dad05-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="dad05-113">إذا تم إيقاف تشغيل التوزيع، فإن المتوقع هو أن سير عمل التجارة الإلكترونية لن يسمح بوضع تسليم مختلط للأصناف في سلة التسوق (أي تحديد بعض الأصناف للشحن وأصناف أخرى للاستلام).</span><span class="sxs-lookup"><span data-stu-id="dad05-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="dad05-114">تتطلب ميزة **تكاليف الرأس من دون توزيع** تشغيل العلامة **تمكين المعالجة المستمرة لوضع التسليم في القناة** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dad05-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="dad05-115">عند تشغيل هذه العلامة، سيتم تطبيق تكاليف الشحن على مستوى الرأس أو على مستوى البند، بحسب التكوين في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dad05-115">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="dad05-116">يدعم نسق Fabrikam وضع تسليم مختلطًا، حيث تم تحديد بعض الأصناف للشحن وأصناف أخرى للاستلام.‬</span><span class="sxs-lookup"><span data-stu-id="dad05-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="dad05-117">في هذا الوضع، سيتم توزيع تكاليف الشحن على كافة الأصناف المحددة لاستخدام الشحن كوضع تسليم.</span><span class="sxs-lookup"><span data-stu-id="dad05-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="dad05-118">لكي يعمل وضع التسليم المختلط، يجب عليك أولاً تكوين الميزة **تكاليف الرأس مع توزيع** في مركز Commerce الرئيسي</span><span class="sxs-lookup"><span data-stu-id="dad05-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="dad05-119">لمزيد من المعلومات حول هذا التكوين، راجع [توزيع تكاليف الرأس لمطابقة بنود المبيعات](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="dad05-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="dad05-120">إذا انطبقت تكاليف الشحن على الأصناف، فيمكن عرضها في بند سلة التسوق لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="dad05-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="dad05-121">تتطلب هذه الوظيفة تشغيل الخاصية **إظهار تكاليف الشحن على البند‬** للوحدة النمطية لسلة التسوق والوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="dad05-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="dad05-122">لمزيد من المعلومات، راجع [الوحدة النمطية لسلة التسوق](add-cart-module.md) و[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md) .</span><span class="sxs-lookup"><span data-stu-id="dad05-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="dad05-123">يبين الشكل التوضيحي التالي مثالاُ عن وحدة خيارات التسليم في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="dad05-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![مثال عن الوحدة النمطية لخيارات التسليم على صفحة السداد مع الخروج](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="dad05-125">خصائص الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="dad05-125">Delivery options module properties</span></span>

| <span data-ttu-id="dad05-126">الخاصية</span><span class="sxs-lookup"><span data-stu-id="dad05-126">Property</span></span> | <span data-ttu-id="dad05-127">القيم</span><span class="sxs-lookup"><span data-stu-id="dad05-127">Values</span></span> | <span data-ttu-id="dad05-128">الوصف</span><span class="sxs-lookup"><span data-stu-id="dad05-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="dad05-129">العنوان</span><span class="sxs-lookup"><span data-stu-id="dad05-129">Heading</span></span> | <span data-ttu-id="dad05-130">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="dad05-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="dad05-131">عنوان اختياري للوحدة النمطية لخيارات التسليم.</span><span class="sxs-lookup"><span data-stu-id="dad05-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="dad05-132">اسم فئة CSS مخصصة</span><span class="sxs-lookup"><span data-stu-id="dad05-132">Custom CSS class name</span></span> | <span data-ttu-id="dad05-133">النص</span><span class="sxs-lookup"><span data-stu-id="dad05-133">Text</span></span> | <span data-ttu-id="dad05-134">اسم فئة أوراق الأنماط المتتالية (CSS) المخصصة التي سيتم استخدامها لتقديم هذه الوحدة النمطية، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="dad05-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="dad05-135">خيار تصفية طريقة التسليم</span><span class="sxs-lookup"><span data-stu-id="dad05-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="dad05-136">**عدم التصفية** أو **أوضاع غير خاصة بالشحن**</span><span class="sxs-lookup"><span data-stu-id="dad05-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="dad05-137">قيمة تحدد ما إذا كان يجب على الوحدة النمطية لخيارات التسليم تصفية كافة أوضاع التسليم غير الخاصة بالشحن.</span><span class="sxs-lookup"><span data-stu-id="dad05-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="dad05-138">إضافة الوحدة النمطية لخيارات التسليم إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="dad05-138">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="dad05-139">يمكن إضافة وحدة نمطية لخيارات التسليم فقط إلى وحدة نمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="dad05-139">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="dad05-140">لمزيد من المعلومات حول كيفية تكوين الوحدة النمطية لخيارات التسليم وإضافتها إلى صفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="dad05-140">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dad05-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dad05-141">Additional resources</span></span>

[<span data-ttu-id="dad05-142">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="dad05-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="dad05-143">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="dad05-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="dad05-144">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="dad05-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="dad05-145">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="dad05-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="dad05-146">الوحدة النمطية لمعلومات الاستلام</span><span class="sxs-lookup"><span data-stu-id="dad05-146">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="dad05-147">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="dad05-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="dad05-148">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="dad05-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="dad05-149">إعداد قناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="dad05-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="dad05-150">التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="dad05-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="dad05-151">توزيع تكاليف الرأس لمطابقة بنود المبيعات</span><span class="sxs-lookup"><span data-stu-id="dad05-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="dad05-152">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="dad05-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]