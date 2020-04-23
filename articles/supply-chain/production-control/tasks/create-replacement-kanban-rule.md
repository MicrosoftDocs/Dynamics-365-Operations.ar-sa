---
title: إنشاء قاعدة كانبان للاستبدال‬
description: يركز هذا الإجراء على استبدال قاعدة كانبان موجودة بقاعدة كانبان جديدة في تاريخ محدد.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae589f81811c1586e0e24de94eaf5f467f19debb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210846"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="cca40-103">إنشاء قاعدة كانبان للاستبدال‬</span><span class="sxs-lookup"><span data-stu-id="cca40-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cca40-104">يركز هذا الإجراء على استبدال قاعدة كانبان موجودة بقاعدة كانبان جديدة في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="cca40-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="cca40-105">هذا مفيد عندما يلزم تنسيق التغييرات في تدفق الإنتاج أو قواعد التزويد وجدولتها.</span><span class="sxs-lookup"><span data-stu-id="cca40-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="cca40-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cca40-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="cca40-107">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج تدفق عمل مغيَّر أو قاعدة تزويد جديدة.</span><span class="sxs-lookup"><span data-stu-id="cca40-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="cca40-108">تستبدل هذه المهمة قاعدة كانبان 000022 بقاعدة جديدة وتزيد الحد الأقصى للكمية من 48 إلى 100 للقاعدة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="cca40-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="cca40-109">حدد قاعدة كانبان لاستبدالها</span><span class="sxs-lookup"><span data-stu-id="cca40-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="cca40-110">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="cca40-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="cca40-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cca40-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cca40-112">حدد "قاعدة كانبان 000022.</span><span class="sxs-lookup"><span data-stu-id="cca40-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="cca40-113">إنشاء قاعدة كانبان للاستبدال‬</span><span class="sxs-lookup"><span data-stu-id="cca40-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="cca40-114">انقر فوق استبدال قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="cca40-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="cca40-115">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="cca40-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="cca40-116">تحديد تاريخ في المستقبل، مثل أسبوع واحد من الآن.</span><span class="sxs-lookup"><span data-stu-id="cca40-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="cca40-117">هذا التاريخ والوقت حيث تصبح قاعدة كانبان الجديدة نشطة وتحل محل قاعدة كانبان القديمة.</span><span class="sxs-lookup"><span data-stu-id="cca40-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="cca40-118">إذا قامت قاعدة كانبان بتغيير المسار في تدفق الإنتاج، فإنه يمكن تحديد نشاط آخر.</span><span class="sxs-lookup"><span data-stu-id="cca40-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="cca40-119">في هذا الإجراء، سنواصل النشاط دون تغيير.</span><span class="sxs-lookup"><span data-stu-id="cca40-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="cca40-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cca40-120">Click OK.</span></span>
    * <span data-ttu-id="cca40-121">لاحظ أنه يتم إنشاء قاعدة كانبان جديدة لتحل محل قاعدة كانبان 000022.</span><span class="sxs-lookup"><span data-stu-id="cca40-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="cca40-122">يتم تعيين تاريخ السريان وفقًا للتاريخ الذي تم اختياره عند قيامك باستبدال قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="cca40-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="cca40-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cca40-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cca40-124">حدد قاعدة كانبان 000022 المستبدلة.</span><span class="sxs-lookup"><span data-stu-id="cca40-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="cca40-125">لاحظ أن قاعدة كانبان المستبدلة تحتوي على تاريخ انتهاء الصلاحية نفسه لأن هذا هو التاريخ الذي ستنتهي به.</span><span class="sxs-lookup"><span data-stu-id="cca40-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="cca40-126">في القائمة، حدد الصف 1.</span><span class="sxs-lookup"><span data-stu-id="cca40-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="cca40-127">حدد قاعدة كانبان الجديدة على رأس القائمة.</span><span class="sxs-lookup"><span data-stu-id="cca40-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="cca40-128">هذه هي قاعدة كانبان التي تحتوي على رقم كانبان الأكبر.</span><span class="sxs-lookup"><span data-stu-id="cca40-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="cca40-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cca40-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cca40-130">انقر فوق رقم قاعدة كانبان لفتح قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="cca40-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="cca40-131">تعديل الحد الأقصى للكمية لاستبدال قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="cca40-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="cca40-132">قم بتعيين الحد الأقصى للكمية إلى "100".</span><span class="sxs-lookup"><span data-stu-id="cca40-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="cca40-133">قم بتوسيع علامة التبويب السريعة "الكميات" لرؤية حقل "الحد الأقصى للكمية".</span><span class="sxs-lookup"><span data-stu-id="cca40-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="cca40-134">سيسمح تغيير الحد الأقصى للكمية 100 بوصول كانبان إلى 100 كانبان تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="cca40-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="cca40-135">وهذه هي الخطوة الأخيرة في هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="cca40-135">This is the last step in this task.</span></span>  

