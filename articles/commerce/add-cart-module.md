---
title: الوحدة النمطية لسلة التسوق
description: يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 07d121d5a68970dd29f0e77babda735de12871ca
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761119"
---
# <a name="cart-module"></a><span data-ttu-id="383ca-103">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="383ca-103">Cart module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="383ca-104">يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="383ca-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="383ca-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="383ca-105">Overview</span></span>

<span data-ttu-id="383ca-106">تُظهر وحدة سلة التسوق لعرض الأصناف التي تمت إضافتها إلى سلة التسوق قبل أن يتابع العميل السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="383ca-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="383ca-107">كما تعرض الوحدة ملخص أدوار وتتيح للعميل تطبيق الأكواد الترويجية أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="383ca-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="383ca-108">تدعم الوحدة النمطية لسلة التسوق والسداد مع الخروج‬ للشخص الذي سجل دخوله والسداد مع الخروج‬ للضيوف.</span><span class="sxs-lookup"><span data-stu-id="383ca-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="383ca-109">وهي تتضمن أيضًا ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="383ca-110">يمكنك تكوين المسار إلى هذا الارتباط في **إعدادات الموقع \> الملحقات \> المسارات**.</span><span class="sxs-lookup"><span data-stu-id="383ca-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="383ca-111">تعرض وحدة سلة البيانات استنادًا إلى معرف السلة، والذي يعد ملف تعريف ارتباط المستعرض المتاح عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="383ca-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="383ca-112">تعرض الصورة التالية مثالاً عن صفحة سلة التسوق في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="383ca-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![مثال عن وحدة سلة التسوق](./media/cart2.PNG)

<span data-ttu-id="383ca-114">تعرض الصورة التالية مثالاً عن صفحة سلة التسوق في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="383ca-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="383ca-115">في هذا المثال، يوجد رسم معالجة لصنف بند.</span><span class="sxs-lookup"><span data-stu-id="383ca-115">In this example, there is a handling fee for a line item.</span></span>

