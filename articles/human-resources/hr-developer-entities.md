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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087336"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="1d962-103">كيانات Common Data Service .</span><span class="sxs-lookup"><span data-stu-id="1d962-103">Common Data Service entities</span></span>

<span data-ttu-id="1d962-104">تستخدم Microsoft Dynamics 365 Human Resources خدمة Common Data Service لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.</span><span class="sxs-lookup"><span data-stu-id="1d962-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="1d962-105">لمزيدٍ من المعلومات حول Common Data Service، راجع [ما المقصود بـ Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="1d962-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="1d962-106">كيانات الموارد البشرية التالية متوفرة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1d962-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="1d962-107">كيانات الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-107">Benefit entities</span></span>

| <span data-ttu-id="1d962-108">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-108">Name</span></span> | <span data-ttu-id="1d962-109">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-110">تكرار حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="1d962-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="1d962-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="1d962-112">حساب تكرار فترة دفع الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="1d962-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="1d962-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="1d962-114">معدل حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="1d962-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="1d962-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="1d962-116">تفاصيل معدل حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="1d962-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="1d962-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="1d962-118">خيار الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-118">Benefit Option</span></span> | <span data-ttu-id="1d962-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="1d962-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="1d962-120">خطة الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-120">Benefit Plan</span></span> | <span data-ttu-id="1d962-121">cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص)</span><span class="sxs-lookup"><span data-stu-id="1d962-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1d962-122">نوع الميزة</span><span class="sxs-lookup"><span data-stu-id="1d962-122">Benefit Type</span></span> | <span data-ttu-id="1d962-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="1d962-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="1d962-124">كيانات مهام العملية التجارية</span><span class="sxs-lookup"><span data-stu-id="1d962-124">Business process tasks entities</span></span>

| <span data-ttu-id="1d962-125">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-125">Name</span></span> | <span data-ttu-id="1d962-126">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-127">تقويم عملية الأعمال</span><span class="sxs-lookup"><span data-stu-id="1d962-127">Business Process Calendar</span></span> | <span data-ttu-id="1d962-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="1d962-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="1d962-129">تعيين مجموعة عمليات الأعمال</span><span class="sxs-lookup"><span data-stu-id="1d962-129">Business Process Group Assignment</span></span> | <span data-ttu-id="1d962-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="1d962-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="1d962-131">مجموعة مهام مكتبة عمليات الأعمال</span><span class="sxs-lookup"><span data-stu-id="1d962-131">Business Process Library Task Group</span></span> | <span data-ttu-id="1d962-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="1d962-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="1d962-133">مرحلة عملية الأعمال‬</span><span class="sxs-lookup"><span data-stu-id="1d962-133">Business Process Stage</span></span> | <span data-ttu-id="1d962-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="1d962-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="1d962-135">رأس قالب قائمة الاختيار</span><span class="sxs-lookup"><span data-stu-id="1d962-135">Checklist Template Header</span></span> | <span data-ttu-id="1d962-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="1d962-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="1d962-137">مهمة قالب قائمة الاختيار</span><span class="sxs-lookup"><span data-stu-id="1d962-137">Checklist Template Task</span></span> | <span data-ttu-id="1d962-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="1d962-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="1d962-139">كيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-139">Compensation entities</span></span>

| <span data-ttu-id="1d962-140">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-140">Name</span></span> | <span data-ttu-id="1d962-141">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-142">الخطة الثابتة للتعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="1d962-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="1d962-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="1d962-144">شبكة التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-144">Compensation Grid</span></span> | <span data-ttu-id="1d962-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="1d962-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="1d962-146">مستوى التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-146">Compensation Level</span></span> | <span data-ttu-id="1d962-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="1d962-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="1d962-148">تكرار دفع التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="1d962-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="1d962-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="1d962-150">إعداد النقاط المرجعية للتعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="1d962-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="1d962-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="1d962-152">إعداد بند النقاط المرجعية للتعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="1d962-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="1d962-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="1d962-154">منطقة التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-154">Compensation Region</span></span> | <span data-ttu-id="1d962-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="1d962-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="1d962-156">بنية التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-156">Compensation Structure</span></span> | <span data-ttu-id="1d962-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="1d962-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="1d962-158">خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="1d962-158">Compensation Variable Plan</span></span> | <span data-ttu-id="1d962-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="1d962-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="1d962-160">مستوى خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="1d962-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="1d962-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="1d962-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="1d962-162">نوع خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="1d962-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="1d962-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="1d962-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="1d962-164">حدث التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="1d962-164">Fixed Compensation Event</span></span> | <span data-ttu-id="1d962-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="1d962-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="1d962-166">قاعدة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="1d962-166">Vesting Rule</span></span> | <span data-ttu-id="1d962-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="1d962-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="1d962-168">التعويض الثابت للعامل</span><span class="sxs-lookup"><span data-stu-id="1d962-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="1d962-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="1d962-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="1d962-170">كيانات المؤسسة</span><span class="sxs-lookup"><span data-stu-id="1d962-170">Organization entities</span></span>

