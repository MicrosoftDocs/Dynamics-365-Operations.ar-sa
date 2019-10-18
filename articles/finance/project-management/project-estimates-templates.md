---
title: مزامنة تقديرات المشروع مباشرةً من Project Service Automation إلى Finance and Operations
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرة من Dynamics 365 Project Service Automation Microsoft إلى Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250474"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3a5b9-103">مزامنة تقديرات المشروع مباشرةً من Project Service Automation إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3a5b9-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3a5b9-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرة من Dynamics 365 Project Service Automation إلى Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3a5b9-105">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="3a5b9-106">يتوفر تكامل القيم الفعلية في الإصدار 8.0.1 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="3a5b9-107">تدفق البيانات الخاصة بـ Project Service Automation إلى Finance</span><span class="sxs-lookup"><span data-stu-id="3a5b9-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="3a5b9-108">يستخدم الحل المتكامل لـ Project Service Automation إلى Finance ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation وFinance</span><span class="sxs-lookup"><span data-stu-id="3a5b9-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="3a5b9-109">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات، تدفق البيانات حول تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3a5b9-110">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="3a5b9-111">[![تدفق البيانات الخاصة بتكامل Project Service Automation مع Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="3a5b9-112">تقديرات ساعات المشروع</span><span class="sxs-lookup"><span data-stu-id="3a5b9-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3a5b9-113">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="3a5b9-113">Template and tasks</span></span>

<span data-ttu-id="3a5b9-114">للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-114">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3a5b9-115">يتم استخدام القالب التالي والمهام الأساسية لمزامنة تقديرات عدد ساعات المشروع من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3a5b9-116">**اسم القالب في تكامل البيانات:** تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3a5b9-117">**أسماء المهام في المشروع:**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3a5b9-118">علاقات الحركات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-118">Transaction relationships</span></span>
    - <span data-ttu-id="3a5b9-119">تقديرات المصروفات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3a5b9-120">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-120">Entity set</span></span>

| <span data-ttu-id="3a5b9-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3a5b9-121">Project Service Automation</span></span> | <span data-ttu-id="3a5b9-122">المالية</span><span class="sxs-lookup"><span data-stu-id="3a5b9-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="3a5b9-123">مهام المشروع</span><span class="sxs-lookup"><span data-stu-id="3a5b9-123">Project tasks</span></span>              | <span data-ttu-id="3a5b9-124">كيان تكامل تقديرات عدد الساعات للمشروع</span><span class="sxs-lookup"><span data-stu-id="3a5b9-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="3a5b9-125">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="3a5b9-125">Entity flow</span></span>

<span data-ttu-id="3a5b9-126">تتم إدارة تقديرات عدد ساعات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance كتنبؤات عدد ساعات المشروع.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3a5b9-127">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="3a5b9-127">Prerequisites</span></span>

<span data-ttu-id="3a5b9-128">قبل القيام بمزامنة تقديرات عدد ساعات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3a5b9-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="3a5b9-129">Power Query</span></span>

<span data-ttu-id="3a5b9-130">في قالب تقديرات ساعات المشروع، يجب عليك استخدام Microsoft Power Query لـ Excel لإكمال هذه المهام:</span><span class="sxs-lookup"><span data-stu-id="3a5b9-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="3a5b9-131">تعيين معرّف نموذج التنبؤ الافتراضي الذي سيتم استخدامه عندما ينشئ التكامل تنبؤات عدد ساعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3a5b9-132">تصفية سجلات خاصة بالموارد في المهمة التي سوف تفشل التكامل في تنبؤات عدد الساعات .</span><span class="sxs-lookup"><span data-stu-id="3a5b9-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="3a5b9-133">قم بتصفية أي صفوف فئات حركات فارغة.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="3a5b9-134">قد يؤدي الفشل في إكمال هذه المهمة إلى تنبؤات عدد ساعات غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3a5b9-135">تعيين معرّف نموذج التنبؤ الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3a5b9-135">Set the default forecast model ID</span></span>

<span data-ttu-id="3a5b9-136">لتحديث مُعرف نموذج التنبؤ الافتراضي في القالب، انقر فوق سهم **تعيين** لفتح التعيين.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3a5b9-137">ثم حدد الارتباط **الاستعلام المتقدم والتصفية**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3a5b9-138">إذا كنت تستخدم قالب تقديرات ساعات المشروع الافتراضية (PSA إلى Fin and Ops)، فحدد **الشرط المُدرج** في قائمة **الخطوات المُطبقة**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="3a5b9-139">في إدخال **الوظيفة**، استبدل **O\_forecast** باسم معرّف نموذج التنبؤ الذي يتعين استخدامه مع التكامل.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3a5b9-140">يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3a5b9-141">إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3a5b9-142">في Power Query، حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود الجديد، مثل **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3a5b9-143">أدخل الشرط للعمود بحيث إذا لم تكن مهمة المشروع بقيمة null، عندئذٍ \<أدخل معرّف نموذج التنبؤ\>؛ وإلا null.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="3a5b9-144">تصفية سجلات خاصة بالموارد</span><span class="sxs-lookup"><span data-stu-id="3a5b9-144">Filter out resource-specific records</span></span>

<span data-ttu-id="3a5b9-145">يحتوي قالب تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops) على عامل تصفية افتراضي يقوم بإزالة أي سجلات خاصة بالموارد.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="3a5b9-146">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3a5b9-147">حدد الارتباط **الاستعلام المتقدم والتصفية** لإجراء التصفية على العمود **msdyn\_islinetask** بحيث لا يتم تضمين سوى السجلات ذات القيمة **False**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="3a5b9-148">تصفية صفوف فئات حركات فارغة</span><span class="sxs-lookup"><span data-stu-id="3a5b9-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="3a5b9-149">يجب إضافة عامل تصفية لإزالة أي صفوف تتضمن فئات حركات فارغة.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="3a5b9-150">تعتبر هذه المهمة ضرورية، بصرف النظر عما إذا كنت تستخدم القالب الافتراضي أو تعمل على إنشاء قالبك الخاص.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="3a5b9-151">يزيل عامل التصفية هذا بإزالة أي صفوف ملخص واردة من Project Service Automation قد تتسبب في حدوث خطأ في تنبؤات عدد الساعات في Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="3a5b9-152">حدد الارتباط **الاستعلام المتقدم والتصفية** لتصفية السجلات ذات القيمة null في العمود **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3a5b9-153">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-153">Template mapping in Data integration</span></span>

<span data-ttu-id="3a5b9-154">يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="3a5b9-155">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3a5b9-156">[![تعيين القالب](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="3a5b9-157">‏‏تقديرات مصروفات المشروع</span><span class="sxs-lookup"><span data-stu-id="3a5b9-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3a5b9-158">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="3a5b9-158">Template and tasks</span></span>

<span data-ttu-id="3a5b9-159">يتم استخدام القالب التالي والمهام الأساسية لمزامنة تقديرات مصروفات المشروع من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3a5b9-160">**اسم القالب في تكامل البيانات:** تقديرات مصروفات المشروع (PSA إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3a5b9-161">**أسماء المهام في المشروع:**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3a5b9-162">علاقات الحركات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-162">Transaction relationships</span></span> 
    - <span data-ttu-id="3a5b9-163">تقديرات المصروفات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3a5b9-164">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-164">Entity set</span></span>

| <span data-ttu-id="3a5b9-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3a5b9-165">Project Service Automation</span></span> | <span data-ttu-id="3a5b9-166">المالية</span><span class="sxs-lookup"><span data-stu-id="3a5b9-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="3a5b9-167">اتصالات الحركات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-167">Transaction Connections</span></span>    | <span data-ttu-id="3a5b9-168">كيان التكامل لعلاقات حركات المشروع</span><span class="sxs-lookup"><span data-stu-id="3a5b9-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="3a5b9-169">بنود التقدير</span><span class="sxs-lookup"><span data-stu-id="3a5b9-169">Estimate Lines</span></span>             | <span data-ttu-id="3a5b9-170">كيان تكامل تقديرات المصروفات للمشروع</span><span class="sxs-lookup"><span data-stu-id="3a5b9-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="3a5b9-171">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="3a5b9-171">Entity flow</span></span>

<span data-ttu-id="3a5b9-172">تتم إدارة تقديرات مصروفات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance كتنبؤات مصروفات المشروع.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3a5b9-173">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="3a5b9-173">Prerequisites</span></span>

<span data-ttu-id="3a5b9-174">قبل القيام بمزامنة تقديرات مصروفات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3a5b9-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="3a5b9-175">Power Query</span></span>

<span data-ttu-id="3a5b9-176">يجب عليك استخدام Power Query في قالب تقديرات مصروفات المشروع لإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="3a5b9-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="3a5b9-177">التصفية لتضمين سجلات بنود تقدير المصروفات فقط.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="3a5b9-178">تعيين معرّف نموذج التنبؤ الافتراضي الذي سيتم استخدامه عندما ينشئ التكامل تنبؤات عدد ساعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3a5b9-179">تحويل أنواع الفوترة.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-179">Transform the billing types.</span></span>
- <span data-ttu-id="3a5b9-180">تحويل أنواع الحركات.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="3a5b9-181">التصفية لتضمين بنود تقدير المصروفات فقط</span><span class="sxs-lookup"><span data-stu-id="3a5b9-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="3a5b9-182">يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يتضمن فقط بنود المصروفات في التكامل.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="3a5b9-183">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3a5b9-184">حدد مهمة **علاقات الحركة** ثم انقر فوق السهم **تعيين‏‎** لفتح التعيين.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3a5b9-185">حدد الارتباط **الاستعلام المتقدم والتصفية**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="3a5b9-186">قم بتصفية العمود **msdyn\_transactiontype1** بحيث يتضمن **msdyn\_estimateline** فقط.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3a5b9-187">تعيين معرّف نموذج التنبؤ الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3a5b9-187">Set the default forecast model ID</span></span>

<span data-ttu-id="3a5b9-188">لتحديث معرّف نموذج التنبؤ الافتراضي في القالب، حدد مهمة **تقديرات المصروفات**، ثم انقر فوق السهم **تعيين‏‎** لفتح التعيين.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3a5b9-189">حدد الارتباط **الاستعلام المتقدم والتصفية**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3a5b9-190">إذا كنت تستخدم قالب تقديرات مصروفات المشروع الافتراضي (PSA إلى Fin and Ops)، في Power Query، حدد **الشرط المُدرج** الأول من قسم **الخطوات المُطبقة**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="3a5b9-191">في إدخال **الوظيفة**، استبدل **O\_forecast** باسم معرّف نموذج التنبؤ الذي يتعين استخدامه مع التكامل.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3a5b9-192">يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3a5b9-193">إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3a5b9-194">في Power Query، حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود الجديد، مثل **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3a5b9-195">أدخل الشرط للعمود بحيث إذا لم يكن معرّف بند التقدير بقيمة null، عندئذٍ \<أدخل معرّف نموذج التنبؤ\>؛ وإلا null.‬</span><span class="sxs-lookup"><span data-stu-id="3a5b9-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="3a5b9-196">تحويل أنواع الفوترة</span><span class="sxs-lookup"><span data-stu-id="3a5b9-196">Transform the billing types</span></span>

<span data-ttu-id="3a5b9-197">يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عمودًا شرطيُا يُستخدم لتحويل أنواع الفوترة المستلمة من Project Service Automation خلال التكامل.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3a5b9-198">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3a5b9-199">حدد الارتباط **الاستعلام المتقدم والتصفية** ثم حدد **إضافة عمود شرطي**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3a5b9-200">أدخل اسمًا للعمود الجديد، مثل **BillingType‎**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="3a5b9-201">بعد ذلك، أدخل الشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="3a5b9-201">Then enter the following condition:</span></span>

<span data-ttu-id="3a5b9-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="3a5b9-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="3a5b9-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="3a5b9-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="3a5b9-206">تحويل أنواع الحركات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-206">Transform the transaction types</span></span>

<span data-ttu-id="3a5b9-207">يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عمودًا شرطيُا يُستخدم لتحويل أنواع الحركات المستلمة من Project Service Automation خلال التكامل.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3a5b9-208">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3a5b9-209">حدد الارتباط **الاستعلام المتقدم والتصفية** ثم حدد **إضافة عمود شرطي**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3a5b9-210">أدخل اسمًا للعمود الجديد، مثل **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="3a5b9-211">بعد ذلك، أدخل الشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="3a5b9-211">Then enter the following condition:</span></span>

<span data-ttu-id="3a5b9-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="3a5b9-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="3a5b9-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3a5b9-215">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="3a5b9-215">Template mapping in Data integration</span></span>

<span data-ttu-id="3a5b9-216">يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="3a5b9-217">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3a5b9-218">[![تعيين القالب](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="3a5b9-219">[![تعيين القالب](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
