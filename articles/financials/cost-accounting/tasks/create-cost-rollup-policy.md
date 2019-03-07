---
title: إنشاء سياسة زيادة التكاليف
description: يظهر هذا الإجراء كيفية إنشاء سياسة زيادة التكاليف وإنشاء قواعد للسياسة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f1fa434061832bd306cef13afc46c7f3adab0c0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "362592"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="8ee3b-103">إنشاء سياسة زيادة التكاليف</span><span class="sxs-lookup"><span data-stu-id="8ee3b-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ee3b-104">يظهر هذا الإجراء كيفية إنشاء سياسة زيادة التكاليف وإنشاء قواعد للسياسة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="8ee3b-105">بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USP2.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8ee3b-106">إنشاء سياسة</span><span class="sxs-lookup"><span data-stu-id="8ee3b-106">Create a policy</span></span>
1. <span data-ttu-id="8ee3b-107">انتقل إلى محاسبة التكاليف > السياسات > سياسات زيادة التكاليف‬‬.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="8ee3b-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-108">Click New.</span></span>
3. <span data-ttu-id="8ee3b-109">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8ee3b-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8ee3b-111">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-112">حدد "زيادة التكلفة‬ CC".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="8ee3b-113">في الحقل "تدرج بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-114">حدد "زيادة التكلفة‬ CC".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="8ee3b-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="8ee3b-116">إنشاء قواعد لسياسة زيادة التكاليف</span><span class="sxs-lookup"><span data-stu-id="8ee3b-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="8ee3b-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-117">Click New.</span></span>
2. <span data-ttu-id="8ee3b-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8ee3b-119">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-120">حدد 007.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-120">Select 007.</span></span>  
4. <span data-ttu-id="8ee3b-121">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-122">حدد "زيادة التكلفة‬ CE".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="8ee3b-123">في الحقل "عنصر التكلفة الثانوي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-124">على سبيل المثال، قم بتعيين عنصر التكلفة الثانوي CC-007 إلى مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="8ee3b-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-125">Click New.</span></span>
7. <span data-ttu-id="8ee3b-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8ee3b-127">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-128">حدد 008.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-128">Select 008.</span></span>  
9. <span data-ttu-id="8ee3b-129">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-130">حدد "زيادة التكلفة‬ CE".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="8ee3b-131">في الحقل "عنصر التكلفة الثانوي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-132">على سبيل المثال، قم بتعيين عنصر التكلفة الثانوي CC-008 إلى مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="8ee3b-133">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-133">Click New.</span></span>
12. <span data-ttu-id="8ee3b-134">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8ee3b-135">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-136">حدد 009.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-136">Select 009.</span></span>  
14. <span data-ttu-id="8ee3b-137">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-138">حدد "زيادة التكلفة‬ CE".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="8ee3b-139">في الحقل "عنصر التكلفة الثانوي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8ee3b-140">على سبيل المثال، قم بتعيين عنصر التكلفة الثانوي CC-009 إلى مركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="8ee3b-141">تابع حتى يتم تعيين كافة مراكز التكلفة إلى عناصر التكلفة الفرعية المناظرة.</span><span class="sxs-lookup"><span data-stu-id="8ee3b-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="8ee3b-142">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8ee3b-142">Click Save.</span></span>

