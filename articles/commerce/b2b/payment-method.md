---
title: تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات B2B
description: يوضح هذا الموضوع كيفية تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211191"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="251d3-103">تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="251d3-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="251d3-104">يوضح هذا الموضوع كيفية تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات (B2B).</span><span class="sxs-lookup"><span data-stu-id="251d3-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="251d3-105">يستطيع تجار التجزئة قبول أنواع مختلفة من الدفع مقابل المنتجات والخدمات التي يبيعونها في قناة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="251d3-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="251d3-106">يجب أن يتم تكوين كل نوع دفع يقبله بائع تجزئة في Microsoft Dynamics 365 Commerce عند إعداد النظام.</span><span class="sxs-lookup"><span data-stu-id="251d3-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="251d3-107">يجب اعتماد طريقة الدفع بحساب العميل (أو "على الحساب")على مواقع التجارة الإلكترونية بين الشركات (B2B).</span><span class="sxs-lookup"><span data-stu-id="251d3-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="251d3-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="251d3-108">Prerequisites</span></span>

1. <span data-ttu-id="251d3-109">إضافة طريقة دفع حساب العميل في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="251d3-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="251d3-110">اربط طريقة دفع حساب العميل بقناة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="251d3-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="251d3-111">تأكد من تمكين **السماح على الحساب** للعميل في **البيع بالتجزئة والتجارة \> العملاء \> كافة العملاء \> افتراضيات الدفع** في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="251d3-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="251d3-112">وتأكد أيضًا من تعيين معلمات **حد الائتمان** بشكل مناسب للعميل في **البيع بالتجزئة والتجارة \> العملاء \> جميع العملاء \> الائتمان والتحصيلات** في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="251d3-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="251d3-113">تمكين طريقة دفع حساب العميل في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="251d3-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="251d3-114">لتمكين طريقة دفع حساب العميل في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="251d3-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="251d3-115">انتقل إلى **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="251d3-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="251d3-116">قم بتعيين خاصية **تمكين مدفوعات حساب العميل** إلى **ممكّن لعملاء B2B**.</span><span class="sxs-lookup"><span data-stu-id="251d3-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="251d3-117">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="251d3-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="251d3-118">تصبح إعدادات الموقع الجديدة سارية المفعول فقط بعد تحديث ملف app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="251d3-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="251d3-119">لمزيد من المعلومات ، راجع [تحديثات مكتبة SDK والوحدات النمطية](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="251d3-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="251d3-120">تمكين طريقة دفع حساب العميل في صفحة السداد مع الخروج لموقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="251d3-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="251d3-121">لتمكين طريقة دفع حساب العميل في صفحة السداد مع الخروج لموقع التجارة الإلكترونية بين الشركات B2B، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="251d3-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="251d3-122">في منشئ موقع Commerce، ابحث عن أو حرر صفحة السداد مع الخروج أو الجزء الذي يحتوي على الوحدة النمطية للسداد مع الخروج في موقع التجارة الإلكترونية بين الشركات B2B.</span><span class="sxs-lookup"><span data-stu-id="251d3-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="251d3-123">في فتحة **حاوية قسم السداد مع الخروج**، حدد **إضافة وحدة نمطية**، ثم أضف الوحدة النمطية **الدفع لحساب العميل**.</span><span class="sxs-lookup"><span data-stu-id="251d3-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="251d3-124">حدد وضع الوحدة النمطية **الدفع حساب العميل** عن طريق تحديد علامة القطع (**...**)، ثم حدد **التحريك لأعلى** أو **التحريك لأسفل** كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="251d3-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="251d3-125">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="251d3-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="251d3-126">التأكد من تمكين طريقة الدفع لحساب العميل ونشرها</span><span class="sxs-lookup"><span data-stu-id="251d3-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="251d3-127">للتأكد من تمكين طريقة الدفع لحساب العميل ونشرها، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="251d3-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="251d3-128">تسجيل الدخول إلى موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="251d3-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="251d3-129">أضف منتجًا إلى عربة التسوق.</span><span class="sxs-lookup"><span data-stu-id="251d3-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="251d3-130">انتقل إلى صفحة سداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="251d3-130">Go to the checkout page.</span></span> <span data-ttu-id="251d3-131">يجب أن تشاهد طريقة دفع **حساب العميل** الجديدة.</span><span class="sxs-lookup"><span data-stu-id="251d3-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="251d3-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="251d3-132">Additional resources</span></span>

[<span data-ttu-id="251d3-133">إعداد موقع تجارة إلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="251d3-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="251d3-134">إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات B2B</span><span class="sxs-lookup"><span data-stu-id="251d3-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="251d3-135">إدارة مستخدمي شركاء الأعمال على مواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="251d3-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="251d3-136">تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="251d3-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="251d3-137">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="251d3-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]