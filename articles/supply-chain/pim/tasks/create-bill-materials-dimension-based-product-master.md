--- 
title: "إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد"
description: "لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية."
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d6d98b33d819fd7c68af7d0d5df8eaeb381853b1
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="32276-103">إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد</span><span class="sxs-lookup"><span data-stu-id="32276-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32276-104">لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية.</span><span class="sxs-lookup"><span data-stu-id="32276-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="32276-105">تعمل التسجيلات الأربعة الأولى على إعداد البيانات المطلوبة لإكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="32276-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="32276-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="32276-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="32276-107">عادة ما تتم معالجة هذه المهمة بواسطة مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="32276-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="32276-108">تحديد المنتج</span><span class="sxs-lookup"><span data-stu-id="32276-108">Select the product</span></span>
1. <span data-ttu-id="32276-109">انقر فوق "صيانة المنتج الذي تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="32276-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="32276-110">انقر فوق "المنتجات التي تم إصدارها".</span><span class="sxs-lookup"><span data-stu-id="32276-110">Click Released products.</span></span>
3. <span data-ttu-id="32276-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32276-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="32276-112">ابحث عن أصل المنتج الذي تم إصداره باستخدام تقنية التكوين المستندة إلى البعد الذي قمت بإنشائه في دليل المهمة الأولى في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="32276-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="32276-113">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="32276-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="32276-114">انقر فوق "إصدارات قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="32276-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="32276-115">قم بإنشاء قائمة مكونات صنف جديدة وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="32276-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="32276-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="32276-116">Click New.</span></span>
2. <span data-ttu-id="32276-117">انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="32276-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="32276-118">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="32276-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="32276-119">إعداد موقع</span><span class="sxs-lookup"><span data-stu-id="32276-119">Setting a site</span></span>  
    * <span data-ttu-id="32276-120">في هذا الإجراء، لا نحدد موقع معين لقائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="32276-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="32276-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="32276-121">Click OK.</span></span>
5. <span data-ttu-id="32276-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="32276-122">Click New.</span></span>
    * <span data-ttu-id="32276-123">في هذا الإجراء، سنقوم بإضافة أربعة بنود إلى قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="32276-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="32276-124">يمثل بندين خيارات الكبل ويمثل بندين خيارات الكابينة.</span><span class="sxs-lookup"><span data-stu-id="32276-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="32276-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32276-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="32276-126">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-127">حدد رقم الصنف A0001، كبلات HDMI 6.</span><span class="sxs-lookup"><span data-stu-id="32276-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="32276-128">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-129">حدد مجموعة تكوين الكبل التي تم إنشاؤها في دليل 4 في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="32276-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="32276-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="32276-130">Click New.</span></span>
    * <span data-ttu-id="32276-131">حدد رقم الصنف A0002، كبلات HDMI 12.</span><span class="sxs-lookup"><span data-stu-id="32276-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="32276-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32276-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="32276-133">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="32276-134">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-135">قم بتحديد مجموعة تكوين الكبل مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="32276-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="32276-136">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="32276-136">Click New.</span></span>
14. <span data-ttu-id="32276-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32276-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="32276-138">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-139">حدد رقم الصنف، كابينة D0002.</span><span class="sxs-lookup"><span data-stu-id="32276-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="32276-140">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-141">قم بتحديد مجموعة التكوين الخاصة ببند قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="32276-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="32276-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="32276-142">Click New.</span></span>
18. <span data-ttu-id="32276-143">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32276-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="32276-144">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-145">حدد رقم الصنف M0007 StandardCabinet كآخر بند في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="32276-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="32276-146">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="32276-147">قم بتحديد مجموعة التكوين الخاصة بالكابينة لبند قائمة مكونات الصنف الأخير.</span><span class="sxs-lookup"><span data-stu-id="32276-147">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="32276-148">الموافقة والتنشيط</span><span class="sxs-lookup"><span data-stu-id="32276-148">Approve and activate</span></span>
1. <span data-ttu-id="32276-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="32276-149">Close the page.</span></span>
2. <span data-ttu-id="32276-150">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="32276-150">Click Approve.</span></span>
3. <span data-ttu-id="32276-151">في الحقل "تم اعتماده بوساطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32276-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="32276-152">حدد "نعم" في "هل تريد أيضًا الموافقة على قائمة مكونات الصنف؟ الحقل.</span><span class="sxs-lookup"><span data-stu-id="32276-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="32276-153">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="32276-153">Click OK.</span></span>
6. <span data-ttu-id="32276-154">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="32276-154">Click Activate.</span></span>


