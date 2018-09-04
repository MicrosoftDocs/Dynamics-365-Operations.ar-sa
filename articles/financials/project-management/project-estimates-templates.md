---
title: "مزامنة تقديرات المشروع مباشرةً من Project Service Automation إلى Finance and Operations"
description: "يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرةً من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0f2e1-103">مزامنة تقديرات المشروع مباشرةً من Project Service Automation إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f2e1-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f2e1-104">يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="0f2e1-105">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="0f2e1-106">يتوافر تكامل القيم الفعلية في Microsoft Dynamics 365 for Finance and Operations، الإصدار 8.01 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="0f2e1-107">إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستتمكن من استخدام القوالب لإجراء تكامل لمهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية ولتكوين تأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="0f2e1-108">إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0f2e1-109">تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f2e1-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="0f2e1-110">يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f2e1-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="0f2e1-111">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات، تدفق البيانات حول تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0f2e1-112">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="0f2e1-113">[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="0f2e1-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="0f2e1-114">تقديرات ساعات المشروع</span><span class="sxs-lookup"><span data-stu-id="0f2e1-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="0f2e1-115">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="0f2e1-115">Template and tasks</span></span>

<span data-ttu-id="0f2e1-116">للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0f2e1-117">يتم استخدام القالب التالي والمهام الأساسية لمزامنة تقديرات عدد ساعات المشروع من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="0f2e1-118">**اسم القالب في تكامل البيانات:** تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0f2e1-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0f2e1-119">**أسماء المهام في المشروع:**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="0f2e1-120">علاقات الحركات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-120">Transaction relationships</span></span>
    - <span data-ttu-id="0f2e1-121">تقديرات المصروفات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="0f2e1-122">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-122">Entity set</span></span>

| <span data-ttu-id="0f2e1-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0f2e1-123">Project Service Automation</span></span> | <span data-ttu-id="0f2e1-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f2e1-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0f2e1-125">مهام المشروع</span><span class="sxs-lookup"><span data-stu-id="0f2e1-125">Project tasks</span></span>              | <span data-ttu-id="0f2e1-126">كيان تكامل تقديرات عدد الساعات للمشروع</span><span class="sxs-lookup"><span data-stu-id="0f2e1-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="0f2e1-127">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="0f2e1-127">Entity flow</span></span>

<span data-ttu-id="0f2e1-128">تتم إدارة تقديرات عدد ساعات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كتنبؤات عدد ساعات المشروع.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0f2e1-129">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="0f2e1-129">Prerequisites</span></span>

<span data-ttu-id="0f2e1-130">قبل القيام بمزامنة تقديرات عدد ساعات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0f2e1-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="0f2e1-131">Power Query</span></span>

<span data-ttu-id="0f2e1-132">في قالب تقديرات ساعات المشروع، يجب عليك استخدام Microsoft Power Query لـ Excel لإكمال هذه المهام:</span><span class="sxs-lookup"><span data-stu-id="0f2e1-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="0f2e1-133">تعيين معرّف نموذج التنبؤ الافتراضي الذي سيتم استخدامه عندما ينشئ التكامل تنبؤات عدد ساعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="0f2e1-134">تصفية سجلات خاصة بالموارد في المهمة التي سوف تفشل التكامل في تنبؤات عدد الساعات .</span><span class="sxs-lookup"><span data-stu-id="0f2e1-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="0f2e1-135">قم بتصفية أي صفوف فئات حركات فارغة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="0f2e1-136">قد يؤدي الفشل في إكمال هذه المهمة إلى تنبؤات عدد ساعات غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="0f2e1-137">تعيين معرّف نموذج التنبؤ الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0f2e1-137">Set the default forecast model ID</span></span>

<span data-ttu-id="0f2e1-138">لتحديث مُعرف نموذج التنبؤ الافتراضي في القالب، انقر فوق سهم **تعيين** لفتح التعيين.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0f2e1-139">ثم حدد الارتباط **الاستعلام المتقدم والتصفية**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="0f2e1-140">إذا كنت تستخدم قالب تقديرات ساعات المشروع الافتراضية (PSA إلى Fin and Ops)، فحدد **الشرط المُدرج** في قائمة **الخطوات المُطبقة**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="0f2e1-141">في إدخال **الوظيفة**، استبدل **O\_forecast** باسم معرّف نموذج التنبؤ الذي يتعين استخدامه مع التكامل.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="0f2e1-142">يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="0f2e1-143">إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="0f2e1-144">في Power Query، حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود الجديد، مثل **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="0f2e1-145">أدخل الشرط للعمود بحيث إذا لم تكن مهمة المشروع بقيمة null، عندئذٍ \<أدخل معرّف نموذج التنبؤ\>؛ وإلا null.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="0f2e1-146">تصفية سجلات خاصة بالموارد</span><span class="sxs-lookup"><span data-stu-id="0f2e1-146">Filter out resource-specific records</span></span>

