---
title: تغيير قواعد كانبان لوظيفة عملية
description: يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0e1989bcc4ca02d097f9ebff40f21158f26546
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981345"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="00e7e-103">تغيير قواعد كانبان لوظيفة عملية</span><span class="sxs-lookup"><span data-stu-id="00e7e-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00e7e-104">يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة.</span><span class="sxs-lookup"><span data-stu-id="00e7e-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="00e7e-105">وهذا مفيد لقياس مستوى حمل الموارد أو في حالة التصنيف.</span><span class="sxs-lookup"><span data-stu-id="00e7e-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="00e7e-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="00e7e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="00e7e-107">هذا الإجراء مخصص للمخطط، الذي يعمل في شركة lean manufacturing، والمسؤول عن تدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="00e7e-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="00e7e-108">نسخ قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="00e7e-108">Copy kanban rule</span></span>
1. <span data-ttu-id="00e7e-109">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="00e7e-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="00e7e-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="00e7e-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="00e7e-111">حدد الحدث "قاعدة كانبان" 000022 لـ L0001.</span><span class="sxs-lookup"><span data-stu-id="00e7e-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="00e7e-112">انقر فوق "تكرار قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="00e7e-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="00e7e-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="00e7e-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="00e7e-114">تغيير قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="00e7e-114">Change kanban rule</span></span>
1. <span data-ttu-id="00e7e-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="00e7e-115">Close the page.</span></span>
2. <span data-ttu-id="00e7e-116">انتقل إلى جدولة وظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="00e7e-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="00e7e-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="00e7e-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="00e7e-118">حدد بند مع كانبان 000177.</span><span class="sxs-lookup"><span data-stu-id="00e7e-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="00e7e-119">انقر فوق استخدام قاعدة كانبان البديلة.</span><span class="sxs-lookup"><span data-stu-id="00e7e-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="00e7e-120">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="00e7e-120">Click Next.</span></span>
6. <span data-ttu-id="00e7e-121">في حقل "قاعدة كانبان"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00e7e-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="00e7e-122">حدد قاعدة كانبان التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="00e7e-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="00e7e-123">هذه هي قاعدة كانبان مع الرقم الأعلى.</span><span class="sxs-lookup"><span data-stu-id="00e7e-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="00e7e-124">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="00e7e-124">Click Finish.</span></span>
    * <span data-ttu-id="00e7e-125">تستخدم وظيفة كانبان الآن قاعدة كانبان أخرى.</span><span class="sxs-lookup"><span data-stu-id="00e7e-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="00e7e-126">يمكن أن يكون ذلك مفيدًا لقياس مستوى حمل خلايا العمل.</span><span class="sxs-lookup"><span data-stu-id="00e7e-126">This can be useful to level load work cells.</span></span>  

