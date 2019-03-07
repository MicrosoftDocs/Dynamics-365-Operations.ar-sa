---
title: إنشاء قاعدة كانبان الكمية الثابتة للتصنيع
description: يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان تصنيع ثابتة لبدء أنشطة التحويل وفي خلية عمل وفي البيئة محدودة الفاقد.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0f58d1e265fb001474eb572b9bc325cf08790c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "338672"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="12f1a-103">إنشاء قاعدة كانبان الكمية الثابتة للتصنيع</span><span class="sxs-lookup"><span data-stu-id="12f1a-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12f1a-104">يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان تصنيع ثابتة لبدء أنشطة التحويل وفي خلية عمل وفي البيئة محدودة الفاقد.</span><span class="sxs-lookup"><span data-stu-id="12f1a-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="12f1a-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="12f1a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="12f1a-106">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج منتج جديد أو معدل.</span><span class="sxs-lookup"><span data-stu-id="12f1a-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="12f1a-107">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="12f1a-107">Create new kanban rule</span></span>
1. <span data-ttu-id="12f1a-108">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="12f1a-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="12f1a-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="12f1a-109">Click New.</span></span>
    * <span data-ttu-id="12f1a-110">لاحظ أن النوع الافتراضي هو "التصنيع" وأنه يتم تثبيت إستراتيجية التزويد.</span><span class="sxs-lookup"><span data-stu-id="12f1a-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="12f1a-111">وليس عليك تغيير هذه المعلمات.</span><span class="sxs-lookup"><span data-stu-id="12f1a-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="12f1a-112">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f1a-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="12f1a-113">وهذا النشاط الذي سيتم تنفيذه لبطاقات كانبان التي يتم إنشاؤها استناداً إلى قاعدة كانبان هذه.</span><span class="sxs-lookup"><span data-stu-id="12f1a-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="12f1a-114">حدد "SpeakerTestAndPackaging".</span><span class="sxs-lookup"><span data-stu-id="12f1a-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="12f1a-115">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="12f1a-115">Expand the Details section.</span></span>
