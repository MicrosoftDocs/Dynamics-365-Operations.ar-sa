---
title: إنشاء قوائم مهام وأضافه مهام
description: يصف هذا الموضوع كيفية إنشاء قوائم المهام وإضافة المهام إليها في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006200"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="36821-103">إنشاء قوائم مهام وأضافه مهام</span><span class="sxs-lookup"><span data-stu-id="36821-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36821-104">يصف هذا الموضوع كيفية إنشاء قوائم المهام وإضافة المهام إليها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="36821-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="36821-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="36821-105">Overview</span></span>

<span data-ttu-id="36821-106">تحدد *المهمة* جزءًا محددًا من العمل أو الإجراء الذي يجب أن يكمله أي شخص إكماله في تاريخ استحقاق معين أو قبله.</span><span class="sxs-lookup"><span data-stu-id="36821-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="36821-107">في Dynamics 365 Commerce، يمكن ان تتضمن المهمة إرشادات تفصيلية ومعلومات حول الشخص المسؤول.</span><span class="sxs-lookup"><span data-stu-id="36821-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="36821-108">كما يمكن أن تتضمن ارتباطات إلى عمليات مكاتب الدعم أو عمليات نقاط البيع (POS) أو صفحات الموقع للمساعدة في تحسين الانتاجية وتوفير السياق الذي يتطلبه مالك المهمة لإكمال المهمة بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="36821-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="36821-109">*قائمة المهام* هي مجموعة من المهام التي يجب إكمالها كجزء من عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="36821-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="36821-110">على سبيل المثال، تكون تكون قائمة مهام يجب على العامل إكمالها أثناء عملية الإعداد، أو قائمة مهام لموظفي الكاشير الذين يعملون في النوبات الليلية، أو قائمة مهام يجب إكمالها لتجهيز المتجر لموسم عطلة قادم.</span><span class="sxs-lookup"><span data-stu-id="36821-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="36821-111">في Commerce، يمكن تعيين كل قائمة مهام لها تاريخ مستهدف إلى أي عدد من المتاجر أو الموظفين، ويمكن تكوينها ليتم تكرارها.</span><span class="sxs-lookup"><span data-stu-id="36821-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="36821-112">يمكن للمديرين والعاملين إنشاء قوائم مهام في مكتب دعم Commerce، ثم تعيينهم لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="36821-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="36821-113">إنشاء قائمة جديدة</span><span class="sxs-lookup"><span data-stu-id="36821-113">Create a task list</span></span>

<span data-ttu-id="36821-114">لإنشاء قائمة مهام اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="36821-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="36821-115">انتقل إلى **Retail and Commerce \> إدارة المهام \> تنظيم إدارة المهام**.</span><span class="sxs-lookup"><span data-stu-id="36821-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="36821-116">حدد **جديد**، ثم أدخل قيمًا في الحقول **الاسم** و **الوصف** و **المالك**.</span><span class="sxs-lookup"><span data-stu-id="36821-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="36821-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36821-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="36821-118">إضافة مهام إلى قائمة مهام</span><span class="sxs-lookup"><span data-stu-id="36821-118">Add tasks to a task list</span></span>

