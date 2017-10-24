--- 
title: "إضافة سياسة حساب كمية كانبان إلى قاعدة كانبان"
description: "يركز هذا الإجراء على إنشاء سياسة حساب كمية كانبان وإضافتها إلى قاعدة كانبان لتحسين حجم كانبان وكمياته."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a947d4a5302c6ed1848396d50cfbfcb78aabf97
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="0702c-103">إضافة سياسة حساب كمية كانبان إلى قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="0702c-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0702c-104">يركز هذا الإجراء على إنشاء سياسة حساب كمية كانبان وإضافتها إلى قاعدة كانبان لتحسين حجم كانبان وكمياته.</span><span class="sxs-lookup"><span data-stu-id="0702c-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="0702c-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="0702c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0702c-106">هذا الإجراء مخصص لمدير تدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="0702c-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="0702c-107">يُعد هذا الإجراء شرطًا مسبقًا لإنشاء الإجراء "حساب اقتراحات كمية كانبان‬".</span><span class="sxs-lookup"><span data-stu-id="0702c-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="0702c-108">إنشاء سياسة حساب كمية كانبان</span><span class="sxs-lookup"><span data-stu-id="0702c-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="0702c-109">انتقل إلى التحكم بالإنتاج > المهام الدورية > حساب كمية كانبان > سياسات حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="0702c-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="0702c-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0702c-110">Click New.</span></span>
3. <span data-ttu-id="0702c-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0702c-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="0702c-112">على سبيل المثال، اكتب Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="0702c-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="0702c-113">في الحقل "الخطة الرئيسية‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0702c-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0702c-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0702c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0702c-115">حدد StaticPlan لحساب الطلب.</span><span class="sxs-lookup"><span data-stu-id="0702c-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="0702c-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0702c-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0702c-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0702c-117">Click Save.</span></span>
8. <span data-ttu-id="0702c-118">في الحقل "الحد الأدنى لكمية كانبان‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="0702c-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="0702c-119">هذا هو العدد الإضافي من كانبان الذي يتم تضمينه في حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="0702c-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="0702c-120">عيّن عامل الأمان إلى "1".</span><span class="sxs-lookup"><span data-stu-id="0702c-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="0702c-121">هذا هو العامل المستخدم لحساب الكمية الإضافية للمخزون الاحتياطي.</span><span class="sxs-lookup"><span data-stu-id="0702c-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="0702c-122">في الحقل "الأيام المقبلة‬‬‬"، أدخل "30".</span><span class="sxs-lookup"><span data-stu-id="0702c-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="0702c-123">هذا هو عدد الأيام التي تسبق تاريخ حساب كمية كانبان المضمن في حساب الطلب.</span><span class="sxs-lookup"><span data-stu-id="0702c-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="0702c-124">في الحقل "الأيام السابقة‬"، أدخل "30".</span><span class="sxs-lookup"><span data-stu-id="0702c-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="0702c-125">هذا هو عدد الأيام التي تلي تاريخ حساب كمية كانبان المضمن في حساب الطلب.</span><span class="sxs-lookup"><span data-stu-id="0702c-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="0702c-126">يتم عرض المعادلة المستخدمة للحساب مع القيم الحقيقية.</span><span class="sxs-lookup"><span data-stu-id="0702c-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="0702c-127">على سبيل المثال، كمية كانبان = ((متوسط الطلب اليومي × الحد الأدنى لوقت الإنتاج × 2.00) / كمية المنتجات لكل وحدة معالجة مواد) + 1</span><span class="sxs-lookup"><span data-stu-id="0702c-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="0702c-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0702c-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="0702c-129">إضافة سياسة حساب كمية كانبان إلى قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="0702c-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="0702c-130">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="0702c-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="0702c-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0702c-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0702c-132">حدد قاعدة كانبان 000020 لتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0702c-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="0702c-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0702c-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0702c-134">بدّل توسيع المقطع "سياسات حساب كمية كانبان‬‬‬".</span><span class="sxs-lookup"><span data-stu-id="0702c-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="0702c-135">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0702c-135">Click Add.</span></span>
    * <span data-ttu-id="0702c-136">أضف سياسة حساب كمية كانبان التي أنشأتها في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="0702c-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="0702c-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0702c-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0702c-138">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0702c-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0702c-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0702c-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0702c-140">حدد السياسة Speaker2016 التي أنشأتها في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="0702c-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  


