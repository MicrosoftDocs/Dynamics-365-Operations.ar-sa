---
title: مراقبة الأشخاص
description: يصف هذا الموضوع كيان مراقبة الشخص لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059270"
---
# <a name="person-screening"></a><span data-ttu-id="6d4bf-103">مراقبة الأشخاص</span><span class="sxs-lookup"><span data-stu-id="6d4bf-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6d4bf-104">يصف هذا الموضوع كيان مراقبة الشخص لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6d4bf-105">الاسم الفعلي: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="6d4bf-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="6d4bf-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="6d4bf-106">Description</span></span>

<span data-ttu-id="6d4bf-107">يصف هذا الكيان عمليات المراقبة لمرشح الذي نجح أو يجب أن ينجح في التوظيف.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6d4bf-108">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="6d4bf-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="6d4bf-109">الخصائص</span><span class="sxs-lookup"><span data-stu-id="6d4bf-109">Properties</span></span>

| <span data-ttu-id="6d4bf-110">الخاصية</span><span class="sxs-lookup"><span data-stu-id="6d4bf-110">Property</span></span><br><span data-ttu-id="6d4bf-111">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-111">**Physical name**</span></span><br><span data-ttu-id="6d4bf-112">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-112">**_Type_**</span></span> | <span data-ttu-id="6d4bf-113">استخدام</span><span class="sxs-lookup"><span data-stu-id="6d4bf-113">Use</span></span> | <span data-ttu-id="6d4bf-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="6d4bf-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6d4bf-115">**معرف كيان مراقبة الشخص**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="6d4bf-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="6d4bf-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="6d4bf-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-117">*GUID*</span></span> | <span data-ttu-id="6d4bf-118">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d4bf-118">Read-only</span></span><br><span data-ttu-id="6d4bf-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-119">Required</span></span><br><span data-ttu-id="6d4bf-120">منشأ بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="6d4bf-120">System-generated</span></span> | <span data-ttu-id="6d4bf-121">المعرف الأساسي الفريد لسجل مراقبة الشخص.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="6d4bf-122">**رقم الطرف**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-122">**Party Number**</span></span><br><span data-ttu-id="6d4bf-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="6d4bf-123">mshr_partynumber</span></span><br><span data-ttu-id="6d4bf-124">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-124">*String*</span></span> | <span data-ttu-id="6d4bf-125">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="6d4bf-125">Read/write</span></span><br><span data-ttu-id="6d4bf-126">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-126">Required</span></span> | <span data-ttu-id="6d4bf-127">رقم الطرف (الشخص) المقترن بالمرشح.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="6d4bf-128">**قيمة معرف الشخص**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-128">**Person ID Value**</span></span><br><span data-ttu-id="6d4bf-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="6d4bf-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="6d4bf-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-130">*GUID*</span></span> | <span data-ttu-id="6d4bf-131">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d4bf-131">Read-only</span></span><br><span data-ttu-id="6d4bf-132">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-132">Required</span></span><br><span data-ttu-id="6d4bf-133">المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="6d4bf-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="6d4bf-134">المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص).</span><span class="sxs-lookup"><span data-stu-id="6d4bf-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="6d4bf-135">**معرف نوع المراقبة**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-135">**Screening Type ID**</span></span><br><span data-ttu-id="6d4bf-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="6d4bf-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="6d4bf-137">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-137">*String*</span></span> | <span data-ttu-id="6d4bf-138">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="6d4bf-138">Read/write</span></span><br><span data-ttu-id="6d4bf-139">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-139">Required</span></span><br><span data-ttu-id="6d4bf-140">المفتاح الخارجي: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="6d4bf-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="6d4bf-141">معرف نوع المراقبة المحدد في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="6d4bf-142">**قيمة معرف نوع المراقبة**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="6d4bf-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="6d4bf-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="6d4bf-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-144">*GUID*</span></span> | <span data-ttu-id="6d4bf-145">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d4bf-145">Read-only</span></span><br><span data-ttu-id="6d4bf-146">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-146">Required</span></span><br><span data-ttu-id="6d4bf-147">المفتاح الخارجي: mshr_hcmscreeningtypeentityid لـ mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="6d4bf-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="6d4bf-148">معرف فريد منشأ بواسطة النظام لسجل نوع المراقبة في الكيان المقترن.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="6d4bf-149">**مطلوب من**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-149">**Required By**</span></span><br><span data-ttu-id="6d4bf-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="6d4bf-150">mshr_requiredby</span></span><br><span data-ttu-id="6d4bf-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-151">*Datetime*</span></span> | <span data-ttu-id="6d4bf-152">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="6d4bf-152">Read/write</span></span><br><span data-ttu-id="6d4bf-153">اختياري</span><span class="sxs-lookup"><span data-stu-id="6d4bf-153">Optional</span></span> | <span data-ttu-id="6d4bf-154">التاريخ المطلوب فيه إكمال عملية المراقبة.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="6d4bf-155">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-155">**Status**</span></span><br><span data-ttu-id="6d4bf-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="6d4bf-156">mshr_status</span></span><br><span data-ttu-id="6d4bf-157">*مجموعة خيارات mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="6d4bf-158">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="6d4bf-158">Read/write</span></span><br><span data-ttu-id="6d4bf-159">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-159">Required</span></span> | <span data-ttu-id="6d4bf-160">يوفر حالة المرشح لعملية المراقبة.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="6d4bf-161">**تاريخ الإكمال**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-161">**Completed Date**</span></span><br><span data-ttu-id="6d4bf-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="6d4bf-162">mshr_completeddate</span></span><br><span data-ttu-id="6d4bf-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-163">*Datetime*</span></span> | <span data-ttu-id="6d4bf-164">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="6d4bf-164">Read/write</span></span><br><span data-ttu-id="6d4bf-165">اختياري</span><span class="sxs-lookup"><span data-stu-id="6d4bf-165">Optional</span></span> | <span data-ttu-id="6d4bf-166">تاريخ اكتمال عملية المراقبة.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="6d4bf-167">**الملاحظات**</span><span class="sxs-lookup"><span data-stu-id="6d4bf-167">**Notes**</span></span><br><span data-ttu-id="6d4bf-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="6d4bf-168">mshr_note</span></span><br><span data-ttu-id="6d4bf-169">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d4bf-169">*String*</span></span> | <span data-ttu-id="6d4bf-170">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="6d4bf-170">Read/write</span></span><br><span data-ttu-id="6d4bf-171">اختياري</span><span class="sxs-lookup"><span data-stu-id="6d4bf-171">Optional</span></span> | <span data-ttu-id="6d4bf-172">ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف.</span><span class="sxs-lookup"><span data-stu-id="6d4bf-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6d4bf-173">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="6d4bf-173">See also</span></span>

[<span data-ttu-id="6d4bf-174">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="6d4bf-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="6d4bf-175">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="6d4bf-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]