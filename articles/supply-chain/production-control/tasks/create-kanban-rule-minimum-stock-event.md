---
title: إنشاء قاعدة كانبان باستخدام حدث الحد الأدنى للمخزون
description: يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان باستخدام حدث مخزون الحد أدنى لضمان توفر منتج معين في موقع معين في كل الأوقات.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a9ba8ec2abb26e3b9ee7e14bdf882c1ffcb205b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558516"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="85302-103">إنشاء قاعدة كانبان باستخدام حدث الحد الأدنى للمخزون</span><span class="sxs-lookup"><span data-stu-id="85302-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85302-104">يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان باستخدام حدث مخزون الحد أدنى لضمان توفر منتج معين في موقع معين في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="85302-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="85302-105">يتم إنشاء قاعدة كانبان لتحويل المواد إلى الموقع عندما ينخفض مستوى المخزون إلى أقل من 200 قطعة.</span><span class="sxs-lookup"><span data-stu-id="85302-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="85302-106">من خلال تشغيل معالجة حدث تثبيت السعر، يتم إنشاء كانبان المطلوب.</span><span class="sxs-lookup"><span data-stu-id="85302-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="85302-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="85302-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="85302-108">هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند قيامه بتحضير عملية إنتاج منتج جديد أو معدل في بيئة محدودة.</span><span class="sxs-lookup"><span data-stu-id="85302-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="85302-109">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="85302-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="85302-110">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="85302-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="85302-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="85302-111">Click New.</span></span>
3. <span data-ttu-id="85302-112">في حقل "النوع"، حدد "انسحاب".</span><span class="sxs-lookup"><span data-stu-id="85302-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="85302-113">يتم استخدام هذا النوع لإنشاء كانبان للتحويل.</span><span class="sxs-lookup"><span data-stu-id="85302-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="85302-114">في الحقل "إستراتيجية التزويد"، حدد "الحدث".</span><span class="sxs-lookup"><span data-stu-id="85302-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="85302-115">يتم استخدام استراتيجية الحدث لإنشاء كانبان للتحويل استنادًا إلى حدث.</span><span class="sxs-lookup"><span data-stu-id="85302-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="85302-116">لاحقًا في الإجراء، ستقوم بتشغيل كانبان للتحويل باستخدام تزويد المخزون‬.</span><span class="sxs-lookup"><span data-stu-id="85302-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="85302-117">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="85302-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="85302-118">أدخل ReplenishSpeakerComponents أو حدده.</span><span class="sxs-lookup"><span data-stu-id="85302-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="85302-119">هناك مستودع استلام (مخرجات) والموقع 12 لنشاط التحويل هذا، مما يعني أنه سيتم نقل المواد إلى الموقع 12 في المستودع 12.</span><span class="sxs-lookup"><span data-stu-id="85302-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="85302-120">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="85302-120">Expand the Details section.</span></span>
7. <span data-ttu-id="85302-121">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="85302-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="85302-122">حدد "M0007".</span><span class="sxs-lookup"><span data-stu-id="85302-122">Select M0007.</span></span>  
8. <span data-ttu-id="85302-123">قم بتوسيع القسم "الأحداث".</span><span class="sxs-lookup"><span data-stu-id="85302-123">Expand the Events section.</span></span>
9. <span data-ttu-id="85302-124">في حقل "حدث تزويد المخزون"، حدد "دُفعة".</span><span class="sxs-lookup"><span data-stu-id="85302-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="85302-125">يؤدي هذا إلى إنشاء كانبان لتلبية الاحتياجات المادية في الموقع ذي الصلة أثناء معالجة حدث تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="85302-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="85302-126">تعيين الحد الأدنى لكمية الصنف</span><span class="sxs-lookup"><span data-stu-id="85302-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="85302-127">انقر لمتابعة الارتباط في حقل "المنتج".</span><span class="sxs-lookup"><span data-stu-id="85302-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="85302-128">انقر لمتابعة الارتباط في الحقل "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="85302-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="85302-129">قم بتوسيع مربع حقائق صورة المنتج.</span><span class="sxs-lookup"><span data-stu-id="85302-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="85302-130">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="85302-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="85302-131">انقر فوق "تغطية الصنف‬".</span><span class="sxs-lookup"><span data-stu-id="85302-131">Click Item coverage.</span></span>
6. <span data-ttu-id="85302-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="85302-132">Click New.</span></span>
7. <span data-ttu-id="85302-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="85302-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="85302-134">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="85302-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="85302-135">قم بتعيين المستودع على 12.</span><span class="sxs-lookup"><span data-stu-id="85302-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="85302-136">عيّن الحد الأدنى إلى "200".</span><span class="sxs-lookup"><span data-stu-id="85302-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="85302-137">تشغيل الوظيفة الدفعية إنشاء حدث</span><span class="sxs-lookup"><span data-stu-id="85302-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="85302-138">انتقل إلى التحكم بالإنتاج‬ > المهام الدورية > معالجة دُفعة وظيفة كانبان‬ > معالجة حدث تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="85302-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="85302-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="85302-139">Click OK.</span></span>
3. <span data-ttu-id="85302-140">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="85302-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="85302-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="85302-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="85302-142">حدد قاعدة كانبان التي أنشأتها في السابق.</span><span class="sxs-lookup"><span data-stu-id="85302-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="85302-143">قم بتوسيع القسم "كانبان".</span><span class="sxs-lookup"><span data-stu-id="85302-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="85302-144">لاحظ أنه تم إنشاء كانبان لنقل المواد المطلوبة إلى المستودع 12.</span><span class="sxs-lookup"><span data-stu-id="85302-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

