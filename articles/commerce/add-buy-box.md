---
title: الوحدة النمطية لمربع شراء
description: يتناول هذا الموضوع وحدات مربع الشراء ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: e07bf02f10c943947fdf9ed3333373b859ff5b6c
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817075"
---
# <a name="buy-box-module"></a><span data-ttu-id="fd049-103">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="fd049-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fd049-104">يتناول هذا الموضوع وحدات مربع الشراء ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd049-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd049-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="fd049-105">Overview</span></span>

<span data-ttu-id="fd049-106">يُشير مصطلح *مربع الشراء* عادةً إلى منطقة صفحة تفاصيل المنتج التي تكون "فوق المُجلد،" والتي تستضيف كافة المعلومات الأكثر أهمية المطلوبة لإجراء عملية شراء للمنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="fd049-107">(وتكون المنطقة الموجود "فوق المُجلد" مرئية عند تحميل الصفحة للمرة الأولى، بحيث لا يضطر المستخدمون للتمرير لأسفل لعرضها.)</span><span class="sxs-lookup"><span data-stu-id="fd049-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="fd049-108">تُعد الوحدة النمطية لمربع الشراء حاوية خاصة يتم استخدامها لاستضافة كافة الوحدات النمطية التي تظهر في مساحة مربع شراء صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="fd049-109">ويتضمن عنوان URL الخاص بصفحة تفاصيل المنتج مُعرف المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="fd049-110">يتم اشتقاق كافة المعلومات المطلوبة لعرض الوحدة النمطية لمربع الشراء من مُعرف المنتج هذا.</span><span class="sxs-lookup"><span data-stu-id="fd049-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="fd049-111">إذا لم يتم توفير مُعرف منتج، فلن يتم عرض الوحدة النمطية لصندوق الشراء بشكل صحيح في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fd049-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="fd049-112">وبالتالي، لا يمكن استخدام الوحدة النمطية لصندوق الشراء الا في الصفحات التي تتضمن سياق المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="fd049-113">لاستخدامها في صفحة لا تتضمن سياق منتج (على سبيل المثال، صفحة رئيسية أو صفحة تسويق)، يجب القيام بتخصيصات إضافية.</span><span class="sxs-lookup"><span data-stu-id="fd049-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="fd049-114">تعرض الصورة التالية مثالاُ لوحدة نمطيه لمربع شراء في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-114">The following image shows an example of a buy box module on a product details page.</span></span>

