---
title: الوحدة النمطية للسداد مع الخروج
description: يوضح هذا الموضوع كيفية إضافة الوحدة النمطية للسداد مع الخروج إلى صفحة، وتعيين الخصائص المطلوبة.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 28d58caba71ea98ccf163e756e879587aa254bb3
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410050"
---
# <a name="checkout-module"></a><span data-ttu-id="b403c-103">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="b403c-103">Checkout module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b403c-104">يوضح هذا الموضوع كيفية إضافة الوحدة النمطية للسداد مع الخروج إلى صفحة، وتعيين الخصائص المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b403c-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="b403c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="b403c-105">Overview</span></span>

<span data-ttu-id="b403c-106">تُمثل الوحدة النمطية للسداد مع الخروج حاوية خاصة تستضيف كافة الوحدات المطلوبة لإنشاء أمر.</span><span class="sxs-lookup"><span data-stu-id="b403c-106">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="b403c-107">وهي توضح التدفق خطوة بخطوة الذي يستخدمه العميل لإدخال كافة المعلومات ذات الصلة لإجراء عملية شراء.</span><span class="sxs-lookup"><span data-stu-id="b403c-107">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="b403c-108">وهي تسجل عنوان الشحن وأسلوب الشحن ومعلومات الفوترة.</span><span class="sxs-lookup"><span data-stu-id="b403c-108">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="b403c-109">وتوفر أيضًا ملخص الأمر ومعلومات أخرى مرتبطة بأم العميل.</span><span class="sxs-lookup"><span data-stu-id="b403c-109">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="b403c-110">تعرض الوحدة النمطية للسداد مع الخروج البيانات بناءً على مُعرف سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="b403c-110">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="b403c-111">يتم حفظ مُعرف سلة التسوق كملف تعريف ارتباط للمستعرض.</span><span class="sxs-lookup"><span data-stu-id="b403c-111">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="b403c-112">ويُكون مُعرف سلة التسوق مطلوبًا لعرض المعلومات في الوحدة النمطية للسداد مع الخروج، مثل الأصناف في الأمر والمبلغ الإجمالي والخصومات.</span><span class="sxs-lookup"><span data-stu-id="b403c-112">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="b403c-113">تعرض الصورة التالية مثالاُ عن وحدة السداد مع الخروج لشركة Fabrikam في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-113">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![مثال عن وحدة السداد مع الخروج‬](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="b403c-115">خصائص الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="b403c-115">Checkout module properties</span></span>

<span data-ttu-id="b403c-116">تعرض الوحدة النمطية للسداد مع الخروج ملخص الأمر وتوفر الوظيفة الخاصة بوضع أمر.</span><span class="sxs-lookup"><span data-stu-id="b403c-116">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="b403c-117">لتجميع كافة معلومات العميل المطلوبة قبل وضع الأمر، يجب إضافة المزيد من الوحدات النمطية إلى الوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-117">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="b403c-118">وبالتالي، تتوفر لبائعي التجزئة المرونة الكافية لإضافة وحدات نمطيه مخصصة إلى سير عمل السداد مع الخروج أو لاستثناء وحدات نمطية، استنادًا إلى متطلباتهم.</span><span class="sxs-lookup"><span data-stu-id="b403c-118">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

