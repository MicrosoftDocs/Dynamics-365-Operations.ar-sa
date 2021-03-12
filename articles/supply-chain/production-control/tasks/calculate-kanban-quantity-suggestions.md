---
title: حساب اقتراحات كمية كانبان
description: يركز هذا الإجراء على تحسين حجم وكميات كانبان لقاعدة كانبان معينة باستخدام حساب كمية كانبان.
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e7343d0a9ea3082a3fad90bdcbb8962e56c70a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981371"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="7622c-103">حساب اقتراحات كمية كانبان</span><span class="sxs-lookup"><span data-stu-id="7622c-103">Calculate kanban quantity suggestions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7622c-104">يركز هذا الإجراء على تحسين حجم وكميات كانبان لقاعدة كانبان معينة باستخدام حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="7622c-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="7622c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7622c-106">هذا الإجراء مخصص لمدير تدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="7622c-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="7622c-107">من الضروري أن تكمل الإجراء: "إضافة سياسة حساب كمية كانبان جديدة إلى قاعدة كانبان".‬</span><span class="sxs-lookup"><span data-stu-id="7622c-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="7622c-108">إنشاء حساب كمية كانبان</span><span class="sxs-lookup"><span data-stu-id="7622c-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="7622c-109">انتقل إلى التحكم بالإنتاج > المهام الدورية > حساب كمية كانبان > حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="7622c-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7622c-110">Click New.</span></span>
3. <span data-ttu-id="7622c-111">في الحقل "الاسم، اكتب "Speaker2016".‬</span><span class="sxs-lookup"><span data-stu-id="7622c-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="7622c-112">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7622c-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7622c-113">حدد السياسة التي أنشأتها في الإجراء: "إضافة سياسة حساب كمية كانبان جديدة إلى قاعدة كانبان".‬</span><span class="sxs-lookup"><span data-stu-id="7622c-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="7622c-114">على سبيل المثال، Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="7622c-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="7622c-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7622c-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7622c-116">في الحقل "تاريخ سريان القاعدة‬"، عيّن التاريخ والوقت إلى "2012-12-17T08:00:00".</span><span class="sxs-lookup"><span data-stu-id="7622c-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="7622c-117">يعمل هذا التاريخ كأساس لتحديد قواعد كانبان الثابتة المضمنة في حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="7622c-118">في الحقل "تاريخ بدء فترة الطلب المستوفاة‬‬"، عيّن التاريخ والوقت إلى "2012-11-17T09:00:00".</span><span class="sxs-lookup"><span data-stu-id="7622c-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="7622c-119">التاريخ الذي يتم اعتبارًا منه تضمين حركات الطلبات السابقة في حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="7622c-120">في الحقل "تاريخ انتهاء فترة الطلب المنفذة‬" عيّن التاريخ والوقت إلى "2012-12-17T07:59:59".</span><span class="sxs-lookup"><span data-stu-id="7622c-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="7622c-121">التاريخ الذي ينتهي عنده تضمين حركات الطلبات السابقة في حساب كمية كانبان.‬</span><span class="sxs-lookup"><span data-stu-id="7622c-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="7622c-122">في الحقل "‏‫تاريخ بدء فترة الطلب‬"، عيّن التاريخ والوقت إلى "2012-12-17T08:00:00".</span><span class="sxs-lookup"><span data-stu-id="7622c-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="7622c-123">التاريخ الذي يتم اعتبارًا منه تضمين حركات الطلبات الحالية في حساب كمية كانبان.‬</span><span class="sxs-lookup"><span data-stu-id="7622c-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="7622c-124">في الحقل "تاريخ انتهاء فترة الطلب‬‬" عيّن التاريخ والوقت إلى "2013-01-16T07:59:59".</span><span class="sxs-lookup"><span data-stu-id="7622c-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="7622c-125">التاريخ الذي ينتهي عنده تضمين حركات الطلبات الحالية في حساب كمية كانبان.‬</span><span class="sxs-lookup"><span data-stu-id="7622c-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="7622c-126">إنشاء مقترح كمية كانبان</span><span class="sxs-lookup"><span data-stu-id="7622c-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="7622c-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7622c-127">Click Save.</span></span>
2. <span data-ttu-id="7622c-128">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="7622c-128">Click Generate.</span></span>
    * <span data-ttu-id="7622c-129">يؤدي ذلك إلى إنشاء بند مقترح كمية كانبان لقاعدة كانبان 000020.</span><span class="sxs-lookup"><span data-stu-id="7622c-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="7622c-130">تشغيل حساب كمية كانبان</span><span class="sxs-lookup"><span data-stu-id="7622c-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="7622c-131">انقر فوق "حساب".</span><span class="sxs-lookup"><span data-stu-id="7622c-131">Click Calculate.</span></span>
    * <span data-ttu-id="7622c-132">يقوم ذلك بحساب مقترح كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="7622c-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7622c-133">Click OK.</span></span>
