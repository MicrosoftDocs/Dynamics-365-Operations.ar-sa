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
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972723"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="cb903-103">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="cb903-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb903-104">يغطي هذا الموضوع الوحدات النمطية لتأكيد الأمر ويصف كيفية إستخدامها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb903-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb903-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="cb903-105">Overview</span></span>

<span data-ttu-id="cb903-106">تُستخدم وحدة تأكيد الأمر لإظهار تفاصيل تأكيد الأمر بعد إنشاء أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="cb903-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="cb903-107">ويعرض معرف تأكيد الأمر ومعلومات جهة الاتصال الخاصة بالأمر وتفاصيل الأمر الأخرى، مثل الأصناف التي تم شراؤها وخيارات الالتقاط وطريقة الشحن.</span><span class="sxs-lookup"><span data-stu-id="cb903-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="cb903-108">خصائص الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="cb903-108">Order confirmation module properties</span></span>

| <span data-ttu-id="cb903-109">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="cb903-109">Property name</span></span>  | <span data-ttu-id="cb903-110">القيم</span><span class="sxs-lookup"><span data-stu-id="cb903-110">Values</span></span> | <span data-ttu-id="cb903-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cb903-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="cb903-112">العنوان</span><span class="sxs-lookup"><span data-stu-id="cb903-112">Heading</span></span>        | <span data-ttu-id="cb903-113">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="cb903-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="cb903-114">يمكن أن تحتوي الوحدة النمطية تأكيد الأمر على عنوان.</span><span class="sxs-lookup"><span data-stu-id="cb903-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="cb903-115">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="cb903-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="cb903-116">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="cb903-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="cb903-117">رقم الاتصال</span><span class="sxs-lookup"><span data-stu-id="cb903-117">Contact number</span></span> | <span data-ttu-id="cb903-118">النص</span><span class="sxs-lookup"><span data-stu-id="cb903-118">Text</span></span> | <span data-ttu-id="cb903-119">يمكن توفير رقم جهة الاتصال للاسئله المتعلقة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="cb903-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="cb903-120">إظهار معلومات الفترة الزمنية للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="cb903-120">Show pickup timeslot information</span></span> | <span data-ttu-id="cb903-121">صحيح أو خطأ</span><span class="sxs-lookup"><span data-stu-id="cb903-121">True or False</span></span> | <span data-ttu-id="cb903-122">تتوفر هذه الخاصية في Dynamics 365 Commerce 10.0.15 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="cb903-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="cb903-123">عندما تكون القيمة true، فإنه يعرض معلومات الفترة الزمنية للالتقاط إذا كانت متوفرة لالتقاط أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="cb903-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="cb903-124">يمكن استخدام الوحدات النمطية على صفحة تأكيد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="cb903-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="cb903-125">عند إنشاء صفحة تأكيد الأمر، يمكنك إضافة وحدات نمطية أخرى ذات صلة بالإضافة إلى الوحدة النمطية لتأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="cb903-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="cb903-126">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="cb903-126">Here are some examples:</span></span>

- <span data-ttu-id="cb903-127">**الوحدة النمطية للتوصيات** – يمكن إضافة الوحدة النمطية للتوصيات إلى صفحة تأكيد الأوامر لاقتراح منتجات أخرى للعميل.</span><span class="sxs-lookup"><span data-stu-id="cb903-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="cb903-128">**الوحدات النمطية للتسويق** يمكن إضافة أي وحدة نمطية للتسويق إلى صفحة تأكيد الأمر لإظهار محتوي التسويق.</span><span class="sxs-lookup"><span data-stu-id="cb903-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="cb903-129">إضافة الوحدة النمطية لتأكيد الأمر إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="cb903-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="cb903-130">لإضافة الوحدة النمطية لتأكيد الأمر إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cb903-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cb903-131">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="cb903-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="cb903-132">في مربع الحوار **قالب جديد** تحت **اسم القالب**، أدخل الاسم **قالب تأكيد الأمر**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb903-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="cb903-133">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="cb903-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb903-134">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb903-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cb903-135">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="cb903-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb903-136">في مربع الحوار **إضافة وحدة** حدد الوحدة النمطية ‬‏‫**تأكيد الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb903-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cb903-137">حدد **حفظ**، ثم حدد **معاينة** لمعاينة القالب.</span><span class="sxs-lookup"><span data-stu-id="cb903-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="cb903-138">لا ينبغي عرض الوحدة النمطية لتأكيد الأمر، لأنها تتطلب سياق رقم تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="cb903-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="cb903-139">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="cb903-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="cb903-140">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="cb903-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="cb903-141">في مربع الحوار **اختيار قالب** حدد **قالب تأكيد الأمر**.</span><span class="sxs-lookup"><span data-stu-id="cb903-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="cb903-142">ضمن **اسم الصفحة**، أدخل **صفحة تأكيد الأمر** ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="cb903-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="cb903-143">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="cb903-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb903-144">في مربع الحوار **إضافة وحدة** حدد الوحدة النمطية ‬‏‫**تأكيد الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb903-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cb903-145">في جزء الخصائص لتأكيد الأمر، حدد **العنوان** بجوار رمز القلم.</span><span class="sxs-lookup"><span data-stu-id="cb903-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="cb903-146">في حقل **نص العنوان** لمربع الحوار **العنوان** أدخل نص العنوان **تأكيد الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb903-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="cb903-147">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cb903-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="cb903-148">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="cb903-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb903-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb903-149">Additional resources</span></span>

[<span data-ttu-id="cb903-150">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="cb903-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cb903-151">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="cb903-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="cb903-152">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="cb903-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cb903-153">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="cb903-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="cb903-154">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="cb903-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="cb903-155">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="cb903-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="cb903-156">الوحدة النمطية لمعلومات الالتقاط</span><span class="sxs-lookup"><span data-stu-id="cb903-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="cb903-157">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="cb903-157">Gift card module</span></span>](add-giftcard.md)
