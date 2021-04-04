---
title: جداول Dataverse
description: تستخدم Microsoft Dynamics 365 Human Resources خدمة Dataverse لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465212"
---
# <a name="dataverse-tables"></a><span data-ttu-id="c8f55-103">جداول Dataverse</span><span class="sxs-lookup"><span data-stu-id="c8f55-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c8f55-104">تستخدم Microsoft Dynamics 365 Human Resources خدمة Dataverse لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.</span><span class="sxs-lookup"><span data-stu-id="c8f55-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="c8f55-105">تتوافق كيانات Human Resources مع جداول Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c8f55-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="c8f55-106">لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="c8f55-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="c8f55-107">جداول Dataverse التالي متوفرة استنادًا إلى كيانات Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8f55-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="c8f55-108">جداول الميزات</span><span class="sxs-lookup"><span data-stu-id="c8f55-108">Benefit tables</span></span>

| <span data-ttu-id="c8f55-109">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-109">Name</span></span> | <span data-ttu-id="c8f55-110">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-111">تكرار حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="c8f55-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="c8f55-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="c8f55-113">حساب تكرار فترة دفع الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="c8f55-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="c8f55-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="c8f55-115">معدل حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="c8f55-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="c8f55-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="c8f55-117">تفاصيل معدل حساب الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="c8f55-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="c8f55-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="c8f55-119">خيار الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-119">Benefit Option</span></span> | <span data-ttu-id="c8f55-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="c8f55-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="c8f55-121">خطة الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-121">Benefit Plan</span></span> | <span data-ttu-id="c8f55-122">cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص)</span><span class="sxs-lookup"><span data-stu-id="c8f55-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="c8f55-123">نوع الميزة</span><span class="sxs-lookup"><span data-stu-id="c8f55-123">Benefit Type</span></span> | <span data-ttu-id="c8f55-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="c8f55-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="c8f55-125">جداول مهام العملية التجارية</span><span class="sxs-lookup"><span data-stu-id="c8f55-125">Business process tasks tables</span></span>

| <span data-ttu-id="c8f55-126">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-126">Name</span></span> | <span data-ttu-id="c8f55-127">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-128">تقويم عملية الأعمال</span><span class="sxs-lookup"><span data-stu-id="c8f55-128">Business Process Calendar</span></span> | <span data-ttu-id="c8f55-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="c8f55-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="c8f55-130">تعيين مجموعة عمليات الأعمال</span><span class="sxs-lookup"><span data-stu-id="c8f55-130">Business Process Group Assignment</span></span> | <span data-ttu-id="c8f55-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="c8f55-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="c8f55-132">مجموعة مهام مكتبة عمليات الأعمال</span><span class="sxs-lookup"><span data-stu-id="c8f55-132">Business Process Library Task Group</span></span> | <span data-ttu-id="c8f55-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="c8f55-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="c8f55-134">مرحلة عملية الأعمال‬</span><span class="sxs-lookup"><span data-stu-id="c8f55-134">Business Process Stage</span></span> | <span data-ttu-id="c8f55-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="c8f55-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="c8f55-136">رأس قالب قائمة الاختيار</span><span class="sxs-lookup"><span data-stu-id="c8f55-136">Checklist Template Header</span></span> | <span data-ttu-id="c8f55-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="c8f55-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="c8f55-138">مهمة قالب قائمة الاختيار</span><span class="sxs-lookup"><span data-stu-id="c8f55-138">Checklist Template Task</span></span> | <span data-ttu-id="c8f55-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="c8f55-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="c8f55-140">جداول التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-140">Compensation tables</span></span>