3. <span data-ttu-id="7622c-134">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7622c-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7622c-135">لاحظ أن كمية كانبان المقترحة هي 2.</span><span class="sxs-lookup"><span data-stu-id="7622c-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="7622c-136">تغيير كمية المنتجات والحساب مرة أخرى</span><span class="sxs-lookup"><span data-stu-id="7622c-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="7622c-137">عيّن كمية المنتجات إلى "5".</span><span class="sxs-lookup"><span data-stu-id="7622c-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="7622c-138">انقر فوق "حساب".</span><span class="sxs-lookup"><span data-stu-id="7622c-138">Click Calculate.</span></span>
3. <span data-ttu-id="7622c-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7622c-139">Click OK.</span></span>
    * <span data-ttu-id="7622c-140">لاحظ أنه بكمية كانبان 5، تغير الاقتراح إلى كمية كانبان 4.</span><span class="sxs-lookup"><span data-stu-id="7622c-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="7622c-141">يعود سبب ذلك إلى أننا بحاجة إلى مزيد من كميات كانبان لتلبية الطلب نظرًا لوجود كمية منتجات أقل.</span><span class="sxs-lookup"><span data-stu-id="7622c-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="7622c-142">تحديث قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="7622c-142">Update kanban rule</span></span>
1. <span data-ttu-id="7622c-143">في الحقل "تاريخ سريان القاعدة‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="7622c-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="7622c-144">عيّن "تاريخ سريان القاعدة'" إلى تاريخ في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="7622c-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="7622c-145">على سبيل المثال، اليوم + سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="7622c-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="7622c-146">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="7622c-146">Click Update.</span></span>
3. <span data-ttu-id="7622c-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7622c-147">Click OK.</span></span>
4. <span data-ttu-id="7622c-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7622c-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="7622c-149">التحقق من صحة التغيير في قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="7622c-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="7622c-150">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="7622c-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7622c-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7622c-152">حدد قاعدة كانبان التي تم إنشاؤها في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="7622c-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="7622c-153">يجب أن تكون هذه القاعدة قاعدة كانبان الأول في القائمة التي تم فرزها حسب الرقم.</span><span class="sxs-lookup"><span data-stu-id="7622c-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="7622c-154">بدّل توسيع المقطع "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="7622c-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="7622c-155">لاحظ تاريخ السريان، مما يعني أنه لن يتم تنشيط هذه القاعدة حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="7622c-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="7622c-156">بدّل توسيع مقطع "الكميات".</span><span class="sxs-lookup"><span data-stu-id="7622c-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="7622c-157">لاحظ أن هذه هي الكمية الافتراضية التي قمت بإدخالها في حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="7622c-158">لاحظ أن هذه هي كمية كانبان الثابتة من 4 من حساب كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="7622c-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="7622c-159">انقر فوق علامة التبويب "ListPanel".</span><span class="sxs-lookup"><span data-stu-id="7622c-159">Click the ListPanel tab.</span></span>

