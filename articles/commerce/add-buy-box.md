---
title: الوحدة النمطية لمربع شراء
description: يتناول هذا الموضوع وحدات مربع الشراء ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686660"
---
# <a name="buy-box-module"></a><span data-ttu-id="c9b51-103">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="c9b51-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c9b51-104">يتناول هذا الموضوع وحدات مربع الشراء ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9b51-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9b51-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c9b51-105">Overview</span></span>

<span data-ttu-id="c9b51-106">يُشير مصطلح *مربع الشراء* عادةً إلى منطقة صفحة تفاصيل المنتج التي تكون "فوق المُجلد،" والتي تستضيف كافة المعلومات الأكثر أهمية المطلوبة لإجراء عملية شراء للمنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="c9b51-107">(وتكون المنطقة الموجود "فوق المُجلد" مرئية عند تحميل الصفحة للمرة الأولى، بحيث لا يضطر المستخدمون للتمرير لأسفل لعرضها.)</span><span class="sxs-lookup"><span data-stu-id="c9b51-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="c9b51-108">تُعد الوحدة النمطية لمربع الشراء حاوية خاصة يتم استخدامها لاستضافة كافة الوحدات النمطية التي تظهر في مساحة مربع شراء صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="c9b51-109">ويتضمن عنوان URL الخاص بصفحة تفاصيل المنتج مُعرف المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="c9b51-110">يتم اشتقاق كافة المعلومات المطلوبة لعرض الوحدة النمطية لمربع الشراء من مُعرف المنتج هذا.</span><span class="sxs-lookup"><span data-stu-id="c9b51-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="c9b51-111">إذا لم يتم توفير مُعرف منتج، فلن يتم عرض الوحدة النمطية لصندوق الشراء بشكل صحيح في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c9b51-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="c9b51-112">وبالتالي، لا يمكن استخدام الوحدة النمطية لصندوق الشراء الا في الصفحات التي تتضمن سياق المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="c9b51-113">لاستخدامها في صفحة لا تتضمن سياق منتج (على سبيل المثال، صفحة رئيسية أو صفحة تسويق)، يجب القيام بتخصيصات إضافية.</span><span class="sxs-lookup"><span data-stu-id="c9b51-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="c9b51-114">تعرض الصورة التالية مثالاُ لوحدة نمطيه لمربع شراء في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-114">The following image shows an example of a buy box module on a product details page.</span></span>

