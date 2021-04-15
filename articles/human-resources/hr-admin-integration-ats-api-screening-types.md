---
title: أنواع المراقبة
description: يصف هذا الموضوع كيان أنواع المراقبة لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805120"
---
# <a name="screening-types"></a><span data-ttu-id="82290-103">أنواع المراقبة</span><span class="sxs-lookup"><span data-stu-id="82290-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="82290-104">يصف هذا الموضوع كيان أنواع المراقبة لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="82290-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="82290-105">الاسم الفعلي: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="82290-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="82290-106">الوصف</span><span class="sxs-lookup"><span data-stu-id="82290-106">Description</span></span>

<span data-ttu-id="82290-107">يصف هذا الكيان أنواع عمليات المراقبة التي قامت الشركة بإعدادها لعمليات مراقبة التوظيف المسبق والمستمر.</span><span class="sxs-lookup"><span data-stu-id="82290-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="82290-108">تمثيل JSON</span><span class="sxs-lookup"><span data-stu-id="82290-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="82290-109">الخصائص</span><span class="sxs-lookup"><span data-stu-id="82290-109">Properties</span></span>

| <span data-ttu-id="82290-110">الخاصية</span><span class="sxs-lookup"><span data-stu-id="82290-110">Property</span></span><br><span data-ttu-id="82290-111">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="82290-111">**Physical name**</span></span><br><span data-ttu-id="82290-112">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="82290-112">**_Type_**</span></span> | <span data-ttu-id="82290-113">استخدام</span><span class="sxs-lookup"><span data-stu-id="82290-113">Use</span></span> | <span data-ttu-id="82290-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="82290-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="82290-115">**معرف كيان نوع المراقبة**</span><span class="sxs-lookup"><span data-stu-id="82290-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="82290-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="82290-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="82290-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="82290-117">*GUID*</span></span> | <span data-ttu-id="82290-118">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="82290-118">Read-only</span></span><br><span data-ttu-id="82290-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="82290-119">Required</span></span><br><span data-ttu-id="82290-120">منشأ بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="82290-120">System-generated</span></span> | <span data-ttu-id="82290-121">المعرف الأساسي الفريد لسجل نوع المراقبة.</span><span class="sxs-lookup"><span data-stu-id="82290-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="82290-122">**معرف نوع المراقبة**</span><span class="sxs-lookup"><span data-stu-id="82290-122">**Screening Type ID**</span></span><br><span data-ttu-id="82290-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="82290-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="82290-124">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="82290-124">*String*</span></span> | <span data-ttu-id="82290-125">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="82290-125">Read/write</span></span><br><span data-ttu-id="82290-126">مطلوب</span><span class="sxs-lookup"><span data-stu-id="82290-126">Required</span></span> | <span data-ttu-id="82290-127">المعرف الفريد المحدد بواسطة المستخدم لنوع المراقبة.</span><span class="sxs-lookup"><span data-stu-id="82290-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="82290-128">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="82290-128">**Description**</span></span><br><span data-ttu-id="82290-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="82290-129">mshr_description</span></span><br><span data-ttu-id="82290-130">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="82290-130">*String*</span></span> | <span data-ttu-id="82290-131">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="82290-131">Read/write</span></span><br><span data-ttu-id="82290-132">مطلوب</span><span class="sxs-lookup"><span data-stu-id="82290-132">Required</span></span> | <span data-ttu-id="82290-133">وصف نوع المراقبة.</span><span class="sxs-lookup"><span data-stu-id="82290-133">The description of the screening type.</span></span> |
| <span data-ttu-id="82290-134">**وحدة التكرار**</span><span class="sxs-lookup"><span data-stu-id="82290-134">**Frequency Unit**</span></span><br><span data-ttu-id="82290-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="82290-135">mshr_frequencyunit</span></span><br><span data-ttu-id="82290-136">*مجموعة خيارات mshr_hcmfrequencyunit*</span><span class="sxs-lookup"><span data-stu-id="82290-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="82290-137">قراءة/كتابة</span><span class="sxs-lookup"><span data-stu-id="82290-137">Read/write</span></span><br><span data-ttu-id="82290-138">مطلوب</span><span class="sxs-lookup"><span data-stu-id="82290-138">Required</span></span> | <span data-ttu-id="82290-139">يصف التكرار الذي يجب أن تكتمل معه المراقبة للشخص المعين.</span><span class="sxs-lookup"><span data-stu-id="82290-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="82290-140">**إنشاء من**</span><span class="sxs-lookup"><span data-stu-id="82290-140">**Generate From**</span></span><br><span data-ttu-id="82290-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="82290-141">mshr_generatefrom</span></span><br><span data-ttu-id="82290-142">*مجموعة خيارات mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="82290-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="82290-143">قراءة-كتابة</span><span class="sxs-lookup"><span data-stu-id="82290-143">Read-write</span></span><br><span data-ttu-id="82290-144">مطلوب</span><span class="sxs-lookup"><span data-stu-id="82290-144">Required</span></span> | <span data-ttu-id="82290-145">إذا كانت قيمة التكرار هي أي قيمة بخلاف "مرة واحدة فقط" ، تحدد القيمة GenerateFrom التاريخ الذي يتم منه حساب حدث المراقبة التالي.</span><span class="sxs-lookup"><span data-stu-id="82290-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="82290-146">**فاصل التكرار**</span><span class="sxs-lookup"><span data-stu-id="82290-146">**Frequency Interval**</span></span><br><span data-ttu-id="82290-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="82290-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="82290-148">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="82290-148">*Integer*</span></span> | <span data-ttu-id="82290-149">قراءة-كتابة</span><span class="sxs-lookup"><span data-stu-id="82290-149">Read-write</span></span><br><span data-ttu-id="82290-150">مطلوب</span><span class="sxs-lookup"><span data-stu-id="82290-150">Required</span></span> | <span data-ttu-id="82290-151">إذا كانت قيمة التكرار هي أي قيمة خلاف "مرة واحدة فقط" ، فيجب عليك تحديد فاصل زمني لوحدات الوقت بين كل حدث من أحداث المراقبة.</span><span class="sxs-lookup"><span data-stu-id="82290-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="82290-152">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="82290-152">See also</span></span>

[<span data-ttu-id="82290-153">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="82290-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="82290-154">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="82290-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]