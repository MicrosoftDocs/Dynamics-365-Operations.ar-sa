---
title: إنشاء أنشطة تحويل لـ lean manufacturing
description: قم بإنشاء نشاط نقل لـ lean manufacturing.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2411dc51dc1b85499edb30d9a580f396277a5bd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828864"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="5a3b6-103">إنشاء أنشطة تحويل لـ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="5a3b6-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a3b6-104">قم بإنشاء نشاط نقل لـ lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="5a3b6-105">المتطلبات الأساسية:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-105">Prerequisites:</span></span> 

1. <span data-ttu-id="5a3b6-106">يجب إنشاء تدفق إنتاج وإصدار غير نشط.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="5a3b6-107">يجب إنشاء الموقعين والمستودعين المصدر والهدف.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="5a3b6-108">بشكل اختياري، يجب إنشاء خلية العمل المزوِّدة أو المزوَّدة.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="5a3b6-109">البحث عن إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="5a3b6-109">Find the production flow version</span></span>
1. <span data-ttu-id="5a3b6-110">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="5a3b6-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5a3b6-112">لاحظ أنه يجب أن يكون لتدفق الإنتاج إصدار في الحالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="5a3b6-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="5a3b6-114">إنشاء نشاط جديد</span><span class="sxs-lookup"><span data-stu-id="5a3b6-114">Create a new activity</span></span>
1. <span data-ttu-id="5a3b6-115">انقر فوق "الأنشطة".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-115">Click Activities.</span></span>
    * <span data-ttu-id="5a3b6-116">تأكد من وجود إصدار في صيغة مسودة لتدفق الإنتاج المحدد وحدد الإصدار.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="5a3b6-117">انقر فوق "إنشاء نشاط خطة جديد".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="5a3b6-118">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-118">Click Next.</span></span>
4. <span data-ttu-id="5a3b6-119">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5a3b6-120">في الحقل "نوع النشاط"، حدد "نقل".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="5a3b6-121">في الحقل "كمية العملية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="5a3b6-122">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="5a3b6-123">تحديد خلايا العمل</span><span class="sxs-lookup"><span data-stu-id="5a3b6-123">Select the Work cells</span></span>
1. <span data-ttu-id="5a3b6-124">في الحقل "التزويد"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5a3b6-125">لاستخدام لموقع إخراج خلية العمل كموقع مصدر في نشاط النقل، حدد خلية عمل.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="5a3b6-126">يمكن تنفيذ نفس الإجراء مع خلية العمل المزوَّدة، وهو ما يؤدي إلى تعيين الموقع الهدف لنشاط النقل.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="5a3b6-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="5a3b6-128">تحديد تحديثات المخزون</span><span class="sxs-lookup"><span data-stu-id="5a3b6-128">Define the inventory updates</span></span>
1. <span data-ttu-id="5a3b6-129">في الحقل "نوع المنتج‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="5a3b6-130">لاحظ أن عمليات النقل لا تغير نوع المنتج.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="5a3b6-131">يمكنك نقل المنتجات المنتهية أو المنتجات غير النهائية (نقل بين نشاطي تدفق إنتاج وربما تدفق كانبان).</span><span class="sxs-lookup"><span data-stu-id="5a3b6-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="5a3b6-132">عند نقل المنتجات المنتهية، يمكنك تحديد ما إذا كان الانتقاء أو الاستلام سيتسبب في حركة مخزون.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="5a3b6-133">تحديد مواقع النقل</span><span class="sxs-lookup"><span data-stu-id="5a3b6-133">Define the transfer locations</span></span>
1. <span data-ttu-id="5a3b6-134">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-134">Click Next.</span></span>
2. <span data-ttu-id="5a3b6-135">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5a3b6-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5a3b6-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5a3b6-138">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5a3b6-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5a3b6-140">في الحقل "شُحن بواسطة"، حدد "الشاحن".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="5a3b6-141">تتضمن الخيارات: الشاحن-مؤسسة تشغل المستودع الشحن، المستلم - مؤسسة تشغيل مستودع الاستلام، الناقل-مورد يمثل طرفًا آخر.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="5a3b6-142">إذا كان مؤسسة التشغيل موردًا، سيتطلب نشاط النقل اتفاقية تعاقد من الباطن.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="5a3b6-143">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="5a3b6-144">تحديد أوقات النشاط</span><span class="sxs-lookup"><span data-stu-id="5a3b6-144">Define the activity times</span></span>
1. <span data-ttu-id="5a3b6-145">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5a3b6-146">تعريف وقت التشغيل مطلوب.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="5a3b6-147">يُستخدم وقت التشغيل لحساب التكاليف وأوقات الإنتاجية لوظائف كانبان.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="5a3b6-148">ولا تُستخدم أوقات التشغيل لحساب القدرة الإنتاجية والاستهلاك، اللذان يُحسبان بزمن الدورة، المشتق من مهمة إصدار تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="5a3b6-149">في الحقل "الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="5a3b6-150">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="5a3b6-151">حدد وحدة "الوقت".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-151">Select the Time unit.</span></span>
5. <span data-ttu-id="5a3b6-152">في الحقل "حسب الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="5a3b6-153">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5a3b6-154">أوقات الانتظار اختيارية.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="5a3b6-155">في الحقل "الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="5a3b6-156">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="5a3b6-157">حدد وحدة "الوقت".</span><span class="sxs-lookup"><span data-stu-id="5a3b6-157">Select the Time unit.</span></span>
10. <span data-ttu-id="5a3b6-158">في الحقل "حسب الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="5a3b6-159">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-159">Click Next.</span></span>
12. <span data-ttu-id="5a3b6-160">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-160">Click Finish.</span></span>
13. <span data-ttu-id="5a3b6-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-161">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]