--- 
title: "إنشاء قاعدة كانبان لحدث المبيعات"
description: "يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان يتم تشغيلها أثناء إنشاء أمر مبيعات."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: e727f240b7aebe501f073cf8c4e311530e7605e1
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="c8f22-103">إنشاء قاعدة كانبان لحدث المبيعات</span><span class="sxs-lookup"><span data-stu-id="c8f22-103">Create a sales event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8f22-104">يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان يتم تشغيلها أثناء إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="c8f22-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="c8f22-105">تزود قاعدة كانبان الخاصة بالحدث المتطلبات التي تنشأ من بنود أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c8f22-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="c8f22-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="c8f22-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c8f22-107">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج منتج جديد أو معدل.</span><span class="sxs-lookup"><span data-stu-id="c8f22-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="c8f22-108">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="c8f22-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="c8f22-109">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="c8f22-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="c8f22-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c8f22-110">Click New.</span></span>
3. <span data-ttu-id="c8f22-111">في الحقل "إستراتيجية التزويد"، حدد "الحدث".</span><span class="sxs-lookup"><span data-stu-id="c8f22-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="c8f22-112">يعني تحديد الحدث تشغيل قاعدة كانبان بواسطة الحدث، على سبيل المثال، إنشاء بند أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="c8f22-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="c8f22-113">يتم تطبيق هذا على المناطق التي يجب أن يغطي كل كانبان طلب محدد.</span><span class="sxs-lookup"><span data-stu-id="c8f22-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="c8f22-114">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f22-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f22-115">حدد "التجميع النهائي".</span><span class="sxs-lookup"><span data-stu-id="c8f22-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="c8f22-116">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="c8f22-116">Expand the Details section.</span></span>
6. <span data-ttu-id="c8f22-117">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f22-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f22-118">حدد "L0050".</span><span class="sxs-lookup"><span data-stu-id="c8f22-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="c8f22-119">تحديد حدث</span><span class="sxs-lookup"><span data-stu-id="c8f22-119">Define an event</span></span>
1. <span data-ttu-id="c8f22-120">قم بتوسيع القسم "الأحداث".</span><span class="sxs-lookup"><span data-stu-id="c8f22-120">Expand the Events section.</span></span>
2. <span data-ttu-id="c8f22-121">في الحقل "حدث المبيعات"، حدد "تلقائي".</span><span class="sxs-lookup"><span data-stu-id="c8f22-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="c8f22-122">بتحديد "تلقائي" لحدث المبيعات، سيتم تشغيل قاعدة كانبان هذه تلقائياً عندما يطابق بند مبيعات المنتج وموقع الاستلام.</span><span class="sxs-lookup"><span data-stu-id="c8f22-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="c8f22-123">في هذا الإجراء، يُستخدم المنتج L0050 بالمستودع 13.</span><span class="sxs-lookup"><span data-stu-id="c8f22-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="c8f22-124">قم بتعيين الحد الأدنى لكمية الحدث على "50".</span><span class="sxs-lookup"><span data-stu-id="c8f22-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="c8f22-125">بتعيين الحد الأدنى 50 لكمية الحدث، لن يتم تشغيل قاعدة كانبان إلا بواسطة الأحداث التي تكون كميتها 50 أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="c8f22-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="c8f22-126">قم بتوسيع القسم "تدفق الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="c8f22-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="c8f22-127">لاحظ أن موقع الاستلام هو المستودع 13.</span><span class="sxs-lookup"><span data-stu-id="c8f22-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="c8f22-128">وهذا يعني أنه سيتم تشغيل قاعدة كانبان هذه لهذا الموقع.</span><span class="sxs-lookup"><span data-stu-id="c8f22-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="c8f22-129">في هذا المثال، سيشغل بند مبيعات للمنتج L0050، بكمية 50 أو أكثر في المستودع 13، قاعدة كانبان هذه.</span><span class="sxs-lookup"><span data-stu-id="c8f22-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="c8f22-130">إنشاء بند مبيعات لتشغيل قاعدة كانبان خاصة بحدث</span><span class="sxs-lookup"><span data-stu-id="c8f22-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="c8f22-131">انتقل إلى "كافة أوامر المبيعات‬".</span><span class="sxs-lookup"><span data-stu-id="c8f22-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="c8f22-132">يتم عرض تحذير عند حفظ قاعدة كانبان، وهو ما يعني أنه سيتم إنشاء كانبان في الوقت الفعلي أثناء إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="c8f22-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="c8f22-133">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c8f22-133">Click New.</span></span>
3. <span data-ttu-id="c8f22-134">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f22-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f22-135">على سبيل المثال، حدد "الولايات المتحدة-003".</span><span class="sxs-lookup"><span data-stu-id="c8f22-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="c8f22-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c8f22-136">Click OK.</span></span>
5. <span data-ttu-id="c8f22-137">في الحقل "رقم الصنف، اكتب "L0050".</span><span class="sxs-lookup"><span data-stu-id="c8f22-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="c8f22-138">في الحقل "الموقع"، اكتب ''1".</span><span class="sxs-lookup"><span data-stu-id="c8f22-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="c8f22-139">حدد "الموقع 1" لأن المستودع 13 موجود بالموقع 1.</span><span class="sxs-lookup"><span data-stu-id="c8f22-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="c8f22-140">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f22-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f22-141">قم بتعيين المستودع على 13.</span><span class="sxs-lookup"><span data-stu-id="c8f22-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="c8f22-142">تعيين الكمية إلى "75".</span><span class="sxs-lookup"><span data-stu-id="c8f22-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="c8f22-143">أدخل كمية 50 أو أكثر، لتشغيل قاعدة كانبان التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c8f22-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="c8f22-144">التحقق من إنشاء تلك الكانبان</span><span class="sxs-lookup"><span data-stu-id="c8f22-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="c8f22-145">انقر فوق "المنتج والتوريد".</span><span class="sxs-lookup"><span data-stu-id="c8f22-145">Click Product and supply.</span></span>
2. <span data-ttu-id="c8f22-146">انقر فوق "عرض شجرة تثبيت السعر".</span><span class="sxs-lookup"><span data-stu-id="c8f22-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="c8f22-147">لاحظ أنه يتم إنشاء كانبان بنفس الكمية كبند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c8f22-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="c8f22-148">ويمكنك أيضًا مشاهدة إصدارات المواد اللازمة لإنتاج L0050.</span><span class="sxs-lookup"><span data-stu-id="c8f22-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="c8f22-149">وهذه هي الخطوة الأخيرة في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="c8f22-149">This is the last step in this procedure.</span></span>  


