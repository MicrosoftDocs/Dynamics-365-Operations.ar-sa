---
title: خطة التعويض الثابتة لكشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان خطة التعويض الثابت في كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
manager: tfehr
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881921"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="6d178-103">خطة التعويض الثابتة لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="6d178-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6d178-104">يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان خطة التعويض الثابت في كشف الرواتب في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6d178-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="6d178-105">الخصائص</span><span class="sxs-lookup"><span data-stu-id="6d178-105">Properties</span></span>

| <span data-ttu-id="6d178-106">الخاصية</span><span class="sxs-lookup"><span data-stu-id="6d178-106">Property</span></span><br><span data-ttu-id="6d178-107">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="6d178-107">**Physical name**</span></span><br><span data-ttu-id="6d178-108">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="6d178-108">**_Type_**</span></span> | <span data-ttu-id="6d178-109">استخدام</span><span class="sxs-lookup"><span data-stu-id="6d178-109">Use</span></span> | <span data-ttu-id="6d178-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="6d178-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6d178-111">**معرف الموظف**</span><span class="sxs-lookup"><span data-stu-id="6d178-111">**Employee ID**</span></span><br><span data-ttu-id="6d178-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="6d178-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="6d178-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6d178-113">*GUID*</span></span> | <span data-ttu-id="6d178-114">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-114">Read-only</span></span><br><span data-ttu-id="6d178-115">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-115">Required</span></span><br><span data-ttu-id="6d178-116">مفتاح خارجي:mshr_Employee_id لـ mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="6d178-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="6d178-117">معرف الموظف</span><span class="sxs-lookup"><span data-stu-id="6d178-117">Employee ID</span></span> |
| <span data-ttu-id="6d178-118">**معدل الدفع**</span><span class="sxs-lookup"><span data-stu-id="6d178-118">**Pay rate**</span></span><br><span data-ttu-id="6d178-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="6d178-119">mshr_payrate</span></span><br><span data-ttu-id="6d178-120">*عشري*</span><span class="sxs-lookup"><span data-stu-id="6d178-120">*Decimal*</span></span> | <span data-ttu-id="6d178-121">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-121">Read-only</span></span><br><span data-ttu-id="6d178-122">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-122">Required</span></span> | <span data-ttu-id="6d178-123">معدل الدفع المحدد في خطة التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="6d178-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="6d178-124">**معرف الخطة**</span><span class="sxs-lookup"><span data-stu-id="6d178-124">**Plan ID**</span></span><br><span data-ttu-id="6d178-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="6d178-125">mshr_planid</span></span><br><span data-ttu-id="6d178-126">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d178-126">*String*</span></span> | <span data-ttu-id="6d178-127">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-127">Read-only</span></span><br><span data-ttu-id="6d178-128">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-128">Required</span></span> |<span data-ttu-id="6d178-129">تحدد خطة التعويض.</span><span class="sxs-lookup"><span data-stu-id="6d178-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="6d178-130">**صالح من**</span><span class="sxs-lookup"><span data-stu-id="6d178-130">**Valid from**</span></span><br><span data-ttu-id="6d178-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="6d178-131">mshr_validfrom</span></span><br><span data-ttu-id="6d178-132">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="6d178-132">*Date Time Offset*</span></span> |  <span data-ttu-id="6d178-133">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-133">Read-only</span></span><br><span data-ttu-id="6d178-134">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-134">Required</span></span> |<span data-ttu-id="6d178-135">تاريخ بدء صلاحية التعويض الثابت للموظف.</span><span class="sxs-lookup"><span data-stu-id="6d178-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="6d178-136">**كيان خطة التعويض الثابتة لكشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="6d178-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="6d178-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="6d178-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="6d178-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6d178-138">*GUID*</span></span> | <span data-ttu-id="6d178-139">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-139">Required</span></span><br><span data-ttu-id="6d178-140">منشأ بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="6d178-140">Sytem generated</span></span> | <span data-ttu-id="6d178-141">قيمة معرف GUID منشأ بواسطة النظام لتعريف خطة التعويض بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="6d178-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="6d178-142">**تكرار الدفع**</span><span class="sxs-lookup"><span data-stu-id="6d178-142">**Pay frequency**</span></span><br><span data-ttu-id="6d178-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="6d178-143">mshr_payfrequency</span></span><br><span data-ttu-id="6d178-144">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d178-144">*String*</span></span> | <span data-ttu-id="6d178-145">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-145">Read-only</span></span><br><span data-ttu-id="6d178-146">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-146">Required</span></span> |<span data-ttu-id="6d178-147">تكرار تنفيذ عملية الدفع للموظف.</span><span class="sxs-lookup"><span data-stu-id="6d178-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="6d178-148">**صالح حتى**</span><span class="sxs-lookup"><span data-stu-id="6d178-148">**Valid to**</span></span><br><span data-ttu-id="6d178-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="6d178-149">mshr_validto</span></span><br><span data-ttu-id="6d178-150">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="6d178-150">*Date Time Offset*</span></span> | <span data-ttu-id="6d178-151">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-151">Read-only</span></span> <br><span data-ttu-id="6d178-152">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-152">Required</span></span> | <span data-ttu-id="6d178-153">تاريخ انتهاء صلاحية التعويض الثابت للموظف.</span><span class="sxs-lookup"><span data-stu-id="6d178-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="6d178-154">**معرف المنصب**</span><span class="sxs-lookup"><span data-stu-id="6d178-154">**Position ID**</span></span><br><span data-ttu-id="6d178-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="6d178-155">mshr_positionid</span></span><br><span data-ttu-id="6d178-156">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d178-156">*String*</span></span> | <span data-ttu-id="6d178-157">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-157">Read-only</span></span> <br><span data-ttu-id="6d178-158">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-158">Required</span></span> | <span data-ttu-id="6d178-159">معرف المنصب المرتبط بالموظف وتسجيل خطة التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="6d178-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="6d178-160">**عملة**</span><span class="sxs-lookup"><span data-stu-id="6d178-160">**Currency**</span></span><br><span data-ttu-id="6d178-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="6d178-161">mshr_currency</span></span><br><span data-ttu-id="6d178-162">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d178-162">*String*</span></span> | <span data-ttu-id="6d178-163">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-163">Read-only</span></span> <br><span data-ttu-id="6d178-164">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-164">Required</span></span> |<span data-ttu-id="6d178-165">العملة المحددة لخطة التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="6d178-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="6d178-166">**رقم الموظف**</span><span class="sxs-lookup"><span data-stu-id="6d178-166">**Personnel number**</span></span><br><span data-ttu-id="6d178-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="6d178-167">mshr_personnelnumber</span></span><br><span data-ttu-id="6d178-168">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="6d178-168">*String*</span></span> | <span data-ttu-id="6d178-169">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="6d178-169">Read-only</span></span><br><span data-ttu-id="6d178-170">مطلوب</span><span class="sxs-lookup"><span data-stu-id="6d178-170">Required</span></span> |<span data-ttu-id="6d178-171">رقم الموظف الفريد الخاص بالموظف.</span><span class="sxs-lookup"><span data-stu-id="6d178-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="6d178-172">**استعلام**</span><span class="sxs-lookup"><span data-stu-id="6d178-172">**Query**</span></span>

<span data-ttu-id="6d178-173">**الطلب**</span><span class="sxs-lookup"><span data-stu-id="6d178-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="6d178-174">**استجابة**</span><span class="sxs-lookup"><span data-stu-id="6d178-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
