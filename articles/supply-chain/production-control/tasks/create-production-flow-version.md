---
title: إنشاء إصدار تدفق إنتاج
description: يركز هذا الإجراء على إنشاء إصدار تدفق إنتاج جديد.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5512c30be586c75d2571d60588a1179c0d47570b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146987"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="1fedf-103">إنشاء إصدار تدفق إنتاج</span><span class="sxs-lookup"><span data-stu-id="1fedf-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1fedf-104">يركز هذا الإجراء على إنشاء إصدار تدفق إنتاج جديد.</span><span class="sxs-lookup"><span data-stu-id="1fedf-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="1fedf-105">بالنسبة لهذا الإجراء، يجب تعريف معلمات lean manufacturing للإنتاج ووحدات القياس للوقت الخاص بالفئة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="1fedf-106">كما تحتاج أيضا إلى تعريف تدفق قيم ومجموعة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="1fedf-107">لمعرفة المزيد حول تدفقات الإنتاج والأنشطة المضمنة في lean manufacturing، راجع المستندات التقنية حول lean manufacturing لتطبيق Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="1fedf-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="1fedf-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="1fedf-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="1fedf-109">إنشاء تدفق إنتاج</span><span class="sxs-lookup"><span data-stu-id="1fedf-109">Create a production flow</span></span>
1. <span data-ttu-id="1fedf-110">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="1fedf-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1fedf-111">Click New.</span></span>
3. <span data-ttu-id="1fedf-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1fedf-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1fedf-114">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1fedf-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1fedf-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1fedf-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1fedf-116">حدد وحدة تشغيل من نوع تدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="1fedf-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="1fedf-117">تدفق القيم هي وحدة تشغيل تشمل جميع الأنشطة والتدفقات الخاصة بتدفق القيم.</span><span class="sxs-lookup"><span data-stu-id="1fedf-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="1fedf-118">في هذه المرحلة، تتقيد وحدات التشغيل بكيان قانوني ولا يكون لها أية وظيفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="1fedf-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="1fedf-119">في الحقل "مجموعة الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1fedf-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1fedf-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1fedf-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1fedf-121">حدد مجموعة إنتاج لتدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-121">Select a production group for the production flow.</span></span> <span data-ttu-id="1fedf-122">تسمح مجموعات الإنتاج بتعريف المواد والعمالة وحسابات الأعمال تحت التنفيذ لعملية إنتاج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="1fedf-123">لربط سياق المحاسبة بتدفق إنتاج، يجب تحديد مجموعة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="1fedf-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1fedf-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="1fedf-125">إنشاء إصدار تدفق إنتاج</span><span class="sxs-lookup"><span data-stu-id="1fedf-125">Create a production flow version</span></span>
1. <span data-ttu-id="1fedf-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-126">Click Add.</span></span>
2. <span data-ttu-id="1fedf-127">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="1fedf-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="1fedf-128">إذا لزم الأمر، حدد تاريخ انتهاء صلاحية للإصدار.</span><span class="sxs-lookup"><span data-stu-id="1fedf-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="1fedf-129">يمكنك تحديث التاريخ في أي وقت، حتى بالنسبة للإصدارات النشطة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="1fedf-130">ويمكنك استخدامه للتخطيط للتخلص التدريجي من إصدار ما.</span><span class="sxs-lookup"><span data-stu-id="1fedf-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="1fedf-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1fedf-131">Click OK.</span></span>
4. <span data-ttu-id="1fedf-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1fedf-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="1fedf-133">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="1fedf-134">عرّف وحدة المنتج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="1fedf-135">في الحقل "متوسط الوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1fedf-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="1fedf-136">حدد متوسط الوقت اللازم لإنتاج وحدة من المنتج فيما يخص الإصدار.</span><span class="sxs-lookup"><span data-stu-id="1fedf-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="1fedf-137">بالنسبة للتحكم في كمية الإنتاج حسب الوقت لإصدار تدفق الإنتاج، حدد متوسطًا مستهدفًا للوقت اللازم لإنتاج وحدة من المنتج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="1fedf-138">تعرف كمية الإنتاج حسب الوقت بأنه كمية الإنتاج لكل فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="1fedf-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="1fedf-139">في المثال، يساوي الوقت اللازم لإنتاج وحدة من المنتج 0.2 ساعة لكل 10 قطع.</span><span class="sxs-lookup"><span data-stu-id="1fedf-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="1fedf-140">بالنسبة لفترة عمل قدرها 8 ساعات، يوافق هذا قدرة إنتاجية يومية قدرها 400 قطعة.</span><span class="sxs-lookup"><span data-stu-id="1fedf-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="1fedf-141">في الحقل "الكمية لكل دورة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1fedf-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="1fedf-142">حدد الكمية لكل دورة المتعلقة بمتوسط الوقت اللازم لإنتاج وحدة من المنتج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="1fedf-143">قم بتبديل التوسيع للقسم "تفاصيل الإصدار".</span><span class="sxs-lookup"><span data-stu-id="1fedf-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="1fedf-144">في الحقل "الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1fedf-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="1fedf-145">حدد الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج.</span><span class="sxs-lookup"><span data-stu-id="1fedf-145">Define the minimum takt time.</span></span> <span data-ttu-id="1fedf-146">يجب أن يكون الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج أقل من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.</span><span class="sxs-lookup"><span data-stu-id="1fedf-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="1fedf-147">في الحقل "الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا</span><span class="sxs-lookup"><span data-stu-id="1fedf-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="1fedf-148">يجب أن يكون الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج أكبر من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.</span><span class="sxs-lookup"><span data-stu-id="1fedf-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="1fedf-149">في الحقل "فترة زمن الدورة الفعلي (الأيام)"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1fedf-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="1fedf-150">أدخل عدد الأيام المضمنة في فترة زمن الدورة الفعلي.</span><span class="sxs-lookup"><span data-stu-id="1fedf-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="1fedf-151">تمثل فترة زمن الدورة الفعلي عدد الأيام التي يتم تجميع الوظائف بها منذ الدقيقة رجوعًا لحساب زمن الدورة الفعلي.</span><span class="sxs-lookup"><span data-stu-id="1fedf-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="1fedf-152">يمكن تغيير القيمة في أي وقت وتُستخدم لحساب أزمنة الدورة الفعلية فقط.</span><span class="sxs-lookup"><span data-stu-id="1fedf-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="1fedf-153">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1fedf-153">Click Save.</span></span>

