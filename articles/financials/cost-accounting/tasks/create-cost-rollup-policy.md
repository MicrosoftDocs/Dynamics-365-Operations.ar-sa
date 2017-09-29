--- 
title: "إنشاء سياسة زيادة التكاليف"
description: "يظهر هذا الإجراء كيفية إنشاء سياسة زيادة التكاليف وإنشاء قواعد للسياسة."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="8f5e5-103">إنشاء سياسة زيادة التكاليف</span><span class="sxs-lookup"><span data-stu-id="8f5e5-103">Create a cost rollup policy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f5e5-104">يظهر هذا الإجراء كيفية إنشاء سياسة زيادة التكاليف وإنشاء قواعد للسياسة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="8f5e5-105">بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USP2.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8f5e5-106">إنشاء سياسة</span><span class="sxs-lookup"><span data-stu-id="8f5e5-106">Create a policy</span></span>
1. <span data-ttu-id="8f5e5-107">انتقل إلى محاسبة التكاليف > السياسات > سياسات زيادة التكاليف‬‬.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="8f5e5-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-108">Click New.</span></span>
3. <span data-ttu-id="8f5e5-109">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8f5e5-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8f5e5-111">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-112">حدد "زيادة التكلفة‬ CC".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="8f5e5-113">في الحقل "تدرج بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-114">حدد "زيادة التكلفة‬ CC".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="8f5e5-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="8f5e5-116">إنشاء قواعد لسياسة زيادة التكاليف</span><span class="sxs-lookup"><span data-stu-id="8f5e5-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="8f5e5-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-117">Click New.</span></span>
2. <span data-ttu-id="8f5e5-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8f5e5-119">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-120">حدد 007.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-120">Select 007.</span></span>  
4. <span data-ttu-id="8f5e5-121">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-122">حدد "زيادة التكلفة‬ CE".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="8f5e5-123">في الحقل "عنصر التكلفة الثانوي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-124">على سبيل المثال، قم بتعيين عنصر التكلفة الثانوي CC-007 إلى مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="8f5e5-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-125">Click New.</span></span>
7. <span data-ttu-id="8f5e5-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8f5e5-127">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-128">حدد 008.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-128">Select 008.</span></span>  
9. <span data-ttu-id="8f5e5-129">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-130">حدد "زيادة التكلفة‬ CE".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="8f5e5-131">في الحقل "عنصر التكلفة الثانوي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-132">على سبيل المثال، قم بتعيين عنصر التكلفة الثانوي CC-008 إلى مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="8f5e5-133">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-133">Click New.</span></span>
12. <span data-ttu-id="8f5e5-134">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8f5e5-135">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-136">حدد 009.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-136">Select 009.</span></span>  
14. <span data-ttu-id="8f5e5-137">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-138">حدد "زيادة التكلفة‬ CE".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="8f5e5-139">في الحقل "عنصر التكلفة الثانوي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8f5e5-140">على سبيل المثال، قم بتعيين عنصر التكلفة الثانوي CC-009 إلى مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="8f5e5-141">تابع حتى يتم تعيين كافة مراكز التكلفة إلى عناصر التكلفة الفرعية المناظرة.</span><span class="sxs-lookup"><span data-stu-id="8f5e5-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="8f5e5-142">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8f5e5-142">Click Save.</span></span>


