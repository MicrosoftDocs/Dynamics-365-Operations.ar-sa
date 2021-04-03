---
title: الوحدة النمطية للعرض السريع
description: يتناول هذا الموضوع وحدات العرض السريع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 07fbf8d4115561808b7c61489b343e1c72dd1b6d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243783"
---
# <a name="quick-view-module"></a><span data-ttu-id="5733a-103">الوحدة النمطية للعرض السريع</span><span class="sxs-lookup"><span data-stu-id="5733a-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="5733a-104">يتناول هذا الموضوع وحدات العرض السريع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5733a-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5733a-105">تتيح الوحدة النمطية للعرض السريع للمستخدمين عرض معلومات المنتج سريعًا عند استعراضهم للمنتجات في صفحة قائمة، وإضافة منتج أو أكثر إلى سلة التسوق من صفحة القائمة، دون الحاجة إلى الانتقال إلى صفحة تفاصيل المنتج (PDP).</span><span class="sxs-lookup"><span data-stu-id="5733a-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="5733a-106">توفر الوحدة النمطية للعرض السريع نظرة عامة حول معلومات المنتج التي يتطلبها المستخدمون لإجراء قرار "إضافة إلى عربة التسوق".</span><span class="sxs-lookup"><span data-stu-id="5733a-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="5733a-107">كما توفر أيضًا ارتباطًا إلى صفحة تفاصيل المنتج (PDP)، بحيث يمكن للمستخدمين عرض تفاصيل المنتج الإضافية وخيارات الشراء.</span><span class="sxs-lookup"><span data-stu-id="5733a-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="5733a-108">يتم دعم الوحدة النمطية للعرض السريع بواسطة الوحدتين النمطيتين [مجموعة المنتجات](product-collection-module-overview.md) و[نتائج البحث](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="5733a-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5733a-109">تتوفر الوحدة النمطية للعرض السريع اعتبارا من إصدار 10.0.17 من Commerce.</span><span class="sxs-lookup"><span data-stu-id="5733a-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="5733a-110">يبين الشكل التوضيحي التالي مثالًا عن وحدة العرض السريع في صفحة قائمة المنتج.</span><span class="sxs-lookup"><span data-stu-id="5733a-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![مثال عن الوحدة النمطية للعرض السريع في صفحة قائمة المنتج](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="5733a-112">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="5733a-112">Module properties</span></span>

<span data-ttu-id="5733a-113">تدعم الوحدة النمطية للعرض السريع بعض الوظائف نفسها الخاصة بالوحدة النمطية لمربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="5733a-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="5733a-114">لذلك، تشبه خصائص الوحدة النمطية للعرض السريع خصائص الوحدة النمطية لمربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="5733a-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="5733a-115">الخاصية</span><span class="sxs-lookup"><span data-stu-id="5733a-115">Property</span></span> | <span data-ttu-id="5733a-116">القيم</span><span class="sxs-lookup"><span data-stu-id="5733a-116">Values</span></span> | <span data-ttu-id="5733a-117">الوصف</span><span class="sxs-lookup"><span data-stu-id="5733a-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="5733a-118">علامة العنوان</span><span class="sxs-lookup"><span data-stu-id="5733a-118">Heading tag</span></span> | <span data-ttu-id="5733a-119">**H1** أو **H2** أو **H3** أو **H4** أو **H5** أو **H6**</span><span class="sxs-lookup"><span data-stu-id="5733a-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="5733a-120"> تقوم هذه الخاصية بتعريف علامة العنوان لعنوان المنتج.</span><span class="sxs-lookup"><span data-stu-id="5733a-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="5733a-121">إذا كانت الوحدة النمطية للعرض السريع في أعلى الصفحة، فيجب تعيين هذه الخاصية إلى **H1** لتلبيه معايير إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="5733a-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="5733a-122">السماح بالسعر المخصص</span><span class="sxs-lookup"><span data-stu-id="5733a-122">Allow custom price</span></span> | <span data-ttu-id="5733a-123">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="5733a-123">**True** or **False**</span></span> | <span data-ttu-id="5733a-124">إذا تم تعيين هذه الخاصية على **صحيح**، فيمكن للمستخدم إدخال سعر مخصص.</span><span class="sxs-lookup"><span data-stu-id="5733a-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="5733a-125">الحد الأدنى للسعر</span><span class="sxs-lookup"><span data-stu-id="5733a-125">Minimum price</span></span> | <span data-ttu-id="5733a-126">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="5733a-126">Integer</span></span> | <span data-ttu-id="5733a-127">لا تنطبق هذه الخاصية إلا في حالة تعيين خاصية **السماح بالسعر المخصص** إلى **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="5733a-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="5733a-128">وتحدد الحد الأدنى للسعر الذي يمكن للمستخدم إدخاله (على سبيل المثال، 1 دولار).</span><span class="sxs-lookup"><span data-stu-id="5733a-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="5733a-129">الحد الأقصى للسعر</span><span class="sxs-lookup"><span data-stu-id="5733a-129">Maximum price</span></span> | <span data-ttu-id="5733a-130">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="5733a-130">Integer</span></span> | <span data-ttu-id="5733a-131">لا تنطبق هذه الخاصية إلا في حالة تعيين خاصية **السماح بالسعر المخصص** إلى **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="5733a-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="5733a-132">وتحدد الحد الأقصى للسعر الذي يمكن للمستخدم إدخاله (على سبيل المثال، 1,000 دولار).</span><span class="sxs-lookup"><span data-stu-id="5733a-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="5733a-133">إعدادات منشئ موقع التجارة</span><span class="sxs-lookup"><span data-stu-id="5733a-133">Commerce site builder settings</span></span>

