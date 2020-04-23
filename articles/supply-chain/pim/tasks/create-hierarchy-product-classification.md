---
title: إنشاء تدرج هرمي لتصنيف منتج
description: يوضح هذا الإجراء كيفية إنشاء تدرج هرمي جديد للفئة وتعيين نوع تدرج هرمي لكود السلعة.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ff1a2ba20059d3fcb0347220e6e81130e03ac0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203723"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="e545f-103">إنشاء تدرج هرمي لتصنيف منتج</span><span class="sxs-lookup"><span data-stu-id="e545f-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e545f-104">يوضح هذا الإجراء كيفية إنشاء تدرج هرمي جديد للفئة وتعيين نوع تدرج هرمي لكود السلعة.</span><span class="sxs-lookup"><span data-stu-id="e545f-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="e545f-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e545f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e545f-106">هذا الإجراء مخصص لمدير الفئات.</span><span class="sxs-lookup"><span data-stu-id="e545f-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="e545f-107">إنشاء تدرج هرمي جديد للفئات</span><span class="sxs-lookup"><span data-stu-id="e545f-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="e545f-108">انتقل إلى **جزء التنقل > إدارة معلومات المنتج > الإعداد > الفئات والسمات > التدرجات الهرمية للفئات**.</span><span class="sxs-lookup"><span data-stu-id="e545f-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="e545f-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e545f-109">Click **New**.</span></span>
3. <span data-ttu-id="e545f-110">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e545f-111">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e545f-112">انقر فوق **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="e545f-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="e545f-113">إنشاء التسلسل الهرمي</span><span class="sxs-lookup"><span data-stu-id="e545f-113">Build the hierarchy</span></span>
1. <span data-ttu-id="e545f-114">انقر فوق **عقدة فئة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e545f-114">Click **New** category node.</span></span>
2. <span data-ttu-id="e545f-115">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="e545f-116">في حقل **الكود**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="e545f-117">في حقل **الاسم المألوف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="e545f-118">انقر فوق **عقدة فئة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e545f-118">Click **New** category node.</span></span>
6. <span data-ttu-id="e545f-119">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="e545f-120">في حقل **الكود**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="e545f-121">في حقل **الاسم المألوف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="e545f-122">انقر فوق **عقدة فئة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e545f-122">Click **New** category node.</span></span>
10. <span data-ttu-id="e545f-123">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="e545f-124">في حقل **الكود**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="e545f-125">في حقل **الاسم المألوف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="e545f-126">انقر فوق **عقدة فئة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e545f-126">Click **New** category node.</span></span>
14. <span data-ttu-id="e545f-127">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="e545f-128">في حقل **الكود**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="e545f-129">في حقل **الاسم المألوف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e545f-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="e545f-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e545f-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="e545f-131">تصنيف التسلسل الهرمي</span><span class="sxs-lookup"><span data-stu-id="e545f-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="e545f-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e545f-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="e545f-133">في **جزء الإجراءات**، انقر فوق **التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="e545f-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="e545f-134">انقر فوق **إقران نوع التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="e545f-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="e545f-135">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e545f-135">Click **New**.</span></span>
5. <span data-ttu-id="e545f-136">في حقل **نوع التدرج الهرمي للفئات**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e545f-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="e545f-137">حدد **نوع التدرج الهرمي لفئة كود السلعة لتصنيف المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="e545f-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="e545f-138">في حقل **التدرج الهرمي للفئات**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e545f-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e545f-139">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e545f-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e545f-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e545f-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e545f-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e545f-141">Close the page.</span></span>

