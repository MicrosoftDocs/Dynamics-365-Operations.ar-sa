---
title: تغيير ترتيب الفرز لكيانات الترويج للبضائع
description: يشرح هذا الموضوع المفاهيم المرتبطة بالتحكم في ترتيب عرض كيانات مختلفة المرتبطة بالترويج للبضائع في Microsoft Dynamics 365 for Retail.
author: ashishharchwani
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
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866151"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="e4cdb-103">تغيير ترتيب الفرز لكيانات الترويج للبضائع</span><span class="sxs-lookup"><span data-stu-id="e4cdb-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e4cdb-104">يعتبر اكتشاف المنتجات بالنسبة إلى بائعي التجزئة أداة أساسية لتفاعلات العملاء عبر جميع قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="e4cdb-105">بإمكان وظائف مختلفة أن تساعد العملاء على اكتشاف المنتجات بسهوله.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="e4cdb-106">على سبيل المثال، يمكنهم استعراض الفئات والبحث والتصفية.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="e4cdb-107">يشرح هذا الموضوع المفاهيم المرتبطة بالتحكم في ترتيب عرض كيانات مختلفة المرتبطة بالترويج للبضائع.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="e4cdb-108">كما يشرح كيفية تغيير ترتيب الفرز.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="e4cdb-109">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e4cdb-109">Overview</span></span>

<span data-ttu-id="e4cdb-110">تم تحسين الدعم لفرز كيانات مختلفة ذات صلة بالترويج للبضائع.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="e4cdb-111">يتماشى هذا الدعم الآن بشكل أفضل مع سيناريوهات العميل الموجودة التي كانت تحتاج في السابق إلى ملحقات من أطراف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="e4cdb-112">في إصدارات Microsoft Dynamics 365 for Retail التي سبقت الإصدار 10.0.5، كان ترتيب الفرز أبجديًا للفئات في التدرج الهرمي للتنقل.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="e4cdb-113">تتيح وظيفة ترتيب الفرز المخصص الجديدة لمدراء الترويج للبضائع بتكوين ترتيب الفرز لمختلف الكيانات ذات الصلة بالترويج للبضائع عبر جميع عملاء المستخدمين النهائيين.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="e4cdb-114">ويشمل هؤلاء العملاء المقرات الرئيسية ومراكز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="e4cdb-115">تكوين ترتيب العرض للفئات في التدرج الهرمي لمنتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="e4cdb-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="e4cdb-116">قبل ان تتمكن من إكمال هذا الإجراء، يجب تثبيت بيانات العرض التوضيحي في بيئتك.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="e4cdb-117">انتقل إلى **البيع بالتجزئة \> المنتجات والفئات \> التدرج الهرمي لمنتجات البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="e4cdb-118">انقر فوق **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="e4cdb-119">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-119">Click **Edit**.</span></span>
4. <span data-ttu-id="e4cdb-120">في الشجرة، قم بتوسيع **الكل \> الرياضات الخطيرة**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="e4cdb-121">في الشجرة، قم بتوسيع **الكل \> رياضات الفرق**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="e4cdb-122">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="e4cdb-123">(بإمكان الرقم أن يكون سالبًا.)</span><span class="sxs-lookup"><span data-stu-id="e4cdb-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="e4cdb-124">كرر الخطوات من 4 إلى 6 لأي فئات إضافية ترغب في تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="e4cdb-125">سيظهر ترتيب عرض التدرج الهرمي للتنقل في القناة في المقر الرئيسي للتدرج الهرمي لمنتجات البيع بالتجزئة والمنتجات الصادرة حسب الفئة.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![تدرج هرمي لمنتجات البيع بالتجزئة تم فرزها بطريقة مخصصة مع قيم سالبة](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![منتجات صادرة حسب الفئة تم فرزها بطريقة مخصصة استنادًا إلى التدرج الهرمي لمنتجات البيع بالتجزئة](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="e4cdb-128">تكوين ترتيب العرض للفئات في التدرج الهرمي للتنقل في القناة</span><span class="sxs-lookup"><span data-stu-id="e4cdb-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="e4cdb-129">قبل ان تتمكن من إكمال هذا الإجراء، يجب تثبيت بيانات العرض التوضيحي في بيئتك.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="e4cdb-130">انتقل إلى **البيع بالتجزئة \> المنتجات والفئات \> فئات التنقل في القنوات**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="e4cdb-131">في القائمة، حدد التدرج الهرمي **للتنقل في الأزياء**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="e4cdb-132">انقر فوق **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="e4cdb-133">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-133">Click **Edit**.</span></span>
5. <span data-ttu-id="e4cdb-134">في الشجرة، حدد **أزياء \> ملابس للنساء \> أحذية للنساء**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="e4cdb-135">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="e4cdb-136">في الشجرة، حدد **أزياء \> ملابس للنساء \> قمصان**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="e4cdb-137">بطريقة مماثلة، يمكنك تحديد ترتيب الفرز للفئات الفرعية.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="e4cdb-138">في الشجرة، حدد **أزياء \> ملابس للنساء \> قمصان عادية**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="e4cdb-139">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="e4cdb-140">في الشجرة، حدد **أزياء \> ملابس للرجال \> معاطف وجاكيتات**.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="e4cdb-141">في حقل **ترتيب العرض**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="e4cdb-142">كرر أي فئات إضافية ترغب في تغيير ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="e4cdb-143">ينعكس ترتيب عرض التدرج الهرمي للتنقل في القناة في المقرات الرئيسية والكتالوجات وقنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![تدرج الهرمي للتنقل في القناة تم فرزه بشكل مخصص](./media/ChannelNavCustomSorted.png)

![تدرج الهرمي للتنقل في الكتالوج تم فرزه بشكل مخصص استنادًا إلى التدرج الهرمي للتنقل في القناة](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![نقطة بيع مع فئات تم فرزها بشكل مخصص](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="e4cdb-147">بشكل افتراضي، تكون ميزة ترتيب الفرز المخصص متوقفة عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="e4cdb-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="e4cdb-148">لمعرفة كيفية تشغيل هذه الميزة وميزات أخرى، راجع [إدارة الميزات](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="e4cdb-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
