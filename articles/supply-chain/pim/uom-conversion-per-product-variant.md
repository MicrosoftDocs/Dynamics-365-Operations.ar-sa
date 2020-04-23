---
title: تحويل وحدة القياس لكل متغير منتج
description: يشرح هذا الموضوع كيفية إعداد تحويلات وحدات القياس على متغيرات المنتج.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204483"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="543a1-103">تحويل وحدة القياس لكل متغير منتج</span><span class="sxs-lookup"><span data-stu-id="543a1-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="543a1-104">يشرح هذا الموضوع كيفية إعداد تحويلات وحدات القياس على متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="543a1-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="543a1-105">يتضمن مثالاً عن الإعداد.</span><span class="sxs-lookup"><span data-stu-id="543a1-105">It includes an example of the setup.</span></span>

<span data-ttu-id="543a1-106">هذه الميزة تسمح للشركات بتحديد تحويل وحدات مختلفة بين متغيرات من المنتج نفسه.</span><span class="sxs-lookup"><span data-stu-id="543a1-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="543a1-107">تم استخدام المثال التالي في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="543a1-107">The following example is used in this topic.</span></span> <span data-ttu-id="543a1-108">تبيع شركة قمصان بمقاسات صغيرة ومتوسطة وكبيرة وكبيرة جدًا.</span><span class="sxs-lookup"><span data-stu-id="543a1-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="543a1-109">تم تحديد القميص على أنه منتج، وتم تحديد المقاسات المختلفة على أنها متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="543a1-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="543a1-110">تمت تعبئة القمصان في صناديق حيث يتسع كل صندوق لخمسة قمصان، باستثناء المقاس الكبير جدًا حيث يتسع الصندوق لأربعة قمصان فقط.</span><span class="sxs-lookup"><span data-stu-id="543a1-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="543a1-111">تريد الشركة تعقب المتغيرات المختلفة للقمصان في وحدة **القطع** ولكنها تبيع القمصان في وحدة **الصناديق**.</span><span class="sxs-lookup"><span data-stu-id="543a1-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="543a1-112">التحويل بين وحدة المخزون ووحدة المبيعات هي 1 صندوق = 5 قطع، باستثناء متغير الحجم الكبير جدًا، حيث 1 صندوق = 4 قطع.</span><span class="sxs-lookup"><span data-stu-id="543a1-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="543a1-113">إعداد منتج لتحويل الوحدة لكل متغير</span><span class="sxs-lookup"><span data-stu-id="543a1-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="543a1-114">يمكن إنشاء متغيرات المنتج فقط للمنتجات من **النوع الفرعي للمنتج**: **أصل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="543a1-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="543a1-115">لمزيد من المعلومات، راجع [إنشاء أصل منتج](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="543a1-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="543a1-116">لم يتم تمكين هذه الميزة للمنتجات التي تم إعدادها لعمليات "وزن التعبئة".</span><span class="sxs-lookup"><span data-stu-id="543a1-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="543a1-117">عند إنشاء أصل المنتج مع متغيرات المنتجات الصادرة، يمكن إعداد تحويلات الوحدات للمتغيرات.</span><span class="sxs-lookup"><span data-stu-id="543a1-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="543a1-118">يمكنك العثور على عنصر القائمة لفتح صفحة تحويل الوحدة في سياق منتج أو متغير المنتج في الصفحات التالية.</span><span class="sxs-lookup"><span data-stu-id="543a1-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="543a1-119">صفحة **تفاصيل المنتج‬**</span><span class="sxs-lookup"><span data-stu-id="543a1-119">**Product details** page</span></span>
-   <span data-ttu-id="543a1-120">صفحة **تفاصيل المنتجات الصادرة**</span><span class="sxs-lookup"><span data-stu-id="543a1-120">**Released products details** page</span></span>
-   <span data-ttu-id="543a1-121">صفحة **متغيرات المنتجات الصادرة**</span><span class="sxs-lookup"><span data-stu-id="543a1-121">**Released product variants** page</span></span>

<span data-ttu-id="543a1-122">عندما تفتح صفحة **تحويل الوحدة** في سياق أصل منتج أو متغير منتج صادر، يمكنك تحديد إن كنت تريد إعداد تحويل الوحدات للمنتج أو لمتغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="543a1-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="543a1-123">يمكنك القيام بذلك بتحديد **متغير المنتج** أو **المنتج** في الحقل **إنشاء تحويل لـ‬**.</span><span class="sxs-lookup"><span data-stu-id="543a1-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="543a1-124">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="543a1-124">Product variant</span></span>

<span data-ttu-id="543a1-125">إذا حددت **متغير المنتج،** فيمكنك تحديد المتغير الذي تريد إعداد تحويل الوحدة له في الحقل **متغير المنتج**.</span><span class="sxs-lookup"><span data-stu-id="543a1-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="543a1-126">منتج</span><span class="sxs-lookup"><span data-stu-id="543a1-126">Product</span></span>

<span data-ttu-id="543a1-127">إذا حددت **المنتج**، فيمكنك إعداد تحويل الوحدة لأصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="543a1-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="543a1-128">سيتم تطبيق تحويل الوحدة هذا على جميع متغيرات المنتج التي ليس لم يتم تحديد تحويل وحدة لها.</span><span class="sxs-lookup"><span data-stu-id="543a1-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="543a1-129">مثال</span><span class="sxs-lookup"><span data-stu-id="543a1-129">Example</span></span>

<span data-ttu-id="543a1-130">يتضمن أصل المنتج، **قميص**، أربعة متغيرات منتجات صادرة وهي صغير ومتوسط وكبير وكبير جدًا.</span><span class="sxs-lookup"><span data-stu-id="543a1-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="543a1-131">تمت تعبئة القمصان في صناديق حيث يتسع كل صندوق لخمسة قمصان، باستثناء المقاس الكبير جدًا حيث يتسع الصندوق لأربعة قمصان فقط.</span><span class="sxs-lookup"><span data-stu-id="543a1-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="543a1-132">أولاً، افتح صفحة **تحويل الوحدة** من صفحة "تفاصيل المنتجات الصادرة لأصل المنتج **قميص.**</span><span class="sxs-lookup"><span data-stu-id="543a1-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="543a1-133">في صفحة **تحويل الوحدة**، قم بإعداد تحويل الوحدة لمتغير المنتج المقاس الكبير جدًا.</span><span class="sxs-lookup"><span data-stu-id="543a1-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="543a1-134">**الحقل**</span><span class="sxs-lookup"><span data-stu-id="543a1-134">**Field**</span></span>             | <span data-ttu-id="543a1-135">**إعداد**</span><span class="sxs-lookup"><span data-stu-id="543a1-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="543a1-136">إنشاء تحويل لـ</span><span class="sxs-lookup"><span data-stu-id="543a1-136">Create conversion for</span></span> | <span data-ttu-id="543a1-137">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="543a1-137">Product variant</span></span>         |
| <span data-ttu-id="543a1-138">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="543a1-138">Product variant</span></span>       | <span data-ttu-id="543a1-139">قميص : : كبير جدًا : :</span><span class="sxs-lookup"><span data-stu-id="543a1-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="543a1-140">من وحدة</span><span class="sxs-lookup"><span data-stu-id="543a1-140">From unit</span></span>             | <span data-ttu-id="543a1-141">صناديق</span><span class="sxs-lookup"><span data-stu-id="543a1-141">Boxes</span></span>                   |
| <span data-ttu-id="543a1-142">عامل</span><span class="sxs-lookup"><span data-stu-id="543a1-142">Factor</span></span>                | <span data-ttu-id="543a1-143">4</span><span class="sxs-lookup"><span data-stu-id="543a1-143">4</span></span>                       |
| <span data-ttu-id="543a1-144">إلى وحدة</span><span class="sxs-lookup"><span data-stu-id="543a1-144">To Unit</span></span>               | <span data-ttu-id="543a1-145">القطع</span><span class="sxs-lookup"><span data-stu-id="543a1-145">Pieces</span></span>                  |

<span data-ttu-id="543a1-146">متغيرات المنتجات الصادرة وهي صغير ومتوسط وكبير لديها تحويل الوحدة نفسه بين وحدة الصناديق والقطع، مما يعني أنه يمكنك تحديد تحويل الوحدة لمتغيرات المنتجات هذه على أصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="543a1-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="543a1-147">**الحقل**</span><span class="sxs-lookup"><span data-stu-id="543a1-147">**Field**</span></span>             | <span data-ttu-id="543a1-148">**إعداد**</span><span class="sxs-lookup"><span data-stu-id="543a1-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="543a1-149">إنشاء تحويل لـ</span><span class="sxs-lookup"><span data-stu-id="543a1-149">Create conversion for</span></span> | <span data-ttu-id="543a1-150">منتج</span><span class="sxs-lookup"><span data-stu-id="543a1-150">Product</span></span>     |
| <span data-ttu-id="543a1-151">منتج</span><span class="sxs-lookup"><span data-stu-id="543a1-151">Product</span></span>               | <span data-ttu-id="543a1-152">قميص</span><span class="sxs-lookup"><span data-stu-id="543a1-152">T-Shirt</span></span>     |
| <span data-ttu-id="543a1-153">من وحدة</span><span class="sxs-lookup"><span data-stu-id="543a1-153">From unit</span></span>             | <span data-ttu-id="543a1-154">صناديق</span><span class="sxs-lookup"><span data-stu-id="543a1-154">Boxes</span></span>       |
| <span data-ttu-id="543a1-155">عامل</span><span class="sxs-lookup"><span data-stu-id="543a1-155">Factor</span></span>                | <span data-ttu-id="543a1-156">5</span><span class="sxs-lookup"><span data-stu-id="543a1-156">5</span></span>           |
| <span data-ttu-id="543a1-157">إلى وحدة</span><span class="sxs-lookup"><span data-stu-id="543a1-157">To Unit</span></span>               | <span data-ttu-id="543a1-158">القطع</span><span class="sxs-lookup"><span data-stu-id="543a1-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="543a1-159">استخدام Excel لتحديث تحويلات الوحدات</span><span class="sxs-lookup"><span data-stu-id="543a1-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="543a1-160">إذا تضمن أحد المنتجات الكثير من متغيرات المنتجات مع تحويلات وحدات مختلفة، فمن المستحسن تصدير تحويلات الوحدات من صفحة **تحويل الوحدة** إلى جدول بيانات Excel، وتحديث التحويلات، ثم إعادة نشرها في Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="543a1-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="543a1-161">يمكن تمكين خيار التصدير إلى Excel وإعادة نشر عمليات التحرير في Supply Chain Mangement من عنصر القائمة **فتح في Microsoft Office** في "جزء الإجراءات" في صفحة  **تحويل الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="543a1-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
