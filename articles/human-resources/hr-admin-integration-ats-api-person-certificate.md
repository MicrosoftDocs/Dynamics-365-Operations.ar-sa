---
title: شهادة الشخص
description: يصف هذا الموضوع كيان شهادة الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055186"
---
# <a name="person-certificate"></a><span data-ttu-id="589bf-103">شهادة الشخص</span><span class="sxs-lookup"><span data-stu-id="589bf-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="589bf-104">يصف هذا الموضوع كيان شهادة الشخص لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="589bf-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="589bf-105">الاسم الفعلي: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="589bf-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="589bf-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="589bf-106">Description</span></span>

<span data-ttu-id="589bf-107">يصف هذا الكيان الشهادات المهنية لأحد المرشحين.</span><span class="sxs-lookup"><span data-stu-id="589bf-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="589bf-108">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="589bf-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="589bf-109">الخصائص</span><span class="sxs-lookup"><span data-stu-id="589bf-109">Properties</span></span>

| <span data-ttu-id="589bf-110">الخاصية</span><span class="sxs-lookup"><span data-stu-id="589bf-110">Property</span></span><br><span data-ttu-id="589bf-111">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="589bf-111">**Physical name**</span></span><br><span data-ttu-id="589bf-112">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="589bf-112">**_Type_**</span></span> | <span data-ttu-id="589bf-113">استخدام</span><span class="sxs-lookup"><span data-stu-id="589bf-113">Use</span></span> | <span data-ttu-id="589bf-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="589bf-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="589bf-115">**معرف كيان شهادة الشخص**</span><span class="sxs-lookup"><span data-stu-id="589bf-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="589bf-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="589bf-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="589bf-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="589bf-117">*GUID*</span></span> | <span data-ttu-id="589bf-118">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="589bf-118">Read-only</span></span><br><span data-ttu-id="589bf-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-119">Required</span></span> | <span data-ttu-id="589bf-120">معرف فريد منشأ بواسطة النظام لسجل كيان شهادة الشخص.</span><span class="sxs-lookup"><span data-stu-id="589bf-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="589bf-121">**رقم الطرف**</span><span class="sxs-lookup"><span data-stu-id="589bf-121">**Party Number**</span></span><br><span data-ttu-id="589bf-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="589bf-122">mshr_partynumber</span></span><br><span data-ttu-id="589bf-123">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="589bf-123">*String*</span></span> | <span data-ttu-id="589bf-124">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="589bf-124">Read/write</span></span><br><span data-ttu-id="589bf-125">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-125">Required</span></span> | <span data-ttu-id="589bf-126">معرف الطرف (الشخص) للمرشح.</span><span class="sxs-lookup"><span data-stu-id="589bf-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="589bf-127">**قيمة معرف الشخص**</span><span class="sxs-lookup"><span data-stu-id="589bf-127">**Person ID Value**</span></span><br><span data-ttu-id="589bf-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="589bf-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="589bf-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="589bf-129">*GUID*</span></span> | <span data-ttu-id="589bf-130">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="589bf-130">Read-only</span></span><br><span data-ttu-id="589bf-131">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-131">Required</span></span><br><span data-ttu-id="589bf-132">المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="589bf-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="589bf-133">المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص).</span><span class="sxs-lookup"><span data-stu-id="589bf-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="589bf-134">**معرف نوع الشهادة**</span><span class="sxs-lookup"><span data-stu-id="589bf-134">**Certificate Type ID**</span></span><br><span data-ttu-id="589bf-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="589bf-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="589bf-136">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="589bf-136">*String*</span></span> | <span data-ttu-id="589bf-137">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="589bf-137">Read/write</span></span><br><span data-ttu-id="589bf-138">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-138">Required</span></span> |  <span data-ttu-id="589bf-139">معرف نوع الشهادة المحدد في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="589bf-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="589bf-140">**قيمة معرف نوع الشهادة**</span><span class="sxs-lookup"><span data-stu-id="589bf-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="589bf-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="589bf-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="589bf-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="589bf-142">*GUID*</span></span> | <span data-ttu-id="589bf-143">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="589bf-143">Read-only</span></span><br><span data-ttu-id="589bf-144">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-144">Required</span></span><br><span data-ttu-id="589bf-145">المفتاح الخارجي: mshr_hcmcertificatetypeentityid لـ mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="589bf-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="589bf-146">معرف فريد منشأ بواسطة النظام لنوع الشهادة في الكيان المقترن.</span><span class="sxs-lookup"><span data-stu-id="589bf-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="589bf-147">**تاريخ البدء**</span><span class="sxs-lookup"><span data-stu-id="589bf-147">**Start Date**</span></span><br><span data-ttu-id="589bf-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="589bf-148">mshr_startdate</span></span><br><span data-ttu-id="589bf-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="589bf-149">*Datetime*</span></span> | <span data-ttu-id="589bf-150">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="589bf-150">Read/write</span></span><br><span data-ttu-id="589bf-151">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-151">Required</span></span> | <span data-ttu-id="589bf-152">التاريخ الذي تم فيه إصدار الشهادة.</span><span class="sxs-lookup"><span data-stu-id="589bf-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="589bf-153">**تاريخ النهاية**</span><span class="sxs-lookup"><span data-stu-id="589bf-153">**End Date**</span></span><br><span data-ttu-id="589bf-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="589bf-154">mshr_enddate</span></span><br><span data-ttu-id="589bf-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="589bf-155">*Datetime*</span></span> | <span data-ttu-id="589bf-156">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="589bf-156">Read/write</span></span><br><span data-ttu-id="589bf-157">اختياري</span><span class="sxs-lookup"><span data-stu-id="589bf-157">Optional</span></span> | <span data-ttu-id="589bf-158">التاريخ الذي ستنتهي فيه الشهادة.</span><span class="sxs-lookup"><span data-stu-id="589bf-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="589bf-159">**الملاحظات**</span><span class="sxs-lookup"><span data-stu-id="589bf-159">**Notes**</span></span><br><span data-ttu-id="589bf-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="589bf-160">mshr_notes</span></span><br><span data-ttu-id="589bf-161">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="589bf-161">*String*</span></span> | <span data-ttu-id="589bf-162">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="589bf-162">Read/write</span></span><br><span data-ttu-id="589bf-163">اختياري</span><span class="sxs-lookup"><span data-stu-id="589bf-163">Optional</span></span> | <span data-ttu-id="589bf-164">ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف.</span><span class="sxs-lookup"><span data-stu-id="589bf-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="589bf-165">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="589bf-165">**Primary Field**</span></span><br><span data-ttu-id="589bf-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="589bf-166">mshr_primaryfield</span></span><br><span data-ttu-id="589bf-167">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="589bf-167">*String*</span></span> | <span data-ttu-id="589bf-168">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="589bf-168">Read-only</span></span><br><span data-ttu-id="589bf-169">مطلوب</span><span class="sxs-lookup"><span data-stu-id="589bf-169">Required</span></span> |  <span data-ttu-id="589bf-170">حقل المطلوب استخدامه كمعرف لسجل الكيان.</span><span class="sxs-lookup"><span data-stu-id="589bf-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="589bf-171">مجموعة رقم الطرف ومعرف نوع الشهادة وتاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="589bf-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="589bf-172">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="589bf-172">See also</span></span>

[<span data-ttu-id="589bf-173">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="589bf-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="589bf-174">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="589bf-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]