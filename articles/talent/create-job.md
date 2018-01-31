---
title: "إعداد مكونات وظيفة"
description: "يصف هذا الموضوع العناصر التصورية التي يمكن أن تشملها الوظيفة، ويوفر أمثلة على كيفية استخدام هذه العناصر في مؤسستك."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: b3fec97811c5096e81d7adb3d1a304b11a6fd788
ms.contentlocale: ar-sa
ms.lasthandoff: 01/31/2018

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="10498-103">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="10498-104">يصف هذا الموضوع العناصر التصورية التي يمكن أن تشملها الوظيفة، ويوفر أمثلة على كيفية استخدام هذه العناصر في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="10498-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="10498-105">قبل قيامك بإنشاء وظائف، يجب عليك إعداد بعض معلومات المرجع.</span><span class="sxs-lookup"><span data-stu-id="10498-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="10498-106">يمكنك إنشاء وظيفة لها اسم فقط.</span><span class="sxs-lookup"><span data-stu-id="10498-106">You can create a job that has only a name.</span></span> <span data-ttu-id="10498-107">ولكن، بإدراج معلومات إضافية، مثل عنوان الوظيفة، فأنت بذلك توفر قيم افتراضية للمناصب المعيّنة للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="10498-108">بالإضافة إلى ذلك، بعض المعلومات التي تقوم بإدخالها يمكن استخدام لتصفية خطط التعويض لوظائف معينة.</span><span class="sxs-lookup"><span data-stu-id="10498-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="10498-109">إذا كنت تريد إعداد الأهلية التي يمكنك استخدامها لتصفية خطط التعويض لوظيفة معينة، يجب عليك إعداد مهام الوظائف وأنواع الوظائف قبل إعداد الوظائف.</span><span class="sxs-lookup"><span data-stu-id="10498-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="10498-110">مع توافر هذه القيم الافتراضية، فسوف توفر الوقت عندما تقوم بإضافة مناصب إلى الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="10498-111">تسري تفاصيل بعض الوظائف، مثل المسمى الوظيفي والنوع والوظيفة من تاريخه.</span><span class="sxs-lookup"><span data-stu-id="10498-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="10498-112">إذا قمت بإنشاء وظيفة اليوم ولكن لم تقم بإضافة هذه التفاصيل حتى وقت لاحق، ثم قمت بالنظر لبعض تفاصيل الوظيفة مثل تاريخ الإنشاء، فلن تظهر هذه التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="10498-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="10498-113">وبناءً عليه، يجب عليك إنشاء بعض من هذه المعلومات المرجعية قبل أن تطلبها.</span><span class="sxs-lookup"><span data-stu-id="10498-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="10498-114">وبهذه الطريقة، يمكنك إضافة المعلومات إلى الوظائف الجديدة عند إنشائها.</span><span class="sxs-lookup"><span data-stu-id="10498-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="10498-115">المسميات الوظيفية</span><span class="sxs-lookup"><span data-stu-id="10498-115">Job titles</span></span>
<span data-ttu-id="10498-116">قبل إنشاء الوظائف، يجب عليك إعداد المسميات الخاصة بهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="10498-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="10498-117">ترث المناصب مسميات الوظائف من الوظائف التي تم إقران المناصب معها.</span><span class="sxs-lookup"><span data-stu-id="10498-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="10498-118">الاحتفاظ بالمسميات الوظيفية باستخدام صفحة **العناوين**، والتي يمكنك فتحها باستخدام وظيفة البحث.</span><span class="sxs-lookup"><span data-stu-id="10498-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="10498-119">في صفحة **العناوين **، قم بإدخال العناوين التي تخطط لاستخدامها لوظائفك.</span><span class="sxs-lookup"><span data-stu-id="10498-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="10498-120">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-120">Job types</span></span>
<span data-ttu-id="10498-121">استخدم أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="10498-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="10498-122">أنواع الوظائف ليست مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="10498-122">Job types aren't required.</span></span> <span data-ttu-id="10498-123">وبالرغم من هذا، إذا كنت تخطط لاستخدام أنواع الوظائف عندما تقوم بإعداد قواعد الأهلية لإدارة تعويض، فيجب عليك إعداد أنواع الوظائف قبل إعداد الوظائف.</span><span class="sxs-lookup"><span data-stu-id="10498-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="10498-124">بعض أمثلة أنواع الوظائف هي الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="10498-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="10498-125">يمكنك الاحتفاظ بأنواع الوظائف باستخدام صفحة **أنواع الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="10498-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="10498-126">في صفحة **أنواع الوظائف**، قم بإدخال الاسم ووصفًا مختصرًا لنوع الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="10498-127">في حقل **حالة الإعفاء**، حدد أحد الخيارات التالية للإشارة إلى حالة الإعفاء لهذه الوظائف في قانون معايير العمل العادل (FLSA) والتي لها نوع الوظيفة هذا.</span><span class="sxs-lookup"><span data-stu-id="10498-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="10498-128">**معفي** – هي الوظائف المُعفاة من العمل الإضافي بموجب قانون معايير العمل العادل.</span><span class="sxs-lookup"><span data-stu-id="10498-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="10498-129">**غير معفي** – هي الوظائف غير المُعفاة من العمل الإضافي بموجب قانون معايير العمل العادل.</span><span class="sxs-lookup"><span data-stu-id="10498-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="10498-130">**لا ينطبق** – لا تنطبق تغطية قانون معايير العمل العادل.</span><span class="sxs-lookup"><span data-stu-id="10498-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="10498-131">مهام الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-131">Job functions</span></span>
<span data-ttu-id="10498-132">تصف مهام الوظائف فئات وظيفية عالية المستوى وارتباطها بالمهام رفيعة المستوى.</span><span class="sxs-lookup"><span data-stu-id="10498-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="10498-133">مهام الوظائف ليست مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="10498-133">Job functions aren't required.</span></span> <span data-ttu-id="10498-134">يمكنك استخدام مهام الوظائف، إلى جانب أنواع الوظائف لتصفية خطط التعويض لوظائف محددة.</span><span class="sxs-lookup"><span data-stu-id="10498-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="10498-135">يمكنك إرفاق مهام الوظائف وأنواع الوظائف مع خطط التعويض من خلال إعداد قواعد الأهلية على صفحة **قواعد الأهلية**.</span><span class="sxs-lookup"><span data-stu-id="10498-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="10498-136">ثم يمكنك إرفاق مجموعة من المستويات لخطة التعويض التي تنطبق على مجموعة محددة من أنواع الوظائف ومهام الوظائف التي قمت بتحديدها من خلال أحد قواعد الأهلية.</span><span class="sxs-lookup"><span data-stu-id="10498-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="10498-137">(تطبق هذه الميزات على كل من خطط التعويض الثابتة وخطط التعويض المتغيرة.). ولكن، إذا كنت تخطط لاستخدام مهام الوظائف عندما تقوم بإعداد قواعد الأهلية لإدارة التعويض، فينبغي عليك إعداد مهام الوظائف قبل إعداد الوظائف.</span><span class="sxs-lookup"><span data-stu-id="10498-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="10498-138">يوضح الجدول التالي بعض أمثلة مهام الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="10498-139">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-139">Job</span></span>           | <span data-ttu-id="10498-140">مهمة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="10498-141">مدير المبيعات</span><span class="sxs-lookup"><span data-stu-id="10498-141">Sales manager</span></span> | <span data-ttu-id="10498-142">مدير المستوى المتوسط</span><span class="sxs-lookup"><span data-stu-id="10498-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="10498-143">المحاسب</span><span class="sxs-lookup"><span data-stu-id="10498-143">Accountant</span></span>    | <span data-ttu-id="10498-144">المهنيين</span><span class="sxs-lookup"><span data-stu-id="10498-144">Professionals</span></span>        |