<span data-ttu-id="0f2e1-147">يحتوي قالب تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops) على عامل تصفية افتراضي يقوم بإزالة أي سجلات خاصة بالموارد.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="0f2e1-148">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="0f2e1-149">حدد الارتباط **الاستعلام المتقدم والتصفية** لإجراء التصفية على العمود **msdyn\_islinetask** بحيث لا يتم تضمين سوى السجلات ذات القيمة **False**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="0f2e1-150">تصفية صفوف فئات حركات فارغة</span><span class="sxs-lookup"><span data-stu-id="0f2e1-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="0f2e1-151">يجب إضافة عامل تصفية لإزالة أي صفوف تتضمن فئات حركات فارغة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="0f2e1-152">تعتبر هذه المهمة ضرورية، بصرف النظر عما إذا كنت تستخدم القالب الافتراضي أو تعمل على إنشاء قالبك الخاص.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="0f2e1-153">يزيل عامل التصفية هذا بإزالة أي صفوف ملخص واردة من Project Service Automation قد تتسبب في حدوث خطأ في تنبؤات عدد الساعات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="0f2e1-154">حدد الارتباط **الاستعلام المتقدم والتصفية** لتصفية السجلات ذات القيمة null في العمود **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0f2e1-155">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-155">Template mapping in Data integration</span></span>

<span data-ttu-id="0f2e1-156">يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="0f2e1-157">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0f2e1-158">[![تعيين القالب](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0f2e1-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="0f2e1-159">‏‏تقديرات مصروفات المشروع</span><span class="sxs-lookup"><span data-stu-id="0f2e1-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="0f2e1-160">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="0f2e1-160">Template and tasks</span></span>

<span data-ttu-id="0f2e1-161">يتم استخدام القالب التالي والمهام الأساسية التالية لمزامنة تقديرات مصروفات المشروع من Project Service Automation إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="0f2e1-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="0f2e1-162">**اسم القالب في تكامل البيانات:** تقديرات مصروفات المشروع (PSA إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0f2e1-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0f2e1-163">**أسماء المهام في المشروع:**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="0f2e1-164">علاقات الحركات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-164">Transaction relationships</span></span> 
    - <span data-ttu-id="0f2e1-165">تقديرات المصروفات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="0f2e1-166">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-166">Entity set</span></span>

| <span data-ttu-id="0f2e1-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0f2e1-167">Project Service Automation</span></span> | <span data-ttu-id="0f2e1-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f2e1-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="0f2e1-169">اتصالات الحركات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-169">Transaction Connections</span></span>    | <span data-ttu-id="0f2e1-170">كيان التكامل لعلاقات حركات المشروع</span><span class="sxs-lookup"><span data-stu-id="0f2e1-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="0f2e1-171">بنود التقدير</span><span class="sxs-lookup"><span data-stu-id="0f2e1-171">Estimate Lines</span></span>             | <span data-ttu-id="0f2e1-172">كيان تكامل تقديرات المصروفات للمشروع</span><span class="sxs-lookup"><span data-stu-id="0f2e1-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="0f2e1-173">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="0f2e1-173">Entity flow</span></span>

<span data-ttu-id="0f2e1-174">تتم إدارة تقديرات مصروفات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كتنبؤات مصروفات المشروع.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0f2e1-175">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="0f2e1-175">Prerequisites</span></span>

<span data-ttu-id="0f2e1-176">قبل القيام بمزامنة تقديرات مصروفات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0f2e1-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="0f2e1-177">Power Query</span></span>

