---
title: بطاقات الهدايا الرقمية في التجارة الإلكترونية
description: يصف هذا الموضوع كيفية عمل بطاقات الهدايا الرقمية في تنفيذ التجارة الإلكترونية لـ Microsoft Dynamics 365 Commerce. كما يوفر نظرة عامة على الخطوات الهامة للتكوين.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: bd93744cf947dcc343d2b31d3d52b2b748c062a9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792861"
---
# <a name="e-commerce-digital-gift-cards"></a><span data-ttu-id="c0461-104">بطاقات الهدايا الرقمية في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c0461-104">E-commerce digital gift cards</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c0461-105">يصف هذا الموضوع كيفية عمل بطاقات الهدايا الرقمية في تنفيذ التجارة الإلكترونية لـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c0461-105">This topic describes how digital gift cards work in the e-commerce implementation of Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="c0461-106">كما يوفر نظرة عامة على الخطوات الهامة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="c0461-106">It also provides an overview of important configuration steps.</span></span>

<span data-ttu-id="c0461-107">في Dynamics 365 Commerce، يتبع شراء بطاقات الهدايا الرقمية نفس سير العمل مثل شراء المنتجات الأخرى في النظام.</span><span class="sxs-lookup"><span data-stu-id="c0461-107">In Dynamics 365 Commerce, the purchase of digital gift cards follows the same flow as the purchase of other products in the system.</span></span> <span data-ttu-id="c0461-108">لا يلزم تكوين أي وحدات نمطية إضافية.</span><span class="sxs-lookup"><span data-stu-id="c0461-108">No additional modules have to be configured.</span></span> <span data-ttu-id="c0461-109">في حالة إضافة العديد من بطاقات الهدايا إلى سلة التسوق، لا يتم تجميع أصناف بطاقة الهدايا في بند مبيعات واحد.</span><span class="sxs-lookup"><span data-stu-id="c0461-109">If multiple gift cards are added to the cart, the gift card items aren't aggregated on a single sales line.</span></span> <span data-ttu-id="c0461-110">وهذا السلوك مطلوب نظرا لأنه تتم فوترة كل بند مبيعات عن طريق استخدام رقم بطاقة هدايا منفصل.</span><span class="sxs-lookup"><span data-stu-id="c0461-110">This behavior is required because each sales line is invoiced by using a separate gift card number.</span></span>

<span data-ttu-id="c0461-111">يتم دعم شراء بطاقات الهدايا الرقمية في Dynamics 365 Commerce الإصدار 10.0.16 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="c0461-111">The purchase of digital gift cards is supported in the Dynamics 365 Commerce 10.0.16 release and later.</span></span>

<span data-ttu-id="c0461-112">يبين الرسم التوضيحي التالي مثالا لصفحة تفاصيل المنتج (PDP) لبطاقة الهدايا الرقمية على موقع التجارة الإلكترونية Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c0461-112">The following illustration shows an example of the product details page (PDP) for a digital gift card on the Fabrikam e-commerce site.</span></span>