<span data-ttu-id="36821-119">لإضافة مهام إلى قائمة مهام، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="36821-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="36821-120">على علامة التبويب السريعة **المهام** لقائمة مهام موجودة، حدد **جديد** لإضافة مهمة.</span><span class="sxs-lookup"><span data-stu-id="36821-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="36821-121">في مربع الحوار **إنشاء مهمة جديدة** في حقل **الاسم** أدخل اسماً للمهمة.</span><span class="sxs-lookup"><span data-stu-id="36821-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="36821-122">في الحقل **إزاحة تاريخ الاستحقاق من التاريخ المستهدف** أدخل قيمة صحيحه موجبة أو سالبة.</span><span class="sxs-lookup"><span data-stu-id="36821-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="36821-123">على سبيل المثال، أدخل **-2** إذا كان يجب إكمال المهمة قبل يومين من تاريخ استحقاق قائمة المهام.</span><span class="sxs-lookup"><span data-stu-id="36821-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="36821-124">في حقل **الملاحظات** أدخل الإرشادات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="36821-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="36821-125">في الحقل **‏‫جهة الاتصال‬** أدخل اسم مختص في مجال يمكن لمالك المهمة الاتصال به إذا كانت هناك حاجة إلى المساعدة.</span><span class="sxs-lookup"><span data-stu-id="36821-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="36821-126">في الحقل **ارتباط المهمة** أدخل ارتباطا استنادا إلى طبيعة المهمة.</span><span class="sxs-lookup"><span data-stu-id="36821-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="36821-127">على من أنه يمكنك استخدام الحقل **تعيين إلى** لتعيين مهام إلى شخص ما أثناء قيامك بإنشاء قائمة مهام، فإننا نوصي بتجنب تعيين مهام أثناء إنشاء قائمه المهام.</span><span class="sxs-lookup"><span data-stu-id="36821-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="36821-128">وبدلا من ذلك، قم بتعيين المهام بعد إنشاء مثيل للقائمة للمتاجر الفردية.</span><span class="sxs-lookup"><span data-stu-id="36821-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="36821-129">استخدام ارتباطات المهام للمساعدة في تحسين إنتاجيه العامل</span><span class="sxs-lookup"><span data-stu-id="36821-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="36821-130">يتيح لك Commerce ربط المهام بعمليات نقطة البيع المحددة، مثل تشغيل تقرير مبيعات أو عرض فيديو تدريب عبر الإنترنت لاتجاه الموظف الجديد أو إجراء عملية لمكتب الدعم.</span><span class="sxs-lookup"><span data-stu-id="36821-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="36821-131">تساعد هذه الميزة مالكي المهام في الحصول علي المعلومات التي يحتاجون إليها لإكمال المهام بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="36821-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="36821-132">لإضافة ارتباطات مهام أثناء إنشاء مهمة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="36821-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="36821-133">على علامة التبويب السريعة **المهام** لقائمة مهام موجودة، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="36821-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="36821-134">في مربع الحوار **تحرير مهمة** في الحقل **ارتباط المهمة** حدد واحدا أو أكثر من الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="36821-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="36821-135">حدد **عنصر قائمة** لتكوين عملية مكتب الدعم، مثل "مجموعات المنتجات".</span><span class="sxs-lookup"><span data-stu-id="36821-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="36821-136">حدد **عملية POS** لتكوين عمليه POS، مثل "تقارير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="36821-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="36821-137">حدد **عنوان URL** لتكوين عنوان URL مطلق.</span><span class="sxs-lookup"><span data-stu-id="36821-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="36821-138">يبين الرسم التوضيحي التالي تحديد ارتباطات المهام في مربع الحوار **تحرير المهمة**.</span><span class="sxs-lookup"><span data-stu-id="36821-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![تحديد ارتباطات المهام في مربع الحوار تحرير مهمة](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="36821-140">تكوين عملية POS بحيث يمكن ربطها بمهمة</span><span class="sxs-lookup"><span data-stu-id="36821-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="36821-141">لتكوين عملية POS بحيث يمكن ربطها بمهمة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="36821-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="36821-142">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="36821-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="36821-143">حدد **تحرير**، وابحث عن عملية نقطة البيع، ثم حدد خانة الاختيار **تمكين إدارة المهام** لها.</span><span class="sxs-lookup"><span data-stu-id="36821-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36821-144">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="36821-144">Additional resources</span></span>

[<span data-ttu-id="36821-145">نظرة عامة حول إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="36821-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="36821-146">تكوين إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="36821-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="36821-147">تعيين قوائم المهام إلى المتاجر أو الموظفين</span><span class="sxs-lookup"><span data-stu-id="36821-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="36821-148">إدارة المهام في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="36821-148">Task management in POS</span></span>](task-mgmt-POS.md)
