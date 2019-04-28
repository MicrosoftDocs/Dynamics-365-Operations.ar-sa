---
title: تحويل وحدة القياس لكل متغير منتج
description: يشرح هذا الموضوع كيفية إعداد تحويلات وحدات القياس على متغيرات المنتج.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: a47f705976b7a5b34492294e28aa8cd47ea38825
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/22/2019
ms.locfileid: "345917"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="3ca60-103">تحويل وحدة القياس لكل متغير منتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="3ca60-104">يشرح هذا الموضوع كيفية إعداد تحويلات وحدات القياس على متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="3ca60-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="3ca60-105">يتضمن مثالاً عن الإعداد.</span><span class="sxs-lookup"><span data-stu-id="3ca60-105">It includes an example of the setup.</span></span>

<span data-ttu-id="3ca60-106">هذه الميزة تسمح للشركات بتحديد تحويل وحدات مختلفة بين متغيرات من المنتج نفسه.</span><span class="sxs-lookup"><span data-stu-id="3ca60-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="3ca60-107">تم استخدام المثال التالي في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="3ca60-107">The following example is used in this topic.</span></span> <span data-ttu-id="3ca60-108">تبيع شركة قمصان بمقاسات صغيرة ومتوسطة وكبيرة وكبيرة جدًا.</span><span class="sxs-lookup"><span data-stu-id="3ca60-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="3ca60-109">تم تحديد القميص على أنه منتج، وتم تحديد المقاسات المختلفة على أنها متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="3ca60-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="3ca60-110">تمت تعبئة القمصان في صناديق حيث يتسع كل صندوق لخمسة قمصان، باستثناء المقاس الكبير جدًا حيث يتسع الصندوق لأربعة قمصان فقط.</span><span class="sxs-lookup"><span data-stu-id="3ca60-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="3ca60-111">تريد الشركة تعقب المتغيرات المختلفة للقمصان في وحدة **القطع** ولكنها تبيع القمصان في وحدة **الصناديق**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="3ca60-112">التحويل بين وحدة المخزون ووحدة المبيعات هي 1 صندوق = 5 قطع، باستثناء متغير الحجم الكبير جدًا، حيث 1 صندوق = 4 قطع.</span><span class="sxs-lookup"><span data-stu-id="3ca60-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="3ca60-113">الإعداد</span><span class="sxs-lookup"><span data-stu-id="3ca60-113">Setup</span></span>

<span data-ttu-id="3ca60-114">يمكنك تكوين المعلمات لاستخدام الميزة للمنتجات التي تم تمكينها من أجل **كافة عمليات** أو فقط للمنتج الذي تم تمكينه من أجل **عمليات المستودع** باستخدام الخيار **تمكين تحويلات وحدة القياس‬** في صفحة **معلمات معلومات المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="3ca60-115">إعداد منتج لتحويل الوحدة لكل متغير</span><span class="sxs-lookup"><span data-stu-id="3ca60-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="3ca60-116">يمكن إنشاء متغيرات المنتج فقط للمنتجات من **النوع الفرعي للمنتج**: **أصل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="3ca60-117">لمزيد من المعلومات، راجع [إنشاء أصل منتج](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="3ca60-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="3ca60-118">لم يتم تمكين هذه الميزة للمنتجات التي تم إعدادها لعمليات "وزن التعبئة".</span><span class="sxs-lookup"><span data-stu-id="3ca60-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="3ca60-119">أثناء إنشاء أصل منتج، اعمل على تمكين تحويل وحدة القياس باستخدام الخيار **‏‫تمكين تحويلات وحدة القياس‬** في صفحة **تفاصيل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="3ca60-120">عند إنشاء أصل المنتج مع متغيرات المنتجات الصادرة، يمكن إعداد تحويلات الوحدات للمتغيرات.</span><span class="sxs-lookup"><span data-stu-id="3ca60-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="3ca60-121">يمكنك العثور على عنصر القائمة لفتح صفحة تحويل الوحدة في سياق منتج أو متغير المنتج في الصفحات التالية.</span><span class="sxs-lookup"><span data-stu-id="3ca60-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="3ca60-122">صفحة **تفاصيل المنتج‬**</span><span class="sxs-lookup"><span data-stu-id="3ca60-122">**Product details** page</span></span>
-   <span data-ttu-id="3ca60-123">صفحة **تفاصيل المنتجات الصادرة**</span><span class="sxs-lookup"><span data-stu-id="3ca60-123">**Released products details** page</span></span>
-   <span data-ttu-id="3ca60-124">صفحة **متغيرات المنتجات الصادرة**</span><span class="sxs-lookup"><span data-stu-id="3ca60-124">**Released product variants** page</span></span>

<span data-ttu-id="3ca60-125">عندما تفتح صفحة **تحويل الوحدة** في سياق أصل منتج أو متغير منتج صادر، يمكنك تحديد إن كنت تريد إعداد تحويل الوحدات للمنتج أو لمتغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="3ca60-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="3ca60-126">يمكنك القيام بذلك بتحديد **متغير المنتج** أو **المنتج** في الحقل **إنشاء تحويل لـ‬**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="3ca60-127">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-127">Product variant</span></span>

<span data-ttu-id="3ca60-128">إذا حددت **متغير المنتج،** فيمكنك تحديد المتغير الذي تريد إعداد تحويل الوحدة له في الحقل **متغير المنتج**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="3ca60-129">منتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-129">Product</span></span>

<span data-ttu-id="3ca60-130">إذا حددت **المنتج**، فيمكنك إعداد تحويل الوحدة لأصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="3ca60-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="3ca60-131">سيتم تطبيق تحويل الوحدة هذا على جميع متغيرات المنتج التي ليس لم يتم تحديد تحويل وحدة لها.</span><span class="sxs-lookup"><span data-stu-id="3ca60-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="3ca60-132">مثال</span><span class="sxs-lookup"><span data-stu-id="3ca60-132">Example</span></span>

