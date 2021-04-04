---
title: إنشاء قاعدة كانبان لسحب
description: يظهر هذا الإجراء الإعداد المطلوب لإنشاء قاعدة كانبان للسحب لنقل المواد في بيئة محدودة.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1e1fc6dff80457cecdcd1659ffa42fd6c9c4447
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263984"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="b1cdf-103">إنشاء قاعدة كانبان لسحب</span><span class="sxs-lookup"><span data-stu-id="b1cdf-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1cdf-104">يظهر هذا الإجراء الإعداد المطلوب لإنشاء قاعدة كانبان للسحب لنقل المواد في بيئة محدودة.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="b1cdf-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b1cdf-106">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لتزويد مادة جديدة أو معدلة.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="b1cdf-107">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="b1cdf-107">Create new kanban rule</span></span>
1. <span data-ttu-id="b1cdf-108">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="b1cdf-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-109">Click New.</span></span>
3. <span data-ttu-id="b1cdf-110">في حقل "النوع"، حدد "انسحاب".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="b1cdf-111">يتم استخدام نوع الانسحاب لقواعد كانبان لنقل المواد أو السلع.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="b1cdf-112">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cdf-113">حدد ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="b1cdf-114">يتم إعداد هذا النشاط لنقل المكونات من المستودع 11 والموقع 11 إلى 12 المستودع والموقع 12.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="b1cdf-115">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cdf-116">حدد "M0007".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-116">Select M0007.</span></span>  
6. <span data-ttu-id="b1cdf-117">في الحقل "وقت الإنتاج‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="b1cdf-118">على سبيل المثال، 60.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-118">For example, 60.</span></span>  
7. <span data-ttu-id="b1cdf-119">في الحقل "وحدة القياس"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cdf-120">فمثلاً، الدقائق.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="b1cdf-121">قم بإعداد كميات لكانبان</span><span class="sxs-lookup"><span data-stu-id="b1cdf-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="b1cdf-122">قم بتعيين الكمية الافتراضية على "5".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="b1cdf-123">هذه هي الكمية التي سيتم تحويلها لكل كانبان.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="b1cdf-124">في الحقل "كانبان الكمية الثابتة"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="b1cdf-125">وهذا هو كمية كانبان التي يجب أن تكون نشطة.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="b1cdf-126">في هذه الحالة، يوجد 2 كانبان تنقل كل منها 5.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="b1cdf-127">في الحقل "الحد الأدنى للتنبيه"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="b1cdf-128">تُستخدم لتعقب الحد الأدنى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="b1cdf-129">على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="b1cdf-130">في الحقل "الحد الأقصى للتنبيه"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="b1cdf-131">تُستخدم لتعقب الحد الأقصى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="b1cdf-132">على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="b1cdf-133">إنشاء بطاقات كانبان</span><span class="sxs-lookup"><span data-stu-id="b1cdf-133">Create kanbans</span></span>
1. <span data-ttu-id="b1cdf-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-134">Click Save.</span></span>
    * <span data-ttu-id="b1cdf-135">يجب حفظ قاعدة كانبان قبل إنشاء كانبان.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="b1cdf-136">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-136">Click Add.</span></span>
    * <span data-ttu-id="b1cdf-137">لاحظ أنه لا وجود لكانبان نشطة، بسبب أن "عدد الكانبان الجديدة" المقترح هو 2، وهذا يساوي "كمية كانبان ثابتة".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="b1cdf-138">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="b1cdf-138">Click Create.</span></span>
    * <span data-ttu-id="b1cdf-139">سيؤدي هذا إلى إنشاء 2 كانبان.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="b1cdf-140">لاحظ أنه تم إنشاء 2 كانبان، لكل منها 5، لقاعدة كانبان للسحب.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="b1cdf-141">وهذه هي الخطوة الأخيرة في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-141">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]