---
title: مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce
description: يصف هذا الموضوع كيفية مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce (POS).
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b4a9ad561e3bff67720a08d6e4184a81e01f734
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908259"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="5bc96-103">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5bc96-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5bc96-104">يصف هذا الموضوع كيفية مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce (POS).</span><span class="sxs-lookup"><span data-stu-id="5bc96-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="5bc96-105">أحد الأغراض الرئيسية لتكامل Teams هو تمكين مزامنة إدارة المهام بين تطبيق نقطة البيع (POS) وTeams.</span><span class="sxs-lookup"><span data-stu-id="5bc96-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="5bc96-106">بهذه الطريقة، يمكن لموظفي المتجر استخدام إما تطبيق نقطة البيع (POS) أو Teams لإدارة المهام، ولا يتعين عليهم تبديل التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="5bc96-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="5bc96-107">نظرًا لاستخدام Planner كمستودع للمهام في Teams، يجب أن يكون هناك ارتباط بين Teams وDynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5bc96-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="5bc96-108">يتم إنشاء هذا الارتباط باستخدام معرف خطة معين لفريق متجر معين.</span><span class="sxs-lookup"><span data-stu-id="5bc96-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="5bc96-109">توضح الإجراءات التالية كيفية إعداد مزامنة إدارة المهام بين تطبيقي نقطة البيع (POS) وTeams.</span><span class="sxs-lookup"><span data-stu-id="5bc96-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="5bc96-110">نشر قائمة مهام الاختبار في Teams</span><span class="sxs-lookup"><span data-stu-id="5bc96-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="5bc96-111">يفترض الإجراء التالي أن فرق متجرك تستخدم تكامل إدارة مهام Microsoft Teams مع Commerce للمرة الأولى.</span><span class="sxs-lookup"><span data-stu-id="5bc96-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="5bc96-112">لنشر قائمة مهام اختبار في Teams، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5bc96-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="5bc96-113">قم بتسجيل الدخول إلى Teams كمدير اتصالات.</span><span class="sxs-lookup"><span data-stu-id="5bc96-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="5bc96-114">عادةً ما يكون مديرو الاتصالات مستخدمين لديهم دور **المدير الإقليمي** في Commerce.</span><span class="sxs-lookup"><span data-stu-id="5bc96-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="5bc96-115">في جزء التنقل الأيمن، حدد **المهام حسب Planner**</span><span class="sxs-lookup"><span data-stu-id="5bc96-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="5bc96-116">في علامة التبويب **القوائم المنشورة**، حدد **قائمة جديدة** في أسفل اليسار، وقم بتسمية القائمة الجديدة **قائمة مهام الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="5bc96-117">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-117">Select **Create**.</span></span> <span data-ttu-id="5bc96-118">تظهر القائمة الجديدة ضمن **المسودات**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="5bc96-119">ضمن **عنوان المهمة**، قم بإعطاء المهمة الأولى العنوان **تكامل Teams في الاختبارات**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="5bc96-120">ثم حدد **إدخال**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="5bc96-121">في قائمة **المسودات**، حدد قائمة المهام.</span><span class="sxs-lookup"><span data-stu-id="5bc96-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="5bc96-122">وبعد ذلك، حدد  **نشر** في الزاوية العلوية اليمنى.</span><span class="sxs-lookup"><span data-stu-id="5bc96-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="5bc96-123">في مربع الحوار **تحديد من تريد النشر إليه**، حدد الفرق التي يجب أن تتلقى قائمة مهام الاختبار.</span><span class="sxs-lookup"><span data-stu-id="5bc96-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="5bc96-124">حدد **التالي** لمراجعة خطة المنشور.</span><span class="sxs-lookup"><span data-stu-id="5bc96-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="5bc96-125">إذا كان يجب عليك إجراء التغييرات، فحدد  **السابق**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="5bc96-126">حدد **تأكيد للمتابعة**، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="5bc96-127">بعد اكتمال النشر، تظهر رسالة أعلى علامة التبويب **القوائم المنشورة** تشير إلى ما إذا كان قد تم تسليم قائمة المهام الخاصة بك بنجاح.</span><span class="sxs-lookup"><span data-stu-id="5bc96-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="5bc96-128">لمزيد من المعلومات، راجع [نشر قوائم المهام لإنشاء وتعقب العمل في مؤسستك](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="5bc96-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="5bc96-129">ربط نقطة البيع وTeams لإدارة المهام</span><span class="sxs-lookup"><span data-stu-id="5bc96-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="5bc96-130">لربط نقطة البيع وتطبيقات Microsoft Teams لإدارة المهام في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5bc96-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5bc96-131">انتقل إلى **Retail وCommerce \> إدارة المهام \> تكامل المهام مع Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="5bc96-132">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5bc96-133">قم بتعيين خيار **تمكين تكامل إدارة المهام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="5bc96-134">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5bc96-135">في جزء الإجراء، حدد **إعداد إدارة المهام**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="5bc96-136">يجب أن تتلقى إعلامًا يشير إلى أنه جاري إنشاء وظيفة دفعة تحمل الاسم **توفير Teams**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="5bc96-137">انتقل إلى **إدارة النظام \> الاستعلامات \> وظائف الدفعات**، وابحث عن الوظيفة الأحدث التي تشتمل على وصف **توفير Teams**.</span><span class="sxs-lookup"><span data-stu-id="5bc96-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="5bc96-138">انتظر حتى انتهاء تشغيل هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="5bc96-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="5bc96-139">قم بتشغيل **وظيفة CDX رقم 1070** لنشر معرف الخطة ومراجع المتجر إلى خادم Retail.</span><span class="sxs-lookup"><span data-stu-id="5bc96-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bc96-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5bc96-140">Additional resources</span></span>

[<span data-ttu-id="5bc96-141">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="5bc96-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="5bc96-142">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="5bc96-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="5bc96-143">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5bc96-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="5bc96-144">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5bc96-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="5bc96-145">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5bc96-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="5bc96-146">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="5bc96-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