| <span data-ttu-id="1d962-171">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-171">Name</span></span> | <span data-ttu-id="1d962-172">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-173">قسم</span><span class="sxs-lookup"><span data-stu-id="1d962-173">Department</span></span> | <span data-ttu-id="1d962-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="1d962-174">cdm_department</span></span> |
| <span data-ttu-id="1d962-175">التوظيف</span><span class="sxs-lookup"><span data-stu-id="1d962-175">Employment</span></span> | <span data-ttu-id="1d962-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="1d962-176">cdm_employment</span></span> |
| <span data-ttu-id="1d962-177">الشركة</span><span class="sxs-lookup"><span data-stu-id="1d962-177">Company</span></span> | <span data-ttu-id="1d962-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="1d962-178">cdm_company</span></span> |
| <span data-ttu-id="1d962-179">وظيفة</span><span class="sxs-lookup"><span data-stu-id="1d962-179">Job</span></span> | <span data-ttu-id="1d962-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="1d962-180">cdm_job</span></span> |
| <span data-ttu-id="1d962-181">مهمة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="1d962-181">Job Function</span></span> | <span data-ttu-id="1d962-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="1d962-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="1d962-183">منصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="1d962-183">Job Position</span></span> | <span data-ttu-id="1d962-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="1d962-184">cdm_jobposition</span></span> |
| <span data-ttu-id="1d962-185">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="1d962-185">Position Type</span></span> | <span data-ttu-id="1d962-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="1d962-186">cdm_positiontype</span></span> |
| <span data-ttu-id="1d962-187">تعيين العامل بالمنصب</span><span class="sxs-lookup"><span data-stu-id="1d962-187">Position Worker Assignment</span></span> | <span data-ttu-id="1d962-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="1d962-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="1d962-189">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="1d962-189">Job Type</span></span> | <span data-ttu-id="1d962-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="1d962-190">cdm_jobtype</span></span> |
| <span data-ttu-id="1d962-191">اللغة</span><span class="sxs-lookup"><span data-stu-id="1d962-191">Language</span></span> | <span data-ttu-id="1d962-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="1d962-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="1d962-193">كيانات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="1d962-193">Leave and absence entities</span></span>

| <span data-ttu-id="1d962-194">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-194">Name</span></span> | <span data-ttu-id="1d962-195">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-196">حركة أجازة البنك</span><span class="sxs-lookup"><span data-stu-id="1d962-196">Leave Bank Transaction</span></span> | <span data-ttu-id="1d962-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="1d962-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="1d962-198">تسجيل الأجازة</span><span class="sxs-lookup"><span data-stu-id="1d962-198">Leave Enrollment</span></span> | <span data-ttu-id="1d962-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="1d962-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="1d962-200">خطة الإجازة</span><span class="sxs-lookup"><span data-stu-id="1d962-200">Leave Plan</span></span> | <span data-ttu-id="1d962-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="1d962-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="1d962-202">طلب الإجازة</span><span class="sxs-lookup"><span data-stu-id="1d962-202">Leave Request</span></span> | <span data-ttu-id="1d962-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="1d962-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="1d962-204">تفاصيل طلب المستخدم</span><span class="sxs-lookup"><span data-stu-id="1d962-204">Leave Request Detail</span></span> | <span data-ttu-id="1d962-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="1d962-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="1d962-206">نوع الإجازة</span><span class="sxs-lookup"><span data-stu-id="1d962-206">Leave Type</span></span> | <span data-ttu-id="1d962-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="1d962-207">cdm_leavetype</span></span> |
| <span data-ttu-id="1d962-208">كود سبب نوع الإجازة‬</span><span class="sxs-lookup"><span data-stu-id="1d962-208">Leave Type Reason Code</span></span> | <span data-ttu-id="1d962-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="1d962-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="1d962-210">كيانات الرواتب</span><span class="sxs-lookup"><span data-stu-id="1d962-210">Payroll entities</span></span>

| <span data-ttu-id="1d962-211">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-211">Name</span></span> | <span data-ttu-id="1d962-212">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-213">دورة الدفع</span><span class="sxs-lookup"><span data-stu-id="1d962-213">Pay Cycle</span></span> | <span data-ttu-id="1d962-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="1d962-214">cdm_paycycle</span></span> |
| <span data-ttu-id="1d962-215">فترة الدفع</span><span class="sxs-lookup"><span data-stu-id="1d962-215">Pay Period</span></span> | <span data-ttu-id="1d962-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="1d962-216">cdm_payperiod</span></span> |
| <span data-ttu-id="1d962-217">كود أرباح كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="1d962-217">Payroll Earning Code</span></span> | <span data-ttu-id="1d962-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="1d962-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="1d962-219">مصروف الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="1d962-219">Bank Account Disbursement</span></span> | <span data-ttu-id="1d962-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="1d962-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="1d962-221">منطقة الضريبة</span><span class="sxs-lookup"><span data-stu-id="1d962-221">Tax Region</span></span> | <span data-ttu-id="1d962-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="1d962-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="1d962-223">كيانات العامل</span><span class="sxs-lookup"><span data-stu-id="1d962-223">Worker entities</span></span>

