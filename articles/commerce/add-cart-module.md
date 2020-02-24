---
title: الوحدة النمطية لسلة التسوق
description: يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025426"
---
# <a name="cart-module"></a><span data-ttu-id="5f471-103">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="5f471-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5f471-104">يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f471-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f471-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5f471-105">Overview</span></span>

<span data-ttu-id="5f471-106">يتم استخدام الوحدة النمطية لسلة التسوق لعرض الأصناف التي تمت إضافتها إلى سله التسوق قبل أن يتابع العميل إلى السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="5f471-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="5f471-107">على سبيل المثال، إنها تتضمن جميع الأصناف التي تمت إضافتها إلى سلة التسوق وملخص الأمر.</span><span class="sxs-lookup"><span data-stu-id="5f471-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="5f471-108">كما تتيح للعميل تطبيق الرموز الترويجية أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="5f471-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="5f471-109">تدعم الوحدة النمطية لسلة التسوق والسداد مع الخروج‬ للشخص الذي سجل دخوله والسداد مع الخروج‬ للضيوف.</span><span class="sxs-lookup"><span data-stu-id="5f471-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="5f471-110">وهي تتضمن أيضًا ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="5f471-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="5f471-111">يمكنك تكوين المسار إلى هذا الارتباط في **إعدادات الموقع \> الملحقات \> المسارات**.</span><span class="sxs-lookup"><span data-stu-id="5f471-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="5f471-112">تعرض الوحدة النمطية لسلة التسوق البيانات بناءً على مُعرف سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="5f471-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="5f471-113">يُمثل مُعرف سلة التسوق ملف تعريف ارتباط المستعرض المتوفر من خلال الموقع.</span><span class="sxs-lookup"><span data-stu-id="5f471-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="5f471-114">خصائص الوحدة النمطية لسلة التسوق وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="5f471-114">Cart module properties and slots</span></span>

<span data-ttu-id="5f471-115">تتضمن الوحدة النمطية لسله التسوق خاصية **العنوان‬** التي يمكن تعيينها إلى قيم مثل **حقيبة التسوق‬‏‫** و**الأصناف في سلة التسوق الخاصة بك‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="5f471-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="5f471-116">الوحدات التي يُمكن استخدامها في الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="5f471-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="5f471-117">**كتلة النص**- تدعم هذه الوحدة المُراسلة المخصصة في الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="5f471-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="5f471-118">يتم التحكم في الرسائل بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="5f471-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="5f471-119">يُمكن إضافة أي رسالة، مثل "للمشكلات الخاصة بالطلب، اتصل بالرقم التالي 1-800-شركة Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="5f471-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="5f471-120">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="5f471-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="5f471-121">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="5f471-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="5f471-122">تتكامل وحدة محدد المتجر مع واجهة برمجة تطبيقات (API) للتشفير الجغرافي لخرائط Bing لتحويل الموقع الذي ادخله العميل إلى خط عرض وخط طول.</span><span class="sxs-lookup"><span data-stu-id="5f471-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="5f471-123">يلزم إدخال مفتاح API لخرائط Bing ويجب إضافته إلى صفحة المعلمات المشتركة للبيع بالتجزئة في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="5f471-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="5f471-124">تدعم هذه الوحدة الخاصيتين **شعاع البحث** و**ارتباط شروط الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="5f471-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="5f471-125">تحدد خاصية **شعاع البحث** نطاق البحث للمتاجر، بالأميال.</span><span class="sxs-lookup"><span data-stu-id="5f471-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="5f471-126">إذا لم يتم تحديد قيمة، فيتم استخدام شعاع البحث الافتراضي، 50 ميلاً.</span><span class="sxs-lookup"><span data-stu-id="5f471-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="5f471-127">إذا تم استخدام خرائط Bing أو أي خدمة خارجية، فيمكن استخدام خاصية **ارتباط شروط الخدمة** لتوفير ارتباط إلى شروط الخدمة.</span><span class="sxs-lookup"><span data-stu-id="5f471-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="5f471-128">يعتبر ارتباط شروط الخدمة ضروريًا لخدمة خرائط Bing.</span><span class="sxs-lookup"><span data-stu-id="5f471-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="5f471-129">إعداد الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="5f471-129">Cart module settings</span></span>

