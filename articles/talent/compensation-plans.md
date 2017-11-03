---
title: "خطط التعويض"
description: "باستطاعة مدراء التعويضات والميزات‬ استخدام إدارة التعويضات لصيانة ومعالجة خطط التعويضات الثابتة والمتغيرة لموظفي المؤسسة."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a298ab26e343f50cb8dd80622a414695950a7
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="compensation-plans"></a><span data-ttu-id="4ce5f-103">خطط التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-103">Compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="4ce5f-104">باستطاعة مدراء التعويضات والميزات‬ استخدام إدارة التعويضات لصيانة ومعالجة خطط التعويضات الثابتة والمتغيرة لموظفي المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="4ce5f-105">مقدمة</span><span class="sxs-lookup"><span data-stu-id="4ce5f-105">Introduction</span></span>

<span data-ttu-id="4ce5f-106">‏‫يتم استخدام إدارة التعويض للتحكم في تسليم الراتب الأساسي والمنح.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="4ce5f-107">ويتم التحكم في دفع الأساس الثابت وزيادات الأهلية للموظف من خلال خطط التعويض الثابت.‬</span><span class="sxs-lookup"><span data-stu-id="4ce5f-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="4ce5f-108">ويتم التحكم في دفعة دفع الحوافز، مثل دفعات العلاوات، ومكافآت الأداء، وخيارات الأسهم، والمنح، وأيضًا المنح لمرة واحدة، من خلال خطط التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="4ce5f-109">يمكن إدراج الموظفين في خطة واحدة أو أكثر لكلا النوعين.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="4ce5f-110">ويلبي الموظف المتطلبات التالية ليكون مؤهلاً للإدراج في خطة تعويض:</span><span class="sxs-lookup"><span data-stu-id="4ce5f-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="4ce5f-111">يجب أن يكون لدى الموظف تعيين منصب نشط.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="4ce5f-112">يجب على الموظف تلبية المعايير التي تحددها قواعد الأهلية لخطة تعويض.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="4ce5f-113"> إعداد التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-113">Compensation setup</span></span>
<span data-ttu-id="4ce5f-114">يسرد الجدول التالي مكونات عملية التعويض التي يمكن أن تكون جزءًا لا يتجزأ في إعداد خطط التعويض الخاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4ce5f-115">المكون</span><span class="sxs-lookup"><span data-stu-id="4ce5f-115">Component</span></span></th>
<th><span data-ttu-id="4ce5f-116">مزيد من المعلومات...</span><span class="sxs-lookup"><span data-stu-id="4ce5f-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ce5f-117">إجراءات التعويض الثابتة</span><span class="sxs-lookup"><span data-stu-id="4ce5f-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="4ce5f-118">تنفذ إجراءات التعويض الثابت غرضين:</span><span class="sxs-lookup"><span data-stu-id="4ce5f-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="4ce5f-119">يمكن للإجراءات تحديد نوع المعلومات التي يجب تسجيلها عندما يتغير تعويض الموظف.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="4ce5f-120">على سبيل المثال، يمكنك أن تطلب تسجيل سبب التغيير، مثل ترقية أو تخفيض مرتبة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="4ce5f-121">‏يمكن للإجراءات ضمان استخدام عملية حسابية عند معالجة خطط التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="4ce5f-122">على سبيل المثال، ستقوم إجراءات نوع الأسهم بمقارنة دفع الموظفين بالنقطة المرجعية الدنيا لمستوى الموظف وضمان الدفع إلى الموظف بالحد الأدنى على الأقل.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee's and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-123">المستويات</span><span class="sxs-lookup"><span data-stu-id="4ce5f-123">Levels</span></span></td>
<td><span data-ttu-id="4ce5f-124">ترتبط المستويات بالوظائف وأي مناصب مرتبطة بمرجع وظيفة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="4ce5f-125">ويمكنك إنشاء مستويات منفصلة لأنواع خطط التعويض الثلاثة: الدرجة والنطاق والخطوة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-126">مصفوفة مقياس معدل استخدام النطاق</span><span class="sxs-lookup"><span data-stu-id="4ce5f-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="4ce5f-127">تساعدك مصفوفة استخدام النطاق في نقل الموظفين إلى نقطة التحكم لوظائفهم.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="4ce5f-128">كما يمكنك استخدام النطاق للتحكم في تساوي معدل الدفع داخل الشركة بغض النظر عن أداء الموظف أو الأداء العام للشركة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee's performance or the overall performance of the company.</span></span> <span data-ttu-id="4ce5f-129">على سبيل المثال، يحصل الموظفون الذين ينالون أجورًا منخفضة في النطاق الخاص بهم على زيادات ذات نسبة مئوية أعلى من الموظفين الذين ينالون أجورًا أعلى في النطاق.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="4ce5f-130">وبهذه الطريقة، يمكن تعويض فوارق الأسهم المقابلة بصورة منتظمة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="4ce5f-131">ويتم حساب استخدام النطاق كالتالي: (سعر الدفع الثابت - الحد الأدنى للنطاق) ÷ (الحد الأقصى للنطاق - الحد الأدنى للنطاق).</span><span class="sxs-lookup"><span data-stu-id="4ce5f-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-132">إعدادات النقطة المرجعية</span><span class="sxs-lookup"><span data-stu-id="4ce5f-132">Reference point setups</span></span></td>
<td><span data-ttu-id="4ce5f-133">يشمل إعداد النقاط المرجعية مجموعة نقاط مرجعية تمثل نطاقات في مصفوفة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="4ce5f-134">ويمكن ربط كل نطاق بمعدل دفع.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="4ce5f-135">على سبيل المثال، غالبصا ما ستشمل خطط التصنيف نقاط مرجعية للحد الأدنى ونقطة الوسط والحد الأقصى.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-136">مصفوفة التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="4ce5f-137">مصفوفة التعويض هو مجموعة من النقاط المرجعية والمستويات التي تستخدمها لإنشاء بنية تعويض.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-138">بنية التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-138">Compensation structure</span></span></td>
<td><span data-ttu-id="4ce5f-139">بنية التعويض هي مصفوفة تعويض تشمل معدلات الدفع المقترنة بالنقاط المرجعية لكل مستوى.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-140">قواعد الأهلية</span><span class="sxs-lookup"><span data-stu-id="4ce5f-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="4ce5f-141">يتم استخدام قواعد الأهلية لتحديد الموظفين في وظائف محددة، أو مهام الوظيفة، أو أنواع الوظائف، أو الإدارات، أو اتحادات العمال، أو مناطق التعويض التي تشملها خطط التعويض المحددة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="4ce5f-142">ويجب عليك إنشاء قواعد الأهلية لكلٍّ من خطط التعويض الثابتة والمتغيرة لتسجيل الموظفين في الخطة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="4ce5f-143">وبعد تحديد قواعد الأهلية لخطة التعويض، يمكنك تحديد مجموعة المستويات من الخطة التي يجب أن تسري على الوظائف التي تغطيها الخطة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-144">تكرارات الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce5f-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="4ce5f-145">‏‫يتم استخدام تكرارات الدفع لتحديد الفترة الزمنية التي يتم تحديد التعويض لها.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="4ce5f-146">على سبيل المثال، يساعد تكرار الدفع على فهم ما إذا تم تحديد مبلغ التعويض كمرتب سنوي مقابل سعر الأجر بالساعة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="4ce5f-147">كما يتم استخدام تكرارات الدفع لإعداد عوامل التحويل لتحويل مبالغ التعويض من شهرية وأسبوعية وكل أسبوعين وتكرارات الدفع بالساعة إلى تكرار دفع سنوي.‬</span><span class="sxs-lookup"><span data-stu-id="4ce5f-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-148">مناطق التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-148">Compensation regions</span></span></td>
<td><span data-ttu-id="4ce5f-149">يتم استخدام مناطق التعويض لتحديد تعويض الموظف استنادًا إلى موقع مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-150">نقطة التحكم</span><span class="sxs-lookup"><span data-stu-id="4ce5f-150">Control point</span></span></td>
<td><span data-ttu-id="4ce5f-151">تحدد نقطة التحكم ما تعتبره الدفع المثالي لكافة الموظفين عند مستوى تعويض معين.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="4ce5f-152">وبالنسبة لبنيات خطة التصنيف، فإن نقاط التحكم عادةً ما تكون هي نقطة المنتصف للنطاقات.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="4ce5f-153">ونادرًا ما تستخدم بنيات النطاق نقاط التحكم.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-153">Band structures rarely use control points.</span></span> <span data-ttu-id="4ce5f-154">يمكنك تحديد نقطة التحكم لخطة تعويض ثابتة في نموذج خطط التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-155">مهام الوظيفة</span><span class="sxs-lookup"><span data-stu-id="4ce5f-155">Job functions</span></span></td>
<td><span data-ttu-id="4ce5f-156">يتم استخدام المهام الوظيفية لتصنيف وتصفية خطط التعويض لوظائف معيَّنة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-157">أنواع الوظائف</span><span class="sxs-lookup"><span data-stu-id="4ce5f-157">Job types</span></span></td>
<td><span data-ttu-id="4ce5f-158">يتم استخدام أنواع الوظائف لتصنيف وتصفية خطط التعويض لوظائف معيَّنة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-159">أنواع التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="4ce5f-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="4ce5f-160">يتم إعداد أنواع التعويض المتغيرة كمنحة على شكل أسهم أو مكافأة على شكل منحة نقدية في خطط تعويض متغيرة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-161">شبكات التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-161">Compensation grids</span></span></td>
<td><span data-ttu-id="4ce5f-162">‏‫تحتوي شبكات التعويض على بنية التعويض.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="4ce5f-163">ويمكن استخدام شبكات التعويض بواسطة خطة تعويض واحدة أو أكثر.‬</span><span class="sxs-lookup"><span data-stu-id="4ce5f-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ce5f-164">خطط الأداء</span><span class="sxs-lookup"><span data-stu-id="4ce5f-164">Performance plans</span></span></td>
<td><span data-ttu-id="4ce5f-165">يتم استخدام خطط الأداء لإقران الأداء بمصفوفة التوزيع، بحيث يمكنك استخدام الخطة في استراتيجية الدفع مقابل الأداء.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ce5f-166">تقييمات الأداء</span><span class="sxs-lookup"><span data-stu-id="4ce5f-166">Performance ratings</span></span></td>
<td><span data-ttu-id="4ce5f-167">يتم استخدام تقديرات الأداء في خطط الأداء للتحديد مبلغ منحة الأهلية ومنحة الأداء.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="4ce5f-168">أحداث العملية</span><span class="sxs-lookup"><span data-stu-id="4ce5f-168">Process events</span></span>
<span data-ttu-id="4ce5f-169">يقوم حدث عملية بحساب معلومات التعويض لفترة معينة لكافة الموظفين الذين تم تسجيلهم في خطة واحدة أو أكثر من خطط التعويض الثابتة أو المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="4ce5f-170">كما يمكن أيضًا تشغيل حدث عملية بشكل متكرر، على سبيل المثال، لاختبار أو تحديث نتائج التعويض التي تم حسابها.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="4ce5f-171">أحداث التعويض</span><span class="sxs-lookup"><span data-stu-id="4ce5f-171">Compensation events</span></span>
-------------------

<span data-ttu-id="4ce5f-172">‏‫في كل مرة يتم فيها تشغيل حدث عملية، يتم إنشاء حدث تعويض.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="4ce5f-173">وتحتوي أحداث التعويض على نتائج عملية التعويض لكل موظف يتم تضمينه في حدث العملية هذا.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="4ce5f-174">وعندما تكون العمليات الحسابية صحيحة، يمكنك تحميل حدث التعويض لتحديث سجلات التعويض للموظفين الذين يتأثرون بحدث العملية.‬</span><span class="sxs-lookup"><span data-stu-id="4ce5f-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="4ce5f-175"> التوصيات</span><span class="sxs-lookup"><span data-stu-id="4ce5f-175">Recommendations</span></span>
<span data-ttu-id="4ce5f-176">بعد تشغيل حدث عملية، يمكنك أن توصي بتعديلات لزيادة تأهيل أو مبلغ منحة الموظف، استناداً إلى المبادئ التوجيهية المحسوبة لحدث العملية.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="4ce5f-177">ولتقديم توصيات للموظفين، يجب عليك تمكين التوصيات عند إعداد خطط التعويض أو عند إعداد حدث العملية.</span><span class="sxs-lookup"><span data-stu-id="4ce5f-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




