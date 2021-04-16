---
title: إنشاء قاعدة كانبان باستخدام حدث بند كانبان
description: ينشئ هذا الإجراء قاعدة كانبان باستخدام إعداد حدث بند كانبان للضغط على المشغّل من نشاط معالجة.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe92336c3f80909e5b0865b461e45d55bf08c4b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829128"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="6a70e-103">إنشاء قاعدة كانبان باستخدام حدث بند كانبان</span><span class="sxs-lookup"><span data-stu-id="6a70e-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a70e-104">ينشئ هذا الإجراء قاعدة كانبان باستخدام إعداد حدث بند كانبان للضغط على المشغّل من نشاط معالجة.</span><span class="sxs-lookup"><span data-stu-id="6a70e-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="6a70e-105">يتم تشغيل قاعدة كانبان بواسطة نشاط معالجة كانبان، مع كمية مساوية لـ 25 أو أكبر من 25 لكل منها.</span><span class="sxs-lookup"><span data-stu-id="6a70e-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="6a70e-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="6a70e-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6a70e-107">هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند قيامه بتحضير عملية إنتاج منتج جديد أو معدل في بيئة محدودة.</span><span class="sxs-lookup"><span data-stu-id="6a70e-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="6a70e-108">إنشاء قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="6a70e-108">Create a kanban rule</span></span>
1. <span data-ttu-id="6a70e-109">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="6a70e-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="6a70e-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6a70e-110">Click New.</span></span>
3. <span data-ttu-id="6a70e-111">في الحقل "إستراتيجية التزويد"، حدد "الحدث".</span><span class="sxs-lookup"><span data-stu-id="6a70e-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="6a70e-112">يؤدي ذلك إلى إنشاء كانبان من الطلب مباشرة.</span><span class="sxs-lookup"><span data-stu-id="6a70e-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="6a70e-113">ويتم استخدامه لتعيين القواعد التي تحدد سيناريو إدراج في الأمر.</span><span class="sxs-lookup"><span data-stu-id="6a70e-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="6a70e-114">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6a70e-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="6a70e-115">أدخل SpeakerAssemblyAndPolish أو حدده.</span><span class="sxs-lookup"><span data-stu-id="6a70e-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="6a70e-116">يجب أن يكون النشاط الأول لقاعدة كانبان للتصنيع عبارة عن نشاط معالجة في تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6a70e-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="6a70e-117">عندما تحدد النشاط، يتم نسخ تواريخ صلاحية النشاط إلى تواريخ صلاحية قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="6a70e-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="6a70e-118">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="6a70e-118">Expand the Details section.</span></span>
6. <span data-ttu-id="6a70e-119">في حقل "المنتج"، اكتب "L0001".</span><span class="sxs-lookup"><span data-stu-id="6a70e-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="6a70e-120">قم بتوسيع القسم "الأحداث".</span><span class="sxs-lookup"><span data-stu-id="6a70e-120">Expand the Events section.</span></span>
8. <span data-ttu-id="6a70e-121">في الحقل "حدث سطر كانبان"، حدد "تلقائي".</span><span class="sxs-lookup"><span data-stu-id="6a70e-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="6a70e-122">يؤدي ذلك إلى إنشاء كانبان الحدث عند الطلب.</span><span class="sxs-lookup"><span data-stu-id="6a70e-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="6a70e-123">يُستخدم الحقل لتكوين قواعد كانبان التي تزود المواد المطلوبة لنشاط عملية نهائية.</span><span class="sxs-lookup"><span data-stu-id="6a70e-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="6a70e-124">عند تحديد "تلقائي"، يتم إنشاء كانبان الحدث مع الطلب.</span><span class="sxs-lookup"><span data-stu-id="6a70e-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="6a70e-125">يوصي بهذا الإعداد إذا كنت تتوقع تنفيذ الإنتاج في نفس اليوم.</span><span class="sxs-lookup"><span data-stu-id="6a70e-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="6a70e-126">قم بتعيين الحد الأدنى لكمية الحدث على "25".</span><span class="sxs-lookup"><span data-stu-id="6a70e-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="6a70e-127">يتم إنشاء كانبان الأحداث عندما تكون كمية الطلب مساوية لهذا الحقل أو أكبر منه.</span><span class="sxs-lookup"><span data-stu-id="6a70e-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="6a70e-128">يُعد ذلك مفيدًا إذا كنت تريد إنتاج كمية طلب أقل من هذا الحقل على جهاز وكمية أكبر من هذا الحقل على جهاز آخر.</span><span class="sxs-lookup"><span data-stu-id="6a70e-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="6a70e-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6a70e-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="6a70e-130">إنشاء أمر مبيعات وتشغيل سلسلة كانبان</span><span class="sxs-lookup"><span data-stu-id="6a70e-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="6a70e-131">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6a70e-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6a70e-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6a70e-132">Click New.</span></span>
3. <span data-ttu-id="6a70e-133">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6a70e-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="6a70e-134">حدد حساب العميل US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="6a70e-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="6a70e-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6a70e-135">Click OK.</span></span>
5. <span data-ttu-id="6a70e-136">في الحقل "رقم الصنف، اكتب "L0001".</span><span class="sxs-lookup"><span data-stu-id="6a70e-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="6a70e-137">L0001 هو الصنف الذي قمت بإنشاء قاعدة كانبان له.</span><span class="sxs-lookup"><span data-stu-id="6a70e-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="6a70e-138">تعيين الكمية إلى "27".</span><span class="sxs-lookup"><span data-stu-id="6a70e-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="6a70e-139">لأن 27 أكبر من الحد الأدنى للكمية 25 في قاعدة كانبان، سيؤدي ذلك إلى تشغيل كانبان حدث.</span><span class="sxs-lookup"><span data-stu-id="6a70e-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="6a70e-140">في الحقل "الموقع"، اكتب ''1".</span><span class="sxs-lookup"><span data-stu-id="6a70e-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="6a70e-141">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6a70e-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6a70e-142">حديد المستودع 13.</span><span class="sxs-lookup"><span data-stu-id="6a70e-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="6a70e-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6a70e-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="6a70e-144">عرض كانبان الذي تم إنشاؤه باستخدام قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="6a70e-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="6a70e-145">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="6a70e-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="6a70e-146">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6a70e-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6a70e-147">قم بتوسيع القسم "كانبان".</span><span class="sxs-lookup"><span data-stu-id="6a70e-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="6a70e-148">لاحظ أنه قد تم إنشاء كانبان لـ 27 لمعالجة النشاط استنادًا إلى قاعدة كانبان التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="6a70e-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="6a70e-149">هذه هي الخطوة الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="6a70e-149">This is the last step.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]