<span data-ttu-id="10498-145">يمكنك الاحتفاظ بمهام الوظائف باستخدام صفحة **مهام الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="10498-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="10498-146">في صفحة **مهام الوظائف**، قم بإدخال كود الهوية ووصف موجز لمهمة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="10498-147">مهام الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-147">Job tasks</span></span>
<span data-ttu-id="10498-148">تصف مهام الوظائف المهام الأساسية التي يجب على عامل في أحد المناصب لهذه الوظيفة إتمامها.</span><span class="sxs-lookup"><span data-stu-id="10498-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="10498-149">كما يمكن إضافة نفس مهمة الوظيفة إلى وظائف متعددة، وإلى المناصب لهذه الوظائف التي تستخدم مهام الوظائف تلك.</span><span class="sxs-lookup"><span data-stu-id="10498-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="10498-150">يوضح الجدول التالي بعض أمثلة مهام الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10498-151">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-151">Job</span></span></th>
<th><span data-ttu-id="10498-152">مهمة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="10498-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10498-153">مدير المبيعات</span><span class="sxs-lookup"><span data-stu-id="10498-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="10498-154"><strong>مراجعة الأداء</strong> - مراجعة الأداء الوظيفي لكل مندوب مبيعات.</span><span class="sxs-lookup"><span data-stu-id="10498-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="10498-155"><strong>مراجعة الغياب</strong> - قبول أو رفض تسجيلات أو طلبات غياب كل مندوب مبيعات.</span><span class="sxs-lookup"><span data-stu-id="10498-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10498-156">المحاسب</span><span class="sxs-lookup"><span data-stu-id="10498-156">Accountant</span></span></td>
<td><span data-ttu-id="10498-157"><strong>التقرير المالي</strong> – تقديم التقارير المالية الأسبوعية للمدير المالي.</span><span class="sxs-lookup"><span data-stu-id="10498-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10498-158">يمكنك الاحتفاظ بأنواع الوظائف باستخدام صفحة **مهام الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="10498-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="10498-159">في صفحة **مهام الوظائف**، قم بإدخال الاسم ووصفًا مختصرًا لمهمة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="10498-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="10498-160">في حقل **ملاحظة**، يمكنك إدخال المعلومات الإضافية اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="10498-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="10498-161">يمكن تحديث الملاحظات لوظيفة محددة بدون تغيير الملاحظات التي قمت بإدخالها هنا.</span><span class="sxs-lookup"><span data-stu-id="10498-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="10498-162">نطاقات المسؤولية</span><span class="sxs-lookup"><span data-stu-id="10498-162">Areas of responsibility</span></span>
<span data-ttu-id="10498-163">استخدم نطاقات المسؤولية للإشارة إلى أدوار العمل، والعمليات، والمنتجات، والإجراءات التي يتحمل عامل في منصب لهذه الوظيفة المسؤولية عنها.</span><span class="sxs-lookup"><span data-stu-id="10498-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="10498-164">على سبيل المثال، للوظيفة التي تسمى "محاسب"، يمكن أن يكون أحد نطاقات المسؤولية هو "التقرير المالي للمنتج أ".</span><span class="sxs-lookup"><span data-stu-id="10498-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="10498-165">يمكن الحفاظ على نطاقات المسؤولية باستخدام صفحة **نطاقات المسؤولية**، والتي يمكنك العثور عليها باستخدام وظيفة البحث.</span><span class="sxs-lookup"><span data-stu-id="10498-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="10498-166">في صفحة **نطاقات المسؤولية**، قم بإدخال اسم ووصف للمسؤولية.</span><span class="sxs-lookup"><span data-stu-id="10498-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="10498-167">في حقل **ملاحظة**، يمكنك إدخال المعلومات الإضافية اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="10498-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="10498-168">يمكن تحديث الملاحظات لوظيفة محددة بدون تغيير الملاحظات التي قمت بإدخالها هنا.</span><span class="sxs-lookup"><span data-stu-id="10498-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>




