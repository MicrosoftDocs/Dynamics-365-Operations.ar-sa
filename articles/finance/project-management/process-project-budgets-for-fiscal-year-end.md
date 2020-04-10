---
title: نقل موازنات المشروع في نهاية السنة المالية
description: يقدم هذا المقال معلومات حول كيفيةه تحويل مبالغ الموازنة المتبقية إلى سنوات مستقبلية وإنشاء تفاصيل سجل الموازنة.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172320"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="18a12-103">نقل موازنات المشروع في نهاية السنة المالية</span><span class="sxs-lookup"><span data-stu-id="18a12-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18a12-104">عند العمل في مشروع متعدد السنوات، فقد يكون لديك الميزانية المتبقية في نهاية السنه المالية.</span><span class="sxs-lookup"><span data-stu-id="18a12-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="18a12-105">يمكنك تحويل مبالغ الموازنة المتبقية لسنة مستقبلية، وإنشاء تفاصيل سجل الموازنة للمبالغ في حسابات دفاتر الأستاذ العام المقترنة.</span><span class="sxs-lookup"><span data-stu-id="18a12-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="18a12-106">قبل تحويل المبالغ المتبقية إلى الموازنة، قم بمراجعة مبالغ الموازنة المتبقية وتحليلها.</span><span class="sxs-lookup"><span data-stu-id="18a12-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="18a12-107">مراجعة مبالغ الموازنة المتبقية وتحليلها</span><span class="sxs-lookup"><span data-stu-id="18a12-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="18a12-108">أكمل الخطوات التالية لمراجعة مبالغ موازنة نهاية العام للمشاريع، ولكنك دون تحويل المبالغ في الموازنة.</span><span class="sxs-lookup"><span data-stu-id="18a12-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="18a12-109">انتقل إلى **إدارة المشاريع ومحاسبتها** > **دوري** > **الموازنات** > **الموازنات المحولة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="18a12-110">في صفحة **معالجة موازنة محوّلة للمشروع**، في علامة التبويب **خيارات نهاية السنة**، تأكد من عدم تمكين**المبالغ المحولة لموازنة المشروع المتبقية‬**.</span><span class="sxs-lookup"><span data-stu-id="18a12-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="18a12-111">في علامة التبويب **المعلمات**، في حقل **سنة موازنة المشروع**، حدد بداية العام المالي الذي تريد عرض مبالغ الموازنة المتبقية له.</span><span class="sxs-lookup"><span data-stu-id="18a12-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="18a12-112">في حقل **افتتاح السنة المالية**، حدد بداية العام المالي الذي تريد عرض مبلغ الموازنة المتبقية له.</span><span class="sxs-lookup"><span data-stu-id="18a12-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="18a12-113">في حقل **من نموذج التنبؤ**، حدد **الموازنة المتبقية**.</span><span class="sxs-lookup"><span data-stu-id="18a12-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="18a12-114">لتضمين المشاريع التي تفي بمعاييرك المحددة وليس لديها أي موازنة متبقية، حدد **إظهار القيمة صفر متبقية**.</span><span class="sxs-lookup"><span data-stu-id="18a12-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="18a12-115">في علامة التبويب **تحديد الموازنات**، حددد **استرداد جميع الموازنات** لتحميل جميع الموازنات التي تطابق معاييرك المحددة، ثم حدد **معالجة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="18a12-116">لتصميم استعلام قاعدة البيانات التي تقوم بتحميل مجموعة محددة من الموازنات إلى الجزء، حدد **استرداد الموازنات المحددة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="18a12-117">لمزيد من المعلومات حول بند معين في الجزء، حدد البند، ثم حدد **عرض تفاصيل الموازنة** أو**عرض الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="18a12-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="18a12-118">المبالغ المحولة للموازنة المتبقية</span><span class="sxs-lookup"><span data-stu-id="18a12-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="18a12-119">عندما تقوم بمعالجة مبالغ الموازنة المتبقية، يمكنك إنشاء حركات في دفتر الأستاذ العام للمبالغ التي تقوم بتحويلها.</span><span class="sxs-lookup"><span data-stu-id="18a12-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="18a12-120">لإنشاء حركات دفتر أستاذ عام، قم باستكمال الخطوات الموجودة في قسم [تحويل مبالغ الموازنة، وإنشاء حركات دفتر الأستاذ العام‬](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="18a12-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="18a12-121">يتم نقل مبالغ الموازنة التي يتم تحويلها إلى نموذج التنبؤ المحدد كنموذج تنبؤ تحويل في صفحة **نماذج التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="18a12-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="18a12-122">تحويل مبالغ الموازنة، وإنشاء حركات دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="18a12-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="18a12-123">حدد **إدارة المشاريع ومحاسبتها** > **دوري** > **الموازنات** > **الموازنات المحولة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="18a12-124">في صفحة **صفحة معالجة موازنة محوّلة للمشروع‬**، حدد **نهاية السنة**، وقم بتمكين **المبالغ المحولة لموازنة المشروع المتبقية‬** و**إنشاء إدخالات سجلات الموازنة في دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="18a12-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="18a12-125">في علامة التبويب **المعلمات**، في مجموعة حقول **معلمات المشروع**، حدد ما يلي:</span><span class="sxs-lookup"><span data-stu-id="18a12-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="18a12-126">**عام موازنة المشروع**: تحديد بداية العام المالي الذي تريد عرض مبالغ الموازنة المتبقية له.</span><span class="sxs-lookup"><span data-stu-id="18a12-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="18a12-127">**الربح والخسارة**: إنشاء حركات أرباح وخسائر في دفتر الأستاذ العام، حدد خانة الاختيار .</span><span class="sxs-lookup"><span data-stu-id="18a12-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="18a12-128">**الأعمال تحت التنفيذ**: إنشاء حركات الأعمال تحت التنفيذ (WIP) في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="18a12-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="18a12-129">**كشف الرواتب**: إنشاء حركات توزيع كشف المرتبات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="18a12-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="18a12-130">في مجموعة حقول **دفتر الأستاذ العام**، قدم المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="18a12-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="18a12-131">في **افتتاح العام المالي** حدد العام المالي الذي تريد تحويل مبالغ الموازنة المتبقية الخاصة بالمشاريع له.</span><span class="sxs-lookup"><span data-stu-id="18a12-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="18a12-132">القيمة الافتراضية هي عام واحد بعد القيمة الموجودة في حقل **عام موازنة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="18a12-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="18a12-133">في حقل **فترة الموازنة المحولة**، حدد الفترة التي تريد إنشاء تفاصيل سجل الموازنة فيها في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="18a12-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="18a12-134">وهذه هي الفترة الأولى عادةً في السنة المالية الافتتاحية.</span><span class="sxs-lookup"><span data-stu-id="18a12-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="18a12-135">في مجموعة حقول **نسخ من/إلى**، قدم المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="18a12-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="18a12-136">في حقل **من نموذج التنبؤ**، حدد نموذج تنبؤ موازنة المشروع المرتبط بمبالغ الموازنة المتبقية التي تريد تحويلها للمشاريع.</span><span class="sxs-lookup"><span data-stu-id="18a12-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="18a12-137">في حقل **إلى نموذج موازنة دفتر الأستاذ**، حدد نموذج موازنة دفتر الأستاذ المرتبط بمبالغ الموازنة التي تريد تحويلها لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="18a12-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="18a12-138">حدد **تحويل عملة المبيعات** لاستخدام عملة مبيعات المشروع لحركات دفتر الأستاذ العام التي تم إنشاؤها عند تحويل مبالغ الموازنة للمشاريع.</span><span class="sxs-lookup"><span data-stu-id="18a12-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="18a12-139">في حالة عدم تحديد هذا الخيار، تستخدم الحركات عملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="18a12-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="18a12-140">حدد **إظهار القيمة صفر المتبقية** تضمين المشاريع التي لا تحتوي على أي مبالغ موازنة متبقية، ولكنها تستوفي المعايير الأخرى التي تقوم بتحديدها في المشاريع المعروضة في الجزء السفلي.</span><span class="sxs-lookup"><span data-stu-id="18a12-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="18a12-141">في علامة التبويب **تحديد الموازنات**، حدد **استرداد جميع الموازنات** لتحميل جميع الموازنات التي تطابق المعايير التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="18a12-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="18a12-142">إذا كنت تفضل تصميم استعلام قاعدة البيانات التي تقوم بتحميل مجموعة محددة من موازنات المشاريع إلى الجزء، حدد **استرداد الموازنات المحددة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="18a12-143">فيما يخص كل مشروع تريد معالجته، حدد الخيار الموجود في بداية بند المشروع.</span><span class="sxs-lookup"><span data-stu-id="18a12-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="18a12-144">لتحديد جميع المشاريع أو معظمها، حدد علامة الاختيار في الركن العلوي الأيسر بالجانب العلوي.</span><span class="sxs-lookup"><span data-stu-id="18a12-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="18a12-145">لاستثناء معالجة أي مشروع، قم بإلغاء تحديد علامة الاختيار الخاصة بذلك المشروع.</span><span class="sxs-lookup"><span data-stu-id="18a12-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="18a12-146">لتحويل مبالغ الموازنة المتبقية للمشاريع المحددة للسنة المالية المحددة وإنشاء تفاصيل سجل الموازنة في دفتر الأستاذ العام، حدد **معالجة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="18a12-147">تحويل مبالغ الموازنة دون إنشاء حركات دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="18a12-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="18a12-148">انتقل إلى **إدارة المشاريع ومحاسبتها** > **دوري** > **الموازنات** > **الموازنات المحولة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="18a12-149">في صفحة **معالجة موازنة محوّلة للمشروع**، في علامة التبويب **خيارات نهاية السنة**، حدد **المبالغ المحولة لموازنة المشروع المتبقية‬**.</span><span class="sxs-lookup"><span data-stu-id="18a12-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="18a12-150">في مجموعة **المعلمات**، في حقل **سنة موازنة المشروع**، حدد العام المالي الذي تريد عرض مبالغ الموازنة المتبقية له.</span><span class="sxs-lookup"><span data-stu-id="18a12-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="18a12-151">في مجموعة **نسخ من/إلى**، قدم المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="18a12-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="18a12-152">في حقل **من نموذج التنبؤ**، حدد نموذج تنبؤ موازنة المشروع المرتبط بمبالغ الموازنة المتبقية التي تريد تحويلها للمشاريع.</span><span class="sxs-lookup"><span data-stu-id="18a12-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="18a12-153">حدد **إظهار القيمة صفر المتبقية** لتضمين المشاريع التي لا تشتمل على أي مبالغ موازنة متبقية ولكنها تفي بالمعايير الأخرى التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="18a12-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="18a12-154">في مجموعة **تحديد الموازنات**، حدد **استرداد جميع الموازنات** لتحميل جميع الموازنات التي تطابق المعايير التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="18a12-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="18a12-155">لتصميم استعلام قاعدة البيانات التي تقوم بتحميل مجموعة محددة من موازنات المشاريع إلى الجزء، حدد **استرداد الموازنات المحددة**.</span><span class="sxs-lookup"><span data-stu-id="18a12-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="18a12-156">فيما يخص كل مشروع تريد معالجته، حدد الخيار الموجود في بداية بند المشروع.</span><span class="sxs-lookup"><span data-stu-id="18a12-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="18a12-157">حدد **معالجة** لتحويل مبالغ الموازنة المتبقية للمشاريع المحددة للعام المالي المحدد.</span><span class="sxs-lookup"><span data-stu-id="18a12-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

