---
title: وحدة بطاقة الهدايا
description: يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761071"
---
# <a name="gift-card-module"></a><span data-ttu-id="810e0-103">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="810e0-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="810e0-104">يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="810e0-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="810e0-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="810e0-105">Overview</span></span>

<span data-ttu-id="810e0-106">يمكن استخدام وحدات بطاقات الهدايا في وحدات السداد مع الخروج لقبول بطاقات الهدايا، وهي عبارة عن طريقة دفع شائعة الاستخدام في حركات التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="810e0-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="810e0-107">تدعم وحدة بطاقة الهدايا بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="810e0-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="810e0-108">يتم استرداد بطاقات الهدايا من SVS وGivex من خلال موفر الدفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="810e0-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="810e0-109">لمزيد من المعلومات جول دعم بطاقات الهدايا الخارجية مثل SVS وGivex، راجع [دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="810e0-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="810e0-110">هناك وحدتان لبطاقة الهدايا:</span><span class="sxs-lookup"><span data-stu-id="810e0-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="810e0-111">**بطاقة الهدايا** - يمكن استخدام هذه الوحدة على صفحة السداد مع الخروج‬ لاسترداد بطاقة الهدايا كطريقة دفع.</span><span class="sxs-lookup"><span data-stu-id="810e0-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="810e0-112">**فحص رصيد بطاقة الهدايا** - يمكن استخدام هذه الوحدة على أي صفحة لفحص الرصيد على بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="810e0-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="810e0-113">تتوفر هذه الوحدة في الإصدار 10.0.14 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="810e0-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="810e0-114">تعرض الصورة التالية مثالاً عن وحدة بطاقة هدايا في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="810e0-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![مثال عن وحدة بطاقة هدايا](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="810e0-116">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="810e0-116">Module properties</span></span>

- <span data-ttu-id="810e0-117">**إظهار حقول** - تحدد هذه الخاصية الحقول التي يجب عرضها لبطاقات الهدايا بالإضافة إلى رقم بطاقة الهدايا، الذي يظهر دائمًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="810e0-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="810e0-118">على سبيل المثال، تدعم بعض بطاقات الهدايا رقم تعريف شخصي (PIN) ويدعم البعض الآخر عرض رمز PIN وتاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="810e0-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="810e0-119">بدلاً من ذلك،،يمكن تعيين هذه الخاصية إلى "بلا"، مما يؤدي إلى عرض رقم بطاقة الهدايا فقط ومن دون حقول إضافية.</span><span class="sxs-lookup"><span data-stu-id="810e0-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="810e0-120">القيم المدعومة:</span><span class="sxs-lookup"><span data-stu-id="810e0-120">Supported values:</span></span>
-   <span data-ttu-id="810e0-121">رمز PIN</span><span class="sxs-lookup"><span data-stu-id="810e0-121">PIN</span></span>
-   <span data-ttu-id="810e0-122">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="810e0-122">Expiration date</span></span>
-   <span data-ttu-id="810e0-123">رمز PIN وتاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="810e0-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="810e0-124">بلا‬‬</span><span class="sxs-lookup"><span data-stu-id="810e0-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="810e0-125">إعدادات الموقع لوحدات بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="810e0-125">Site settings for gift card modules</span></span>

<span data-ttu-id="810e0-126">في منشئ موقع Commerce، ضمن **إعدادات الموقع \> Extensions**، هناك إعداد لوحدة بطاقة هدايا يسمى **نوع بطاقة الهدايا المدعومة**.</span><span class="sxs-lookup"><span data-stu-id="810e0-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="810e0-127">يدعم هذا الإعداد ثلاث قيم:</span><span class="sxs-lookup"><span data-stu-id="810e0-127">This setting supports three values:</span></span>
- <span data-ttu-id="810e0-128">**بطاقة هدايا Dynamics 365** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 فقط.</span><span class="sxs-lookup"><span data-stu-id="810e0-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="810e0-129">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="810e0-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="810e0-130">**بطاقات هدايا SVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا SVS وGivex فقط.</span><span class="sxs-lookup"><span data-stu-id="810e0-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="810e0-131">هذا الإعداد مدعوم للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية بالإضافة إلى المستخدمين المجهولي الهوية.</span><span class="sxs-lookup"><span data-stu-id="810e0-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="810e0-132">**بطاقات هدايا Dynamics 365 وSVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="810e0-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="810e0-133">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="810e0-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="810e0-134">إضافة وحدة بطاقة هدايا إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="810e0-134">Add a gift card module to a page</span></span>

<span data-ttu-id="810e0-135">للحصول علي إرشادات حول كيفية إضافة وحدة بطاقة هدايا إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [وحدة السداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="810e0-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="810e0-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="810e0-136">Additional resources</span></span>

[<span data-ttu-id="810e0-137">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="810e0-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="810e0-138">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="810e0-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="810e0-139">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="810e0-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="810e0-140">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="810e0-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="810e0-141">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="810e0-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="810e0-142">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="810e0-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="810e0-143">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="810e0-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="810e0-144">دعم بطاقات الهدايا الخارجية</span><span class="sxs-lookup"><span data-stu-id="810e0-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
