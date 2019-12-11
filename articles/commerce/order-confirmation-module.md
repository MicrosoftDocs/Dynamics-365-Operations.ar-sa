---
title: الوحدة النمطية لتأكيد الأمر
description: يغطي هذا الموضوع الوحدات النمطية لتأكيد الأمر ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698316"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="bed44-103">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="bed44-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bed44-104">يغطي هذا الموضوع الوحدات النمطية لتأكيد الأمر ويصف كيفية إنشائها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bed44-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bed44-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="bed44-105">Overview</span></span>

<span data-ttu-id="bed44-106">تُستخدم الوحدة النمطية لتاكيد الأمر لعرض رسالة تأكيد في صفحه تأكيد الأمر بعد إصدار أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="bed44-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="bed44-107">تعرض الوحدة النمطية لتأكيد الأمر رقم تأكيد الأمر وعنوان البريد الإلكتروني للعميل الذي تم توفيره أثناء السحب.</span><span class="sxs-lookup"><span data-stu-id="bed44-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="bed44-108">عند وضع أمر أثناء السحب، يتم تمرير رقم تأكيد الأمر وعنوان البريد الكتروني للعميل إلى صفحة تأكيد الأمر كسلسلة استعلام في عنوان URL الخاص بالصفحة.</span><span class="sxs-lookup"><span data-stu-id="bed44-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="bed44-109">تتلقي الوحدة النمطية لتأكيد الأمر هذه المعلومات وتعرض حالة الأمر على صفحة تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="bed44-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="bed44-110">تتطلب الوحدة النمطية لتأكيد الأمر سياق هذه الصفحة لتوفير حاله الأمر.</span><span class="sxs-lookup"><span data-stu-id="bed44-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="bed44-111">خصائص الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="bed44-111">Order confirmation module properties</span></span>

| <span data-ttu-id="bed44-112">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="bed44-112">Property name</span></span> | <span data-ttu-id="bed44-113">القيم</span><span class="sxs-lookup"><span data-stu-id="bed44-113">Values</span></span> | <span data-ttu-id="bed44-114">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="bed44-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bed44-115">العنوان</span><span class="sxs-lookup"><span data-stu-id="bed44-115">Heading</span></span>       | <span data-ttu-id="bed44-116">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="bed44-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="bed44-117">يمكن أن تحتوي الوحدة النمطية تأكيد الأمر على عنوان.</span><span class="sxs-lookup"><span data-stu-id="bed44-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="bed44-118">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="bed44-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="bed44-119">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="bed44-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="bed44-120">الوحدات النمطية التي يمكن استخدامها في الوحدة النمطية لصفحة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="bed44-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="bed44-121">**التوصيات** – يمكن وضع الوحدة النمطية الخاصة بالتوصيات في صفحة تأكيد الأمر لاقتراح منتجات أخرى للعميل.</span><span class="sxs-lookup"><span data-stu-id="bed44-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="bed44-122">**التسويق** – يمكن للوحدة النمطية للتسويق إضافة محتوى تسويقي إلى صفحة تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="bed44-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="bed44-123">إنشاء وحدة نمطية لصفحة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="bed44-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="bed44-124">قم إنشاء قالب صفحة يُسمى **قالب تأكيد الأمر**.</span><span class="sxs-lookup"><span data-stu-id="bed44-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="bed44-125">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة وحدة نمطية لتأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="bed44-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="bed44-126">في الوحدة النمطية لتأكيد الأمر، أضف وحدة نمطية للتوصيات.</span><span class="sxs-lookup"><span data-stu-id="bed44-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="bed44-127">احفظ القالب وقم بمعاينته.</span><span class="sxs-lookup"><span data-stu-id="bed44-127">Save and preview the template.</span></span> <span data-ttu-id="bed44-128">لا ينبغي عرض الوحدة النمطية لتأكيد الأمر، لأنها تتطلب سياق رقم تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="bed44-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="bed44-129">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="bed44-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="bed44-130">استخدم قالب تأكيد الأمر الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة تأكيد الأمر**.</span><span class="sxs-lookup"><span data-stu-id="bed44-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="bed44-131">أضف الصفحة الافتراضية إلى المخطط التفصيلي للصفحة.</span><span class="sxs-lookup"><span data-stu-id="bed44-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="bed44-132">في فتحة **الرأس**، أضف جزء الرأس.</span><span class="sxs-lookup"><span data-stu-id="bed44-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="bed44-133">في فتحة **التذييل**، أضف جزء التذييل.</span><span class="sxs-lookup"><span data-stu-id="bed44-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="bed44-134">في الفتحة **الرئيسية**، أضف وحدة نمطية لتأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="bed44-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="bed44-135">في جزء الخصائص الخاص بالوحدة النمطية لتأكيد الأمر، أضف العنوان **تأكيد الأمر**.</span><span class="sxs-lookup"><span data-stu-id="bed44-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="bed44-136">أسفل الوحدة النمطية لتأكيد الأمر، أضف وحدة نمطية لأحدي التوصيات، وقم بتكوينها لكي تستخدم إعدادات **جديد** و **الأفضل مبيعًا‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="bed44-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="bed44-137">احفظ الصفحة وقم بمعاينتها، وقم بإيداعها ونشرها.</span><span class="sxs-lookup"><span data-stu-id="bed44-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bed44-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bed44-138">Additional resources</span></span>

[<span data-ttu-id="bed44-139">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="bed44-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bed44-140">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="bed44-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bed44-141">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="bed44-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bed44-142">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="bed44-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bed44-143">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="bed44-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bed44-144">وحدة نمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="bed44-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bed44-145">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="bed44-145">Footer module</span></span>](author-footer-module.md)
