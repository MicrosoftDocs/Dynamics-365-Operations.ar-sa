---
title: وحدة بطاقة الهدايا
description: يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962753"
---
# <a name="gift-card-module"></a><span data-ttu-id="9d924-103">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="9d924-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d924-104">يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d924-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9d924-105">يمكن استخدام وحدات بطاقات الهدايا في وحدات السداد مع الخروج لقبول بطاقات الهدايا، وهي عبارة عن طريقة دفع شائعة الاستخدام في حركات التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9d924-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="9d924-106">تدعم وحدة بطاقة الهدايا بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="9d924-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="9d924-107">يتم استرداد بطاقات الهدايا من SVS وGivex من خلال موفر الدفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="9d924-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="9d924-108">لمزيد من المعلومات جول دعم بطاقات الهدايا الخارجية مثل SVS وGivex، راجع [دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="9d924-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9d924-109">يتوفر دعم استرداد بطاقات الهدايا SVS وGivex اثناء سير عمل السداد مع الخروج في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="9d924-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="9d924-110">هناك وحدتان لبطاقة الهدايا:</span><span class="sxs-lookup"><span data-stu-id="9d924-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="9d924-111">**بطاقة الهدايا** - يمكن استخدام هذه الوحدة على صفحة السداد مع الخروج‬ لاسترداد بطاقة الهدايا كطريقة دفع.</span><span class="sxs-lookup"><span data-stu-id="9d924-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="9d924-112">**فحص رصيد بطاقة الهدايا** - يمكن استخدام هذه الوحدة على أي صفحة لفحص الرصيد على بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9d924-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="9d924-113">تتوفر هذه الوحدة في الإصدار 10.0.14 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="9d924-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="9d924-114">يتوفر دعم الوحدة النمطية فحص رصيد بطاقة الهدايا‬‏‫ في Dynamics 365 Commerce الإصدار 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="9d924-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="9d924-115">تعرض الصورة التالية مثالاً عن وحدة بطاقة هدايا في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="9d924-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![مثال عن وحدة بطاقة هدايا](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="9d924-117">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="9d924-117">Module properties</span></span>

- <span data-ttu-id="9d924-118">**إظهار حقول** - تحدد هذه الخاصية الحقول التي يجب عرضها لبطاقات الهدايا بالإضافة إلى رقم بطاقة الهدايا، الذي يظهر دائمًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="9d924-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="9d924-119">على سبيل المثال، تدعم بعض بطاقات الهدايا رقم تعريف شخصي (PIN) ويدعم البعض الآخر عرض رمز PIN وتاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="9d924-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="9d924-120">بدلاً من ذلك،،يمكن تعيين هذه الخاصية إلى "بلا"، مما يؤدي إلى عرض رقم بطاقة الهدايا فقط ومن دون حقول إضافية.</span><span class="sxs-lookup"><span data-stu-id="9d924-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="9d924-121">القيم المدعومة:</span><span class="sxs-lookup"><span data-stu-id="9d924-121">Supported values:</span></span>
-   <span data-ttu-id="9d924-122">رمز PIN</span><span class="sxs-lookup"><span data-stu-id="9d924-122">PIN</span></span>
-   <span data-ttu-id="9d924-123">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="9d924-123">Expiration date</span></span>
-   <span data-ttu-id="9d924-124">رمز PIN وتاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="9d924-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="9d924-125">بلا‬‬</span><span class="sxs-lookup"><span data-stu-id="9d924-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="9d924-126">إعدادات الموقع لوحدات بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="9d924-126">Site settings for gift card modules</span></span>

