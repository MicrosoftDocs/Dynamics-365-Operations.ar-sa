---
title: إنشاء كتالوج تدبير
description: يوضح هذا الدليل كيفية إنشاء كتالوج التدبير.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f2a010e21f16b3908a6ee5f18d8f144c5130be7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "314683"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="1f958-103">إنشاء كتالوج تدبير</span><span class="sxs-lookup"><span data-stu-id="1f958-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f958-104">يوضح هذا الدليل كيفية إنشاء كتالوج التدبير.</span><span class="sxs-lookup"><span data-stu-id="1f958-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="1f958-105">يقوم أخصائي التدبير عادةً بتنفيذ هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="1f958-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="1f958-106">ستتعلم أيضًا كيف يستخدم الموظفون الكتالوج عند إنشاء طلب.</span><span class="sxs-lookup"><span data-stu-id="1f958-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="1f958-107">قبل إنشاء كتالوج، من الضروري وجود تدرج هرمي لفئات التدبير في النظام.</span><span class="sxs-lookup"><span data-stu-id="1f958-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="1f958-108">يتوارث الكتالوج الجديد التدرج الهرمي، إلى جانب جميع المنتجات الموجودة في التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="1f958-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="1f958-109">يمكن استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF حيث يتوفر التدرج الهرمي لفئات التدبير، بالإضافة إلى الأمثلة المستخدمة في خطوات الإجراء.</span><span class="sxs-lookup"><span data-stu-id="1f958-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="1f958-110">التأكد من وجود تدرج هرمي لفئات التدبير</span><span class="sxs-lookup"><span data-stu-id="1f958-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="1f958-111">انتقل إلى التدبير والتوريد > فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="1f958-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="1f958-112">يتوفر التدرج الهرمي لفئات التدبير في شركة بيانات العرض التوضيحي USMF، وتمت إضافة المنتجات إلى فئة الأجهزة المكتبية/أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="1f958-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="1f958-113">إذا كنت تنفذ هذا الإجراء كدليل مهمة، فستحتاج إلى إلغاء تأمين الدليل إذا أردت استعراض الفئة.</span><span class="sxs-lookup"><span data-stu-id="1f958-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="1f958-114">إذا لم يتوفر التدرج هرمي، فيمكنك النقر فوق "جديد" لإنشائه.</span><span class="sxs-lookup"><span data-stu-id="1f958-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="1f958-115">يمكن إجراء ذلك مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="1f958-115">This can only be done once.</span></span>  
2. <span data-ttu-id="1f958-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f958-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="1f958-117">إنشاء كتالوج</span><span class="sxs-lookup"><span data-stu-id="1f958-117">Create a catalog</span></span>
1. <span data-ttu-id="1f958-118">انتقل إلى التدبير وتحديد الموارد > الكتالوجات > كتالوجات التدبير.</span><span class="sxs-lookup"><span data-stu-id="1f958-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="1f958-119">انقر فوق "كتالوج تدبير جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="1f958-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="1f958-120">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1f958-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1f958-121">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="1f958-121">Click OK.</span></span>
5. <span data-ttu-id="1f958-122">في الشجرة، قم بتوسيع "فئات التدبير للشركة".</span><span class="sxs-lookup"><span data-stu-id="1f958-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="1f958-123">في الشجرة، قم بتوسيع "أجهزة المكتب".</span><span class="sxs-lookup"><span data-stu-id="1f958-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="1f958-124">في الشجرة ، حدد "أجهزة الكمبيوتر"</span><span class="sxs-lookup"><span data-stu-id="1f958-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="1f958-125">يتم عرض المنتجات من فئة التدبير في القائمة.</span><span class="sxs-lookup"><span data-stu-id="1f958-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="1f958-126">إذا أردت إضافة منتج إلى الفئة، فستحتاج إلى القيام بذلك على صفحة "التدرج الهرمي لفئات التدبير‬" أو صفحة "تفاصيل الصنف‬".</span><span class="sxs-lookup"><span data-stu-id="1f958-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="1f958-127">يحدد نوع التحديث الافتراضي ما إذا كانت المنتجات الجديدة المضافة إلى التدرج الهرمي لفئات التدبير تكون مرئية على الفور في الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="1f958-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="1f958-128">إذا تم تعيين نوع التحديث إلى "ديناميكي"، فستكون التغييرات مرئية على الفور.</span><span class="sxs-lookup"><span data-stu-id="1f958-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="1f958-129">إما إذا كان نوع التحديث "ثابت"، فستكون المنتجات الجديدة مرئية فقط للأشخاص الذين يستخدمون الكتالوج بعد إعادة نشر الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="1f958-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="1f958-130">يتوفر "إجراء النشر" في جزء الإجراءات في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f958-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="1f958-131">في حالة إزالة منتجات من التدرج الهرمي لفئات التدبير، سيكون التغيير مرئيًا على الفور، بغض النظر عن القيمة الموجودة في حقل نوع التحديث الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="1f958-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="1f958-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1f958-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="1f958-133">انقر فوق "إخفاء".</span><span class="sxs-lookup"><span data-stu-id="1f958-133">Click Hide.</span></span>
10. <span data-ttu-id="1f958-134">في جزء الإجراءات، انقر فوق "تنقل الفئة‬".</span><span class="sxs-lookup"><span data-stu-id="1f958-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="1f958-135">انقر فوق "تعطيل".</span><span class="sxs-lookup"><span data-stu-id="1f958-135">Click Disable.</span></span>
12. <span data-ttu-id="1f958-136">في جزء الإجراءات، انقر فوق "تنقل الفئة‬".</span><span class="sxs-lookup"><span data-stu-id="1f958-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="1f958-137">انقر فوق "تمكين".</span><span class="sxs-lookup"><span data-stu-id="1f958-137">Click Enable.</span></span>
14. <span data-ttu-id="1f958-138">انقر فوق "تنشيط الكتالوج".</span><span class="sxs-lookup"><span data-stu-id="1f958-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="1f958-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f958-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="1f958-140">جعل الكتالوج مرئيًا</span><span class="sxs-lookup"><span data-stu-id="1f958-140">Make the catalog visible</span></span>
1. <span data-ttu-id="1f958-141">انتقل إلى التدبير وتحديد الموارد > إعداد > السياسات > سياسات الشراء.</span><span class="sxs-lookup"><span data-stu-id="1f958-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="1f958-142">حدد "USMF لسياسة التدبير".</span><span class="sxs-lookup"><span data-stu-id="1f958-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="1f958-143">يتعينّ عليك تحديد سياسة الشراء للكيان القانوني الذي يُسمح للعامل المرتبط بملف تعريف المستخدم الخاص بك بطلب المنتجات فيه.</span><span class="sxs-lookup"><span data-stu-id="1f958-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="1f958-144">في بيانات العرض التوضيحي USMF، المستخدم المسؤول مرتبط بالعاملة جوليا فونديربورك، وهي تطلب المنتجات في USMF بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="1f958-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="1f958-145">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1f958-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1f958-146">حدد الكتالوج الذي قمت بإنشائه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="1f958-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="1f958-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1f958-147">Click OK.</span></span>
6. <span data-ttu-id="1f958-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f958-148">Close the page.</span></span>
7. <span data-ttu-id="1f958-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f958-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="1f958-150">استخدام الكتالوج</span><span class="sxs-lookup"><span data-stu-id="1f958-150">Use the catalog</span></span>
1. <span data-ttu-id="1f958-151">انتقل إلى التدبير وتحديد الموارد > طلبات الشراء > كافة طلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="1f958-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="1f958-152">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1f958-152">Click New.</span></span>
3. <span data-ttu-id="1f958-153">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1f958-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1f958-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1f958-154">Click OK.</span></span>
5. <span data-ttu-id="1f958-155">انقر فوق "إضافة المنتجات".</span><span class="sxs-lookup"><span data-stu-id="1f958-155">Click Add products.</span></span>
6. <span data-ttu-id="1f958-156">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1f958-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f958-157">يمكنك استخدام التدرج الهرمي للفئات إلى اليمين أو عامل التصفية في أعلى القائمة لتصفية المنتجات.</span><span class="sxs-lookup"><span data-stu-id="1f958-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="1f958-158">انقر فوق "إضافة إلى البنود".</span><span class="sxs-lookup"><span data-stu-id="1f958-158">Click Add to lines.</span></span>
8. <span data-ttu-id="1f958-159">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1f958-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="1f958-160">انقر فوق "إضافة إلى البنود".</span><span class="sxs-lookup"><span data-stu-id="1f958-160">Click Add to lines.</span></span>
10. <span data-ttu-id="1f958-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1f958-161">Click OK.</span></span>

