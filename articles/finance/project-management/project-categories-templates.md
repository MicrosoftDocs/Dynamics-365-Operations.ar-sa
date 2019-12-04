---
title: مزامنة فئات مصروفات المشروع بين Finance and Operations و Project Service Automation
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بين Dynamics 365 Finance Microsoft و Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770302"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="ecf93-103">مزامنة فئات مصروفات المشروع بين Finance and Operations و Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ecf93-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ecf93-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بين Dynamics 365 Finance وDynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ecf93-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="ecf93-105">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0.</span><span class="sxs-lookup"><span data-stu-id="ecf93-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="ecf93-106">يتوفر تكامل القيم الفعلية في الإصدار 8.0.1 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="ecf93-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="ecf93-107">إذا كنت تستخدم , Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="ecf93-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="ecf93-108">إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.</span><span class="sxs-lookup"><span data-stu-id="ecf93-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="ecf93-109">تدفق البيانات الخاصة بـ Project Service Automation إلى Finance</span><span class="sxs-lookup"><span data-stu-id="ecf93-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="ecf93-110">يستخدم الحل المتكامل لـ Project Service Automation وFinance ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation وFinance</span><span class="sxs-lookup"><span data-stu-id="ecf93-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ecf93-111">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بفئات حركات مصروفات المشروع بين Finance وProject Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ecf93-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="ecf93-112">إذا تمت إدارة في فئات مصروفات المشروع في Finance، فيكون تدفق التكامل أولًا من Finance إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ecf93-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="ecf93-113">يتم عندئذٍ تحديث معرّفات التكامل لفئات مصروفات المشروع عبر المزامنة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf93-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ecf93-114">إذا تم التحكم في فئات مصروفات المشروع في Project Service Automation، فيكون تدفق التكامل أولًا من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf93-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="ecf93-115">يجب تكوين فئات المشروع بشكل مسبق في Finance قبل إجراء المزامنة من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ecf93-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="ecf93-116">ثم نفّذ المزامنة من Finance مرة أخرى إلى Project Service Automation، ثم من Project Service Automation إلى Finance مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ecf93-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="ecf93-117">بهذه الطريقة، يمكنك المساعدة في ضمان الحصول على فئات مرتبطة وعدم إنشاء أي تكرارات.</span><span class="sxs-lookup"><span data-stu-id="ecf93-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="ecf93-118">تتم عادةً إدارة فئات مصروفات المشروع في Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf93-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="ecf93-119">ومع ذلك، إذا لم تتم إدارتها، أو إذا تم إنشاء فئات المصروفات بشكل مسبق في Project Service Automation، فيجب عليك إجراء المزامنة أولاً باستخدام قالب فئات حركات مصروفات المشروع (PSA إلى Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="ecf93-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="ecf93-120">ثم نفّذ المزامنة باستخدام قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA).</span><span class="sxs-lookup"><span data-stu-id="ecf93-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="ecf93-121">يجب بعد ذلك تشغيل المزامنة من Project Service Automation إلى Finance مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ecf93-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="ecf93-122">إذ أجريت المزامنة من Project Service Automation أولاً، فيجب تلبية المتطلبات التالية في Finance قبل تشغيل عملية المزامنة:</span><span class="sxs-lookup"><span data-stu-id="ecf93-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="ecf93-123">يلزم وجود الفئة المشتركة التي تتطابق مع فئة المشروع التي تم إعدادها في Project Service Automation، ويجب تمكينها لكل من **المشروع** و**المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="ecf93-124">لكل كيان قانوني في Finance يجب دمجه فيه، يلزم وجود فئات المشروع التالية:</span><span class="sxs-lookup"><span data-stu-id="ecf93-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="ecf93-125">**فئة المشروع** موجودة.</span><span class="sxs-lookup"><span data-stu-id="ecf93-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="ecf93-126">تمكين **الاستخدام في المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="ecf93-127">تمكين **نشط في دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="ecf93-128">تعيين **نوع الحركة** إلى **مصروفات**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="ecf93-129">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf93-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ecf93-130">[![تدفق البيانات الخاصة بتكامل Project Service Automation مع Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ecf93-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="ecf93-131">مزامنة فئات مصروفات المشروع من Finance إلى Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ecf93-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ecf93-132">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="ecf93-132">Template and task</span></span>

<span data-ttu-id="ecf93-133">للوصول إلى القالب، في مركز إدارة Microsoft Power Apps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="ecf93-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ecf93-134">يتم استخدام القالب والمهمة الأساسية التالية لمزامنة فئات مصروفات المشروع من Finance إلى Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="ecf93-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="ecf93-135">**اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (Fin and Ops إلى PSA)</span><span class="sxs-lookup"><span data-stu-id="ecf93-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="ecf93-136">**اسم المهمة في المشروع:** مزامنة الفئات إلى PSA</span><span class="sxs-lookup"><span data-stu-id="ecf93-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="ecf93-137">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="ecf93-137">Entity set</span></span>

| <span data-ttu-id="ecf93-138">المالية</span><span class="sxs-lookup"><span data-stu-id="ecf93-138">Finance</span></span>                           | <span data-ttu-id="ecf93-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ecf93-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="ecf93-140">كيان التكامل للفئات</span><span class="sxs-lookup"><span data-stu-id="ecf93-140">Integration entity for categories</span></span> | <span data-ttu-id="ecf93-141">فئات الحركات</span><span class="sxs-lookup"><span data-stu-id="ecf93-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="ecf93-142">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="ecf93-142">Entity flow</span></span>

<span data-ttu-id="ecf93-143">تتم إدارة فئات مصروفات المشروع في Finance، وتتم مزامنتها لـ Project Service Automation كفئات حركات.</span><span class="sxs-lookup"><span data-stu-id="ecf93-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ecf93-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="ecf93-144">Power Query</span></span>

<span data-ttu-id="ecf93-145">عند المزامنة إلى Project Service Automation، يجب عليك استخدام Microsoft Power Query لـ Excel لتعيين نوع الفوترة في فئة الحركة.</span><span class="sxs-lookup"><span data-stu-id="ecf93-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="ecf93-146">يوفر قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA) تعيينًا وعمودًا افتراضيًا.</span><span class="sxs-lookup"><span data-stu-id="ecf93-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="ecf93-147">إذا قمت بإنشاء قالبك الخاص، يجب عليك إضافة عمود شرطي في Power Query.</span><span class="sxs-lookup"><span data-stu-id="ecf93-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="ecf93-148">اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ecf93-148">Follow these steps.</span></span>

1. <span data-ttu-id="ecf93-149">انقر فوق السهم لفتح تعيين مهمة فئات حركات مصروفات المشروع في قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA).</span><span class="sxs-lookup"><span data-stu-id="ecf93-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="ecf93-150">انقر فوق الارتباط **الاستعلام المتقدم والتصفية** لفتح Power Query.</span><span class="sxs-lookup"><span data-stu-id="ecf93-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="ecf93-151">حدد **إضافة عمود شرطي**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="ecf93-152">أدخل اسمًا للعمود الجديد، مثل **BillingType‎**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="ecf93-153">أدخل الشرط التالي: **إذا لم تكن قيمة CATEGORYID تساوي null، عندئذٍ 19235001، وإلا null**.</span><span class="sxs-lookup"><span data-stu-id="ecf93-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="ecf93-154">انقر فوق **موافق** في العمود.</span><span class="sxs-lookup"><span data-stu-id="ecf93-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="ecf93-155">تأكد من تعيين هذا العمود الجديد في صفحة التعيين.</span><span class="sxs-lookup"><span data-stu-id="ecf93-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="ecf93-156">يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ecf93-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ecf93-157">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ecf93-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="ecf93-158">[![تعيين القالب](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ecf93-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="ecf93-159">مزامنة فئات مصروفات المشروع من Project Service Automation إلى Finance</span><span class="sxs-lookup"><span data-stu-id="ecf93-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ecf93-160">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="ecf93-160">Template and task</span></span>

<span data-ttu-id="ecf93-161">يتم استخدام القالب والمهمة الأساسية التالية لمزامنة فئات مصروفات المشروع من من Project Service Automation إلى Finance:</span><span class="sxs-lookup"><span data-stu-id="ecf93-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ecf93-162">**اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (PSA إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ecf93-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ecf93-163">**اسم المهمة في المشروع:** مزامنة الفئات إلى Fin Ops</span><span class="sxs-lookup"><span data-stu-id="ecf93-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="ecf93-164">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="ecf93-164">Entity set</span></span>

| <span data-ttu-id="ecf93-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ecf93-165">Project Service Automation</span></span> | <span data-ttu-id="ecf93-166">المالية</span><span class="sxs-lookup"><span data-stu-id="ecf93-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="ecf93-167">فئات الحركات</span><span class="sxs-lookup"><span data-stu-id="ecf93-167">Transaction categories</span></span>     | <span data-ttu-id="ecf93-168">كيان التكامل للفئات</span><span class="sxs-lookup"><span data-stu-id="ecf93-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ecf93-169">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="ecf93-169">Entity flow</span></span>

<span data-ttu-id="ecf93-170">تتم إدارة فئات مصروفات المشروع في Finance، وتتم مزامنتها لـ Project Service Automation كفئات حركات.</span><span class="sxs-lookup"><span data-stu-id="ecf93-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="ecf93-171">تؤدي المزامنة مرة أخرى إلى Finance إلى تحديث فئة المشروع في Finance مع معرّف التكامل من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ecf93-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ecf93-172">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="ecf93-172">Template mapping in Data integration</span></span>

<span data-ttu-id="ecf93-173">يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ecf93-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ecf93-174">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf93-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ecf93-175">[![تعيين القالب](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ecf93-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
