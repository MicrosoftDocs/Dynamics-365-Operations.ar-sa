---
title: متطلبات الإعداد الأساسية لإدارة عدم التوافق
description: استخدم هذا الإجراء لتمكين عمليات إدارة عدم المطابقة.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "337660"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="b4e51-103">متطلبات الإعداد الأساسية لإدارة عدم التوافق</span><span class="sxs-lookup"><span data-stu-id="b4e51-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4e51-104">استخدم هذا الإجراء لتمكين عمليات إدارة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="b4e51-105">يصف عدم المطابقة إجراءًا أو صنفًا به مشكلة في الجودة، حيث تتضمن المعلومات الوصفية مصدر المشكلة ونوعها.</span><span class="sxs-lookup"><span data-stu-id="b4e51-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="b4e51-106">ويستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="b4e51-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="b4e51-107">عادة ما يتم تنفيذ هذا الإجراء بواسطة مدير جودة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="b4e51-108">تمكين عمليات إدارة الجودة داخل الشركة</span><span class="sxs-lookup"><span data-stu-id="b4e51-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="b4e51-109">انتقل إلى إدارة المخزون > الإعداد > معلمات إدارة المستودعات والمخزون‬.</span><span class="sxs-lookup"><span data-stu-id="b4e51-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="b4e51-110">انقر فوق علامة التبويب "إدارة الجودة".</span><span class="sxs-lookup"><span data-stu-id="b4e51-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="b4e51-111">حدد "نعم" في حقل "إدارة الجودة".</span><span class="sxs-lookup"><span data-stu-id="b4e51-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="b4e51-112">حدد هذه المعلمة لتمكين عمليات إدارة الجودة للشركة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="b4e51-113">في حقل "المعدل في الساعة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b4e51-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="b4e51-114">استخدم حقل الأجر بالساعة لإدخال أجر عامل بالساعة بالعملة المحلية.</span><span class="sxs-lookup"><span data-stu-id="b4e51-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="b4e51-115">يتم استخدام الأجر بالساعة لحساب تكاليف العمليات المرتبطة بعدم التوافق.</span><span class="sxs-lookup"><span data-stu-id="b4e51-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="b4e51-116">يقدم حقلا المعدل في الساعة والتكاليف المحسوبة معلومات مرجعية حول عدم التوافق، كما أنهما لا يتفاعلان مع الوظائف الأخرى.</span><span class="sxs-lookup"><span data-stu-id="b4e51-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="b4e51-117">انقر فوق "‏‫إعداد التقرير‬".</span><span class="sxs-lookup"><span data-stu-id="b4e51-117">Click Report setup.</span></span>
    * <span data-ttu-id="b4e51-118">تسمح لك هذه الصفحة بتحديد أنواع ملاحظات تقرير الجودة الذي سيتم استخدامه على أنواع مختلفة من تقارير إدارة الجودة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="b4e51-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-119">Close the page.</span></span>
