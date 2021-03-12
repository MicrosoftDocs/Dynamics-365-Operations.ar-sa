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
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980372"
---
# <a name="gift-card-module"></a><span data-ttu-id="d5cb7-103">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="d5cb7-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5cb7-104">يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d5cb7-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d5cb7-105">Overview</span></span>

<span data-ttu-id="d5cb7-106">يمكن استخدام وحدات بطاقات الهدايا في وحدات السداد مع الخروج لقبول بطاقات الهدايا، وهي عبارة عن طريقة دفع شائعة الاستخدام في حركات التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="d5cb7-107">تدعم وحدة بطاقة الهدايا بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="d5cb7-108">يتم استرداد بطاقات الهدايا من SVS وGivex من خلال موفر الدفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="d5cb7-109">لمزيد من المعلومات جول دعم بطاقات الهدايا الخارجية مثل SVS وGivex، راجع [دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="d5cb7-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d5cb7-110">يتوفر دعم استرداد بطاقات الهدايا SVS وGivex اثناء سير عمل السداد مع الخروج في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="d5cb7-111">هناك وحدتان لبطاقة الهدايا:</span><span class="sxs-lookup"><span data-stu-id="d5cb7-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="d5cb7-112">**بطاقة الهدايا** - يمكن استخدام هذه الوحدة على صفحة السداد مع الخروج‬ لاسترداد بطاقة الهدايا كطريقة دفع.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="d5cb7-113">**فحص رصيد بطاقة الهدايا** - يمكن استخدام هذه الوحدة على أي صفحة لفحص الرصيد على بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="d5cb7-114">تتوفر هذه الوحدة في الإصدار 10.0.14 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cb7-115">يتوفر دعم الوحدة النمطية فحص رصيد بطاقة الهدايا‬‏‫ في Dynamics 365 Commerce الإصدار 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="d5cb7-116">تعرض الصورة التالية مثالاً عن وحدة بطاقة هدايا في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![مثال عن وحدة بطاقة هدايا](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="d5cb7-118">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="d5cb7-118">Module properties</span></span>

- <span data-ttu-id="d5cb7-119">**إظهار حقول** - تحدد هذه الخاصية الحقول التي يجب عرضها لبطاقات الهدايا بالإضافة إلى رقم بطاقة الهدايا، الذي يظهر دائمًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="d5cb7-120">على سبيل المثال، تدعم بعض بطاقات الهدايا رقم تعريف شخصي (PIN) ويدعم البعض الآخر عرض رمز PIN وتاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="d5cb7-121">بدلاً من ذلك،،يمكن تعيين هذه الخاصية إلى "بلا"، مما يؤدي إلى عرض رقم بطاقة الهدايا فقط ومن دون حقول إضافية.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="d5cb7-122">القيم المدعومة:</span><span class="sxs-lookup"><span data-stu-id="d5cb7-122">Supported values:</span></span>
-   <span data-ttu-id="d5cb7-123">رمز PIN</span><span class="sxs-lookup"><span data-stu-id="d5cb7-123">PIN</span></span>
-   <span data-ttu-id="d5cb7-124">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="d5cb7-124">Expiration date</span></span>
-   <span data-ttu-id="d5cb7-125">رمز PIN وتاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="d5cb7-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="d5cb7-126">بلا‬‬</span><span class="sxs-lookup"><span data-stu-id="d5cb7-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="d5cb7-127">إعدادات الموقع لوحدات بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="d5cb7-127">Site settings for gift card modules</span></span>

<span data-ttu-id="d5cb7-128">في منشئ موقع Commerce، ضمن **إعدادات الموقع \> Extensions**، هناك إعداد لوحدة بطاقة هدايا يسمى **نوع بطاقة الهدايا المدعومة**.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="d5cb7-129">يدعم هذا الإعداد ثلاث قيم:</span><span class="sxs-lookup"><span data-stu-id="d5cb7-129">This setting supports three values:</span></span>
- <span data-ttu-id="d5cb7-130">**بطاقة هدايا Dynamics 365** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 فقط.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="d5cb7-131">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="d5cb7-132">**بطاقات هدايا SVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا SVS وGivex فقط.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="d5cb7-133">هذا الإعداد مدعوم للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية بالإضافة إلى المستخدمين المجهولي الهوية.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="d5cb7-134">**بطاقات هدايا Dynamics 365 وSVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="d5cb7-135">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cb7-136">تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.11، وهي مطلوبة فقط إذا احتجت إلى دعم بطاقات الهدايا SVS أو Givex.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="d5cb7-137">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="d5cb7-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="d5cb7-138">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="d5cb7-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="d5cb7-139">إضافة وحدة بطاقة هدايا إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="d5cb7-139">Add a gift card module to a page</span></span>

<span data-ttu-id="d5cb7-140">للحصول على إرشادات حول كيفية إضافة وحدة بطاقة هدايا إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [وحدة السداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d5cb7-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5cb7-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d5cb7-141">Additional resources</span></span>

[<span data-ttu-id="d5cb7-142">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="d5cb7-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d5cb7-143">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="d5cb7-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d5cb7-144">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="d5cb7-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d5cb7-145">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="d5cb7-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d5cb7-146">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="d5cb7-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d5cb7-147">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="d5cb7-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d5cb7-148">الوحدة النمطية لمعلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="d5cb7-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d5cb7-149">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="d5cb7-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d5cb7-150">دعم بطاقات الهدايا الخارجية</span><span class="sxs-lookup"><span data-stu-id="d5cb7-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="d5cb7-151">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="d5cb7-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
