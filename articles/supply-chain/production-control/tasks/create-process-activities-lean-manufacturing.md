---
title: إنشاء أنشطة عملية لـ lean manufacturing
description: قم بإنشاء نشاط عملية لـ lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc93f3f696f470d7e2f174bd3342f0877e0b4e74
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212148"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="56259-103">إنشاء أنشطة عملية لـ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="56259-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56259-104">قم بإنشاء نشاط عملية لـ lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="56259-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="56259-105">المتطلبات الأساسية:</span><span class="sxs-lookup"><span data-stu-id="56259-105">Prerequisites:</span></span> 

1. <span data-ttu-id="56259-106">يجب إنشاء تدفق إنتاج وإصدار غير نشط.</span><span class="sxs-lookup"><span data-stu-id="56259-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="56259-107">يجب إنشاء خلية عمل.</span><span class="sxs-lookup"><span data-stu-id="56259-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="56259-108">البحث عن إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="56259-108">Find the production flow version</span></span>
1. <span data-ttu-id="56259-109">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="56259-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="56259-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="56259-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="56259-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="56259-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="56259-112">إنشاء نشاط جديد</span><span class="sxs-lookup"><span data-stu-id="56259-112">Create a new activity</span></span>
1. <span data-ttu-id="56259-113">انقر فوق "الأنشطة".</span><span class="sxs-lookup"><span data-stu-id="56259-113">Click Activities.</span></span>
    * <span data-ttu-id="56259-114">تأكد من وجود إصدار في صيغة مسودة لتدفق الإنتاج المحدد وحدد الإصدار.</span><span class="sxs-lookup"><span data-stu-id="56259-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="56259-115">انقر فوق "إنشاء نشاط خطة جديد".</span><span class="sxs-lookup"><span data-stu-id="56259-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="56259-116">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="56259-116">Click Next.</span></span>
4. <span data-ttu-id="56259-117">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="56259-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="56259-118">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="56259-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="56259-119">لاحظ أن الاسم يجب أن يكون فريدًا بالنسبة للتدفق إنتاج معين لجميع الإصدارات.</span><span class="sxs-lookup"><span data-stu-id="56259-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="56259-120">في الحقل "كمية العملية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="56259-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="56259-121">لاحظ أنه بصرف النظر عن كمية الوظائف التي ستتم معالجتها، هذا هو الحد الأدنى للكمية لكل وظيفة لحساب تكلفة العمالة.</span><span class="sxs-lookup"><span data-stu-id="56259-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="56259-122">إذا تفاوتت كميات الوظائف عن هذه الكمية، سيتم إنشاء فرق التكلفة للعمالة.</span><span class="sxs-lookup"><span data-stu-id="56259-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="56259-123">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="56259-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="56259-124">تحديد خلية العمل</span><span class="sxs-lookup"><span data-stu-id="56259-124">Select the work cell</span></span>
1. <span data-ttu-id="56259-125">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="56259-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="56259-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="56259-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="56259-127">تحديد تحديثات المخزون</span><span class="sxs-lookup"><span data-stu-id="56259-127">Define the inventory updates</span></span>
1. <span data-ttu-id="56259-128">حدد خانة اختيار "تحديث استلام المخزون الفعلي" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="56259-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="56259-129">إذا كان التحديث المخزون الفعلي = لا، يمكنك تحديد النشاط لتلقي منتج غير نهائي (لا يصل النشاط إلى مستوى قائمة مكونات الصنف التالية).</span><span class="sxs-lookup"><span data-stu-id="56259-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="56259-130">كما يمكنك أيضًا تحديد استهلاك المنتجات غير النهائية.</span><span class="sxs-lookup"><span data-stu-id="56259-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="56259-131">تحديد أنشطة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="56259-131">Define the picking activities</span></span>
1. <span data-ttu-id="56259-132">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="56259-132">Click Next.</span></span>
2. <span data-ttu-id="56259-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="56259-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="56259-134">يتم إنشاء نشاط انتقاء افتراضي لموقع الإدخال لخلية العمل المحددة.</span><span class="sxs-lookup"><span data-stu-id="56259-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="56259-135">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="56259-135">Click Add.</span></span>
    * <span data-ttu-id="56259-136">ويمكنك إنشاء أنشطة انتقاء إضافية لمنتجات معينة، منتجات لا يتم تقسيمها مرحليًا في نشاط إدخال خلية العمل.</span><span class="sxs-lookup"><span data-stu-id="56259-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="56259-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="56259-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="56259-138">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="56259-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="56259-139">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="56259-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="56259-140">باستخدام هذا التعريف، يتم انتقاء جميع المواد المستهلكة في النشاط من مستودع الإدخال والموقع الافتراضي باستثناء الصنف الذي يتم تعريفه في نشاط الانتقاء الثاني.</span><span class="sxs-lookup"><span data-stu-id="56259-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="56259-141">سيتم انتقاء هذا الصنف من مستودع وموقع مختلفين.</span><span class="sxs-lookup"><span data-stu-id="56259-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="56259-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="56259-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="56259-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="56259-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="56259-144">حدد خانة اختيار "تسجيل الخردة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="56259-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="56259-145">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="56259-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="56259-146">تحديد أوقات النشاط</span><span class="sxs-lookup"><span data-stu-id="56259-146">Define the activity times</span></span>
1. <span data-ttu-id="56259-147">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="56259-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="56259-148">تعريف وقت التشغيل مطلوب.</span><span class="sxs-lookup"><span data-stu-id="56259-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="56259-149">يتم استخدام وقت التشغيل لحساب التكاليف وأوقات الإنتاجية لوظائف كانبان.</span><span class="sxs-lookup"><span data-stu-id="56259-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="56259-150">ولا تُستخدم أوقات التشغيل لحساب القدرة الإنتاجية والاستهلاك، حيث تحسب هذه بزمن الدورة، المشتق من مهمة إصدار تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="56259-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="56259-151">في الحقل "الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="56259-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="56259-152">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="56259-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="56259-153">حدد وحدة "الوقت".</span><span class="sxs-lookup"><span data-stu-id="56259-153">Select the Time unit.</span></span>
5. <span data-ttu-id="56259-154">في الحقل "حسب الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="56259-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="56259-155">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="56259-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="56259-156">أوقات الانتظار اختيارية.</span><span class="sxs-lookup"><span data-stu-id="56259-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="56259-157">في الحقل "الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="56259-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="56259-158">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="56259-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="56259-159">حدد وحدة "الوقت".</span><span class="sxs-lookup"><span data-stu-id="56259-159">Select the Time unit.</span></span>
10. <span data-ttu-id="56259-160">في الحقل "حسب الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="56259-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="56259-161">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="56259-161">Click Next.</span></span>
12. <span data-ttu-id="56259-162">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="56259-162">Click Finish.</span></span>
13. <span data-ttu-id="56259-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="56259-163">Close the page.</span></span>

