---
title: كيانات Common Data Service .
description: تستخدم Microsoft Dynamics 365 Human Resources خدمة Common Data Service لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166488"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="69f4a-103">كيانات Common Data Service .</span><span class="sxs-lookup"><span data-stu-id="69f4a-103">Common Data Service entities</span></span>

<span data-ttu-id="69f4a-104">تستخدم Microsoft Dynamics 365 Human Resources خدمة Common Data Service لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.</span><span class="sxs-lookup"><span data-stu-id="69f4a-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="69f4a-105">لمزيدٍ من المعلومات حول Common Data Service، راجع [ما المقصود بـ Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="69f4a-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="69f4a-106">كيانات الموارد البشرية التالية متوفرة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69f4a-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="69f4a-107">كيانات الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-107">Benefit entities</span></span>

| <span data-ttu-id="69f4a-108">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-108">Name</span></span> | <span data-ttu-id="69f4a-109">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-110">تكرار حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="69f4a-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="69f4a-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="69f4a-112">حساب تكرار فترة دفع الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="69f4a-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="69f4a-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="69f4a-114">معدل حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="69f4a-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="69f4a-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="69f4a-116">تفاصيل معدل حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="69f4a-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="69f4a-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="69f4a-118">خيار الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-118">Benefit Option</span></span> | <span data-ttu-id="69f4a-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="69f4a-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="69f4a-120">خطة الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-120">Benefit Plan</span></span> | <span data-ttu-id="69f4a-121">cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص)</span><span class="sxs-lookup"><span data-stu-id="69f4a-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="69f4a-122">نوع الميزة</span><span class="sxs-lookup"><span data-stu-id="69f4a-122">Benefit Type</span></span> | <span data-ttu-id="69f4a-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="69f4a-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="69f4a-124">كيانات مهام العملية التجارية</span><span class="sxs-lookup"><span data-stu-id="69f4a-124">Business process tasks entities</span></span>

| <span data-ttu-id="69f4a-125">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-125">Name</span></span> | <span data-ttu-id="69f4a-126">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-127">تقويم عملية الأعمال</span><span class="sxs-lookup"><span data-stu-id="69f4a-127">Business Process Calendar</span></span> | <span data-ttu-id="69f4a-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="69f4a-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="69f4a-129">تعيين مجموعة عمليات الأعمال</span><span class="sxs-lookup"><span data-stu-id="69f4a-129">Business Process Group Assignment</span></span> | <span data-ttu-id="69f4a-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="69f4a-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="69f4a-131">مجموعة مهام مكتبة عمليات الأعمال</span><span class="sxs-lookup"><span data-stu-id="69f4a-131">Business Process Library Task Group</span></span> | <span data-ttu-id="69f4a-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="69f4a-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="69f4a-133">مرحلة عملية الأعمال‬</span><span class="sxs-lookup"><span data-stu-id="69f4a-133">Business Process Stage</span></span> | <span data-ttu-id="69f4a-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="69f4a-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="69f4a-135">رأس قالب قائمة الاختيار</span><span class="sxs-lookup"><span data-stu-id="69f4a-135">Checklist Template Header</span></span> | <span data-ttu-id="69f4a-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="69f4a-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="69f4a-137">مهمة قالب قائمة الاختيار</span><span class="sxs-lookup"><span data-stu-id="69f4a-137">Checklist Template Task</span></span> | <span data-ttu-id="69f4a-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="69f4a-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="69f4a-139">كيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-139">Compensation entities</span></span>

