---
title: تحويل وحدة القياس لكل متغير منتج
description: يشرح هذا الموضوع كيفية إعداد تحويلات وحدات القياس لمتغيرات المنتج. يتضمن مثالاً عن الإعداد.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5f327d1d0b38ad724da6a302cefc115262317812
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001689"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="790c9-104">تحويل وحدة القياس لكل متغير منتج</span><span class="sxs-lookup"><span data-stu-id="790c9-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="790c9-105">يشرح هذا الموضوع كيفية إعداد تحويلات وحدات القياس لمتغيرات المنتج المختلفة.</span><span class="sxs-lookup"><span data-stu-id="790c9-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="790c9-106">بدلا من إنشاء منتجات فردية متعددة والتي يجب الاحتفاظ بها، يمكنك استخدام متغيرات المنتج لإنشاء تباينات لمنتج واحد.</span><span class="sxs-lookup"><span data-stu-id="790c9-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="790c9-107">على سبيل المثال، قد يكون أحد متغيرات المنتج قميص تي شيرت بحجم ولون محدد.</span><span class="sxs-lookup"><span data-stu-id="790c9-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="790c9-108">سابقا، كان يمكن إعداد تحويلات الوحدات فقط على أصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="790c9-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="790c9-109">بالتالي، تكون كافة متغيرات المنتجات لها نفس قواعد التحويل.</span><span class="sxs-lookup"><span data-stu-id="790c9-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="790c9-110">ومع ذلك، عند تشغيل ميزة *تحويلات وحدة القياس لمتغيرات المنتجات*، إذا كانت أقمصة التي شيرت تُباع في عبوات، فيمكن تعبئة عدد أقمصة التي شيرت في العبوة تبعًا لحجم التي شيرت، يمكنك الآن إعداد تحويلات الوحدات بين أحجام التي شيرت المختلفة والمربعات المستخدمة للتحويل.</span><span class="sxs-lookup"><span data-stu-id="790c9-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="790c9-111">تشغيل الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="790c9-111">Turn on the feature in your system</span></span>

<span data-ttu-id="790c9-112">إذا لم تشاهد هذه الميزة في النظام بالفعل، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)، وقم بتشغيل ميزة *تحويلات وحدة القياس لمتغيرات المنتجات*.</span><span class="sxs-lookup"><span data-stu-id="790c9-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="790c9-113">إعداد منتج لتحويل الوحدة لكل متغير</span><span class="sxs-lookup"><span data-stu-id="790c9-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="790c9-114">يمكن إنشاء متغيرات المنتج فقط للمنتجات التي هي أصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="790c9-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="790c9-115">لمزيد من المعلومات، راجع [إنشاء أصل منتج](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="790c9-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="790c9-116">لا تتوفر ميزة *تحويلات وحدة القياس لمتغيرات المنتجات* للمنتجات التي يتم إعدادها لعمليات وزن التعبئة.</span><span class="sxs-lookup"><span data-stu-id="790c9-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="790c9-117">لتكوين أصل منتج لدعم تحويل الوحدة لكل متغير، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="790c9-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="790c9-118">‏‫انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> أصول المنتجات‬‬**.</span><span class="sxs-lookup"><span data-stu-id="790c9-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="790c9-119">قم بإنشاء أصل منتج أو افتحه للانتقال إلى صفحة **تفاصيل المنتج** الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="790c9-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="790c9-120">قم بتعيين خيار **تمكين تحويلات وحدة القياس** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="790c9-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="790c9-121">في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **إعداد‬**، حدد **تحويلات الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="790c9-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="790c9-122">يتم فتح صفحة **تحويلات الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="790c9-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="790c9-123">حدد إحدى علامات التبويب التالية:</span><span class="sxs-lookup"><span data-stu-id="790c9-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="790c9-124">**تحويلات بين الفئات** – حدد علامة التبويب هذه للتحويل بين الوحدات التي تنتمي إلى نفس فئة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="790c9-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="790c9-125">**تحويلات عبر الفئات** – حدد علامة التبويب هذه للتحويل بين الوحدات التي تنتمي إلى فئات وحدات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="790c9-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="790c9-126">حدد **جديد** لإضافة تحويل وحدة جديد.</span><span class="sxs-lookup"><span data-stu-id="790c9-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="790c9-127">قم بتعيين حقل **إنشاء تحويل لـ** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="790c9-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="790c9-128">**المنتج** - إذا حددت هذه القيمة، فيمكنك إعداد تحويل الوحدة لأصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="790c9-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="790c9-129">سيتم استخدام تحويل الوحدة هذا كإعداد احتياطي لكافة متغيرات المنتجات التي لم يتم تحديد تحويل وحدة لها.</span><span class="sxs-lookup"><span data-stu-id="790c9-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="790c9-130">**متغير المنتج** - إذا حددت هذه القيمة، فيمكنك إعداد تحويل الوحدة لمتغير منتج محدد.</span><span class="sxs-lookup"><span data-stu-id="790c9-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="790c9-131">استخدم حقل **متغير المنتج** لتحديد المتغير.</span><span class="sxs-lookup"><span data-stu-id="790c9-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="790c9-132">![إضافة تحويل وحدة جديد](media/uom-new-conversion.png "إضافة تحويل وحدة جديد")</span><span class="sxs-lookup"><span data-stu-id="790c9-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="790c9-133">استخدم الحقول الأخرى التي يتم توفيرها لإعداد تحويل الوحدة.</span><span class="sxs-lookup"><span data-stu-id="790c9-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="790c9-134">حدد **موافق** لحفظ تحويل الوحدة الجديد.</span><span class="sxs-lookup"><span data-stu-id="790c9-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="790c9-135">يمكنك فتح صفحة **تحويلات الوحدات** لمنتج أو لمتغير منتج من أي من الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="790c9-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="790c9-136">تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="790c9-136">Product details</span></span>
> - <span data-ttu-id="790c9-137">تفاصيل المنتجات الصادرة</span><span class="sxs-lookup"><span data-stu-id="790c9-137">Released products details</span></span>
> - <span data-ttu-id="790c9-138">متغيرات المنتج الذي تم إصداره</span><span class="sxs-lookup"><span data-stu-id="790c9-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="790c9-139">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="790c9-139">Example scenario</span></span>