| <span data-ttu-id="c8f55-141">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-141">Name</span></span> | <span data-ttu-id="c8f55-142">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-143">خطة التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="c8f55-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="c8f55-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="c8f55-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="c8f55-145">شبكة التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-145">Compensation Grid</span></span> | <span data-ttu-id="c8f55-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="c8f55-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="c8f55-147">مستوى التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-147">Compensation Level</span></span> | <span data-ttu-id="c8f55-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="c8f55-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="c8f55-149">تكرار دفع التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="c8f55-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="c8f55-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="c8f55-151">إعداد النقاط المرجعية للتعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="c8f55-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="c8f55-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="c8f55-153">إعداد بند النقاط المرجعية للتعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="c8f55-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="c8f55-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="c8f55-155">منطقة التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-155">Compensation Region</span></span> | <span data-ttu-id="c8f55-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="c8f55-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="c8f55-157">بنية التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-157">Compensation Structure</span></span> | <span data-ttu-id="c8f55-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="c8f55-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="c8f55-159">خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="c8f55-159">Compensation Variable Plan</span></span> | <span data-ttu-id="c8f55-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="c8f55-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="c8f55-161">مستوى خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="c8f55-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="c8f55-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="c8f55-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="c8f55-163">نوع خطة التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="c8f55-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="c8f55-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="c8f55-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="c8f55-165">حدث التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="c8f55-165">Fixed Compensation Event</span></span> | <span data-ttu-id="c8f55-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="c8f55-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="c8f55-167">قاعدة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="c8f55-167">Vesting Rule</span></span> | <span data-ttu-id="c8f55-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="c8f55-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="c8f55-169">التعويض الثابت للعاملين</span><span class="sxs-lookup"><span data-stu-id="c8f55-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="c8f55-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="c8f55-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="c8f55-171">جداول المؤسسة</span><span class="sxs-lookup"><span data-stu-id="c8f55-171">Organization tables</span></span>

| <span data-ttu-id="c8f55-172">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-172">Name</span></span> | <span data-ttu-id="c8f55-173">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-174">قسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-174">Department</span></span> | <span data-ttu-id="c8f55-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="c8f55-175">cdm_department</span></span> |
| <span data-ttu-id="c8f55-176">التوظيف</span><span class="sxs-lookup"><span data-stu-id="c8f55-176">Employment</span></span> | <span data-ttu-id="c8f55-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="c8f55-177">cdm_employment</span></span> |
| <span data-ttu-id="c8f55-178">الشركة</span><span class="sxs-lookup"><span data-stu-id="c8f55-178">Company</span></span> | <span data-ttu-id="c8f55-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="c8f55-179">cdm_company</span></span> |
| <span data-ttu-id="c8f55-180">وظيفة</span><span class="sxs-lookup"><span data-stu-id="c8f55-180">Job</span></span> | <span data-ttu-id="c8f55-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="c8f55-181">cdm_job</span></span> |
| <span data-ttu-id="c8f55-182">مهمة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="c8f55-182">Job Function</span></span> | <span data-ttu-id="c8f55-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="c8f55-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="c8f55-184">منصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="c8f55-184">Job Position</span></span> | <span data-ttu-id="c8f55-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="c8f55-185">cdm_jobposition</span></span> |
| <span data-ttu-id="c8f55-186">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="c8f55-186">Position Type</span></span> | <span data-ttu-id="c8f55-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="c8f55-187">cdm_positiontype</span></span> |
| <span data-ttu-id="c8f55-188">تعيين العامل بالمنصب</span><span class="sxs-lookup"><span data-stu-id="c8f55-188">Position Worker Assignment</span></span> | <span data-ttu-id="c8f55-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="c8f55-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="c8f55-190">بُعد منصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="c8f55-190">Job Position Dimension</span></span> | <span data-ttu-id="c8f55-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="c8f55-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="c8f55-192">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="c8f55-192">Job Type</span></span> | <span data-ttu-id="c8f55-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="c8f55-193">cdm_jobtype</span></span> |
| <span data-ttu-id="c8f55-194">اللغة</span><span class="sxs-lookup"><span data-stu-id="c8f55-194">Language</span></span> | <span data-ttu-id="c8f55-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="c8f55-195">cdm_language</span></span> |
| <span data-ttu-id="c8f55-196">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="c8f55-196">Title</span></span> | <span data-ttu-id="c8f55-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="c8f55-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="c8f55-198">توفر الأبعاد المالية لـ **نوع المنصب**، و **تعيين عامل المنصب**، و **التوظيف** تكاملاً من اتجاه واحد لـ Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c8f55-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="c8f55-199">في الوقت الحالي، لا يمكن مزامنة تحديثات الأبعاد المالية من Dataverse إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8f55-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="c8f55-200">جداول الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="c8f55-200">Leave and absence tables</span></span>

