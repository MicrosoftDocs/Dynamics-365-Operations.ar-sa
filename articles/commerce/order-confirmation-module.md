---
title: وحدة تفاصيل الأوامر
description: يغطي هذا الموضوع وحدات تفاصيل الأوامر ويصف كيفية استخدامها في Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015170"
---
# <a name="order-details-module"></a><span data-ttu-id="89da9-103">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="89da9-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89da9-104">يغطي هذا الموضوع وحدات تفاصيل الأوامر ويصف كيفية استخدامها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="89da9-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="89da9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="89da9-105">Overview</span></span>

<span data-ttu-id="89da9-106">يتم استخدام وحدة تفاصيل الأوامر لإظهار تفاصيل تأكيد الأوامر بعد تقديم أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="89da9-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="89da9-107">ويعرض معرف تاكيد الأمر ومعلومات الاتصال بالطلب وتفاصيل الطلبات الأخرى، مثل الأصناف التي تم شراؤها ومعلومات الدفع وطريقه الشحن.</span><span class="sxs-lookup"><span data-stu-id="89da9-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="89da9-108">خصائص الوحدة النمطية لتفاصيل الأمر</span><span class="sxs-lookup"><span data-stu-id="89da9-108">Order details module properties</span></span>

| <span data-ttu-id="89da9-109">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="89da9-109">Property name</span></span>  | <span data-ttu-id="89da9-110">القيم</span><span class="sxs-lookup"><span data-stu-id="89da9-110">Values</span></span> | <span data-ttu-id="89da9-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="89da9-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="89da9-112">العنوان</span><span class="sxs-lookup"><span data-stu-id="89da9-112">Heading</span></span>        | <span data-ttu-id="89da9-113">نص العنوان وعلامة العنوان ( **H1** , **H2** , **H3** , **H4** , **H5** , أو **H6** )</span><span class="sxs-lookup"><span data-stu-id="89da9-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="89da9-114">يمكن أن تحتوي الوحدة النمطية لتفاصيل الأمر على عنوان.</span><span class="sxs-lookup"><span data-stu-id="89da9-114">The order details module can have a heading.</span></span> <span data-ttu-id="89da9-115">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="89da9-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="89da9-116">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="89da9-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="89da9-117">رقم الاتصال</span><span class="sxs-lookup"><span data-stu-id="89da9-117">Contact number</span></span> | <span data-ttu-id="89da9-118">النص</span><span class="sxs-lookup"><span data-stu-id="89da9-118">Text</span></span> | <span data-ttu-id="89da9-119">يمكن توفير رقم جهة الاتصال للاسئله المتعلقة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="89da9-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="89da9-120">يمكن استخدام الوحدات على صفحة تفاصيل الأوامر.</span><span class="sxs-lookup"><span data-stu-id="89da9-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="89da9-121">عند إنشاء صفحه تفاصيل أمر، يمكنك أضافه وحدات نمطيه أخرى ذات صله بالاضافه إلى الوحدة النمطية لتفاصيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="89da9-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="89da9-122">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="89da9-122">Here are some examples:</span></span>

- <span data-ttu-id="89da9-123">**وحدة التوصيات** – يمكن إضافة وحدة التوصيات إلى صفحة تفاصيل الأوامر لاقتراح منتجات أخرى للعميل.</span><span class="sxs-lookup"><span data-stu-id="89da9-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="89da9-124">**وحدات التسويق** يمكن أضافه إيه وحده نمطيه للتسويق إلى صفحه تفاصيل الأمر لإظهار محتويات التسويق.</span><span class="sxs-lookup"><span data-stu-id="89da9-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="89da9-125">إضافة وحدة نمطية لتفاصيل الأمر إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="89da9-125">Add an order details module to a page</span></span>

<span data-ttu-id="89da9-126">لإضافة الوحدة النمطية لتفاصيل الأمر إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="89da9-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="89da9-127">انتقل إلى **القوالب** ، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="89da9-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="89da9-128">في مربع الحوار **قالب جديد** تحت **اسم القالب** ، أدخل الاسم **قالب تفاصيل الأمر** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="89da9-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="89da9-129">في فتحة **النص الأساسي‬‬‏‫** ، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="89da9-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="89da9-130">في مربع الحوار **إضافة وحدة** ، حدد وحدة **الصفحة الافتراضية‬** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="89da9-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="89da9-131">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية** ، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="89da9-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="89da9-132">في مربع الحوار **إضافة وحدة** حدد وحدة ‬‏‫ **تفاصيل الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="89da9-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="89da9-133">حدد **حفظ** ، ثم حدد **معاينة** لمعاينة القالب.</span><span class="sxs-lookup"><span data-stu-id="89da9-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="89da9-134">لن يتم عرض وحدة تفاصيل الأوامر، لأنها تتطلب سياق رقم تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="89da9-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="89da9-135">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="89da9-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="89da9-136">انتقل إلى **الصفحات** ، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="89da9-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="89da9-137">في مربع الحوار **اختيار قالب** حدد **قالب تفاصيل الأمر**.</span><span class="sxs-lookup"><span data-stu-id="89da9-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="89da9-138">ضمن **اسم الصفحة** ، أدخل **صفحة تفاصيل الأمر** ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="89da9-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="89da9-139">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية** ، حدد علامة القطع ( **...** )، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="89da9-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="89da9-140">في مربع الحوار **إضافة وحدة** حدد وحدة ‬‏‫ **تفاصيل الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="89da9-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="89da9-141">في جزء الخصائص لتفاصيل الأمر، حدد **العنوان** بجوار رمز القلم الرصاص.</span><span class="sxs-lookup"><span data-stu-id="89da9-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="89da9-142">في حقل **نص العنوان** لمربع الحوار **العنوان** أدخل نص العنوان **تفاصيل الأمر** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="89da9-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="89da9-143">حدد **حفظ** ، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="89da9-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="89da9-144">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="89da9-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89da9-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="89da9-145">Additional resources</span></span>

[<span data-ttu-id="89da9-146">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="89da9-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="89da9-147">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="89da9-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="89da9-148">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="89da9-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="89da9-149">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="89da9-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="89da9-150">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="89da9-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="89da9-151">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="89da9-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="89da9-152">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="89da9-152">Gift card module</span></span>](add-giftcard.md)
