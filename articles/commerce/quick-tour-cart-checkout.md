---
title: نظرة عامة على صفحات سلة التسوق والسداد مع الخروج
description: يقدم هذا الموضوع نظرة عامة صفحات سلة التسوق والسداد مع الخروج‬ في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: a574494784e9a534307cceff584e047d870dc401
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027929"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="0921d-103">نظرة عامة على صفحات سلة التسوق والسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="0921d-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0921d-104">يقدم هذا الموضوع نظرة عامة صفحات سلة التسوق والسداد مع الخروج‬ في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0921d-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0921d-105">تعرض صفحة سلة التسوق في موقع ويب التجارة الإلكترونية كافة الأصناف التي قام العميل بإضافتها إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="0921d-105">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="0921d-106">يتم إنشاء صفحة سلة التسوق باستخدام الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="0921d-106">The cart page is built by using the cart module.</span></span> <span data-ttu-id="0921d-107">تُمثل وحدة سلة التسوق حاوية تستضيف كافة الوحدات المطلوبة لإظهار الأصناف الموجودة في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="0921d-107">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="0921d-108">كما يمكن للوحدة النمطية لسلة التسوق استخدام الوحدات النمطية الأخرى لإظهار ملخص الأمر وأية أكواد ترويجية تم تطبيقها على أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="0921d-108">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="0921d-109">تقدم صفحة السداد مع الخروج بموقع التجارة الإلكترونية سير عمل خطوة بخطوة يمكن للعملاء اتباعه لإدخال كافة المعلومات المطلوبة لإصدار أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="0921d-109">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="0921d-110">ويُمكن أن تشمل وحدة السداد مع الخروج التي تُعالج عنوان الشحن وأساليب الشحن ومعلومات الفوترة وملخص الأمر والمعلومات الأخرى ذات الصلة بأوامر العميل.</span><span class="sxs-lookup"><span data-stu-id="0921d-110">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="0921d-111">صفحة سلة التسوق</span><span class="sxs-lookup"><span data-stu-id="0921d-111">Cart page</span></span>

<span data-ttu-id="0921d-112">تعمل صفحة السلة كحقيبة تسوق وتتضمن كافة الأصناف التي تمت إضافتها إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="0921d-112">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="0921d-113">يبين الرسم التوضيحي التالي مثال على صفحة سلة التسوق تم إنشاؤها باستخدام مكتبة الوحدات النمطية والنسق "Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="0921d-113">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![مثال لصفحة سلة تسوق](./media/cart2.PNG)

