---
title: الوحدة النمطية لمربع شراء
description: يتناول هذا الموضوع وحدات مربع الشراء ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 35b7027e0f0b680dd82ebfcea754fef1617c0163
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261388"
---
# <a name="buy-box-module"></a><span data-ttu-id="8df9f-103">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="8df9f-103">Buy box module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8df9f-104">يتناول هذا الموضوع وحدات مربع الشراء ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8df9f-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8df9f-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8df9f-105">Overview</span></span>

<span data-ttu-id="8df9f-106">يُشير مصطلح *مربع الشراء* عادةً إلى منطقة صفحة تفاصيل المنتج التي تكون "فوق المُجلد،" والتي تستضيف كافة المعلومات الأكثر أهمية المطلوبة لإجراء عملية شراء للمنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="8df9f-107">(وتكون المنطقة الموجود "فوق المُجلد" مرئية عند تحميل الصفحة للمرة الأولى، بحيث لا يضطر المستخدمون للتمرير لأسفل لعرضها.)</span><span class="sxs-lookup"><span data-stu-id="8df9f-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="8df9f-108">تُعد الوحدة النمطية لمربع الشراء حاوية خاصة يتم استخدامها لاستضافة كافة الوحدات النمطية التي تظهر في مساحة مربع شراء صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="8df9f-109">ويتضمن عنوان URL الخاص بصفحة تفاصيل المنتج مُعرف المنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="8df9f-110">يتم اشتقاق كافة المعلومات المطلوبة لعرض الوحدة النمطية لمربع الشراء من مُعرف المنتج هذا.</span><span class="sxs-lookup"><span data-stu-id="8df9f-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="8df9f-111">إذا لم يتم توفير مُعرف منتج، فلن يتم عرض الوحدة النمطية لصندوق الشراء بشكل صحيح في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8df9f-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="8df9f-112">وبالتالي، لا يمكن استخدام الوحدة النمطية لصندوق الشراء الا في الصفحات التي تتضمن سياق المنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="8df9f-113">لاستخدامها في صفحة لا تتضمن سياق منتج (على سبيل المثال، صفحة رئيسية أو صفحة تسويق)، يجب القيام بتخصيصات إضافية.</span><span class="sxs-lookup"><span data-stu-id="8df9f-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="8df9f-114">خصائص الوحدة النمطية لمربع شراء وفتحات التشغيل</span><span class="sxs-lookup"><span data-stu-id="8df9f-114">Buy box module properties and slots</span></span> 

<span data-ttu-id="8df9f-115">في صفحة تفاصيل المنتج، يتم تقسيم مربع الشراء إلى منطقتين: منطقة الوسائط على اليسار ومنطقة المحتوى على اليمين.</span><span class="sxs-lookup"><span data-stu-id="8df9f-115">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="8df9f-116">بشكل افتراضي، نسبة عرض عمود منطقة الوسائط إلى عرض عمود منطقة المحتوى هي 2:1.</span><span class="sxs-lookup"><span data-stu-id="8df9f-116">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="8df9f-117">على الأجهزة المحمولة، يتم تكديس المنطقتين، بحيث تظهر منطقة تحت المنطقة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="8df9f-117">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="8df9f-118">يمكن استخدام النُسق لتخصيص عرض الأعمدة وترتيب التكديس.</span><span class="sxs-lookup"><span data-stu-id="8df9f-118">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="8df9f-119">تعرض الوحدة النمطية لصندوق الشراء العنوان والوصف والسعر والتقييمات الخاصة بأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="8df9f-119">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="8df9f-120">وتسمح أيضًا للعملاء بتحديد متغيرات المنتج التي لها سمات منتج مختلفة، مثل الحجم والنمط واللون.</span><span class="sxs-lookup"><span data-stu-id="8df9f-120">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="8df9f-121">عند تحديد مُتغير منتج، يتم تحديث الخصائص الأخرى في مربع الشراء (على سبيل المثال، وصف المنتج والصور) لتعكس معلومات المتغير.</span><span class="sxs-lookup"><span data-stu-id="8df9f-121">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="8df9f-122">يتم توفير محدد الكمية، بحيث يمكن للعملاء تحديد كمية الأصناف لشرائها.</span><span class="sxs-lookup"><span data-stu-id="8df9f-122">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="8df9f-123">يمكن تحديد الكمية القصوى التي يمكن شراؤها في إعدادات الموقع.</span><span class="sxs-lookup"><span data-stu-id="8df9f-123">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="8df9f-124">من صندوق الشراء، بإمكان العملاء أيضًا تنفيذ إجراءات مثل إضافة منتج إلى سلة التسوق وإضافة منتج إلى قائمة الأمنيات وتحديد موقع انتقاء.</span><span class="sxs-lookup"><span data-stu-id="8df9f-124">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="8df9f-125">يمكن القيام بهذه الإجراءات في منتج أو متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-125">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="8df9f-126">لإضافة منتج إلى قائمة أمنيات، يجب على العميل تسجيل دخوله.</span><span class="sxs-lookup"><span data-stu-id="8df9f-126">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="8df9f-127">يمكن استخدام النُسق لإزالة خصائص منتج صندوق الشراء وعناصر التحكم في الإجراء أو تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="8df9f-127">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="8df9f-128">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="8df9f-128">Module properties</span></span>

