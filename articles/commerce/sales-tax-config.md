---
title: تكوين ضريبة المبيعات للأوامر عبر الإنترنت
description: يوفر هذا الموضوع نظرة عامة على تحديد مجموعة ضريبة المبيعات لأنواع مختلفة من الأوامر عبر الإنترنت في Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 56621bb9658b71551c7312aa47812903914bc888
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031779"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="60f94-103">تكوين ضريبة المبيعات للأوامر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="60f94-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60f94-104">يقدم هذا الموضوع نظرة عامة حول تحديد مجموعة ضريبة المبيعات لأنواع مختلفة من الأوامر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="60f94-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="60f94-105">قد ترغب قناة التجارة الإلكترونية الخاصة بك في دعم خيارات مثل التسليم أو الالتقاط للأوامر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="60f94-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="60f94-106">يعتمد تطبيق ضريبة المبيعات على الخيار الذي حدده المستخدمون عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="60f94-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="60f94-107">عندما يختار عميل الموقع شراء عنصر عبر الإنترنت وشحنه إلى عنوان، يتم تحديد ضريبة المبيعات بناءً على إعداد مجموعة ضريبة عنوان الشحن الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="60f94-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="60f94-108">عندما يختار العميل استلام عنصر تم شراؤه من متجر، يتم تحديد ضريبة المبيعات بناءً على إعداد مجموعة ضرائب متجر الالتقاط.</span><span class="sxs-lookup"><span data-stu-id="60f94-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="60f94-109">الأوامر التي يتم شحنها إلى عنوان العميل</span><span class="sxs-lookup"><span data-stu-id="60f94-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="60f94-110">بشكل عام ، يتم تحديد ضرائب الأوامر عبر الإنترنت التي يتم شحنها إلى عناوين العملاء حسب الوجهة.</span><span class="sxs-lookup"><span data-stu-id="60f94-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="60f94-111">تحتوي كل مجموعة ضرائب مبيعات على تكوين ضريبي قائم على وجهة البيع بالتجزئة حيث يمكن لنشاطك التجاري تحديد تفاصيل الوجهة مثل المقاطعة / المنطقة والولاية والمقاطعة والمدينة في شكل هرمي.</span><span class="sxs-lookup"><span data-stu-id="60f94-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="60f94-112">عند إنشاء أمر عبر الإنترنت، يستخدم مُشغل الضرائب التجارية عنوان التسليم لكل صنف في الأمر، ويبحث عن مجموعات ضريبة المبيعات بمعايير ضريبية مطابقة للوجهة.</span><span class="sxs-lookup"><span data-stu-id="60f94-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="60f94-113">على سبيل المثال، بالنسبة للأمر عبر الإنترنت وعنوان تسليم صنف إلى سان فرانسيسكو، كاليفورنيا، سوف يبحث محرك الضرائب عن مجموعة ضريبة المبيعات ورمز ضريبة المبيعات لولاية كاليفورنيا، ثم يحسب الضريبة لكل صنف وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="60f94-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="60f94-114">مجموعات الضرائب المستندة إلى العميل</span><span class="sxs-lookup"><span data-stu-id="60f94-114">Customer-based tax groups</span></span>

