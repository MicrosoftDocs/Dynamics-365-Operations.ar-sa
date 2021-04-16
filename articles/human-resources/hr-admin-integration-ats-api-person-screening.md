---
title: مراقبة الأشخاص
description: يصف هذا الموضوع كيان مراقبة الشخص لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798023"
---
# <a name="person-screening"></a><span data-ttu-id="b48cd-103">مراقبة الأشخاص</span><span class="sxs-lookup"><span data-stu-id="b48cd-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b48cd-104">يصف هذا الموضوع كيان مراقبة الشخص لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b48cd-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b48cd-105">الاسم الفعلي: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="b48cd-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="b48cd-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="b48cd-106">Description</span></span>

<span data-ttu-id="b48cd-107">يصف هذا الكيان عمليات المراقبة لمرشح الذي نجح أو يجب أن ينجح في التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b48cd-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b48cd-108">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="b48cd-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="b48cd-109">الخصائص</span><span class="sxs-lookup"><span data-stu-id="b48cd-109">Properties</span></span>

| <span data-ttu-id="b48cd-110">الخاصية</span><span class="sxs-lookup"><span data-stu-id="b48cd-110">Property</span></span><br><span data-ttu-id="b48cd-111">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="b48cd-111">**Physical name**</span></span><br><span data-ttu-id="b48cd-112">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="b48cd-112">**_Type_**</span></span> | <span data-ttu-id="b48cd-113">استخدام</span><span class="sxs-lookup"><span data-stu-id="b48cd-113">Use</span></span> | <span data-ttu-id="b48cd-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="b48cd-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b48cd-115">**معرف كيان مراقبة الشخص**</span><span class="sxs-lookup"><span data-stu-id="b48cd-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="b48cd-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="b48cd-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="b48cd-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b48cd-117">*GUID*</span></span> | <span data-ttu-id="b48cd-118">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="b48cd-118">Read-only</span></span><br><span data-ttu-id="b48cd-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="b48cd-119">Required</span></span><br><span data-ttu-id="b48cd-120">منشأ بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="b48cd-120">System-generated</span></span> | <span data-ttu-id="b48cd-121">المعرف الأساسي الفريد لسجل مراقبة الشخص.</span><span class="sxs-lookup"><span data-stu-id="b48cd-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="b48cd-122">**رقم الطرف**</span><span class="sxs-lookup"><span data-stu-id="b48cd-122">**Party Number**</span></span><br><span data-ttu-id="b48cd-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="b48cd-123">mshr_partynumber</span></span><br><span data-ttu-id="b48cd-124">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="b48cd-124">*String*</span></span> | <span data-ttu-id="b48cd-125">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="b48cd-125">Read/write</span></span><br><span data-ttu-id="b48cd-126">مطلوب</span><span class="sxs-lookup"><span data-stu-id="b48cd-126">Required</span></span> | <span data-ttu-id="b48cd-127">رقم الطرف (الشخص) المقترن بالمرشح.</span><span class="sxs-lookup"><span data-stu-id="b48cd-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="b48cd-128">**قيمة معرف الشخص**</span><span class="sxs-lookup"><span data-stu-id="b48cd-128">**Person ID Value**</span></span><br><span data-ttu-id="b48cd-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="b48cd-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="b48cd-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b48cd-130">*GUID*</span></span> | <span data-ttu-id="b48cd-131">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="b48cd-131">Read-only</span></span><br><span data-ttu-id="b48cd-132">مطلوب</span><span class="sxs-lookup"><span data-stu-id="b48cd-132">Required</span></span><br><span data-ttu-id="b48cd-133">المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="b48cd-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="b48cd-134">المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص).</span><span class="sxs-lookup"><span data-stu-id="b48cd-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="b48cd-135">**معرف نوع المراقبة**</span><span class="sxs-lookup"><span data-stu-id="b48cd-135">**Screening Type ID**</span></span><br><span data-ttu-id="b48cd-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="b48cd-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="b48cd-137">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="b48cd-137">*String*</span></span> | <span data-ttu-id="b48cd-138">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="b48cd-138">Read/write</span></span><br><span data-ttu-id="b48cd-139">مطلوب</span><span class="sxs-lookup"><span data-stu-id="b48cd-139">Required</span></span><br><span data-ttu-id="b48cd-140">المفتاح الخارجي: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="b48cd-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="b48cd-141">معرف نوع المراقبة المحدد في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="b48cd-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="b48cd-142">**قيمة معرف نوع المراقبة**</span><span class="sxs-lookup"><span data-stu-id="b48cd-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="b48cd-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="b48cd-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="b48cd-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b48cd-144">*GUID*</span></span> | <span data-ttu-id="b48cd-145">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="b48cd-145">Read-only</span></span><br><span data-ttu-id="b48cd-146">مطلوب</span><span class="sxs-lookup"><span data-stu-id="b48cd-146">Required</span></span><br><span data-ttu-id="b48cd-147">المفتاح الخارجي: mshr_hcmscreeningtypeentityid لـ mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="b48cd-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="b48cd-148">معرف فريد منشأ بواسطة النظام لسجل نوع المراقبة في الكيان المقترن.</span><span class="sxs-lookup"><span data-stu-id="b48cd-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="b48cd-149">**مطلوب من**</span><span class="sxs-lookup"><span data-stu-id="b48cd-149">**Required By**</span></span><br><span data-ttu-id="b48cd-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="b48cd-150">mshr_requiredby</span></span><br><span data-ttu-id="b48cd-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="b48cd-151">*Datetime*</span></span> | <span data-ttu-id="b48cd-152">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="b48cd-152">Read/write</span></span><br><span data-ttu-id="b48cd-153">اختياري</span><span class="sxs-lookup"><span data-stu-id="b48cd-153">Optional</span></span> | <span data-ttu-id="b48cd-154">التاريخ المطلوب فيه إكمال عملية المراقبة.</span><span class="sxs-lookup"><span data-stu-id="b48cd-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="b48cd-155">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="b48cd-155">**Status**</span></span><br><span data-ttu-id="b48cd-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="b48cd-156">mshr_status</span></span><br><span data-ttu-id="b48cd-157">*مجموعة خيارات mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="b48cd-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="b48cd-158">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="b48cd-158">Read/write</span></span><br><span data-ttu-id="b48cd-159">مطلوب</span><span class="sxs-lookup"><span data-stu-id="b48cd-159">Required</span></span> | <span data-ttu-id="b48cd-160">يوفر حالة المرشح لعملية المراقبة.</span><span class="sxs-lookup"><span data-stu-id="b48cd-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="b48cd-161">**تاريخ الإكمال**</span><span class="sxs-lookup"><span data-stu-id="b48cd-161">**Completed Date**</span></span><br><span data-ttu-id="b48cd-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="b48cd-162">mshr_completeddate</span></span><br><span data-ttu-id="b48cd-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="b48cd-163">*Datetime*</span></span> | <span data-ttu-id="b48cd-164">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="b48cd-164">Read/write</span></span><br><span data-ttu-id="b48cd-165">اختياري</span><span class="sxs-lookup"><span data-stu-id="b48cd-165">Optional</span></span> | <span data-ttu-id="b48cd-166">تاريخ اكتمال عملية المراقبة.</span><span class="sxs-lookup"><span data-stu-id="b48cd-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="b48cd-167">**الملاحظات**</span><span class="sxs-lookup"><span data-stu-id="b48cd-167">**Notes**</span></span><br><span data-ttu-id="b48cd-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="b48cd-168">mshr_note</span></span><br><span data-ttu-id="b48cd-169">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="b48cd-169">*String*</span></span> | <span data-ttu-id="b48cd-170">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="b48cd-170">Read/write</span></span><br><span data-ttu-id="b48cd-171">اختياري</span><span class="sxs-lookup"><span data-stu-id="b48cd-171">Optional</span></span> | <span data-ttu-id="b48cd-172">ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b48cd-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b48cd-173">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b48cd-173">See also</span></span>

[<span data-ttu-id="b48cd-174">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="b48cd-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b48cd-175">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="b48cd-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]