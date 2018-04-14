---
title: "إنشاء ومعالجته توافق"
description: "استخدم هذا الإجراء لتنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: adecf9b2ea29abaee378f1c02c64551c3aeede6d
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="3fb76-103">إنشاء ومعالجته توافق</span><span class="sxs-lookup"><span data-stu-id="3fb76-103">Create and process a conformance</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3fb76-104">استخدم هذا الإجراء لتنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.</span><span class="sxs-lookup"><span data-stu-id="3fb76-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="3fb76-105">يمكنك تشغيل هذا التسجيل في شركة العرض التوضيحي USMF ويمكنك استخدام القيم المقترحة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="3fb76-106">عادة ما يتم تنفيذ هذا الإجراء بواسطة كاتب جودة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="3fb76-107">كشرط مسبق، قم بتشغيل تسجيل المهمة "فحص جودة البضاعة".</span><span class="sxs-lookup"><span data-stu-id="3fb76-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="3fb76-108">لمعالجة اعتماد عدم المطابقة، يجب أن تكون للمستخدم الذي يقوم بتشغيل تسجيل المهمة قيمة "اسم" معينة بصفحة "المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="3fb76-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="3fb76-109">لاستخدام ملاحظات المستند، يجب أيضًا تنشيط "معالجة المستندات" للمستخدم في خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="3fb76-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="3fb76-110">تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="3fb76-110">Select a quality order</span></span>
1. <span data-ttu-id="3fb76-111">انتقل إلى أوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="3fb76-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3fb76-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3fb76-113">حدد أمر الجودة الذي تم إنشاؤه من تسجيل المهمة "فحص جودة البضائع".</span><span class="sxs-lookup"><span data-stu-id="3fb76-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="3fb76-114">إنشاء عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3fb76-114">Create a nonconformance</span></span>
1. <span data-ttu-id="3fb76-115">انقر فوق "استعلامات".</span><span class="sxs-lookup"><span data-stu-id="3fb76-115">Click Inquiries.</span></span>
2. <span data-ttu-id="3fb76-116">انقر فوق "حالات عدم المطابقة".</span><span class="sxs-lookup"><span data-stu-id="3fb76-116">Click Non conformances.</span></span>
3. <span data-ttu-id="3fb76-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3fb76-117">Click New.</span></span>
4. <span data-ttu-id="3fb76-118">في الحقل "نوع المشكلة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3fb76-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3fb76-119">حدد المشكلة التي تم اكتشافها خلال عملية الفحص.</span><span class="sxs-lookup"><span data-stu-id="3fb76-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="3fb76-120">في الحقل "نوع المشكلة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3fb76-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3fb76-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3fb76-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3fb76-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3fb76-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3fb76-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3fb76-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="3fb76-124">اعتماد/رفض عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3fb76-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="3fb76-125">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="3fb76-125">Click Functions.</span></span>
2. <span data-ttu-id="3fb76-126">انقر فوق "اعتماد عدم المطابقة".</span><span class="sxs-lookup"><span data-stu-id="3fb76-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="3fb76-127">على سبيل المثال، قم باعتماد عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="3fb76-128">يمكن ربط عدم المطابقة المعتمدة بالعمليات ذات الصلة لتسجيل عمل يتم تنفيذه كجزء من معالجة عدم المطابقة ومعالجة معالجة التصحيح، كما هو الحال في تسجيل المهمة هذا.</span><span class="sxs-lookup"><span data-stu-id="3fb76-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="3fb76-129">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="3fb76-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="3fb76-130">إنشاء إجراء تصحيح</span><span class="sxs-lookup"><span data-stu-id="3fb76-130">Create a correction action</span></span>
1. <span data-ttu-id="3fb76-131">انقر فوق "التصحيحات".</span><span class="sxs-lookup"><span data-stu-id="3fb76-131">Click Corrections.</span></span>
2. <span data-ttu-id="3fb76-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3fb76-132">Click New.</span></span>
3. <span data-ttu-id="3fb76-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3fb76-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3fb76-134">في الحقل "رقم الموظف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3fb76-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3fb76-135">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3fb76-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3fb76-136">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="3fb76-136">Click Select.</span></span>
7. <span data-ttu-id="3fb76-137">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="3fb76-137">Click Attach.</span></span>
    * <span data-ttu-id="3fb76-138">قم بإنشاء ملاحظة حول التصحيح.</span><span class="sxs-lookup"><span data-stu-id="3fb76-138">Create a note about the correction.</span></span> <span data-ttu-id="3fb76-139">على سبيل المثال، يتمثل الإجراء في الاتصال بالمورد لمناقشة حالة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="3fb76-140">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3fb76-140">Click New.</span></span>
9. <span data-ttu-id="3fb76-141">انقر فوق "ملاحظة".</span><span class="sxs-lookup"><span data-stu-id="3fb76-141">Click Note.</span></span>
    * <span data-ttu-id="3fb76-142">لاحظ أنه تبعاً لإعداد التقرير، يمكن طباعة أنواع مختلفة من المستندات على التقارير المتعلقة بإدارة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="3fb76-143">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3fb76-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="3fb76-145">الاحتفاظ بإجراء التصحيح</span><span class="sxs-lookup"><span data-stu-id="3fb76-145">Maintain a correction</span></span>
1. <span data-ttu-id="3fb76-146">انقر فوق "وضع علامة كمكتمل".</span><span class="sxs-lookup"><span data-stu-id="3fb76-146">Click Mark complete.</span></span>
2. <span data-ttu-id="3fb76-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3fb76-147">Click OK.</span></span>
3. <span data-ttu-id="3fb76-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="3fb76-149">إغلاق حالة عدم مطابقة</span><span class="sxs-lookup"><span data-stu-id="3fb76-149">Close a nonconformance</span></span>
1. <span data-ttu-id="3fb76-150">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="3fb76-150">Click Functions.</span></span>
2. <span data-ttu-id="3fb76-151">انقر فوق "إغلاق عدم المطابقة".</span><span class="sxs-lookup"><span data-stu-id="3fb76-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="3fb76-152">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="3fb76-152">Click Yes.</span></span>
4. <span data-ttu-id="3fb76-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-153">Close the page.</span></span>
5. <span data-ttu-id="3fb76-154">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3fb76-154">Close the page.</span></span>

