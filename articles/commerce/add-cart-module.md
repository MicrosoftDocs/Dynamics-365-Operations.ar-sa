---
title: الوحدة النمطية لسلة التسوق
description: يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261411"
---
# <a name="cart-module"></a><span data-ttu-id="c82ba-103">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="c82ba-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c82ba-104">يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c82ba-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c82ba-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c82ba-105">Overview</span></span>

<span data-ttu-id="c82ba-106">تُظهر وحدة سلة التسوق لعرض الأصناف التي تمت إضافتها إلى سلة التسوق قبل أن يتابع العميل السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="c82ba-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="c82ba-107">كما تعرض الوحدة ملخص أدوار وتتيح للعميل تطبيق الأكواد الترويجية أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="c82ba-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="c82ba-108">تدعم الوحدة النمطية لسلة التسوق والسداد مع الخروج‬ للشخص الذي سجل دخوله والسداد مع الخروج‬ للضيوف.</span><span class="sxs-lookup"><span data-stu-id="c82ba-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="c82ba-109">وهي تتضمن أيضًا ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="c82ba-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="c82ba-110">يمكنك تكوين المسار إلى هذا الارتباط في **إعدادات الموقع \> الملحقات \> المسارات**.</span><span class="sxs-lookup"><span data-stu-id="c82ba-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="c82ba-111">تعرض وحدة سلة البيانات استنادًا إلى معرف السلة، والذي يعد ملف تعريف ارتباط المستعرض المتاح عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="c82ba-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="c82ba-112">خصائص الوحدة النمطية لسلة التسوق وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="c82ba-112">Cart module properties and slots</span></span>

<span data-ttu-id="c82ba-113">تتضمن الوحدة النمطية لسله التسوق خاصية **العنوان‬** التي يمكن تعيينها إلى قيم مثل **حقيبة التسوق‬‏‫** و**الأصناف في سلة التسوق الخاصة بك‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c82ba-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="c82ba-114">الوحدات التي يُمكن استخدامها في الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="c82ba-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="c82ba-115">**كتلة النص**- تدعم هذه الوحدة المُراسلة المخصصة في الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="c82ba-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="c82ba-116">يتم التحكم في الرسائل بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="c82ba-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="c82ba-117">يُمكن إضافة أي رسالة، مثل "للمشكلات الخاصة بالطلب، اتصل بالرقم التالي 1-800-شركة Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="c82ba-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="c82ba-118">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="c82ba-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="c82ba-119">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="c82ba-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="c82ba-120">لمزيد من المعلومات حول هذه الوحدة، راجع [وحدة محدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="c82ba-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="c82ba-121">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="c82ba-121">Module properties</span></span>

