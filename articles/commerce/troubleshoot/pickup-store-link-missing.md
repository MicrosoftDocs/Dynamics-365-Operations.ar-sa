---
title: لا يظهر خيار الانتقاء في صفحات سلة التسوق أو تفاصيل المنتج
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خيار التقاط في المتجر على صفحة سلة التسوق أو تفاصيل المنتج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46eeed18bb547035603d7e9a01e8f131a2393f01
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801617"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="cde90-103">لا يظهر خيار "انتقاء هذا" في صفحات سلة التسوق أو تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="cde90-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cde90-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خيار التقاط في المتجر على صفحة سلة التسوق أو تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="cde90-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="cde90-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="cde90-105">Description</span></span>

<span data-ttu-id="cde90-106">لا يظهر زر **انتقاء هذا** في صفحة سلة التسوق أو صفحات تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="cde90-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="cde90-107">يبين الرسم التوضيحي التالي مثالا للصفحة التي تتضمن زر **انتقاء هذا**.</span><span class="sxs-lookup"><span data-stu-id="cde90-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![زر انتهاء هذا](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="cde90-109">الدقة</span><span class="sxs-lookup"><span data-stu-id="cde90-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="cde90-110">تمكين ملحق BOPIS في منشئ مواقع Commerce</span><span class="sxs-lookup"><span data-stu-id="cde90-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="cde90-111">لتمكين ملحق "الشراء عبر الإنترنت، الانتقاء في المتجر" (BOPIS) في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cde90-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cde90-112">حدد موقعك.</span><span class="sxs-lookup"><span data-stu-id="cde90-112">Select your site.</span></span>
1. <span data-ttu-id="cde90-113">حدد **إعدادات الموقع**، ثم حدد **الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="cde90-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="cde90-114">تاكد من أنه تم مسح خيار **تعطيل BOPIS**.</span><span class="sxs-lookup"><span data-stu-id="cde90-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="cde90-115">تكوين أوضاع التسليم في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="cde90-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="cde90-116">لتكوين أوضاع التسليم في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cde90-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cde90-117">انتقل إلى **‏‫التدبير والتوريد‬ \> الإعداد \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="cde90-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="cde90-118">تأكد من أنه تم إنشاء وضع **الالتقاط للعميل**، وأنه تعيين المنتجات والعناوين إليه.</span><span class="sxs-lookup"><span data-stu-id="cde90-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="cde90-119">انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="cde90-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="cde90-120">في جزء التنقل الأيسر، حدد **أوامر العملاء**.</span><span class="sxs-lookup"><span data-stu-id="cde90-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="cde90-121">تأكد من تكوين **وضع انتقاء التسليم** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="cde90-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="cde90-122">تكوين مدفوعات أوامر العميل</span><span class="sxs-lookup"><span data-stu-id="cde90-122">Configure customer orders payments</span></span>

<span data-ttu-id="cde90-123">لتكوين مدفوعات أوامر العميل في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cde90-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cde90-124">انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="cde90-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="cde90-125">في جزء التنقل الأيسر، حدد **أوامر العملاء**.</span><span class="sxs-lookup"><span data-stu-id="cde90-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="cde90-126">في علامة التبويب السريعة **المدفوعات**، تأكد من تعيين حقول **شروط الدفع** و **طريقة الدفع** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="cde90-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cde90-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cde90-127">Additional resources</span></span>

[<span data-ttu-id="cde90-128">تكوين BOPIS</span><span class="sxs-lookup"><span data-stu-id="cde90-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="cde90-129">تمكين أوضاع تسليم الانتقاء المتعددة لأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="cde90-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="cde90-130">مدفوعات أمر Commerce بالقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="cde90-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="cde90-131">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="cde90-131">Store selector module</span></span>](../store-selector.md)
