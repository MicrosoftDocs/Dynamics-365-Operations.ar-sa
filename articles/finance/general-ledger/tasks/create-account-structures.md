---
title: إنشاء بُنى الحساب‬
description: يوضح دليل المهام هذا خطوات إنشاء بنية حساب.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b75ee76a1fb874652415a2174441f629955d763a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145137"
---
# <a name="create-account-structures"></a><span data-ttu-id="73f60-103">إنشاء بُنى الحساب‬</span><span class="sxs-lookup"><span data-stu-id="73f60-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73f60-104">يوضح دليل المهام هذا خطوات إنشاء بنية حساب.</span><span class="sxs-lookup"><span data-stu-id="73f60-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="73f60-105">تستخدم الخطوات شركة بيانات الشركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="73f60-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="73f60-106">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > دليل الحسابات > البنى > تكوين بنى الحسابات‬**.</span><span class="sxs-lookup"><span data-stu-id="73f60-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="73f60-107">في **جزء الإجراءات**، انقر فوق **جديد** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="73f60-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="73f60-108">في الحقل **بنية الحساب**، اكتب اسمًا لوصف الغرض من بنية الحساب.</span><span class="sxs-lookup"><span data-stu-id="73f60-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="73f60-109">في الحقل **الوصف**، اكتب وصفًا لتحديد الغرض من بنية الحساب.</span><span class="sxs-lookup"><span data-stu-id="73f60-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="73f60-110">انقر فوق **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="73f60-110">Click **Create**.</span></span>
6. <span data-ttu-id="73f60-111">في **الشرائح والقيم المسموح بها‬**، انقر فوق **إضافة شريحة‬**.</span><span class="sxs-lookup"><span data-stu-id="73f60-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="73f60-112">في قائمة الأبعاد، حدد البعد المطلوب إضافته إلى بنية الحساب.</span><span class="sxs-lookup"><span data-stu-id="73f60-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="73f60-113">في نهاية القائمة، انقر فوق **إضافة شريحة**.</span><span class="sxs-lookup"><span data-stu-id="73f60-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="73f60-114">كرر الخطوات من 6 إلى 9 حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="73f60-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="73f60-115">في القسم **تفاصيل القيم المسموح بها‬‏‫**، حدد الشريحة لتحرير القيم المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="73f60-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="73f60-116">على سبيل المثال، انقر فوق فوق حقل **الحساب الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="73f60-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="73f60-117">في حقل **عامل التشغيل**، حدد أحد الخيارات، مثل "بين" و"يتضمن".</span><span class="sxs-lookup"><span data-stu-id="73f60-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="73f60-118">في حقل **القيمة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="73f60-119">على سبيل المثال، 600000.</span><span class="sxs-lookup"><span data-stu-id="73f60-119">For example, 600000.</span></span>  
13. <span data-ttu-id="73f60-120">في الحقل **خلال**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-120">In the **through** field, type a value.</span></span> <span data-ttu-id="73f60-121">على سبيل المثال، 699999.</span><span class="sxs-lookup"><span data-stu-id="73f60-121">For example, 699999.</span></span>  
14. <span data-ttu-id="73f60-122">في القسم **تفاصيل القيم المسموح بها**، انقر فوق **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="73f60-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="73f60-123">كرر الخطوات من 10 إلى 15 حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="73f60-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="73f60-124">في القسم **تفاصيل القيم المسموح بها**، انقر فوق **إضافة معايير جديدة**.</span><span class="sxs-lookup"><span data-stu-id="73f60-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="73f60-125">في الحقل "العامل"، حدد أحد الخيارات، مثل "بين" و"يتضمن".</span><span class="sxs-lookup"><span data-stu-id="73f60-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="73f60-126">في حقل **القيمة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="73f60-127">على سبيل المثال، 033.</span><span class="sxs-lookup"><span data-stu-id="73f60-127">For example, 033.</span></span>  
19. <span data-ttu-id="73f60-128">في الحقل **خلال**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-128">In the **through** field, type a value.</span></span> <span data-ttu-id="73f60-129">على سبيل المثال، 034.</span><span class="sxs-lookup"><span data-stu-id="73f60-129">For example, 034.</span></span>  
20. <span data-ttu-id="73f60-130">انقر فوق **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="73f60-130">Click **Apply**.</span></span>
21. <span data-ttu-id="73f60-131">في الشبكة، حدد المقطع لتحرير القيم المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="73f60-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="73f60-132">على سبيل المثال، مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="73f60-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="73f60-133">في الحقل **مركز التكلفة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="73f60-134">على سبيل المثال، 007..021.</span><span class="sxs-lookup"><span data-stu-id="73f60-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="73f60-135">في **الشرائح والقيم المسموح بها‬**، انقر فوق **إضافة‬**.</span><span class="sxs-lookup"><span data-stu-id="73f60-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="73f60-136">في الحقل **الحساب الرئيسي**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="73f60-137">على سبيل المثال، 600000..699999.</span><span class="sxs-lookup"><span data-stu-id="73f60-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="73f60-138">في الشبكة، حدد المقطع لتحرير القيم المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="73f60-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="73f60-139">على سبيل المثال، "القسم".</span><span class="sxs-lookup"><span data-stu-id="73f60-139">For example, Department.</span></span>  
26. <span data-ttu-id="73f60-140">في الحقل "القسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-140">In the Department field, type a value.</span></span> <span data-ttu-id="73f60-141">على سبيل المثال، 032.</span><span class="sxs-lookup"><span data-stu-id="73f60-141">For example, 032.</span></span>  
27. <span data-ttu-id="73f60-142">في الحقل "مركز التكلفة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73f60-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="73f60-143">على سبيل المثال، 086.</span><span class="sxs-lookup"><span data-stu-id="73f60-143">For example, 086.</span></span>  
28. <span data-ttu-id="73f60-144">في **جزء الإجراءات**، انقر فوق **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="73f60-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="73f60-145">في **جزء الإجراءات**، انقر فوق **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="73f60-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="73f60-146">انقر فوق **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="73f60-146">Click **Activate**.</span></span>

