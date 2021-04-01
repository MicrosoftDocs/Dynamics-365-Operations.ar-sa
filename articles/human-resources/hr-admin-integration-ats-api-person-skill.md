---
title: مهارة الشخص
description: يصف هذا الموضوع كيان مهارة الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: b6bcbbd1203f4e9e80f6c5264cf4d5ea7d0970fc
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126088"
---
# <a name="person-skill"></a><span data-ttu-id="f1dad-103">مهارة الشخص</span><span class="sxs-lookup"><span data-stu-id="f1dad-103">Person skill</span></span>

<span data-ttu-id="f1dad-104">يصف هذا الموضوع كيان مهارة الشخص لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f1dad-104">This topic describes the Person skill entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f1dad-105">الاسم الفعلي: mshr_hcmpersonskillentity</span><span class="sxs-lookup"><span data-stu-id="f1dad-105">Physical name: mshr_hcmpersonskillentity</span></span>

## <a name="description"></a><span data-ttu-id="f1dad-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="f1dad-106">Description</span></span>

<span data-ttu-id="f1dad-107">يصف هذا الكيان المهارات الخاصة بالمرشح.</span><span class="sxs-lookup"><span data-stu-id="f1dad-107">This entity describes the skills of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f1dad-108">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="f1dad-108">JSON representation</span></span>

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="f1dad-109">الخصائص</span><span class="sxs-lookup"><span data-stu-id="f1dad-109">Properties</span></span>

