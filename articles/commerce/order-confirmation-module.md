---
title: الوحدة النمطية لتأكيد الأمر
description: يغطي هذا الموضوع الوحدات النمطية لتأكيد الأمر ويصف كيفية إستخدامها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 407fc2724d4b589ef5f611974f9358e879dba7ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257137"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="e7110-103">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="e7110-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7110-104">يغطي هذا الموضوع الوحدات النمطية لتأكيد الأمر ويصف كيفية إستخدامها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7110-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e7110-105">تُستخدم وحدة تأكيد الأمر لإظهار تفاصيل تأكيد الأمر بعد إنشاء أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="e7110-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="e7110-106">ويعرض معرف تأكيد الأمر ومعلومات جهة الاتصال الخاصة بالأمر وتفاصيل الأمر الأخرى، مثل الأصناف التي تم شراؤها وخيارات الالتقاط وطريقة الشحن.</span><span class="sxs-lookup"><span data-stu-id="e7110-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="e7110-107">خصائص الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="e7110-107">Order confirmation module properties</span></span>

| <span data-ttu-id="e7110-108">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="e7110-108">Property name</span></span>  | <span data-ttu-id="e7110-109">القيم</span><span class="sxs-lookup"><span data-stu-id="e7110-109">Values</span></span> | <span data-ttu-id="e7110-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e7110-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e7110-111">العنوان</span><span class="sxs-lookup"><span data-stu-id="e7110-111">Heading</span></span>        | <span data-ttu-id="e7110-112">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="e7110-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e7110-113">يمكن أن تحتوي الوحدة النمطية تأكيد الأمر على عنوان.</span><span class="sxs-lookup"><span data-stu-id="e7110-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="e7110-114">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="e7110-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e7110-115">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="e7110-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e7110-116">رقم الاتصال</span><span class="sxs-lookup"><span data-stu-id="e7110-116">Contact number</span></span> | <span data-ttu-id="e7110-117">النص</span><span class="sxs-lookup"><span data-stu-id="e7110-117">Text</span></span> | <span data-ttu-id="e7110-118">يمكن توفير رقم جهة الاتصال للاسئله المتعلقة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="e7110-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="e7110-119">إظهار معلومات الفترة الزمنية للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="e7110-119">Show pickup timeslot information</span></span> | <span data-ttu-id="e7110-120">صحيح أو خطأ</span><span class="sxs-lookup"><span data-stu-id="e7110-120">True or False</span></span> | <span data-ttu-id="e7110-121">تتوفر هذه الخاصية في Dynamics 365 Commerce 10.0.15 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="e7110-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="e7110-122">عندما تكون القيمة true، فإنه يعرض معلومات الفترة الزمنية للالتقاط إذا كانت متوفرة لالتقاط أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="e7110-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="e7110-123">يمكن استخدام الوحدات النمطية على صفحة تأكيد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="e7110-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="e7110-124">عند إنشاء صفحة تأكيد الأمر، يمكنك إضافة وحدات نمطية أخرى ذات صلة بالإضافة إلى الوحدة النمطية لتأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="e7110-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="e7110-125">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="e7110-125">Here are some examples:</span></span>

- <span data-ttu-id="e7110-126">**الوحدة النمطية للتوصيات** – يمكن إضافة الوحدة النمطية للتوصيات إلى صفحة تأكيد الأوامر لاقتراح منتجات أخرى للعميل.</span><span class="sxs-lookup"><span data-stu-id="e7110-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="e7110-127">**الوحدات النمطية للتسويق** يمكن إضافة أي وحدة نمطية للتسويق إلى صفحة تأكيد الأمر لإظهار محتوي التسويق.</span><span class="sxs-lookup"><span data-stu-id="e7110-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="e7110-128">إضافة الوحدة النمطية لتأكيد الأمر إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="e7110-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="e7110-129">لإضافة الوحدة النمطية لتأكيد الأمر إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e7110-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e7110-130">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="e7110-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e7110-131">في مربع الحوار **قالب جديد** تحت **اسم القالب**، أدخل الاسم **قالب تأكيد الأمر**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e7110-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="e7110-132">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="e7110-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7110-133">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e7110-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e7110-134">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="e7110-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7110-135">في مربع الحوار **إضافة وحدة** حدد الوحدة النمطية ‬‏‫**تأكيد الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e7110-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e7110-136">حدد **حفظ**، ثم حدد **معاينة** لمعاينة القالب.</span><span class="sxs-lookup"><span data-stu-id="e7110-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="e7110-137">لا ينبغي عرض الوحدة النمطية لتأكيد الأمر، لأنها تتطلب سياق رقم تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="e7110-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="e7110-138">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="e7110-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e7110-139">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="e7110-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="e7110-140">في مربع الحوار **اختيار قالب** حدد **قالب تأكيد الأمر**.</span><span class="sxs-lookup"><span data-stu-id="e7110-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="e7110-141">ضمن **اسم الصفحة**، أدخل **صفحة تأكيد الأمر** ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="e7110-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="e7110-142">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="e7110-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7110-143">في مربع الحوار **إضافة وحدة** حدد الوحدة النمطية ‬‏‫**تأكيد الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e7110-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e7110-144">في جزء الخصائص لتأكيد الأمر، حدد **العنوان** بجوار رمز القلم.</span><span class="sxs-lookup"><span data-stu-id="e7110-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="e7110-145">في حقل **نص العنوان** لمربع الحوار **العنوان** أدخل نص العنوان **تأكيد الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e7110-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="e7110-146">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e7110-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e7110-147">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="e7110-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7110-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e7110-148">Additional resources</span></span>

[<span data-ttu-id="e7110-149">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="e7110-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e7110-150">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="e7110-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e7110-151">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="e7110-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e7110-152">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="e7110-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e7110-153">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="e7110-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e7110-154">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="e7110-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e7110-155">الوحدة النمطية لمعلومات الالتقاط</span><span class="sxs-lookup"><span data-stu-id="e7110-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="e7110-156">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="e7110-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]