--- 
title: "إنشاء قاعدة كانبان لحدث بند قائمة مكونات الصنف"
description: "تركز هذه المهمة على الإعداد المطلوب لإنشاء قاعدة كانبان الحدث لضمان بنود مكونات قائمة الصنف الخاصة بالإنتاج في بيئة إنتاج محدودة مختلطة وتقليدية."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="47511-103">إنشاء قاعدة كانبان لحدث بند قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="47511-103">Create a BOM line event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47511-104">تركز هذه المهمة على الإعداد المطلوب لإنشاء قاعدة كانبان الحدث لضمان بنود مكونات قائمة الصنف الخاصة بالإنتاج في بيئة إنتاج محدودة مختلطة وتقليدية.</span><span class="sxs-lookup"><span data-stu-id="47511-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="47511-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="47511-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="47511-106">هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند تحضير إنتاج منتج جديد أو معدل.</span><span class="sxs-lookup"><span data-stu-id="47511-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="47511-107">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="47511-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="47511-108">انتقل إلى التحكم بالإنتاج‬ > المهام الدورية > حساب كمية كانبان > قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="47511-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="47511-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="47511-109">Click New.</span></span>
3. <span data-ttu-id="47511-110">في حقل "النوع"، حدد "انسحاب".</span><span class="sxs-lookup"><span data-stu-id="47511-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="47511-111">يتم استخدام نوع الانسحاب لإنشاء نقل عمليات كانبان.</span><span class="sxs-lookup"><span data-stu-id="47511-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="47511-112">في الحقل "إستراتيجية التزويد"، حدد "الحدث".</span><span class="sxs-lookup"><span data-stu-id="47511-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="47511-113">يتم تحديد استراتيجية الحدث لإنشاء نقل عمليات كانبان استنادًا إلى حدث.</span><span class="sxs-lookup"><span data-stu-id="47511-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="47511-114">فيما بعد في دليل الوظيفة، سنقوم بتشغيله عن طريق تقدير أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="47511-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="47511-115">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="47511-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="47511-116">أدخل ReplenishSpeakerComponents أو حدده.</span><span class="sxs-lookup"><span data-stu-id="47511-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="47511-117">يحتوي نشاط النقل هذا على مستودع استلام (مخرجات) وموقع 12، مما يعني أنه سيتم نقل المواد إلى موقع 12 في مستودع 12.</span><span class="sxs-lookup"><span data-stu-id="47511-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="47511-118">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="47511-118">Expand the Details section.</span></span>
7. <span data-ttu-id="47511-119">في الحقل "المنتج"، أدخل قيمة M0001 أو حددها.</span><span class="sxs-lookup"><span data-stu-id="47511-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="47511-120">قم بتوسيع القسم "الأحداث".</span><span class="sxs-lookup"><span data-stu-id="47511-120">Expand the Events section.</span></span>
9. <span data-ttu-id="47511-121">في الحقل "حدث بند قائمة مكونات الصنف"، حدد "تلقائي".</span><span class="sxs-lookup"><span data-stu-id="47511-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="47511-122">ومع تعيين حقل حدث بند قائمة مكونات الصنف إلى تلقائي، فإنه سيتم إنشاء كانبان لتلبية الاحتياجات المادية لبنود قائمة مكونات صنف أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="47511-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="47511-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="47511-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="47511-124">إنشاء أمر إنتاج جديد وتعديله</span><span class="sxs-lookup"><span data-stu-id="47511-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="47511-125">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="47511-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="47511-126">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="47511-126">Click New production order.</span></span>
3. <span data-ttu-id="47511-127">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="47511-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="47511-128">أدخل "L0001" أو حدده.</span><span class="sxs-lookup"><span data-stu-id="47511-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="47511-129">إننا نستخدم الصنف L0001 لأنه يتم تضمين الصنف M0001 في قائمة مكونات الصنف للصنف L0001.</span><span class="sxs-lookup"><span data-stu-id="47511-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="47511-130">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="47511-130">Click Create.</span></span>
5. <span data-ttu-id="47511-131">في القائمة، انقر فوق الارتباط في الصف لـ L0001</span><span class="sxs-lookup"><span data-stu-id="47511-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="47511-132">انقر فوق "قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="47511-132">Click BOM.</span></span>
7. <span data-ttu-id="47511-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="47511-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="47511-134">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="47511-134">Click Edit.</span></span>
9. <span data-ttu-id="47511-135">في حقل "نوع البند"، حدد "التوريد مثبت السعر.</span><span class="sxs-lookup"><span data-stu-id="47511-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="47511-136">يتم تحديد التوريد مثبت السعر لتشغيل إنشاء توريد كانبان.</span><span class="sxs-lookup"><span data-stu-id="47511-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="47511-137">حدد "لا" في حقل "استهلاك المورد".</span><span class="sxs-lookup"><span data-stu-id="47511-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="47511-138">يعمل إلغاء تحديد خانة الاختيار الخاصة باستهلاك الموارد على إتاحة تغيير المستودع.</span><span class="sxs-lookup"><span data-stu-id="47511-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="47511-139">قم بتوسيع مقطع "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="47511-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="47511-140">في الحقل "المستودع"، اكتب "12".</span><span class="sxs-lookup"><span data-stu-id="47511-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="47511-141">يتم تعيين المستودع إلى 12 لأنه مستودع المخرجات لنشاط السحب.</span><span class="sxs-lookup"><span data-stu-id="47511-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="47511-142">في الحقل "الموقع"، اكتب "12".</span><span class="sxs-lookup"><span data-stu-id="47511-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="47511-143">يتم تعيين الموقع إلى 12 لأنه موقع المخرجات لنشاط السحب.</span><span class="sxs-lookup"><span data-stu-id="47511-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="47511-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="47511-144">Close the page.</span></span>
15. <span data-ttu-id="47511-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="47511-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="47511-146">تقدير أمر الإنتاج وعرض كانبان التي تم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="47511-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="47511-147">انقر فوق "تقدير".</span><span class="sxs-lookup"><span data-stu-id="47511-147">Click Estimate.</span></span>
    * <span data-ttu-id="47511-148">سيعمل تقدير أمر الإنتاج على تشغيل إنشاء كانبان المقترنة بتوريد صنف M0001.</span><span class="sxs-lookup"><span data-stu-id="47511-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="47511-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="47511-149">Click OK.</span></span>
3. <span data-ttu-id="47511-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="47511-150">Close the page.</span></span>
4. <span data-ttu-id="47511-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="47511-151">Close the page.</span></span>
5. <span data-ttu-id="47511-152">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="47511-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="47511-153">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="47511-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="47511-154">حدد قاعدة كانبان الحدث التي تم إنشائها للصنف M0001.</span><span class="sxs-lookup"><span data-stu-id="47511-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="47511-155">قم بتوسيع القسم "كانبان".</span><span class="sxs-lookup"><span data-stu-id="47511-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="47511-156">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="47511-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="47511-157">لاحظ أنه تم إنشاء كانبان لإمداد M0001 لأمر الإنتاج المقدر.</span><span class="sxs-lookup"><span data-stu-id="47511-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="47511-158">هذه هي الخطوة الأخيرة!</span><span class="sxs-lookup"><span data-stu-id="47511-158">This is the last step!</span></span>  