<span data-ttu-id="5733a-134">ومثل الوحدة النمطية لمربع الشراء، فإن الوحدة النمطية للعرض السريع تستخدم الإعدادات في **إعدادات الموقع \> الملحقات \> إضافة منتج إلى سلة التسوق**.</span><span class="sxs-lookup"><span data-stu-id="5733a-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="5733a-135">ومع ذلك، يتم تجاهل إعداد **صفحة الانتقال إلى سلة التسوق**، لأنه غير متناسق مع الغرض من الوحدة النمطية للعرض السريع، وهو تمكين المستخدمين من استعراض منتجات متعددة في صفحة القوائم وإضافتها إلى سلة التسوق دون الانتقال من صفحة القائمة.</span><span class="sxs-lookup"><span data-stu-id="5733a-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="5733a-136">إضافة وحدة نمطية للعرض السريع إلى الوحدة النمطية لمجموعة منتجات</span><span class="sxs-lookup"><span data-stu-id="5733a-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="5733a-137">يتم إضافة الوحدة النمطية للعرض السريع إلى الوحدتين النمطيتين مجموعة المنتجات ونتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="5733a-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="5733a-138">لإضافة وحدة نمطية للعرض السريع إلى وحدة مجموعة منتجات في منشئ مواقع Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5733a-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5733a-139">انتقل إلى **الصفحات**، ثم حدد الصفحة الرئيسية لموقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="5733a-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="5733a-140">انتقل إلى أي وحدة نمطية لـ **مجموعة المنتجات** في الصفحة الرئيسية، وحدد علامة القطع (**...**)، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="5733a-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5733a-141">في مربع الحوار **إضافة وحدة نمطية**، حدد الوحدة النمطية **العرض السريع**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5733a-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5733a-142">في جزء الخصائص من الوحدة النمطية **للعرض السريع**، حدد **عنوان**.</span><span class="sxs-lookup"><span data-stu-id="5733a-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="5733a-143">في مربع الحوار **العنوان**، قم بتعيين حقل **مستوى العنوان** إلى **H2**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5733a-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="5733a-144">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="5733a-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5733a-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5733a-145">Additional resources</span></span>

[<span data-ttu-id="5733a-146">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="5733a-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5733a-147">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="5733a-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5733a-148">الوحدة النمطية لمجموعة المنتجات</span><span class="sxs-lookup"><span data-stu-id="5733a-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="5733a-149">وحدة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="5733a-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]