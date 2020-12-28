---
title: التحقق من صحة تدفق الإنتاج وإصداره
description: يوضح هذا الإجراء كيفية إنشاء تدفق إنتاج جديد وإصدار أول لـlean manufacturing.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c30947d01cfb85ea3dbf1aa3e4ea8e092efd18cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421467"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="f1e77-103">التحقق من صحة تدفق الإنتاج وإصداره</span><span class="sxs-lookup"><span data-stu-id="f1e77-103">Validate a production flow and version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1e77-104">يوضح هذا الإجراء كيفية إنشاء تدفق إنتاج جديد وإصدار أول لـlean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="f1e77-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="f1e77-105">المتطلبات الأساسية: يجب تحديد معلمات lean manufacturing ووحدات القياس للوقت الخاص بالفئة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="f1e77-106">وتحتاج إلى تحديد تدفق قيم ومجموعة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="f1e77-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="f1e77-107">ارجع إلى المستندات التقنية حول lean manufacturing للتعرف على مفاهيم تدفقات الإنتاج والأنشطة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="f1e77-108">يشير هذا الإجراء إلى الكيان القانوني USMF في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="f1e77-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="f1e77-109">ومع ذلك، مع افتراض أنه يتم تكوين الكيان القانوني لـlean manufacturing، يمكن استخدام كيانات قانونية أخرى.</span><span class="sxs-lookup"><span data-stu-id="f1e77-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="f1e77-110">إنشاء تدفق إنتاج</span><span class="sxs-lookup"><span data-stu-id="f1e77-110">Create a production flow</span></span>
1. <span data-ttu-id="f1e77-111">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f1e77-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f1e77-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f1e77-112">Click New.</span></span>
3. <span data-ttu-id="f1e77-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f1e77-114">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f1e77-115">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f1e77-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f1e77-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f1e77-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f1e77-117">تدفق القيم هو وحدة تشغيل تشمل جميع الأنشطة والتدفقات الخاصة بتدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="f1e77-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="f1e77-118">في هذه المرحلة، تتقيد وحدات التشغيل بكيان قانوني ولا يكون لها أية وظيفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="f1e77-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="f1e77-119">في الحقل "مجموعة الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f1e77-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f1e77-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f1e77-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f1e77-121">تسمح مجموعات الإنتاج بتعريف المواد والعمالة وحسابات الأعمال تحت التنفيذ لعملية إنتاج.</span><span class="sxs-lookup"><span data-stu-id="f1e77-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="f1e77-122">لربط سياق المحاسبة بتدفق إنتاج، يجب تحديد مجموعة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="f1e77-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="f1e77-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f1e77-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="f1e77-124">إنشاء إصدار تدفق إنتاج</span><span class="sxs-lookup"><span data-stu-id="f1e77-124">Create a production flow version</span></span>
1. <span data-ttu-id="f1e77-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-125">Click Add.</span></span>
2. <span data-ttu-id="f1e77-126">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f1e77-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="f1e77-127">يمكنك تحديث تاريخ انتهاء الصلاحية للإصدار في أي وقت، حتى بالنسبة للإصدارات النشطة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="f1e77-128">استخدم انتهاء صلاحية الإصدار للتخطيط للتخلص التدريجي من إصدار.</span><span class="sxs-lookup"><span data-stu-id="f1e77-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="f1e77-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f1e77-129">Click OK.</span></span>
4. <span data-ttu-id="f1e77-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f1e77-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="f1e77-131">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="f1e77-132">حدد وحدة المنتج.</span><span class="sxs-lookup"><span data-stu-id="f1e77-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="f1e77-133">في الحقل "متوسط الوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f1e77-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="f1e77-134">بالنسبة للتحكم في كمية الإنتاج حسب الوقت لإصدار تدفق الإنتاج، حدد متوسطًا مستهدفًا للوقت اللازم لإنتاج وحدة من المنتج.</span><span class="sxs-lookup"><span data-stu-id="f1e77-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="f1e77-135">تعرف كمية الإنتاج حسب الوقت بأنه كمية الإنتاج لكل فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="f1e77-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="f1e77-136">في المثال الموضح، يساوي الوقت اللازم لإنتاج وحدة من المنتج 0.2 ساعة لكل 10 قطع.</span><span class="sxs-lookup"><span data-stu-id="f1e77-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="f1e77-137">بالنسبة لفترة عمل قدرها 8 ساعات، يوافق هذا قدرة إنتاجية يومية قدرها 400 قطعة.</span><span class="sxs-lookup"><span data-stu-id="f1e77-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="f1e77-138">في الحقل "الكمية لكل دورة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f1e77-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="f1e77-139">قم بتوسيع القسم "تفاصيل الإصدار" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="f1e77-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="f1e77-140">في الحقل "الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f1e77-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="f1e77-141">يجب أن يكون الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج أقل من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.</span><span class="sxs-lookup"><span data-stu-id="f1e77-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="f1e77-142">في الحقل "الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا</span><span class="sxs-lookup"><span data-stu-id="f1e77-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="f1e77-143">يجب أن يكون الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج أكبر من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.</span><span class="sxs-lookup"><span data-stu-id="f1e77-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="f1e77-144">أدخل عددًا للأيام المضمنة في فترة زمن الدورة الفعلي.</span><span class="sxs-lookup"><span data-stu-id="f1e77-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="f1e77-145">تمثل فترة زمن الدورة الفعلي عدد الأيام التي يتم تجميع الوظائف بها منذ الدقيقة رجوعًا لحساب زمن الدورة الفعلي.</span><span class="sxs-lookup"><span data-stu-id="f1e77-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="f1e77-146">يمكن تغيير القيمة في أي وقت وتُستخدم لحساب أزمنة الدورة الفعلية فقط.</span><span class="sxs-lookup"><span data-stu-id="f1e77-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="f1e77-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f1e77-147">Click Save.</span></span>

