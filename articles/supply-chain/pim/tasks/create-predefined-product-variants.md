---
title: إنشاء متغيرات المنتج المعرفة مسبقًا
description: يتناول هذا الإجراء إنشاء متغيرات المنتجات لأصل المنتج باستخدام مجموعات أبعاد المنتجات.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa9c6d4862a49bbf0b5ecbb8c0c3d573e0f49e6
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986133"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="12f7d-103">إنشاء متغيرات المنتج المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="12f7d-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12f7d-104">يتناول هذا الإجراء إنشاء متغيرات المنتجات لأصل المنتج باستخدام مجموعات أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="12f7d-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="12f7d-105">شركة بيانات العرض التوضيحي المُستخدمة لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="12f7d-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="12f7d-106">إنشاء أصل منتج</span><span class="sxs-lookup"><span data-stu-id="12f7d-106">Create a product master</span></span>
1. <span data-ttu-id="12f7d-107">‏‫انتقل إلى إدارة معلومات المنتج‬ > المنتجات > أصول المنتجات‬‬.</span><span class="sxs-lookup"><span data-stu-id="12f7d-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="12f7d-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="12f7d-108">Click New.</span></span>
3. <span data-ttu-id="12f7d-109">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="12f7d-110">يجب إدخال رقم منتج يدويًا فقط إذا لم يتم إعداد تسلسل رقمي للحقل "رقم المنتج".</span><span class="sxs-lookup"><span data-stu-id="12f7d-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="12f7d-111">بمعنى آخر، تجاوز الخطوة إذا تم تعيين تسلسل الرقم للحقل.</span><span class="sxs-lookup"><span data-stu-id="12f7d-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="12f7d-112">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="12f7d-113">في الحقل "مجموعة بُعد المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f7d-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12f7d-114">حدد مجموعة بُعد المنتج SizeCol (الحجم واللون).</span><span class="sxs-lookup"><span data-stu-id="12f7d-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="12f7d-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="12f7d-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="12f7d-116">إضافة أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="12f7d-116">Add product dimensions</span></span>
1. <span data-ttu-id="12f7d-117">انقر فوق "أبعاد المنتجات".</span><span class="sxs-lookup"><span data-stu-id="12f7d-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="12f7d-118">يوضح هذا المثال كيفية إدخال أبعاد المنتجات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="12f7d-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="12f7d-119">يمكنك كذلك اختيار تحديد الحجم أو اللون أو مجموعة النمط التي تتضمن قيم بُعد المنتج الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="12f7d-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="12f7d-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="12f7d-120">Click New.</span></span>
3. <span data-ttu-id="12f7d-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="12f7d-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="12f7d-122">في حقل "الحجم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f7d-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="12f7d-123">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="12f7d-124">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="12f7d-124">Click New.</span></span>
7. <span data-ttu-id="12f7d-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="12f7d-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="12f7d-126">في حقل "الحجم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f7d-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="12f7d-127">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="12f7d-128">انقر فوق علامة التبويب "الألوان".</span><span class="sxs-lookup"><span data-stu-id="12f7d-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="12f7d-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="12f7d-129">Click New.</span></span>
12. <span data-ttu-id="12f7d-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="12f7d-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="12f7d-131">في الحقل "اللون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f7d-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="12f7d-132">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="12f7d-133">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="12f7d-133">Click New.</span></span>
16. <span data-ttu-id="12f7d-134">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="12f7d-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="12f7d-135">في الحقل "اللون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f7d-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="12f7d-136">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="12f7d-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="12f7d-137">Click Save.</span></span>
20. <span data-ttu-id="12f7d-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="12f7d-139">إنشاء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="12f7d-139">Generate product variants</span></span>
1. <span data-ttu-id="12f7d-140">انقر فوق "متغيرات المنتج".</span><span class="sxs-lookup"><span data-stu-id="12f7d-140">Click Product variants.</span></span>
2. <span data-ttu-id="12f7d-141">انقر فوق "اقتراحات المتغيرات".</span><span class="sxs-lookup"><span data-stu-id="12f7d-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="12f7d-142">انقر فوق "تحديد الكل".</span><span class="sxs-lookup"><span data-stu-id="12f7d-142">Click Select all.</span></span>
    * <span data-ttu-id="12f7d-143">في هذا المثال، يتم تحديد كافة المتغيرات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="12f7d-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="12f7d-144">في حالة استخدام مجموعة فرعية محتملة من مجموعات أبعاد المنتجات لإنشاء متغيرات، فإنه يمكنك تحديد الإدخالات الفردية.</span><span class="sxs-lookup"><span data-stu-id="12f7d-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="12f7d-145">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="12f7d-145">Click Create.</span></span>
    * <span data-ttu-id="12f7d-146">يمكنك إنشاء أوصاف لكافة المتغيرات التي تعتمد على مجموعة قيم أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="12f7d-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="12f7d-147">الأوصاف اختيارية.</span><span class="sxs-lookup"><span data-stu-id="12f7d-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="12f7d-148">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="12f7d-148">Click Save.</span></span>

