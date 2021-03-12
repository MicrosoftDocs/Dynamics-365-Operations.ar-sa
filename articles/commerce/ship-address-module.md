---
title: الوحدة النمطية لعنوان الشحن
description: يتناول هذا الموضوع الوحدة النمطية لعنوان الشحن ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985626"
---
# <a name="shipping-address-module"></a><span data-ttu-id="791a6-103">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="791a6-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="791a6-104">يصف هذا الموضوع الوحدة النمطية لعنوان الشحن ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="791a6-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="791a6-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="791a6-105">Overview</span></span>

<span data-ttu-id="791a6-106">تسمح الوحدة النمطية لعنوان الشحن للعملاء بإضافة أو تحديد عنوان الشحن لأحد الأوامر أثناء سير مهام السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="791a6-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="791a6-107">إذا قام العميل بتسجيل الدخول، فسوف يتم عرض أي عناوين تم حفظها في وقت سابق لهذا العميل، ويمكن للعميل الاختيار من بينها.</span><span class="sxs-lookup"><span data-stu-id="791a6-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="791a6-108">ويُمكن للعميل أيضًا إضافة عنوان جديد.</span><span class="sxs-lookup"><span data-stu-id="791a6-108">The customer can also add a new address.</span></span> <span data-ttu-id="791a6-109">يتم استخدام الوحدة النمطية لعنوان الشحن لكافة الأصناف في الأمر التي تتطلب الشحن.</span><span class="sxs-lookup"><span data-stu-id="791a6-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="791a6-110">يمكن تحديد تنسيقات عناوين الشحن في مركز Commerce الرئيسي لكل بلد أو منطقة، وعندئذ تقوم الوحدة النمطية لعنوان الشحن بفرض القواعد الخاصة بالبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="791a6-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="791a6-111">عندما يقوم العملاء بإدخال عنوان شحن أثناء سير مهام السداد مع الخروج، يمكنهم حفظ العنوان كعنوان رئيسي.</span><span class="sxs-lookup"><span data-stu-id="791a6-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="791a6-112">يظهر هذا الخيار فقط إذا سجل العميل دخوله.</span><span class="sxs-lookup"><span data-stu-id="791a6-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="791a6-113">وعلى الرغم من أن الوحدة النمطية لعنوان الشحن لا توفر ميزة التحقق من صحة العنوان، إلا أنه يُمكن تطبيق هذه الميزة من خلال التخصيص.</span><span class="sxs-lookup"><span data-stu-id="791a6-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="791a6-114">يبين الشكل التوضيحي التالي مثالاُ عن وحدة عنوان شحن جديدة في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="791a6-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![مثال عن الوحدة النمطية لعنوان الشحن على صفحة السداد مع الخروج](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="791a6-116">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="791a6-116">Module properties</span></span>

| <span data-ttu-id="791a6-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="791a6-117">Property name</span></span> | <span data-ttu-id="791a6-118">القيم</span><span class="sxs-lookup"><span data-stu-id="791a6-118">Values</span></span> | <span data-ttu-id="791a6-119">الوصف</span><span class="sxs-lookup"><span data-stu-id="791a6-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="791a6-120">العنوان</span><span class="sxs-lookup"><span data-stu-id="791a6-120">Heading</span></span> | <span data-ttu-id="791a6-121">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="791a6-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="791a6-122">عنوان اختياري للوحدة النمطية لعنوان الشحن.</span><span class="sxs-lookup"><span data-stu-id="791a6-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="791a6-123">إظهار نوع العنوان</span><span class="sxs-lookup"><span data-stu-id="791a6-123">Show address type</span></span> | <span data-ttu-id="791a6-124">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="791a6-124">**True** or **False**</span></span> | <span data-ttu-id="791a6-125">إذا تم تعيين هذه الخاصية الاختيارية إلى **صواب**، فسيظهر نوع عنوان مثل **المنزل** أو **العمل**.</span><span class="sxs-lookup"><span data-stu-id="791a6-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="791a6-126">إذا لم يتم تحديد نوع عنوان، سيتم حفظ العنوان تلقائيًا **النوع**=**غير ذلك**.</span><span class="sxs-lookup"><span data-stu-id="791a6-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="791a6-127">إضافة الوحدة النمطية لعنوان الشحن إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة</span><span class="sxs-lookup"><span data-stu-id="791a6-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="791a6-128">يمكن إضافة وحدة نمطية لعنوان الشحن فقط إلى وحدة نمطية للسداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="791a6-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="791a6-129">لمزيد من المعلومات حول كيفية تكوين الوحدة النمطية لعنوان الشحن وإضافتها إلى صفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="791a6-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="791a6-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="791a6-130">Additional resources</span></span>

[<span data-ttu-id="791a6-131">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="791a6-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="791a6-132">الوحدة النمطية لرمز عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="791a6-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="791a6-133">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="791a6-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="791a6-134">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="791a6-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="791a6-135">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="791a6-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="791a6-136">وحده معلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="791a6-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="791a6-137">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="791a6-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="791a6-138">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="791a6-138">Gift card module</span></span>](add-giftcard.md)
