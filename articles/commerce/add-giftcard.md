---
title: وحدة بطاقة الهدايا
description: يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661232"
---
# <a name="gift-card-module"></a><span data-ttu-id="806bc-103">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="806bc-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="806bc-104">يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="806bc-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="806bc-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="806bc-105">Overview</span></span>

<span data-ttu-id="806bc-106">تعتبر بطاقات الهدايا طريقة دفع شائعة، ويمكن استخدام وحدة بطاقة الهدايا في وحدة السداد مع الخروج لقبول بطاقات الهدايا.</span><span class="sxs-lookup"><span data-stu-id="806bc-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="806bc-107">تدعم وحدة بطاقة الهدايا بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="806bc-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="806bc-108">يتم استرداد بطاقات الهدايا من SVS وGivex من خلال موفر الدفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="806bc-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="806bc-109">لمزيد من المعلومات عن دعم بطاقات الهدايا الخارجية مثل SVS وGivex، راجع [و دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="806bc-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="806bc-110">تعرض الصورة التالية مثالاً عن وحدة بطاقة هدايا في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="806bc-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![مثال عن وحدة بطاقة هدايا](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="806bc-112">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="806bc-112">Module properties</span></span>

- <span data-ttu-id="806bc-113">**إظهار حقول** - تحدد هذه الخاصية الحقول التي يجب عرضها لبطاقات الهدايا بالإضافة إلى رقم بطاقة الهدايا، الذي يظهر دائمًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="806bc-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="806bc-114">على سبيل المثال، تدعم بعض بطاقات الهدايا رقم تعريف شخصي (PIN) ويدعم البعض الآخر عرض رمز PIN وتاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="806bc-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="806bc-115">بدلاً من ذلك،،يمكن تعيين هذه الخاصية إلى "بلا"، مما يؤدي إلى عرض رقم بطاقة الهدايا فقط ومن دون حقول إضافية.</span><span class="sxs-lookup"><span data-stu-id="806bc-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="806bc-116">القيم المدعومة:</span><span class="sxs-lookup"><span data-stu-id="806bc-116">Supported values:</span></span>
-   <span data-ttu-id="806bc-117">رمز PIN</span><span class="sxs-lookup"><span data-stu-id="806bc-117">PIN</span></span>
-   <span data-ttu-id="806bc-118">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="806bc-118">Expiration date</span></span>
-   <span data-ttu-id="806bc-119">رمز PIN وتاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="806bc-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="806bc-120">بلا‬‬</span><span class="sxs-lookup"><span data-stu-id="806bc-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="806bc-121">إعدادات الموقع لوحدات بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="806bc-121">Site settings for gift card modules</span></span>

<span data-ttu-id="806bc-122">في منشئ موقع Commerce، ضمن **إعدادات الموقع \> Extensions**، هناك إعداد لوحدة بطاقة هدايا يسمى **نوع بطاقة الهدايا المدعومة**.</span><span class="sxs-lookup"><span data-stu-id="806bc-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="806bc-123">يدعم هذا الإعداد ثلاث قيم:</span><span class="sxs-lookup"><span data-stu-id="806bc-123">This setting supports three values:</span></span>
- <span data-ttu-id="806bc-124">**بطاقة هدايا Dynamics 365** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 فقط.</span><span class="sxs-lookup"><span data-stu-id="806bc-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="806bc-125">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="806bc-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="806bc-126">**بطاقات هدايا SVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا SVS وGivex فقط.</span><span class="sxs-lookup"><span data-stu-id="806bc-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="806bc-127">هذا الإعداد مدعوم للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية بالإضافة إلى المستخدمين المجهولي الهوية.</span><span class="sxs-lookup"><span data-stu-id="806bc-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="806bc-128">**بطاقات هدايا Dynamics 365 وSVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="806bc-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="806bc-129">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="806bc-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="806bc-130">إضافة وحدة بطاقة هدايا إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="806bc-130">Add a gift card module to a page</span></span>

<span data-ttu-id="806bc-131">للحصول علي إرشادات حول كيفية إضافة وحدة بطاقة هدايا إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [وحدة السداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="806bc-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="806bc-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="806bc-132">Additional resources</span></span>

[<span data-ttu-id="806bc-133">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="806bc-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="806bc-134">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="806bc-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="806bc-135">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="806bc-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="806bc-136">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="806bc-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="806bc-137">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="806bc-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="806bc-138">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="806bc-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="806bc-139">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="806bc-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="806bc-140">دعم بطاقات الهدايا الخارجية</span><span class="sxs-lookup"><span data-stu-id="806bc-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
