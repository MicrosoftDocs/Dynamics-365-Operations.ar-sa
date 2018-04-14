--- 
title: "تحليل نتائج الاستبيان"
description: "يمكن استخدام إحصاءات الاستبيان لحساب المتوسطات والإجماليات والنسب المئوية استنادًا إلى مجموعة من البيانات الديموغرافية."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7d0bece11b4f78d2e7abc701b8b5b9aa0d76a6a6
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="analyze-questionnaire-results"></a><span data-ttu-id="72a12-103">تحليل نتائج الاستبيان</span><span class="sxs-lookup"><span data-stu-id="72a12-103">Analyze questionnaire results</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72a12-104">يمكن استخدام إحصاءات الاستبيان لحساب المتوسطات والإجماليات والنسب المئوية استنادًا إلى مجموعة من البيانات الديموغرافية.</span><span class="sxs-lookup"><span data-stu-id="72a12-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="72a12-105">لبدء هذا الإجراء، انتقل إلى الاستبيان > عرض النتائج وتحليلها‬ > إحصاءات الاستبيان‬.</span><span class="sxs-lookup"><span data-stu-id="72a12-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="72a12-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="72a12-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="72a12-107">إنشاء سجل إحصاءات الاستبيان‬</span><span class="sxs-lookup"><span data-stu-id="72a12-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="72a12-108">انتقل إلى "إحصاءات الاستبيان".</span><span class="sxs-lookup"><span data-stu-id="72a12-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="72a12-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="72a12-109">Click New.</span></span>
3. <span data-ttu-id="72a12-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="72a12-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="72a12-111">في الحقل "الإحصاءات‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="72a12-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="72a12-112">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="72a12-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="72a12-113">في الحقل "الاستبيان"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="72a12-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="72a12-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="72a12-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="72a12-115">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="72a12-115">Click the General tab.</span></span>
    * <span data-ttu-id="72a12-116">حدد إذا كنت تريد تضمين نتائج مجهولة أو نتائج من العاملين والعقود ومقدمي الطلبات.</span><span class="sxs-lookup"><span data-stu-id="72a12-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="72a12-117">حدد خانة الاختيار "العامل" أو امسحها.</span><span class="sxs-lookup"><span data-stu-id="72a12-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="72a12-118">إذا أردت عرض النتائج حسب الأقدمية أو العمر، فحدد الفواصل الزمنية التي تريد استخدامها لتجميع النتائج.</span><span class="sxs-lookup"><span data-stu-id="72a12-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="72a12-119">سيؤدي إدخال 5 لفترة العمر إلى تجميع النتائج استنادًا إلى فترات عمر من خمس سنوات.</span><span class="sxs-lookup"><span data-stu-id="72a12-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="72a12-120">في الحقل "العمر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="72a12-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="72a12-121">حدد إذا كنت تريد تشغيل الحساب مقابل الاستبيان بالكامل، لكل مجموعة نتائج أو لكل سؤال أو لكل صف أسئلة.</span><span class="sxs-lookup"><span data-stu-id="72a12-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="72a12-122">حدد كيف تريد تجميع النتائج.</span><span class="sxs-lookup"><span data-stu-id="72a12-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="72a12-123">على سبيل المثال، إذا قمت بحساب متوسط النقاط لكل سؤال، فقد تحتاج إلى رؤية الأسئلة مجمعة حسب "مجموعة النتائج".</span><span class="sxs-lookup"><span data-stu-id="72a12-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="72a12-124">حدد البيانات التي تريد إجراء الحساب بالاستناد إليها.</span><span class="sxs-lookup"><span data-stu-id="72a12-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="72a12-125">على سبيل المثال، إذا أردت الاطلاع على متوسط ‏‫النسبة المئوية‬ التي تم تلقيها في الاستبيان عبر العاملين في مقابل متوسط عدد النقاط التي تم تحقيقها عبر العاملين.</span><span class="sxs-lookup"><span data-stu-id="72a12-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="72a12-126">انقر فوق علامة التبويب "النطاق".</span><span class="sxs-lookup"><span data-stu-id="72a12-126">Click the Range tab.</span></span>
    * <span data-ttu-id="72a12-127">استخدم النطاقات لتحديد مجموعة النتائج بحيث تقتصر فقط على تلك التي تستوفي معايير النطاق.</span><span class="sxs-lookup"><span data-stu-id="72a12-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="72a12-128">انقر فوق علامة التبويب "تجميع حسب‬".</span><span class="sxs-lookup"><span data-stu-id="72a12-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="72a12-129">استخدم التجميعات لتحديد كيفية عرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="72a12-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="72a12-130">على سبيل المثال، يمكنك تجميع النتائج حسب نوع الجنس أولاً، ثم حسب العمر.</span><span class="sxs-lookup"><span data-stu-id="72a12-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="72a12-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="72a12-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="72a12-132">انقل التجميعات إلى جانب "محدَد‬" وضعها في الترتيب المطلوب.</span><span class="sxs-lookup"><span data-stu-id="72a12-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="72a12-133">تنفيذ عملية الإحصاءات</span><span class="sxs-lookup"><span data-stu-id="72a12-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="72a12-134">انقر فوق "تنفيذ".</span><span class="sxs-lookup"><span data-stu-id="72a12-134">Click Execute.</span></span>
    * <span data-ttu-id="72a12-135">حدد وظيفة الحساب التي تريد تنفيذها على النتائج.</span><span class="sxs-lookup"><span data-stu-id="72a12-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="72a12-136">على سبيل المثال، يمكنك حساب متوسط النسب المئوية عبر الاستبيان للتجميعات المحددة أو حساب إجمالي النقاط عبر مجموعات النتائج للتجميعات المحددة.</span><span class="sxs-lookup"><span data-stu-id="72a12-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="72a12-137">حدد خانة الاختيار "حذف عمليات البحث السابقة‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="72a12-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="72a12-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="72a12-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="72a12-139">عرض نتائج تشغيل إحصاءات الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="72a12-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="72a12-140">انقر فوق "نتيجة".</span><span class="sxs-lookup"><span data-stu-id="72a12-140">Click Result.</span></span>
2. <span data-ttu-id="72a12-141">انقر فوق "نتيجة".</span><span class="sxs-lookup"><span data-stu-id="72a12-141">Click Result.</span></span>
3. <span data-ttu-id="72a12-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="72a12-142">Close the page.</span></span>


