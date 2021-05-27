---
title: عنوان عامل كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان عنوان عامل كشف الرواتب في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020695"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="aeaaf-103">عنوان عامل كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aeaaf-104">يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان عنوان عامل كشف الرواتب في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="aeaaf-105">الخصائص</span><span class="sxs-lookup"><span data-stu-id="aeaaf-105">Properties</span></span>

| <span data-ttu-id="aeaaf-106">الخاصية</span><span class="sxs-lookup"><span data-stu-id="aeaaf-106">Property</span></span><br><span data-ttu-id="aeaaf-107">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-107">**Physical name**</span></span><br><span data-ttu-id="aeaaf-108">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-108">**_Type_**</span></span> | <span data-ttu-id="aeaaf-109">استخدام</span><span class="sxs-lookup"><span data-stu-id="aeaaf-109">Use</span></span> | <span data-ttu-id="aeaaf-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="aeaaf-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aeaaf-111">**المدينة**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-111">**City**</span></span><br><span data-ttu-id="aeaaf-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="aeaaf-112">mshr_city</span></span><br><span data-ttu-id="aeaaf-113">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-113">*String*</span></span> | <span data-ttu-id="aeaaf-114">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-114">Read-only</span></span><br><span data-ttu-id="aeaaf-115">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-115">Required</span></span> | <span data-ttu-id="aeaaf-116">المدينة المحددة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="aeaaf-117">**رقم الموظف**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-117">**Personnel number**</span></span><br><span data-ttu-id="aeaaf-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="aeaaf-118">mshr_personnelnumber</span></span><br><span data-ttu-id="aeaaf-119">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-119">*String*</span></span> | <span data-ttu-id="aeaaf-120">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-120">Read-only</span></span><br><span data-ttu-id="aeaaf-121">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-121">Required</span></span> | <span data-ttu-id="aeaaf-122">رقم الموظف الفريد الخاص بالموظف.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="aeaaf-123">**منطقة البلد**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-123">**Country region**</span></span><br><span data-ttu-id="aeaaf-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="aeaaf-124">mshr_countryregionid</span></span><br><span data-ttu-id="aeaaf-125">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-125">*String*</span></span> | <span data-ttu-id="aeaaf-126">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-126">Read-only</span></span><br><span data-ttu-id="aeaaf-127">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-127">Required</span></span> | <span data-ttu-id="aeaaf-128">منطقة البلد المحددة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="aeaaf-129">**صالح من**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-129">**Valid from**</span></span><br><span data-ttu-id="aeaaf-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="aeaaf-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="aeaaf-131">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-131">*Date Time Offset*</span></span> | <span data-ttu-id="aeaaf-132">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-132">Read-only</span></span> <br><span data-ttu-id="aeaaf-133">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-133">Required</span></span> | <span data-ttu-id="aeaaf-134">تاريخ بدء صلاحية العنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="aeaaf-135">**عمل في العنوان**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-135">**Worked in address**</span></span><br><span data-ttu-id="aeaaf-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="aeaaf-137">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-137">Read-only</span></span><br><span data-ttu-id="aeaaf-138">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-138">Required</span></span> | <span data-ttu-id="aeaaf-139">الإشارة إلى ما إذا كان العنوان هو المكان الذي يعمل به الموظف.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="aeaaf-140">**المقاطعة**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-140">**County**</span></span><br><span data-ttu-id="aeaaf-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="aeaaf-141">mshr_county</span></span><br><span data-ttu-id="aeaaf-142">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-142">*String*</span></span> | <span data-ttu-id="aeaaf-143">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-143">Read-only</span></span><br><span data-ttu-id="aeaaf-144">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-144">Required</span></span> | <span data-ttu-id="aeaaf-145">البلد المحدد للعنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="aeaaf-146">**معرف عنوان عامل كشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="aeaaf-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="aeaaf-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="aeaaf-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-148">*GUID*</span></span> | <span data-ttu-id="aeaaf-149">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-149">Required</span></span><br><span data-ttu-id="aeaaf-150">النظام منشأ</span><span class="sxs-lookup"><span data-stu-id="aeaaf-150">System generated</span></span> | <span data-ttu-id="aeaaf-151">قيمة معرف GUID منشأ بواسطة النظام لتعريف العنوان بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="aeaaf-152">**الحقل الأساسي**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-152">**Primary field**</span></span><br><span data-ttu-id="aeaaf-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="aeaaf-153">mshr_primaryfield</span></span><br><span data-ttu-id="aeaaf-154">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-154">*String*</span></span> | <span data-ttu-id="aeaaf-155">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-155">Read-only</span></span><br><span data-ttu-id="aeaaf-156">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-156">Required</span></span> |  |
| <span data-ttu-id="aeaaf-157">**الشارع**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-157">**Street**</span></span><br><span data-ttu-id="aeaaf-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="aeaaf-158">mshr_street</span></span><br><span data-ttu-id="aeaaf-159">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-159">*String*</span></span> | <span data-ttu-id="aeaaf-160">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-160">Read-only</span></span><br><span data-ttu-id="aeaaf-161">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-161">Required</span></span> | <span data-ttu-id="aeaaf-162">الشارع المحدد للعنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-162">The street defined for the address.</span></span> |
| <span data-ttu-id="aeaaf-163">**صالح حتى**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-163">**Valid to**</span></span><br><span data-ttu-id="aeaaf-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="aeaaf-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="aeaaf-165">*الفرق بالتاريخ والوقت*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-165">*Date Time Offset*</span></span> | <span data-ttu-id="aeaaf-166">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-166">Read-only</span></span> <br><span data-ttu-id="aeaaf-167">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-167">Required</span></span> | <span data-ttu-id="aeaaf-168">تاريخ انتهاء صلاحية العنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="aeaaf-169">**معرف الموقع**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-169">**Location ID**</span></span><br><span data-ttu-id="aeaaf-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="aeaaf-171">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-171">Read-only</span></span> <br><span data-ttu-id="aeaaf-172">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-172">Required</span></span> | <span data-ttu-id="aeaaf-173">المعرف الخاص بالعنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-173">The ID for the address.</span></span>  |
| <span data-ttu-id="aeaaf-174">**الرمز البريدي**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-174">**Postal code**</span></span><br><span data-ttu-id="aeaaf-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="aeaaf-175">mshr_zipcode</span></span><br><span data-ttu-id="aeaaf-176">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-176">*String*</span></span> | <span data-ttu-id="aeaaf-177">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-177">Read-only</span></span> <br><span data-ttu-id="aeaaf-178">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-178">Required</span></span> |<span data-ttu-id="aeaaf-179">رقم التعريف المحدد للموظف.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="aeaaf-180">**أقام في العنوان**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-180">**Lived in address**</span></span><br><span data-ttu-id="aeaaf-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="aeaaf-182">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-182">Read-only</span></span><br><span data-ttu-id="aeaaf-183">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-183">Required</span></span> | <span data-ttu-id="aeaaf-184">الإشارة إلى ما إذا كان العنوان هو المكان الذي يقيم فيه الموظف.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="aeaaf-185">**الولاية**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-185">**State**</span></span><br><span data-ttu-id="aeaaf-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="aeaaf-186">mshr_state</span></span><br><span data-ttu-id="aeaaf-187">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="aeaaf-187">*String*</span></span> | <span data-ttu-id="aeaaf-188">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="aeaaf-188">Read-only</span></span><br><span data-ttu-id="aeaaf-189">مطلوب</span><span class="sxs-lookup"><span data-stu-id="aeaaf-189">Required</span></span> | <span data-ttu-id="aeaaf-190">الولاية المحددة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="aeaaf-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="aeaaf-191">مثال الاستعلام</span><span class="sxs-lookup"><span data-stu-id="aeaaf-191">Example query</span></span>

<span data-ttu-id="aeaaf-192">**الطلب**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="aeaaf-193">**استجابة**</span><span class="sxs-lookup"><span data-stu-id="aeaaf-193">**Response**</span></span>

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
