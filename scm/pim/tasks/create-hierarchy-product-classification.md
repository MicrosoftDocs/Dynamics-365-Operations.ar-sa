--- 
title: "إنشاء تدرج هرمي لتصنيف منتج"
description: "يوضح هذا الإجراء كيفية إنشاء تدرج هرمي جديد للفئة وتعيين نوع تدرج هرمي لكود السلعة."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="0e067-103">إنشاء تدرج هرمي لتصنيف منتج</span><span class="sxs-lookup"><span data-stu-id="0e067-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e067-104">يوضح هذا الإجراء كيفية إنشاء تدرج هرمي جديد للفئة وتعيين نوع تدرج هرمي لكود السلعة.</span><span class="sxs-lookup"><span data-stu-id="0e067-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="0e067-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="0e067-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0e067-106">هذا الإجراء مخصص لمدير الفئات.</span><span class="sxs-lookup"><span data-stu-id="0e067-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="0e067-107">إنشاء تدرج هرمي جديد للفئات</span><span class="sxs-lookup"><span data-stu-id="0e067-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="0e067-108">انتقل إلى إدارة معلومات المنتج > الإعداد > الفئات والسمات > التدرجات الهرمية للفئات.</span><span class="sxs-lookup"><span data-stu-id="0e067-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="0e067-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0e067-109">Click New.</span></span>
3. <span data-ttu-id="0e067-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0e067-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0e067-112">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="0e067-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="0e067-113">إنشاء التسلسل الهرمي</span><span class="sxs-lookup"><span data-stu-id="0e067-113">Build the hierarchy</span></span>
1. <span data-ttu-id="0e067-114">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="0e067-114">Click New category node.</span></span>
2. <span data-ttu-id="0e067-115">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="0e067-116">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="0e067-117">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="0e067-118">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="0e067-118">Click New category node.</span></span>
6. <span data-ttu-id="0e067-119">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="0e067-120">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="0e067-121">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="0e067-122">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="0e067-122">Click New category node.</span></span>
10. <span data-ttu-id="0e067-123">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="0e067-124">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="0e067-125">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="0e067-126">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="0e067-126">Click New category node.</span></span>
14. <span data-ttu-id="0e067-127">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="0e067-128">في الحقل "الرمز"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="0e067-129">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0e067-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="0e067-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0e067-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="0e067-131">تصنيف التسلسل الهرمي</span><span class="sxs-lookup"><span data-stu-id="0e067-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="0e067-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0e067-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="0e067-133">في جزء الإجراءات، انقر فوق "التدرج الهرمي للفئات".</span><span class="sxs-lookup"><span data-stu-id="0e067-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="0e067-134">انقر فوق "إقران نوع التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="0e067-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="0e067-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0e067-135">Click New.</span></span>
5. <span data-ttu-id="0e067-136">في الحقل "نوع التدرج الهرمي للفئات"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="0e067-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="0e067-137">حدد نوع التدرج الهرمي لفئة كود السلعة لتصنيف المنتجات.</span><span class="sxs-lookup"><span data-stu-id="0e067-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="0e067-138">في الحقل "التدرج الهرمي للفئات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0e067-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0e067-139">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0e067-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0e067-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e067-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0e067-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0e067-141">Close the page.</span></span>


