---
title: تغيير ترتيب الفرز لكيانات الترويج للبضائع
description: يشرح هذا الموضوع المفاهيم المرتبطة بالتحكم في ترتيب عرض كيانات مختلفة المرتبطة بالترويج للبضائع في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021440"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="d73e6-103">تغيير ترتيب الفرز لكيانات الترويج للبضائع</span><span class="sxs-lookup"><span data-stu-id="d73e6-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d73e6-104">يعتبر اكتشاف المنتجات بالنسبة إلى بائعي التجزئة أداة أساسية لتفاعلات العملاء عبر جميع القنوات.</span><span class="sxs-lookup"><span data-stu-id="d73e6-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="d73e6-105">بإمكان وظائف مختلفة أن تساعد العملاء على اكتشاف المنتجات بسهوله.</span><span class="sxs-lookup"><span data-stu-id="d73e6-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="d73e6-106">على سبيل المثال، يمكنهم استعراض الفئات والبحث والتصفية.</span><span class="sxs-lookup"><span data-stu-id="d73e6-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="d73e6-107">يشرح هذا الموضوع المفاهيم المرتبطة بالتحكم في ترتيب عرض كيانات مختلفة المرتبطة بالترويج للبضائع.</span><span class="sxs-lookup"><span data-stu-id="d73e6-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="d73e6-108">كما يشرح كيفية تغيير ترتيب الفرز.</span><span class="sxs-lookup"><span data-stu-id="d73e6-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="d73e6-109">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d73e6-109">Overview</span></span>

<span data-ttu-id="d73e6-110">تم تحسين الدعم لفرز كيانات مختلفة ذات صلة بالترويج للبضائع.</span><span class="sxs-lookup"><span data-stu-id="d73e6-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="d73e6-111">يتماشى هذا الدعم الآن بشكل أفضل مع سيناريوهات العميل الموجودة التي كانت تحتاج في السابق إلى ملحقات من أطراف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="d73e6-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="d73e6-112">في إصدارات Retail التي سبقت الإصدار 10.0.5، كان ترتيب الفرز أبجديًا للفئات في التدرج الهرمي للتنقل.</span><span class="sxs-lookup"><span data-stu-id="d73e6-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="d73e6-113">تتيح وظيفة ترتيب الفرز المخصص الجديدة لمدراء الترويج للبضائع بتكوين ترتيب الفرز لمختلف الكيانات ذات الصلة بالترويج للبضائع عبر جميع عملاء المستخدمين النهائيين.</span><span class="sxs-lookup"><span data-stu-id="d73e6-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="d73e6-114">ويشمل هؤلاء العملاء المقرات الرئيسية ومراكز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="d73e6-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="d73e6-115">تكوين ترتيب العرض للفئات في التدرج الهرمي للمنتجات</span><span class="sxs-lookup"><span data-stu-id="d73e6-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="d73e6-116">قبل ان تتمكن من إكمال هذا الإجراء، يجب تثبيت بيانات العرض التوضيحي في بيئتك.</span><span class="sxs-lookup"><span data-stu-id="d73e6-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="d73e6-117">انتقل إلى **البيع بالتجزئة والتجارة \> المنتجات والفئات \> التدرج الهرمي للمنتجات التجارية**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="d73e6-118">انقر فوق **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="d73e6-119">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-119">Click **Edit**.</span></span>
4. <span data-ttu-id="d73e6-120">في الشجرة، قم بتوسيع **الكل \> الرياضات الخطيرة**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="d73e6-121">في الشجرة، قم بتوسيع **الكل \> رياضات الفرق**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="d73e6-122">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d73e6-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="d73e6-123">(بإمكان الرقم أن يكون سالبًا.)</span><span class="sxs-lookup"><span data-stu-id="d73e6-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="d73e6-124">كرر الخطوات من 4 إلى 6 لأي فئات إضافية ترغب في تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="d73e6-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="d73e6-125">سيظهر ترتيب عرض التدرج الهرمي للتنقل في القناة في المقر الرئيسي للتدرج الهرمي للمنتجات التجارية والمنتجات الصادرة حسب الفئة.</span><span class="sxs-lookup"><span data-stu-id="d73e6-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![تم فرز التدرج الهرمي للمنتجات بطريقة مخصصة بقيم سالبة](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![تم فرز المنتجات الصادرة حسب الفئة بطريقة مخصصة استنادًا إلى التدرج الهرمي للمنتجات](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="d73e6-128">تكوين ترتيب العرض للفئات في التدرج الهرمي للتنقل في القناة</span><span class="sxs-lookup"><span data-stu-id="d73e6-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="d73e6-129">قبل ان تتمكن من إكمال هذا الإجراء، يجب تثبيت بيانات العرض التوضيحي في بيئتك.</span><span class="sxs-lookup"><span data-stu-id="d73e6-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="d73e6-130">انتقل إلى **البيع بالتجزئة والتجارة \> المنتجات والفئات \> فئات التنقل في القنوات**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="d73e6-131">في القائمة، حدد التدرج الهرمي **للتنقل في الأزياء**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="d73e6-132">انقر فوق **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="d73e6-133">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-133">Click **Edit**.</span></span>
5. <span data-ttu-id="d73e6-134">في الشجرة، حدد **أزياء \> ملابس للنساء \> أحذية للنساء**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="d73e6-135">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d73e6-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="d73e6-136">في الشجرة، حدد **أزياء \> ملابس للنساء \> قمصان**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="d73e6-137">بطريقة مماثلة، يمكنك تحديد ترتيب الفرز للفئات الفرعية.</span><span class="sxs-lookup"><span data-stu-id="d73e6-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="d73e6-138">في الشجرة، حدد **أزياء \> ملابس للنساء \> قمصان عادية**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="d73e6-139">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d73e6-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="d73e6-140">في الشجرة، حدد **أزياء \> ملابس للرجال \> معاطف وجاكيتات**.</span><span class="sxs-lookup"><span data-stu-id="d73e6-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="d73e6-141">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d73e6-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="d73e6-142">كرر أي فئات إضافية ترغب في تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="d73e6-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="d73e6-143">يظهر ترتيب عرض التدرج الهرمي للتنقل في القناة في المقر الرئيسي والكتالوج والقنوات.</span><span class="sxs-lookup"><span data-stu-id="d73e6-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![تدرج الهرمي للتنقل في القناة تم فرزه بشكل مخصص](./media/ChannelNavCustomSorted.png)

![تدرج الهرمي للتنقل في الكتالوج تم فرزه بشكل مخصص استنادًا إلى التدرج الهرمي للتنقل في القناة](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![نقطة بيع مع فئات تم فرزها بشكل مخصص](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="d73e6-147">بشكل افتراضي، تكون ميزة ترتيب الفرز المخصص متوقفة عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d73e6-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="d73e6-148">لمعرفة كيفية تشغيل هذه الميزة وميزات أخرى، راجع [إدارة الميزات](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="d73e6-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>