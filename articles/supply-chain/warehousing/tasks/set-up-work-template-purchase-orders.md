---
title: إعداد قالب عمل لأوامر الشراء
description: يصف هذا الموضوع كيفية إعداد قالب عمل بسيط لاستخدامه عند تخزين الأصناف المستلمة.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6628936a56619de255ca7dc7b332b5819918c310
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980576"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="6dcca-103">إعداد قالب عمل لأوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="6dcca-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6dcca-104">يصف هذا الموضوع كيفية إعداد قالب عمل بسيط لاستخدامه عند تخزين الأصناف المستلمة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="6dcca-105">تحدد قوالب العمل مجموعة الإرشادات المقدمة إلى عامل المستودع على جهاز محمول عند نقل الأصناف من منطقة الاستلام.</span><span class="sxs-lookup"><span data-stu-id="6dcca-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="6dcca-106">يمكنك استخدام هذا الإجراء مع البيانات المذكورة في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="6dcca-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="6dcca-107">قبل تشغيل هذا الدليل، قم بإنشاء معرف وعاء عمل.</span><span class="sxs-lookup"><span data-stu-id="6dcca-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="6dcca-108">في هذا المثال، يُستخدم معرف وعاء عمل يتم استدعاؤه في "الوارد".</span><span class="sxs-lookup"><span data-stu-id="6dcca-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="6dcca-109">هذا الإجراء مخصص لمدير المستودعات.</span><span class="sxs-lookup"><span data-stu-id="6dcca-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="6dcca-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > العمل > قوالب العمل** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates** .</span></span>
2. <span data-ttu-id="6dcca-111">في الحقل **نوع أمر العمل** ، حدد **أوامر الشراء** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-111">In the **Work order type** field, select **Purchase orders** .</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="6dcca-112">إنشاء رأس قالب عمل</span><span class="sxs-lookup"><span data-stu-id="6dcca-112">Create a work template header</span></span>
1. <span data-ttu-id="6dcca-113">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-113">Select **New** .</span></span>
2. <span data-ttu-id="6dcca-114">الرقم التسلسلي **الرقم التسلسلي** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6dcca-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="6dcca-115">هذا هو التسلسل الذي يتم من خلاله تقييم قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="6dcca-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="6dcca-116">يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="6dcca-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="6dcca-117">في الحقل **قالب العمل** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="6dcca-118">هذا هو المعرف الفريد لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="6dcca-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="6dcca-119">في الحقل **وصف قالب العمل** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="6dcca-120">لن يتم تحديد الخيار **صالح** حتى تُكمل جميع المعلومات التي يحتاجها القالب ثم تنقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save** .</span></span>  
    - <span data-ttu-id="6dcca-121">لا يمكن معالجة أمر عمل من النوع **أمر شراء** تلقائيًا، وبالتالي اترك الخيار **المعالجة تلقائيًا** معينًا على **لا** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No** .</span></span>  
5. <span data-ttu-id="6dcca-122">في الحقل **معرف وعاء العمل** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="6dcca-123">تتيح لك معرفات أوعية العمل تنظيم العمل في مجموعات.</span><span class="sxs-lookup"><span data-stu-id="6dcca-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="6dcca-124">ستكون القيمة التي تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="6dcca-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="6dcca-125">في الحقل **أولوية العمل** ، أدخل `1`.</span><span class="sxs-lookup"><span data-stu-id="6dcca-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="6dcca-126">ويشير هذا إلى أهمية العمل، وستكون القيمة التي تقوم تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="6dcca-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="6dcca-127">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-127">Select **Save** .</span></span> <span data-ttu-id="6dcca-128">يجب حفظ رأس القالب قبل يصبح الزر **تحرير الاستعلام** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="6dcca-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="6dcca-129">إعداد الاستعلام الخاص بقالب العمل</span><span class="sxs-lookup"><span data-stu-id="6dcca-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="6dcca-130">حدد **تحرير الاستعلام** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-130">Select **Edit query** .</span></span> <span data-ttu-id="6dcca-131">سنقوم بتعيين قيد بحيث لا يمكن استخدام القالب إلا في مستودع معين.</span><span class="sxs-lookup"><span data-stu-id="6dcca-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="6dcca-132">حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-132">Select **Add** .</span></span>
3. <span data-ttu-id="6dcca-133">في حقل **الحقل** على الصف الجديد، اكتب `warehouse`‬.</span><span class="sxs-lookup"><span data-stu-id="6dcca-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="6dcca-134">في الحقل **المعايير** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="6dcca-135">حدد **موافق** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-135">Select **OK** .</span></span>
6. <span data-ttu-id="6dcca-136">حدد **نعم** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-136">Select **Yes** .</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="6dcca-137">تعيين تفاصيل قالب العمل</span><span class="sxs-lookup"><span data-stu-id="6dcca-137">Set work template details</span></span>
1. <span data-ttu-id="6dcca-138">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-138">Select **New** .</span></span>
2. <span data-ttu-id="6dcca-139">في الحقل **نوع العمل** ، حدد **انتقاء** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-139">In the **Work type** field, select **Pick** .</span></span>
3. <span data-ttu-id="6dcca-140">في الحقل **معرف فئة العمل** ، اكتب `purchase`.</span><span class="sxs-lookup"><span data-stu-id="6dcca-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="6dcca-141">ستكون فئة العمل التي تعينها هنا هي الفئة الافتراضية بجميع بنود العمل من النوع "الانتقاء" التي يتم إنشاؤها باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="6dcca-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="6dcca-142">لا يمكن إلغاء فئة العمل من بنود أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="6dcca-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="6dcca-143">تُستخدم فئات العمل لتوجيه و/أو الحد من نوع بنود أوامر العمل التي يستطيع عامل مستودع معالجتها باستخدام جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="6dcca-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="6dcca-144">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-144">Select **New** .</span></span>
5. <span data-ttu-id="6dcca-145">في الحقل **نوع العمل** ، حدد **تم وضعه** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-145">In the **Work type** field, select **Put** .</span></span>
6. <span data-ttu-id="6dcca-146">في الحقل **معرف فئة العمل** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="6dcca-147">تكون إرشادات الانتقاء والوضع مجموعة.</span><span class="sxs-lookup"><span data-stu-id="6dcca-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="6dcca-148">يجب أن تتضمن كل مجموعة انتقاء/وضع نفس فئة العمل.</span><span class="sxs-lookup"><span data-stu-id="6dcca-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="6dcca-149">استخدم نفس فئة العمل التي قمت بتوفيرها لإرشادات الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="6dcca-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="6dcca-150">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="6dcca-150">Select **Save** .</span></span> <span data-ttu-id="6dcca-151">لاحظ أن خانة الاختيار **صالح** أصبحت محددة الآن.</span><span class="sxs-lookup"><span data-stu-id="6dcca-151">Note that the **Valid** checkbox is now checked.</span></span>  

