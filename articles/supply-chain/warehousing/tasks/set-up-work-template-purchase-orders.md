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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9acf6db9138a009527c6662f1cbb7e5fedc8778
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976853"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="dad31-103">إعداد قالب عمل لأوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="dad31-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dad31-104">يصف هذا الموضوع كيفية إعداد قالب عمل بسيط لاستخدامه عند تخزين الأصناف المستلمة.</span><span class="sxs-lookup"><span data-stu-id="dad31-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="dad31-105">تحدد قوالب العمل مجموعة الإرشادات المقدمة إلى عامل المستودع على جهاز محمول عند نقل الأصناف من منطقة الاستلام.</span><span class="sxs-lookup"><span data-stu-id="dad31-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="dad31-106">يمكنك استخدام هذا الإجراء مع البيانات المذكورة في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="dad31-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="dad31-107">قبل تشغيل هذا الدليل، قم بإنشاء معرف وعاء عمل.</span><span class="sxs-lookup"><span data-stu-id="dad31-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="dad31-108">في هذا المثال، يُستخدم معرف وعاء عمل يتم استدعاؤه في "الوارد".</span><span class="sxs-lookup"><span data-stu-id="dad31-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="dad31-109">هذا الإجراء مخصص لمدير المستودعات.</span><span class="sxs-lookup"><span data-stu-id="dad31-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="dad31-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > العمل > قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="dad31-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="dad31-111">في الحقل **نوع أمر العمل**، حدد **أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="dad31-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="dad31-112">إنشاء رأس قالب عمل</span><span class="sxs-lookup"><span data-stu-id="dad31-112">Create a work template header</span></span>
1. <span data-ttu-id="dad31-113">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dad31-113">Select **New**.</span></span>
2. <span data-ttu-id="dad31-114">الرقم التسلسلي **الرقم التسلسلي**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="dad31-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="dad31-115">هذا هو التسلسل الذي يتم من خلاله تقييم قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="dad31-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="dad31-116">يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="dad31-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="dad31-117">في الحقل **قالب العمل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dad31-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="dad31-118">هذا هو المعرف الفريد لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="dad31-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="dad31-119">في الحقل **وصف قالب العمل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dad31-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="dad31-120">لن يتم تحديد الخيار **صالح** حتى تُكمل جميع المعلومات التي يحتاجها القالب ثم تنقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dad31-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="dad31-121">لا يمكن معالجة أمر عمل من النوع **أمر شراء** تلقائيًا، وبالتالي اترك الخيار **المعالجة تلقائيًا** معينًا على **لا**.</span><span class="sxs-lookup"><span data-stu-id="dad31-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="dad31-122">في الحقل **معرف وعاء العمل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dad31-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="dad31-123">تتيح لك معرفات أوعية العمل تنظيم العمل في مجموعات.</span><span class="sxs-lookup"><span data-stu-id="dad31-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="dad31-124">ستكون القيمة التي تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="dad31-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="dad31-125">في الحقل **أولوية العمل**، أدخل `1`.</span><span class="sxs-lookup"><span data-stu-id="dad31-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="dad31-126">ويشير هذا إلى أهمية العمل، وستكون القيمة التي تقوم تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="dad31-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="dad31-127">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dad31-127">Select **Save**.</span></span> <span data-ttu-id="dad31-128">يجب حفظ رأس القالب قبل يصبح الزر **تحرير الاستعلام** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="dad31-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="dad31-129">إعداد الاستعلام الخاص بقالب العمل</span><span class="sxs-lookup"><span data-stu-id="dad31-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="dad31-130">حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="dad31-130">Select **Edit query**.</span></span> <span data-ttu-id="dad31-131">سنقوم بتعيين قيد بحيث لا يمكن استخدام القالب إلا في مستودع معين.</span><span class="sxs-lookup"><span data-stu-id="dad31-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="dad31-132">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="dad31-132">Select **Add**.</span></span>
3. <span data-ttu-id="dad31-133">في حقل **الحقل** على الصف الجديد، اكتب `warehouse`‬.</span><span class="sxs-lookup"><span data-stu-id="dad31-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="dad31-134">في الحقل **المعايير**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dad31-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="dad31-135">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dad31-135">Select **OK**.</span></span>
6. <span data-ttu-id="dad31-136">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="dad31-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="dad31-137">تعيين تفاصيل قالب العمل</span><span class="sxs-lookup"><span data-stu-id="dad31-137">Set work template details</span></span>
1. <span data-ttu-id="dad31-138">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dad31-138">Select **New**.</span></span>
2. <span data-ttu-id="dad31-139">في الحقل **نوع العمل**، حدد **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="dad31-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="dad31-140">في الحقل **معرف فئة العمل**، اكتب `purchase`.</span><span class="sxs-lookup"><span data-stu-id="dad31-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="dad31-141">ستكون فئة العمل التي تعينها هنا هي الفئة الافتراضية بجميع بنود العمل من النوع "الانتقاء" التي يتم إنشاؤها باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="dad31-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="dad31-142">لا يمكن إلغاء فئة العمل من بنود أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dad31-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="dad31-143">تُستخدم فئات العمل لتوجيه و/أو الحد من نوع بنود أوامر العمل التي يستطيع عامل مستودع معالجتها باستخدام جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="dad31-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="dad31-144">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dad31-144">Select **New**.</span></span>
5. <span data-ttu-id="dad31-145">في الحقل **نوع العمل**، حدد **تم وضعه**.</span><span class="sxs-lookup"><span data-stu-id="dad31-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="dad31-146">في الحقل **معرف فئة العمل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dad31-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="dad31-147">تكون إرشادات الانتقاء والوضع مجموعة.</span><span class="sxs-lookup"><span data-stu-id="dad31-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="dad31-148">يجب أن تتضمن كل مجموعة انتقاء/وضع نفس فئة العمل.</span><span class="sxs-lookup"><span data-stu-id="dad31-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="dad31-149">استخدم نفس فئة العمل التي قمت بتوفيرها لإرشادات الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="dad31-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="dad31-150">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dad31-150">Select **Save**.</span></span> <span data-ttu-id="dad31-151">لاحظ أن خانة الاختيار **صالح** أصبحت محددة الآن.</span><span class="sxs-lookup"><span data-stu-id="dad31-151">Note that the **Valid** checkbox is now checked.</span></span>  

