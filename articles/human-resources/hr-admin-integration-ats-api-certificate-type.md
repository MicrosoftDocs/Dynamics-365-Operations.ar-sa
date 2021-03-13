---
title: نوع الشهادة
description: يصف هذا الموضوع كيان نوع المرشح لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125703"
---
# <a name="certificate-type"></a><span data-ttu-id="d5f97-103">نوع الشهادة</span><span class="sxs-lookup"><span data-stu-id="d5f97-103">Certificate type</span></span>

<span data-ttu-id="d5f97-104">يصف هذا الموضوع كيان نوع المرشح لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d5f97-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d5f97-105">الاسم الفعلي: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="d5f97-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="d5f97-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="d5f97-106">Description</span></span>

<span data-ttu-id="d5f97-107">يحدد هذا الكيان قائمة أنواع الشهادات المهنية التي تم إعدادها في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="d5f97-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="d5f97-108">الكيان غير خاص بأحد الكيانات القانونية (الشركة).</span><span class="sxs-lookup"><span data-stu-id="d5f97-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="d5f97-109">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="d5f97-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="d5f97-110">الخصائص</span><span class="sxs-lookup"><span data-stu-id="d5f97-110">Properties</span></span>

| <span data-ttu-id="d5f97-111">الخاصية</span><span class="sxs-lookup"><span data-stu-id="d5f97-111">Property</span></span><br><span data-ttu-id="d5f97-112">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="d5f97-112">**Physical name**</span></span><br><span data-ttu-id="d5f97-113">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="d5f97-113">**_Type_**</span></span> | <span data-ttu-id="d5f97-114">استخدام</span><span class="sxs-lookup"><span data-stu-id="d5f97-114">Use</span></span> | <span data-ttu-id="d5f97-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="d5f97-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d5f97-116">**معرف كيان نوع الشهادة**</span><span class="sxs-lookup"><span data-stu-id="d5f97-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="d5f97-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="d5f97-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="d5f97-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d5f97-118">*GUID*</span></span> | <span data-ttu-id="d5f97-119">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="d5f97-119">Read-only</span></span><br><span data-ttu-id="d5f97-120">مطلوب</span><span class="sxs-lookup"><span data-stu-id="d5f97-120">Required</span></span> 
<span data-ttu-id="d5f97-121">منشأ بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="d5f97-121">System-generated</span></span> | <span data-ttu-id="d5f97-122">المعرف الرئيسي الفريد لنوع الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d5f97-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="d5f97-123">**نوع الشهادة**</span><span class="sxs-lookup"><span data-stu-id="d5f97-123">**Certificate Type**</span></span><br><span data-ttu-id="d5f97-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="d5f97-124">mshr_certificatetype</span></span><br><span data-ttu-id="d5f97-125">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="d5f97-125">*String*</span></span> | <span data-ttu-id="d5f97-126">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="d5f97-126">Read/write</span></span><br><span data-ttu-id="d5f97-127">مطلوب</span><span class="sxs-lookup"><span data-stu-id="d5f97-127">Required</span></span> | <span data-ttu-id="d5f97-128">معرف فريد قابل للقراءة بواسطة المستخدم لنوع الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d5f97-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="d5f97-129">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="d5f97-129">**Description**</span></span><br><span data-ttu-id="d5f97-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="d5f97-130">mshr_description</span></span><br><span data-ttu-id="d5f97-131">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="d5f97-131">*String*</span></span> | <span data-ttu-id="d5f97-132">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="d5f97-132">Read/write</span></span><br><span data-ttu-id="d5f97-133">مطلوب</span><span class="sxs-lookup"><span data-stu-id="d5f97-133">Required</span></span> | <span data-ttu-id="d5f97-134">وصف نوع الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d5f97-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="d5f97-135">**يتطلب التجديد**</span><span class="sxs-lookup"><span data-stu-id="d5f97-135">**Require Renewal**</span></span><br><span data-ttu-id="d5f97-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="d5f97-136">mshr_requirerenewal</span></span><br><span data-ttu-id="d5f97-137">*مجموعة خيارات mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="d5f97-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="d5f97-138">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="d5f97-138">Read/write</span></span><br><span data-ttu-id="d5f97-139">اختياري</span><span class="sxs-lookup"><span data-stu-id="d5f97-139">Optional</span></span> | <span data-ttu-id="d5f97-140">يشير إلى ما إذا كان التجديد مطلوبًا للشهادة أم لا.</span><span class="sxs-lookup"><span data-stu-id="d5f97-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5f97-141">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d5f97-141">See also</span></span>

[<span data-ttu-id="d5f97-142">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="d5f97-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d5f97-143">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="d5f97-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

