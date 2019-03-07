---
title: إنشاء تدرج هرمي لتصنيف منتج
description: يوضح هذا الإجراء كيفية إنشاء تدرج هرمي جديد للفئة وتعيين نوع تدرج هرمي لكود السلعة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "346814"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="5e8f2-103">إنشاء تدرج هرمي لتصنيف منتج</span><span class="sxs-lookup"><span data-stu-id="5e8f2-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e8f2-104">يوضح هذا الإجراء كيفية إنشاء تدرج هرمي جديد للفئة وتعيين نوع تدرج هرمي لكود السلعة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="5e8f2-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5e8f2-106">هذا الإجراء مخصص لمدير الفئات.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="5e8f2-107">إنشاء تدرج هرمي جديد للفئات</span><span class="sxs-lookup"><span data-stu-id="5e8f2-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="5e8f2-108">انتقل إلى إدارة معلومات المنتج > الإعداد > الفئات والسمات > التدرجات الهرمية للفئات.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="5e8f2-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5e8f2-109">Click New.</span></span>
3. <span data-ttu-id="5e8f2-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5e8f2-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5e8f2-112">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="5e8f2-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="5e8f2-113">إنشاء التسلسل الهرمي</span><span class="sxs-lookup"><span data-stu-id="5e8f2-113">Build the hierarchy</span></span>
1. <span data-ttu-id="5e8f2-114">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="5e8f2-114">Click New category node.</span></span>
2. <span data-ttu-id="5e8f2-115">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="5e8f2-116">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="5e8f2-117">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="5e8f2-118">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="5e8f2-118">Click New category node.</span></span>
6. <span data-ttu-id="5e8f2-119">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="5e8f2-120">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="5e8f2-121">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="5e8f2-122">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="5e8f2-122">Click New category node.</span></span>
10. <span data-ttu-id="5e8f2-123">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="5e8f2-124">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="5e8f2-125">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="5e8f2-126">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="5e8f2-126">Click New category node.</span></span>
14. <span data-ttu-id="5e8f2-127">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="5e8f2-128">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="5e8f2-129">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="5e8f2-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="5e8f2-131">تصنيف التسلسل الهرمي</span><span class="sxs-lookup"><span data-stu-id="5e8f2-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="5e8f2-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="5e8f2-133">في جزء الإجراءات، انقر فوق "التدرج الهرمي للفئات".</span><span class="sxs-lookup"><span data-stu-id="5e8f2-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="5e8f2-134">انقر فوق "إقران نوع التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="5e8f2-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="5e8f2-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5e8f2-135">Click New.</span></span>
5. <span data-ttu-id="5e8f2-136">في الحقل "نوع التدرج الهرمي للفئات"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="5e8f2-137">حدد نوع التدرج الهرمي لفئة كود السلعة لتصنيف المنتجات.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="5e8f2-138">في الحقل "التدرج الهرمي للفئات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5e8f2-139">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5e8f2-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5e8f2-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-141">Close the page.</span></span>

