--- 
title: "إنشاء أنشطة عملية لـ lean manufacturing"
description: "قم بإنشاء نشاط عملية لـ lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dbedbf6cd5d366d10726a9c10846c171a297a07f
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="fb480-103">إنشاء أنشطة عملية لـ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="fb480-103">Create process activities for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb480-104">قم بإنشاء نشاط عملية لـ lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="fb480-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="fb480-105">المتطلبات الأساسية:</span><span class="sxs-lookup"><span data-stu-id="fb480-105">Prerequisites:</span></span> 

1. <span data-ttu-id="fb480-106">يجب إنشاء تدفق إنتاج وإصدار غير نشط.</span><span class="sxs-lookup"><span data-stu-id="fb480-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="fb480-107">يجب إنشاء خلية عمل.</span><span class="sxs-lookup"><span data-stu-id="fb480-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="fb480-108">البحث عن إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="fb480-108">Find the production flow version</span></span>
1. <span data-ttu-id="fb480-109">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="fb480-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="fb480-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb480-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fb480-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb480-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="fb480-112">إنشاء نشاط جديد</span><span class="sxs-lookup"><span data-stu-id="fb480-112">Create a new activity</span></span>
1. <span data-ttu-id="fb480-113">انقر فوق "الأنشطة".</span><span class="sxs-lookup"><span data-stu-id="fb480-113">Click Activities.</span></span>
    * <span data-ttu-id="fb480-114">تأكد من وجود إصدار في صيغة مسودة لتدفق الإنتاج المحدد وحدد الإصدار.</span><span class="sxs-lookup"><span data-stu-id="fb480-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="fb480-115">انقر فوق "إنشاء نشاط خطة جديد".</span><span class="sxs-lookup"><span data-stu-id="fb480-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="fb480-116">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="fb480-116">Click Next.</span></span>
4. <span data-ttu-id="fb480-117">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb480-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fb480-118">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb480-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fb480-119">لاحظ أن الاسم يجب أن يكون فريدًا بالنسبة للتدفق إنتاج معين لجميع الإصدارات.</span><span class="sxs-lookup"><span data-stu-id="fb480-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="fb480-120">في الحقل "كمية العملية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fb480-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="fb480-121">لاحظ أنه بصرف النظر عن كمية الوظائف التي ستتم معالجتها، هذا هو الحد الأدنى للكمية لكل وظيفة لحساب تكلفة العمالة.</span><span class="sxs-lookup"><span data-stu-id="fb480-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="fb480-122">إذا تفاوتت كميات الوظائف عن هذه الكمية، سيتم إنشاء فرق التكلفة للعمالة.</span><span class="sxs-lookup"><span data-stu-id="fb480-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="fb480-123">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="fb480-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="fb480-124">تحديد خلية العمل</span><span class="sxs-lookup"><span data-stu-id="fb480-124">Select the work cell</span></span>
1. <span data-ttu-id="fb480-125">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fb480-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="fb480-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb480-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="fb480-127">تحديد تحديثات المخزون</span><span class="sxs-lookup"><span data-stu-id="fb480-127">Define the inventory updates</span></span>
1. <span data-ttu-id="fb480-128">حدد خانة اختيار "تحديث استلام المخزون الفعلي" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="fb480-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="fb480-129">إذا كان التحديث المخزون الفعلي = لا، يمكنك تحديد النشاط لتلقي منتج غير نهائي (لا يصل النشاط إلى مستوى قائمة مكونات الصنف التالية).</span><span class="sxs-lookup"><span data-stu-id="fb480-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="fb480-130">كما يمكنك أيضًا تحديد استهلاك المنتجات غير النهائية.</span><span class="sxs-lookup"><span data-stu-id="fb480-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="fb480-131">تحديد أنشطة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="fb480-131">Define the picking activities</span></span>
1. <span data-ttu-id="fb480-132">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="fb480-132">Click Next.</span></span>
2. <span data-ttu-id="fb480-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb480-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fb480-134">يتم إنشاء نشاط انتقاء افتراضي لموقع الإدخال لخلية العمل المحددة.</span><span class="sxs-lookup"><span data-stu-id="fb480-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="fb480-135">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="fb480-135">Click Add.</span></span>
    * <span data-ttu-id="fb480-136">ويمكنك إنشاء أنشطة انتقاء إضافية لمنتجات معينة، منتجات لا يتم تقسيمها مرحليًا في نشاط إدخال خلية العمل.</span><span class="sxs-lookup"><span data-stu-id="fb480-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="fb480-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb480-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fb480-138">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb480-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="fb480-139">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fb480-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fb480-140">باستخدام هذا التعريف، يتم انتقاء جميع المواد المستهلكة في النشاط من مستودع الإدخال والموقع الافتراضي باستثناء الصنف الذي يتم تعريفه في نشاط الانتقاء الثاني.</span><span class="sxs-lookup"><span data-stu-id="fb480-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="fb480-141">سيتم انتقاء هذا الصنف من مستودع وموقع مختلفين.</span><span class="sxs-lookup"><span data-stu-id="fb480-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="fb480-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb480-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fb480-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb480-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="fb480-144">حدد خانة اختيار "تسجيل الخردة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="fb480-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="fb480-145">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="fb480-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="fb480-146">تحديد أوقات النشاط</span><span class="sxs-lookup"><span data-stu-id="fb480-146">Define the activity times</span></span>
1. <span data-ttu-id="fb480-147">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb480-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fb480-148">تعريف وقت التشغيل مطلوب.</span><span class="sxs-lookup"><span data-stu-id="fb480-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="fb480-149">يتم استخدام وقت التشغيل لحساب التكاليف وأوقات الإنتاجية لوظائف كانبان.</span><span class="sxs-lookup"><span data-stu-id="fb480-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="fb480-150">ولا تُستخدم أوقات التشغيل لحساب القدرة الإنتاجية والاستهلاك، حيث تحسب هذه بزمن الدورة، المشتق من مهمة إصدار تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="fb480-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="fb480-151">في الحقل "الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fb480-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="fb480-152">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb480-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="fb480-153">حدد وحدة "الوقت".</span><span class="sxs-lookup"><span data-stu-id="fb480-153">Select the Time unit.</span></span>
5. <span data-ttu-id="fb480-154">في الحقل "حسب الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fb480-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="fb480-155">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb480-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fb480-156">أوقات الانتظار اختيارية.</span><span class="sxs-lookup"><span data-stu-id="fb480-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="fb480-157">في الحقل "الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fb480-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="fb480-158">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb480-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="fb480-159">حدد وحدة "الوقت".</span><span class="sxs-lookup"><span data-stu-id="fb480-159">Select the Time unit.</span></span>
10. <span data-ttu-id="fb480-160">في الحقل "حسب الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fb480-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="fb480-161">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="fb480-161">Click Next.</span></span>
12. <span data-ttu-id="fb480-162">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="fb480-162">Click Finish.</span></span>
13. <span data-ttu-id="fb480-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fb480-163">Close the page.</span></span>


