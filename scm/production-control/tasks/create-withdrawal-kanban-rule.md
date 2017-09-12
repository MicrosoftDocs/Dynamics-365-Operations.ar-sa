--- 
title: "إنشاء قاعدة كانبان لسحب"
description: "يظهر هذا الإجراء الإعداد المطلوب لإنشاء قاعدة كانبان للسحب لنقل المواد في بيئة محدودة."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="d6fe0-103">إنشاء قاعدة كانبان لسحب</span><span class="sxs-lookup"><span data-stu-id="d6fe0-103">Create a withdrawal kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6fe0-104">يظهر هذا الإجراء الإعداد المطلوب لإنشاء قاعدة كانبان للسحب لنقل المواد في بيئة محدودة.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="d6fe0-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d6fe0-106">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لتزويد مادة جديدة أو معدلة.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="d6fe0-107">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="d6fe0-107">Create new kanban rule</span></span>
1. <span data-ttu-id="d6fe0-108">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="d6fe0-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-109">Click New.</span></span>
3. <span data-ttu-id="d6fe0-110">في حقل "النوع"، حدد "انسحاب".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="d6fe0-111">يتم استخدام نوع الانسحاب لقواعد كانبان لنقل المواد أو السلع.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="d6fe0-112">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="d6fe0-113">حدد ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="d6fe0-114">يتم إعداد هذا النشاط لنقل المكونات من المستودع 11 والموقع 11 إلى 12 المستودع والموقع 12.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="d6fe0-115">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="d6fe0-116">حدد "M0007".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-116">Select M0007.</span></span>  
6. <span data-ttu-id="d6fe0-117">في الحقل "وقت الإنتاج‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="d6fe0-118">على سبيل المثال، 60.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-118">For example, 60.</span></span>  
7. <span data-ttu-id="d6fe0-119">في الحقل "وحدة القياس"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="d6fe0-120">فمثلاً، الدقائق.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="d6fe0-121">قم بإعداد كميات لكانبان</span><span class="sxs-lookup"><span data-stu-id="d6fe0-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="d6fe0-122">قم بتعيين الكمية الافتراضية على "5".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="d6fe0-123">هذه هي الكمية التي سيتم تحويلها لكل كانبان.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="d6fe0-124">في الحقل "كانبان الكمية الثابتة"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="d6fe0-125">وهذا هو كمية كانبان التي يجب أن تكون نشطة.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="d6fe0-126">في هذه الحالة، يوجد 2 كانبان تنقل كل منها 5.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="d6fe0-127">في الحقل "الحد الأدنى للتنبيه"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="d6fe0-128">تُستخدم لتعقب الحد الأدنى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="d6fe0-129">على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="d6fe0-130">في الحقل "الحد الأقصى للتنبيه"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="d6fe0-131">تُستخدم لتعقب الحد الأقصى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="d6fe0-132">على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="d6fe0-133">إنشاء بطاقات كانبان</span><span class="sxs-lookup"><span data-stu-id="d6fe0-133">Create kanbans</span></span>
1. <span data-ttu-id="d6fe0-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-134">Click Save.</span></span>
    * <span data-ttu-id="d6fe0-135">يجب حفظ قاعدة كانبان قبل إنشاء كانبان.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="d6fe0-136">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-136">Click Add.</span></span>
    * <span data-ttu-id="d6fe0-137">لاحظ أنه لا وجود لكانبان نشطة، بسبب أن "عدد الكانبان الجديدة" المقترح هو 2، وهذا يساوي "كمية كانبان ثابتة".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="d6fe0-138">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="d6fe0-138">Click Create.</span></span>
    * <span data-ttu-id="d6fe0-139">سيؤدي هذا إلى إنشاء 2 كانبان.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="d6fe0-140">لاحظ أنه تم إنشاء 2 كانبان، لكل منها 5، لقاعدة كانبان للسحب.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="d6fe0-141">وهذه هي الخطوة الأخيرة في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-141">This is the last step in this procedure.</span></span>  