| <span data-ttu-id="f1dad-110">الخاصية</span><span class="sxs-lookup"><span data-stu-id="f1dad-110">Property</span></span><br><span data-ttu-id="f1dad-111">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="f1dad-111">**Physical name**</span></span><br><span data-ttu-id="f1dad-112">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="f1dad-112">**_Type_**</span></span> | <span data-ttu-id="f1dad-113">استخدام</span><span class="sxs-lookup"><span data-stu-id="f1dad-113">Use</span></span> | <span data-ttu-id="f1dad-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="f1dad-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f1dad-115">**معرف كيان مهارة الشخص**</span><span class="sxs-lookup"><span data-stu-id="f1dad-115">**Person Skill Entity ID**</span></span><br><span data-ttu-id="f1dad-116">mshr_hcmpersonskillentityid</span><span class="sxs-lookup"><span data-stu-id="f1dad-116">mshr_hcmpersonskillentityid</span></span><br><span data-ttu-id="f1dad-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f1dad-117">*GUID*</span></span> | <span data-ttu-id="f1dad-118">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-118">Read-only</span></span><br><span data-ttu-id="f1dad-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-119">Required</span></span> | <span data-ttu-id="f1dad-120">معرف فريد منشأ بواسطة النظام لسجل الكيان.</span><span class="sxs-lookup"><span data-stu-id="f1dad-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="f1dad-121">**رقم الطرف**</span><span class="sxs-lookup"><span data-stu-id="f1dad-121">**Party Number**</span></span><br><span data-ttu-id="f1dad-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="f1dad-122">mshr_partynumber</span></span><br><span data-ttu-id="f1dad-123">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-123">*String*</span></span> | <span data-ttu-id="f1dad-124">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-124">Read/write</span></span><br><span data-ttu-id="f1dad-125">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-125">Required</span></span> |   <span data-ttu-id="f1dad-126">معرف سجل الطرف المرتبط (الشخص).</span><span class="sxs-lookup"><span data-stu-id="f1dad-126">The ID of the associated party (person) record.</span></span> |
| <span data-ttu-id="f1dad-127">**قيمة معرف الشخص**</span><span class="sxs-lookup"><span data-stu-id="f1dad-127">**Person ID Value**</span></span><br><span data-ttu-id="f1dad-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="f1dad-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="f1dad-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f1dad-129">*GUID*</span></span> | <span data-ttu-id="f1dad-130">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-130">Read-only</span></span><br><span data-ttu-id="f1dad-131">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-131">Required</span></span><br><span data-ttu-id="f1dad-132">المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="f1dad-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="f1dad-133">المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص).</span><span class="sxs-lookup"><span data-stu-id="f1dad-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="f1dad-134">**مصدر الشهادة**</span><span class="sxs-lookup"><span data-stu-id="f1dad-134">**Certifier**</span></span><br><span data-ttu-id="f1dad-135">mshr_certifier</span><span class="sxs-lookup"><span data-stu-id="f1dad-135">mshr_certifier</span></span><br><span data-ttu-id="f1dad-136">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-136">*String*</span></span> | <span data-ttu-id="f1dad-137">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-137">Read/write</span></span><br><span data-ttu-id="f1dad-138">اختياري</span><span class="sxs-lookup"><span data-stu-id="f1dad-138">Optional</span></span> | <span data-ttu-id="f1dad-139">رقم الموظف للعامل الذي قام باعتماد هذه المهارة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-139">The personnel number of the worker who certified this skill.</span></span> |
| <span data-ttu-id="f1dad-140">**قيمة معرف مصدر الشهادة**</span><span class="sxs-lookup"><span data-stu-id="f1dad-140">**Certifier ID Value**</span></span><br><span data-ttu-id="f1dad-141">_mshr_fk_certifier_id_value</span><span class="sxs-lookup"><span data-stu-id="f1dad-141">_mshr_fk_certifier_id_value</span></span><br><span data-ttu-id="f1dad-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f1dad-142">*GUID*</span></span> | <span data-ttu-id="f1dad-143">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-143">Read-only</span></span><br><span data-ttu-id="f1dad-144">اختياري</span><span class="sxs-lookup"><span data-stu-id="f1dad-144">Optional</span></span><br><span data-ttu-id="f1dad-145">المفتاح الخارجي mshr_hcmworkerentityid لـ mshr_hcmworkerentity</span><span class="sxs-lookup"><span data-stu-id="f1dad-145">Foreign key: mshr_hcmworkerentityid of mshr_hcmworkerentity</span></span> | <span data-ttu-id="f1dad-146">المعرف الفريد الذي تم إنشاؤه بواسطة النظام لسجل العامل للعامل الذي قام باعتماد المهارة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-146">System-generated unique identifier of the worker record for the worker who certified the skill.</span></span> |
| <span data-ttu-id="f1dad-147">**معرف المهارة**</span><span class="sxs-lookup"><span data-stu-id="f1dad-147">**Skill ID**</span></span><br><span data-ttu-id="f1dad-148">mshr_skillid</span><span class="sxs-lookup"><span data-stu-id="f1dad-148">mshr_skillid</span></span><br><span data-ttu-id="f1dad-149">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-149">*String*</span></span> | <span data-ttu-id="f1dad-150">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-150">Read/write</span></span><br><span data-ttu-id="f1dad-151">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-151">Required</span></span> | <span data-ttu-id="f1dad-152">معرف المهارة المحددة في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="f1dad-152">The identifier of the skill defined in Human Resources.</span></span> |
| <span data-ttu-id="f1dad-153">**قيمة معرف المهارة**</span><span class="sxs-lookup"><span data-stu-id="f1dad-153">**Skill ID Value**</span></span><br><span data-ttu-id="f1dad-154">_mshr_fk_skill_id_value</span><span class="sxs-lookup"><span data-stu-id="f1dad-154">_mshr_fk_skill_id_value</span></span><br><span data-ttu-id="f1dad-155">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f1dad-155">*GUID*</span></span> | <span data-ttu-id="f1dad-156">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-156">Read-only</span></span><br><span data-ttu-id="f1dad-157">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-157">Required</span></span><br><span data-ttu-id="f1dad-158">المفتاح الخارجي: mshr_hcmskillentityid of mshr_hcmskillentity</span><span class="sxs-lookup"><span data-stu-id="f1dad-158">Foreign key: mshr_hcmskillentityid of mshr_hcmskillentity</span></span> | <span data-ttu-id="f1dad-159">المعرف الذي تم إنشاؤه بواسطة النظام للمهارة المحددة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-159">The system-generated identifier of the selected skill.</span></span> |
| <span data-ttu-id="f1dad-160">**سنوات الخبرة**</span><span class="sxs-lookup"><span data-stu-id="f1dad-160">**Years of Experience**</span></span><br><span data-ttu-id="f1dad-161">mshr_yearsofexperience</span><span class="sxs-lookup"><span data-stu-id="f1dad-161">mshr_yearsofexperience</span></span><br><span data-ttu-id="f1dad-162">*عشري*</span><span class="sxs-lookup"><span data-stu-id="f1dad-162">*Decimal*</span></span> | <span data-ttu-id="f1dad-163">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-163">Read/write</span></span><br><span data-ttu-id="f1dad-164">اختياري</span><span class="sxs-lookup"><span data-stu-id="f1dad-164">Optional</span></span> | <span data-ttu-id="f1dad-165">سنوات الخبرة التي يتمتع بها المرشح في هذه المهارة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-165">The years of experience the candidate has in this skill.</span></span> |
| <span data-ttu-id="f1dad-166">**معرف التقييم**</span><span class="sxs-lookup"><span data-stu-id="f1dad-166">**Rating ID**</span></span><br><span data-ttu-id="f1dad-167">mshr_ratingid</span><span class="sxs-lookup"><span data-stu-id="f1dad-167">mshr_ratingid</span></span><br><span data-ttu-id="f1dad-168">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-168">*String*</span></span> | <span data-ttu-id="f1dad-169">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-169">Read/write</span></span><br><span data-ttu-id="f1dad-170">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-170">Required</span></span> | <span data-ttu-id="f1dad-171">نوع مقياس التقييم.</span><span class="sxs-lookup"><span data-stu-id="f1dad-171">The rating scale type.</span></span> <span data-ttu-id="f1dad-172">بالنسبة لهذا الكيان، تكون القيمة **مهارات**.</span><span class="sxs-lookup"><span data-stu-id="f1dad-172">For this entity, the value is **Skills**.</span></span> |
| <span data-ttu-id="f1dad-173">**نوع المستوى**</span><span class="sxs-lookup"><span data-stu-id="f1dad-173">**Level Type**</span></span><br><span data-ttu-id="f1dad-174">mshr_leveltype</span><span class="sxs-lookup"><span data-stu-id="f1dad-174">mshr_leveltype</span></span><br><span data-ttu-id="f1dad-175">*مجموعة خيارات mshr_hrmskillleveltype*</span><span class="sxs-lookup"><span data-stu-id="f1dad-175">*mshr_hrmskillleveltype option set*</span></span> | <span data-ttu-id="f1dad-176">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-176">Read/write</span></span><br><span data-ttu-id="f1dad-177">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-177">Required</span></span> | <span data-ttu-id="f1dad-178">تصنيف نوع للمستوى المعين للمهارة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-178">A type categorization for the level assigned to the skill.</span></span> |
| <span data-ttu-id="f1dad-179">**معرف المستوى**</span><span class="sxs-lookup"><span data-stu-id="f1dad-179">**Level ID**</span></span><br><span data-ttu-id="f1dad-180">mshr_levelid</span><span class="sxs-lookup"><span data-stu-id="f1dad-180">mshr_levelid</span></span><br><span data-ttu-id="f1dad-181">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-181">*String*</span></span> | <span data-ttu-id="f1dad-182">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-182">Read/write</span></span><br><span data-ttu-id="f1dad-183">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-183">Required</span></span> | <span data-ttu-id="f1dad-184">معرف مستوى التقييم الخاص بالمرشح لهذه المهارة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-184">The ID of the Rating Level the candidate has for this skill.</span></span> |
| <span data-ttu-id="f1dad-185">**قيم معرف مستوى التقييم**</span><span class="sxs-lookup"><span data-stu-id="f1dad-185">**Rating Level ID Value**</span></span><br><span data-ttu-id="f1dad-186">_mshr_fk_ratinglevel_id_value</span><span class="sxs-lookup"><span data-stu-id="f1dad-186">_mshr_fk_ratinglevel_id_value</span></span><br><span data-ttu-id="f1dad-187">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f1dad-187">*GUID*</span></span> | <span data-ttu-id="f1dad-188">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-188">Read-only</span></span><br><span data-ttu-id="f1dad-189">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-189">Required</span></span><br><span data-ttu-id="f1dad-190">المفتاح الخارجي: mshr_hcmratinglevelentityid لـ mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="f1dad-190">Foreign key: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity</span></span> | <span data-ttu-id="f1dad-191">المعرف الذي تم إنشاؤه بواسطة النظام لمستوى التقييم.</span><span class="sxs-lookup"><span data-stu-id="f1dad-191">The system-generated identifier of the rating level.</span></span> |
| <span data-ttu-id="f1dad-192">**تاريخ المستوى**</span><span class="sxs-lookup"><span data-stu-id="f1dad-192">**Level Date**</span></span><br><span data-ttu-id="f1dad-193">mshr_leveldate</span><span class="sxs-lookup"><span data-stu-id="f1dad-193">mshr_leveldate</span></span><br><span data-ttu-id="f1dad-194">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="f1dad-194">*Datetime*</span></span> | <span data-ttu-id="f1dad-195">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-195">Read/write</span></span><br><span data-ttu-id="f1dad-196">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-196">Required</span></span> | <span data-ttu-id="f1dad-197">التاريخ الذي تم فيه تصنيف المرشح في المهارة.</span><span class="sxs-lookup"><span data-stu-id="f1dad-197">The date at which the candidate was rated in the skill.</span></span> |
| <span data-ttu-id="f1dad-198">**مسؤول اختبار مستوى التقييم**</span><span class="sxs-lookup"><span data-stu-id="f1dad-198">**Rating Level Examiner**</span></span><br><span data-ttu-id="f1dad-199">mshr_ratinglevelexaminer</span><span class="sxs-lookup"><span data-stu-id="f1dad-199">mshr_ratinglevelexaminer</span></span><br><span data-ttu-id="f1dad-200">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-200">*String*</span></span> | <span data-ttu-id="f1dad-201">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-201">Read/write</span></span><br><span data-ttu-id="f1dad-202">اختياري</span><span class="sxs-lookup"><span data-stu-id="f1dad-202">Optional</span></span> | <span data-ttu-id="f1dad-203">رقم الموظف للعامل الذي قام بتقييم المرشح.</span><span class="sxs-lookup"><span data-stu-id="f1dad-203">The personnel number of the worker who rated the candidate.</span></span> |
| <span data-ttu-id="f1dad-204">**قيم معرف مسؤول اختبار مستوى التقييم**</span><span class="sxs-lookup"><span data-stu-id="f1dad-204">**Rating Level Examiner ID Value**</span></span><br><span data-ttu-id="f1dad-205">_mshr_fk_ratinglevelexaminer_id_value</span><span class="sxs-lookup"><span data-stu-id="f1dad-205">_mshr_fk_ratinglevelexaminer_id_value</span></span><br><span data-ttu-id="f1dad-206">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f1dad-206">*GUID*</span></span> | <span data-ttu-id="f1dad-207">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-207">Read-only</span></span><br><span data-ttu-id="f1dad-208">اختياري</span><span class="sxs-lookup"><span data-stu-id="f1dad-208">Optional</span></span><br><span data-ttu-id="f1dad-209">المفتاح الخارجي mshr_hcmworkerentityid لـ mshr_hcmworkerentity</span><span class="sxs-lookup"><span data-stu-id="f1dad-209">Foreign key: mshr_hcmworkerentityid of mshr_hcmworkerentity</span></span> | <span data-ttu-id="f1dad-210">المعرف المنشأ بواسطة النظام للعامل الذي قام باختبار مستوى مهارة المرشح.</span><span class="sxs-lookup"><span data-stu-id="f1dad-210">The system-generated identifier of the worker who examined the candidate’s skill level.</span></span> |
| <span data-ttu-id="f1dad-211">**تم التحقق من الصحة**</span><span class="sxs-lookup"><span data-stu-id="f1dad-211">**Verified**</span></span><br><span data-ttu-id="f1dad-212">mshr_verified</span><span class="sxs-lookup"><span data-stu-id="f1dad-212">mshr_verified</span></span><br><span data-ttu-id="f1dad-213">*مجموعة خيارات mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="f1dad-213">*mshr_noyes option set*</span></span> | <span data-ttu-id="f1dad-214">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="f1dad-214">Read/write</span></span><br><span data-ttu-id="f1dad-215">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-215">Required</span></span> | <span data-ttu-id="f1dad-216">يشير إلى إذا تم التحقق من مستوى المهارة الذي تم تقييمه أم لا.</span><span class="sxs-lookup"><span data-stu-id="f1dad-216">Indicates whether the assessed skill level has been verified.</span></span> |
| <span data-ttu-id="f1dad-217">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="f1dad-217">**Primary Field**</span></span><br><span data-ttu-id="f1dad-218">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f1dad-218">mshr_primaryfield</span></span><br><span data-ttu-id="f1dad-219">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="f1dad-219">*String*</span></span> | <span data-ttu-id="f1dad-220">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="f1dad-220">Read-only</span></span><br><span data-ttu-id="f1dad-221">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f1dad-221">Required</span></span> | <span data-ttu-id="f1dad-222">حقل المطلوب استخدامه كمعرف لسجل الكيان.</span><span class="sxs-lookup"><span data-stu-id="f1dad-222">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="f1dad-223">مجموعة رقم الطرف ونوع المستوى ومعرف المهارة وتاريخ المستوى.</span><span class="sxs-lookup"><span data-stu-id="f1dad-223">Combination of party number, level type, skill ID, and level date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f1dad-224">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f1dad-224">See also</span></span>

[<span data-ttu-id="f1dad-225">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="f1dad-225">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f1dad-226">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="f1dad-226">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
