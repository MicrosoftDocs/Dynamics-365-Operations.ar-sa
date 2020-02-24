---
title: وحدة تفاصيل الأوامر
description: يغطي هذا الموضوع وحدات تفاصيل الأوامر ويصف كيفية استخدامها في Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026007"
---
# <a name="order-details-module"></a><span data-ttu-id="cb20b-103">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="cb20b-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb20b-104">يغطي هذا الموضوع وحدات تفاصيل الأوامر ويصف كيفية استخدامها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb20b-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb20b-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="cb20b-105">Overview</span></span>

<span data-ttu-id="cb20b-106">يتم استخدام وحدة تفاصيل الأوامر لإظهار تفاصيل تأكيد الأوامر بعد تقديم أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="cb20b-107">ويعرض معرف تاكيد الأمر ومعلومات الاتصال بالطلب وتفاصيل الطلبات الأخرى ، مثل الأصناف التي تم شراؤها ومعلومات الدفع وطريقه الشحن.</span><span class="sxs-lookup"><span data-stu-id="cb20b-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="cb20b-108">خصائص الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="cb20b-108">Order confirmation module properties</span></span>

| <span data-ttu-id="cb20b-109">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="cb20b-109">Property name</span></span>  | <span data-ttu-id="cb20b-110">القيم</span><span class="sxs-lookup"><span data-stu-id="cb20b-110">Values</span></span> | <span data-ttu-id="cb20b-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cb20b-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="cb20b-112">العنوان</span><span class="sxs-lookup"><span data-stu-id="cb20b-112">Heading</span></span>        | <span data-ttu-id="cb20b-113">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="cb20b-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="cb20b-114">يمكن أن تحتوي الوحدة النمطية تأكيد الأمر على عنوان.</span><span class="sxs-lookup"><span data-stu-id="cb20b-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="cb20b-115">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="cb20b-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="cb20b-116">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="cb20b-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="cb20b-117">رقم الاتصال</span><span class="sxs-lookup"><span data-stu-id="cb20b-117">Contact number</span></span> | <span data-ttu-id="cb20b-118">النص</span><span class="sxs-lookup"><span data-stu-id="cb20b-118">Text</span></span> | <span data-ttu-id="cb20b-119">يمكن توفير رقم جهة الاتصال للاسئله المتعلقة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="cb20b-120">يمكن استخدام الوحدات على صفحة تفاصيل الأوامر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="cb20b-121">عند إنشاء صفحه تفاصيل أمر ، يمكنك أضافه وحدات نمطيه أخرى ذات صله بالاضافه إلى الوحدة النمطية لتفاصيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="cb20b-122">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="cb20b-122">Here are some examples:</span></span>

- <span data-ttu-id="cb20b-123">**وحدة التوصيات** – يمكن إضافة وحدة التوصيات إلى صفحة تفاصيل الأوامر لاقتراح منتجات أخرى للعميل.</span><span class="sxs-lookup"><span data-stu-id="cb20b-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="cb20b-124">**وحدات التسويق** يمكن أضافه إيه وحده نمطيه للتسويق إلى صفحه تفاصيل الأمر لإظهار محتويات التسويق.</span><span class="sxs-lookup"><span data-stu-id="cb20b-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="cb20b-125">إنشاء وحدة صفحة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="cb20b-125">Create an order details page module</span></span>

1. <span data-ttu-id="cb20b-126">قم بإنشاء قالب صفحة يُسمى **قالب تفاصيل الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="cb20b-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="cb20b-127">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة وحدة تفاصيل أوامر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="cb20b-128">في وحدة تفاصيل الأوامر، أضف وحدة توصيات.</span><span class="sxs-lookup"><span data-stu-id="cb20b-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="cb20b-129">احفظ القالب وقم بمعاينته.</span><span class="sxs-lookup"><span data-stu-id="cb20b-129">Save and preview the template.</span></span> <span data-ttu-id="cb20b-130">لن يتم عرض وحدة تفاصيل الأوامر، لأنها تتطلب سياق رقم تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="cb20b-131">انشر القالب بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="cb20b-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="cb20b-132">استخدم قالب تفاصيل الأوامر الذي قمت بإنشائه للتو لإنشاء صفحة تُسمى **صفحة تفاصيل الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="cb20b-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="cb20b-133">أضف الصفحة الافتراضية إلى المخطط التفصيلي للصفحة.</span><span class="sxs-lookup"><span data-stu-id="cb20b-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="cb20b-134">في فتحة **الرأس**، أضف جزء الرأس.</span><span class="sxs-lookup"><span data-stu-id="cb20b-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="cb20b-135">في فتحة **التذييل**، أضف جزء التذييل.</span><span class="sxs-lookup"><span data-stu-id="cb20b-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="cb20b-136">في الفتحة **الرئيسية**، أضف وحدة تفاصيل أمر.</span><span class="sxs-lookup"><span data-stu-id="cb20b-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="cb20b-137">في جزء الخصائص لوحدة تفاصيل الأوام، أضف العنوان **تفاصيل الأمر**.</span><span class="sxs-lookup"><span data-stu-id="cb20b-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="cb20b-138">أسفل وحدة تفاصيل الأمر، أضف وحدة نمطية لأحدي التوصيات، وقم بتكوينها لكي تستخدم إعدادات **جديد** و **الأفضل مبيعًا‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="cb20b-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="cb20b-139">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="cb20b-139">Save and preview the page.</span></span>
1. <span data-ttu-id="cb20b-140">انشر الصفحة بعد الانتهاء من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="cb20b-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb20b-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb20b-141">Additional resources</span></span>

[<span data-ttu-id="cb20b-142">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="cb20b-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cb20b-143">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="cb20b-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="cb20b-144">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="cb20b-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cb20b-145">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="cb20b-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cb20b-146">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="cb20b-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cb20b-147">وحدة نمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="cb20b-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="cb20b-148">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="cb20b-148">Footer module</span></span>](author-footer-module.md)
