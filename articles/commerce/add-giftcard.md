---
title: وحدة بطاقة الهدايا
description: يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206285"
---
# <a name="gift-card-module"></a><span data-ttu-id="ac50f-103">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="ac50f-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac50f-104">يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ac50f-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ac50f-105">يمكن استخدام وحدات بطاقات الهدايا في وحدات السداد مع الخروج لقبول بطاقات الهدايا، وهي عبارة عن طريقة دفع شائعة الاستخدام في حركات التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ac50f-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="ac50f-106">تدعم وحدة بطاقة الهدايا بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="ac50f-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="ac50f-107">يتم استرداد بطاقات الهدايا من SVS وGivex من خلال موفر الدفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="ac50f-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="ac50f-108">لمزيد من المعلومات جول دعم بطاقات الهدايا الخارجية مثل SVS وGivex، راجع [دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="ac50f-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ac50f-109">يتوفر دعم استرداد بطاقات الهدايا SVS وGivex اثناء سير عمل السداد مع الخروج في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="ac50f-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="ac50f-110">هناك وحدتان لبطاقة الهدايا:</span><span class="sxs-lookup"><span data-stu-id="ac50f-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="ac50f-111">**بطاقة الهدايا** - يمكن استخدام هذه الوحدة على صفحة السداد مع الخروج‬ لاسترداد بطاقة الهدايا كطريقة دفع.</span><span class="sxs-lookup"><span data-stu-id="ac50f-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="ac50f-112">**فحص رصيد بطاقة الهدايا** - يمكن استخدام هذه الوحدة على أي صفحة لفحص الرصيد على بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="ac50f-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="ac50f-113">تتوفر هذه الوحدة في الإصدار 10.0.14 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="ac50f-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="ac50f-114">يتوفر دعم الوحدة النمطية فحص رصيد بطاقة الهدايا‬‏‫ في Dynamics 365 Commerce الإصدار 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="ac50f-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="ac50f-115">تعرض الصورة التالية مثالاً عن وحدة بطاقة هدايا في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="ac50f-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![مثال عن وحدة بطاقة هدايا](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="ac50f-117">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="ac50f-117">Module properties</span></span>

- <span data-ttu-id="ac50f-118">**إظهار حقول** - تحدد هذه الخاصية الحقول التي يجب عرضها لبطاقات الهدايا بالإضافة إلى رقم بطاقة الهدايا، الذي يظهر دائمًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="ac50f-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="ac50f-119">على سبيل المثال، تدعم بعض بطاقات الهدايا رقم تعريف شخصي (PIN) ويدعم البعض الآخر عرض رمز PIN وتاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="ac50f-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="ac50f-120">بدلاً من ذلك،،يمكن تعيين هذه الخاصية إلى "بلا"، مما يؤدي إلى عرض رقم بطاقة الهدايا فقط ومن دون حقول إضافية.</span><span class="sxs-lookup"><span data-stu-id="ac50f-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="ac50f-121">القيم المدعومة:</span><span class="sxs-lookup"><span data-stu-id="ac50f-121">Supported values:</span></span>
-   <span data-ttu-id="ac50f-122">رمز PIN</span><span class="sxs-lookup"><span data-stu-id="ac50f-122">PIN</span></span>
-   <span data-ttu-id="ac50f-123">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="ac50f-123">Expiration date</span></span>
-   <span data-ttu-id="ac50f-124">رمز PIN وتاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="ac50f-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="ac50f-125">بلا‬‬</span><span class="sxs-lookup"><span data-stu-id="ac50f-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="ac50f-126">إعدادات الموقع لوحدات بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="ac50f-126">Site settings for gift card modules</span></span>

<span data-ttu-id="ac50f-127">في منشئ موقع Commerce، ضمن **إعدادات الموقع \> Extensions**، هناك إعداد لوحدة بطاقة هدايا يسمى **نوع بطاقة الهدايا المدعومة**.</span><span class="sxs-lookup"><span data-stu-id="ac50f-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="ac50f-128">يدعم هذا الإعداد ثلاث قيم:</span><span class="sxs-lookup"><span data-stu-id="ac50f-128">This setting supports three values:</span></span>
- <span data-ttu-id="ac50f-129">**بطاقة هدايا Dynamics 365** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 فقط.</span><span class="sxs-lookup"><span data-stu-id="ac50f-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="ac50f-130">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ac50f-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="ac50f-131">**بطاقات هدايا SVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا SVS وGivex فقط.</span><span class="sxs-lookup"><span data-stu-id="ac50f-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="ac50f-132">هذا الإعداد مدعوم للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية بالإضافة إلى المستخدمين المجهولي الهوية.</span><span class="sxs-lookup"><span data-stu-id="ac50f-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="ac50f-133">**بطاقات هدايا Dynamics 365 وSVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="ac50f-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="ac50f-134">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ac50f-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac50f-135">تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.11، وهي مطلوبة فقط إذا احتجت إلى دعم بطاقات الهدايا SVS أو Givex.</span><span class="sxs-lookup"><span data-stu-id="ac50f-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="ac50f-136">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ac50f-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="ac50f-137">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="ac50f-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="ac50f-138">إضافة وحدة بطاقة هدايا إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="ac50f-138">Add a gift card module to a page</span></span>

<span data-ttu-id="ac50f-139">للحصول على إرشادات حول كيفية إضافة وحدة بطاقة هدايا إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [وحدة السداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="ac50f-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac50f-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ac50f-140">Additional resources</span></span>

[<span data-ttu-id="ac50f-141">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="ac50f-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ac50f-142">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="ac50f-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="ac50f-143">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="ac50f-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ac50f-144">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="ac50f-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="ac50f-145">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="ac50f-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="ac50f-146">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="ac50f-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="ac50f-147">الوحدة النمطية لمعلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ac50f-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="ac50f-148">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="ac50f-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ac50f-149">دعم بطاقات الهدايا الخارجية</span><span class="sxs-lookup"><span data-stu-id="ac50f-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="ac50f-150">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="ac50f-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]