| <span data-ttu-id="b403c-119">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="b403c-119">Property name</span></span> | <span data-ttu-id="b403c-120">القيم</span><span class="sxs-lookup"><span data-stu-id="b403c-120">Values</span></span> | <span data-ttu-id="b403c-121">الوصف</span><span class="sxs-lookup"><span data-stu-id="b403c-121">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b403c-122">عنوان ‏‫السداد مع الخروج‬</span><span class="sxs-lookup"><span data-stu-id="b403c-122">Checkout heading</span></span> | <span data-ttu-id="b403c-123">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="b403c-123">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b403c-124">عنوان للوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-124">A heading for the checkout module.</span></span> |
| <span data-ttu-id="b403c-125">عنوان ملخص الأمر</span><span class="sxs-lookup"><span data-stu-id="b403c-125">Order summary heading</span></span> | <span data-ttu-id="b403c-126">نص العنوان</span><span class="sxs-lookup"><span data-stu-id="b403c-126">Heading text</span></span> | <span data-ttu-id="b403c-127">عنوان لقسم ملخص الأمر الخاص بالوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="b403c-127">A heading for the order summary section of the module.</span></span> |
| <span data-ttu-id="b403c-128">عنوان بنود سلة التسوق</span><span class="sxs-lookup"><span data-stu-id="b403c-128">Cart line items heading</span></span> | <span data-ttu-id="b403c-129">نص العنوان</span><span class="sxs-lookup"><span data-stu-id="b403c-129">Heading text</span></span> | <span data-ttu-id="b403c-130">عنوان لبنود سلة التسوق التي تظهر في الوحدة النمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-130">A heading for cart line items that are shown in the checkout module.</span></span> |
| <span data-ttu-id="b403c-131">إظهار تكاليف الشحن على البند</span><span class="sxs-lookup"><span data-stu-id="b403c-131">Show shipping charges on line item</span></span> | <span data-ttu-id="b403c-132">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="b403c-132">**True** or **False**</span></span> | <span data-ttu-id="b403c-133">في حالة تعيين هذه الخاصية إلى **صواب**، سيتم عرض تكاليف الشحن القابلة للتطبيق على البنود في بنود سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="b403c-133">If this property is set to **True**, the shipping charges that are applicable for line items will be shown on cart lines.</span></span> <span data-ttu-id="b403c-134">إذا تم تشغيل ميزة **تكاليف الشحن بدون تناسب** في مركز Commerce الرئيسي، فسيتم تطبيق تكاليف الشحن على مستوى الرأس وليس على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="b403c-134">If the **Header charge with no proration** feature is turned on in Commerce headquarters, the shipping charge will be applied at the header level, not the line level.</span></span> <span data-ttu-id="b403c-135">تمت إضافة هذه الميزة في الإصدار 10.0.13 من Commerce.</span><span class="sxs-lookup"><span data-stu-id="b403c-135">This feature was added in Commerce version 10.0.13.</span></span> |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="b403c-136">الوحدات التي يُمكن استخدامها في الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="b403c-136">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="b403c-137">**عنوان الشحن** - تتيح هذه الوحدة للعميل إضافة أو تحديد عنوان الشحن لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="b403c-137">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="b403c-138">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لعنوان الشحن‬](ship-address-module.md).</span><span class="sxs-lookup"><span data-stu-id="b403c-138">For more information about this module, see [Shipping address module](ship-address-module.md).</span></span>

    <span data-ttu-id="b403c-139">تعرض الصورة التالية مثالاُ عن وحدة عنوان الشحن في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-139">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![مثال عن وحدة عنوان الشحن](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="b403c-141">**خيارات التسليم** - تتيح هذه الوحدة للعميل تحديد وضع التسليم لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="b403c-141">**Delivery options** – This module lets a customer select a mode of delivery for an order.</span></span> <span data-ttu-id="b403c-142">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لخيارات التسليم‬](delivery-options-module.md).</span><span class="sxs-lookup"><span data-stu-id="b403c-142">For more information about this module, see [Delivery options module](delivery-options-module.md).</span></span>

    <span data-ttu-id="b403c-143">تعرض الصورة التالية مثالاُ عن وحدة خيارات التسليم في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-143">The following image shows an example of a delivery options module on a checkout page.</span></span>
 
    ![مثال عن وحدة خيارات التسليم](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="b403c-145">**حاوية قسم السداد مع الخروج** - تُمثل هذه حاوية يُمكنك وضع وحدات متعددة داخلها لإنشاء قسم داخل تدفق السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-145">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="b403c-146">على سبيل المثال، يُمكنك وضع كافة الوحدات المرتبطة بالدفع داخل هذه الحاوية لجعلها تظهر كقسم واحد.</span><span class="sxs-lookup"><span data-stu-id="b403c-146">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="b403c-147">تؤثر هذه الوحدة فقط على تخطيط التدفق.</span><span class="sxs-lookup"><span data-stu-id="b403c-147">This module affects only the layout of the flow.</span></span>

- <span data-ttu-id="b403c-148">**بطاقة الهدايا**- تتيح هذه الوحدة للعميل تسديد قيمة الأوامر باستخدام بطاقة هدايا.</span><span class="sxs-lookup"><span data-stu-id="b403c-148">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="b403c-149">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لبطاقة الهدايا‬](add-giftcard.md).</span><span class="sxs-lookup"><span data-stu-id="b403c-149">For more information about this module, see [Gift card module](add-giftcard.md).</span></span>

