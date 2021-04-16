---
title: الوحدة النمطية لسلة التسوق
description: يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797853"
---
# <a name="cart-module"></a><span data-ttu-id="d2b6e-103">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="d2b6e-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2b6e-104">يتناول هذا الموضوع وحدات سلة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d2b6e-105">تُظهر وحدة سلة التسوق لعرض الأصناف التي تمت إضافتها إلى سلة التسوق قبل أن يتابع العميل السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="d2b6e-106">كما تعرض الوحدة ملخص أدوار وتتيح للعميل تطبيق الأكواد الترويجية أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="d2b6e-107">تدعم الوحدة النمطية لسلة التسوق والسداد مع الخروج‬ للشخص الذي سجل دخوله والسداد مع الخروج‬ للضيوف.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="d2b6e-108">وهي تتضمن أيضًا ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="d2b6e-109">يمكنك تكوين المسار إلى هذا الارتباط في **إعدادات الموقع \> الملحقات \> المسارات**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="d2b6e-110">تعرض وحدة سلة البيانات استنادًا إلى معرف السلة، والذي يعد ملف تعريف ارتباط المستعرض المتاح عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="d2b6e-111">تعرض الصورة التالية مثالاً عن صفحة سلة التسوق في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![مثال عن وحدة نمطية لسلة التسوق‬ في موقع Fabrikam](./media/cart2.PNG)

<span data-ttu-id="d2b6e-113">تعرض الصورة التالية مثالاً عن صفحة سلة التسوق في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="d2b6e-114">في هذا المثال، يوجد رسم معالجة لصنف بند.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-114">In this example, there is a handling fee for a line item.</span></span>