7. <span data-ttu-id="b4e51-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="b4e51-121">تمكين المستخدم لمعالجة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="b4e51-122">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="b4e51-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="b4e51-123">لمعالجة اعتماد عدم المطابقة، يجب أن يكون للمستخدم الذي يوافق على عدم المطابقات أو يرفضها قيمة "اسم" معينة بصفحة "المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="b4e51-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="b4e51-124">لاستخدام ملاحظات المستند، يجب أيضًا تنشيط "معالجة المستندات" للمستخدم في خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b4e51-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="b4e51-125">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="b4e51-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b4e51-126">على سبيل المثال، قم بإجراء التصفية بالحقل "الاسم" باستخدام القيمة "ريكاردو".</span><span class="sxs-lookup"><span data-stu-id="b4e51-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="b4e51-127">استخدم عامل التصفية للبحث عن المستخدم الذي سيوافق على سجلات عدم المطابقة أو رفضها.</span><span class="sxs-lookup"><span data-stu-id="b4e51-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="b4e51-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b4e51-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b4e51-129">لمعالجة اعتماد عدم المطابقة، تأكد من أن للمستخدم الذي يوافق على عدم المطابقات أو يرفضها قيمة "اسم" معينة بصفحة "المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="b4e51-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="b4e51-130">انقر فوق خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b4e51-130">Click User options.</span></span>
5. <span data-ttu-id="b4e51-131">انقر فوق علامة التبويب "التفضيلات".</span><span class="sxs-lookup"><span data-stu-id="b4e51-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="b4e51-132">حدد "نعم" في تمكين حقل معالجة المستند.</span><span class="sxs-lookup"><span data-stu-id="b4e51-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="b4e51-133">لاستخدام ملاحظات المستند، يجب أيضًا تنشيط "معالجة المستندات" للمستخدم في خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b4e51-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="b4e51-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-134">Close the page.</span></span>
8. <span data-ttu-id="b4e51-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-135">Close the page.</span></span>
9. <span data-ttu-id="b4e51-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="b4e51-137">تعريف أنواع التشخيصات لمعالجة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b4e51-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="b4e51-138">انتقل إلى إدارة المخزون > إعداد > إدارة الجودة > أنواع التشخيص‬.</span><span class="sxs-lookup"><span data-stu-id="b4e51-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="b4e51-139">واستخدم صفحة أنواع التشخيص لتحديد تصنيف إجراءات التشخيص.</span><span class="sxs-lookup"><span data-stu-id="b4e51-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="b4e51-140">يحدد التصحيح نوع إجراء التشخيص الذي ينبغي القيام به على عدم توافق معتمد وكذلك الشخص الذي ينبغي عليه القيام بالإجراء الإضافة إلى تاريخ الاكتمال المطلوب والمخطط.</span><span class="sxs-lookup"><span data-stu-id="b4e51-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="b4e51-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4e51-141">Click New.</span></span>
3. <span data-ttu-id="b4e51-142">في الحقل "تشخيص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="b4e51-143">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4e51-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="b4e51-145">تعريف تكاليف الجودة لمعالجة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b4e51-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="b4e51-146">انتقل إلى إدارة المخزون > إعداد > إدارة الجودة > تكاليف الجودة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="b4e51-147">استخدم صفحة تكاليف الجودة لتعريف تصنيف التكاليف التي سيتم استخدامها في العمليات المرتبطة بعدم المطابقات.</span><span class="sxs-lookup"><span data-stu-id="b4e51-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="b4e51-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4e51-148">Click New.</span></span>
3. <span data-ttu-id="b4e51-149">في الحقل "كود التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="b4e51-150">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4e51-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="b4e51-152">تعريف العمليات لمعالجة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b4e51-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="b4e51-153">انتقل إلى إدارة المخزون > إعداد > إدارة الجودة > العمليات.</span><span class="sxs-lookup"><span data-stu-id="b4e51-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="b4e51-154">استخدم صفحة العمليات لتحديد تصنيف العمل الذي قد يتم تطبيقه لحالة عدم مطابقة معتمدة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="b4e51-155">وعند ربط عملية بعدم مطابقة، فإنه يمكنك تعريف معلومات مفصلة حول المواد الضرورية وساعات العمل والمصاريف المتنوعة اللازمة لتنفيذ العملية.</span><span class="sxs-lookup"><span data-stu-id="b4e51-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="b4e51-156">توفر هذه المعلومات الأساس لحساب التكلفة التقديرية اللازمة للقيام بالعملية.</span><span class="sxs-lookup"><span data-stu-id="b4e51-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="b4e51-157">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4e51-157">Click New.</span></span>
3. <span data-ttu-id="b4e51-158">في الحقل "عملية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="b4e51-159">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4e51-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="b4e51-161">تعريف أنواع المشكلات لمعالجة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b4e51-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="b4e51-162">انتقل إلى إدارة المخزون > إعداد > إدارة الجودة > أنواع المشاكل‬.</span><span class="sxs-lookup"><span data-stu-id="b4e51-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="b4e51-163">استخدم صفحة أنواع المشكلات لتحديد تصنيف مشكلات الجودة التي تتم مواجهتها في مختلف أنواع حالات عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="b4e51-164">تتضمن أنواع عدم المطابقة الداخلية والعميل والمورد وطلب الخدمة والإنتاج وإنتاج المنتج المساعد.</span><span class="sxs-lookup"><span data-stu-id="b4e51-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="b4e51-165">يمكن ربط نوع مشكلة واحدة بالعديد من أنواع عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="b4e51-166">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4e51-166">Click New.</span></span>
3. <span data-ttu-id="b4e51-167">في الحقل "نوع المشكلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="b4e51-168">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4e51-169">انقر فوق "أنواع عدم المطابقة".</span><span class="sxs-lookup"><span data-stu-id="b4e51-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="b4e51-170">استخدم صفحة أنواع عدم المطابقة لتخويل استخدام نوع المشكلة في واحد أو أكثر من أنواع عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="b4e51-171">على سبيل المثال، يمكن تطبيق نوع مشكلة يتعلق بكود عيب معين على كافة أنواع عدم التوافق، في حين أنه لا يمكن تطبيق نوع مشكلة بشأن شكاوى العملاء إلا على أنواع عدم التوافق الخاصة بالعميل وطلب الخدمة فقط.</span><span class="sxs-lookup"><span data-stu-id="b4e51-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="b4e51-172">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4e51-172">Click New.</span></span>
7. <span data-ttu-id="b4e51-173">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b4e51-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b4e51-174">في الحقل "نوع عدم المطابقة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="b4e51-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="b4e51-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-175">Close the page.</span></span>
10. <span data-ttu-id="b4e51-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="b4e51-177">تعريف مناطق العزل لمعالجة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b4e51-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="b4e51-178">انتقل إلى إدارة المخزون > إعداد > إدارة الجودة > مناطق العزل.</span><span class="sxs-lookup"><span data-stu-id="b4e51-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="b4e51-179">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4e51-179">Click New.</span></span>
3. <span data-ttu-id="b4e51-180">في الحقل "منطقة العزل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="b4e51-181">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4e51-182">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4e51-182">Close the page.</span></span>