| <span data-ttu-id="c8f55-201">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-201">Name</span></span> | <span data-ttu-id="c8f55-202">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-203">حركة بنك الإجازة</span><span class="sxs-lookup"><span data-stu-id="c8f55-203">Leave Bank Transaction</span></span> | <span data-ttu-id="c8f55-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="c8f55-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="c8f55-205">تسجيل الإجازات</span><span class="sxs-lookup"><span data-stu-id="c8f55-205">Leave Enrollment</span></span> | <span data-ttu-id="c8f55-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="c8f55-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="c8f55-207">خطة الإجازة</span><span class="sxs-lookup"><span data-stu-id="c8f55-207">Leave Plan</span></span> | <span data-ttu-id="c8f55-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="c8f55-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="c8f55-209">طلب الإجازة</span><span class="sxs-lookup"><span data-stu-id="c8f55-209">Leave Request</span></span> | <span data-ttu-id="c8f55-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="c8f55-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="c8f55-211">تفاصيل طلب المستخدم</span><span class="sxs-lookup"><span data-stu-id="c8f55-211">Leave Request Detail</span></span> | <span data-ttu-id="c8f55-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="c8f55-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="c8f55-213">نوع الإجازة</span><span class="sxs-lookup"><span data-stu-id="c8f55-213">Leave Type</span></span> | <span data-ttu-id="c8f55-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="c8f55-214">cdm_leavetype</span></span> |
| <span data-ttu-id="c8f55-215">كود سبب نوع الإجازة‬</span><span class="sxs-lookup"><span data-stu-id="c8f55-215">Leave Type Reason Code</span></span> | <span data-ttu-id="c8f55-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="c8f55-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="c8f55-217">جداول الرواتب</span><span class="sxs-lookup"><span data-stu-id="c8f55-217">Payroll tables</span></span>

| <span data-ttu-id="c8f55-218">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-218">Name</span></span> | <span data-ttu-id="c8f55-219">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-220">دورة الدفع</span><span class="sxs-lookup"><span data-stu-id="c8f55-220">Pay Cycle</span></span> | <span data-ttu-id="c8f55-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="c8f55-221">cdm_paycycle</span></span> |
| <span data-ttu-id="c8f55-222">فترة الدفع</span><span class="sxs-lookup"><span data-stu-id="c8f55-222">Pay Period</span></span> | <span data-ttu-id="c8f55-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="c8f55-223">cdm_payperiod</span></span> |
| <span data-ttu-id="c8f55-224">كود أرباح كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="c8f55-224">Payroll Earning Code</span></span> | <span data-ttu-id="c8f55-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="c8f55-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="c8f55-226">مصروف الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="c8f55-226">Bank Account Disbursement</span></span> | <span data-ttu-id="c8f55-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="c8f55-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="c8f55-228">منطقة الضريبة</span><span class="sxs-lookup"><span data-stu-id="c8f55-228">Tax Region</span></span> | <span data-ttu-id="c8f55-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="c8f55-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="c8f55-230">جداول العامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-230">Worker tables</span></span>

| <span data-ttu-id="c8f55-231">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-231">Name</span></span> | <span data-ttu-id="c8f55-232">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-233">العامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-233">Worker</span></span> | <span data-ttu-id="c8f55-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="c8f55-234">cdm_worker</span></span> |
| <span data-ttu-id="c8f55-235">عنوان العامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-235">Worker Address</span></span> | <span data-ttu-id="c8f55-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="c8f55-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="c8f55-237">التفاصيل الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-237">Worker Personal Detail</span></span> | <span data-ttu-id="c8f55-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="c8f55-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="c8f55-239">رقم الهوية الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-239">Worker Person Identification Number</span></span> | <span data-ttu-id="c8f55-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="c8f55-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="c8f55-241">نوع الهوية الشخصية للعامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-241">Worker Person Identification Type</span></span> | <span data-ttu-id="c8f55-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="c8f55-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="c8f55-243">تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="c8f55-243">Work Calendar</span></span> | <span data-ttu-id="c8f55-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="c8f55-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="c8f55-245">يوم تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="c8f55-245">Work Calendar Day</span></span> | <span data-ttu-id="c8f55-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="c8f55-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="c8f55-247">إجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="c8f55-247">Work Calendar Holiday</span></span> |<span data-ttu-id="c8f55-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="c8f55-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="c8f55-249">بند أجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="c8f55-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="c8f55-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="c8f55-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="c8f55-251">الفاصل الزمني لتقويم العمل</span><span class="sxs-lookup"><span data-stu-id="c8f55-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="c8f55-252">cdm_workcalendartimeinterval (غير ممكّن‬ لدعم الحقل المخصص)</span><span class="sxs-lookup"><span data-stu-id="c8f55-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="c8f55-253">الحساب البنكي للعامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-253">Worker Bank Account</span></span> | <span data-ttu-id="c8f55-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="c8f55-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="c8f55-255">جداول إعداد العامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-255">Worker setup tables</span></span>