| <span data-ttu-id="69f4a-140">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-140">Name</span></span> | <span data-ttu-id="69f4a-141">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-142">الخطة الثابتة للتعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="69f4a-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="69f4a-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="69f4a-144">شبكة التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-144">Compensation Grid</span></span> | <span data-ttu-id="69f4a-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="69f4a-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="69f4a-146">مستوى التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-146">Compensation Level</span></span> | <span data-ttu-id="69f4a-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="69f4a-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="69f4a-148">تكرار دفع التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="69f4a-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="69f4a-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="69f4a-150">إعداد النقاط المرجعية للتعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="69f4a-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="69f4a-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="69f4a-152">إعداد بند النقاط المرجعية للتعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="69f4a-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="69f4a-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="69f4a-154">منطقة التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-154">Compensation Region</span></span> | <span data-ttu-id="69f4a-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="69f4a-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="69f4a-156">بنية التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-156">Compensation Structure</span></span> | <span data-ttu-id="69f4a-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="69f4a-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="69f4a-158">خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="69f4a-158">Compensation Variable Plan</span></span> | <span data-ttu-id="69f4a-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="69f4a-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="69f4a-160">مستوى خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="69f4a-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="69f4a-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="69f4a-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="69f4a-162">نوع خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="69f4a-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="69f4a-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="69f4a-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="69f4a-164">حدث التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="69f4a-164">Fixed Compensation Event</span></span> | <span data-ttu-id="69f4a-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="69f4a-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="69f4a-166">قاعدة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="69f4a-166">Vesting Rule</span></span> | <span data-ttu-id="69f4a-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="69f4a-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="69f4a-168">التعويض الثابت للعامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="69f4a-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="69f4a-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="69f4a-170">كيانات المؤسسة</span><span class="sxs-lookup"><span data-stu-id="69f4a-170">Organization entities</span></span>

| <span data-ttu-id="69f4a-171">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-171">Name</span></span> | <span data-ttu-id="69f4a-172">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-173">قسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-173">Department</span></span> | <span data-ttu-id="69f4a-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="69f4a-174">cdm_department</span></span> |
| <span data-ttu-id="69f4a-175">التوظيف</span><span class="sxs-lookup"><span data-stu-id="69f4a-175">Employment</span></span> | <span data-ttu-id="69f4a-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="69f4a-176">cdm_employment</span></span> |
| <span data-ttu-id="69f4a-177">الشركة</span><span class="sxs-lookup"><span data-stu-id="69f4a-177">Company</span></span> | <span data-ttu-id="69f4a-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="69f4a-178">cdm_company</span></span> |
| <span data-ttu-id="69f4a-179">وظيفة</span><span class="sxs-lookup"><span data-stu-id="69f4a-179">Job</span></span> | <span data-ttu-id="69f4a-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="69f4a-180">cdm_job</span></span> |
| <span data-ttu-id="69f4a-181">مهمة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="69f4a-181">Job Function</span></span> | <span data-ttu-id="69f4a-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="69f4a-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="69f4a-183">منصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="69f4a-183">Job Position</span></span> | <span data-ttu-id="69f4a-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="69f4a-184">cdm_jobposition</span></span> |
| <span data-ttu-id="69f4a-185">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="69f4a-185">Position Type</span></span> | <span data-ttu-id="69f4a-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="69f4a-186">cdm_positiontype</span></span> |
| <span data-ttu-id="69f4a-187">تعيين العامل بالمنصب</span><span class="sxs-lookup"><span data-stu-id="69f4a-187">Position Worker Assignment</span></span> | <span data-ttu-id="69f4a-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="69f4a-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="69f4a-189">بُعد منصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="69f4a-189">Job Position Dimension</span></span> | <span data-ttu-id="69f4a-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="69f4a-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="69f4a-191">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="69f4a-191">Job Type</span></span> | <span data-ttu-id="69f4a-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="69f4a-192">cdm_jobtype</span></span> |
| <span data-ttu-id="69f4a-193">اللغة</span><span class="sxs-lookup"><span data-stu-id="69f4a-193">Language</span></span> | <span data-ttu-id="69f4a-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="69f4a-194">cdm_language</span></span> |
| <span data-ttu-id="69f4a-195">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="69f4a-195">Title</span></span> | <span data-ttu-id="69f4a-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="69f4a-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="69f4a-197">توفر الأبعاد المالية لـ **نوع المنصب **، و**تعيين عامل المنصب**، و**التوظيف** تكاملاً من اتجاه واحد لـ Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69f4a-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="69f4a-198">في الوقت الحالي، لا يمكن مزامنة تحديثات الأبعاد المالية من Common Data Service إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="69f4a-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="69f4a-199">كيانات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="69f4a-199">Leave and absence entities</span></span>