<span data-ttu-id="c82ba-122">تتضمن وحدات سلة التسوق الإعدادات التالية التي يمكن تكوينها في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="c82ba-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="c82ba-123">**الحد الأقصى للكمية**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="c82ba-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="c82ba-124">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="c82ba-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="c82ba-125">**فحص المخزون**- عندما يتم تعيين القيمة إلى **صحيح**، تتم إضافة عنصر إلى سلة التسوق فقط بعد تأكد وحدة مُربع الشراء من وجودها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="c82ba-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="c82ba-126">يتم إجراء فحص المخزون للسيناريوهات التي سوف يتم فيها شحن الصنف وللسيناريوهات التي سوف يتم فيها انتقاؤها في المتجر.</span><span class="sxs-lookup"><span data-stu-id="c82ba-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="c82ba-127">إذا تم تعيين القيمة إلى **خطأ**، فلن يتم إجراء فحص المخزون قبل إضافة أي صنف إلى سلة التسوق ووضع الأمر.</span><span class="sxs-lookup"><span data-stu-id="c82ba-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="c82ba-128">للحصول على معلومات حول كيفية تكوين إعدادات المخزون في المكتب الخلفي ، راجع [حساب توفر المخزون لقنوات البيع بالتجزئة‬](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="c82ba-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="c82ba-129">**المخزن المؤقت للمخزون‬‏‫** – تُستخدم هذه الخاصية لتحديد رقم المخزن المؤقت للمخزون.</span><span class="sxs-lookup"><span data-stu-id="c82ba-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="c82ba-130">يتم الاحتفاظ بالمخزون في الوقت الفعلي، وعندما يقوم العديد من العملاء بوضع الأوامر، قد يكون من الصعب الحفاظ على جرد المخزون الدقيق.</span><span class="sxs-lookup"><span data-stu-id="c82ba-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="c82ba-131">وعند إجراء فحص للمخزون، إذا كان المخزون أقل من مبلغ المخزن المؤقت، يتم مُعاملة المنتج على أنه خارج المخزون.</span><span class="sxs-lookup"><span data-stu-id="c82ba-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="c82ba-132">وبالتالي، عندما تُجرى المبيعات سريعًا من خلال قنوات متعددة، ولا تتم مزامنة جرد المخزون بالكامل، فمن ثم تقل فرصة خطر بيع صنف غير موجود في المخزون.</span><span class="sxs-lookup"><span data-stu-id="c82ba-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="c82ba-133">**عودة إلى التسوق** – تُستخدم هذه الخاصية لتحديد مسار العودة إلى ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="c82ba-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="c82ba-134">يمكن تكوين المسار على مستوي الموقع، مما يسمح لبائعي التجزئة بإعادة العميل إلى الصفحة الرئيسية أو أي صفحه أخرى على الموقع.</span><span class="sxs-lookup"><span data-stu-id="c82ba-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="c82ba-135">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="c82ba-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="c82ba-136">تسترد الوحدة النمطية لسلة التسوق معلومات المنتج باستخدام واجهات API لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="c82ba-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="c82ba-137">يتم استخدام مُعرف سلة التسوق من ملف تعريف ارتباط المستعرض لاسترداد كافة معلومات المنتج من Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="c82ba-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="c82ba-138">إضافة الوحدة النمطية لسلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="c82ba-138">Add a cart module to a page</span></span>

<span data-ttu-id="c82ba-139">لإضافة وحدة سلة تسوق إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c82ba-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c82ba-140">أنشئ جزءًا يسمى **جزء سلة التسوق**، وأضف وحدة سلة التسوق إلى الجزء الجديد.</span><span class="sxs-lookup"><span data-stu-id="c82ba-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="c82ba-141">أضف عنوانًا إلى الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="c82ba-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="c82ba-142">أضف وحدة نمطية لمحدد المتجر إلى الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="c82ba-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="c82ba-143">احفظ الجزء، وقم بإنهاء التحرير، ثم انشر هذا الجزء.</span><span class="sxs-lookup"><span data-stu-id="c82ba-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="c82ba-144">أنشئ قالبًا يُسمى **قالب سلة التسوق**، وأضف جزء السلة الذي قمت بإنشائه للتو.</span><span class="sxs-lookup"><span data-stu-id="c82ba-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="c82ba-145">احفظ القالب، وقم بإنهاء التحرير، ثم انشر هذا االقالب.</span><span class="sxs-lookup"><span data-stu-id="c82ba-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="c82ba-146">قم بإنشاء صفحة تستخدم القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="c82ba-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="c82ba-147">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="c82ba-147">Save and preview the page.</span></span>
1. <span data-ttu-id="c82ba-148">قم بإنهاء تحرير الصفحة، ثم انشر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c82ba-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c82ba-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c82ba-149">Additional resources</span></span>

[<span data-ttu-id="c82ba-150">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="c82ba-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c82ba-151">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="c82ba-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c82ba-152">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="c82ba-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c82ba-153">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="c82ba-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c82ba-154">الوحدة النمطية لأيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="c82ba-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c82ba-155">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="c82ba-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c82ba-156">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="c82ba-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c82ba-157">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="c82ba-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c82ba-158">الوحدة النمطية للتذييلات‬</span><span class="sxs-lookup"><span data-stu-id="c82ba-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="c82ba-159">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c82ba-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
