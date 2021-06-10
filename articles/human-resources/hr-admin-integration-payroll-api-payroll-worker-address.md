---
title: عنوان عامل كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان عنوان عامل كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052279"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="3e14f-103">عنوان عامل كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="3e14f-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3e14f-104">يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان عنوان عامل كشف الرواتب في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e14f-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3e14f-105">الخصائص</span><span class="sxs-lookup"><span data-stu-id="3e14f-105">Properties</span></span>

| <span data-ttu-id="3e14f-106">الخاصية</span><span class="sxs-lookup"><span data-stu-id="3e14f-106">Property</span></span><br><span data-ttu-id="3e14f-107">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="3e14f-107">**Physical name**</span></span><br><span data-ttu-id="3e14f-108">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="3e14f-108">**_Type_**</span></span> | <span data-ttu-id="3e14f-109">استخدام</span><span class="sxs-lookup"><span data-stu-id="3e14f-109">Use</span></span> | <span data-ttu-id="3e14f-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="3e14f-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3e14f-111">**المدينة**</span><span class="sxs-lookup"><span data-stu-id="3e14f-111">**City**</span></span><br><span data-ttu-id="3e14f-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="3e14f-112">mshr_city</span></span><br><span data-ttu-id="3e14f-113">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-113">*String*</span></span> | <span data-ttu-id="3e14f-114">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-114">Read-only</span></span><br><span data-ttu-id="3e14f-115">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-115">Required</span></span> | <span data-ttu-id="3e14f-116">المدينة المحددة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="3e14f-117">**رقم الموظف**</span><span class="sxs-lookup"><span data-stu-id="3e14f-117">**Personnel number**</span></span><br><span data-ttu-id="3e14f-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="3e14f-118">mshr_personnelnumber</span></span><br><span data-ttu-id="3e14f-119">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-119">*String*</span></span> | <span data-ttu-id="3e14f-120">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-120">Read-only</span></span><br><span data-ttu-id="3e14f-121">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-121">Required</span></span> | <span data-ttu-id="3e14f-122">رقم الموظف الفريد الخاص بالموظف.</span><span class="sxs-lookup"><span data-stu-id="3e14f-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="3e14f-123">**منطقة البلد**</span><span class="sxs-lookup"><span data-stu-id="3e14f-123">**Country region**</span></span><br><span data-ttu-id="3e14f-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="3e14f-124">mshr_countryregionid</span></span><br><span data-ttu-id="3e14f-125">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-125">*String*</span></span> | <span data-ttu-id="3e14f-126">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-126">Read-only</span></span><br><span data-ttu-id="3e14f-127">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-127">Required</span></span> | <span data-ttu-id="3e14f-128">منطقة البلد المحددة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="3e14f-129">**صالح من**</span><span class="sxs-lookup"><span data-stu-id="3e14f-129">**Valid from**</span></span><br><span data-ttu-id="3e14f-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="3e14f-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="3e14f-131">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="3e14f-131">*Date Time Offset*</span></span> | <span data-ttu-id="3e14f-132">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-132">Read-only</span></span> <br><span data-ttu-id="3e14f-133">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-133">Required</span></span> | <span data-ttu-id="3e14f-134">تاريخ بدء صلاحية العنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="3e14f-135">**عمل في العنوان**</span><span class="sxs-lookup"><span data-stu-id="3e14f-135">**Worked in address**</span></span><br><span data-ttu-id="3e14f-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="3e14f-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="3e14f-137">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-137">Read-only</span></span><br><span data-ttu-id="3e14f-138">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-138">Required</span></span> | <span data-ttu-id="3e14f-139">الإشارة إلى ما إذا كان العنوان هو المكان الذي يعمل به الموظف.</span><span class="sxs-lookup"><span data-stu-id="3e14f-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="3e14f-140">**المقاطعة**</span><span class="sxs-lookup"><span data-stu-id="3e14f-140">**County**</span></span><br><span data-ttu-id="3e14f-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="3e14f-141">mshr_county</span></span><br><span data-ttu-id="3e14f-142">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-142">*String*</span></span> | <span data-ttu-id="3e14f-143">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-143">Read-only</span></span><br><span data-ttu-id="3e14f-144">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-144">Required</span></span> | <span data-ttu-id="3e14f-145">البلد المحدد للعنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="3e14f-146">**معرف عنوان عامل كشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="3e14f-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="3e14f-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="3e14f-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="3e14f-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3e14f-148">*GUID*</span></span> | <span data-ttu-id="3e14f-149">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-149">Required</span></span><br><span data-ttu-id="3e14f-150">النظام منشأ</span><span class="sxs-lookup"><span data-stu-id="3e14f-150">System generated</span></span> | <span data-ttu-id="3e14f-151">قيمة معرف GUID منشأ بواسطة النظام لتعريف العنوان بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="3e14f-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="3e14f-152">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="3e14f-152">**Primary field**</span></span><br><span data-ttu-id="3e14f-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3e14f-153">mshr_primaryfield</span></span><br><span data-ttu-id="3e14f-154">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-154">*String*</span></span> | <span data-ttu-id="3e14f-155">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-155">Read-only</span></span><br><span data-ttu-id="3e14f-156">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-156">Required</span></span> |  |
| <span data-ttu-id="3e14f-157">**الشارع**</span><span class="sxs-lookup"><span data-stu-id="3e14f-157">**Street**</span></span><br><span data-ttu-id="3e14f-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="3e14f-158">mshr_street</span></span><br><span data-ttu-id="3e14f-159">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-159">*String*</span></span> | <span data-ttu-id="3e14f-160">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-160">Read-only</span></span><br><span data-ttu-id="3e14f-161">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-161">Required</span></span> | <span data-ttu-id="3e14f-162">الشارع المحدد للعنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-162">The street defined for the address.</span></span> |
| <span data-ttu-id="3e14f-163">**صالح حتى**</span><span class="sxs-lookup"><span data-stu-id="3e14f-163">**Valid to**</span></span><br><span data-ttu-id="3e14f-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="3e14f-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="3e14f-165">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="3e14f-165">*Date Time Offset*</span></span> | <span data-ttu-id="3e14f-166">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-166">Read-only</span></span> <br><span data-ttu-id="3e14f-167">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-167">Required</span></span> | <span data-ttu-id="3e14f-168">تاريخ انتهاء صلاحية العنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="3e14f-169">**معرف الموقع**</span><span class="sxs-lookup"><span data-stu-id="3e14f-169">**Location ID**</span></span><br><span data-ttu-id="3e14f-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="3e14f-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="3e14f-171">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-171">Read-only</span></span> <br><span data-ttu-id="3e14f-172">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-172">Required</span></span> | <span data-ttu-id="3e14f-173">المعرف الخاص بالعنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-173">The ID for the address.</span></span>  |
| <span data-ttu-id="3e14f-174">**الرمز البريدي**</span><span class="sxs-lookup"><span data-stu-id="3e14f-174">**Postal code**</span></span><br><span data-ttu-id="3e14f-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="3e14f-175">mshr_zipcode</span></span><br><span data-ttu-id="3e14f-176">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-176">*String*</span></span> | <span data-ttu-id="3e14f-177">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-177">Read-only</span></span> <br><span data-ttu-id="3e14f-178">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-178">Required</span></span> |<span data-ttu-id="3e14f-179">رقم التعريف المحدد للموظف.</span><span class="sxs-lookup"><span data-stu-id="3e14f-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="3e14f-180">**أقام في العنوان**</span><span class="sxs-lookup"><span data-stu-id="3e14f-180">**Lived in address**</span></span><br><span data-ttu-id="3e14f-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="3e14f-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="3e14f-182">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-182">Read-only</span></span><br><span data-ttu-id="3e14f-183">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-183">Required</span></span> | <span data-ttu-id="3e14f-184">الإشارة إلى ما إذا كان العنوان هو المكان الذي يقيم فيه الموظف.</span><span class="sxs-lookup"><span data-stu-id="3e14f-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="3e14f-185">**الولاية**</span><span class="sxs-lookup"><span data-stu-id="3e14f-185">**State**</span></span><br><span data-ttu-id="3e14f-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="3e14f-186">mshr_state</span></span><br><span data-ttu-id="3e14f-187">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="3e14f-187">*String*</span></span> | <span data-ttu-id="3e14f-188">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="3e14f-188">Read-only</span></span><br><span data-ttu-id="3e14f-189">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e14f-189">Required</span></span> | <span data-ttu-id="3e14f-190">الولاية المحددة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="3e14f-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="3e14f-191">مثال الاستعلام</span><span class="sxs-lookup"><span data-stu-id="3e14f-191">Example query</span></span>

<span data-ttu-id="3e14f-192">**الطلب**</span><span class="sxs-lookup"><span data-stu-id="3e14f-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="3e14f-193">**استجابة**</span><span class="sxs-lookup"><span data-stu-id="3e14f-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