- <span data-ttu-id="b403c-150">**نقاط الولاء** - تسمح هذه الوحدة للعميل بدفع في مقابل أمر باستخدام نقاط الولاء.</span><span class="sxs-lookup"><span data-stu-id="b403c-150">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="b403c-151">وتوفر ملخصًا للنقاط المتاحة والنقاط منتهية الصلاحية، كما تتيح للعميل تحديد عدد النقاط المطلوب استردادها.</span><span class="sxs-lookup"><span data-stu-id="b403c-151">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="b403c-152">إذا لم يقم العميل بتسجيل الدخول أو إذا لم يكن عضوًا في برنامج الولاء، أو إذا كان المبلغ  الإجمالي في سلة التسوق هو 0 (صفر)، فمن ثم يتم إخفاء هذه الوحدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b403c-152">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>

- <span data-ttu-id="b403c-153">**الدفع** – تتيح هذه الوحدة للعميل تسديد قيمة الأوامر باستخدام بطاقة الائتمان أو بطاقة الخصم.</span><span class="sxs-lookup"><span data-stu-id="b403c-153">**Payment** – This module lets a customer pay for an order by using a credit or debit card.</span></span> <span data-ttu-id="b403c-154">كما يمكن للعملاء توفير عنوان فوترة لخيار الدفع الذي يقومون بتحديده.</span><span class="sxs-lookup"><span data-stu-id="b403c-154">Customers can also provide a billing address for the payment option that they select.</span></span> <span data-ttu-id="b403c-155">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية للدفع‬](payment-module.md).</span><span class="sxs-lookup"><span data-stu-id="b403c-155">For more information about this module, see [Payment module](payment-module.md).</span></span>

    <span data-ttu-id="b403c-156">تعرض الصورة التالية مثالاً عن وحدات بطاقة الهدايا ونقاط الولاء والدفع في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-156">The following image shows an example of gift card, loyalty points, and payment modules on a checkout page.</span></span>

    ![مثال عن وحدات بطاقة الهدايا ونقاط الولاء والدفع في صفحة السداد مع الخروج](./media/ecommerce-payments.PNG)

- <span data-ttu-id="b403c-158">**معلومات الاتصال**- تُتيح هذه الوحدة للعميل إضافة أو تغيير معلومات الاتصال (عنوان البريد الإلكتروني) لأحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="b403c-158">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="b403c-159">**كتلة النص** - تحتوي هذه الوحدة على أي مُراسلات يتم التحكم فيها بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="b403c-159">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="b403c-160">على سبيل المثال، قد تحتوي على رسالة تنص على، "للمشاكل الخاصة بطلبك، يُرجى الاتصال بالرقم التالي 1-800- شركة Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="b403c-160">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