- <span data-ttu-id="8df9f-129">**علامة العنوان** – تقوم هذه الخاصية بتعريف علامة العنوان لعنوان المنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-129">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="8df9f-130">إذا كان صندوق الشراء في أعلى الصفحة، فيجب تعيين هذه الخاصية إلى **h1** لتلبيه معايير إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="8df9f-130">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="8df9f-131">الوحدات التي يُمكن استخدامها في وحدة مربع الشراء</span><span class="sxs-lookup"><span data-stu-id="8df9f-131">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="8df9f-132">**معرض الوسائط** - تستخدم هذه الوحدة النمطية لإظهار صور أحد المنتجات في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-132">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="8df9f-133">يُمكن أن يدعم صورة واحدة وحتى العديد من الصور.</span><span class="sxs-lookup"><span data-stu-id="8df9f-133">It can support one to many images.</span></span> <span data-ttu-id="8df9f-134">وهي تدعم أيضًا الصور المُصغرة.</span><span class="sxs-lookup"><span data-stu-id="8df9f-134">It also supports thumbnail images.</span></span> <span data-ttu-id="8df9f-135">يُمكن ترتيب الصور المُصغرة إما أفقيًا (كصف أسفل الصورة) أو عموديًا (كعمود بجانب الصورة).</span><span class="sxs-lookup"><span data-stu-id="8df9f-135">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="8df9f-136">يُمكن إضافة الوحدة النمطية لمعرض الوسائط إلى فتحة **الوسائط** في الوحدة النمطية لصندوق الشراء.</span><span class="sxs-lookup"><span data-stu-id="8df9f-136">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="8df9f-137">وهي تدعم حاليًا الصور فقط.</span><span class="sxs-lookup"><span data-stu-id="8df9f-137">It currently supports only images.</span></span> 
- <span data-ttu-id="8df9f-138">**محدد المتجر**- تعرض هذه الوحدة قائمة بالمتاجر القريبة المتاح فيها الصنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="8df9f-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="8df9f-139">وهو يتيح للمستخدمين إدخال موقع للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="8df9f-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="8df9f-140">لمزيد من المعلومات حول هذه الوحدة، راجع [وحدة محدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="8df9f-140">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="8df9f-141">إعدادات الوحدة النمطية لمربع الشراء</span><span class="sxs-lookup"><span data-stu-id="8df9f-141">Buy box module settings</span></span>

<span data-ttu-id="8df9f-142">تتضمن وحدات صندوق الشراء ثلاثة إعدادات يمكن تكوينها في **إعدادات الموقع \> الملحقات**:</span><span class="sxs-lookup"><span data-stu-id="8df9f-142">Buy box modules have three settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="8df9f-143">**الحد الأقصى للكمية**- تُستخدم هذه لخاصية لتحديد العدد الأقصى لكل صنف يُمكن إضافته إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="8df9f-143">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="8df9f-144">على سبيل المثال، يُمكن لبائع التجزئة أن يُقرر إمكانية بيع 10 فقط من كل منتج في حركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="8df9f-144">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="8df9f-145">**فحص المخزون**- عندما يتم تعيين القيمة إلى **صحيح**، تتم إضافة عنصر إلى سلة التسوق فقط بعد تأكد وحدة مُربع الشراء من وجودها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="8df9f-145">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="8df9f-146">يتم إجراء فحص المخزون للسيناريوهات التي سوف يتم فيها شحن الصنف وللسيناريوهات التي سوف يتم فيها انتقاؤها في المتجر.</span><span class="sxs-lookup"><span data-stu-id="8df9f-146">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="8df9f-147">إذا تم تعيين القيمة إلى **خطأ**، فلن يتم إجراء فحص المخزون قبل إضافة أي صنف إلى سلة التسوق ووضع الأمر.</span><span class="sxs-lookup"><span data-stu-id="8df9f-147">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="8df9f-148">للحصول على معلومات حول كيفية تكوين إعدادات المخزون في المكتب الخلفي ، راجع [حساب توفر المخزون لقنوات البيع بالتجزئة‬](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="8df9f-148">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

- <span data-ttu-id="8df9f-149">**المخزن المؤقت للمخزون‬‏‫** – تُستخدم هذه الخاصية لتحديد رقم المخزن المؤقت للمخزون.</span><span class="sxs-lookup"><span data-stu-id="8df9f-149">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="8df9f-150">يتم الاحتفاظ بالمخزون في الوقت الفعلي، وعندما يقوم العديد من العملاء بوضع الأوامر، قد يكون من الصعب الحفاظ على جرد المخزون الدقيق.</span><span class="sxs-lookup"><span data-stu-id="8df9f-150">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="8df9f-151">وعند إجراء فحص للمخزون، إذا كان المخزون أقل من مبلغ المخزن المؤقت، يتم مُعاملة المنتج على أنه خارج المخزون.</span><span class="sxs-lookup"><span data-stu-id="8df9f-151">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="8df9f-152">وبالتالي، عندما تُجرى المبيعات سريعًا من خلال قنوات متعددة، ولا تتم مزامنة جرد المخزون بالكامل، فمن ثم تقل فرصة خطر بيع صنف غير موجود في المخزون.</span><span class="sxs-lookup"><span data-stu-id="8df9f-152">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="8df9f-153">تفاعل Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="8df9f-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="8df9f-154">تسترد الوحدة النمطية لصندوق الشراء معلومات المنتج باستخدام واجهات API لـ Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="8df9f-154">The buy box module retrieves product information using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="8df9f-155">يتم استخدام مُعرف المنتج من صفحة تفاصيل المنتج لاسترداد كافة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="8df9f-155">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="8df9f-156">إضافة وحدة نمطية لمربع شراء إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="8df9f-156">Add a buy box module to a page</span></span>

<span data-ttu-id="8df9f-157">لإضافة الوحدة النمطية لمربع الشراء إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8df9f-157">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8df9f-158">إنشاء جزء يسمى **جزء مربع الشراء**، وإضافة وحدة نمطية لمربع الشراء إليه.</span><span class="sxs-lookup"><span data-stu-id="8df9f-158">Create a fragment that is named **buy box fragment**, and add a buy box module to it.</span></span>
1. <span data-ttu-id="8df9f-159">في فتحة **الوسائط** في الوحدة النمطية لمربع الشراء، قم بإضافة الوحدة النمطية لمعرض الوسائط.</span><span class="sxs-lookup"><span data-stu-id="8df9f-159">In the **Media** slot of the buy box module, add a media gallery module.</span></span>
1. <span data-ttu-id="8df9f-160">في فتحة **محدد المتجر** في الوحدة النمطية لصندوق الشراء، أضف الوحدة النمطية لمحدد المتجر.</span><span class="sxs-lookup"><span data-stu-id="8df9f-160">In the **Store selector** slot of the buy box module, add a store selector module.</span></span>
1. <span data-ttu-id="8df9f-161">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="8df9f-161">Check in the page, and publish it.</span></span>
1. <span data-ttu-id="8df9f-162">قم بإنشاء قالب لصفحة تفاصيل المنتج، وقم بتسميتها **قالب PDP**.</span><span class="sxs-lookup"><span data-stu-id="8df9f-162">Create a template for a product details page, and name it **PDP template**.</span></span>
1. <span data-ttu-id="8df9f-163">أضف صفحة افتراضية.</span><span class="sxs-lookup"><span data-stu-id="8df9f-163">Add a default page.</span></span>
1. <span data-ttu-id="8df9f-164">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة جزء مربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="8df9f-164">In the **Main** slot of the default page, add a buy box fragment.</span></span>
1. <span data-ttu-id="8df9f-165">احفظ القالب ثم انشره بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="8df9f-165">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="8df9f-166">استخدم القالب الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة PDP**.</span><span class="sxs-lookup"><span data-stu-id="8df9f-166">Use the template that you just created to create a page that is named **PDP page**.</span></span>
1. <span data-ttu-id="8df9f-167">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة جزء مربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="8df9f-167">In the **Main** slot of the new page, add a buy box fragment.</span></span>
1. <span data-ttu-id="8df9f-168">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="8df9f-168">Save and preview the page.</span></span> <span data-ttu-id="8df9f-169">أضف مُعلمة سلسلة استعلام **?productid=&lt;product id&gt;** إلى عنوان URL الخاص بصفحة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="8df9f-169">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="8df9f-170">وبهذه الطريقة، يتم استخدام سياق المنتج لتحميل وعرض صفحة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="8df9f-170">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="8df9f-171">احفظ الصفحة ثم انشرها بعد الانتهاء من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="8df9f-171">Save the page, finish editing it, and publish it.</span></span> <span data-ttu-id="8df9f-172">يجب أن يظهر مُربع الشراء في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="8df9f-172">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8df9f-173">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8df9f-173">Additional resources</span></span>

[<span data-ttu-id="8df9f-174">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="8df9f-174">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8df9f-175">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="8df9f-175">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8df9f-176">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="8df9f-176">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8df9f-177">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="8df9f-177">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8df9f-178">الوحدة النمطية لأيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="8df9f-178">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8df9f-179">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="8df9f-179">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8df9f-180">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="8df9f-180">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8df9f-181">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="8df9f-181">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8df9f-182">الوحدة النمطية للتذييلات‬</span><span class="sxs-lookup"><span data-stu-id="8df9f-182">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="8df9f-183">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8df9f-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