| <span data-ttu-id="69f4a-200">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-200">Name</span></span> | <span data-ttu-id="69f4a-201">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-202">حركة بنك الإجازة</span><span class="sxs-lookup"><span data-stu-id="69f4a-202">Leave Bank Transaction</span></span> | <span data-ttu-id="69f4a-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="69f4a-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="69f4a-204">تسجيل الأجازة</span><span class="sxs-lookup"><span data-stu-id="69f4a-204">Leave Enrollment</span></span> | <span data-ttu-id="69f4a-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="69f4a-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="69f4a-206">خطة الإجازة</span><span class="sxs-lookup"><span data-stu-id="69f4a-206">Leave Plan</span></span> | <span data-ttu-id="69f4a-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="69f4a-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="69f4a-208">طلب الإجازة</span><span class="sxs-lookup"><span data-stu-id="69f4a-208">Leave Request</span></span> | <span data-ttu-id="69f4a-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="69f4a-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="69f4a-210">تفاصيل طلب المستخدم</span><span class="sxs-lookup"><span data-stu-id="69f4a-210">Leave Request Detail</span></span> | <span data-ttu-id="69f4a-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="69f4a-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="69f4a-212">نوع الإجازة</span><span class="sxs-lookup"><span data-stu-id="69f4a-212">Leave Type</span></span> | <span data-ttu-id="69f4a-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="69f4a-213">cdm_leavetype</span></span> |
| <span data-ttu-id="69f4a-214">كود سبب نوع الإجازة‬</span><span class="sxs-lookup"><span data-stu-id="69f4a-214">Leave Type Reason Code</span></span> | <span data-ttu-id="69f4a-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="69f4a-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="69f4a-216">كيانات الرواتب</span><span class="sxs-lookup"><span data-stu-id="69f4a-216">Payroll entities</span></span>

| <span data-ttu-id="69f4a-217">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-217">Name</span></span> | <span data-ttu-id="69f4a-218">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-219">دورة الدفع</span><span class="sxs-lookup"><span data-stu-id="69f4a-219">Pay Cycle</span></span> | <span data-ttu-id="69f4a-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="69f4a-220">cdm_paycycle</span></span> |
| <span data-ttu-id="69f4a-221">فترة الدفع</span><span class="sxs-lookup"><span data-stu-id="69f4a-221">Pay Period</span></span> | <span data-ttu-id="69f4a-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="69f4a-222">cdm_payperiod</span></span> |
| <span data-ttu-id="69f4a-223">كود أرباح كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="69f4a-223">Payroll Earning Code</span></span> | <span data-ttu-id="69f4a-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="69f4a-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="69f4a-225">مصروف الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="69f4a-225">Bank Account Disbursement</span></span> | <span data-ttu-id="69f4a-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="69f4a-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="69f4a-227">منطقة الضريبة</span><span class="sxs-lookup"><span data-stu-id="69f4a-227">Tax Region</span></span> | <span data-ttu-id="69f4a-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="69f4a-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="69f4a-229">كيانات العامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-229">Worker entities</span></span>