| <span data-ttu-id="1d962-224">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-224">Name</span></span> | <span data-ttu-id="1d962-225">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-226">العامل</span><span class="sxs-lookup"><span data-stu-id="1d962-226">Worker</span></span> | <span data-ttu-id="1d962-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="1d962-227">cdm_worker</span></span> |
| <span data-ttu-id="1d962-228">عنوان العامل</span><span class="sxs-lookup"><span data-stu-id="1d962-228">Worker Address</span></span> | <span data-ttu-id="1d962-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="1d962-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="1d962-230">التفاصيل الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="1d962-230">Worker Personal Detail</span></span> | <span data-ttu-id="1d962-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="1d962-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="1d962-232">رقم الهوية الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="1d962-232">Worker Person Identification Number</span></span> | <span data-ttu-id="1d962-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="1d962-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="1d962-234">نوع الهوية الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="1d962-234">Worker Person Identification Type</span></span> | <span data-ttu-id="1d962-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="1d962-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="1d962-236">تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="1d962-236">Work Calendar</span></span> | <span data-ttu-id="1d962-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="1d962-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="1d962-238">يوم تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="1d962-238">Work Calendar Day</span></span> | <span data-ttu-id="1d962-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="1d962-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="1d962-240">إجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="1d962-240">Work Calendar Holiday</span></span> |<span data-ttu-id="1d962-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="1d962-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="1d962-242">بند أجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="1d962-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="1d962-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="1d962-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="1d962-244">الفاصل الزمني لتقويم العمل</span><span class="sxs-lookup"><span data-stu-id="1d962-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="1d962-245">cdm_workcalendartimeinterval (غير ممكّن‬ لدعم الحقل المخصص)</span><span class="sxs-lookup"><span data-stu-id="1d962-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1d962-246">الحساب البنكي للعامل</span><span class="sxs-lookup"><span data-stu-id="1d962-246">Worker Bank Account</span></span> | <span data-ttu-id="1d962-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="1d962-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="1d962-248">كيانات إعداد العامل</span><span class="sxs-lookup"><span data-stu-id="1d962-248">Worker setup entities</span></span>

| <span data-ttu-id="1d962-249">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-249">Name</span></span> | <span data-ttu-id="1d962-250">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-251">حالة الخبير</span><span class="sxs-lookup"><span data-stu-id="1d962-251">Veteran Status</span></span> | <span data-ttu-id="1d962-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="1d962-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="1d962-253">الأصل العرقي</span><span class="sxs-lookup"><span data-stu-id="1d962-253">Ethnic Origin</span></span> | <span data-ttu-id="1d962-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="1d962-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="1d962-255">كود السبب</span><span class="sxs-lookup"><span data-stu-id="1d962-255">Reason Code</span></span> | <span data-ttu-id="1d962-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="1d962-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="1d962-257">وكاله إصدار الهوية الشخصية</span><span class="sxs-lookup"><span data-stu-id="1d962-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="1d962-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="1d962-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="1d962-259">كيانات الاختصاص</span><span class="sxs-lookup"><span data-stu-id="1d962-259">Competency entities</span></span>

| <span data-ttu-id="1d962-260">الاسم</span><span class="sxs-lookup"><span data-stu-id="1d962-260">Name</span></span> | <span data-ttu-id="1d962-261">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1d962-262">نوع المهارة</span><span class="sxs-lookup"><span data-stu-id="1d962-262">Skill Type</span></span> | <span data-ttu-id="1d962-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="1d962-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="1d962-264">نماذج علاقة الكيان</span><span class="sxs-lookup"><span data-stu-id="1d962-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="1d962-265">العامل</span><span class="sxs-lookup"><span data-stu-id="1d962-265">Worker</span></span>

![العامل](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="1d962-267">الوظيفة ومنصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="1d962-267">Job and Job Position</span></span>

![الوظيفة ومنصب الوظيفة](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="1d962-269">المزايا</span><span class="sxs-lookup"><span data-stu-id="1d962-269">Benefits</span></span>

![المزايا](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="1d962-271">التعويض</span><span class="sxs-lookup"><span data-stu-id="1d962-271">Compensation</span></span>

![التعويض](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="1d962-273">الإجازة</span><span class="sxs-lookup"><span data-stu-id="1d962-273">Leave</span></span>

![الإجازة](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="1d962-275">تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="1d962-275">Work Calendar</span></span>

![تقويم العمل](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="1d962-277">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="1d962-277">See also</span></span>

[<span data-ttu-id="1d962-278">اختيار تقنية تكامل بيانات</span><span class="sxs-lookup"><span data-stu-id="1d962-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="1d962-279">تكوين تكامل Common Data Service </span><span class="sxs-lookup"><span data-stu-id="1d962-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)