| <span data-ttu-id="c8f55-256">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-256">Name</span></span> | <span data-ttu-id="c8f55-257">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-258">حالة الخبير</span><span class="sxs-lookup"><span data-stu-id="c8f55-258">Veteran Status</span></span> | <span data-ttu-id="c8f55-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="c8f55-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="c8f55-260">الأصل العرقي</span><span class="sxs-lookup"><span data-stu-id="c8f55-260">Ethnic Origin</span></span> | <span data-ttu-id="c8f55-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="c8f55-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="c8f55-262">كود السبب</span><span class="sxs-lookup"><span data-stu-id="c8f55-262">Reason Code</span></span> | <span data-ttu-id="c8f55-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="c8f55-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="c8f55-264">وكالة إصدار هوية العامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="c8f55-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="c8f55-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="c8f55-266">جداول الاختصاص</span><span class="sxs-lookup"><span data-stu-id="c8f55-266">Competency tables</span></span>

| <span data-ttu-id="c8f55-267">الاسم</span><span class="sxs-lookup"><span data-stu-id="c8f55-267">Name</span></span> | <span data-ttu-id="c8f55-268">الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="c8f55-269">نوع المهارة</span><span class="sxs-lookup"><span data-stu-id="c8f55-269">Skill Type</span></span> | <span data-ttu-id="c8f55-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="c8f55-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="c8f55-271">نماذج علاقة الجدول</span><span class="sxs-lookup"><span data-stu-id="c8f55-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="c8f55-272">العامل</span><span class="sxs-lookup"><span data-stu-id="c8f55-272">Worker</span></span>

![العامل](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="c8f55-274">الوظيفة ومنصب الوظيفة</span><span class="sxs-lookup"><span data-stu-id="c8f55-274">Job and Job Position</span></span>

![الوظيفة ومنصب الوظيفة](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="c8f55-276">المزايا</span><span class="sxs-lookup"><span data-stu-id="c8f55-276">Benefits</span></span>

![المزايا](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="c8f55-278">التعويض</span><span class="sxs-lookup"><span data-stu-id="c8f55-278">Compensation</span></span>

![التعويض](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="c8f55-280">الإجازة</span><span class="sxs-lookup"><span data-stu-id="c8f55-280">Leave</span></span>

![الإجازة](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="c8f55-282">تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="c8f55-282">Work Calendar</span></span>

![تقويم العمل](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="c8f55-284">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="c8f55-284">See also</span></span>

[<span data-ttu-id="c8f55-285">اختيار تقنية تكامل بيانات</span><span class="sxs-lookup"><span data-stu-id="c8f55-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="c8f55-286">تكوين تكامل Dataverse </span><span class="sxs-lookup"><span data-stu-id="c8f55-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="c8f55-287">تكوين جداول Dataverse الظاهرية</span><span class="sxs-lookup"><span data-stu-id="c8f55-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="c8f55-288">الأسئلة المتداولة حول الجداول الظاهرية في Human Resources</span><span class="sxs-lookup"><span data-stu-id="c8f55-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="c8f55-289">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="c8f55-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="c8f55-290">تحديثات المصطلحات</span><span class="sxs-lookup"><span data-stu-id="c8f55-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]