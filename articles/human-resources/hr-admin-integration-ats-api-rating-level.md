---
title: مستوى التقييم
description: يصف هذا الموضوع كيان مستوى التقييم لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054826"
---
# <a name="rating-level"></a><span data-ttu-id="acb6e-103">مستوى التقييم</span><span class="sxs-lookup"><span data-stu-id="acb6e-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="acb6e-104">يصف هذا الموضوع كيان مستوى التقييم لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="acb6e-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="acb6e-105">الاسم الفعلي: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="acb6e-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="acb6e-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="acb6e-106">Description</span></span>

<span data-ttu-id="acb6e-107">يوفر هذا الكيان مستويات التقييم المتاحة للمهارات.</span><span class="sxs-lookup"><span data-stu-id="acb6e-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="acb6e-108">تنطبق مستويات التصنيف عبر كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="acb6e-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="acb6e-109">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="acb6e-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="acb6e-110">الخصائص</span><span class="sxs-lookup"><span data-stu-id="acb6e-110">Properties</span></span>

| <span data-ttu-id="acb6e-111">الخاصية</span><span class="sxs-lookup"><span data-stu-id="acb6e-111">Property</span></span><br><span data-ttu-id="acb6e-112">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="acb6e-112">**Physical name**</span></span><br><span data-ttu-id="acb6e-113">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="acb6e-113">**_Type_**</span></span> | <span data-ttu-id="acb6e-114">استخدام</span><span class="sxs-lookup"><span data-stu-id="acb6e-114">Use</span></span> | <span data-ttu-id="acb6e-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="acb6e-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="acb6e-116">**معرف كيان مستوى التقييم**</span><span class="sxs-lookup"><span data-stu-id="acb6e-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="acb6e-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="acb6e-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="acb6e-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="acb6e-118">*GUID*</span></span> | <span data-ttu-id="acb6e-119">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="acb6e-119">Read-only</span></span><br><span data-ttu-id="acb6e-120">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-120">Required</span></span><br><span data-ttu-id="acb6e-121">منشأ بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="acb6e-121">System-generated</span></span> | <span data-ttu-id="acb6e-122">معرف فريد منشأ بواسطة النظام للمستوى.</span><span class="sxs-lookup"><span data-stu-id="acb6e-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="acb6e-123">**معرف مستوى التقييم**</span><span class="sxs-lookup"><span data-stu-id="acb6e-123">**Rating Level ID**</span></span><br><span data-ttu-id="acb6e-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="acb6e-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="acb6e-125">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="acb6e-125">*String*</span></span> | <span data-ttu-id="acb6e-126">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="acb6e-126">Read/write</span></span><br><span data-ttu-id="acb6e-127">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-127">Required</span></span> | <span data-ttu-id="acb6e-128">معرف فريد قابل للقراءة بواسطة المستخدم للمستوى.</span><span class="sxs-lookup"><span data-stu-id="acb6e-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="acb6e-129">**معرف نموذج التقييم**</span><span class="sxs-lookup"><span data-stu-id="acb6e-129">**Rating Model ID**</span></span><br><span data-ttu-id="acb6e-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="acb6e-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="acb6e-131">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="acb6e-131">*String*</span></span> | <span data-ttu-id="acb6e-132">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="acb6e-132">Read/write</span></span><br><span data-ttu-id="acb6e-133">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-133">Required</span></span> | <span data-ttu-id="acb6e-134">نموذج التقييم الذي ينتمي إليه مستوى التقييم.</span><span class="sxs-lookup"><span data-stu-id="acb6e-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="acb6e-135">**معرف كيان نموذج التقييم**</span><span class="sxs-lookup"><span data-stu-id="acb6e-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="acb6e-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="acb6e-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="acb6e-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="acb6e-137">*GUID*</span></span> | <span data-ttu-id="acb6e-138">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="acb6e-138">Read-only</span></span><br><span data-ttu-id="acb6e-139">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-139">Required</span></span><br><span data-ttu-id="acb6e-140">المفتاح الخارجي: mshr_hcmratingmodelentityid لـ mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="acb6e-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="acb6e-141">المعرف المنشأ بواسطة النظام لنموذج التقييم الذي ينتمي إليه مستوى التقييم.</span><span class="sxs-lookup"><span data-stu-id="acb6e-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="acb6e-142">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="acb6e-142">**Description**</span></span><br><span data-ttu-id="acb6e-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="acb6e-143">mshr_description</span></span><br><span data-ttu-id="acb6e-144">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="acb6e-144">*String*</span></span> | <span data-ttu-id="acb6e-145">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="acb6e-145">Read/write</span></span><br><span data-ttu-id="acb6e-146">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-146">Required</span></span> | <span data-ttu-id="acb6e-147">الوصف الخاص بمستوى التقييم.</span><span class="sxs-lookup"><span data-stu-id="acb6e-147">The description of the rating level.</span></span> |
| <span data-ttu-id="acb6e-148">**العامل‬**</span><span class="sxs-lookup"><span data-stu-id="acb6e-148">**Factor**</span></span><br><span data-ttu-id="acb6e-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="acb6e-149">mshr_factor</span></span><br><span data-ttu-id="acb6e-150">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="acb6e-150">*Integer*</span></span> | <span data-ttu-id="acb6e-151">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="acb6e-151">Read/write</span></span><br><span data-ttu-id="acb6e-152">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-152">Required</span></span> | <span data-ttu-id="acb6e-153">العامل لمستوى التقييم.</span><span class="sxs-lookup"><span data-stu-id="acb6e-153">The factor for the rating level.</span></span> <span data-ttu-id="acb6e-154">وعندما تقوم بمقارنة الأصناف برقم مختلف لمستويات التقييم، يتم استخدام العامل لتسوية النتائج.</span><span class="sxs-lookup"><span data-stu-id="acb6e-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="acb6e-155">يجب أن تكون القيمة عددًا صحيحًا بين 0 و9.</span><span class="sxs-lookup"><span data-stu-id="acb6e-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="acb6e-156">**ملاحظة**</span><span class="sxs-lookup"><span data-stu-id="acb6e-156">**Note**</span></span><br><span data-ttu-id="acb6e-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="acb6e-157">mshr_note</span></span><br><span data-ttu-id="acb6e-158">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="acb6e-158">*String*</span></span> | <span data-ttu-id="acb6e-159">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="acb6e-159">Read/write</span></span><br><span data-ttu-id="acb6e-160">اختياري</span><span class="sxs-lookup"><span data-stu-id="acb6e-160">Optional</span></span> | <span data-ttu-id="acb6e-161">أية ملاحظات مرتبطة بمستوى التقييم.</span><span class="sxs-lookup"><span data-stu-id="acb6e-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="acb6e-162">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="acb6e-162">**Primary Field**</span></span><br><span data-ttu-id="acb6e-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="acb6e-163">mshr_primaryfield</span></span><br><span data-ttu-id="acb6e-164">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="acb6e-164">*String*</span></span> | <span data-ttu-id="acb6e-165">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="acb6e-165">Read-only</span></span><br><span data-ttu-id="acb6e-166">مطلوب</span><span class="sxs-lookup"><span data-stu-id="acb6e-166">Required</span></span> | <span data-ttu-id="acb6e-167">حقل المطلوب استخدامه كمعرف لسجل الكيان.</span><span class="sxs-lookup"><span data-stu-id="acb6e-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="acb6e-168">مجموعة معرف مستوى التقييم ومعرف نموذج التقييم.</span><span class="sxs-lookup"><span data-stu-id="acb6e-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="acb6e-169">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="acb6e-169">See also</span></span>

[<span data-ttu-id="acb6e-170">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="acb6e-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="acb6e-171">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="acb6e-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]