![مثال عن وحدة نمطية لسلة التسوق‬ مع رسوم معالجة لصنف بند](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="d2b6e-116">خصائص الوحدة النمطية لسلة التسوق وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="d2b6e-116">Cart module properties and slots</span></span>

| <span data-ttu-id="d2b6e-117">الخاصية</span><span class="sxs-lookup"><span data-stu-id="d2b6e-117">Property</span></span> | <span data-ttu-id="d2b6e-118">القيم</span><span class="sxs-lookup"><span data-stu-id="d2b6e-118">Values</span></span> | <span data-ttu-id="d2b6e-119">الوصف</span><span class="sxs-lookup"><span data-stu-id="d2b6e-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d2b6e-120">العنوان</span><span class="sxs-lookup"><span data-stu-id="d2b6e-120">Heading</span></span> | <span data-ttu-id="d2b6e-121">نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="d2b6e-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d2b6e-122">عنوان لسلة التسوق، مثل "حقيبة التسوق" أو أصناف في سلتك".</span><span class="sxs-lookup"><span data-stu-id="d2b6e-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="d2b6e-123">عرض أخطاء نفاد المخزون</span><span class="sxs-lookup"><span data-stu-id="d2b6e-123">Show out of stock errors</span></span> | <span data-ttu-id="d2b6e-124">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="d2b6e-124">**True** or **False**</span></span> | <span data-ttu-id="d2b6e-125">إذا تم تعيين هذه الخاصية إلى **صواب**، ستعرض صفحة السلة الأخطاء المتعلقة بالمخزون.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="d2b6e-126">ونوصي بتعيين هذه الخاصية إلى **صواب** إذا تم تطبيق عمليات فحص المخزون على الموقع.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="d2b6e-127">عرض تكاليف الشحن لأصناف البند</span><span class="sxs-lookup"><span data-stu-id="d2b6e-127">Show shipping charges for line items</span></span> | <span data-ttu-id="d2b6e-128">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="d2b6e-128">**True** or **False**</span></span> | <span data-ttu-id="d2b6e-129">في حالة تعيين هذه الخاصية إلى **خطأ**، ستعرض أصناف بنود السلة تكاليف الشحن، إذا توفرت هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="d2b6e-130">هذه الميزة غير مدعومة في نسق Fabrikam، بسبب قيام المستخدمين بتحديد الشحن فقط في سير مهام السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="d2b6e-131">ومع ذلك، يمكن تشغيل هذه الميزة في مهام سير العمل الأخرى إذا كانت قابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="d2b6e-132">إظهار العروض المتوفرة</span><span class="sxs-lookup"><span data-stu-id="d2b6e-132">Show available promotions</span></span>| <span data-ttu-id="d2b6e-133">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="d2b6e-133">**True** or **False**</span></span> | <span data-ttu-id="d2b6e-134">إذا تم تعيين هذه الخاصية على **صحيح**، ستعرض السلة العروض الترويجية المتوفرة، استنادا إلى الأصناف الموجودة في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="d2b6e-135">تتوفر هذه الإمكانية في الإصدار 10.0.16 من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="d2b6e-136">الوحدات التي يُمكن استخدامها في الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="d2b6e-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="d2b6e-137">**كتلة النص**- تدعم هذه الوحدة المُراسلة المخصصة في الوحدة النمطية لسلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="d2b6e-138">يتم التحكم في الرسائل بواسطة نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="d2b6e-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="d2b6e-139">يُمكن إضافة أي رسالة، مثل "للمشكلات الخاصة بالطلب، اتصل بالرقم التالي 1-800-شركة Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="d2b6e-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="d2b6e-140">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="d2b6e-141">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="d2b6e-142">لمزيد من المعلومات حول هذه الوحدة، راجع [وحدة محدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d2b6e-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="d2b6e-143">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="d2b6e-143">Module properties</span></span>

<span data-ttu-id="d2b6e-144">يمكن تكوين إعدادات وحدة سلة التسوق في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="d2b6e-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="d2b6e-145">**الحد الأقصى للكمية**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="d2b6e-146">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="d2b6e-147">**المخزون** – لمزيد من المعلومات حول كيفيه تطبيق إعدادات المخزون، راجع  [تطبيق إعدادات المخزون](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d2b6e-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="d2b6e-148">**عودة إلى التسوق** – تُستخدم هذه الخاصية لتحديد مسار العودة إلى ارتباط **عودة إلى التسوق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="d2b6e-149">يمكن تكوين المسار على مستوي الموقع، مما يسمح لبائعي التجزئة بإعادة العميل إلى الصفحة الرئيسية أو أي صفحه أخرى على الموقع.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2b6e-150">في Dynamics 365 Commerce الإصدار 10.0.14 والإصدارات الأحدث، يتم تجميع الأصناف الموجودة في سلة التسوق استنادًا إلى الإعدادات المحددة في ملف تعريف الوظائف عبر الإنترنت للمتجر عبر الإنترنت في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="d2b6e-151">لمزيد من المعلومات حول كيفية إنشاء ملف تعريف الوظائف عبر الإنترنت وتعيين الخصائص المطلوبة للتجميع، راجع [إنشاء ملف تعريف الوظائف عبر الإنترنت](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="d2b6e-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="d2b6e-152">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="d2b6e-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="d2b6e-153">تسترد الوحدة النمطية لسلة التسوق معلومات المنتج باستخدام واجهات API لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="d2b6e-154">يتم استخدام مُعرف سلة التسوق من ملف تعريف ارتباط المستعرض لاسترداد كافة معلومات المنتج من Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="d2b6e-155">إضافة الوحدة النمطية لسلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="d2b6e-155">Add a cart module to a page</span></span>

<span data-ttu-id="d2b6e-156">لإضافة وحدة سلة تسوق إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d2b6e-157">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d2b6e-158">في مربع الحوار **جزء جديد**، حدد وحدة **سلة التسوق‬**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="d2b6e-159">ضمن **اسم الجزء**، أدخل الاسم **جزء سلة التسوق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="d2b6e-160">حدد فتحة **سلة التسوق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="d2b6e-161">في جزء الخصائص على الجانب الأيسر، حدد رمز القلم الرصاص، وأدخل نص العنوان في الحقل، ثم حدد رمز علامة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="d2b6e-162">في فتحة **سلة التسوق‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2b6e-163">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**محدد المتجر‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2b6e-164">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d2b6e-165">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d2b6e-166">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="d2b6e-167">في شجرة المخطط التفصيلي، حدد فتحة **النص الأساسي**، وحدد علامة القطع (**...**)، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d2b6e-168">في مربع الحوار **تحديد جزء‬‏‫**، حدد **جزء سلة التسوق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d2b6e-169">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d2b6e-170">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d2b6e-171">في مربع الحوار **اختيار**، حدد القالب الذي أنشأته، وأدخل اسم صفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="d2b6e-172">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d2b6e-173">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="d2b6e-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2b6e-174">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d2b6e-174">Additional resources</span></span>

[<span data-ttu-id="d2b6e-175">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="d2b6e-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d2b6e-176">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="d2b6e-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d2b6e-177">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="d2b6e-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d2b6e-178">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="d2b6e-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d2b6e-179">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="d2b6e-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d2b6e-180">الوحدة النمطية لمعلومات الاستلام</span><span class="sxs-lookup"><span data-stu-id="d2b6e-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d2b6e-181">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="d2b6e-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d2b6e-182">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="d2b6e-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="d2b6e-183">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="d2b6e-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="d2b6e-184">إنشاء ملف تعريف وظائف على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="d2b6e-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]