![مثال لوحدة نمطية لمربع شراء](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="c9b51-116">خصائص الوحدة النمطية لمربع شراء وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="c9b51-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="c9b51-117">في صفحة تفاصيل المنتج، يتم تقسيم مربع الشراء إلى منطقتين: منطقة الوسائط على اليسار ومنطقة المحتوى على اليمين.</span><span class="sxs-lookup"><span data-stu-id="c9b51-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="c9b51-118">بشكل افتراضي، نسبة عرض عمود منطقة الوسائط إلى عرض عمود منطقة المحتوى هي 2:1.</span><span class="sxs-lookup"><span data-stu-id="c9b51-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="c9b51-119">على الأجهزة المحمولة، يتم تكديس المنطقتين، بحيث تظهر منطقة تحت المنطقة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c9b51-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="c9b51-120">يمكن استخدام النُسق لتخصيص عرض الأعمدة وترتيب التكديس.</span><span class="sxs-lookup"><span data-stu-id="c9b51-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="c9b51-121">تعرض الوحدة النمطية لصندوق الشراء العنوان والوصف والسعر والتقييمات الخاصة بأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c9b51-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="c9b51-122">وتسمح أيضًا للعملاء بتحديد متغيرات المنتج التي لها سمات منتج مختلفة، مثل الحجم والنمط واللون.</span><span class="sxs-lookup"><span data-stu-id="c9b51-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="c9b51-123">عند تحديد مُتغير منتج، يتم تحديث الخصائص الأخرى في مربع الشراء (على سبيل المثال، وصف المنتج والصور) لتعكس معلومات المتغير.</span><span class="sxs-lookup"><span data-stu-id="c9b51-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="c9b51-124">يتم توفير محدد الكمية، بحيث يمكن للعملاء تحديد كمية الأصناف لشرائها.</span><span class="sxs-lookup"><span data-stu-id="c9b51-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="c9b51-125">يمكن تحديد الكمية القصوى التي يمكن شراؤها في إعدادات الموقع.</span><span class="sxs-lookup"><span data-stu-id="c9b51-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="c9b51-126">من صندوق الشراء، بإمكان العملاء أيضًا تنفيذ إجراءات مثل إضافة منتج إلى سلة التسوق وإضافة منتج إلى قائمة الأمنيات وتحديد موقع انتقاء.</span><span class="sxs-lookup"><span data-stu-id="c9b51-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="c9b51-127">يمكن القيام بهذه الإجراءات في منتج أو متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="c9b51-128">لإضافة منتج إلى قائمة أمنيات، يجب على العميل تسجيل دخوله.</span><span class="sxs-lookup"><span data-stu-id="c9b51-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="c9b51-129">يمكن استخدام النُسق لإزالة خصائص منتج صندوق الشراء وعناصر التحكم في الإجراء أو تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="c9b51-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="c9b51-130">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="c9b51-130">Module properties</span></span>

- <span data-ttu-id="c9b51-131">**علامة العنوان** – تقوم هذه الخاصية بتعريف علامة العنوان لعنوان المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="c9b51-132">إذا كان صندوق الشراء في أعلى الصفحة، فيجب تعيين هذه الخاصية إلى **h1** لتلبيه معايير إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="c9b51-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="c9b51-133">الوحدات التي يُمكن استخدامها في وحدة مربع الشراء</span><span class="sxs-lookup"><span data-stu-id="c9b51-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="c9b51-134">**معرض الوسائط** - تستخدم هذه الوحدة النمطية لإظهار صور أحد المنتجات في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="c9b51-135">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لمعرض الوسائط‬](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="c9b51-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="c9b51-136">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="c9b51-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="c9b51-137">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="c9b51-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="c9b51-138">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لمحدد المتجر‬](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="c9b51-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="c9b51-139">إعدادات الوحدة النمطية لمربع الشراء</span><span class="sxs-lookup"><span data-stu-id="c9b51-139">Buy box module settings</span></span>

<span data-ttu-id="c9b51-140">يمكن تكوين إعدادات الوحدة النمطية لمربع الشراء في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="c9b51-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="c9b51-141">**الحد الأقصى لبنود عربة التسوق‬‏‫**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="c9b51-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="c9b51-142">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="c9b51-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="c9b51-143">**المخزون** – لمزيد من المعلومات حول كيفيه تطبيق إعدادات المخزون، راجع  [تطبيق إعدادات المخزون](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c9b51-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="c9b51-144">**إضافة إلى عربة التسويق** - تستخدم هذه الخاصية لتحديد السلوك بعد إضافة صنف إلى عربة التسوق.</span><span class="sxs-lookup"><span data-stu-id="c9b51-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="c9b51-145">القيم المحتملة هي **الانتقال إلى عربة التسوق** و**الانتقال إلى عربة التسوق** و**إظهار الإعلامات**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="c9b51-146">عند تعيين القيمة إلى **الانتقال إلى عربة التسوق**، يتم إرسال المستخدمين إلى صفحة عربة التسوق بعد إضافة صنف.</span><span class="sxs-lookup"><span data-stu-id="c9b51-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="c9b51-147">عند تعيين القيمة إلى **عدم الانتقال إلى عربة التسوق**، لا يتم إرسال المستخدمين إلى صفحة عربة التسوق بعد إضافة صنف.</span><span class="sxs-lookup"><span data-stu-id="c9b51-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="c9b51-148">عند تعيين القيمة إلى **إظهار الاعلامات**، يظهر إعلام تأكيد للمستخدمين ويمكنهم متابعة الاستعراض في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="c9b51-149">تعرض الصورة التالية مثالاً لإعلام التأكيد "تمت الإضافة إلى عربة التسوق" في موقع شركه Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c9b51-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![مثال عن وحدة نمطية للإعلام](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="c9b51-151">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="c9b51-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="c9b51-152">تسترد الوحدة النمطية لصندوق الشراء معلومات المنتج باستخدام واجهات برمجة التطبيقات (API) لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="c9b51-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="c9b51-153">يتم استخدام مُعرف المنتج من صفحة تفاصيل المنتج لاسترداد كافة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="c9b51-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="c9b51-154">إضافة وحدة لمربع شراء إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="c9b51-154">Add a buy box module to a page</span></span>

<span data-ttu-id="c9b51-155">لإضافة الوحدة النمطية لمربع الشراء إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c9b51-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c9b51-156">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="c9b51-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="c9b51-157">في مربع الحوار **جزء صفحة جديد**، حدد وحدة **صندوق الشراء‬**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="c9b51-158">ضمن **اسم جزء الصفحة**، أدخل الاسم **جزء صندوق الشراء**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-159">في فتحة **معرض الوسائط** للوحدة النمطية لصندوق الشراء، حدد علامة القطع (**...**), ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c9b51-160">في مربع الحوار **إضافة وحدة**، حدد الوحدة النمطية **معرض الوسائط**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-161">في فتحة **محدد المتجر** للوحدة النمطية لصندوق الشراء، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c9b51-162">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**محدد المتجر‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-163">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="c9b51-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c9b51-164">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="c9b51-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c9b51-165">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب ‎PDP**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-166">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c9b51-167">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-168">في الفتحة **الرئيسية** للصفحة الافتراضية، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء الصفحة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="c9b51-169">في مربع الحوار **تحديد جزء الصفحة‬‏‫**، حدد **جزء صندوق الشراء** الذي أنشأته في وقت سابق، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-170">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="c9b51-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c9b51-171">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="c9b51-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c9b51-172">في مربع الحوار **اختيار قالب**، حدد **قالب PDP**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="c9b51-173">ضمن **اسم الصفحة**، أدخل **صفحة PDP**، ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-174">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء الصفحة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="c9b51-175">في مربع الحوار **تحديد جزء الصفحة‬‏‫**، حدد **جزء صندوق الشراء** الذي أنشأته في وقت سابق، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9b51-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="c9b51-176">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="c9b51-176">Save and preview the page.</span></span> <span data-ttu-id="c9b51-177">أضف مُعلمة سلسلة استعلام **?productid=&lt;product id&gt;** إلى عنوان URL الخاص بصفحة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c9b51-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="c9b51-178">وبهذه الطريقة، يتم استخدام سياق المنتج لتحميل وعرض صفحة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c9b51-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="c9b51-179">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="c9b51-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="c9b51-180">يجب أن يظهر مُربع الشراء في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9b51-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9b51-181">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c9b51-181">Additional resources</span></span>

[<span data-ttu-id="c9b51-182">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="c9b51-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c9b51-183">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="c9b51-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c9b51-184">وحدة معرض الوسائط</span><span class="sxs-lookup"><span data-stu-id="c9b51-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="c9b51-185">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="c9b51-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c9b51-186">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="c9b51-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c9b51-187">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="c9b51-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c9b51-188">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="c9b51-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c9b51-189">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="c9b51-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c9b51-190">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="c9b51-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c9b51-191">الوحدة النمطية للتذييلات‬</span><span class="sxs-lookup"><span data-stu-id="c9b51-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="c9b51-192">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c9b51-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
