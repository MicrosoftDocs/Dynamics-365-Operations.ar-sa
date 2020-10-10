---
title: الوحدة النمطية لخيارات التسليم
description: يتناول هذا الموضوع الوحدات النمطية لخيارات التصليم ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.openlocfilehash: 39e597b88afcca69623b1a23acc95e4da3873082
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818289"
---
# <a name="delivery-options-module"></a><span data-ttu-id="a284a-103">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="a284a-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a284a-104">يتناول هذا الموضوع الوحدات النمطية لخيارات التصليم ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a284a-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a284a-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a284a-105">Overview</span></span>

<span data-ttu-id="a284a-106">تتيح الوحدات النمطية لخيارات التسليم للعملاء تحديد وضع التسليم مثل الشحن أو الاستلام لطلباتهم عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="a284a-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="a284a-107">عنوان الشحن مطلوب لتحديد طريقة التسليم.</span><span class="sxs-lookup"><span data-stu-id="a284a-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="a284a-108">إذا تغيّر عنوان الشحن، فيجب البحث عن خيارات التسليم مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="a284a-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="a284a-109">إذا تضمن الأمر أصنافًا سيتم استلامها في المتجر فقط، فسيتم إخفاء هذه الوحدة النمطية بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="a284a-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="a284a-110">للحصول على معلومات حول كيفية تكوين أوضاع التسليم، راجع [إعداد القناة عبر الإنترنت](channel-setup-online.md) و[إعداد أوضاع التسليم](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="a284a-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="a284a-111">بإمكان كل وضع تسليم أن يكون لديهم تكلفة مرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="a284a-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="a284a-112">للحصول على معلومات حول كيفية تكوين التكاليف لمتجر عبر الإنترنت، راجع [التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="a284a-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="a284a-113">في الإصدار 10.0.13 من Commerce، تم تحديث خيارات التسليم لدعم الميزتين **تكاليف الرأس من دون توزيع** و **الشحن كتكلفة البنود**.</span><span class="sxs-lookup"><span data-stu-id="a284a-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="a284a-114">إذا تم إيقاف تشغيل التوزيع، فإن المتوقع هو أن سير عمل التجارة الإلكترونية لن يسمح بوضع تسليم مختلط للأصناف في سلة التسوق (أي تحديد بعض الأصناف للشحن وأصناف أخرى للاستلام).</span><span class="sxs-lookup"><span data-stu-id="a284a-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="a284a-115">تتطلب ميزة **تكاليف الرأس من دون توزيع** تشغيل العلامة **تمكين المعالجة المستمرة لوضع التسليم في القناة** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a284a-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="a284a-116">عند تشغيل هذه العلامة، سيتم تطبيق تكاليف الشحن على مستوى الرأس أو على مستوى البند، بحسب التكوين في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a284a-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="a284a-117">يدعم نسق Fabrikam وضع تسليم مختلطًا، حيث تم تحديد بعض الأصناف للشحن وأصناف أخرى للاستلام.‬</span><span class="sxs-lookup"><span data-stu-id="a284a-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="a284a-118">في هذا الوضع، سيتم توزيع تكاليف الشحن على كافة الأصناف المحددة لاستخدام الشحن كوضع تسليم.</span><span class="sxs-lookup"><span data-stu-id="a284a-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="a284a-119">لكي يعمل وضع التسليم المختلط، يجب عليك أولاً تكوين الميزة **تكاليف الرأس مع توزيع** في مركز Commerce الرئيسي</span><span class="sxs-lookup"><span data-stu-id="a284a-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="a284a-120">لمزيد من المعلومات حول هذا التكوين، راجع [توزيع تكاليف الرأس لمطابقة بنود المبيعات](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="a284a-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="a284a-121">إذا انطبقت تكاليف الشحن على الأصناف، فيمكن عرضها في بند سلة التسوق لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="a284a-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="a284a-122">تتطلب هذه الوظيفة تشغيل الخاصية **إظهار تكاليف الشحن على البند‬** للوحدة النمطية لسلة التسوق والوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="a284a-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="a284a-123">لمزيد من المعلومات، راجع [الوحدة النمطية لسلة التسوق](add-cart-module.md) و[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md) .</span><span class="sxs-lookup"><span data-stu-id="a284a-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="a284a-124">يبين الشكل التوضيحي التالي مثالاُ عن وحدة خيارات التسليم في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="a284a-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![مثال عن الوحدة النمطية لخيارات التسليم على صفحة السداد مع الخروج](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="a284a-126">خصائص الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="a284a-126">Delivery options module properties</span></span>

| <span data-ttu-id="a284a-127">الخاصية</span><span class="sxs-lookup"><span data-stu-id="a284a-127">Property</span></span> | <span data-ttu-id="a284a-128">القيم</span><span class="sxs-lookup"><span data-stu-id="a284a-128">Values</span></span> | <span data-ttu-id="a284a-129">الوصف</span><span class="sxs-lookup"><span data-stu-id="a284a-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="a284a-130">العنوان</span><span class="sxs-lookup"><span data-stu-id="a284a-130">Heading</span></span> | <span data-ttu-id="a284a-131">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="a284a-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a284a-132">عنوان اختياري للوحدة النمطية لخيارات التسليم.</span><span class="sxs-lookup"><span data-stu-id="a284a-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="a284a-133">اسم فئة CSS مخصصة</span><span class="sxs-lookup"><span data-stu-id="a284a-133">Custom CSS class name</span></span> | <span data-ttu-id="a284a-134">النص</span><span class="sxs-lookup"><span data-stu-id="a284a-134">Text</span></span> | <span data-ttu-id="a284a-135">اسم فئة أوراق الأنماط المتتالية (CSS) المخصصة التي سيتم استخدامها لتقديم هذه الوحدة النمطية، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="a284a-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="a284a-136">خيار تصفية طريقة التسليم</span><span class="sxs-lookup"><span data-stu-id="a284a-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="a284a-137">**عدم التصفية** أو **أوضاع غير خاصة بالشحن**</span><span class="sxs-lookup"><span data-stu-id="a284a-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="a284a-138">قيمة تحدد ما إذا كان يجب على الوحدة النمطية لخيارات التسليم تصفية كافة أوضاع التسليم غير الخاصة بالشحن.</span><span class="sxs-lookup"><span data-stu-id="a284a-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="a284a-139">إضافة الوحدة النمطية لخيارات التسليم إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="a284a-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="a284a-140">يمكن إضافة وحدة نمطية لخيارات التسليم فقط إلى وحدة نمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="a284a-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="a284a-141">لمزيد من المعلومات حول كيفية تكوين الوحدة النمطية لخيارات التسليم وإضافتها إلى صفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="a284a-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a284a-142">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a284a-142">Additional resources</span></span>

[<span data-ttu-id="a284a-143">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="a284a-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a284a-144">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="a284a-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a284a-145">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="a284a-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a284a-146">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="a284a-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a284a-147">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="a284a-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a284a-148">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="a284a-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="a284a-149">إعداد قناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="a284a-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="a284a-150">التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="a284a-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="a284a-151">توزيع تكاليف الرأس لمطابقة بنود المبيعات</span><span class="sxs-lookup"><span data-stu-id="a284a-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="a284a-152">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="a284a-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
