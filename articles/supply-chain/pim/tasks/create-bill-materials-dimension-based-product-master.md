---
title: إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد
description: لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820072"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="37fae-103">إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد</span><span class="sxs-lookup"><span data-stu-id="37fae-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37fae-104">لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية.</span><span class="sxs-lookup"><span data-stu-id="37fae-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="37fae-105">تعمل التسجيلات الأربعة الأولى على إعداد البيانات المطلوبة لإكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="37fae-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="37fae-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="37fae-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37fae-107">عادة ما تتم معالجة هذه المهمة بواسطة مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="37fae-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="37fae-108">تحديد المنتج</span><span class="sxs-lookup"><span data-stu-id="37fae-108">Select the product</span></span>
1. <span data-ttu-id="37fae-109">انقر فوق "صيانة المنتج الذي تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="37fae-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="37fae-110">انقر فوق "المنتجات التي تم إصدارها".</span><span class="sxs-lookup"><span data-stu-id="37fae-110">Click Released products.</span></span>
3. <span data-ttu-id="37fae-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37fae-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="37fae-112">ابحث عن أصل المنتج الذي تم إصداره باستخدام تقنية التكوين المستندة إلى البعد الذي قمت بإنشائه في دليل المهمة الأولى في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="37fae-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="37fae-113">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="37fae-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="37fae-114">انقر فوق "إصدارات قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="37fae-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="37fae-115">قم بإنشاء قائمة مكونات صنف جديدة وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="37fae-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="37fae-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37fae-116">Click New.</span></span>
2. <span data-ttu-id="37fae-117">انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="37fae-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="37fae-118">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="37fae-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="37fae-119">إعداد موقع</span><span class="sxs-lookup"><span data-stu-id="37fae-119">Setting a site</span></span>  
    * <span data-ttu-id="37fae-120">في هذا الإجراء، لا نحدد موقع معين لقائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="37fae-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="37fae-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37fae-121">Click OK.</span></span>
5. <span data-ttu-id="37fae-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37fae-122">Click New.</span></span>
    * <span data-ttu-id="37fae-123">في هذا الإجراء، سنقوم بإضافة أربعة بنود إلى قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="37fae-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="37fae-124">يمثل بندين خيارات الكبل ويمثل بندين خيارات الكابينة.</span><span class="sxs-lookup"><span data-stu-id="37fae-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="37fae-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37fae-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="37fae-126">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-127">حدد رقم الصنف A0001، كبلات HDMI 6.</span><span class="sxs-lookup"><span data-stu-id="37fae-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="37fae-128">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-129">حدد مجموعة تكوين الكبل التي تم إنشاؤها في دليل 4 في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="37fae-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="37fae-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37fae-130">Click New.</span></span>
    * <span data-ttu-id="37fae-131">حدد رقم الصنف A0002، كبلات HDMI 12.</span><span class="sxs-lookup"><span data-stu-id="37fae-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="37fae-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37fae-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="37fae-133">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="37fae-134">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-135">قم بتحديد مجموعة تكوين الكبل مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="37fae-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="37fae-136">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37fae-136">Click New.</span></span>
14. <span data-ttu-id="37fae-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37fae-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="37fae-138">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-139">حدد رقم الصنف، كابينة D0002.</span><span class="sxs-lookup"><span data-stu-id="37fae-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="37fae-140">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-141">قم بتحديد مجموعة التكوين الخاصة ببند قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="37fae-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="37fae-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37fae-142">Click New.</span></span>
18. <span data-ttu-id="37fae-143">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37fae-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="37fae-144">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-145">حدد رقم الصنف M0007 StandardCabinet كآخر بند في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="37fae-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="37fae-146">في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="37fae-147">قم بتحديد مجموعة التكوين الخاصة بالكابينة لبند قائمة مكونات الصنف الأخير.</span><span class="sxs-lookup"><span data-stu-id="37fae-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="37fae-148">الموافقة والتنشيط</span><span class="sxs-lookup"><span data-stu-id="37fae-148">Approve and activate</span></span>
1. <span data-ttu-id="37fae-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37fae-149">Close the page.</span></span>
2. <span data-ttu-id="37fae-150">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="37fae-150">Click Approve.</span></span>
3. <span data-ttu-id="37fae-151">في الحقل "تم اعتماده بوساطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37fae-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="37fae-152">حدد "نعم" في "هل تريد أيضًا الموافقة على قائمة مكونات الصنف؟ الحقل.</span><span class="sxs-lookup"><span data-stu-id="37fae-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="37fae-153">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37fae-153">Click OK.</span></span>
6. <span data-ttu-id="37fae-154">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="37fae-154">Click Activate.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]