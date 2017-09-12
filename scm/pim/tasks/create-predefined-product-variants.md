--- 
title: "إنشاء متغيرات المنتج المعرفة مسبقًا"
description: "يتناول هذا الإجراء إنشاء متغيرات المنتجات لأصل المنتج باستخدام مجموعات أبعاد المنتجات."
author: BibiSp
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa23f1449e750b4ed1c0f631a98c42b18b7dbb40
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="749d8-103">إنشاء متغيرات المنتج المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="749d8-103">Create predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="749d8-104">يتناول هذا الإجراء إنشاء متغيرات المنتجات لأصل المنتج باستخدام مجموعات أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="749d8-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="749d8-105">شركة بيانات العرض التوضيحي المُستخدمة لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="749d8-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="749d8-106">إنشاء أصل منتج</span><span class="sxs-lookup"><span data-stu-id="749d8-106">Create a product master</span></span>
1. <span data-ttu-id="749d8-107">‏‫انتقل إلى إدارة معلومات المنتج‬ > المنتجات > أصول المنتجات‬‬.</span><span class="sxs-lookup"><span data-stu-id="749d8-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="749d8-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="749d8-108">Click New.</span></span>
3. <span data-ttu-id="749d8-109">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="749d8-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="749d8-110">يجب إدخال رقم منتج يدويًا فقط إذا لم يتم إعداد تسلسل رقمي للحقل "رقم المنتج".</span><span class="sxs-lookup"><span data-stu-id="749d8-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="749d8-111">بمعنى آخر، تجاوز الخطوة إذا تم تعيين تسلسل الرقم للحقل.</span><span class="sxs-lookup"><span data-stu-id="749d8-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="749d8-112">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="749d8-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="749d8-113">في الحقل "مجموعة بُعد المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="749d8-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="749d8-114">حدد مجموعة بُعد المنتج SizeCol (الحجم واللون).</span><span class="sxs-lookup"><span data-stu-id="749d8-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="749d8-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="749d8-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="749d8-116">إضافة أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="749d8-116">Add product dimensions</span></span>
1. <span data-ttu-id="749d8-117">انقر فوق "أبعاد المنتجات".</span><span class="sxs-lookup"><span data-stu-id="749d8-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="749d8-118">يوضح هذا المثال كيفية إدخال أبعاد المنتجات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="749d8-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="749d8-119">يمكنك كذلك اختيار تحديد الحجم أو اللون أو مجموعة النمط التي تتضمن قيم بُعد المنتج الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="749d8-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="749d8-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="749d8-120">Click New.</span></span>
3. <span data-ttu-id="749d8-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="749d8-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="749d8-122">في حقل "الحجم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="749d8-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="749d8-123">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="749d8-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="749d8-124">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="749d8-124">Click New.</span></span>
7. <span data-ttu-id="749d8-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="749d8-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="749d8-126">في حقل "الحجم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="749d8-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="749d8-127">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="749d8-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="749d8-128">انقر فوق علامة التبويب "الألوان".</span><span class="sxs-lookup"><span data-stu-id="749d8-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="749d8-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="749d8-129">Click New.</span></span>
12. <span data-ttu-id="749d8-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="749d8-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="749d8-131">في الحقل "اللون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="749d8-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="749d8-132">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="749d8-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="749d8-133">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="749d8-133">Click New.</span></span>
16. <span data-ttu-id="749d8-134">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="749d8-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="749d8-135">في الحقل "اللون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="749d8-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="749d8-136">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="749d8-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="749d8-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="749d8-137">Click Save.</span></span>
20. <span data-ttu-id="749d8-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="749d8-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="749d8-139">إنشاء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="749d8-139">Generate product variants</span></span>
1. <span data-ttu-id="749d8-140">انقر فوق "متغيرات المنتج".</span><span class="sxs-lookup"><span data-stu-id="749d8-140">Click Product variants.</span></span>
2. <span data-ttu-id="749d8-141">انقر فوق "اقتراحات المتغيرات".</span><span class="sxs-lookup"><span data-stu-id="749d8-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="749d8-142">انقر فوق "تحديد الكل".</span><span class="sxs-lookup"><span data-stu-id="749d8-142">Click Select all.</span></span>
    * <span data-ttu-id="749d8-143">في هذا المثال، يتم تحديد كافة المتغيرات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="749d8-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="749d8-144">في حالة استخدام مجموعة فرعية محتملة من مجموعات أبعاد المنتجات لإنشاء متغيرات، فإنه يمكنك تحديد الإدخالات الفردية.</span><span class="sxs-lookup"><span data-stu-id="749d8-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="749d8-145">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="749d8-145">Click Create.</span></span>
    * <span data-ttu-id="749d8-146">يمكنك إنشاء أوصاف لكافة المتغيرات التي تعتمد على مجموعة قيم أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="749d8-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="749d8-147">الأوصاف اختيارية.</span><span class="sxs-lookup"><span data-stu-id="749d8-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="749d8-148">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="749d8-148">Click Save.</span></span>


