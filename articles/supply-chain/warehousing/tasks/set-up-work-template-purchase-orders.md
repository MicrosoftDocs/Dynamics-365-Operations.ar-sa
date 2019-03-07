---
title: إعداد قالب عمل لأوامر الشراء
description: يركز هذا الإجراء على إعداد قالب العمل البسيط لاستخدامه عند تخزين الأصناف المستلمة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "318018"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="d42f1-103">إعداد قالب عمل لأوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="d42f1-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d42f1-104">يركز هذا الإجراء على إعداد قالب العمل البسيط لاستخدامه عند تخزين الأصناف المستلمة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="d42f1-105">تحدد قوالب العمل مجموعة الإرشادات المقدمة إلى عامل المستودع على جهاز محمول عند نقل الأصناف من منطقة الاستلام.</span><span class="sxs-lookup"><span data-stu-id="d42f1-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="d42f1-106">يمكنك استخدام هذا الإجراء مع البيانات المذكورة في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d42f1-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="d42f1-107">قبل تشغيل هذا الدليل، قم بإنشاء معرف وعاء عمل.</span><span class="sxs-lookup"><span data-stu-id="d42f1-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="d42f1-108">في هذا المثال، يُستخدم معرف وعاء عمل يتم استدعاؤه في "الوارد".</span><span class="sxs-lookup"><span data-stu-id="d42f1-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="d42f1-109">هذا الإجراء مخصص لمدير المستودعات.</span><span class="sxs-lookup"><span data-stu-id="d42f1-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="d42f1-110">انتقل إلى إدارة المستودعات > إعداد > العمل > قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="d42f1-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="d42f1-111">في الحقل "نوع أمر العمل"، حدد "أوامر الشراء".</span><span class="sxs-lookup"><span data-stu-id="d42f1-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="d42f1-112">إنشاء رأس قالب عمل</span><span class="sxs-lookup"><span data-stu-id="d42f1-112">Create a work template header</span></span>
1. <span data-ttu-id="d42f1-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d42f1-113">Click New.</span></span>
2. <span data-ttu-id="d42f1-114">في الحقل "الرقم التسلسلي"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d42f1-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="d42f1-115">هذا هو التسلسل الذي يتم من خلاله تقييم قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="d42f1-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="d42f1-116">يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="d42f1-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="d42f1-117">في الحقل "قالب العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="d42f1-118">هذا هو المعرف الفريد لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d42f1-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="d42f1-119">في الحقل "وصف قالب العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="d42f1-120">لن يتم التحقق من الخيار "صالح" حتى تُكمل جميع المعلومات التي يحتاجها القالب ثم تنقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d42f1-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="d42f1-121">لا يمكن معالجة أمر عمل من النوع "أمر الشراء" تلقائياً، فاترك الخيار "المعالجة تلقائياً" معينًا على "لا".</span><span class="sxs-lookup"><span data-stu-id="d42f1-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="d42f1-122">في الحقل "معرف وعاء العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="d42f1-123">تتيح لك معرفات أوعية العمل تنظيم العمل في مجموعات.</span><span class="sxs-lookup"><span data-stu-id="d42f1-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="d42f1-124">ستكون القيمة التي تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d42f1-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="d42f1-125">في الحقل "أولوية العمل"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="d42f1-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="d42f1-126">ويشير هذا إلى أهمية العمل، وستكون القيمة التي تقوم تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d42f1-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="d42f1-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d42f1-127">Click Save.</span></span>
    * <span data-ttu-id="d42f1-128">يجب حفظ رأس قالب قبل أن تتوفر أزرار "تحرير استعلام".</span><span class="sxs-lookup"><span data-stu-id="d42f1-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="d42f1-129">إعداد الاستعلام الخاص بقالب العمل</span><span class="sxs-lookup"><span data-stu-id="d42f1-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="d42f1-130">انقر فوق "تحرير استعلام".</span><span class="sxs-lookup"><span data-stu-id="d42f1-130">Click Edit query.</span></span>
    * <span data-ttu-id="d42f1-131">سنقوم بتعيين قيد بحيث لا يمكن استخدام القالب إلا في مستودع معين.</span><span class="sxs-lookup"><span data-stu-id="d42f1-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="d42f1-132">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-132">Click Add.</span></span>
3. <span data-ttu-id="d42f1-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d42f1-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d42f1-134">في الحقل "الحقل" اكتب "مستودع".</span><span class="sxs-lookup"><span data-stu-id="d42f1-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="d42f1-135">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="d42f1-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d42f1-136">Click OK.</span></span>
7. <span data-ttu-id="d42f1-137">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="d42f1-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="d42f1-138">تعيين تفاصيل قالب العمل</span><span class="sxs-lookup"><span data-stu-id="d42f1-138">Set work template details</span></span>
1. <span data-ttu-id="d42f1-139">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d42f1-139">Click New.</span></span>
2. <span data-ttu-id="d42f1-140">في الحقل "نوع العمل"، حدد "انتقاء".</span><span class="sxs-lookup"><span data-stu-id="d42f1-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="d42f1-141">في الحقل "معرف فئة العمل"، اكتب "شراء".</span><span class="sxs-lookup"><span data-stu-id="d42f1-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="d42f1-142">ستكون فئة العمل التي تعينها هنا هي الفئة الافتراضية بجميع بنود العمل من النوع "الانتقاء" التي يتم إنشاؤها باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d42f1-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="d42f1-143">لا يمكن إلغاء فئة العمل من بنود أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d42f1-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="d42f1-144">تُستخدم فئات العمل لتوجيه و/أو الحد من نوع بنود أوامر العمل التي يستطيع عامل مستودع معالجتها باستخدام جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="d42f1-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="d42f1-145">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d42f1-145">Click New.</span></span>
5. <span data-ttu-id="d42f1-146">في الحقل "نوع العمل"، حدد "تم وضعه".</span><span class="sxs-lookup"><span data-stu-id="d42f1-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="d42f1-147">في الحقل "معرف فئة العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="d42f1-148">تكون إرشادات الانتقاء والوضع مجموعة.</span><span class="sxs-lookup"><span data-stu-id="d42f1-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="d42f1-149">يجب أن تتضمن كل مجموعة انتقاء/وضع نفس فئة العمل.</span><span class="sxs-lookup"><span data-stu-id="d42f1-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="d42f1-150">استخدم نفس فئة العمل التي قمت بتوفيرها لإرشادات الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="d42f1-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="d42f1-151">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d42f1-151">Click Save.</span></span>
    * <span data-ttu-id="d42f1-152">لاحظ أنه تم الآن تحديد خانة اختيار "صالح".</span><span class="sxs-lookup"><span data-stu-id="d42f1-152">Note that the Valid checkbox is now checked.</span></span>  