![مثال عن وحدة سلة التسوق](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="383ca-117">خصائص الوحدة النمطية لسلة التسوق وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="383ca-117">Cart module properties and slots</span></span>

| <span data-ttu-id="383ca-118">الخاصية</span><span class="sxs-lookup"><span data-stu-id="383ca-118">Property</span></span> | <span data-ttu-id="383ca-119">القيم</span><span class="sxs-lookup"><span data-stu-id="383ca-119">Values</span></span> | <span data-ttu-id="383ca-120">الوصف</span><span class="sxs-lookup"><span data-stu-id="383ca-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="383ca-121">العنوان</span><span class="sxs-lookup"><span data-stu-id="383ca-121">Heading</span></span> | <span data-ttu-id="383ca-122">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="383ca-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="383ca-123">عنوان لسلة التسوق، مثل "حقيبة التسوق" أو أصناف في سلتك".</span><span class="sxs-lookup"><span data-stu-id="383ca-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="383ca-124">عرض أخطاء نفاد المخزون</span><span class="sxs-lookup"><span data-stu-id="383ca-124">Show out of stock errors</span></span> | <span data-ttu-id="383ca-125">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="383ca-125">**True** or **False**</span></span> | <span data-ttu-id="383ca-126">إذا تم تعيين هذه الخاصية إلى **صواب**، ستعرض صفحة السلة الأخطاء المتعلقة بالمخزون.</span><span class="sxs-lookup"><span data-stu-id="383ca-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="383ca-127">ونوصي بتعيين هذه الخاصية إلى **صواب** إذا تم تطبيق عمليات فحص المخزون على الموقع.</span><span class="sxs-lookup"><span data-stu-id="383ca-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="383ca-128">عرض تكاليف الشحن لأصناف البند</span><span class="sxs-lookup"><span data-stu-id="383ca-128">Show shipping charges for line items</span></span> | <span data-ttu-id="383ca-129">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="383ca-129">**True** or **False**</span></span> | <span data-ttu-id="383ca-130">في حالة تعيين هذه الخاصية إلى **خطأ**، ستعرض أصناف بنود السلة تكاليف الشحن، إذا توفرت هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="383ca-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="383ca-131">هذه الميزة غير مدعومة في نسق Fabrikam، بسبب قيام المستخدمين بتحديد الشحن فقط في سير مهام السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="383ca-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="383ca-132">ومع ذلك، يمكن تشغيل هذه الميزة في مهام سير العمل الأخرى إذا كانت قابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="383ca-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="383ca-133">الوحدات التي يُمكن استخدامها في الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="383ca-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="383ca-134">**كتلة النص**- تدعم هذه الوحدة المُراسلة المخصصة في الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="383ca-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="383ca-135">يتم التحكم في الرسائل بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="383ca-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="383ca-136">يُمكن إضافة أي رسالة، مثل "للمشكلات الخاصة بالطلب، اتصل بالرقم التالي 1-800-شركة Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="383ca-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="383ca-137">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="383ca-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="383ca-138">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="383ca-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="383ca-139">لمزيد من المعلومات حول هذه الوحدة، راجع [وحدة محدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="383ca-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="383ca-140">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="383ca-140">Module properties</span></span>

<span data-ttu-id="383ca-141">يمكن تكوين إعدادات وحدة سلة التسوق في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="383ca-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="383ca-142">**الحد الأقصى للكمية**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="383ca-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="383ca-143">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="383ca-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="383ca-144">**المخزون** – لمزيد من المعلومات حول كيفيه تطبيق إعدادات المخزون، راجع  [تطبيق إعدادات المخزون](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="383ca-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="383ca-145">**عودة إلى التسوق** – تُستخدم هذه الخاصية لتحديد مسار العودة إلى ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="383ca-146">يمكن تكوين المسار على مستوي الموقع، مما يسمح لبائعي التجزئة بإعادة العميل إلى الصفحة الرئيسية أو أي صفحه أخرى على الموقع.</span><span class="sxs-lookup"><span data-stu-id="383ca-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="383ca-147">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="383ca-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="383ca-148">تسترد الوحدة النمطية لسلة التسوق معلومات المنتج باستخدام واجهات API لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="383ca-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="383ca-149">يتم استخدام مُعرف سلة التسوق من ملف تعريف ارتباط المستعرض لاسترداد كافة معلومات المنتج من Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="383ca-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="383ca-150">إضافة الوحدة النمطية لسلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="383ca-150">Add a cart module to a page</span></span>

<span data-ttu-id="383ca-151">لإضافة وحدة سلة تسوق إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="383ca-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="383ca-152">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="383ca-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="383ca-153">في مربع الحوار **جزء جديد**، حدد وحدة **سلة التسوق‬**.</span><span class="sxs-lookup"><span data-stu-id="383ca-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="383ca-154">ضمن **اسم الجزء**، أدخل الاسم **جزء سلة التسوق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="383ca-155">حدد فتحة **سلة التسوق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="383ca-156">في جزء الخصائص على الجانب الأيسر، حدد رمز القلم الرصاص، وأدخل نص العنوان في الحقل، ثم حدد رمز علامة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="383ca-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="383ca-157">في فتحة **سلة التسوق‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="383ca-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="383ca-158">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**محدد المتجر‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="383ca-159">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="383ca-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="383ca-160">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="383ca-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="383ca-161">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="383ca-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="383ca-162">في شجرة المخطط التفصيلي، حدد فتحة **النص الأساسي**، وحدد علامة القطع (**...**)، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="383ca-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="383ca-163">في مربع الحوار **تحديد جزء‬‏‫**، حدد **جزء سلة التسوق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="383ca-164">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="383ca-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="383ca-165">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="383ca-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="383ca-166">في مربع الحوار **اختيار**، حدد القالب الذي أنشأته، وأدخل اسم صفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="383ca-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="383ca-167">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="383ca-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="383ca-168">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="383ca-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="383ca-169">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="383ca-169">Additional resources</span></span>

[<span data-ttu-id="383ca-170">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="383ca-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="383ca-171">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="383ca-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="383ca-172">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="383ca-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="383ca-173">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="383ca-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="383ca-174">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="383ca-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="383ca-175">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="383ca-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="383ca-176">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="383ca-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="383ca-177">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="383ca-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
