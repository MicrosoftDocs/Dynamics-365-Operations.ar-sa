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
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920695"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="ea4bd-103">إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد</span><span class="sxs-lookup"><span data-stu-id="ea4bd-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea4bd-104">لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="ea4bd-105">تعمل التسجيلات الأربعة الأولى على إعداد البيانات المطلوبة لإكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="ea4bd-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ea4bd-107">عادة ما تتم معالجة هذه المهمة بواسطة مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="ea4bd-108">تحديد المنتج</span><span class="sxs-lookup"><span data-stu-id="ea4bd-108">Select the product</span></span>

1. <span data-ttu-id="ea4bd-109">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ea4bd-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ea4bd-111">ابحث عن أصل المنتج الذي تم إصداره باستخدام تقنية التكوين المستندة إلى البعد الذي قمت بإنشائه في دليل المهمة الأولى في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="ea4bd-112">في جزء الإجراءات، حدد **مهندس**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="ea4bd-113">حدد **إصدارات قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="ea4bd-114">قم بإنشاء قائمة مكونات صنف جديدة وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="ea4bd-115">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-115">Select **New**.</span></span>
1. <span data-ttu-id="ea4bd-116">حدد **قائمة مكونات الصنف وإصدار قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="ea4bd-117">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="ea4bd-118">إعداد موقع</span><span class="sxs-lookup"><span data-stu-id="ea4bd-118">Setting a site</span></span>  
    * <span data-ttu-id="ea4bd-119">في هذا الإجراء، لا نحدد موقع معين لقائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="ea4bd-120">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-120">Select **OK**.</span></span>
1. <span data-ttu-id="ea4bd-121">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-121">Select **New**.</span></span>
    * <span data-ttu-id="ea4bd-122">في هذا الإجراء، سنقوم بإضافة أربعة بنود إلى قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="ea4bd-123">يمثل بندين خيارات الكبل ويمثل بندين خيارات الكابينة.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="ea4bd-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ea4bd-125">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-126">حدد رقم الصنف A0001، كبلات HDMI 6.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="ea4bd-127">في حقل **مجموعة التكوين**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-128">حدد مجموعة تكوين الكبل التي تم إنشاؤها في دليل 4 في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="ea4bd-129">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-129">Select **New**.</span></span>
    * <span data-ttu-id="ea4bd-130">حدد رقم الصنف A0002، كبلات HDMI 12.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="ea4bd-131">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ea4bd-132">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="ea4bd-133">في حقل **مجموعة التكوين**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-134">قم بتحديد مجموعة تكوين الكبل مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="ea4bd-135">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-135">Select **New**.</span></span>
1. <span data-ttu-id="ea4bd-136">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ea4bd-137">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-138">حدد رقم الصنف، كابينة D0002.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="ea4bd-139">في حقل **مجموعة التكوين**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-140">قم بتحديد مجموعة تكوين الخزانة الخاصة ببند قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="ea4bd-141">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-141">Select **New**.</span></span>
1. <span data-ttu-id="ea4bd-142">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ea4bd-143">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-144">حدد رقم الصنف M0007 StandardCabinet كآخر بند في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="ea4bd-145">في حقل **مجموعة التكوين**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4bd-146">قم بتحديد مجموعة التكوين الخاصة بالخزانة لبند قائمة مكونات الصنف الأخير.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="ea4bd-147">الموافقة والتنشيط</span><span class="sxs-lookup"><span data-stu-id="ea4bd-147">Approve and activate</span></span>

1. <span data-ttu-id="ea4bd-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-148">Close the page.</span></span>
1. <span data-ttu-id="ea4bd-149">حدد **موافقة**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-149">Select **Approve**.</span></span>
1. <span data-ttu-id="ea4bd-150">في حقل **تمت الموافقة بواسطة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="ea4bd-151">حدد *نعم* في حقل **هل تريد أيضًا الموافقة على قائمة مكونات الصنف؟**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="ea4bd-152">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-152">Select **OK**.</span></span>
1. <span data-ttu-id="ea4bd-153">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="ea4bd-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]