5. <span data-ttu-id="12f1a-116">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f1a-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="12f1a-117">حدد "L0050".</span><span class="sxs-lookup"><span data-stu-id="12f1a-117">Select L0050.</span></span>  
6. <span data-ttu-id="12f1a-118">في الحقل "وحدة القياس"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="12f1a-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="12f1a-119">حدد "دقائق".</span><span class="sxs-lookup"><span data-stu-id="12f1a-119">Select minutes.</span></span>  
7. <span data-ttu-id="12f1a-120">في الحقل "وقت الإنتاج‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="12f1a-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="12f1a-121">أدخل (5).</span><span class="sxs-lookup"><span data-stu-id="12f1a-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="12f1a-122">تعيين الكميات</span><span class="sxs-lookup"><span data-stu-id="12f1a-122">Set quantities</span></span>
1. <span data-ttu-id="12f1a-123">قم بتوسيع القسم "الكميات".</span><span class="sxs-lookup"><span data-stu-id="12f1a-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="12f1a-124">قم بتعيين الكمية الافتراضية على "10".</span><span class="sxs-lookup"><span data-stu-id="12f1a-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="12f1a-125">هذه هي الكمية التي سيتم تحويلها لكل كانبان.</span><span class="sxs-lookup"><span data-stu-id="12f1a-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="12f1a-126">حدد خانة اختيار "نسبة الفرق في كمية المنتج".</span><span class="sxs-lookup"><span data-stu-id="12f1a-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="12f1a-127">وفي هذه الحالة، يمكن إكمال كانبان المحددة بفرق عن الكمية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="12f1a-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="12f1a-128">للسماح بإكمال كانبان بكمية من 8 إلى 12، قم بتعيين كلا نسبتي الفرق على 2.</span><span class="sxs-lookup"><span data-stu-id="12f1a-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="12f1a-129">قم بتعيين الفرق على أقل من "2".</span><span class="sxs-lookup"><span data-stu-id="12f1a-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="12f1a-130">وسيتيح هذا إكمال كانبان وصولاً إلى 10-2 = 8</span><span class="sxs-lookup"><span data-stu-id="12f1a-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="12f1a-131">قم بتعيين الفرق على أكبر من "2".</span><span class="sxs-lookup"><span data-stu-id="12f1a-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="12f1a-132">وسيتيح هذا إكمال كانبان وصولاً إلى 10+2 = 12</span><span class="sxs-lookup"><span data-stu-id="12f1a-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="12f1a-133">في الحقل "كانبان الكمية الثابتة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="12f1a-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="12f1a-134">وهذا هو كمية كانبان التي يجب أن تكون نشطة.</span><span class="sxs-lookup"><span data-stu-id="12f1a-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="12f1a-135">في هذه الحالة، يوجد 5 كانبان تعالج كل منها 10.</span><span class="sxs-lookup"><span data-stu-id="12f1a-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="12f1a-136">في الحقل "الحد الأدنى للتنبيه"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="12f1a-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="12f1a-137">تُستخدم لتعقب الحد الأدنى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="12f1a-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="12f1a-138">على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="12f1a-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="12f1a-139">في الحقل "الحد الأقصى للتنبيه"، أدخل "4".</span><span class="sxs-lookup"><span data-stu-id="12f1a-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="12f1a-140">تُستخدم لتعقب الحد الأقصى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="12f1a-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="12f1a-141">على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="12f1a-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="12f1a-142">في الحقل "كمية التخطيط التلقائي‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="12f1a-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="12f1a-143">يعني تعيين هذا على 1 أنه سيتم تخطيط كل كانبان تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="12f1a-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="12f1a-144">إذا أدخلنا 3، سيتم تخطيك الكانبان حتى توجد 3 كانبان فارغة على استعداد للتخطيط.</span><span class="sxs-lookup"><span data-stu-id="12f1a-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="12f1a-145">وهذا مفيد لتجميع العمل وتجنب الكثير من الإعداد.</span><span class="sxs-lookup"><span data-stu-id="12f1a-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="12f1a-146">إنشاء كانبان</span><span class="sxs-lookup"><span data-stu-id="12f1a-146">Create Kanbans</span></span>
1. <span data-ttu-id="12f1a-147">قم بتوسيع القسم "كانبان".</span><span class="sxs-lookup"><span data-stu-id="12f1a-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="12f1a-148">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="12f1a-148">Click Save.</span></span>
    * <span data-ttu-id="12f1a-149">يجب حفظ قاعدة كانبان قبل إنشاء كانبان.</span><span class="sxs-lookup"><span data-stu-id="12f1a-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="12f1a-150">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="12f1a-150">Click Add.</span></span>
    * <span data-ttu-id="12f1a-151">لاحظ أنه لا توجد أي كانبانات نشطة، ولهذا السبب فإن "عدد بطاقات كانبان الجديدة‬" المقترح هو 5.</span><span class="sxs-lookup"><span data-stu-id="12f1a-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="12f1a-152">يساوي ذلك "كمية كانبان الثابتة‬".</span><span class="sxs-lookup"><span data-stu-id="12f1a-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="12f1a-153">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="12f1a-153">Click Create.</span></span>
    * <span data-ttu-id="12f1a-154">سيؤدي هذا إلى إنشاء 5 كانبان.</span><span class="sxs-lookup"><span data-stu-id="12f1a-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="12f1a-155">لاحظ أنه تم إنشاء 5 كانبان، لكل منها 10، لقاعدة كانبان التصنيع هذه.</span><span class="sxs-lookup"><span data-stu-id="12f1a-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="12f1a-156">وهذه هي الخطوة الأخيرة في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="12f1a-156">This is the last step in this procedure.</span></span>  