<span data-ttu-id="790c9-140">في هذا السيناريو، تبيع الشركة قمصان تي شيرت بمقاسات صغير ومتوسط وكبير وكبير جدًا.</span><span class="sxs-lookup"><span data-stu-id="790c9-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="790c9-141">تم تحديد قميص التي شيرت على أنه منتج، وتم تحديد المقاسات المختلفة على أنها متغيرات لهذا المنتج.</span><span class="sxs-lookup"><span data-stu-id="790c9-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="790c9-142">تتم تعبئة قمصان التي شيرت في عبوات.</span><span class="sxs-lookup"><span data-stu-id="790c9-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="790c9-143">مع الأحجام الصغيرة والمتوسطة والكبيرة، يمكن وضع خمسة قمصان في كل عبوة.</span><span class="sxs-lookup"><span data-stu-id="790c9-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="790c9-144">ومع ذلك، بالنسبة للحجم الكبير جدًا ، توجد مساحة لأربعة قمصان فقط في كل عبوة.</span><span class="sxs-lookup"><span data-stu-id="790c9-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="790c9-145">تريد الشركة تعقب المتغيرات المختلفة بوحدة *القطع* ولكنها تبيعها بوحدة *الصناديق*.</span><span class="sxs-lookup"><span data-stu-id="790c9-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="790c9-146">بالنسبة للأحجام صغير ومتوسط وكبير، فإن التحويل بين وحدة المخزون ووحدة المبيعات هو 1 عبوة = 5 قطع.</span><span class="sxs-lookup"><span data-stu-id="790c9-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="790c9-147">مع الحجم كبير جدًا، التحويل هو 1 عبوة = 4 قطع.</span><span class="sxs-lookup"><span data-stu-id="790c9-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="790c9-148">من صفحة **تفاصيل المنتجات الصادرة** للمنتج **تي شيرت**، افتح صفحة **تحويلات الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="790c9-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="790c9-149">في صفحة **تحويلات الوحدات**، قم بإعداد تحويل الوحدة التالي لمتغير المنتج الصادر **كبير جدًا**.</span><span class="sxs-lookup"><span data-stu-id="790c9-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="790c9-150">الحقل</span><span class="sxs-lookup"><span data-stu-id="790c9-150">Field</span></span>                 | <span data-ttu-id="790c9-151">إعداد</span><span class="sxs-lookup"><span data-stu-id="790c9-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="790c9-152">إنشاء تحويل لـ</span><span class="sxs-lookup"><span data-stu-id="790c9-152">Create conversion for</span></span> | <span data-ttu-id="790c9-153">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="790c9-153">Product variant</span></span>         |
    | <span data-ttu-id="790c9-154">متغير المنتج</span><span class="sxs-lookup"><span data-stu-id="790c9-154">Product variant</span></span>       | <span data-ttu-id="790c9-155">قميص : : كبير جدًا : :</span><span class="sxs-lookup"><span data-stu-id="790c9-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="790c9-156">من وحدة</span><span class="sxs-lookup"><span data-stu-id="790c9-156">From unit</span></span>             | <span data-ttu-id="790c9-157">صناديق</span><span class="sxs-lookup"><span data-stu-id="790c9-157">Boxes</span></span>                   |
    | <span data-ttu-id="790c9-158">المعامل</span><span class="sxs-lookup"><span data-stu-id="790c9-158">Factor</span></span>                | <span data-ttu-id="790c9-159">4</span><span class="sxs-lookup"><span data-stu-id="790c9-159">4</span></span>                       |
    | <span data-ttu-id="790c9-160">إلى وحدة</span><span class="sxs-lookup"><span data-stu-id="790c9-160">To Unit</span></span>               | <span data-ttu-id="790c9-161">القطع</span><span class="sxs-lookup"><span data-stu-id="790c9-161">Pieces</span></span>                  |

