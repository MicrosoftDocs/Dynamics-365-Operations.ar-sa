---
title: تغيير قواعد كانبان لوظيفة عملية
description: يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c036f6aad79e33df6009913d1e21ff6176f22593
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843783"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="14db5-103">تغيير قواعد كانبان لوظيفة عملية</span><span class="sxs-lookup"><span data-stu-id="14db5-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14db5-104">يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة.</span><span class="sxs-lookup"><span data-stu-id="14db5-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="14db5-105">وهذا مفيد لقياس مستوى حمل الموارد أو في حالة التصنيف.</span><span class="sxs-lookup"><span data-stu-id="14db5-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="14db5-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="14db5-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="14db5-107">هذا الإجراء مخصص للمخطط، الذي يعمل في شركة lean manufacturing، والمسؤول عن تدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="14db5-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="14db5-108">نسخ قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="14db5-108">Copy kanban rule</span></span>
1. <span data-ttu-id="14db5-109">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="14db5-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="14db5-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="14db5-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="14db5-111">حدد الحدث "قاعدة كانبان" 000022 لـ L0001.</span><span class="sxs-lookup"><span data-stu-id="14db5-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="14db5-112">انقر فوق "تكرار قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="14db5-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="14db5-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="14db5-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="14db5-114">تغيير قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="14db5-114">Change kanban rule</span></span>
1. <span data-ttu-id="14db5-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="14db5-115">Close the page.</span></span>
2. <span data-ttu-id="14db5-116">انتقل إلى جدولة وظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="14db5-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="14db5-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="14db5-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="14db5-118">حدد بند مع كانبان 000177.</span><span class="sxs-lookup"><span data-stu-id="14db5-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="14db5-119">انقر فوق استخدام قاعدة كانبان البديلة.</span><span class="sxs-lookup"><span data-stu-id="14db5-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="14db5-120">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="14db5-120">Click Next.</span></span>
6. <span data-ttu-id="14db5-121">في حقل "قاعدة كانبان"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="14db5-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="14db5-122">حدد قاعدة كانبان التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="14db5-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="14db5-123">هذه هي قاعدة كانبان مع الرقم الأعلى.</span><span class="sxs-lookup"><span data-stu-id="14db5-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="14db5-124">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="14db5-124">Click Finish.</span></span>
    * <span data-ttu-id="14db5-125">تستخدم وظيفة كانبان الآن قاعدة كانبان أخرى.</span><span class="sxs-lookup"><span data-stu-id="14db5-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="14db5-126">يمكن أن يكون ذلك مفيدًا لقياس مستوى حمل خلايا العمل.</span><span class="sxs-lookup"><span data-stu-id="14db5-126">This can be useful to level load work cells.</span></span>  

