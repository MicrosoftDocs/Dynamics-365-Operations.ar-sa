---
title: إرسال واعتماد موازنة المشروع
description: يوضح هذا الإجراء كيفية إنشاء ميزانية المشروع وإرسالها.
author: mkirknel
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 798bbc68e625c58d56cdd769f48ba734ace1d028
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914844"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="b568b-103">إرسال واعتماد موازنة المشروع</span><span class="sxs-lookup"><span data-stu-id="b568b-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b568b-104">يوضح هذا الإجراء كيفية إنشاء ميزانية المشروع وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="b568b-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="b568b-105">عندما تنشئ ميزانية المشروع، يمكنك إدخال التكاليف والإيرادات المقدرة لمشروع، ثم استخدامها للتحكم في الحركات الفعلية للمشروع.</span><span class="sxs-lookup"><span data-stu-id="b568b-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="b568b-106">وفي إعداد موازنة المشروع، يجب إرسال جميع المراجعات والموازنات الأصلية إلى سير عمل مشروع للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="b568b-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="b568b-107">يمنحك سير العمل مزيدًا من التحكم في العملية وينشئ سجلاً لمحفوظات التغييرات.</span><span class="sxs-lookup"><span data-stu-id="b568b-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="b568b-108">تم إنشاء هذه المهمة باستخدام مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="b568b-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="b568b-109">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها‬‬ > المشاريع > جميع المشاريع‬**‬.</span><span class="sxs-lookup"><span data-stu-id="b568b-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="b568b-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b568b-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b568b-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b568b-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b568b-112">في **جزء الإجراءات**، انقر فوق **الخطة**.</span><span class="sxs-lookup"><span data-stu-id="b568b-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="b568b-113">انقر فوق **موازنة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="b568b-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="b568b-114">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b568b-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="b568b-115">وسّع علامة التبويب السريعة **التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="b568b-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="b568b-116">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b568b-116">Click **New**.</span></span>
9. <span data-ttu-id="b568b-117">في الحقل **نوع الحركة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="b568b-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="b568b-118">في حقل **الفئة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b568b-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="b568b-119">في حقل **الفئة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b568b-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="b568b-120">قم بتوسيع علامة التبويب السريعة **الإيرادات‬**.</span><span class="sxs-lookup"><span data-stu-id="b568b-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="b568b-121">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b568b-121">Click **New**.</span></span>
14. <span data-ttu-id="b568b-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b568b-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="b568b-123">في الحقل **نوع الحركة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="b568b-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="b568b-124">في حقل **الفئة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b568b-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="b568b-125">في حقل **الفئة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b568b-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="b568b-126">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b568b-126">Click **Save**.</span></span>
19. <span data-ttu-id="b568b-127">انقر فوق **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="b568b-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="b568b-128">انقر فوق **تقديم**.</span><span class="sxs-lookup"><span data-stu-id="b568b-128">Click **Submit**.</span></span>
21. <span data-ttu-id="b568b-129">في الحقل **التعليق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b568b-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="b568b-130">انقر فوق **تقديم**.</span><span class="sxs-lookup"><span data-stu-id="b568b-130">Click **Submit**.</span></span>

