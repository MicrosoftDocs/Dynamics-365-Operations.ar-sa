---
title: الوحدة النمطية لسلة التسوق
description: يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411263"
---
# <a name="cart-module"></a><span data-ttu-id="27655-103">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="27655-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="27655-104">يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27655-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27655-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="27655-105">Overview</span></span>

<span data-ttu-id="27655-106">تُظهر وحدة سلة التسوق لعرض الأصناف التي تمت إضافتها إلى سلة التسوق قبل أن يتابع العميل السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="27655-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="27655-107">كما تعرض الوحدة ملخص أدوار وتتيح للعميل تطبيق الأكواد الترويجية أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="27655-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="27655-108">تدعم الوحدة النمطية لسلة التسوق والسداد مع الخروج‬ للشخص الذي سجل دخوله والسداد مع الخروج‬ للضيوف.</span><span class="sxs-lookup"><span data-stu-id="27655-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="27655-109">وهي تتضمن أيضًا ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="27655-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="27655-110">يمكنك تكوين المسار إلى هذا الارتباط في **إعدادات الموقع \> الملحقات \> المسارات**.</span><span class="sxs-lookup"><span data-stu-id="27655-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="27655-111">تعرض وحدة سلة البيانات استنادًا إلى معرف السلة، والذي يعد ملف تعريف ارتباط المستعرض المتاح عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="27655-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="27655-112">تعرض الصورة التالية مثالاً عن صفحة سلة التسوق في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="27655-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![مثال عن وحدة سلة التسوق](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="27655-114">خصائص الوحدة النمطية لسلة التسوق وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="27655-114">Cart module properties and slots</span></span>

<span data-ttu-id="27655-115">تتضمن الوحدة النمطية لسله التسوق خاصية **العنوان‬** التي يمكن تعيينها إلى قيم مثل **حقيبة التسوق‬‏‫** و**الأصناف في سلة التسوق الخاصة بك‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="27655-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="27655-116">الوحدات التي يُمكن استخدامها في الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="27655-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="27655-117">**كتلة النص**- تدعم هذه الوحدة المُراسلة المخصصة في الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="27655-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="27655-118">يتم التحكم في الرسائل بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="27655-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="27655-119">يُمكن إضافة أي رسالة، مثل "للمشكلات الخاصة بالطلب، اتصل بالرقم التالي 1-800-شركة Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="27655-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="27655-120">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="27655-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="27655-121">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="27655-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="27655-122">لمزيد من المعلومات حول هذه الوحدة، راجع [وحدة محدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="27655-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="27655-123">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="27655-123">Module properties</span></span>

<span data-ttu-id="27655-124">يمكن تكوين إعدادات وحدة سلة التسوق في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="27655-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="27655-125">**الحد الأقصى للكمية**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="27655-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="27655-126">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="27655-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="27655-127">**المخزون** – لمزيد من المعلومات حول كيفيه تطبيق إعدادات المخزون، راجع  [تطبيق إعدادات المخزون](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="27655-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="27655-128">**عودة إلى التسوق** – تُستخدم هذه الخاصية لتحديد مسار العودة إلى ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="27655-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="27655-129">يمكن تكوين المسار على مستوي الموقع، مما يسمح لبائعي التجزئة بإعادة العميل إلى الصفحة الرئيسية أو أي صفحه أخرى على الموقع.</span><span class="sxs-lookup"><span data-stu-id="27655-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="27655-130">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="27655-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="27655-131">تسترد الوحدة النمطية لسلة التسوق معلومات المنتج باستخدام واجهات API لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="27655-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="27655-132">يتم استخدام مُعرف سلة التسوق من ملف تعريف ارتباط المستعرض لاسترداد كافة معلومات المنتج من Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="27655-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="27655-133">إضافة الوحدة النمطية لسلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="27655-133">Add a cart module to a page</span></span>

<span data-ttu-id="27655-134">لإضافة وحدة سلة تسوق إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="27655-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="27655-135">انتقل إلى **أجزاء الصفحة**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="27655-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="27655-136">في مربع الحوار **جزء صفحة جديد**، حدد وحدة **سلة التسوق‬**.</span><span class="sxs-lookup"><span data-stu-id="27655-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="27655-137">ضمن **اسم جزء الصفحة**، أدخل الاسم **جزء سلة التسوق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="27655-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="27655-138">حدد فتحة **سلة التسوق**.</span><span class="sxs-lookup"><span data-stu-id="27655-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="27655-139">في جزء الخصائص على الجانب الأيسر، حدد رمز القلم الرصاص، وأدخل نص العنوان في الحقل، ثم حدد رمز علامة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="27655-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="27655-140">في فتحة **سلة التسوق‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="27655-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="27655-141">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**محدد المتجر‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="27655-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="27655-142">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="27655-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="27655-143">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="27655-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="27655-144">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="27655-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="27655-145">في شجرة المخطط التفصيلي، حدد فتحة **النص الأساسي**، وحدد علامة القطع (**...**)، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="27655-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="27655-146">في مربع الحوار **تحديد جزء الصفحة‬‏‫**، حدد **جزء سلة التسوق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="27655-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="27655-147">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="27655-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="27655-148">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="27655-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="27655-149">في مربع الحوار **اختيار**، حدد القالب الذي أنشأته، وأدخل اسم صفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="27655-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="27655-150">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="27655-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="27655-151">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="27655-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27655-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="27655-152">Additional resources</span></span>

[<span data-ttu-id="27655-153">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="27655-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="27655-154">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="27655-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="27655-155">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="27655-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="27655-156">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="27655-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="27655-157">الوحدة النمطية لأيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="27655-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="27655-158">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="27655-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="27655-159">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="27655-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="27655-160">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="27655-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="27655-161">الوحدة النمطية للتذييلات‬</span><span class="sxs-lookup"><span data-stu-id="27655-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="27655-162">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="27655-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
