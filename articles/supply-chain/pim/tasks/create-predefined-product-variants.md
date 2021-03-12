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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d07a090dbd41eb17e8d604887435bbb8b07e8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966920"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="42995-103">إنشاء متغيرات المنتج المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="42995-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42995-104">يتناول هذا الإجراء إنشاء متغيرات المنتجات لأصل المنتج باستخدام مجموعات أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="42995-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="42995-105">شركة بيانات العرض التوضيحي المُستخدمة لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="42995-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="42995-106">إنشاء أصل منتج</span><span class="sxs-lookup"><span data-stu-id="42995-106">Create a product master</span></span>
1. <span data-ttu-id="42995-107">‏‫انتقل إلى إدارة معلومات المنتج‬ > المنتجات > أصول المنتجات‬‬.</span><span class="sxs-lookup"><span data-stu-id="42995-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="42995-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="42995-108">Click New.</span></span>
3. <span data-ttu-id="42995-109">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="42995-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="42995-110">يجب إدخال رقم منتج يدويًا فقط إذا لم يتم إعداد تسلسل رقمي للحقل "رقم المنتج".</span><span class="sxs-lookup"><span data-stu-id="42995-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="42995-111">بمعنى آخر، تجاوز الخطوة إذا تم تعيين تسلسل الرقم للحقل.</span><span class="sxs-lookup"><span data-stu-id="42995-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="42995-112">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="42995-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="42995-113">في الحقل "مجموعة بُعد المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42995-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="42995-114">حدد مجموعة بُعد المنتج SizeCol (الحجم واللون).</span><span class="sxs-lookup"><span data-stu-id="42995-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="42995-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="42995-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="42995-116">إضافة أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="42995-116">Add product dimensions</span></span>
1. <span data-ttu-id="42995-117">انقر فوق "أبعاد المنتجات".</span><span class="sxs-lookup"><span data-stu-id="42995-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="42995-118">يوضح هذا المثال كيفية إدخال أبعاد المنتجات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="42995-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="42995-119">يمكنك كذلك اختيار تحديد الحجم أو اللون أو مجموعة النمط التي تتضمن قيم بُعد المنتج الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="42995-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="42995-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="42995-120">Click New.</span></span>
3. <span data-ttu-id="42995-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="42995-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="42995-122">في حقل "الحجم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42995-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="42995-123">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="42995-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="42995-124">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="42995-124">Click New.</span></span>
7. <span data-ttu-id="42995-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="42995-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="42995-126">في حقل "الحجم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42995-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="42995-127">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="42995-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="42995-128">انقر فوق علامة التبويب "الألوان".</span><span class="sxs-lookup"><span data-stu-id="42995-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="42995-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="42995-129">Click New.</span></span>
12. <span data-ttu-id="42995-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="42995-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="42995-131">في الحقل "اللون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42995-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="42995-132">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="42995-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="42995-133">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="42995-133">Click New.</span></span>
16. <span data-ttu-id="42995-134">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="42995-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="42995-135">في الحقل "اللون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42995-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="42995-136">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="42995-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="42995-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="42995-137">Click Save.</span></span>
20. <span data-ttu-id="42995-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="42995-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="42995-139">إنشاء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="42995-139">Generate product variants</span></span>
1. <span data-ttu-id="42995-140">انقر فوق "متغيرات المنتج".</span><span class="sxs-lookup"><span data-stu-id="42995-140">Click Product variants.</span></span>
2. <span data-ttu-id="42995-141">انقر فوق "اقتراحات المتغيرات".</span><span class="sxs-lookup"><span data-stu-id="42995-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="42995-142">انقر فوق "تحديد الكل".</span><span class="sxs-lookup"><span data-stu-id="42995-142">Click Select all.</span></span>
    * <span data-ttu-id="42995-143">في هذا المثال، يتم تحديد كافة المتغيرات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="42995-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="42995-144">في حالة استخدام مجموعة فرعية محتملة من مجموعات أبعاد المنتجات لإنشاء متغيرات، فإنه يمكنك تحديد الإدخالات الفردية.</span><span class="sxs-lookup"><span data-stu-id="42995-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="42995-145">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="42995-145">Click Create.</span></span>
    * <span data-ttu-id="42995-146">يمكنك إنشاء أوصاف لكافة المتغيرات التي تعتمد على مجموعة قيم أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="42995-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="42995-147">الأوصاف اختيارية.</span><span class="sxs-lookup"><span data-stu-id="42995-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="42995-148">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="42995-148">Click Save.</span></span>

