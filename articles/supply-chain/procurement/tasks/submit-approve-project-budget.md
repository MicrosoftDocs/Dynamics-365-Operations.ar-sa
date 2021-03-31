---
title: إرسال واعتماد موازنة المشروع
description: يوضح هذا الإجراء كيفية إنشاء ميزانية المشروع وإرسالها.
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72ac6705ef8584ef41980a1cc9490227538de365
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222839"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="c1838-103">إرسال واعتماد موازنة المشروع</span><span class="sxs-lookup"><span data-stu-id="c1838-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1838-104">يوضح هذا الإجراء كيفية إنشاء ميزانية المشروع وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="c1838-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="c1838-105">عندما تنشئ ميزانية المشروع، يمكنك إدخال التكاليف والإيرادات المقدرة لمشروع، ثم استخدامها للتحكم في الحركات الفعلية للمشروع.</span><span class="sxs-lookup"><span data-stu-id="c1838-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="c1838-106">وفي إعداد موازنة المشروع، يجب إرسال جميع المراجعات والموازنات الأصلية إلى سير عمل مشروع للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="c1838-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="c1838-107">يمنحك سير العمل مزيدًا من التحكم في العملية وينشئ سجلاً لمحفوظات التغييرات.</span><span class="sxs-lookup"><span data-stu-id="c1838-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="c1838-108">تم إنشاء هذه المهمة باستخدام مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="c1838-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="c1838-109">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها‬‬ > المشاريع > جميع المشاريع‬**‬.</span><span class="sxs-lookup"><span data-stu-id="c1838-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="c1838-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c1838-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c1838-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1838-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c1838-112">في **جزء الإجراءات**، انقر فوق **الخطة**.</span><span class="sxs-lookup"><span data-stu-id="c1838-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="c1838-113">انقر فوق **موازنة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="c1838-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="c1838-114">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c1838-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="c1838-115">وسّع علامة التبويب السريعة **التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="c1838-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="c1838-116">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c1838-116">Click **New**.</span></span>
9. <span data-ttu-id="c1838-117">في الحقل **نوع الحركة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="c1838-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="c1838-118">في حقل **الفئة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c1838-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="c1838-119">في حقل **الفئة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c1838-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="c1838-120">قم بتوسيع علامة التبويب السريعة **الإيرادات‬**.</span><span class="sxs-lookup"><span data-stu-id="c1838-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="c1838-121">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c1838-121">Click **New**.</span></span>
14. <span data-ttu-id="c1838-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1838-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="c1838-123">في الحقل **نوع الحركة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="c1838-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="c1838-124">في حقل **الفئة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c1838-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="c1838-125">في حقل **الفئة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c1838-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="c1838-126">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c1838-126">Click **Save**.</span></span>
19. <span data-ttu-id="c1838-127">انقر فوق **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="c1838-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="c1838-128">انقر فوق **تقديم**.</span><span class="sxs-lookup"><span data-stu-id="c1838-128">Click **Submit**.</span></span>
21. <span data-ttu-id="c1838-129">في الحقل **التعليق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c1838-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="c1838-130">انقر فوق **تقديم**.</span><span class="sxs-lookup"><span data-stu-id="c1838-130">Click **Submit**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]