<span data-ttu-id="60f94-115">في المراكز الرئيسية لـ Commerce، يوجد مكانان يتم فيهما تكوين مجموعات ضرائب العملاء:</span><span class="sxs-lookup"><span data-stu-id="60f94-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="60f94-116">**ملف تعريف العميل**</span><span class="sxs-lookup"><span data-stu-id="60f94-116">**Customer's profile**</span></span>
- <span data-ttu-id="60f94-117">**عنوان الشحن الخاص بالعميل**</span><span class="sxs-lookup"><span data-stu-id="60f94-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="60f94-118">إذا كان ملف تعريف العميل يحتوي على مجموعة ضريبية مُكونة</span><span class="sxs-lookup"><span data-stu-id="60f94-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="60f94-119">قد يكون لسجل ملف تعريف العميل في المراكز الرئيسية مجموعة ضريبة مبيعات مُكونة، ولكن بالنسبة للأوامر عبر الإنترنت، لن يتم استخدام مجموعة ضريبة المبيعات المُكونة في ملف تعريف العميل بواسطة محرك الضرائب.</span><span class="sxs-lookup"><span data-stu-id="60f94-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="60f94-120">إذا كان عنوان الشحن الخاص بالعميل به مجموعة ضريبية مُكونة</span><span class="sxs-lookup"><span data-stu-id="60f94-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="60f94-121">إذا كان سجل عنوان الشحن الخاص بالعميل يحتوي على مجموعة ضريبية مُكونة وتم شحن الأمر عبر الإنترنت (أو صنف) إلى عنوان الشحن الخاص بالعميل، فسيتم استخدام المجموعة الضريبية المُكونة في سجل عنوان العميل بواسطة محرك الضرائب لحسابات الضرائب.</span><span class="sxs-lookup"><span data-stu-id="60f94-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="60f94-122">تكوين مجموعة ضريبية لسجل عنوان الشحن الخاص بالعميل</span><span class="sxs-lookup"><span data-stu-id="60f94-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="60f94-123">لتكوين مجموعة ضريبية لسجل عنوان الشحن الخاص بالعميل في المراكز الرئيسية لـ Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="60f94-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="60f94-124">انتقل إلى **كافة العملاء**، ثم حدد العميل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="60f94-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="60f94-125">في علامة التبويب السريعة **العناوين** ، حدد العنوان المطلوب، ثم حدد **المزيد من الخيارات \> خيارات متقدمة**.</span><span class="sxs-lookup"><span data-stu-id="60f94-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="60f94-126">ضمن علامة التبويب **عام** في صفحة **إدارة العناوين** ، قم بتعيين قيمة ضريبة المبيعات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="60f94-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="60f94-127">يتم تحديد مجموعة الضرائب باستخدام عنوان التسليم لصنف الأمر ويتم تكوين الضرائب المستندة إلى الوجهة في مجموعة الضرائب نفسها.</span><span class="sxs-lookup"><span data-stu-id="60f94-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="60f94-128">لمزيد من المعلومات، راجع [‏‫إعداد الضرائب للمتاجر على الإنترنت مستندة إلى الوجهة‬](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="60f94-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="60f94-129">التقاط الأمر في المتجر</span><span class="sxs-lookup"><span data-stu-id="60f94-129">Order pickup in store</span></span>

<span data-ttu-id="60f94-130">بالنسبة لأصناف الأمر ذات الوضع التقاط في المتجر أو التقاط على الطريق المُحدد، سيتم تطبيق المجموعة الضريبية من متجر الالتقاط المحدد.</span><span class="sxs-lookup"><span data-stu-id="60f94-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="60f94-131">للحصول على تفاصيل حول كيفية تكوين مجموعة الضرائب لمتجر معين، راجع [تعيين خيارات الضرائب الأخرى للمتاجر](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="60f94-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="60f94-132">عندما يتم استلام بند أمر في أحد المتاجر، سيتم تجاهل إعدادات ضريبة عنوان العميل (في حالة الإعداد) بواسطة محرك الضرائب وسيتم تطبيق تكوين ضريبة متجر الالتقاط.</span><span class="sxs-lookup"><span data-stu-id="60f94-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="60f94-133">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="60f94-133">Additional resources</span></span>

[<span data-ttu-id="60f94-134">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="60f94-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="60f94-135">طرق حساب ضريبة المبيعات في حقل الأصل</span><span class="sxs-lookup"><span data-stu-id="60f94-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="60f94-136"> تعيين ضريبة المبيعات والتجاوزات</span><span class="sxs-lookup"><span data-stu-id="60f94-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="60f94-137">خيارات حساب المبلغ بالكامل والفاصل الزمني لأكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="60f94-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="60f94-138">حساب الإعفاء الضريبي</span><span class="sxs-lookup"><span data-stu-id="60f94-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 

