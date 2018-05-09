--- 
title: "إنشاء قاعدة كانبان للاستبدال‬"
description: "يركز هذا الإجراء على استبدال قاعدة كانبان موجودة بقاعدة كانبان جديدة في تاريخ محدد."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 12df41f14973628063b11f20f7368f47b2ad3488
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="4465a-103">إنشاء قاعدة كانبان للاستبدال‬</span><span class="sxs-lookup"><span data-stu-id="4465a-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4465a-104">يركز هذا الإجراء على استبدال قاعدة كانبان موجودة بقاعدة كانبان جديدة في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="4465a-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="4465a-105">هذا مفيد عندما يلزم تنسيق التغييرات في تدفق الإنتاج أو قواعد التزويد وجدولتها.</span><span class="sxs-lookup"><span data-stu-id="4465a-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="4465a-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="4465a-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="4465a-107">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج تدفق عمل مغيَّر أو قاعدة تزويد جديدة.</span><span class="sxs-lookup"><span data-stu-id="4465a-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="4465a-108">تستبدل هذه المهمة قاعدة كانبان 000022 بقاعدة جديدة وتزيد الحد الأقصى للكمية من 48 إلى 100 للقاعدة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="4465a-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="4465a-109">حدد قاعدة كانبان لاستبدالها</span><span class="sxs-lookup"><span data-stu-id="4465a-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="4465a-110">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="4465a-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="4465a-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4465a-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4465a-112">حدد "قاعدة كانبان 000022.</span><span class="sxs-lookup"><span data-stu-id="4465a-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="4465a-113">إنشاء قاعدة كانبان للاستبدال‬</span><span class="sxs-lookup"><span data-stu-id="4465a-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="4465a-114">انقر فوق استبدال قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="4465a-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="4465a-115">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="4465a-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="4465a-116">تحديد تاريخ في المستقبل، مثل أسبوع واحد من الآن.</span><span class="sxs-lookup"><span data-stu-id="4465a-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="4465a-117">هذا التاريخ والوقت حيث تصبح قاعدة كانبان الجديدة نشطة وتحل محل قاعدة كانبان القديمة.</span><span class="sxs-lookup"><span data-stu-id="4465a-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="4465a-118">إذا قامت قاعدة كانبان بتغيير المسار في تدفق الإنتاج، فإنه يمكن تحديد نشاط آخر.</span><span class="sxs-lookup"><span data-stu-id="4465a-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="4465a-119">في هذا الإجراء، سنواصل النشاط دون تغيير.</span><span class="sxs-lookup"><span data-stu-id="4465a-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="4465a-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4465a-120">Click OK.</span></span>
    * <span data-ttu-id="4465a-121">لاحظ أنه يتم إنشاء قاعدة كانبان جديدة لتحل محل قاعدة كانبان 000022.</span><span class="sxs-lookup"><span data-stu-id="4465a-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="4465a-122">يتم تعيين تاريخ السريان وفقًا للتاريخ الذي تم اختياره عند قيامك باستبدال قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="4465a-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="4465a-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4465a-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4465a-124">حدد قاعدة كانبان 000022 المستبدلة.</span><span class="sxs-lookup"><span data-stu-id="4465a-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="4465a-125">لاحظ أن قاعدة كانبان المستبدلة تحتوي على تاريخ انتهاء الصلاحية نفسه لأن هذا هو التاريخ الذي ستنتهي به.</span><span class="sxs-lookup"><span data-stu-id="4465a-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="4465a-126">في القائمة، حدد الصف 1.</span><span class="sxs-lookup"><span data-stu-id="4465a-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="4465a-127">حدد قاعدة كانبان الجديدة على رأس القائمة.</span><span class="sxs-lookup"><span data-stu-id="4465a-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="4465a-128">هذه هي قاعدة كانبان التي تحتوي على رقم كانبان الأكبر.</span><span class="sxs-lookup"><span data-stu-id="4465a-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="4465a-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4465a-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4465a-130">انقر فوق رقم قاعدة كانبان لفتح قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="4465a-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="4465a-131">تعديل الحد الأقصى للكمية لاستبدال قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="4465a-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="4465a-132">قم بتعيين الحد الأقصى للكمية إلى "100".</span><span class="sxs-lookup"><span data-stu-id="4465a-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="4465a-133">قم بتوسيع علامة التبويب السريعة "الكميات" لرؤية حقل "الحد الأقصى للكمية".</span><span class="sxs-lookup"><span data-stu-id="4465a-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="4465a-134">سيسمح تغيير الحد الأقصى للكمية 100 بوصول كانبان إلى 100 كانبان تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="4465a-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="4465a-135">وهذه هي الخطوة الأخيرة في هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="4465a-135">This is the last step in this task.</span></span>  


