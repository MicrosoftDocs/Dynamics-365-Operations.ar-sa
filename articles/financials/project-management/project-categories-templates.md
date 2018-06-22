---
title: "مزامنة فئات مصروفات المشروع من Project Service Automation"
description: "يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بينMicrosoft Dynamics 365 for  Finance and Operations و Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="e1855-103">مزامنة فئات مصروفات المشروع بين Finance and Operations و Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e1855-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="e1855-104">يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بينMicrosoft Dynamics 365 for  Finance and Operations و Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e1855-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="e1855-105">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.</span><span class="sxs-lookup"><span data-stu-id="e1855-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="e1855-106">تدفق البيانات الخاصة بـ Project Service Automation و Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1855-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="e1855-107">يستخدم الحل المتكامل لـ Project Service Automation و Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1855-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="e1855-108">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بفئات حركات مصروفات المشروع بين Project Service Automation و Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1855-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="e1855-109">إذا تم التحكم في فئات مصروفات المشروع في Finance and Operations، يكون تدفق التكامل أولًا من Finance and Operations إلى Project Service Automation، ومن ثم تحديث معرفات تكامل فئات مصروفات المشروع عن طريق المزامنة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1855-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="e1855-110">إذا تم التحكم في فئات مصروفات المشروع في Project Service Automation، فيكون تدفق التكامل أولًا من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1855-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="e1855-111">يجب أن تكون فئات المشروع قد تم تكوينها مسبقًا في Finance and Operations للمزامنة من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e1855-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="e1855-112">ثم المزامنة من Finance and Operations مرة أخرى إلى Project Service Automation، ثم من Project Service Automation إلى Finance and Operations مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="e1855-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="e1855-113">يضمن ذلك ارتباط الفئات وعدم إنشاء تكرارات.</span><span class="sxs-lookup"><span data-stu-id="e1855-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="e1855-114">وعادةً، سوف يتم التحكم في فئات مصروفات المشروع في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1855-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="e1855-115">وإذا كان الموقف غير ذلك، أو إذا كان لديك فئات مصروفات تم إنشاؤها مسبقًا في Project Service Automation، يجب عليك أولًا المزامنة باستخدام فئات حركات مصروفات المشروعات (PSA إلى Fin and Ops)، ثم المزامنة باستخدام فئات حركات مصروفات المشروعات (Fin and Ops إلى PSA).</span><span class="sxs-lookup"><span data-stu-id="e1855-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="e1855-116">بعد ذلك، يجب تشغيل المزامنة من PSA إلى Fin and Ops مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="e1855-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="e1855-117">إذا تمت المزامنة لأول مرة من Project Service Automation، يجب أن يتم إعداد فئات المشروع مسبقًا في Finance and Operations، ويجب إعداد فئات المشروع التي تتطلب المزامنة مع فئات حركات Project Service Automation لتكون **نشط في دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="e1855-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="e1855-118">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1855-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="e1855-119">[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e1855-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="e1855-120">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="e1855-120">Templates and tasks</span></span>

<span data-ttu-id="e1855-121">للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="e1855-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e1855-122">يتم استخدام القالب التالي والمهمة الأساسية لمزامنة فئات مصروفات المشروع من Finance and Operations إلى Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="e1855-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="e1855-123">**اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (Fin and Ops إلى PSA)</span><span class="sxs-lookup"><span data-stu-id="e1855-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="e1855-124">**اسم المهمة في المشروع:** مزامنة الفئات إلى PSA</span><span class="sxs-lookup"><span data-stu-id="e1855-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="e1855-125">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="e1855-125">Entity set</span></span>

| <span data-ttu-id="e1855-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1855-126">Finance and Operations</span></span>               | <span data-ttu-id="e1855-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e1855-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="e1855-128">كيان التكامل للفئات</span><span class="sxs-lookup"><span data-stu-id="e1855-128">Integration entity for categories</span></span>    | <span data-ttu-id="e1855-129">فئات الحركات</span><span class="sxs-lookup"><span data-stu-id="e1855-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="e1855-130">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="e1855-130">Entity flow</span></span>

<span data-ttu-id="e1855-131">تتم إدارة فئات مصروفات المشروع في Finance and Operations، وتتم مزامنتها لـ Project Service Automation كفئات حركات.</span><span class="sxs-lookup"><span data-stu-id="e1855-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="e1855-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="e1855-132">Power Query</span></span>

<span data-ttu-id="e1855-133">يجب عليك استخدام Microsoft Power Query لتعيين نوع الفوترة في فئة الحركة عند المزامنة إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e1855-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="e1855-134">يحتوي قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA) على عمود افتراضي وتعيين متوفر مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="e1855-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="e1855-135">إذا قمت بإنشاء قالبك الخاص، يجب عليك إضافة عمود شرطي في Power Query.</span><span class="sxs-lookup"><span data-stu-id="e1855-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="e1855-136">افتح استعلام متقدم ونموذج تصفية ضمن مهمة تعيين فئات مصروفات المشروع.</span><span class="sxs-lookup"><span data-stu-id="e1855-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="e1855-137">حدد **إضافة عمود شرطي**.</span><span class="sxs-lookup"><span data-stu-id="e1855-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="e1855-138">قم بتسمية العمود الجديد، على سبيل المثال BilingType.</span><span class="sxs-lookup"><span data-stu-id="e1855-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="e1855-139">إدخال الشرط التالي: إذا **كان CATEGORYID لا يساوي قيمة فارغة فمن ثم يساوي 19235001، وإلا يكون فارغًا**.</span><span class="sxs-lookup"><span data-stu-id="e1855-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="e1855-140">انقر فوق **موافق** في العمود.</span><span class="sxs-lookup"><span data-stu-id="e1855-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="e1855-141">تأكد من تعيين هذا العمود الجديد في صفحة التعيين.</span><span class="sxs-lookup"><span data-stu-id="e1855-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="e1855-142">يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="e1855-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="e1855-143">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance and Operations إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e1855-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="e1855-144">[![تعيين القالب](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e1855-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="e1855-145">يتم استخدام القالب التالي والمهمة الأساسية لمزامنة فئات مصروفات المشروع من Project Service Automation إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e1855-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="e1855-146">-**اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (PSA إلى Fin and Ops)-**اسم المهمة في المشروع:** مزامنة الفئات إلى Fin Ops</span><span class="sxs-lookup"><span data-stu-id="e1855-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="e1855-147">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="e1855-147">Entity set</span></span>

| <span data-ttu-id="e1855-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e1855-148">Project Service Automation</span></span>      | <span data-ttu-id="e1855-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1855-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="e1855-150">فئات الحركات</span><span class="sxs-lookup"><span data-stu-id="e1855-150">Transaction categories</span></span>          | <span data-ttu-id="e1855-151">كيان التكامل للفئات</span><span class="sxs-lookup"><span data-stu-id="e1855-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="e1855-152">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="e1855-152">Entity flow</span></span>

<span data-ttu-id="e1855-153">تتم إدارة فئات مصروفات المشروع في Finance and Operations، وتتم مزامنتها لـ Project Service Automation كفئات حركات.</span><span class="sxs-lookup"><span data-stu-id="e1855-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="e1855-154">تُحدث المزامنة مرة أخرى إلى Finance and Operation مُعرف التكامل من Project Service Automation في فئة مشروع Finance and Operations .</span><span class="sxs-lookup"><span data-stu-id="e1855-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="e1855-155">يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="e1855-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="e1855-156">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1855-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="e1855-157">[![تعيين القالب](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e1855-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