![مثال لوحدة نمطية لمربع شراء](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="fd049-116">خصائص الوحدة النمطية لمربع شراء وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="fd049-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="fd049-117">في صفحة تفاصيل المنتج، يتم تقسيم مربع الشراء إلى منطقتين: منطقة الوسائط على اليسار ومنطقة المحتوى على اليمين.</span><span class="sxs-lookup"><span data-stu-id="fd049-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="fd049-118">بشكل افتراضي، نسبة عرض عمود منطقة الوسائط إلى عرض عمود منطقة المحتوى هي 2:1.</span><span class="sxs-lookup"><span data-stu-id="fd049-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="fd049-119">على الأجهزة المحمولة، يتم تكديس المنطقتين، بحيث تظهر منطقة تحت المنطقة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="fd049-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="fd049-120">يمكن استخدام النُسق لتخصيص عرض الأعمدة وترتيب التكديس.</span><span class="sxs-lookup"><span data-stu-id="fd049-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="fd049-121">تعرض الوحدة النمطية لصندوق الشراء العنوان والوصف والسعر والتقييمات الخاصة بأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="fd049-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="fd049-122">وتسمح أيضًا للعملاء بتحديد متغيرات المنتج التي لها سمات منتج مختلفة، مثل الحجم والنمط واللون.</span><span class="sxs-lookup"><span data-stu-id="fd049-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="fd049-123">عند تحديد مُتغير منتج، يتم تحديث الخصائص الأخرى في مربع الشراء (على سبيل المثال، وصف المنتج والصور) لتعكس معلومات المتغير.</span><span class="sxs-lookup"><span data-stu-id="fd049-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="fd049-124">يتم توفير محدد الكمية، بحيث يمكن للعملاء تحديد كمية الأصناف لشرائها.</span><span class="sxs-lookup"><span data-stu-id="fd049-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="fd049-125">يمكن تحديد الكمية القصوى التي يمكن شراؤها في إعدادات الموقع.</span><span class="sxs-lookup"><span data-stu-id="fd049-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="fd049-126">من صندوق الشراء، بإمكان العملاء أيضًا تنفيذ إجراءات مثل إضافة منتج إلى سلة التسوق وإضافة منتج إلى قائمة الأمنيات وتحديد موقع انتقاء.</span><span class="sxs-lookup"><span data-stu-id="fd049-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="fd049-127">يمكن القيام بهذه الإجراءات في منتج أو متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="fd049-128">لإضافة منتج إلى قائمة أمنيات، يجب على العميل تسجيل دخوله.</span><span class="sxs-lookup"><span data-stu-id="fd049-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="fd049-129">يمكن استخدام النُسق لإزالة خصائص منتج صندوق الشراء وعناصر التحكم في الإجراء أو تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="fd049-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="fd049-130">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="fd049-130">Module properties</span></span>

- <span data-ttu-id="fd049-131">**علامة العنوان** – تقوم هذه الخاصية بتعريف علامة العنوان لعنوان المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="fd049-132">إذا كان صندوق الشراء في أعلى الصفحة، فيجب تعيين هذه الخاصية إلى **h1** لتلبيه معايير إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="fd049-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

- <span data-ttu-id="fd049-133">**تمكين توصيات "تسوق أشكال مماثلة"‬** - تسمح هذه الخاصية لمربع الشراء بإظهار ارتباطات إلى منتجات تبدو مماثلة للصنف المعروض حاليًا.</span><span class="sxs-lookup"><span data-stu-id="fd049-133">**Enable "shop similar looks" recommendations** - This property allows the buy box to show links to products that look similar to the currently viewed item.</span></span> <span data-ttu-id="fd049-134">تتوفر هذه الميزة في الإصدار 10.0.13 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="fd049-134">This feature is available in Commerce release 10.0.13 and later.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="fd049-135">الوحدات التي يُمكن استخدامها في وحدة مربع الشراء</span><span class="sxs-lookup"><span data-stu-id="fd049-135">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="fd049-136">**معرض الوسائط** - تستخدم هذه الوحدة النمطية لإظهار صور أحد المنتجات في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-136">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="fd049-137">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لمعرض الوسائط‬](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="fd049-137">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="fd049-138">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="fd049-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="fd049-139">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="fd049-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="fd049-140">لمزيد من المعلومات حول هذه الوحدة النمطية، راجع [الوحدة النمطية لمحدد المتجر‬](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="fd049-140">For more information about this module, see [Store selector module](store-selector.md).</span></span>
- <span data-ttu-id="fd049-141">**المشاركة الاجتماعية** - يمكن إضافة هذه الوحدة إلى مربع الشراء للسماح للمستخدمين بمشاركة معلومات المنتج على وسائل التواصل الاجتماعي.</span><span class="sxs-lookup"><span data-stu-id="fd049-141">**Social share** - This module can be added to the buy box to allow users to share product information on social media.</span></span> <span data-ttu-id="fd049-142">لمزيد من المعلومات، راجع‏‎ [وحدة المشاركة الاجتماعية](social-share-module.md).</span><span class="sxs-lookup"><span data-stu-id="fd049-142">For more information, see [Social share module](social-share-module.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="fd049-143">إعدادات الوحدة النمطية لمربع الشراء</span><span class="sxs-lookup"><span data-stu-id="fd049-143">Buy box module settings</span></span>

<span data-ttu-id="fd049-144">يمكن تكوين إعدادات الوحدة النمطية لمربع الشراء في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="fd049-144">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="fd049-145">**الحد الأقصى لبنود عربة التسوق‬‏‫**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="fd049-145">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="fd049-146">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="fd049-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="fd049-147">**المخزون** – لمزيد من المعلومات حول كيفيه تطبيق إعدادات المخزون، راجع  [تطبيق إعدادات المخزون](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="fd049-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="fd049-148">**إضافة إلى عربة التسويق** - تستخدم هذه الخاصية لتحديد السلوك بعد إضافة صنف إلى عربة التسوق.</span><span class="sxs-lookup"><span data-stu-id="fd049-148">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="fd049-149">القيم المحتملة هي **الانتقال إلى عربة التسوق** و**الانتقال إلى عربة التسوق** و**إظهار الإعلامات**.</span><span class="sxs-lookup"><span data-stu-id="fd049-149">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="fd049-150">عند تعيين القيمة إلى **الانتقال إلى عربة التسوق**، يتم إرسال المستخدمين إلى صفحة عربة التسوق بعد إضافة صنف.</span><span class="sxs-lookup"><span data-stu-id="fd049-150">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="fd049-151">عند تعيين القيمة إلى **عدم الانتقال إلى عربة التسوق**، لا يتم إرسال المستخدمين إلى صفحة عربة التسوق بعد إضافة صنف.</span><span class="sxs-lookup"><span data-stu-id="fd049-151">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="fd049-152">عند تعيين القيمة إلى **إظهار الاعلامات**، يظهر إعلام تأكيد للمستخدمين ويمكنهم متابعة الاستعراض في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-152">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="fd049-153">تتوفر إعدادات **إضافة إلى سلة التسوق** في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="fd049-153">The **Add to cart** site settings are available in the Dynamics 365 Commerce 10.0.11 release.</span></span> <span data-ttu-id="fd049-154">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="fd049-154">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="fd049-155">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="fd049-155">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

<span data-ttu-id="fd049-156">تعرض الصورة التالية مثالاً لإعلام التأكيد "تمت الإضافة إلى عربة التسوق" في موقع شركه Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="fd049-156">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

![مثال عن وحدة نمطية للإعلام](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="fd049-158">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="fd049-158">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="fd049-159">تسترد الوحدة النمطية لصندوق الشراء معلومات المنتج باستخدام واجهات برمجة التطبيقات (API) لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="fd049-159">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="fd049-160">يتم استخدام مُعرف المنتج من صفحة تفاصيل المنتج لاسترداد كافة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="fd049-160">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="fd049-161">إضافة وحدة لمربع شراء إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="fd049-161">Add a buy box module to a page</span></span>

<span data-ttu-id="fd049-162">لإضافة الوحدة النمطية لمربع الشراء إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="fd049-162">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fd049-163">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="fd049-163">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="fd049-164">في مربع الحوار **جزء جديد**، حدد وحدة **مربع الشراء‬**.</span><span class="sxs-lookup"><span data-stu-id="fd049-164">In the **New fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="fd049-165">ضمن **اسم الجزء**، أدخل الاسم **جزء مربع الشراء**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-165">Under **Fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-166">في فتحة **معرض الوسائط** للوحدة النمطية لصندوق الشراء، حدد علامة القطع (**...**), ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="fd049-166">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fd049-167">في مربع الحوار **إضافة وحدة**، حدد الوحدة النمطية **معرض الوسائط**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-167">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-168">في فتحة **محدد المتجر** للوحدة النمطية لصندوق الشراء، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="fd049-168">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fd049-169">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**محدد المتجر‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-169">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-170">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="fd049-170">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="fd049-171">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="fd049-171">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="fd049-172">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب ‎PDP**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-172">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-173">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="fd049-173">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fd049-174">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-174">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-175">في الفتحة **الرئيسية** للصفحة الافتراضية، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="fd049-175">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="fd049-176">في مربع الحوار **تحديد جزء‬‏‫**، حدد **جزء مربع الشراء** الذي أنشأته في وقت سابق، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-176">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-177">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="fd049-177">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="fd049-178">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="fd049-178">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="fd049-179">في مربع الحوار **اختيار قالب**، حدد **قالب PDP**.</span><span class="sxs-lookup"><span data-stu-id="fd049-179">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="fd049-180">ضمن **اسم الصفحة**، أدخل **صفحة PDP**، ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="fd049-180">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-181">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="fd049-181">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="fd049-182">في مربع الحوار **تحديد جزء‬‏‫**، حدد **جزء مربع الشراء** الذي أنشأته في وقت سابق، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fd049-182">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="fd049-183">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="fd049-183">Save and preview the page.</span></span> <span data-ttu-id="fd049-184">أضف مُعلمة سلسلة استعلام **?productid=&lt;product id&gt;** إلى عنوان URL الخاص بصفحة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="fd049-184">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="fd049-185">وبهذه الطريقة، يتم استخدام سياق المنتج لتحميل وعرض صفحة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="fd049-185">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="fd049-186">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="fd049-186">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="fd049-187">يجب أن يظهر مُربع الشراء في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="fd049-187">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd049-188">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fd049-188">Additional resources</span></span>

[<span data-ttu-id="fd049-189">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="fd049-189">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fd049-190">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="fd049-190">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="fd049-191">الوحدة النمطية لمعرض الوسائط</span><span class="sxs-lookup"><span data-stu-id="fd049-191">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="fd049-192">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="fd049-192">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fd049-193">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="fd049-193">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fd049-194">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="fd049-194">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fd049-195">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="fd049-195">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fd049-196">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="fd049-196">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fd049-197">وحدة التذييلات‬</span><span class="sxs-lookup"><span data-stu-id="fd049-197">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="fd049-198">الوحدة النمطية للمشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="fd049-198">Social share module</span></span>](social-share-module.md)

[<span data-ttu-id="fd049-199">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="fd049-199">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="fd049-200">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="fd049-200">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
