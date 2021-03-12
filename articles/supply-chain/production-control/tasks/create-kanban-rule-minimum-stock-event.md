---
title: إنشاء قاعدة كانبان باستخدام حدث الحد الأدنى للمخزون
description: يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان باستخدام حدث مخزون الحد أدنى لضمان توفر منتج معين في موقع معين في كل الأوقات.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19b4f80c6afa2634c469a23dfcd8dd8f151dd6cc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998693"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="19b25-103">إنشاء قاعدة كانبان باستخدام حدث الحد الأدنى للمخزون</span><span class="sxs-lookup"><span data-stu-id="19b25-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19b25-104">يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان باستخدام حدث مخزون الحد أدنى لضمان توفر منتج معين في موقع معين في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="19b25-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="19b25-105">يتم إنشاء قاعدة كانبان لتحويل المواد إلى الموقع عندما ينخفض مستوى المخزون إلى أقل من 200 قطعة.</span><span class="sxs-lookup"><span data-stu-id="19b25-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="19b25-106">من خلال تشغيل معالجة حدث تثبيت السعر، يتم إنشاء كانبان المطلوب.</span><span class="sxs-lookup"><span data-stu-id="19b25-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="19b25-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="19b25-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="19b25-108">هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند قيامه بتحضير عملية إنتاج منتج جديد أو معدل في بيئة محدودة.</span><span class="sxs-lookup"><span data-stu-id="19b25-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="19b25-109">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="19b25-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="19b25-110">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="19b25-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="19b25-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="19b25-111">Click New.</span></span>
3. <span data-ttu-id="19b25-112">في حقل "النوع"، حدد "انسحاب".</span><span class="sxs-lookup"><span data-stu-id="19b25-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="19b25-113">يتم استخدام هذا النوع لإنشاء كانبان للتحويل.</span><span class="sxs-lookup"><span data-stu-id="19b25-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="19b25-114">في الحقل "إستراتيجية التزويد"، حدد "الحدث".</span><span class="sxs-lookup"><span data-stu-id="19b25-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="19b25-115">يتم استخدام استراتيجية الحدث لإنشاء كانبان للتحويل استنادًا إلى حدث.</span><span class="sxs-lookup"><span data-stu-id="19b25-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="19b25-116">لاحقًا في الإجراء، ستقوم بتشغيل كانبان للتحويل باستخدام تزويد المخزون‬.</span><span class="sxs-lookup"><span data-stu-id="19b25-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="19b25-117">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="19b25-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="19b25-118">أدخل ReplenishSpeakerComponents أو حدده.</span><span class="sxs-lookup"><span data-stu-id="19b25-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="19b25-119">هناك مستودع استلام (مخرجات) والموقع 12 لنشاط التحويل هذا، مما يعني أنه سيتم نقل المواد إلى الموقع 12 في المستودع 12.</span><span class="sxs-lookup"><span data-stu-id="19b25-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="19b25-120">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="19b25-120">Expand the Details section.</span></span>
7. <span data-ttu-id="19b25-121">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="19b25-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="19b25-122">حدد "M0007".</span><span class="sxs-lookup"><span data-stu-id="19b25-122">Select M0007.</span></span>  
8. <span data-ttu-id="19b25-123">قم بتوسيع القسم "الأحداث".</span><span class="sxs-lookup"><span data-stu-id="19b25-123">Expand the Events section.</span></span>
9. <span data-ttu-id="19b25-124">في حقل "حدث تزويد المخزون"، حدد "دُفعة".</span><span class="sxs-lookup"><span data-stu-id="19b25-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="19b25-125">يؤدي هذا إلى إنشاء كانبان لتلبية الاحتياجات المادية في الموقع ذي الصلة أثناء معالجة حدث تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="19b25-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="19b25-126">تعيين الحد الأدنى لكمية الصنف</span><span class="sxs-lookup"><span data-stu-id="19b25-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="19b25-127">انقر لمتابعة الارتباط في حقل "المنتج".</span><span class="sxs-lookup"><span data-stu-id="19b25-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="19b25-128">انقر لمتابعة الارتباط في الحقل "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="19b25-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="19b25-129">قم بتوسيع مربع حقائق صورة المنتج.</span><span class="sxs-lookup"><span data-stu-id="19b25-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="19b25-130">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="19b25-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="19b25-131">انقر فوق "تغطية الصنف‬".</span><span class="sxs-lookup"><span data-stu-id="19b25-131">Click Item coverage.</span></span>
6. <span data-ttu-id="19b25-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="19b25-132">Click New.</span></span>
7. <span data-ttu-id="19b25-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="19b25-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="19b25-134">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="19b25-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="19b25-135">قم بتعيين المستودع على 12.</span><span class="sxs-lookup"><span data-stu-id="19b25-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="19b25-136">عيّن الحد الأدنى إلى "200".</span><span class="sxs-lookup"><span data-stu-id="19b25-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="19b25-137">تشغيل الوظيفة الدفعية إنشاء حدث</span><span class="sxs-lookup"><span data-stu-id="19b25-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="19b25-138">انتقل إلى التحكم بالإنتاج‬ > المهام الدورية > معالجة دُفعة وظيفة كانبان‬ > معالجة حدث تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="19b25-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="19b25-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="19b25-139">Click OK.</span></span>
3. <span data-ttu-id="19b25-140">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="19b25-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="19b25-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="19b25-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="19b25-142">حدد قاعدة كانبان التي أنشأتها في السابق.</span><span class="sxs-lookup"><span data-stu-id="19b25-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="19b25-143">قم بتوسيع القسم "كانبان".</span><span class="sxs-lookup"><span data-stu-id="19b25-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="19b25-144">لاحظ أنه تم إنشاء كانبان لنقل المواد المطلوبة إلى المستودع 12.</span><span class="sxs-lookup"><span data-stu-id="19b25-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