1. <span data-ttu-id="790c9-162">نظرًا لأن متغيرات المنتجات **صغير** و **متوسط** و **كبير** لديها نفس تحويل الوحدة بين وحدتي *العبوة* و *القطع*، يمكنك تحديد تحويل الوحدة التالي لها على أصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="790c9-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="790c9-163">الحقل</span><span class="sxs-lookup"><span data-stu-id="790c9-163">Field</span></span>                 | <span data-ttu-id="790c9-164">إعداد</span><span class="sxs-lookup"><span data-stu-id="790c9-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="790c9-165">إنشاء تحويل لـ</span><span class="sxs-lookup"><span data-stu-id="790c9-165">Create conversion for</span></span> | <span data-ttu-id="790c9-166">منتج</span><span class="sxs-lookup"><span data-stu-id="790c9-166">Product</span></span> |
    | <span data-ttu-id="790c9-167">منتج</span><span class="sxs-lookup"><span data-stu-id="790c9-167">Product</span></span>               | <span data-ttu-id="790c9-168">قميص</span><span class="sxs-lookup"><span data-stu-id="790c9-168">T-Shirt</span></span> |
    | <span data-ttu-id="790c9-169">من وحدة</span><span class="sxs-lookup"><span data-stu-id="790c9-169">From unit</span></span>             | <span data-ttu-id="790c9-170">صناديق</span><span class="sxs-lookup"><span data-stu-id="790c9-170">Boxes</span></span>   |
    | <span data-ttu-id="790c9-171">عامل</span><span class="sxs-lookup"><span data-stu-id="790c9-171">Factor</span></span>                | <span data-ttu-id="790c9-172">5</span><span class="sxs-lookup"><span data-stu-id="790c9-172">5</span></span>       |
    | <span data-ttu-id="790c9-173">إلى وحدة</span><span class="sxs-lookup"><span data-stu-id="790c9-173">To Unit</span></span>               | <span data-ttu-id="790c9-174">القطع</span><span class="sxs-lookup"><span data-stu-id="790c9-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="790c9-175">استخدام Excel لتحديث تحويلات الوحدات</span><span class="sxs-lookup"><span data-stu-id="790c9-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="790c9-176">إذا كان المنتج يحتوي على متغيرات منتجات متعددة لها تحويلات وحدات مختلفة، فمن المفيد تصدير تحويلات الوحدات إلى مصنف Microsoft Excel، ثم تحديثها، وإعادة نشرها مرة أخرى إلى Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="790c9-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="790c9-177">لتصدير تحويلات الوحدات إلى Excel، في صفحة **تحويلات الوحدات**، في جزء الإجراءات، حدد **فتح في Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="790c9-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="790c9-178">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="790c9-178">Additional resources</span></span>

[<span data-ttu-id="790c9-179">إدارة وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="790c9-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
