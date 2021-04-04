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
ms.openlocfilehash: 28bea16c3266115cf09aa80a364344789d60af7a
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477818"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="e3ce1-103">إنشاء قوائم مهام وإضافة مهام</span><span class="sxs-lookup"><span data-stu-id="e3ce1-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3ce1-104">يصف هذا الموضوع كيفية إنشاء قوائم المهام وإضافة المهام إليها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e3ce1-105">تحدد *المهمة* جزءًا محددًا من العمل أو الإجراء الذي يجب أن يكمله أي شخص إكماله في تاريخ استحقاق معين أو قبله.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="e3ce1-106">في Dynamics 365 Commerce، يمكن ان تتضمن المهمة إرشادات تفصيلية ومعلومات حول الشخص المسؤول.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="e3ce1-107">كما يمكن أن تتضمن ارتباطات إلى عمليات مكاتب الدعم أو عمليات نقاط البيع (POS) أو صفحات الموقع للمساعدة في تحسين الانتاجية وتوفير السياق الذي يتطلبه مالك المهمة لإكمال المهمة بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="e3ce1-108">*قائمة المهام* هي مجموعة من المهام التي يجب إكمالها كجزء من عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="e3ce1-109">على سبيل المثال، تكون تكون قائمة مهام يجب على العامل إكمالها أثناء عملية الإعداد، أو قائمة مهام لموظفي الكاشير الذين يعملون في النوبات الليلية، أو قائمة مهام يجب إكمالها لتجهيز المتجر لموسم عطلة قادم.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="e3ce1-110">في Commerce، يمكن تعيين كل قائمة مهام لها تاريخ مستهدف إلى أي عدد من المتاجر أو الموظفين، ويمكن تكوينها ليتم تكرارها.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="e3ce1-111">يمكن للمديرين والعاملين إنشاء قوائم مهام في مكتب دعم Commerce، ثم تعيينهم لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="e3ce1-112">إنشاء قائمة جديدة</span><span class="sxs-lookup"><span data-stu-id="e3ce1-112">Create a task list</span></span>

<span data-ttu-id="e3ce1-113">لإنشاء قائمة مهام اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="e3ce1-114">انتقل إلى **Retail and Commerce \> إدارة المهام \> تنظيم إدارة المهام**.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e3ce1-115">حدد **جديد**، ثم أدخل قيمًا في الحقول **الاسم** و **الوصف** و **المالك**.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="e3ce1-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="e3ce1-117">إضافة مهام إلى قائمة مهام</span><span class="sxs-lookup"><span data-stu-id="e3ce1-117">Add tasks to a task list</span></span>

<span data-ttu-id="e3ce1-118">لإضافة مهام إلى قائمة مهام، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="e3ce1-119">على علامة التبويب السريعة **المهام** لقائمة مهام موجودة، حدد **جديد** لإضافة مهمة.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="e3ce1-120">في مربع الحوار **إنشاء مهمة جديدة** في حقل **الاسم** أدخل اسماً للمهمة.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="e3ce1-121">في الحقل **إزاحة تاريخ الاستحقاق من التاريخ المستهدف** أدخل قيمة صحيحه موجبة أو سالبة.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="e3ce1-122">على سبيل المثال، أدخل **-2** إذا كان يجب إكمال المهمة قبل يومين من تاريخ استحقاق قائمة المهام.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="e3ce1-123">في حقل **الملاحظات** أدخل الإرشادات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="e3ce1-124">في الحقل **‏‫جهة الاتصال‬** أدخل اسم مختص في مجال يمكن لمالك المهمة الاتصال به إذا كانت هناك حاجة إلى المساعدة.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="e3ce1-125">في الحقل **ارتباط المهمة** أدخل ارتباطا استنادا إلى طبيعة المهمة.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="e3ce1-126">على من أنه يمكنك استخدام الحقل **تعيين إلى** لتعيين مهام إلى شخص ما أثناء قيامك بإنشاء قائمة مهام، فإننا نوصي بتجنب تعيين مهام أثناء إنشاء قائمه المهام.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="e3ce1-127">وبدلا من ذلك، قم بتعيين المهام بعد إنشاء مثيل للقائمة للمتاجر الفردية.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="e3ce1-128">استخدام ارتباطات المهام للمساعدة في تحسين إنتاجيه العامل</span><span class="sxs-lookup"><span data-stu-id="e3ce1-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="e3ce1-129">يتيح لك Commerce ربط المهام بعمليات نقطة البيع المحددة، مثل تشغيل تقرير مبيعات أو عرض فيديو تدريب عبر الإنترنت لاتجاه الموظف الجديد أو إجراء عملية لمكتب الدعم.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="e3ce1-130">تساعد هذه الميزة مالكي المهام في الحصول علي المعلومات التي يحتاجون إليها لإكمال المهام بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="e3ce1-131">لإضافة ارتباطات مهام أثناء إنشاء مهمة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="e3ce1-132">على علامة التبويب السريعة **المهام** لقائمة مهام موجودة، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="e3ce1-133">في مربع الحوار **تحرير مهمة** في الحقل **ارتباط المهمة** حدد واحدا أو أكثر من الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="e3ce1-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="e3ce1-134">حدد **عنصر قائمة** لتكوين عملية مكتب الدعم، مثل "مجموعات المنتجات".</span><span class="sxs-lookup"><span data-stu-id="e3ce1-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="e3ce1-135">حدد **عملية POS** لتكوين عمليه POS، مثل "تقارير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="e3ce1-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="e3ce1-136">حدد **عنوان URL** لتكوين عنوان URL مطلق.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="e3ce1-137">يبين الرسم التوضيحي التالي تحديد ارتباطات المهام في مربع الحوار **تحرير المهمة**.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![تحديد ارتباطات المهام في مربع الحوار تحرير مهمة](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="e3ce1-139">تكوين عملية POS بحيث يمكن ربطها بمهمة</span><span class="sxs-lookup"><span data-stu-id="e3ce1-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="e3ce1-140">لتكوين عملية POS بحيث يمكن ربطها بمهمة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="e3ce1-141">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="e3ce1-142">حدد **تحرير**، وابحث عن عملية نقطة البيع، ثم حدد خانة الاختيار **تمكين إدارة المهام** لها.</span><span class="sxs-lookup"><span data-stu-id="e3ce1-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3ce1-143">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e3ce1-143">Additional resources</span></span>

[<span data-ttu-id="e3ce1-144">نظرة عامة حول إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="e3ce1-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="e3ce1-145">تكوين إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="e3ce1-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="e3ce1-146">تعيين قوائم المهام إلى المتاجر أو الموظفين</span><span class="sxs-lookup"><span data-stu-id="e3ce1-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="e3ce1-147">إدارة المهام في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="e3ce1-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