<span data-ttu-id="5f471-130">تتضمن وحدات سلة التسوق الإعدادات التالية التي يمكن تكوينها في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="5f471-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="5f471-131">**الحد الأقصى للكمية**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="5f471-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="5f471-132">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="5f471-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="5f471-133">**فحص المخزون**- عندما يتم تعيين القيمة إلى **صحيح**، تتم إضافة عنصر إلى سلة التسوق فقط بعد تأكد وحدة مُربع الشراء من وجودها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="5f471-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="5f471-134">يتم إجراء فحص المخزون لكل من السيناريوهات التي سوف يتم فيها شحن الصنف وللسيناريوهات التي سوف يتم فيها انتقائها في المتجر.</span><span class="sxs-lookup"><span data-stu-id="5f471-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="5f471-135">إذا تم تعيين القيمة إلى **خطأ**، فلن يتم إجراء فحص المخزون قبل إضافة أي صنف إلى سلة التسوق ووضع الأمر.</span><span class="sxs-lookup"><span data-stu-id="5f471-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="5f471-136">**المخزن المؤقت للمخزون‬‏‫** – تُستخدم هذه الخاصية لتحديد رقم المخزن المؤقت للمخزون.</span><span class="sxs-lookup"><span data-stu-id="5f471-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="5f471-137">يتم الاحتفاظ بالمخزون في الوقت الفعلي، وعندما يقوم العديد من العملاء بوضع الأوامر، قد يكون من الصعب الحفاظ على جرد المخزون الدقيق.</span><span class="sxs-lookup"><span data-stu-id="5f471-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="5f471-138">وعند إجراء فحص للمخزون، إذا كان المخزون أقل من مبلغ المخزن المؤقت، يتم مُعاملة المنتج على أنه خارج المخزون.</span><span class="sxs-lookup"><span data-stu-id="5f471-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="5f471-139">وبالتالي، عندما تُجرى المبيعات سريعًا من خلال قنوات متعددة، ولا تتم مزامنة جرد المخزون بالكامل، فمن ثم تقل فرصة خطر بيع صنف غير موجود في المخزون.</span><span class="sxs-lookup"><span data-stu-id="5f471-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="5f471-140">**عودة إلى التسوق** – تُستخدم هذه الخاصية لتحديد مسار العودة إلى ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="5f471-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="5f471-141">يمكن تكوين هذا المسار على مستوي الموقع.</span><span class="sxs-lookup"><span data-stu-id="5f471-141">This route can be configured at the site level.</span></span> <span data-ttu-id="5f471-142">يسمح هذا التكوين لبائعي التجزئة بإعادة العميل إلى الصفحة الرئيسية أو أي صفحة أخرى في الموقع.</span><span class="sxs-lookup"><span data-stu-id="5f471-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="5f471-143">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="5f471-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="5f471-144">تسترد الوحدة النمطية لسلة التسوق معلومات المنتج باستخدام واجهات API لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="5f471-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="5f471-145">يتم استخدام مُعرف سلة التسوق من ملف تعريف ارتباط المستعرض لاسترداد كافة معلومات المنتج من Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="5f471-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="5f471-146">إضافة الوحدة النمطية لسلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="5f471-146">Add a cart module to a page</span></span>

<span data-ttu-id="5f471-147">لإضافة وحدة سلة تسوق إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5f471-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5f471-148">أنشئ جزءًا يسمى **جزء سلة التسوق**، وأضف الوحدة النمطية لسلة التسوق إليه.</span><span class="sxs-lookup"><span data-stu-id="5f471-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="5f471-149">أضف عنوانًا إلى الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="5f471-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="5f471-150">أضف وحدة نمطية لمحدد المتجر إلى الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="5f471-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="5f471-151">احفظ الجزء ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="5f471-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="5f471-152">أنشئ قالبًا يُسمى **قالب سلة التسوق**، وأضف جزء السلة الذي قمت بإنشائه للتو.</span><span class="sxs-lookup"><span data-stu-id="5f471-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="5f471-153">احفظ القالب ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="5f471-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="5f471-154">قم بإنشاء صفحة تستخدم القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="5f471-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="5f471-155">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="5f471-155">Save and preview the page.</span></span>
1. <span data-ttu-id="5f471-156">انشر الصفحة بعد الانتهاء من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="5f471-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f471-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5f471-157">Additional resources</span></span>

[<span data-ttu-id="5f471-158">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="5f471-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5f471-159">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="5f471-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5f471-160">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="5f471-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5f471-161">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="5f471-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5f471-162">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="5f471-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5f471-163">الوحدة النمطية للعنوان</span><span class="sxs-lookup"><span data-stu-id="5f471-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5f471-164">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="5f471-164">Footer module</span></span>](author-footer-module.md)
