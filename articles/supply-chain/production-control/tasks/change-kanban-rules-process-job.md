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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "314936"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="096e0-103">تغيير قواعد كانبان لوظيفة عملية</span><span class="sxs-lookup"><span data-stu-id="096e0-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="096e0-104">يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة.</span><span class="sxs-lookup"><span data-stu-id="096e0-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="096e0-105">وهذا مفيد لقياس مستوى حمل الموارد أو في حالة التصنيف.</span><span class="sxs-lookup"><span data-stu-id="096e0-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="096e0-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="096e0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="096e0-107">هذا الإجراء مخصص للمخطط، الذي يعمل في شركة lean manufacturing، والمسؤول عن تدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="096e0-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="096e0-108">نسخ قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="096e0-108">Copy kanban rule</span></span>
1. <span data-ttu-id="096e0-109">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="096e0-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="096e0-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="096e0-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="096e0-111">حدد الحدث "قاعدة كانبان" 000022 لـ L0001.</span><span class="sxs-lookup"><span data-stu-id="096e0-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="096e0-112">انقر فوق "تكرار قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="096e0-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="096e0-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="096e0-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="096e0-114">تغيير قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="096e0-114">Change kanban rule</span></span>
1. <span data-ttu-id="096e0-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="096e0-115">Close the page.</span></span>
2. <span data-ttu-id="096e0-116">انتقل إلى جدولة وظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="096e0-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="096e0-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="096e0-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="096e0-118">حدد بند مع كانبان 000177.</span><span class="sxs-lookup"><span data-stu-id="096e0-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="096e0-119">انقر فوق استخدام قاعدة كانبان البديلة.</span><span class="sxs-lookup"><span data-stu-id="096e0-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="096e0-120">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="096e0-120">Click Next.</span></span>
6. <span data-ttu-id="096e0-121">في حقل "قاعدة كانبان"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="096e0-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="096e0-122">حدد قاعدة كانبان التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="096e0-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="096e0-123">هذه هي قاعدة كانبان مع الرقم الأعلى.</span><span class="sxs-lookup"><span data-stu-id="096e0-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="096e0-124">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="096e0-124">Click Finish.</span></span>
    * <span data-ttu-id="096e0-125">تستخدم وظيفة كانبان الآن قاعدة كانبان أخرى.</span><span class="sxs-lookup"><span data-stu-id="096e0-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="096e0-126">يمكن أن يكون ذلك مفيدًا لقياس مستوى حمل خلايا العمل.</span><span class="sxs-lookup"><span data-stu-id="096e0-126">This can be useful to level load work cells.</span></span>  

