---
title: إنشاء مورد عمليات
description: ينفذ مورد العمليات أنشطة مشروع أو عملية إنتاج.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e59b1e6a83d902df98a0b40ee6c572a6567f05
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212171"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="69a70-103">إنشاء مورد عمليات</span><span class="sxs-lookup"><span data-stu-id="69a70-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69a70-104">ينفذ مورد العمليات أنشطة مشروع أو عملية إنتاج.</span><span class="sxs-lookup"><span data-stu-id="69a70-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="69a70-105">تُظهر هذه الإجراءات كيفية تعريف مورد عمليات.</span><span class="sxs-lookup"><span data-stu-id="69a70-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="69a70-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="69a70-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="69a70-107">انتقل إلى "الموارد".</span><span class="sxs-lookup"><span data-stu-id="69a70-107">Go to Resources.</span></span>
2. <span data-ttu-id="69a70-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="69a70-108">Click New.</span></span>
3. <span data-ttu-id="69a70-109">في الحقل "المورد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="69a70-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="69a70-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="69a70-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="69a70-111">تعريف محددات القدرة والاستهلاك</span><span class="sxs-lookup"><span data-stu-id="69a70-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="69a70-112">وسّع مقطع "العملية".</span><span class="sxs-lookup"><span data-stu-id="69a70-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="69a70-113">في حقل النسبة المئوية للخردة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="69a70-114">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="69a70-115">حدد فئة التكلفة التي تحدد كيفية حساب تكلفة الإعداد.</span><span class="sxs-lookup"><span data-stu-id="69a70-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="69a70-116">في حقل "وقت التشغيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="69a70-117">حدد فئة التكلفة التي تحدد كيفية حساب تكلفة وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="69a70-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="69a70-118">في حقل "فئة الكمية‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="69a70-119">حدد فئة التكلفة التي تحدد كيفية حساب تكلفة الموارد استنادًا إلى كمية المخرجات.</span><span class="sxs-lookup"><span data-stu-id="69a70-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="69a70-120">في الحقل "وحدة القدرة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="69a70-121">حدد الوحدة حيث يمكن التعبير عن قدرة موارد العمليات.</span><span class="sxs-lookup"><span data-stu-id="69a70-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="69a70-122">في حقل "القدرة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="69a70-123">في حقل "النسبة المئوية للفعالية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="69a70-124">حدد الكفاءة التي تتوقعها من مورد العمليات.</span><span class="sxs-lookup"><span data-stu-id="69a70-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="69a70-125">تضبط النسبة المئوية للكفاءة إنتاجية‬ مورد العمليات وتؤثر على الوقت المحجوز للمورد.</span><span class="sxs-lookup"><span data-stu-id="69a70-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="69a70-126">في حقل النسبة المئوية لجدولة العمليات، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="69a70-127">حدد الحد الأقصى للنسبة المئوية لقدرة مورد العمليات الذي تريد استخدامه في جدولة العمليات.</span><span class="sxs-lookup"><span data-stu-id="69a70-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="69a70-128">حدد "نعم" في الحقل "قدرة محدودة‬".</span><span class="sxs-lookup"><span data-stu-id="69a70-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="69a70-129">عيّن هذا الخيار إلى "نعم" إذا كان يجب جدولة مورد العمليات استنادًا إلى القدرة الفعلية المتوفرة، وإذا كان يجب أخذ حجوزات القدرة الإنتاجية الموجودة في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="69a70-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="69a70-130">إذا تم تعيين هذا الخيار إلى "لا"، سيتم افتراض أن مورد العمليات ذا قدرة غير محدودة‬‏‫، وقد تكون الموارد تجاوزت الحجز‬.</span><span class="sxs-lookup"><span data-stu-id="69a70-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="69a70-131">حدد "نعم" في حقل "مورد التعامل مع الأزمات‬".</span><span class="sxs-lookup"><span data-stu-id="69a70-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="69a70-132">تحديد أوقات العمل</span><span class="sxs-lookup"><span data-stu-id="69a70-132">Define working times</span></span>
1. <span data-ttu-id="69a70-133">وسّع مقطع "التقويمات".</span><span class="sxs-lookup"><span data-stu-id="69a70-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="69a70-134">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="69a70-134">Click Add.</span></span>
3. <span data-ttu-id="69a70-135">في حقل "التقويم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="69a70-136">حدد تقويم وقت العمل الذي يعرّف قدرة المورد (بالساعات).</span><span class="sxs-lookup"><span data-stu-id="69a70-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="69a70-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="69a70-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="69a70-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="69a70-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="69a70-139">تحديد قدرات الموارد</span><span class="sxs-lookup"><span data-stu-id="69a70-139">Define resource capabilities</span></span>
1. <span data-ttu-id="69a70-140">وسّع المقطع "القدرات‬".</span><span class="sxs-lookup"><span data-stu-id="69a70-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="69a70-141">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="69a70-141">Click Add.</span></span>
    * <span data-ttu-id="69a70-142">القدرة هي إمكانية قيام مورد عمليات بتنفيذ نشاط معين.</span><span class="sxs-lookup"><span data-stu-id="69a70-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="69a70-143">يخصص محرك الجدولة الموارد عن طريق مطابقة متطلبات الموارد‬ لكل نشاط مع قدرات موارد العمليات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="69a70-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="69a70-144">في الحقل "القدرة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="69a70-145">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="69a70-146">حدد مستوى الكفاءة الذي يقوم المورد من خلاله بمعالجة القدرة.</span><span class="sxs-lookup"><span data-stu-id="69a70-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="69a70-147">في حقل "الأولوية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="69a70-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="69a70-148">حدد أولوية مورد العمليات فيما يتعلق بالقدرة.</span><span class="sxs-lookup"><span data-stu-id="69a70-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="69a70-149">عند الجدولة حسب الأولوية، يتم أولاً تحديد مورد العمليات ذي أعلى أولوية (أقل قيمة رقمية) أولاً.</span><span class="sxs-lookup"><span data-stu-id="69a70-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="69a70-150">تعيين مورد إلى مجموعة موارد</span><span class="sxs-lookup"><span data-stu-id="69a70-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="69a70-151">وسّع المقطع "مجموعات الموارد".</span><span class="sxs-lookup"><span data-stu-id="69a70-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="69a70-152">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="69a70-152">Click Add.</span></span>
    * <span data-ttu-id="69a70-153">تعرّف مجموعة الموارد سياق الموقع ووحدة الإنتاج والمستودع لموارد العمليات.</span><span class="sxs-lookup"><span data-stu-id="69a70-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="69a70-154">يمكن جدولة مورد العمليات فقط عند تعيينه إلى مجموعة موارد، وفقط في الموقع الذي توجد فيه مجموعة الموارد.</span><span class="sxs-lookup"><span data-stu-id="69a70-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="69a70-155">في حقل "مجموعة الموارد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="69a70-156">في الحقل "موقع الإدخالات‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="69a70-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="69a70-157">حدد موقع المستودع من حيث يستهلك مورد العمليات المواد.</span><span class="sxs-lookup"><span data-stu-id="69a70-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

