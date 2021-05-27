---
title: لا يظهر خيار الانتقاء في صفحات سلة التسوق أو تفاصيل المنتج
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خيار التقاط في المتجر على صفحة سلة التسوق أو تفاصيل المنتج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020794"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="4998b-103">لا يظهر خيار "انتقاء هذا" في صفحات سلة التسوق أو تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="4998b-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4998b-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خيار التقاط في المتجر على صفحة سلة التسوق أو تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="4998b-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="4998b-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="4998b-105">Description</span></span>

<span data-ttu-id="4998b-106">لا يظهر زر **انتقاء هذا** في صفحة سلة التسوق أو صفحات تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="4998b-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="4998b-107">يبين الرسم التوضيحي التالي مثالا للصفحة التي تتضمن زر **انتقاء هذا**.</span><span class="sxs-lookup"><span data-stu-id="4998b-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![زر انتهاء هذا](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="4998b-109">الدقة</span><span class="sxs-lookup"><span data-stu-id="4998b-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="4998b-110">تمكين ملحق BOPIS في منشئ مواقع Commerce</span><span class="sxs-lookup"><span data-stu-id="4998b-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="4998b-111">لتمكين ملحق "الشراء عبر الإنترنت، الانتقاء في المتجر" (BOPIS) في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4998b-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4998b-112">حدد موقعك.</span><span class="sxs-lookup"><span data-stu-id="4998b-112">Select your site.</span></span>
1. <span data-ttu-id="4998b-113">حدد **إعدادات الموقع**، ثم حدد **الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="4998b-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="4998b-114">تاكد من أنه تم مسح خيار **تعطيل BOPIS**.</span><span class="sxs-lookup"><span data-stu-id="4998b-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="4998b-115">تكوين أوضاع التسليم في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="4998b-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="4998b-116">لتكوين أوضاع التسليم في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4998b-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4998b-117">انتقل إلى **‏‫التدبير والتوريد‬ \> الإعداد \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="4998b-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="4998b-118">تأكد من أنه تم إنشاء وضع **الالتقاط للعميل**، وأنه تعيين المنتجات والعناوين إليه.</span><span class="sxs-lookup"><span data-stu-id="4998b-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="4998b-119">انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="4998b-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="4998b-120">في جزء التنقل الأيسر، حدد **أوامر العملاء**.</span><span class="sxs-lookup"><span data-stu-id="4998b-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="4998b-121">تأكد من تكوين **وضع انتقاء التسليم** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="4998b-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="4998b-122">تكوين مدفوعات أوامر العميل</span><span class="sxs-lookup"><span data-stu-id="4998b-122">Configure customer orders payments</span></span>

<span data-ttu-id="4998b-123">لتكوين مدفوعات أوامر العميل في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4998b-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4998b-124">انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="4998b-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="4998b-125">في جزء التنقل الأيسر، حدد **أوامر العملاء**.</span><span class="sxs-lookup"><span data-stu-id="4998b-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="4998b-126">في علامة التبويب السريعة **المدفوعات**، تأكد من تعيين حقول **شروط الدفع** و **طريقة الدفع** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="4998b-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4998b-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4998b-127">Additional resources</span></span>

[<span data-ttu-id="4998b-128">تكوين BOPIS</span><span class="sxs-lookup"><span data-stu-id="4998b-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="4998b-129">تمكين أوضاع تسليم الانتقاء المتعددة لأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="4998b-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="4998b-130">مدفوعات أمر Commerce بالقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="4998b-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="4998b-131">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="4998b-131">Store selector module</span></span>](../store-selector.md)