- <span data-ttu-id="b403c-161">**بنود وشروط السداد مع الخروج** – تُظهر هذه الوحدة النمطية نصًا منسقًا يحتوي على البنود والشروط وخانة اختيار لإدخال العميل.</span><span class="sxs-lookup"><span data-stu-id="b403c-161">**Checkout terms and conditions** – This module shows rich text that contains the terms and conditions and a check box for the customer input.</span></span> <span data-ttu-id="b403c-162">تعتبر خانة الاختيار اختيارية وقابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="b403c-162">The check box is optional and configurable.</span></span> <span data-ttu-id="b403c-163">يتم التقاط الإدخال بواسطة الوحدة النمطية ويمكن استخدامه كشيك قبل تشغيل تسجيل الأمر، ولكنه غير مضمن في معلومات ملخص الأمر.</span><span class="sxs-lookup"><span data-stu-id="b403c-163">The input is captured by the module and can be used as a check before order placement is triggered, but it isn't included in the order summary information.</span></span> <span data-ttu-id="b403c-164">يمكن إضافة هذه الوحدة النمطية إلى حاوية السداد مع الخروج أو حاوية قسم السداد مع الخروج أو جزء البنود والشروط، وفقًا لاحتياجات العمل.</span><span class="sxs-lookup"><span data-stu-id="b403c-164">This module can be added to the checkout container, checkout section container, or terms and conditions slot, according to business needs.</span></span> <span data-ttu-id="b403c-165">إذا تمت إضافتها إلى حاوية السداد مع الخروج أو جزء حاوية قسم السداد مع الخروج، فستظهر كخطوة في عملية السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-165">If it's added to the checkout container or checkout section container slot, it will appear as a step in the checkout process.</span></span> <span data-ttu-id="b403c-166">إذا تمت إضافتها إلى جزء البنود والشروط، فستظهر بالقرب من زر تسجيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="b403c-166">If it's added to the terms and conditions slot, it will appear near the order placement button.</span></span>

    <span data-ttu-id="b403c-167">تعرض الصورة التالية مثالاً عن البنود والشروط في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="b403c-167">The following image shows an example of terms and conditions on a checkout page.</span></span>

    ![مثال على البنود والشروط في صفحة السداد مع الخروج](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b403c-169">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="b403c-169">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b403c-170">يتم تخزين معظم معلومات السداد مع الخروج، مثل عنوان الشحن وطريقة الشحن في سلة التسوق ومُعالجتها كجزء من الأمر.</span><span class="sxs-lookup"><span data-stu-id="b403c-170">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="b403c-171">والاستثناء الوحيد هو معلومات بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="b403c-171">The only exception is the credit card information.</span></span> <span data-ttu-id="b403c-172">تتم مُعالجة هذه المعلومات مُباشرة باستخدام موصل دفع Adyen.</span><span class="sxs-lookup"><span data-stu-id="b403c-172">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="b403c-173">يتم تخويل الدفع، ولكن لا يتم سحب المبلغ المطلوب حتى يتم استيفاء الأمر.</span><span class="sxs-lookup"><span data-stu-id="b403c-173">The payment is authorized, but it isn't charged until the order is fulfilled.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="b403c-174">إضافة وحدة سداد مع الخروج إلى صفحة وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b403c-174">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="b403c-175">لإضافة الوحدة النمطية للسداد مع الخروج إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b403c-175">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b403c-176">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="b403c-176">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b403c-177">في مربع الحوار **جزء جديد**، حدد وحدة **السداد مع الخروج‬**.</span><span class="sxs-lookup"><span data-stu-id="b403c-177">In the **New fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="b403c-178">ضمن **اسم الجزء**، أدخل الاسم **جزء السداد مع الخروج**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b403c-178">Under **Fragment name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="b403c-179">حدد فتحة **وحدة السداد مع الخروج**.</span><span class="sxs-lookup"><span data-stu-id="b403c-179">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="b403c-180">في جزء الخصائص على الجانب الأيسر، حدد رمز القلم الرصاص، وأدخل نص العنوان في الحقل، ثم حدد رمز علامة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="b403c-180">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="b403c-181">في فتحة **معلومات السداد مع الخروج**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="b403c-181">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b403c-182">في مربع الحوار **إضافة وحدة**، حدد وحدات **عنوان الشحن** و **خيارات التسليم**, **حاوية قسم السداد مع الخروج** و **معلومات الاتصال**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b403c-182">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="b403c-183">في وحدة **حاوية قسم السداد مع الخروج**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="b403c-183">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b403c-184">في مربع الحوار **إضافة وحدة**، حدد وحدات **بطاقة الهدايا** و **الولاء** و **الدفع**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b403c-184">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="b403c-185">وبهذه الطريقة، فسوف تتأكد من ظهور جميع أساليب الدفع في أحد الأقسام.</span><span class="sxs-lookup"><span data-stu-id="b403c-185">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="b403c-186">في جزء **البنود والشروط**، أضف الوحدة النمطية **بنود وشروط السداد مع الخروج‬‏‫** إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b403c-186">In the **Terms and conditions** slot, add a **Checkout terms and conditions** module if it's required.</span></span> <span data-ttu-id="b403c-187">في جزء خصائص الوحدة النمطية، قم بتكوين نص البنود والشروط كما هو مناسب.</span><span class="sxs-lookup"><span data-stu-id="b403c-187">In the module's properties pane, configure the terms and condition text as appropriate.</span></span>
1. <span data-ttu-id="b403c-188">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الجزء.</span><span class="sxs-lookup"><span data-stu-id="b403c-188">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="b403c-189">قد لا تُعرض في المعاينة بعض الوحدات التي ليس لديها سياق سلة تسوق.</span><span class="sxs-lookup"><span data-stu-id="b403c-189">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="b403c-190">حدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="b403c-190">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b403c-191">قم بإنشاء قالب يستخدم جزء السداد مع الخروج جديد.</span><span class="sxs-lookup"><span data-stu-id="b403c-191">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="b403c-192">قم بإنشاء صفحة السداد مع الخروج التي تستخدم القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="b403c-192">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b403c-193">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b403c-193">Additional resources</span></span>

[<span data-ttu-id="b403c-194">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="b403c-194">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b403c-195">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="b403c-195">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b403c-196">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="b403c-196">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b403c-197">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="b403c-197">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b403c-198">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="b403c-198">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b403c-199">الوحدة النمطية لمعلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="b403c-199">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b403c-200">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="b403c-200">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b403c-201">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="b403c-201">Gift card module</span></span>](add-giftcard.md)