<span data-ttu-id="0921d-115">يعرض الجزء الأساسي لصفحة سلة التسوق كافة الأصناف التي قام العميل بإضافتها إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="0921d-115">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="0921d-116">يتم عرضكافة الخصومات القابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="0921d-116">All applicable discounts are showcased.</span></span> <span data-ttu-id="0921d-117">تشمل هذه الخصومات الخصومات المعقدة.</span><span class="sxs-lookup"><span data-stu-id="0921d-117">These discounts include complex discounts.</span></span> <span data-ttu-id="0921d-118">تشمل الأمثلة "شراء 3 أصناف للحصول على خصم 10%" أو "شراء زجاجة وحقيبة ظهر للحصول على خصم 10%."</span><span class="sxs-lookup"><span data-stu-id="0921d-118">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="0921d-119">تعرض الوحدة النمطية لملخص الأمر المبلغ المستحق بعد تطبيق الخصومات والشحن والضرائب وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="0921d-119">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="0921d-120">كما توجد أيضا وحدة الكود الترويجي التي تتيح للعميل تطبيق الأكواد الترويجية أو ازالتها.</span><span class="sxs-lookup"><span data-stu-id="0921d-120">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="0921d-121">يمكن للعميل التسوق بشكل مجهول أو كمستخدم مسجل دخوله.</span><span class="sxs-lookup"><span data-stu-id="0921d-121">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="0921d-122">في حالة تسجيل دخول عميل، يتم الاحتفاظ بالأصناف الموجودة في سلة التسوق بين جلسات العمل.</span><span class="sxs-lookup"><span data-stu-id="0921d-122">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="0921d-123">وبهذه الطريقة، يمكن للعميل متابعة التسوق من عدة أجهزة.</span><span class="sxs-lookup"><span data-stu-id="0921d-123">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="0921d-124">من سلة التسوق، يمكن للعميل المتابعة للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="0921d-124">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="0921d-125">يمكن للعميل بدء السداد مع الخروج كمستخدم ضيف أو كمستخدم مسجل دخوله.</span><span class="sxs-lookup"><span data-stu-id="0921d-125">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="0921d-126">لمزيد من المعلومات حول كيفية تأليف صفحة سلة تسوق، راجع [إضافة وحدة سلة التسوق إلى صفحة‬](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="0921d-126">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="0921d-127">صفحة السداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="0921d-127">Checkout page</span></span>

<span data-ttu-id="0921d-128">صفحة السداد مع الخروج هي المكان الذي يقوم فيه العميل بإدخال المعلومات المطلوبة لإصدار أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="0921d-128">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="0921d-129">يبين الرسم التوضيحي التالي مثال لصفحة السداد مع الخروج التي تم إنشاؤها باستخدام مكتبة الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="0921d-129">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![مثال لصفحة سداد مع الخروج](./media/Checkout.PNG)

<span data-ttu-id="0921d-131">النص الأساسي لصفحة السداد مع الخروج هو المكان الذي يتم فيه جمع كافة معلومات الأمر.</span><span class="sxs-lookup"><span data-stu-id="0921d-131">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="0921d-132">وتتضمن هذه المعلومات عنوان الشحن وخيارات التسليم ومعلومات الدفع.</span><span class="sxs-lookup"><span data-stu-id="0921d-132">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="0921d-133">عملية السداد مع الخروج هي سير عمل خطوة بخطوة، لأنه يجب إدخال المعلومات بترتيب معين لتتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="0921d-133">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="0921d-134">على سبيل المثال، يجب إدخال عنوان الشحن قبل ان يتم حساب تكاليف الشحن ويمكن اعتماد الدفع.</span><span class="sxs-lookup"><span data-stu-id="0921d-134">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="0921d-135">عنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="0921d-135">Shipping address</span></span>

<span data-ttu-id="0921d-136">يلزم وجود عنوان شحن إذا كان يجب شحن الأصناف.</span><span class="sxs-lookup"><span data-stu-id="0921d-136">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="0921d-137">يمكن تكوين تنسيق عناوين الشحن لكل إعداد محلي في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0921d-137">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0921d-138">على سبيل المثال، إذا كانت الأصناف سيتم شحنها إلى الولايات المتحدة، فيجب أن يتضمن عنوان الشحن عنوان الشارع والولاية والرمز البريدي.</span><span class="sxs-lookup"><span data-stu-id="0921d-138">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="0921d-139">يتم التحقق من الإدخالات الأساسية لحقول عنوان الشحن، مثل التحقق من صحة الأحرف الأبجدية الرقمية والحد الأقصى للطول والأرقام.</span><span class="sxs-lookup"><span data-stu-id="0921d-139">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="0921d-140">على الرغم من أنه لا يتم التحقق من صحة العنوان نفسه، يمكن إجراء هذا التحقق باستخدام خدمات مخصصة لجهات خارجية.</span><span class="sxs-lookup"><span data-stu-id="0921d-140">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="0921d-141">يتم تطبيق عنوان الشحن على كافة الأصناف الموجودة في سلة التسوق التي تم تحديد الخيار "شحن" لها.</span><span class="sxs-lookup"><span data-stu-id="0921d-141">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="0921d-142">إذا كنت تستخدم سير عمل السداد مع الخروج الذي تم توفيره في مكتبة الوحدات النمطية، فسيتعذر شحن أصناف السلة الفردية إلى عناوين مختلفة.</span><span class="sxs-lookup"><span data-stu-id="0921d-142">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="0921d-143">وإذا طلبت هذه القدرة، فيمكن تطبيقها من خلال تخصيص الوحدات النمطية لعملية السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="0921d-143">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="0921d-144">بعد توفير عنوان الشحن، يتم عرض طرق الشحن المتوفرة من متجر Dynamics 365 Commerce على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="0921d-144">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="0921d-145">يمكن تكوين طرق الشحن والعناوين التي تدعمها في Commerce.</span><span class="sxs-lookup"><span data-stu-id="0921d-145">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="0921d-146">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="0921d-146">Payment</span></span>

<span data-ttu-id="0921d-147">الخطوة التالية في سير عمل السداد والخروج هي عملية الدفع.</span><span class="sxs-lookup"><span data-stu-id="0921d-147">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="0921d-148">في التجارة الإلكترونية، يمكن استخدام طرق دفع متعددة لإصدار الطلبات الشراء، مثل بطاقات الائتمان وبطاقات الهدايا ونقاط الولاء.</span><span class="sxs-lookup"><span data-stu-id="0921d-148">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="0921d-149">يمكن استخدام مجموعة من أساليب الدفع هذه أيضا.</span><span class="sxs-lookup"><span data-stu-id="0921d-149">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="0921d-150">ووفقا لطرق الدفع المستخدمة، قد يلزم إدخال معلومات إضافية.</span><span class="sxs-lookup"><span data-stu-id="0921d-150">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="0921d-151">على سبيل المثال، يتطلب الدفع بواسطة بطاقة الائتمان عنوان الفوتره.</span><span class="sxs-lookup"><span data-stu-id="0921d-151">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="0921d-152">تتم معالجة مدفوعات بطاقة الائتمان باستخدام موصل مدفوعات Adyen.</span><span class="sxs-lookup"><span data-stu-id="0921d-152">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="0921d-153">نقاط الولاء</span><span class="sxs-lookup"><span data-stu-id="0921d-153">Loyalty points</span></span>

<span data-ttu-id="0921d-154">أثناء سير عمل عملية السداد والخروج، يمكن للعميل الذي يعتبر عضوًا في برنامج الولاء ومن لديه نقاط ولاء مستحقة استرداد نقاط الولاء الخاصة بأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="0921d-154">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="0921d-155">يتم عرض الوحدة النمطية لنقاط الولاء فقط إذا كان للعميل عضوية ولاء حالية.</span><span class="sxs-lookup"><span data-stu-id="0921d-155">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="0921d-156">تكون هذه الوحدة النمطية مخفية للمستخدمين غير الأعضاء والمستخدمين الضيوف.</span><span class="sxs-lookup"><span data-stu-id="0921d-156">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="0921d-157">بطاقات الهدايا</span><span class="sxs-lookup"><span data-stu-id="0921d-157">Gift cards</span></span>

<span data-ttu-id="0921d-158">تتيح مكتبة الوحدات النمطية إمكانية استرجاع بطاقات الهدايا الداخلية الخاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="0921d-158">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="0921d-159">لتطبيق بطاقة هدايا داخلية، يجب تسجيل دخول العميل.</span><span class="sxs-lookup"><span data-stu-id="0921d-159">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="0921d-160">لمزيد من الأمان، نوصي بتخصيص سير العمل باستخدام رقم التعريف الشخصي (PIN) لبطاقات الهدايا الداخلية.</span><span class="sxs-lookup"><span data-stu-id="0921d-160">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="0921d-161">المستخدمون الضيوف والمسجل دخولهم</span><span class="sxs-lookup"><span data-stu-id="0921d-161">Signed-in and guest users</span></span>

<span data-ttu-id="0921d-162">يمكن للعميل إكمال عملية السداد مع الخروج كمستخدم ضيف أو كمستخدم مسجل دخوله.</span><span class="sxs-lookup"><span data-stu-id="0921d-162">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="0921d-163">إذا قام العميل بتسجيل الدخول، سيتم تلقائيًا استرداد معلومات الحساب مثل عناوين الشحن المحفوظة وتفاصيل بطاقة الائتمان المحفوظة.</span><span class="sxs-lookup"><span data-stu-id="0921d-163">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="0921d-164">ملخص الأمر</span><span class="sxs-lookup"><span data-stu-id="0921d-164">Order summary</span></span>

<span data-ttu-id="0921d-165">تعرض عملية السداد مع الخروج ملخصًا لأصناف البنود في سلة التسوق، حتى يتمكن العميل من التحقق من الأمر قبل إصدار الأمر.</span><span class="sxs-lookup"><span data-stu-id="0921d-165">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before placing the order.</span></span> <span data-ttu-id="0921d-166">لا يمكن تحرير أصناف البنود أثناء سير عمل عملية السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="0921d-166">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="0921d-167">ومع ذلك، يتم توفير ارتباط لسلة التسوق في حالة رغبة المستخدم في الرجوع إلى أصناف البنود وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="0921d-167">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="0921d-168">وبعدما يوفر العميل معلومات الشحن والفوترة، يعكس ملخص الأمر المبلغ المستحق بعد نقاط الولاء وبطاقات الهدايا والمدفوعات الأخرى التي تم تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="0921d-168">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="0921d-169">بريد إلكتروني لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="0921d-169">Order confirmation and email</span></span>

<span data-ttu-id="0921d-170">عندما يقوم العميل بإصدار طلب الشراء، يتم توفير رقم تأكيد.</span><span class="sxs-lookup"><span data-stu-id="0921d-170">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="0921d-171">وفي هذه المرحلة، يكون قد تم اعتماد الدفع ولكن لم يتم تحصيله.</span><span class="sxs-lookup"><span data-stu-id="0921d-171">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="0921d-172">لا يتم تحصيل الدفع الا إذا تم استيفاء أمر الشراء (أي ، عندما يتم شحنه أو انتقاءه).</span><span class="sxs-lookup"><span data-stu-id="0921d-172">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="0921d-173">بعد إنشاء أمر الشراء، يتم إرسال تأكيد بالبريد الإلكتروني إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="0921d-173">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="0921d-174">لمزيد من المعلومات حول كيفية تأليف صفحة السداد مع الخروج، راجع [إضافة وحدة السداد مع الخروج إلى صفحة](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="0921d-174">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0921d-175">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0921d-175">Additional resources</span></span>

[<span data-ttu-id="0921d-176">نظرة عامة على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="0921d-176">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="0921d-177">نظرة عامة على صفحات تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="0921d-177">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="0921d-178">نظرة عامة على صفحات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="0921d-178">Account management pages overview</span></span>](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
