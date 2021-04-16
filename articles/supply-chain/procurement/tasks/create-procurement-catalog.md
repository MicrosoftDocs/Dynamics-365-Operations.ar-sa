---
title: إنشاء كتالوج تدبير
description: يوضح هذا الموضوع كيفية إنشاء كتالوج التدبير.
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59117df519b7aa525713d3acd70195cc42614b9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812388"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="9fb7f-103">إنشاء كتالوج تدبير</span><span class="sxs-lookup"><span data-stu-id="9fb7f-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fb7f-104">يوضح هذا الموضوع كيفية إنشاء كتالوج التدبير.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="9fb7f-105">يقوم أخصائي التدبير عادةً بتنفيذ هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="9fb7f-106">ستتعلم أيضًا كيف يستخدم الموظفون الكتالوج عند إنشاء طلب.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="9fb7f-107">قبل إنشاء كتالوج، من الضروري وجود تدرج هرمي لفئات التدبير في النظام.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="9fb7f-108">يتوارث الكتالوج الجديد التدرج الهرمي، إلى جانب جميع المنتجات الموجودة في التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="9fb7f-109">يمكن استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF حيث يتوفر التدرج الهرمي لفئات التدبير، بالإضافة إلى الأمثلة المستخدمة في خطوات الإجراء.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="9fb7f-110">التأكد من وجود تدرج هرمي لفئات التدبير</span><span class="sxs-lookup"><span data-stu-id="9fb7f-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="9fb7f-111">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد‬ > فئات التدبير‬**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="9fb7f-112">يتوفر التدرج الهرمي لفئات التدبير في شركة بيانات العرض التوضيحي USMF، وتمت إضافة المنتجات إلى فئة **الأجهزة المكتبية/أجهزة الكمبيوتر**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="9fb7f-113">إذا كنت تنفذ هذا الإجراء كدليل مهمة، فستحتاج إلى إلغاء تأمين الدليل إذا أردت استعراض الفئة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="9fb7f-114">إذا لم يتوفر التدرج هرمي، فيمكنك النقر فوق **جديد** لإنشائه.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="9fb7f-115">يمكن إجراء ذلك مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-115">This can only be done once.</span></span>  
2. <span data-ttu-id="9fb7f-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="9fb7f-117">إنشاء كتالوج</span><span class="sxs-lookup"><span data-stu-id="9fb7f-117">Create a catalog</span></span>
1. <span data-ttu-id="9fb7f-118">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد‬ > كتالوجات > فئات التدبير‬**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="9fb7f-119">حدد **فئة تدبير جديدة** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="9fb7f-120">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="9fb7f-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-121">Select **OK**.</span></span>
5. <span data-ttu-id="9fb7f-122">في الشجرة، قم بتوسيع **فئات التدبير للشركة**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="9fb7f-123">في الشجرة، قم بتوسيع **أجهزة المكتب**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="9fb7f-124">في الشجرة، حدد **أجهزة الكمبيوتر**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="9fb7f-125">يتم عرض المنتجات من فئة التدبير في القائمة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="9fb7f-126">إذا أردت إضافة منتج إلى الفئة، فستحتاج إلى القيام بذلك على صفحة **التدرج الهرمي لفئات التدبير‬** أو صفحة **تفاصيل الصنف**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="9fb7f-127">يحدد نوع التحديث **الافتراضي** ما إذا كانت المنتجات الجديدة المضافة إلى التدرج الهرمي لفئات التدبير تكون مرئية على الفور في الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="9fb7f-128">إذا تم تعيين نوع التحديث إلى **ديناميكي**، فستكون التغييرات مرئية على الفور.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="9fb7f-129">إذا كان التحديث من النوع **ثابت**، فستكون المنتجات الجديدة مرئية فقط للأشخاص الذين يستخدمون الكتالوج بعد إعادة نشر الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="9fb7f-130">يتوفر **النشر** في جزء الإجراءات في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="9fb7f-131">في حالة إزالة منتجات من التدرج الهرمي لفئات التدبير، سيكون التغيير مرئيًا على الفور، بغض النظر عن القيمة الموجودة في حقل نوع التحديث **الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="9fb7f-132">في جزء الإجراءات، حدد **تنقل الفئة‬** وتأكد من تحديد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="9fb7f-133">حدد **تنشيط الكتالوج**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="9fb7f-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="9fb7f-135">جعل الكتالوج مرئيًا</span><span class="sxs-lookup"><span data-stu-id="9fb7f-135">Make the catalog visible</span></span>
1. <span data-ttu-id="9fb7f-136">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد‬ > الإعداد > السياسات > سياسات الشراء**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="9fb7f-137">حدد **USMF لسياسة التدبير**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="9fb7f-138">يتعينّ عليك تحديد سياسة الشراء للكيان القانوني الذي يُسمح للعامل المرتبط بملف تعريف المستخدم الخاص بك بطلب المنتجات فيه.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="9fb7f-139">في بيانات العرض التوضيحي USMF، المستخدم المسؤول مرتبط بالعاملة **جوليا فونديربورك**، وهي تطلب المنتجات في USMF بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="9fb7f-140">حدد الكتالوج الذي قمت بإنشائه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="9fb7f-141">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="9fb7f-142">استخدام الكتالوج</span><span class="sxs-lookup"><span data-stu-id="9fb7f-142">Use the catalog</span></span>
1. <span data-ttu-id="9fb7f-143">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد > أوامر الشراء > جميع أوامر الشراء‬**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="9fb7f-144">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-144">Select **New**.</span></span>
3. <span data-ttu-id="9fb7f-145">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="9fb7f-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-146">Select **OK**.</span></span>
5. <span data-ttu-id="9fb7f-147">حدد **إضافة منتجات**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-147">Select **Add products**.</span></span>
6. <span data-ttu-id="9fb7f-148">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="9fb7f-149">يمكنك استخدام التدرج الهرمي للفئات إلى اليمين أو عامل التصفية في أعلى القائمة لتصفية المنتجات.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="9fb7f-150">حدد **إضافة إلى البنود**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="9fb7f-151">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9fb7f-151">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]