![مثال على بطاقة الهدايا الرقمية PDP على موقع التجارة الإلكترونية في شركة Fabrikam](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a><span data-ttu-id="c0461-114">تشغيل ميزة بطاقة الهدايا الرقمية في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="c0461-114">Turn on the digital gift card feature in Commerce headquarters</span></span>

<span data-ttu-id="c0461-115">لكي يعمل سير عمل المشتريات لبطاقات الهدايا الرقمية للعمل في Dynamics 365 Commerce، يجب تشغيل ميزة **بطاقة هدايا الشراء في ميزة التجارة الإلكترونية** في المقر الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="c0461-115">For the purchase flow for digital gift cards to work in Dynamics 365 Commerce, the **Purchasing gift card on e-Commerce feature** feature must be turned on in Commerce headquarters.</span></span> <span data-ttu-id="c0461-116">يمكنك العثور على الميزة في مساحة عمل **إدارة الميزات** في المركز الرئيسي لـ Commerce، كما هو موضح في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="c0461-116">You can find the feature in the **Feature management** workspace in Commerce headquarters, as shown in the following illustration.</span></span>

![مساحة عمل إدارة الميزات في المركز الرئيسي لـ Commerce](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a><span data-ttu-id="c0461-118">تكوين بطاقة الهدايا الرقمية في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="c0461-118">Configure a digital gift card in Commerce headquarters</span></span>

<span data-ttu-id="c0461-119">يجب تكوين منتجات بطاقة الهدايا الرقمية في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="c0461-119">Digital gift card products should be configured in Commerce headquarters.</span></span> <span data-ttu-id="c0461-120">وهذه العملية تشبه العملية الخاصة بالمنتجات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0461-120">The process resembles the process for other products.</span></span> <span data-ttu-id="c0461-121">ومع ذلك، تكون الخطوات الهامة التالية خاصة بتكوين بطاقات الهدايا للشراء.</span><span class="sxs-lookup"><span data-stu-id="c0461-121">However, the following important steps are specific to the configuration of gift cards for purchase.</span></span> <span data-ttu-id="c0461-122">لمزيد من المعلومات حول كيفية إنشاء وتكوين المنتجات، راجع [إنشاء منتج جديد في Commerce](create-new-product-commerce.md).</span><span class="sxs-lookup"><span data-stu-id="c0461-122">For more information about how to create and configure products, see [Create a new product in Commerce](create-new-product-commerce.md).</span></span>

- <span data-ttu-id="c0461-123">عند تكوين منتجات بطاقة هدايا رقمية في مربع الحوار **منتج جديد**، قم بتعيين حقل **نوع المنتج** إلى **خدمة**.</span><span class="sxs-lookup"><span data-stu-id="c0461-123">When you configure digital gift card products in the **New product** dialog box, set the **Product type** field to **Service**.</span></span> <span data-ttu-id="c0461-124">(لفتح مربع الحوار، انتقل إلى **البيع بالتجزئة والتجارة \> المنتجات والفئات \> المنتجات حسب الفئة**، وحدد **جديد**.) لا يتم اختيار المنتجات من نوع **خدمة** للمخزون المتوفر قبل تقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c0461-124">(To open the dialog box, go to **Retail and commerce \> Products and categories \> Products by category**, and select **New**.) Products of the **Service** type aren't checked for available inventory before an order is placed.</span></span> <span data-ttu-id="c0461-125">لمزيد من المعلومات، راجع [إنشاء منتج جديد](create-new-product-commerce.md#create-a-new-product).</span><span class="sxs-lookup"><span data-stu-id="c0461-125">For more information, see [Create a new product](create-new-product-commerce.md#create-a-new-product).</span></span>
- <span data-ttu-id="c0461-126">في صفحة **معلمات التجارة** في علامة تبويب **الترحيل**، يجب تعيين حقل **منتج بطاقة الهدايا** إلى **بطاقة الهدايا الرقمية**، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="c0461-126">On the **Commerce parameters** page, on the **Posting** tab, the **Gift card product** field must be set to **Digital Gift Card**, as shown in the following illustration.</span></span> <span data-ttu-id="c0461-127">إذا كان المنتج عبارة عن بطاقة هدايا خارجية، فراجع [دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md) للحصول على مزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="c0461-127">If the product is an external gift card, see [Support for external gift cards](./dev-itpro/gift-card.md) for more information.</span></span>

    ![حقل منتج بطاقة الهدايا في المركز الرئيسي لـ Commerce](./media/PostGiftcard.png)

- <span data-ttu-id="c0461-129">إذا كان يجب أن تدعم بطاقة الهدايا مبالغ متعددة معرفة مسبقًا (على سبيل المثال ، 25 دولار و50 دولار و100 دولار)، فيجب استخدام بُعد **الحجم** لإعداد تلك المبالغ المعرفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="c0461-129">If a gift card must support multiple predefined amounts (for example, $25, $50, and $100), the **Size** dimension should be used to set up those predefined amounts.</span></span> <span data-ttu-id="c0461-130">سيكون كل مبلغ معرف مسبقًا متغيرًا.</span><span class="sxs-lookup"><span data-stu-id="c0461-130">Each predefined amount will be a variant.</span></span> <span data-ttu-id="c0461-131">لمزيد من المعلومات، راجع [أبعاد المنتجات](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c0461-131">For more information, see [Product dimensions](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).</span></span>
- <span data-ttu-id="c0461-132">إذا كان يجب أن يكون العملاء قادرين على تحديد مبلغ مخصص لبطاقة الهدايا، فقم أولا بإعداد متغير يسمح بمبلغ مخصص.</span><span class="sxs-lookup"><span data-stu-id="c0461-132">If customers must be able to specify a custom amount for a gift card, first set up a variant that allows for a custom amount.</span></span> <span data-ttu-id="c0461-133">بعد ذلك، افتح المنتج من صفحة **المنتجات التي تم إصدارها**، ثم في علامة التبويب السريعة **التجارة**، قم بتعيين حقل **إدخال السعر** إلى **يجب إدخال سعر جديد**، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="c0461-133">Next, open the product from the **Released products in category** page, and then, on the **Commerce** FastTab, set the **Key in price** field to **Must key in new price**, as shown in the following illustration.</span></span> <span data-ttu-id="c0461-134">ويعمل هذا الإعداد على ضمان قيام العملاء بإدخال سعر عند استعراض المنتج على PDP.</span><span class="sxs-lookup"><span data-stu-id="c0461-134">This setting ensures that customers can enter a price when they browse the product on a PDP.</span></span>

    ![حقل إدخال السعر في المركز الرئيسي لـ Commerce](./media/KeyInPrice.png)

- <span data-ttu-id="c0461-136">يجب تعيين وضع التسليم لبطاقة الهدايا الرقمية إلى **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="c0461-136">The mode of delivery for a digital gift card must be set to **Electronic**.</span></span> <span data-ttu-id="c0461-137">في صفحة **أوضاع التسليم** (**البيع بالتجزئة والتجارة \> إعداد القناة \> أوضاع التسليم**)، حدد وضع التسليم **إلكتروني** في جزء القائمة، ثم قم بإضافة منتج بطاقة الهدايا الرقمية إلى الشبكة الموجودة في علامة التبويب السريعة **المنتجات**، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="c0461-137">On the **Modes of delivery** page (**Retail and commerce \> Channel setup \> Modes of delivery**), select the **Electronic** mode of delivery in the list pane, and then add the digital gift card product to the grid on the **Products** FastTab, as shown in the following illustration.</span></span> <span data-ttu-id="c0461-138">لمزيد من المعلومات، راجع [إعداد أوضاع التسليم](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="c0461-138">For more information, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

    ![منتجات بطاقة الهدايا الرقمية في الصفحة وضع التسليم في المركز الرئيسي لـ Commerce](./media/ElectronicMode.PNG)

- <span data-ttu-id="c0461-140">تأكد من أنه تم إنشاء ملف تعريف وظائف عبر الإنترنت واقترانه بمتجرك على الإنترنت في المقر الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="c0461-140">Make sure that an online functionality profile has been created and associated with your online store in Commerce headquarters.</span></span> <span data-ttu-id="c0461-141">في ملف تعريف الوظائف، قم بتعيين خيار **تجميع المنتجات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c0461-141">In the functionality profile, set the **Aggregate products** option to **Yes**.</span></span> <span data-ttu-id="c0461-142">يضمن هذا الإعداد تجميع كافة الأصناف باستثناء بطاقات الهدايا.</span><span class="sxs-lookup"><span data-stu-id="c0461-142">This setting ensures that all items except gift cards are aggregated.</span></span> <span data-ttu-id="c0461-143">لمزيد من المعلومات، راجع [إنشاء ملف تعريف وظائف عبر الإنترنت](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="c0461-143">For more information, see [Create an online functionality profile](online-functionality-profile.md).</span></span>
- <span data-ttu-id="c0461-144">للتأكد من تلقي العملاء لرسالة بريد إلكتروني بعد فوتره بطاقة الهدايا، قم بإنشاء نوع إخطار بريد إلكتروني جديد في صفحة **ملفات تعريف إخطارات البريد الإلكتروني**، وقم بتعيين حقل **نوع إخطار البريد الإلكتروني** إلى **إصدار بطاقة هدايا**.</span><span class="sxs-lookup"><span data-stu-id="c0461-144">To ensure that customers receive an email after a gift card is invoiced, create a new email notification type on the **Email notification profiles** page, and set the **Email notification type** field to **Issue gift card**.</span></span> <span data-ttu-id="c0461-145">لمزيد من المعلومات، راجع [إعداد تعريف إخطار البريد الإلكتروني](email-notification-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c0461-145">For more information, see [Set up an email notification profile](email-notification-profiles.md).</span></span>

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a><span data-ttu-id="c0461-146">إضافة صور المنتجات إلى مكتبة وسائط منشئ مواقع التجارة</span><span class="sxs-lookup"><span data-stu-id="c0461-146">Add product images to the Commerce site builder Media library</span></span>

<span data-ttu-id="c0461-147">يجب إضافة صور المنتج الخاصة بمنتجات بطاقة الهدايا الرقمية إلى مكتبة وسائط منشئ مواقع التجارة.</span><span class="sxs-lookup"><span data-stu-id="c0461-147">You must add product images for digital gift card products to the Commerce site builder Media library.</span></span> <span data-ttu-id="c0461-148">تأكد من أن أسماء الملفات الخاصة بملفات صور بطاقة الهدايا تتبع اصطلاحات التسمية الخاصة بموقعك لصور المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c0461-148">Make sure that the file names of the gift card image files follow your site's naming conventions for product images.</span></span> <span data-ttu-id="c0461-149">لمزيد من المعلومات، راجع [تحميل الصور](dam-upload-images.md).</span><span class="sxs-lookup"><span data-stu-id="c0461-149">For more information, see [Upload images](dam-upload-images.md).</span></span>

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a><span data-ttu-id="c0461-150">تكوين مبلغ مخصص لبطاقة هدايا رقمية في منشئ مواقع التجارة</span><span class="sxs-lookup"><span data-stu-id="c0461-150">Configure a custom amount for a digital gift card in Commerce site builder</span></span>

<span data-ttu-id="c0461-151">في حالة تكوين بطاقة هدايا رقمية للسماح بالمبلغ المخصص، يجب تمكين هذا السلوك أيضا في [الوحدة النمطية لصندوق الشراء](add-buy-box.md) المستخدمة في صفحات تفاصيل المنتج (PDP) بموقعك.</span><span class="sxs-lookup"><span data-stu-id="c0461-151">If a digital gift card is configured to allow for a custom amount, this behavior must also be enabled in the [buy box module](add-buy-box.md) that is used on your site's PDPs.</span></span> <span data-ttu-id="c0461-152">تدعم وحدة صندوق الشراء تكوين الوحدة النمطية للسماح بالمبالغ المخصصة.</span><span class="sxs-lookup"><span data-stu-id="c0461-152">The buy box module supports module configuration to allow for custom amounts.</span></span> <span data-ttu-id="c0461-153">يمكنك أيضًا تحديد الحد الأدنى والحد الأقصى للمبالغ المسموح بها للمبالغ المخصصة.</span><span class="sxs-lookup"><span data-stu-id="c0461-153">You can also define the minimum and maximum amounts that are allowed for custom amounts.</span></span>

<span data-ttu-id="c0461-154">لتكوين مبلغ مخصص لبطاقة هدايا رقمية في منشئ مواقع التجارة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c0461-154">To configure a custom amount for a digital gift card in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0461-155">انتقل إلى الوحدة النمطية لمربع الشراء المستخدمة في صفحات تفاصيل المنتج (PDP) بموقعك.</span><span class="sxs-lookup"><span data-stu-id="c0461-155">Go to the buy box module that is used on your site's PDPs.</span></span> <span data-ttu-id="c0461-156">قد يتم تنفيذ الوحدة النمطية لمربع الشراء في شريحة، أو في قالب، أو في صفحة.</span><span class="sxs-lookup"><span data-stu-id="c0461-156">This buy box module might be implemented in a fragment, in a template, or on a page.</span></span>
1. <span data-ttu-id="c0461-157">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c0461-157">Select **Edit**.</span></span>
1. <span data-ttu-id="c0461-158">في جزء الخصائص الموجود على اليسار ، حدد خانة الاختيار **السماح بالسعر المخصص**.</span><span class="sxs-lookup"><span data-stu-id="c0461-158">In the properties pane on the right, select the **Allow custom price** check box.</span></span>
1. <span data-ttu-id="c0461-159">اختياري: لتحديد الحد الأدنى والحد الأقصى للمبالغ المخصصة، ادخل المبالغ تحت **الحد الأدنى للسعر** و **الحد الأقصى للسعر**.</span><span class="sxs-lookup"><span data-stu-id="c0461-159">Optional: To define minimum and maximum amounts for custom amounts, enter amounts under **Minimum price** and **Maximum price**.</span></span>
1. <span data-ttu-id="c0461-160">حدد **إنهاء التحرير**، ثم قم بتحديد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c0461-160">Select **Finish editing**, and then select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0461-161">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c0461-161">Additional resources</span></span>

[<span data-ttu-id="c0461-162">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="c0461-162">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c0461-163">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="c0461-163">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c0461-164">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="c0461-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c0461-165">إنشاء منتج جديد في Commerce</span><span class="sxs-lookup"><span data-stu-id="c0461-165">Create a new product in Commerce</span></span>](create-new-product-commerce.md)

[<span data-ttu-id="c0461-166">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="c0461-166">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="c0461-167">أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="c0461-167">Product dimensions</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[<span data-ttu-id="c0461-168">إنشاء ملف تعريف الإخطار بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="c0461-168">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="c0461-169">إنشاء ملف تعريف وظائف على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="c0461-169">Create an online functionality profile</span></span>](online-functionality-profile.md)

[<span data-ttu-id="c0461-170">دعم بطاقات الهدايا الخارجية</span><span class="sxs-lookup"><span data-stu-id="c0461-170">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]