<span data-ttu-id="0f2e1-178">يجب عليك استخدام Power Query في قالب تقديرات مصروفات المشروع لإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="0f2e1-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="0f2e1-179">التصفية لتضمين سجلات بنود تقدير المصروفات فقط.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="0f2e1-180">تعيين معرّف نموذج التنبؤ الافتراضي الذي سيتم استخدامه عندما ينشئ التكامل تنبؤات عدد ساعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="0f2e1-181">تحويل أنواع الفوترة.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-181">Transform the billing types.</span></span>
- <span data-ttu-id="0f2e1-182">تحويل أنواع الحركات.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="0f2e1-183">التصفية لتضمين بنود تقدير المصروفات فقط</span><span class="sxs-lookup"><span data-stu-id="0f2e1-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="0f2e1-184">يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يتضمن فقط بنود المصروفات في التكامل.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="0f2e1-185">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="0f2e1-186">حدد مهمة **علاقات الحركة** ثم انقر فوق السهم **تعيين‏‎** لفتح التعيين.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0f2e1-187">حدد الارتباط **الاستعلام المتقدم والتصفية**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="0f2e1-188">قم بتصفية العمود **msdyn\_transactiontype1** بحيث يتضمن **msdyn\_estimateline** فقط.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="0f2e1-189">تعيين معرّف نموذج التنبؤ الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0f2e1-189">Set the default forecast model ID</span></span>

<span data-ttu-id="0f2e1-190">لتحديث معرّف نموذج التنبؤ الافتراضي في القالب، حدد مهمة **تقديرات المصروفات**، ثم انقر فوق السهم **تعيين‏‎** لفتح التعيين.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0f2e1-191">حدد الارتباط **الاستعلام المتقدم والتصفية**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="0f2e1-192">إذا كنت تستخدم قالب تقديرات مصروفات المشروع الافتراضي (PSA إلى Fin and Ops)، في Power Query، حدد **الشرط المُدرج** الأول من قسم **الخطوات المُطبقة**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="0f2e1-193">في إدخال **الوظيفة**، استبدل **O\_forecast** باسم معرّف نموذج التنبؤ الذي يتعين استخدامه مع التكامل.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="0f2e1-194">يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="0f2e1-195">إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="0f2e1-196">في Power Query، حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود الجديد، مثل **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="0f2e1-197">أدخل الشرط للعمود بحيث إذا لم يكن معرّف بند التقدير بقيمة null، عندئذٍ \<أدخل معرّف نموذج التنبؤ\>؛ وإلا null.‬</span><span class="sxs-lookup"><span data-stu-id="0f2e1-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="0f2e1-198">تحويل أنواع الفوترة</span><span class="sxs-lookup"><span data-stu-id="0f2e1-198">Transform the billing types</span></span>

<span data-ttu-id="0f2e1-199">يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عمودًا شرطيُا يُستخدم لتحويل أنواع الفوترة المستلمة من Project Service Automation خلال التكامل.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="0f2e1-200">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="0f2e1-201">حدد الارتباط **الاستعلام المتقدم والتصفية** ثم حدد **إضافة عمود شرطي**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="0f2e1-202">أدخل اسمًا للعمود الجديد، مثل **BillingType‎**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="0f2e1-203">بعد ذلك، أدخل الشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="0f2e1-203">Then enter the following condition:</span></span>

<span data-ttu-id="0f2e1-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="0f2e1-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="0f2e1-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="0f2e1-207">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="0f2e1-208">تحويل أنواع الحركات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-208">Transform the transaction types</span></span>

<span data-ttu-id="0f2e1-209">يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عمودًا شرطيُا يُستخدم لتحويل أنواع الحركات المستلمة من Project Service Automation خلال التكامل.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="0f2e1-210">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="0f2e1-211">حدد الارتباط **الاستعلام المتقدم والتصفية** ثم حدد **إضافة عمود شرطي**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="0f2e1-212">أدخل اسمًا للعمود الجديد، مثل **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="0f2e1-213">بعد ذلك، أدخل الشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="0f2e1-213">Then enter the following condition:</span></span>

<span data-ttu-id="0f2e1-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="0f2e1-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="0f2e1-216">else **null**</span><span class="sxs-lookup"><span data-stu-id="0f2e1-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0f2e1-217">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="0f2e1-217">Template mapping in Data integration</span></span>

<span data-ttu-id="0f2e1-218">يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="0f2e1-219">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f2e1-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0f2e1-220">[![تعيين القالب](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0f2e1-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="0f2e1-221">[![تعيين القالب](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0f2e1-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