<span data-ttu-id="9d924-127">في منشئ موقع Commerce، ضمن **إعدادات الموقع \> Extensions**، هناك إعداد لوحدة بطاقة هدايا يسمى **نوع بطاقة الهدايا المدعومة**.</span><span class="sxs-lookup"><span data-stu-id="9d924-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="9d924-128">يدعم هذا الإعداد ثلاث قيم:</span><span class="sxs-lookup"><span data-stu-id="9d924-128">This setting supports three values:</span></span>
- <span data-ttu-id="9d924-129">**بطاقة هدايا Dynamics 365** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 فقط.</span><span class="sxs-lookup"><span data-stu-id="9d924-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="9d924-130">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9d924-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="9d924-131">**بطاقات هدايا SVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا SVS وGivex فقط.</span><span class="sxs-lookup"><span data-stu-id="9d924-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="9d924-132">هذا الإعداد مدعوم للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية بالإضافة إلى المستخدمين المجهولي الهوية.</span><span class="sxs-lookup"><span data-stu-id="9d924-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="9d924-133">**بطاقات هدايا Dynamics 365 وSVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 وSVS وGivex.</span><span class="sxs-lookup"><span data-stu-id="9d924-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="9d924-134">هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9d924-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d924-135">تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.11، وهي مطلوبة فقط إذا احتجت إلى دعم بطاقات الهدايا SVS أو Givex.</span><span class="sxs-lookup"><span data-stu-id="9d924-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="9d924-136">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="9d924-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="9d924-137">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="9d924-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="9d924-138">توسيع بطاقات الهدايا الداخلية لاستخدامها في واجهات متاجر التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9d924-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="9d924-139">بشكل افتراضي ، لم يتم تحسين بطاقات الهدايا الداخلية للاستخدام في واجهات متاجر التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9d924-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="9d924-140">لذلك ، قبل السماح باستخدام بطاقات الهدايا الداخلية للدفع ، يجب عليك تكوينها بملحقات تساعد في جعلها أكثر أمانًا.</span><span class="sxs-lookup"><span data-stu-id="9d924-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="9d924-141">في ما يلي مناطق بطاقات الهدايا التي يجب عليك تمديدها قبل السماح باستخدام بطاقات الهدايا الداخلية في الإنتاج:</span><span class="sxs-lookup"><span data-stu-id="9d924-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="9d924-142">**رقم بطاقة الهدايا** - يتم استخدام التسلسلات الرقمية لإنشاء أرقام بطاقات الهدايا لبطاقات الهدايا الداخلية.</span><span class="sxs-lookup"><span data-stu-id="9d924-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="9d924-143">نظرًا لأنه يمكن توقع تسلسل الأرقام بسهولة ، يجب عليك تمديد إنشاء أرقام بطاقات الهدايا بحيث يتم استخدام سلاسل عشوائية وآمنة من الناحية المشفرة لأرقام بطاقات الهدايا التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="9d924-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="9d924-144">**GetBalance** – يتم استخدام واجهة برمجة تطبيقات **GetBalance** للبحث عن أرصدة بطاقات الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9d924-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="9d924-145">بشكل افتراضي ، تكون واجهة برمجة التطبيقات هذه عامة.</span><span class="sxs-lookup"><span data-stu-id="9d924-145">By default, this API public.</span></span> <span data-ttu-id="9d924-146">إذا لم يكن رقم التعريف الشخصي مطلوبًا للبحث عن أرصدة بطاقات الهدايا ، فهناك خطر أن تستخدم هجمات القوة الغاشمة واجهة برمجة تطبيقات **GetBalance** لمحاولة البحث عن أرقام بطاقات الهدايا التي تحتوي على أرصدة.</span><span class="sxs-lookup"><span data-stu-id="9d924-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="9d924-147">من خلال تنفيذ كل من متطلبات PIN لبطاقات الهدايا الداخلية وتقييد واجهة برمجة التطبيقات ، يمكنك المساعدة في التخفيف من المخاطر.</span><span class="sxs-lookup"><span data-stu-id="9d924-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="9d924-148">**PIN** – افتراضيًا ، لا تدعم بطاقات الهدايا الداخلية أرقام التعريف الشخصية.</span><span class="sxs-lookup"><span data-stu-id="9d924-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="9d924-149">يجب توسيع بطاقات الهدايا الداخلية بحيث يكون رقم التعريف الشخصي مطلوبا للبحث عن الارصده.</span><span class="sxs-lookup"><span data-stu-id="9d924-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="9d924-150">يمكن استخدام هذه الوظيفة أيضا لتامين بطاقات الهدايا بعد المحاولات المتتالية غير الصحيحة لإدخال رقم التعريف الشخصي (PIN).</span><span class="sxs-lookup"><span data-stu-id="9d924-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="9d924-151">تمكين مدفوعات بطاقة الهدايا لسحب الضيف</span><span class="sxs-lookup"><span data-stu-id="9d924-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="9d924-152">بشكل افتراضي ، لا يتم تمكين مدفوعات بطاقات الهدايا لسداد الضيف (مجهول).</span><span class="sxs-lookup"><span data-stu-id="9d924-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="9d924-153">لتمكينها ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9d924-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="9d924-154">في إدارة Commerce، انتقل إلى **Retail وCommerce \> إعداد القنوات \> إعداد نقطة البيع\> نقطة البيع \> عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="9d924-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="9d924-155">حدد باستمرار (أو انقر بزر الماوس الأيمن) على رأس الشبكة ، ثم حدد **إدراج الأعمدة**.</span><span class="sxs-lookup"><span data-stu-id="9d924-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="9d924-156">في مربع الحوار **إدراج الأعمدة**، حدد خانة الاختيار **AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="9d924-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="9d924-157">حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="9d924-157">Select **Update**.</span></span>
1. <span data-ttu-id="9d924-158">بالنسبة للعمليات **520** (رصيد بطاقة الهدايا) و **214**، قم بتعيين قيمة **AllowAnonymousAccess** إلى **1**.</span><span class="sxs-lookup"><span data-stu-id="9d924-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="9d924-159">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9d924-159">Select **Save**.</span></span>
1. <span data-ttu-id="9d924-160">قم بتشغيل وظيفة مجدول **1090** لمزامنة التغييرات لقاعدة بيانات القناة.</span><span class="sxs-lookup"><span data-stu-id="9d924-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="9d924-161">إضافة وحدة بطاقة هدايا إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="9d924-161">Add a gift card module to a page</span></span>

<span data-ttu-id="9d924-162">للحصول على إرشادات حول كيفية إضافة وحدة بطاقة هدايا إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [وحدة السداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="9d924-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d924-163">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9d924-163">Additional resources</span></span>

[<span data-ttu-id="9d924-164">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="9d924-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9d924-165">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="9d924-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="9d924-166">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="9d924-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="9d924-167">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="9d924-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="9d924-168">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="9d924-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="9d924-169">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="9d924-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="9d924-170">الوحدة النمطية لمعلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="9d924-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="9d924-171">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="9d924-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="9d924-172">دعم بطاقات الهدايا الخارجية</span><span class="sxs-lookup"><span data-stu-id="9d924-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="9d924-173">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="9d924-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