| <span data-ttu-id="69f4a-230">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-230">Name</span></span> | <span data-ttu-id="69f4a-231">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-232">العامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-232">Worker</span></span> | <span data-ttu-id="69f4a-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="69f4a-233">cdm_worker</span></span> |
| <span data-ttu-id="69f4a-234">عنوان العامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-234">Worker Address</span></span> | <span data-ttu-id="69f4a-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="69f4a-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="69f4a-236">التفاصيل الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-236">Worker Personal Detail</span></span> | <span data-ttu-id="69f4a-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="69f4a-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="69f4a-238">رقم الهوية الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-238">Worker Person Identification Number</span></span> | <span data-ttu-id="69f4a-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="69f4a-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="69f4a-240">نوع الهوية الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-240">Worker Person Identification Type</span></span> | <span data-ttu-id="69f4a-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="69f4a-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="69f4a-242">تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="69f4a-242">Work Calendar</span></span> | <span data-ttu-id="69f4a-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="69f4a-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="69f4a-244">يوم تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="69f4a-244">Work Calendar Day</span></span> | <span data-ttu-id="69f4a-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="69f4a-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="69f4a-246">إجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="69f4a-246">Work Calendar Holiday</span></span> |<span data-ttu-id="69f4a-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="69f4a-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="69f4a-248">بند أجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="69f4a-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="69f4a-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="69f4a-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="69f4a-250">الفاصل الزمني لتقويم العمل</span><span class="sxs-lookup"><span data-stu-id="69f4a-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="69f4a-251">cdm_workcalendartimeinterval (غير ممكّن‬ لدعم الحقل المخصص)</span><span class="sxs-lookup"><span data-stu-id="69f4a-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="69f4a-252">الحساب البنكي للعامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-252">Worker Bank Account</span></span> | <span data-ttu-id="69f4a-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="69f4a-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="69f4a-254">كيانات إعداد العامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-254">Worker setup entities</span></span>

| <span data-ttu-id="69f4a-255">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-255">Name</span></span> | <span data-ttu-id="69f4a-256">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-257">حالة الخبير</span><span class="sxs-lookup"><span data-stu-id="69f4a-257">Veteran Status</span></span> | <span data-ttu-id="69f4a-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="69f4a-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="69f4a-259">الأصل العرقي</span><span class="sxs-lookup"><span data-stu-id="69f4a-259">Ethnic Origin</span></span> | <span data-ttu-id="69f4a-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="69f4a-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="69f4a-261">كود السبب</span><span class="sxs-lookup"><span data-stu-id="69f4a-261">Reason Code</span></span> | <span data-ttu-id="69f4a-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="69f4a-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="69f4a-263">وكاله إصدار الهوية الشخصية</span><span class="sxs-lookup"><span data-stu-id="69f4a-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="69f4a-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="69f4a-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="69f4a-265">كيانات الاختصاص</span><span class="sxs-lookup"><span data-stu-id="69f4a-265">Competency entities</span></span>

| <span data-ttu-id="69f4a-266">الاسم</span><span class="sxs-lookup"><span data-stu-id="69f4a-266">Name</span></span> | <span data-ttu-id="69f4a-267">الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="69f4a-268">نوع المهارة</span><span class="sxs-lookup"><span data-stu-id="69f4a-268">Skill Type</span></span> | <span data-ttu-id="69f4a-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="69f4a-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="69f4a-270">نماذج علاقة الكيان</span><span class="sxs-lookup"><span data-stu-id="69f4a-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="69f4a-271">العامل</span><span class="sxs-lookup"><span data-stu-id="69f4a-271">Worker</span></span>

![العامل](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="69f4a-273">الوظيفة ومنصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="69f4a-273">Job and Job Position</span></span>

![الوظيفة ومنصب الوظيفة](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="69f4a-275">المزايا</span><span class="sxs-lookup"><span data-stu-id="69f4a-275">Benefits</span></span>

![المزايا](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="69f4a-277">التعويض</span><span class="sxs-lookup"><span data-stu-id="69f4a-277">Compensation</span></span>

![التعويض](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="69f4a-279">الإجازة</span><span class="sxs-lookup"><span data-stu-id="69f4a-279">Leave</span></span>

![الإجازة](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="69f4a-281">تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="69f4a-281">Work Calendar</span></span>

![تقويم العمل](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="69f4a-283">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="69f4a-283">See also</span></span>

[<span data-ttu-id="69f4a-284">اختيار تقنية تكامل بيانات</span><span class="sxs-lookup"><span data-stu-id="69f4a-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="69f4a-285">تكوين تكامل Common Data Service </span><span class="sxs-lookup"><span data-stu-id="69f4a-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
