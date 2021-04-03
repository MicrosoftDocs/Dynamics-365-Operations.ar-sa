---
title: الخبرة المهنية للشخص
description: يصف هذا الموضوع كيان الخبرة المهوية للشخص في Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5672e32b157b46b6863f06fea123fd3d6a3d96d2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466414"
---
# <a name="person-professional-experience"></a><span data-ttu-id="09947-103">الخبرة المهنية للشخص</span><span class="sxs-lookup"><span data-stu-id="09947-103">Person professional experience</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09947-104">يصف هذا الموضوع كيان الخبرة المهوية للشخص في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09947-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="09947-105">الاسم الفعلي: mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="09947-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="09947-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="09947-106">Description</span></span>

<span data-ttu-id="09947-107">يصف هذا الكيان الخبرة المهنية أو محفوظات العمل الخاصة بأحد الترشيحات.</span><span class="sxs-lookup"><span data-stu-id="09947-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="09947-108">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="09947-108">JSON representation</span></span>

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="09947-109">الخصائص</span><span class="sxs-lookup"><span data-stu-id="09947-109">Properties</span></span>

| <span data-ttu-id="09947-110">الخاصية</span><span class="sxs-lookup"><span data-stu-id="09947-110">Property</span></span><br><span data-ttu-id="09947-111">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="09947-111">**Physical name**</span></span><br><span data-ttu-id="09947-112">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="09947-112">**_Type_**</span></span> | <span data-ttu-id="09947-113">استخدام</span><span class="sxs-lookup"><span data-stu-id="09947-113">Use</span></span> | <span data-ttu-id="09947-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="09947-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="09947-115">**معرف كيان الخبرة المهنية للشخص**</span><span class="sxs-lookup"><span data-stu-id="09947-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="09947-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="09947-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="09947-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="09947-117">*GUID*</span></span> | <span data-ttu-id="09947-118">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="09947-118">Read-only</span></span><br><span data-ttu-id="09947-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-119">Required</span></span> | <span data-ttu-id="09947-120">معرف فريد منشأ بواسطة النظام لسجل الكيان.</span><span class="sxs-lookup"><span data-stu-id="09947-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="09947-121">**رقم الطرف**</span><span class="sxs-lookup"><span data-stu-id="09947-121">**Party Number**</span></span><br><span data-ttu-id="09947-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="09947-122">mshr_partynumber</span></span><br><span data-ttu-id="09947-123">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-123">*String*</span></span> | <span data-ttu-id="09947-124">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-124">Read/write</span></span><br><span data-ttu-id="09947-125">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-125">Required</span></span> | <span data-ttu-id="09947-126">المعرف الفريد لسجل الشخص الخاص بالمرشح.</span><span class="sxs-lookup"><span data-stu-id="09947-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="09947-127">**قيمة معرف الشخص**</span><span class="sxs-lookup"><span data-stu-id="09947-127">**Person ID Value**</span></span><br><span data-ttu-id="09947-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="09947-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="09947-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="09947-129">*GUID*</span></span> | <span data-ttu-id="09947-130">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="09947-130">Read-only</span></span><br><span data-ttu-id="09947-131">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-131">Required</span></span><br><span data-ttu-id="09947-132">المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="09947-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="09947-133">معرف فريد منشأ بواسطة النظام لسجل كيان الشخص.</span><span class="sxs-lookup"><span data-stu-id="09947-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="09947-134">**منصب صاحب العمل**</span><span class="sxs-lookup"><span data-stu-id="09947-134">**Employer Position**</span></span><br><span data-ttu-id="09947-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="09947-135">mshr_employerposition</span></span><br><span data-ttu-id="09947-136">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-136">*String*</span></span> | <span data-ttu-id="09947-137">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-137">Read/write</span></span><br><span data-ttu-id="09947-138">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-138">Required</span></span> | <span data-ttu-id="09947-139">لقب المنصب الذي كان المرشح يشغله أثناء التوظيف.</span><span class="sxs-lookup"><span data-stu-id="09947-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="09947-140">**اسم صاحب العمل**</span><span class="sxs-lookup"><span data-stu-id="09947-140">**Employer Name**</span></span><br><span data-ttu-id="09947-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="09947-141">mshr_employername</span></span><br><span data-ttu-id="09947-142">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-142">*String*</span></span> | <span data-ttu-id="09947-143">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-143">Read/write</span></span><br><span data-ttu-id="09947-144">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-144">Required</span></span> | <span data-ttu-id="09947-145">اسم صاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="09947-145">The name of the employer.</span></span> |
| <span data-ttu-id="09947-146">**موقع صاحب العمل**</span><span class="sxs-lookup"><span data-stu-id="09947-146">**Employer Location**</span></span><br><span data-ttu-id="09947-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="09947-147">mshr_employerlocation</span></span><br><span data-ttu-id="09947-148">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-148">*String*</span></span> | <span data-ttu-id="09947-149">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-149">Read/write</span></span><br><span data-ttu-id="09947-150">اختياري</span><span class="sxs-lookup"><span data-stu-id="09947-150">Optional</span></span> | <span data-ttu-id="09947-151">موقع صاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="09947-151">The employer’s location.</span></span> <span data-ttu-id="09947-152">الحد الأقصى للطول: 60.</span><span class="sxs-lookup"><span data-stu-id="09947-152">Max length: 60.</span></span> <span data-ttu-id="09947-153">لا يوجد تنسيق خاص مطلوب أو محدد.</span><span class="sxs-lookup"><span data-stu-id="09947-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="09947-154">**الهاتف**</span><span class="sxs-lookup"><span data-stu-id="09947-154">**Phone**</span></span><br><span data-ttu-id="09947-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="09947-155">mshr_phone</span></span><br><span data-ttu-id="09947-156">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-156">*String*</span></span> | <span data-ttu-id="09947-157">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-157">Read/write</span></span><br><span data-ttu-id="09947-158">اختياري</span><span class="sxs-lookup"><span data-stu-id="09947-158">Optional</span></span> | <span data-ttu-id="09947-159">رقم هاتف صاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="09947-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="09947-160">**عنوان URL**</span><span class="sxs-lookup"><span data-stu-id="09947-160">**URL**</span></span><br><span data-ttu-id="09947-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="09947-161">mshr_url</span></span><br><span data-ttu-id="09947-162">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-162">*String*</span></span> | <span data-ttu-id="09947-163">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-163">Read/write</span></span><br><span data-ttu-id="09947-164">اختياري</span><span class="sxs-lookup"><span data-stu-id="09947-164">Optional</span></span> | <span data-ttu-id="09947-165">عنوان URL لموقع ويب صاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="09947-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="09947-166">**تاريخ البدء**</span><span class="sxs-lookup"><span data-stu-id="09947-166">**Start Date**</span></span><br><span data-ttu-id="09947-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="09947-167">mshr_startdate</span></span><br><span data-ttu-id="09947-168">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="09947-168">*Datetime*</span></span> | <span data-ttu-id="09947-169">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-169">Read/write</span></span><br><span data-ttu-id="09947-170">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-170">Required</span></span> | <span data-ttu-id="09947-171">تاريخ بدء توظيف المرشح.</span><span class="sxs-lookup"><span data-stu-id="09947-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="09947-172">**تاريخ النهاية**</span><span class="sxs-lookup"><span data-stu-id="09947-172">**End Date**</span></span><br><span data-ttu-id="09947-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="09947-173">mshr_enddate</span></span><br><span data-ttu-id="09947-174">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="09947-174">*Datetime*</span></span> | <span data-ttu-id="09947-175">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-175">Read/write</span></span><br><span data-ttu-id="09947-176">اختياري</span><span class="sxs-lookup"><span data-stu-id="09947-176">Optional</span></span> | <span data-ttu-id="09947-177">تاريخ الانتهاء الخاص بتوظيف المرشح أو قيمة خالية في حالة ما إذا كانت المرشح ما يزال موظفًا هنا.</span><span class="sxs-lookup"><span data-stu-id="09947-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="09947-178">**السماح بالاتصال بصاحب العمل**</span><span class="sxs-lookup"><span data-stu-id="09947-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="09947-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="09947-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="09947-180">*مجموعة خيارات mshr_hrmblankyesno*</span><span class="sxs-lookup"><span data-stu-id="09947-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="09947-181">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-181">Read/write</span></span><br><span data-ttu-id="09947-182">اختياري</span><span class="sxs-lookup"><span data-stu-id="09947-182">Optional</span></span> | <span data-ttu-id="09947-183">يشير ما إذا كان المرشح يسمح بالاتصال بصاحب العمل السابق أم لا.</span><span class="sxs-lookup"><span data-stu-id="09947-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="09947-184">**الملاحظات**</span><span class="sxs-lookup"><span data-stu-id="09947-184">**Notes**</span></span><br><span data-ttu-id="09947-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="09947-185">mshr_note</span></span><br><span data-ttu-id="09947-186">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-186">*String*</span></span> | <span data-ttu-id="09947-187">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="09947-187">Read/write</span></span><br><span data-ttu-id="09947-188">اختياري</span><span class="sxs-lookup"><span data-stu-id="09947-188">Optional</span></span> | <span data-ttu-id="09947-189">ملاحظات للاستخدام من جانب مسؤولي التعيين أو مدراء التوظيف.</span><span class="sxs-lookup"><span data-stu-id="09947-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="09947-190">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="09947-190">**Primary Field**</span></span><br><span data-ttu-id="09947-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="09947-191">mshr_primaryfield</span></span><br><span data-ttu-id="09947-192">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09947-192">*String*</span></span> | <span data-ttu-id="09947-193">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="09947-193">Read-only</span></span><br><span data-ttu-id="09947-194">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09947-194">Required</span></span> | <span data-ttu-id="09947-195">حقل يستخدم كمعرف أساسي لسجل الكيان.</span><span class="sxs-lookup"><span data-stu-id="09947-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="09947-196">مجموعة رقم الطرف وتاريخ البدء ومنصب صاحب العمل واسم صاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="09947-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="09947-197">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="09947-197">See also</span></span>

[<span data-ttu-id="09947-198">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="09947-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="09947-199">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="09947-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]