<span data-ttu-id="3ca60-133">يتضمن أصل المنتج، **قميص**، أربعة متغيرات منتجات صادرة وهي صغير ومتوسط وكبير وكبير جدًا.</span><span class="sxs-lookup"><span data-stu-id="3ca60-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="3ca60-134">تمت تعبئة القمصان في صناديق حيث يتسع كل صندوق لخمسة قمصان، باستثناء المقاس الكبير جدًا حيث يتسع الصندوق لأربعة قمصان فقط.</span><span class="sxs-lookup"><span data-stu-id="3ca60-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="3ca60-135">أولاً، افتح صفحة **تحويل الوحدة** من صفحة "تفاصيل المنتجات الصادرة لأصل المنتج **قميص.**</span><span class="sxs-lookup"><span data-stu-id="3ca60-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="3ca60-136">في صفحة **تحويل الوحدة**، قم بإعداد تحويل الوحدة لمتغير المنتج المقاس الكبير جدًا.</span><span class="sxs-lookup"><span data-stu-id="3ca60-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="3ca60-137">**الحقل**</span><span class="sxs-lookup"><span data-stu-id="3ca60-137">**Field**</span></span>             | <span data-ttu-id="3ca60-138">**إعداد**</span><span class="sxs-lookup"><span data-stu-id="3ca60-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="3ca60-139">إنشاء تحويل لـ</span><span class="sxs-lookup"><span data-stu-id="3ca60-139">Create conversion for</span></span> | <span data-ttu-id="3ca60-140">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-140">Product variant</span></span>         |
| <span data-ttu-id="3ca60-141">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-141">Product variant</span></span>       | <span data-ttu-id="3ca60-142">قميص : : كبير جدًا : :</span><span class="sxs-lookup"><span data-stu-id="3ca60-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="3ca60-143">من وحدة</span><span class="sxs-lookup"><span data-stu-id="3ca60-143">From unit</span></span>             | <span data-ttu-id="3ca60-144">صناديق</span><span class="sxs-lookup"><span data-stu-id="3ca60-144">Boxes</span></span>                   |
| <span data-ttu-id="3ca60-145">عامل</span><span class="sxs-lookup"><span data-stu-id="3ca60-145">Factor</span></span>                | <span data-ttu-id="3ca60-146">4</span><span class="sxs-lookup"><span data-stu-id="3ca60-146">4</span></span>                       |
| <span data-ttu-id="3ca60-147">إلى وحدة</span><span class="sxs-lookup"><span data-stu-id="3ca60-147">To Unit</span></span>               | <span data-ttu-id="3ca60-148">القطع</span><span class="sxs-lookup"><span data-stu-id="3ca60-148">Pieces</span></span>                  |

<span data-ttu-id="3ca60-149">متغيرات المنتجات الصادرة وهي صغير ومتوسط وكبير لديها تحويل الوحدة نفسه بين وحدة الصناديق والقطع، مما يعني أنه يمكنك تحديد تحويل الوحدة لمتغيرات المنتجات هذه على أصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="3ca60-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="3ca60-150">**الحقل**</span><span class="sxs-lookup"><span data-stu-id="3ca60-150">**Field**</span></span>             | <span data-ttu-id="3ca60-151">**إعداد**</span><span class="sxs-lookup"><span data-stu-id="3ca60-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="3ca60-152">إنشاء تحويل لـ</span><span class="sxs-lookup"><span data-stu-id="3ca60-152">Create conversion for</span></span> | <span data-ttu-id="3ca60-153">منتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-153">Product</span></span>     |
| <span data-ttu-id="3ca60-154">منتج</span><span class="sxs-lookup"><span data-stu-id="3ca60-154">Product</span></span>               | <span data-ttu-id="3ca60-155">قميص</span><span class="sxs-lookup"><span data-stu-id="3ca60-155">T-Shirt</span></span>     |
| <span data-ttu-id="3ca60-156">من وحدة</span><span class="sxs-lookup"><span data-stu-id="3ca60-156">From unit</span></span>             | <span data-ttu-id="3ca60-157">صناديق</span><span class="sxs-lookup"><span data-stu-id="3ca60-157">Boxes</span></span>       |
| <span data-ttu-id="3ca60-158">عامل</span><span class="sxs-lookup"><span data-stu-id="3ca60-158">Factor</span></span>                | <span data-ttu-id="3ca60-159">5</span><span class="sxs-lookup"><span data-stu-id="3ca60-159">5</span></span>           |
| <span data-ttu-id="3ca60-160">إلى وحدة</span><span class="sxs-lookup"><span data-stu-id="3ca60-160">To Unit</span></span>               | <span data-ttu-id="3ca60-161">القطع</span><span class="sxs-lookup"><span data-stu-id="3ca60-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="3ca60-162">استخدام Excel لتحديث تحويلات الوحدات</span><span class="sxs-lookup"><span data-stu-id="3ca60-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="3ca60-163">إذا تضمن أحد المنتجات الكثير من متغيرات المنتجات مع تحويلات وحدات مختلفة، فمن المستحسن تصدير تحويلات الوحدات من صفحة **تحويل الوحدة** إلى جدول بيانات Excel، وتحديث التحويلات، ثم إعادة نشرها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3ca60-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="3ca60-164">يمكن تمكين خيار التصدير إلى Excel وإعادة نشر عمليات التحرير في Finance and Operations من عنصر القائمة **فتح في Microsoft Office** في "جزء الإجراءات" في صفحة **تحويل الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="3ca60-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
