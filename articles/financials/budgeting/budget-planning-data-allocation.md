---
title: "توزيع بيانات تخطيط الموازنة"
description: "توضح هذه المقالة طرق التوزيع المختلفة المتوفرة في Microsoft Dynamics 365 for Finance and Operations وكيفية استخدامها."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 20dd11ad8b632de279855c1641f7bdeddb33cb4b
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="6ca62-103">توزيع بيانات تخطيط الموازنة</span><span class="sxs-lookup"><span data-stu-id="6ca62-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ca62-104">توضح هذه المقالة طرق التوزيع المختلفة المتوفرة في Microsoft Dynamics 365 for Finance and Operations وكيفية استخدامها.</span><span class="sxs-lookup"><span data-stu-id="6ca62-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations and how they can be used.</span></span>  

<span data-ttu-id="6ca62-105">يمكنك توزيع البيانات في خطة موازنة عدة طرق لتصور المبالغ المتوقعة بدقة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="6ca62-106">أساليب التوزيع</span><span class="sxs-lookup"><span data-stu-id="6ca62-106">Allocation methods</span></span>
<span data-ttu-id="6ca62-107">ويمكن لطرق التوزيع الثلاثة (التوزيع عبر فترات، والتوزيع للأبعاد، واستخدام قواعد توزيع دفتر الأستاذ) إنشاء بنود خطة الموازنة التي تستند إلى بنود في خطة الموازنة ذاتها.</span><span class="sxs-lookup"><span data-stu-id="6ca62-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="6ca62-108">ويمكن لثلاثة طرق أخرى (التجميع والتوزيع والنسخ من خطة الموازنة) إنشاء بنود خطة الموازنة في خطط الموازنة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="6ca62-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="6ca62-109">وبالنسبة لكافة طرق التوزيع الستة، يمكنك تحديد سيناريو الوجهة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="6ca62-110">ويمكن أن يكون سيناريو الوجهة نفس الشيء مثل السيناريو المصدر أو مختلفًا عن السيناريو المصدر.</span><span class="sxs-lookup"><span data-stu-id="6ca62-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="6ca62-111">بالإضافة إلى ذلك، يمكنك تحديد ما إذا كان يتم إلحاق بنود جديدة بخطة الموازنة أو استبدال البنود الحالية في خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="6ca62-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**التوزيع عبر الفترات** – يمكنك استخدام فئة توزيع فترة لتوزيع بنود خطة الموازنة من سيناريو خطة موازنة المصدر عبر الفترات في سيناريو الوجهة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="6ca62-113">ويتم تعيين المبلغ المصدر لعدة بنود في سيناريو الوجهة، استناداً إلى النسبة المئوية والتاريخ اللذين تم تحديدهما في فئة توزيع الفترة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="6ca62-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**التوزيع للأبعاد** – يتم توزيع بنود خطة الموازنة من سيناريو تخطيط الموازنة المصدر إلى بند واحد أو أكثر في السيناريو الوجهة، استناداً إلى النسب المئوية والأبعاد المالية التي تم تحديدها في مدة توزيع الموازنة المحددة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="6ca62-115">![AggregateChart](./media/aggregatechart-300x230.png)
**التجميع** – يتم تجميع بنود خطة الموازنة من سيناريو خطة الموازنة المصدر في خطط الموازنة المرتبطة إلى سيناريو الوجهة في خطة الموازنة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6ca62-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="6ca62-116">تعمل هذه الطريقة على تمكين مبالغ الموازنة التي تم إعدادها في مستوى أدنى في المؤسسة لتجميعها في مستوى أعلى.</span><span class="sxs-lookup"><span data-stu-id="6ca62-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="6ca62-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**التوزيع** - يتم توزيع بنود خطة الموازنة من سيناريو تخطيط الموازنة المصدر في خطة الموازنة الأصلية إلى السيناريو الوجهة في خطط الموازنة المرتبطة بها (الفرعية)، استناداً إلى الأبعاد المالية لوحدات المؤسسة للخطط المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="6ca62-118">تعمل هذه الطريقة على تمكين مبالغ الموازنة التي تم إعدادها في مستوى أعلى في المؤسسة المراد لنشرها لمرجعة مترجمة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6ca62-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="6ca62-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**استخدام قواعد توزيع دفتر الأستاذ** – يتم توزيع بنود خطة الموازنة من سيناريو تخطيط الموازنة المصدر إلى سيناريو الوجهة، وفقًا لقاعدة توزيع دفتر الأستاذ‬ التي تم تحديدها.</span><span class="sxs-lookup"><span data-stu-id="6ca62-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="6ca62-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**نسخ من خطة موازنة‬** – كما في طريقة توزيع التخصيص، يتم إنشاء بنود خطة الموازنة في الوجهة، استناداً إلى بنود في خطة موازنة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="6ca62-121">ومع ذلك، لا يلزم لهذه الطريقة أن تكون خطة الموازنة المصدر هي الخطة الأصلية ولكن يمكن أن توجد في أي مستوى عالٍ في التدرج الهرمي لخطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="6ca62-122">وتفيد طريقة التوزيع هذه إذا تم إدراج المبالغ المجمعة في الموازنة أصلاً عند مستوى أعلى بكثير، ويجب تحويلها إلى مستوى أدنى للمؤسسة لمراجعتها تفصيليًا وتسويتها قبل أن يمكنها الحصول على اعتماد على مستوى أعلى.</span><span class="sxs-lookup"><span data-stu-id="6ca62-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="6ca62-123">استخدام طرق التوزيع في خطة موازنة</span><span class="sxs-lookup"><span data-stu-id="6ca62-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="6ca62-124">لتنفيذ عمليات التوزيع في صفحة خطة الموازنة، حدد البنود المراد توزيعها، ثم انقر فوق **توزيع الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="6ca62-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="6ca62-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="6ca62-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="6ca62-126">في الخطوة التالية، قم بتحديد طريقة توزيع.</span><span class="sxs-lookup"><span data-stu-id="6ca62-126">Next, select an allocation method.</span></span> <span data-ttu-id="6ca62-127">ويتم بعد ذلك تعيين الحقول المتبقية، استناداً إلى الطريقة التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="6ca62-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="6ca62-128">وتتضمن هذه الحقول المصدر والوجهة لبيانات خطة الموازنة وخيارًا يتيح لك ضرب المصدر في عامل محدد عند إنشاء مبالغ الوجهة، لتسهيل التسوية الكبيرة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="6ca62-129">كما يمكنك تعيين خيار **الإلحاق بخطة**.</span><span class="sxs-lookup"><span data-stu-id="6ca62-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="6ca62-130">وحدد **لا** لاستبدال بنود خطة الموازنة الموجودة، أو حدد **نعم** للاحتفاظ ببنود خطة الموازنة الموجودة وإضافة بنود جديدة للمبالغ الموزعة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="6ca62-131">الإجراء التلقائي لعمليات التوزيع أثناء سير العمل</span><span class="sxs-lookup"><span data-stu-id="6ca62-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="6ca62-132">تعمل ميزة قوية واحدة على تمكين إجراء التوزيعات تلقائياً كجزء من سير عمل تخطيط موازنة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="6ca62-133">وعند انتقال خطة موازنة عبر مهمة سير العمل الخاصة به، يمكن للمهام التلقائية أن تؤدي إلى توزيع في مرحلة تخطيط موازنة محددة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="6ca62-134">ولإعداد التوزيع التلقائي، يجب أولاً إنشاء جدول توزيع في صفحة **تكوين تخطيط الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="6ca62-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="6ca62-135">ويحدد جدول التوزيع طريقة التوزيع التي سيتم استخدامها عند تشغيل التوزيع التلقائي، وقيم خيارات التوزيع المختلفة (راجع القسم السابق للأطلاع على الأوصاف).</span><span class="sxs-lookup"><span data-stu-id="6ca62-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="6ca62-136">وبعد ذلك، يمكنك إنشاء توزيع مرحلة في صفحة **تكوين تخطيط الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="6ca62-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="6ca62-137">ويقوم توزيع المرحلة بتعيين جدول توزيع لمرحلة وعملية سير عمل تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="6ca62-138">وأخيراً، أضف مهمة مؤتمتة لتوزيع مراحل تخطيط الموازنة في مرحلة سير العمل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6ca62-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="6ca62-139">وفي المثال التالي، تم إدراج اثنين من توزيعات مراحل تخطيط الموازنة (المُشار إليهما باللون الأحمر) في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6ca62-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="6ca62-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="6ca62-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




