--- 
title: "إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة"
description: "يُعتبر سلوك التكلفة بمثابة تصنيف للتكاليف كثابتة أو متغيرة."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c67c3711871527eada83e1dfe26522ab62828047
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="3c146-103">إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c146-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c146-104">يُعتبر سلوك التكلفة بمثابة تصنيف للتكاليف كثابتة أو متغيرة.</span><span class="sxs-lookup"><span data-stu-id="3c146-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="3c146-105">يجب أن يتم تعيين سياسة وقواعد مناظرة إلى وحدة التحكم بالتكاليف لكي تصبح السياسة سارية.</span><span class="sxs-lookup"><span data-stu-id="3c146-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="3c146-106">استخدم هذا الإجراء لإنشاء سياسة ثم تعيين السياسة إلى وحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c146-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="3c146-107">إنشاء تدرج هرمي لسلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c146-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="3c146-108">انتقل إلى محاسبة التكاليف > الأبعاد > التدرجات الهرمية للأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="3c146-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="3c146-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-109">Click New.</span></span>
3. <span data-ttu-id="3c146-110">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="3c146-110">Click Create.</span></span>
4. <span data-ttu-id="3c146-111">في الحقل "اسم التدرج الهرمي للبعد"، اكتب '"التدرج الهرمي لسلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3c146-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="3c146-112">في حقل "البعد"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c146-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-113">حدد "عناصر التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3c146-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="3c146-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c146-114">Click Save.</span></span>
7. <span data-ttu-id="3c146-115">انقر فوق "عرض التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="3c146-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="3c146-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-116">Click New.</span></span>
9. <span data-ttu-id="3c146-117">في الحقل "اسم العقدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c146-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="3c146-118">أدخل "تكلفة ثابتة".</span><span class="sxs-lookup"><span data-stu-id="3c146-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="3c146-119">في الشجرة، حدد "التدرج الهرمي لسلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3c146-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="3c146-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-120">Click New.</span></span>
12. <span data-ttu-id="3c146-121">في الحقل "اسم العقدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c146-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="3c146-122">أدخل "تكلفة متغيرة".</span><span class="sxs-lookup"><span data-stu-id="3c146-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="3c146-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c146-123">Click Save.</span></span>
14. <span data-ttu-id="3c146-124">في الشجرة، حدد "التدرج الهرمي لسلوك التكلفة\تكلفة ثابتة".</span><span class="sxs-lookup"><span data-stu-id="3c146-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="3c146-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-125">Click New.</span></span>
16. <span data-ttu-id="3c146-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c146-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="3c146-127">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-128">باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.</span><span class="sxs-lookup"><span data-stu-id="3c146-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="3c146-129">في الحقل "إلى عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-130">باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.</span><span class="sxs-lookup"><span data-stu-id="3c146-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="3c146-131">في الشجرة، حدد "التدرج الهرمي لسلوك التكلفة\تكلفة متغيرة".</span><span class="sxs-lookup"><span data-stu-id="3c146-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="3c146-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-132">Click New.</span></span>
21. <span data-ttu-id="3c146-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c146-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="3c146-134">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-135">باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.</span><span class="sxs-lookup"><span data-stu-id="3c146-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="3c146-136">في الحقل "إلى عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-137">باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.</span><span class="sxs-lookup"><span data-stu-id="3c146-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="3c146-138">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c146-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="3c146-139">إنشاء السياسة والقواعد</span><span class="sxs-lookup"><span data-stu-id="3c146-139">Create the policy and rules</span></span>
1. <span data-ttu-id="3c146-140">انتقل إلى محاسبة التكاليف > السياسات > سياسات سلوك التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="3c146-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="3c146-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-141">Click New.</span></span>
3. <span data-ttu-id="3c146-142">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c146-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3c146-143">في الحقل "تدرج بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-144">حدد التدرج الهرمي للسياسة الذي أنشأته للتوّ.</span><span class="sxs-lookup"><span data-stu-id="3c146-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="3c146-145">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-146">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="3c146-146">Select Organization.</span></span>  
6. <span data-ttu-id="3c146-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c146-147">Click Save.</span></span>
7. <span data-ttu-id="3c146-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-148">Click New.</span></span>
8. <span data-ttu-id="3c146-149">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c146-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3c146-150">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-151">قم بتوسيع التدرج الهرمي لتحديد تكلفة متغيرة.</span><span class="sxs-lookup"><span data-stu-id="3c146-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="3c146-152">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3c146-153">بشكل افتراضي، النسبة المئوية المتغيرة هي 100 بالمائة.</span><span class="sxs-lookup"><span data-stu-id="3c146-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="3c146-154">انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c146-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="3c146-155">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c146-155">Click New.</span></span>
13. <span data-ttu-id="3c146-156">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3c146-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="3c146-157">أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".</span><span class="sxs-lookup"><span data-stu-id="3c146-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="3c146-158">للقواعد تاريخ سريان وباستطاعة المستخدم أو النظام إنهاء تاريخ صلاحية قاعدة إذا تم إنشاء إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="3c146-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="3c146-159">في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c146-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="3c146-160">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c146-160">Click Save.</span></span>


