---
title: تفاصيل كشف الرواتب للمناصب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لتفاصيل كشف الرواتب لكيان المناصب في Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019312"
---
# <a name="payroll-position"></a><span data-ttu-id="02a95-103">منصب كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="02a95-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="02a95-104">يوفر هذا الموضوع تفاصيل ومثال استعلام لتفاصيل كشف الرواتب لكيان المناصب في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="02a95-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="02a95-105">الخصائص</span><span class="sxs-lookup"><span data-stu-id="02a95-105">Properties</span></span>

| <span data-ttu-id="02a95-106">الخاصية</span><span class="sxs-lookup"><span data-stu-id="02a95-106">Property</span></span><br><span data-ttu-id="02a95-107">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="02a95-107">**Physical name**</span></span><br><span data-ttu-id="02a95-108">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="02a95-108">**_Type_**</span></span> | <span data-ttu-id="02a95-109">استخدام</span><span class="sxs-lookup"><span data-stu-id="02a95-109">Use</span></span> | <span data-ttu-id="02a95-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="02a95-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="02a95-111">**الساعات العادية السنوية**</span><span class="sxs-lookup"><span data-stu-id="02a95-111">**Annual regular hours**</span></span><br><span data-ttu-id="02a95-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="02a95-112">annualregularhours</span></span><br><span data-ttu-id="02a95-113">*عشري*</span><span class="sxs-lookup"><span data-stu-id="02a95-113">*Decimal*</span></span> | <span data-ttu-id="02a95-114">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-114">Read-only</span></span><br><span data-ttu-id="02a95-115">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-115">Required</span></span> | <span data-ttu-id="02a95-116">ساعات العمل الدورية السنوية المحددة في المنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="02a95-117">**معرف كيان تفاصيل المنصب في كشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="02a95-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="02a95-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="02a95-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="02a95-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="02a95-119">*Guid*</span></span> | <span data-ttu-id="02a95-120">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-120">Required</span></span><br><span data-ttu-id="02a95-121">منشأ بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="02a95-121">System generated.</span></span> | <span data-ttu-id="02a95-122">قيمة معرف GUID منشأ بواسطة النظام لتعريف المنصب بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="02a95-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="02a95-123">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="02a95-123">**Primary field**</span></span><br><span data-ttu-id="02a95-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="02a95-124">mshr_primaryfield</span></span><br><span data-ttu-id="02a95-125">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="02a95-125">*String*</span></span> | <span data-ttu-id="02a95-126">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-126">Required</span></span><br><span data-ttu-id="02a95-127">النظام منشأ</span><span class="sxs-lookup"><span data-stu-id="02a95-127">System generated</span></span> |  |
| <span data-ttu-id="02a95-128">**قيمة معرف وظيفة المنصب**</span><span class="sxs-lookup"><span data-stu-id="02a95-128">**Position job ID value**</span></span><br><span data-ttu-id="02a95-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="02a95-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="02a95-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="02a95-130">*GUID*</span></span> | <span data-ttu-id="02a95-131">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-131">Read-only</span></span><br><span data-ttu-id="02a95-132">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-132">Required</span></span><br><span data-ttu-id="02a95-133">مفتاح خارجي:mshr_PayrollPositionJobEntity لـ mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="02a95-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="02a95-134">معرف الوظيفة المقترنة بالمنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="02a95-135">**قيمة معرف خطة التعويض الثابت**</span><span class="sxs-lookup"><span data-stu-id="02a95-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="02a95-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="02a95-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="02a95-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="02a95-137">*GUID*</span></span> | <span data-ttu-id="02a95-138">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-138">Read-only</span></span><br><span data-ttu-id="02a95-139">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-139">Required</span></span><br><span data-ttu-id="02a95-140">مفتاح خارجي: mshr_FixedCompPlan_id لـ mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="02a95-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="02a95-141">معرف خطة التعويض الثابت المقترنة بالمنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="02a95-142">**معرف دورة الدفع**</span><span class="sxs-lookup"><span data-stu-id="02a95-142">**Pay cycle ID**</span></span><br><span data-ttu-id="02a95-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="02a95-143">mshr_primaryfield</span></span><br><span data-ttu-id="02a95-144">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="02a95-144">*String*</span></span> | <span data-ttu-id="02a95-145">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-145">Read-only</span></span><br><span data-ttu-id="02a95-146">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-146">Required</span></span> | <span data-ttu-id="02a95-147">دورة الدفع المحددة في المنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="02a95-148">**الدفع بواسطة الكيان القانوني**</span><span class="sxs-lookup"><span data-stu-id="02a95-148">**Paid by legal entity**</span></span><br><span data-ttu-id="02a95-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="02a95-149">paidbylegalentity</span></span><br><span data-ttu-id="02a95-150">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="02a95-150">*String*</span></span> | <span data-ttu-id="02a95-151">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-151">Read-only</span></span><br><span data-ttu-id="02a95-152">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-152">Required</span></span> | <span data-ttu-id="02a95-153">الكيان القانوني المحدد في المنصب المسؤول عن إصدار الدفع.</span><span class="sxs-lookup"><span data-stu-id="02a95-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="02a95-154">**معرف المنصب**</span><span class="sxs-lookup"><span data-stu-id="02a95-154">**Position ID**</span></span><br><span data-ttu-id="02a95-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="02a95-155">mshr_positionid</span></span><br><span data-ttu-id="02a95-156">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="02a95-156">*String*</span></span> | <span data-ttu-id="02a95-157">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-157">Read-only</span></span><br><span data-ttu-id="02a95-158">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-158">Required</span></span> | <span data-ttu-id="02a95-159">معرف المنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-159">The ID of the position.</span></span> |
| <span data-ttu-id="02a95-160">**صالح حتى**</span><span class="sxs-lookup"><span data-stu-id="02a95-160">**Valid to**</span></span><br><span data-ttu-id="02a95-161">validto</span><span class="sxs-lookup"><span data-stu-id="02a95-161">validto</span></span><br><span data-ttu-id="02a95-162">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="02a95-162">*Date Time Offset*</span></span> | <span data-ttu-id="02a95-163">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-163">Read-only</span></span><br><span data-ttu-id="02a95-164">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-164">Required</span></span> |<span data-ttu-id="02a95-165">تاريخ بدء صلاحيه تفاصيل المنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="02a95-166">**صالح من**</span><span class="sxs-lookup"><span data-stu-id="02a95-166">**Valid from**</span></span><br><span data-ttu-id="02a95-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="02a95-167">validfrom</span></span><br><span data-ttu-id="02a95-168">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="02a95-168">*Date Time Offset*</span></span> | <span data-ttu-id="02a95-169">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="02a95-169">Read-only</span></span><br><span data-ttu-id="02a95-170">مطلوب</span><span class="sxs-lookup"><span data-stu-id="02a95-170">Required</span></span> |<span data-ttu-id="02a95-171">تاريخ انتهاء صلاحيه تفاصيل المنصب.</span><span class="sxs-lookup"><span data-stu-id="02a95-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="02a95-172">**استعلام**</span><span class="sxs-lookup"><span data-stu-id="02a95-172">**Query**</span></span>

<span data-ttu-id="02a95-173">**الطلب**</span><span class="sxs-lookup"><span data-stu-id="02a95-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="02a95-174">**استجابة**</span><span class="sxs-lookup"><span data-stu-id="02a95-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
