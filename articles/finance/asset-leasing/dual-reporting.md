---
title: تقرير مزدوج
description: يقوم هذا الموضوع بإرشادك من خلال مثال يوضح كيفية استيفاء المتطلبات لكل من تقارير معايير Financial Reporting الدولية (IFRS) والتقارير القانونية في تأجير الأصل.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229540"
---
# <a name="dual-reporting"></a><span data-ttu-id="4cddd-103">تقرير مزدوج</span><span class="sxs-lookup"><span data-stu-id="4cddd-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cddd-104">يقوم هذا الموضوع بإرشادك من خلال مثال يوضح كيفية استيفاء المتطلبات لكل من تقارير معايير Financial Reporting الدولية (IFRS) والتقارير القانونية في تأجير الأصل.</span><span class="sxs-lookup"><span data-stu-id="4cddd-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="4cddd-105">يلزم وجود معرفة بطبقات الترحيل في Microsoft Dynamics 365 Finance وسيعمل ذلك على أن يكون من السهل فهم المثال.</span><span class="sxs-lookup"><span data-stu-id="4cddd-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="4cddd-106">مثال</span><span class="sxs-lookup"><span data-stu-id="4cddd-106">Example</span></span>

<span data-ttu-id="4cddd-107">وفيما يلي مثال على حسابات عقد الإيجار ضمن التقارير القانونية الإيطالية باستخدام كل من أساليب على أساس النقد وأساليب تقارير معايير IFRS.</span><span class="sxs-lookup"><span data-stu-id="4cddd-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="4cddd-108">ويجب أن تقوم الشركة بإنشاء ثلاثة دفاتر لحساب كل من المتطلبات القانونية الإيطالية والمتطلبات الخاصة بمعايير IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="4cddd-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="4cddd-109">ويتطلب وجود دفتر واحد بالنسبة لمعايير IFRS 16، ويكون دفتر واحد مطلوبًا للمتطلبات القانونية، ويلزم دفتر واحد لإلغاء الترحيلات القانونية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="4cddd-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="4cddd-110">يتم إعداد الدفاتر كما هو موضح في الجداول التالية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="4cddd-111">**دفتر IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="4cddd-111">**IFRS 16 book**</span></span>

<span data-ttu-id="4cddd-112">يتم إعداد دفتر معايير IFRS 16 بحيث يتوافق مع معيار المحاسبة الخاص بمعايير IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="4cddd-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="4cddd-113">سيتم ترحيل كافة الإدخالات التي يتم ترحيلها في هذا الدفتر إلى طبقة مخصصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="4cddd-114">الاسم</span><span class="sxs-lookup"><span data-stu-id="4cddd-114">Name</span></span>                                    | <span data-ttu-id="4cddd-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="4cddd-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="4cddd-116">نوع الدفتر</span><span class="sxs-lookup"><span data-stu-id="4cddd-116">Book type</span></span>                               | <span data-ttu-id="4cddd-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4cddd-117">IFRS 16</span></span>        |
| <span data-ttu-id="4cddd-118">وصف الدفتر</span><span class="sxs-lookup"><span data-stu-id="4cddd-118">Book description</span></span>                        | <span data-ttu-id="4cddd-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4cddd-119">IFRS 16</span></span>        |
| <span data-ttu-id="4cddd-120">طبقة الترحيل</span><span class="sxs-lookup"><span data-stu-id="4cddd-120">Posting Layer</span></span>                           | <span data-ttu-id="4cddd-121">الطبقة المخصصة 1</span><span class="sxs-lookup"><span data-stu-id="4cddd-121">Custom layer 1</span></span> |
| <span data-ttu-id="4cddd-122">نوع عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="4cddd-122">Lease Type</span></span>                              | <span data-ttu-id="4cddd-123">Finance</span><span class="sxs-lookup"><span data-stu-id="4cddd-123">Finance</span></span>        |
| <span data-ttu-id="4cddd-124">الإطار المحاسبي</span><span class="sxs-lookup"><span data-stu-id="4cddd-124">Accounting Framework</span></span>                    | <span data-ttu-id="4cddd-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4cddd-125">IFRS 16</span></span>        |
| <span data-ttu-id="4cddd-126">إعداد فترة الإيجار / العمر الإنتاجي</span><span class="sxs-lookup"><span data-stu-id="4cddd-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4cddd-127">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-127">0.00</span></span>           |
| <span data-ttu-id="4cddd-128">إعداد القيمة الحالية / القيمة العادلة للأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4cddd-129">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-129">0.00</span></span>           |
| <span data-ttu-id="4cddd-130">الحد قصير الأجل</span><span class="sxs-lookup"><span data-stu-id="4cddd-130">Short-term threshold</span></span>                    | <span data-ttu-id="4cddd-131">12</span><span class="sxs-lookup"><span data-stu-id="4cddd-131">12</span></span>             |
| <span data-ttu-id="4cddd-132">حد القيمة المنخفضة</span><span class="sxs-lookup"><span data-stu-id="4cddd-132">Low Value Threshold</span></span>                     | <span data-ttu-id="4cddd-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-133">5,000.00</span></span>       |
| <span data-ttu-id="4cddd-134">دفع للمورّد</span><span class="sxs-lookup"><span data-stu-id="4cddd-134">Pay to Vendor</span></span>                           | <span data-ttu-id="4cddd-135">لا</span><span class="sxs-lookup"><span data-stu-id="4cddd-135">No</span></span>             |

<span data-ttu-id="4cddd-136">**دفتر قانوني**</span><span class="sxs-lookup"><span data-stu-id="4cddd-136">**Statutory book**</span></span>

<span data-ttu-id="4cddd-137">يُعد الدفتر القانوني دفتر على أساس النقد ستقوم الشركة به بحساب مصروفات عقد الإيجار كمبلغ نقدي يتم دفعه للإيجار شهريًا.</span><span class="sxs-lookup"><span data-stu-id="4cddd-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="4cddd-138">لن ينتج عن هذا الدفتر حق استخدام الأصل أو التزامات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="4cddd-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="4cddd-139">الاسم</span><span class="sxs-lookup"><span data-stu-id="4cddd-139">Name</span></span>                                    | <span data-ttu-id="4cddd-140">الوصف</span><span class="sxs-lookup"><span data-stu-id="4cddd-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="4cddd-141">نوع الدفتر</span><span class="sxs-lookup"><span data-stu-id="4cddd-141">Book type</span></span>                               | <span data-ttu-id="4cddd-142">قانوني</span><span class="sxs-lookup"><span data-stu-id="4cddd-142">Statutory</span></span>   |
| <span data-ttu-id="4cddd-143">وصف الدفتر</span><span class="sxs-lookup"><span data-stu-id="4cddd-143">Book description</span></span>                        | <span data-ttu-id="4cddd-144">‏‫تقرير التدفقات النقدية GAAP‬ المحلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-144">Local GAAP</span></span>  |
| <span data-ttu-id="4cddd-145">طبقة الترحيل</span><span class="sxs-lookup"><span data-stu-id="4cddd-145">Posting Layer</span></span>                           | <span data-ttu-id="4cddd-146">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-146">Current</span></span>     |
| <span data-ttu-id="4cddd-147">نوع عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="4cddd-147">Lease Type</span></span>                              | <span data-ttu-id="4cddd-148">تلقائي</span><span class="sxs-lookup"><span data-stu-id="4cddd-148">Automatic</span></span>   |
| <span data-ttu-id="4cddd-149">الإطار المحاسبي</span><span class="sxs-lookup"><span data-stu-id="4cddd-149">Accounting Framework</span></span>                    | <span data-ttu-id="4cddd-150">الأساس النقدي</span><span class="sxs-lookup"><span data-stu-id="4cddd-150">Cash basis</span></span>  |
| <span data-ttu-id="4cddd-151">إعداد فترة الإيجار / العمر الإنتاجي</span><span class="sxs-lookup"><span data-stu-id="4cddd-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4cddd-152">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-152">0.00</span></span>        |
| <span data-ttu-id="4cddd-153">إعداد القيمة الحالية / القيمة العادلة للأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4cddd-154">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-154">0.00</span></span>        |
| <span data-ttu-id="4cddd-155">الحد قصير الأجل</span><span class="sxs-lookup"><span data-stu-id="4cddd-155">Short-term threshold</span></span>                    | <span data-ttu-id="4cddd-156">0</span><span class="sxs-lookup"><span data-stu-id="4cddd-156">0</span></span>           |
| <span data-ttu-id="4cddd-157">حد القيمة المنخفضة</span><span class="sxs-lookup"><span data-stu-id="4cddd-157">Low Value Threshold</span></span>                     | <span data-ttu-id="4cddd-158">0</span><span class="sxs-lookup"><span data-stu-id="4cddd-158">0</span></span>           |
| <span data-ttu-id="4cddd-159">دفع للمورّد</span><span class="sxs-lookup"><span data-stu-id="4cddd-159">Pay to Vendor</span></span>                           | <span data-ttu-id="4cddd-160">لا</span><span class="sxs-lookup"><span data-stu-id="4cddd-160">No</span></span>          |

<span data-ttu-id="4cddd-161">**دفتر إلغاء قانوني**</span><span class="sxs-lookup"><span data-stu-id="4cddd-161">**Statutory reversal book**</span></span>

<span data-ttu-id="4cddd-162">يتم إعداد دفتر الإلغاء القانوني بنفس الطريقة التي يستخدمها الدفتر القانوني.</span><span class="sxs-lookup"><span data-stu-id="4cddd-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="4cddd-163">الاسم</span><span class="sxs-lookup"><span data-stu-id="4cddd-163">Name</span></span>                                    | <span data-ttu-id="4cddd-164">الوصف</span><span class="sxs-lookup"><span data-stu-id="4cddd-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="4cddd-165">نوع الدفتر</span><span class="sxs-lookup"><span data-stu-id="4cddd-165">Book type</span></span>                               | <span data-ttu-id="4cddd-166">قانوني – إلغاء</span><span class="sxs-lookup"><span data-stu-id="4cddd-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="4cddd-167">وصف الدفتر</span><span class="sxs-lookup"><span data-stu-id="4cddd-167">Book description</span></span>                        | <span data-ttu-id="4cddd-168">دفتر لإلغاء كتاب قانوني</span><span class="sxs-lookup"><span data-stu-id="4cddd-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="4cddd-169">طبقة الترحيل</span><span class="sxs-lookup"><span data-stu-id="4cddd-169">Posting Layer</span></span>                           | <span data-ttu-id="4cddd-170">الطبقة المخصصة 1</span><span class="sxs-lookup"><span data-stu-id="4cddd-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="4cddd-171">نوع عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="4cddd-171">Lease Type</span></span>                              | <span data-ttu-id="4cddd-172">تلقائي</span><span class="sxs-lookup"><span data-stu-id="4cddd-172">Automatic</span></span>                      |
| <span data-ttu-id="4cddd-173">الإطار المحاسبي</span><span class="sxs-lookup"><span data-stu-id="4cddd-173">Accounting Framework</span></span>                    | <span data-ttu-id="4cddd-174">الأساس النقدي</span><span class="sxs-lookup"><span data-stu-id="4cddd-174">Cash basis</span></span>                     |
| <span data-ttu-id="4cddd-175">إعداد فترة الإيجار / العمر الإنتاجي</span><span class="sxs-lookup"><span data-stu-id="4cddd-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4cddd-176">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-176">0.00</span></span>                           |
| <span data-ttu-id="4cddd-177">إعداد القيمة الحالية / القيمة العادلة للأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4cddd-178">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-178">0.00</span></span>                           |
| <span data-ttu-id="4cddd-179">الحد قصير الأجل</span><span class="sxs-lookup"><span data-stu-id="4cddd-179">Short-term threshold</span></span>                    | <span data-ttu-id="4cddd-180">0</span><span class="sxs-lookup"><span data-stu-id="4cddd-180">0</span></span>                              |
| <span data-ttu-id="4cddd-181">حد القيمة المنخفضة</span><span class="sxs-lookup"><span data-stu-id="4cddd-181">Low Value Threshold</span></span>                     | <span data-ttu-id="4cddd-182">0</span><span class="sxs-lookup"><span data-stu-id="4cddd-182">0</span></span>                              |
| <span data-ttu-id="4cddd-183">دفع للمورّد</span><span class="sxs-lookup"><span data-stu-id="4cddd-183">Pay to Vendor</span></span>                           | <span data-ttu-id="4cddd-184">لا</span><span class="sxs-lookup"><span data-stu-id="4cddd-184">No</span></span>                             |

<span data-ttu-id="4cddd-185">بالنسبة لهذا المثال، تم إنشاء عقد إيجار يحتوي على الإعدادات التالية في علامات التبويب **عام** و **بنود جدول الدفع**.</span><span class="sxs-lookup"><span data-stu-id="4cddd-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="4cddd-186">**علامة التبويب عام**</span><span class="sxs-lookup"><span data-stu-id="4cddd-186">**General tab**</span></span>

| <span data-ttu-id="4cddd-187">الحقل</span><span class="sxs-lookup"><span data-stu-id="4cddd-187">Field</span></span>                      | <span data-ttu-id="4cddd-188">قيمة</span><span class="sxs-lookup"><span data-stu-id="4cddd-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="4cddd-189">سعر الفائدة على الاقتراض الإضافي</span><span class="sxs-lookup"><span data-stu-id="4cddd-189">Incremental borrowing rate</span></span> | <span data-ttu-id="4cddd-190">5%</span><span class="sxs-lookup"><span data-stu-id="4cddd-190">5%</span></span>               |
| <span data-ttu-id="4cddd-191">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="4cddd-191">Commencement date</span></span>          | <span data-ttu-id="4cddd-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="4cddd-192">1/1/2020</span></span>         |
| <span data-ttu-id="4cddd-193">مجموعة عقود الإيجار‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-193">Lease group</span></span>                | <span data-ttu-id="4cddd-194">مباني</span><span class="sxs-lookup"><span data-stu-id="4cddd-194">Buildings</span></span>        |
| <span data-ttu-id="4cddd-195">المورّد</span><span class="sxs-lookup"><span data-stu-id="4cddd-195">Vendor</span></span>                     | <span data-ttu-id="4cddd-196">1001</span><span class="sxs-lookup"><span data-stu-id="4cddd-196">1001</span></span>             |
| <span data-ttu-id="4cddd-197">القيمة العادلة للأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-197">Fair value of the asset</span></span>    | <span data-ttu-id="4cddd-198">245,000</span><span class="sxs-lookup"><span data-stu-id="4cddd-198">245,000</span></span>          |
| <span data-ttu-id="4cddd-199">العمر الإنتاجي للأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-199">Asset useful life</span></span>          | <span data-ttu-id="4cddd-200">120</span><span class="sxs-lookup"><span data-stu-id="4cddd-200">120</span></span>              |
| <span data-ttu-id="4cddd-201">نوع الاستحقاق السنوي</span><span class="sxs-lookup"><span data-stu-id="4cddd-201">Annuity type</span></span>               | <span data-ttu-id="4cddd-202">الاستحقاق السنوي العادي</span><span class="sxs-lookup"><span data-stu-id="4cddd-202">Ordinary annuity</span></span> |
| <span data-ttu-id="4cddd-203">فاصل متراكب</span><span class="sxs-lookup"><span data-stu-id="4cddd-203">Compounding interval</span></span>       | <span data-ttu-id="4cddd-204">شهري</span><span class="sxs-lookup"><span data-stu-id="4cddd-204">Monthly</span></span>          |

<span data-ttu-id="4cddd-205">**علامة التبويب بنود جدول الدفع**</span><span class="sxs-lookup"><span data-stu-id="4cddd-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="4cddd-206">الحقل</span><span class="sxs-lookup"><span data-stu-id="4cddd-206">Field</span></span>             | <span data-ttu-id="4cddd-207">قيمة</span><span class="sxs-lookup"><span data-stu-id="4cddd-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="4cddd-208">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="4cddd-208">Start date</span></span>        | <span data-ttu-id="4cddd-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="4cddd-209">1/1/2020</span></span>   |
| <span data-ttu-id="4cddd-210">الفترة الزمنية</span><span class="sxs-lookup"><span data-stu-id="4cddd-210">Period interval</span></span>   | <span data-ttu-id="4cddd-211">أشهر</span><span class="sxs-lookup"><span data-stu-id="4cddd-211">Months</span></span>     |
| <span data-ttu-id="4cddd-212">الفترات</span><span class="sxs-lookup"><span data-stu-id="4cddd-212">Periods</span></span>           | <span data-ttu-id="4cddd-213">24</span><span class="sxs-lookup"><span data-stu-id="4cddd-213">24</span></span>         |
| <span data-ttu-id="4cddd-214">تاريخ الانتهاء</span><span class="sxs-lookup"><span data-stu-id="4cddd-214">End date</span></span>          | <span data-ttu-id="4cddd-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="4cddd-215">12/31/2020</span></span> |
| <span data-ttu-id="4cddd-216">تكرار الدفع</span><span class="sxs-lookup"><span data-stu-id="4cddd-216">Payment frequency</span></span> | <span data-ttu-id="4cddd-217">شهري</span><span class="sxs-lookup"><span data-stu-id="4cddd-217">Monthly</span></span>    |
| <span data-ttu-id="4cddd-218">مبلغ الدفع</span><span class="sxs-lookup"><span data-stu-id="4cddd-218">Payment amount</span></span>    | <span data-ttu-id="4cddd-219">1,000</span><span class="sxs-lookup"><span data-stu-id="4cddd-219">1,000</span></span>      |

<span data-ttu-id="4cddd-220">لحساب عقد الإيجار هذا ضمن إطاري عمل، فإنك تستخدم طبقة ترحيل حالية وطبقة ترحيل مخصصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="4cddd-221">يعرض الجدول التالي مثالاً لكل إدخال من إدخالات دفتر اليومية المطلوبة لتقديم الأمور المالية بشكل منتظم ضمن كل مقاييس التقارير.</span><span class="sxs-lookup"><span data-stu-id="4cddd-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="4cddd-222">يتم تقديم وصف تفصيلي لكل إدخال في دفتر اليومية لأول شهر من عقد الإيجار بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="4cddd-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="4cddd-223">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="4cddd-224">الوصف</span><span class="sxs-lookup"><span data-stu-id="4cddd-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="4cddd-225">دفتر قانوني (الطبقة الحالية)</span><span class="sxs-lookup"><span data-stu-id="4cddd-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4cddd-226">إجمالي الطبقة الحالية</span><span class="sxs-lookup"><span data-stu-id="4cddd-226">Current layer total</span></span></th>
<th><span data-ttu-id="4cddd-227">لدفتر الإلغاء (طبقة مخصصة)</span><span class="sxs-lookup"><span data-stu-id="4cddd-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="4cddd-228">دفتر معايير IFRS 16 (طبقة مخصصة)</span><span class="sxs-lookup"><span data-stu-id="4cddd-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4cddd-229">الطبقة الحالية + إجمالي الطبقة المخصصة</span><span class="sxs-lookup"><span data-stu-id="4cddd-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4cddd-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="4cddd-230">JE-100</span></span></th>
<th><span data-ttu-id="4cddd-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="4cddd-231">JE-110</span></span></th>
<th><span data-ttu-id="4cddd-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="4cddd-232">JE-120</span></span></th>
<th><span data-ttu-id="4cddd-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="4cddd-233">JE-130</span></span></th>
<th><span data-ttu-id="4cddd-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="4cddd-234">JE-140</span></span></th>
<th><span data-ttu-id="4cddd-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="4cddd-235">JE-150</span></span></th>
<th><span data-ttu-id="4cddd-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="4cddd-236">JE-160</span></span></th>
<th><span data-ttu-id="4cddd-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="4cddd-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4cddd-238">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-239">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-240">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-241">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-242">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-243">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-244">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-245">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4cddd-246">1</span><span class="sxs-lookup"><span data-stu-id="4cddd-246">1</span></span></td>
<td><span data-ttu-id="4cddd-247">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-247">Lease expense</span></span></td>
<td><span data-ttu-id="4cddd-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-249">1,000.00</span></span></td>
<td><span data-ttu-id="4cddd-250">-1000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-251">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-252">2</span><span class="sxs-lookup"><span data-stu-id="4cddd-252">2</span></span></td>
<td><span data-ttu-id="4cddd-253">رسوم بنكية</span><span class="sxs-lookup"><span data-stu-id="4cddd-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-254">3.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-255">3.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-256">3.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-257">3</span><span class="sxs-lookup"><span data-stu-id="4cddd-257">3</span></span></td>
<td><span data-ttu-id="4cddd-258">مصروفات ضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="4cddd-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-259">5.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-260">5.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-261">5.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-262">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-262">4</span></span></td>
<td><span data-ttu-id="4cddd-263">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-263">Clearing account</span></span></td>
<td><span data-ttu-id="4cddd-264">-1000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-264">-1,000.00</span></span></td>
<td><span data-ttu-id="4cddd-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-266">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-266">0.00</span></span></td>
<td><span data-ttu-id="4cddd-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-268">-1000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-269">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-270">5</span><span class="sxs-lookup"><span data-stu-id="4cddd-270">5</span></span></td>
<td><span data-ttu-id="4cddd-271">الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="4cddd-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-272">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-272">-1,008.00</span></span></td>
<td><span data-ttu-id="4cddd-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-273">1,008.00</span></span></td>
<td><span data-ttu-id="4cddd-274">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-275">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-276">6</span><span class="sxs-lookup"><span data-stu-id="4cddd-276">6</span></span></td>
<td><span data-ttu-id="4cddd-277">حق استخدام الأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-278">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4cddd-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-281">7</span><span class="sxs-lookup"><span data-stu-id="4cddd-281">7</span></span></td>
<td><span data-ttu-id="4cddd-282">التزام التأجير التمويلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-283">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-284">-22.794.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-284">-22,794.00</span></span></td>
<td><span data-ttu-id="4cddd-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-285">1,000.00</span></span></td>
<td><span data-ttu-id="4cddd-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-287">-21.888.87</span><span class="sxs-lookup"><span data-stu-id="4cddd-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-288">8</span><span class="sxs-lookup"><span data-stu-id="4cddd-288">8</span></span></td>
<td><span data-ttu-id="4cddd-289">مصروفات الفائدة</span><span class="sxs-lookup"><span data-stu-id="4cddd-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-290">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-291">94.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-292">94.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-293">9</span><span class="sxs-lookup"><span data-stu-id="4cddd-293">9</span></span></td>
<td><span data-ttu-id="4cddd-294">نقدي</span><span class="sxs-lookup"><span data-stu-id="4cddd-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-295">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-295">-1,008.00</span></span></td>
<td><span data-ttu-id="4cddd-296">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-297">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-298">10</span><span class="sxs-lookup"><span data-stu-id="4cddd-298">10</span></span></td>
<td><span data-ttu-id="4cddd-299">مصروفات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-300">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-301">949.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-301">949.75</span></span></td>
<td><span data-ttu-id="4cddd-302">949.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-303">11</span><span class="sxs-lookup"><span data-stu-id="4cddd-303">11</span></span></td>
<td><span data-ttu-id="4cddd-304">مجمع الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-305">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-306">-949.75</span></span></td>
<td><span data-ttu-id="4cddd-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4cddd-308">كما يوضح الجدول السابق، تكون ثلاثة دفاتر مطلوبة للتقرير بموجب كلاً من التقرير القانوني وتقارير معايير IFRS.</span><span class="sxs-lookup"><span data-stu-id="4cddd-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="4cddd-309">يقوم الدفتر القانوني بتسجيل دفعات الإيجار وفقًا لقواعد المحاسبة على أساس النقد ضمن الطبقة الحالية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="4cddd-310">يعمل دفتر الإلغاء القانوني على إلغاء إدخالات دفتر اليومية القانونية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="4cddd-311">يقوم دفتر معايير IFRS 16 بإنشاء إدخالات دفتر اليومية المطلوبة ضمن معايير IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="4cddd-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="4cddd-312">يجب عليك إدخال عقد إيجار مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="4cddd-312">You must enter a lease only one time.</span></span> <span data-ttu-id="4cddd-313">يمكنك بعد ذلك فتح الصفحة **دفاتر** لمشاهدة كافة الدفاتر المقترنة بعقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="4cddd-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="4cddd-314">عند إنشاء الدفاتر، يجب أن تكون كافة الدفاتر الثلاثة مقترنة بسجل عقد الإيجار نفسه.</span><span class="sxs-lookup"><span data-stu-id="4cddd-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="4cddd-315">ويعمل الإدخال الأول لدفتر اليومية على تسجيل مصروفات عقد الإيجار ضمن الدفتر القانوني.</span><span class="sxs-lookup"><span data-stu-id="4cddd-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="4cddd-316">يمكنك إنشاء مدفوعات إما في مجموعة أو عن طريق تحديد جدول الدفع في الدفتر القانوني.</span><span class="sxs-lookup"><span data-stu-id="4cddd-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="4cddd-317">بالنسبة لهذا المثال، يتم إنتاج إدخال دفتر اليومية التالي لدفتر قانوني من جدول الدفع.</span><span class="sxs-lookup"><span data-stu-id="4cddd-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="4cddd-318">دفعات الإيجار – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="4cddd-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="4cddd-319">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-319">Account type</span></span> | <span data-ttu-id="4cddd-320">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-320">Account number</span></span> | <span data-ttu-id="4cddd-321">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-321">Layer</span></span>   | <span data-ttu-id="4cddd-322">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-322">Account description</span></span> | <span data-ttu-id="4cddd-323">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-323">Debit</span></span>    | <span data-ttu-id="4cddd-324">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4cddd-325">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-325">Ledger</span></span>       | <span data-ttu-id="4cddd-326">1</span><span class="sxs-lookup"><span data-stu-id="4cddd-326">1</span></span>              | <span data-ttu-id="4cddd-327">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-327">Current</span></span> | <span data-ttu-id="4cddd-328">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-328">Lease expense</span></span>       | <span data-ttu-id="4cddd-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-329">1,000.00</span></span> |          |
| <span data-ttu-id="4cddd-330">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-330">Ledger</span></span>       | <span data-ttu-id="4cddd-331">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-331">4</span></span>              | <span data-ttu-id="4cddd-332">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-332">Current</span></span> | <span data-ttu-id="4cddd-333">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-333">Clearing account</span></span>    |          | <span data-ttu-id="4cddd-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-334">1,000.00</span></span> |

<span data-ttu-id="4cddd-335">يستخدم أحد موظفي الحسابات الدائنة وظيفة Dynamics 365 القياسية لإنشاء فاتورة لدفع الإيجار خارج تأجير الأصل.</span><span class="sxs-lookup"><span data-stu-id="4cddd-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="4cddd-336">ومع ذلك، فبدلاً من تحديد **مصروفات الإيجار** كحساب مدين، يقوم موظف الحسابات الدائنة بتحديد حساب المقاصة لإنشاء الإدخال التالي.</span><span class="sxs-lookup"><span data-stu-id="4cddd-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="4cddd-337">معالجة AP – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="4cddd-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="4cddd-338">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-338">Account type</span></span> | <span data-ttu-id="4cddd-339">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-339">Account number</span></span> | <span data-ttu-id="4cddd-340">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-340">Layer</span></span>   | <span data-ttu-id="4cddd-341">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-341">Account description</span></span> | <span data-ttu-id="4cddd-342">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-342">Debit</span></span>    | <span data-ttu-id="4cddd-343">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4cddd-344">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-344">Ledger</span></span>       | <span data-ttu-id="4cddd-345">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-345">4</span></span>              | <span data-ttu-id="4cddd-346">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-346">Current</span></span> | <span data-ttu-id="4cddd-347">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-347">Clearing account</span></span>    | <span data-ttu-id="4cddd-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-348">1,000.00</span></span> |          |
| <span data-ttu-id="4cddd-349">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-349">Ledger</span></span>       | <span data-ttu-id="4cddd-350">2</span><span class="sxs-lookup"><span data-stu-id="4cddd-350">2</span></span>              | <span data-ttu-id="4cddd-351">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-351">Current</span></span> | <span data-ttu-id="4cddd-352">رسوم بنكية</span><span class="sxs-lookup"><span data-stu-id="4cddd-352">Bank fee</span></span>            | <span data-ttu-id="4cddd-353">3.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-353">3.00</span></span>     |          |
| <span data-ttu-id="4cddd-354">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-354">Ledger</span></span>       | <span data-ttu-id="4cddd-355">3</span><span class="sxs-lookup"><span data-stu-id="4cddd-355">3</span></span>              | <span data-ttu-id="4cddd-356">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-356">Current</span></span> | <span data-ttu-id="4cddd-357">مصروفات ضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="4cddd-357">VAT expense</span></span>         | <span data-ttu-id="4cddd-358">5.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-358">5.00</span></span>     |          |
| <span data-ttu-id="4cddd-359">المورّد</span><span class="sxs-lookup"><span data-stu-id="4cddd-359">Vendor</span></span>       | <span data-ttu-id="4cddd-360">5</span><span class="sxs-lookup"><span data-stu-id="4cddd-360">5</span></span>              | <span data-ttu-id="4cddd-361">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-361">Current</span></span> | <span data-ttu-id="4cddd-362">الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="4cddd-362">Accounts payable</span></span>    |          | <span data-ttu-id="4cddd-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-363">1,008.00</span></span> |

<span data-ttu-id="4cddd-364">عند إصدار كشف الحساب للمورد، فإنك بذلك تتبع عملية الدفع العادية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="4cddd-365">وأثناء هذه العملية، يتم إنشاء إدخال دفتر اليومية التالي.</span><span class="sxs-lookup"><span data-stu-id="4cddd-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="4cddd-366">الدفع النقدي – 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="4cddd-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="4cddd-367">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-367">Account type</span></span> | <span data-ttu-id="4cddd-368">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-368">Account number</span></span> | <span data-ttu-id="4cddd-369">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-369">Layer</span></span>   | <span data-ttu-id="4cddd-370">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-370">Account description</span></span> | <span data-ttu-id="4cddd-371">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-371">Debit</span></span>    | <span data-ttu-id="4cddd-372">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4cddd-373">المورّد</span><span class="sxs-lookup"><span data-stu-id="4cddd-373">Vendor</span></span>       | <span data-ttu-id="4cddd-374">5</span><span class="sxs-lookup"><span data-stu-id="4cddd-374">5</span></span>              | <span data-ttu-id="4cddd-375">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-375">Current</span></span> | <span data-ttu-id="4cddd-376">حسابات دائنة</span><span class="sxs-lookup"><span data-stu-id="4cddd-376">Accounts Payable</span></span>    | <span data-ttu-id="4cddd-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-377">1,008.00</span></span> |          |
| <span data-ttu-id="4cddd-378">البنك</span><span class="sxs-lookup"><span data-stu-id="4cddd-378">Bank</span></span>         | <span data-ttu-id="4cddd-379">9</span><span class="sxs-lookup"><span data-stu-id="4cddd-379">9</span></span>              | <span data-ttu-id="4cddd-380">حالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-380">Current</span></span> | <span data-ttu-id="4cddd-381">نقدي</span><span class="sxs-lookup"><span data-stu-id="4cddd-381">Cash</span></span>                |          | <span data-ttu-id="4cddd-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-382">1,008.00</span></span> |

<span data-ttu-id="4cddd-383">وعند هذه النقطة، قد قمت بحساب الإيجار هذا بشكل كامل ضمن متطلبات التقارير القانونية ويمكنها إنشاء ميزان مراجعة باستخدام الطبقة الحالية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="4cddd-384">يقوم النظام بإرجاع ميزان مراجعة يحتوي على الأرقام التالية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="4cddd-385">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="4cddd-386">الوصف</span><span class="sxs-lookup"><span data-stu-id="4cddd-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="4cddd-387">دفتر قانوني (الطبقة الحالية)</span><span class="sxs-lookup"><span data-stu-id="4cddd-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4cddd-388">إجمالي الطبقة الحالية</span><span class="sxs-lookup"><span data-stu-id="4cddd-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4cddd-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="4cddd-389">JE-100</span></span></th>
<th><span data-ttu-id="4cddd-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="4cddd-390">JE-110</span></span></th>
<th><span data-ttu-id="4cddd-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="4cddd-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4cddd-392">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-393">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4cddd-394">مدين، دائن</span><span class="sxs-lookup"><span data-stu-id="4cddd-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4cddd-395">1</span><span class="sxs-lookup"><span data-stu-id="4cddd-395">1</span></span></td>
<td><span data-ttu-id="4cddd-396">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-396">Lease expense</span></span></td>
<td><span data-ttu-id="4cddd-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-399">2</span><span class="sxs-lookup"><span data-stu-id="4cddd-399">2</span></span></td>
<td><span data-ttu-id="4cddd-400">رسوم بنكية</span><span class="sxs-lookup"><span data-stu-id="4cddd-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-401">3.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-402">3.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-403">3</span><span class="sxs-lookup"><span data-stu-id="4cddd-403">3</span></span></td>
<td><span data-ttu-id="4cddd-404">مصروفات ضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="4cddd-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-405">5.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-406">5.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-407">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-407">4</span></span></td>
<td><span data-ttu-id="4cddd-408">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-408">Clearing account</span></span></td>
<td><span data-ttu-id="4cddd-409">-1000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-409">-1,000.00</span></span></td>
<td><span data-ttu-id="4cddd-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-411">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-412">5</span><span class="sxs-lookup"><span data-stu-id="4cddd-412">5</span></span></td>
<td><span data-ttu-id="4cddd-413">الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="4cddd-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="4cddd-414">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-414">-1,008.00</span></span></td>
<td><span data-ttu-id="4cddd-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-415">1,008.00</span></span></td>
<td><span data-ttu-id="4cddd-416">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-417">6</span><span class="sxs-lookup"><span data-stu-id="4cddd-417">6</span></span></td>
<td><span data-ttu-id="4cddd-418">حق استخدام الأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-419">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-420">7</span><span class="sxs-lookup"><span data-stu-id="4cddd-420">7</span></span></td>
<td><span data-ttu-id="4cddd-421">التزام التأجير التمويلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-422">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-423">8</span><span class="sxs-lookup"><span data-stu-id="4cddd-423">8</span></span></td>
<td><span data-ttu-id="4cddd-424">مصروفات الفائدة</span><span class="sxs-lookup"><span data-stu-id="4cddd-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-425">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-426">9</span><span class="sxs-lookup"><span data-stu-id="4cddd-426">9</span></span></td>
<td><span data-ttu-id="4cddd-427">نقدي</span><span class="sxs-lookup"><span data-stu-id="4cddd-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-428">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-428">-1,008.00</span></span></td>
<td><span data-ttu-id="4cddd-429">-1.008.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-430">10</span><span class="sxs-lookup"><span data-stu-id="4cddd-430">10</span></span></td>
<td><span data-ttu-id="4cddd-431">مصروفات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-432">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4cddd-433">11</span><span class="sxs-lookup"><span data-stu-id="4cddd-433">11</span></span></td>
<td><span data-ttu-id="4cddd-434">مجمع الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4cddd-435">0.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4cddd-436">إذا كنت ترغب في استخدام أرقام معايير IFRS 16 لتشغيل ميزان المراجعة نفسه، فإنه يجب إلغاء إدخالات دفتر يومية المحاسبة القانونية، كما يجب ترحيل إدخالات دفتر يومية معايير IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="4cddd-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="4cddd-437">لإلغاء إدخالات دفتر اليومية القانوني، يتضمن هذا المثال دفتر الإلغاء قانوني الذي له الإعداد نفسه الخاص بالدفتر القانوني ما عدا ملف تعريف الترحيل المقابل.</span><span class="sxs-lookup"><span data-stu-id="4cddd-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="4cddd-438">على سبيل المثال، عمل الدفتر القانوني على *خصم* حساب مصروفات الإيجار، ولكن سيقوم دفتر الإلغاء *بوضع مبلغ دائن* بهذا الحساب.</span><span class="sxs-lookup"><span data-stu-id="4cddd-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="4cddd-439">يتم تحديد هذه العلاقات بسهولة في حسابات تأجير الأصول على الصفحة **معلمات تأجير الأصول** (**تأجير الأصول \> الإعداد \> معلمات تأجير الأصول**).</span><span class="sxs-lookup"><span data-stu-id="4cddd-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="4cddd-440">عند استخدام نفس العملية التي تم استخدامها مع الدفتر القانوني لدفتر الإلغاء، فإنه يتم إنشاء إدخال دفتر اليومية التالي.</span><span class="sxs-lookup"><span data-stu-id="4cddd-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="4cddd-441">والفرق هو أن دفتر الإلغاء يحجز إدخالات الإلغاء من الدفتر القانوني.</span><span class="sxs-lookup"><span data-stu-id="4cddd-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="4cddd-442">كذلك، يتم إجراء إدخالات الإلغاء على الطبقة المخصصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="4cddd-443">عند تشغيل ميزان المراجعة في الطبقة الحالية، فإنه لا يتم تضمين إدخالات دفتر يومية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="4cddd-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="4cddd-444">دفعات الإيجار – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="4cddd-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="4cddd-445">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-445">Account type</span></span> | <span data-ttu-id="4cddd-446">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-446">Account number</span></span> | <span data-ttu-id="4cddd-447">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-447">Layer</span></span>  | <span data-ttu-id="4cddd-448">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-448">Account description</span></span> | <span data-ttu-id="4cddd-449">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-449">Debit</span></span>    | <span data-ttu-id="4cddd-450">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="4cddd-451">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-451">Ledger</span></span>       | <span data-ttu-id="4cddd-452">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-452">4</span></span>              | <span data-ttu-id="4cddd-453">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-453">Custom</span></span> | <span data-ttu-id="4cddd-454">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-454">Clearing account</span></span>    | <span data-ttu-id="4cddd-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-455">1,000.00</span></span> |          |
| <span data-ttu-id="4cddd-456">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-456">Ledger</span></span>       | <span data-ttu-id="4cddd-457">1</span><span class="sxs-lookup"><span data-stu-id="4cddd-457">1</span></span>              | <span data-ttu-id="4cddd-458">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-458">Custom</span></span> | <span data-ttu-id="4cddd-459">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-459">Lease expense</span></span>       |          | <span data-ttu-id="4cddd-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-460">1,000.00</span></span> |

<span data-ttu-id="4cddd-461">والآن بعد أن قمت بإزالة إدخالات دفتر اليومية القانوني، فإنك ستقوم بحجز كافة إدخالات دفتر اليومية التي تتطلبها معايير IFRS 16 في دفتر معايير IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="4cddd-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="4cddd-462">تتضمن هذه الإدخالات التقييم الأولي لحق استخدام الأصل والالتزام، وسجل الفائدة والإهلاك.</span><span class="sxs-lookup"><span data-stu-id="4cddd-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="4cddd-463">التقييم الأولي – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="4cddd-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="4cddd-464">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-464">Account type</span></span> | <span data-ttu-id="4cddd-465">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-465">Account number</span></span> | <span data-ttu-id="4cddd-466">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-466">Layer</span></span>  | <span data-ttu-id="4cddd-467">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-467">Account description</span></span>      | <span data-ttu-id="4cddd-468">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-468">Debit</span></span>     | <span data-ttu-id="4cddd-469">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="4cddd-470">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-470">Ledger</span></span>       | <span data-ttu-id="4cddd-471">6</span><span class="sxs-lookup"><span data-stu-id="4cddd-471">6</span></span>              | <span data-ttu-id="4cddd-472">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-472">Custom</span></span> | <span data-ttu-id="4cddd-473">حق استخدام الأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-473">ROU Asset</span></span>                | <span data-ttu-id="4cddd-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4cddd-474">22,793.90</span></span> |           |
| <span data-ttu-id="4cddd-475">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-475">Ledger</span></span>       | <span data-ttu-id="4cddd-476">7</span><span class="sxs-lookup"><span data-stu-id="4cddd-476">7</span></span>              | <span data-ttu-id="4cddd-477">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-477">Custom</span></span> | <span data-ttu-id="4cddd-478">التزام التأجير التمويلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-478">Finance lease obligation</span></span> |           | <span data-ttu-id="4cddd-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4cddd-479">22,793.90</span></span> |

<span data-ttu-id="4cddd-480">يتم ترحيل دفعات الإيجار مثل دفعات الإيجار الأخرى.</span><span class="sxs-lookup"><span data-stu-id="4cddd-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="4cddd-481">السبب في استخدام حساب المقاصة هو التأكد من أنه يتم وضع مبلغ نقد دائن مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="4cddd-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="4cddd-482">دفعات الإيجار – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="4cddd-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="4cddd-483">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-483">Account type</span></span> | <span data-ttu-id="4cddd-484">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-484">Account number</span></span> | <span data-ttu-id="4cddd-485">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-485">Layer</span></span>  | <span data-ttu-id="4cddd-486">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-486">Account description</span></span>      | <span data-ttu-id="4cddd-487">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-487">Debit</span></span>    | <span data-ttu-id="4cddd-488">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="4cddd-489">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-489">Ledger</span></span>       | <span data-ttu-id="4cddd-490">7</span><span class="sxs-lookup"><span data-stu-id="4cddd-490">7</span></span>              | <span data-ttu-id="4cddd-491">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-491">Custom</span></span> | <span data-ttu-id="4cddd-492">التزام التأجير التمويلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-492">Finance lease obligation</span></span> | <span data-ttu-id="4cddd-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-493">1,000.00</span></span> |          |
| <span data-ttu-id="4cddd-494">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-494">Ledger</span></span>       | <span data-ttu-id="4cddd-495">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-495">4</span></span>              | <span data-ttu-id="4cddd-496">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-496">Custom</span></span> | <span data-ttu-id="4cddd-497">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-497">Clearing account</span></span>         |          | <span data-ttu-id="4cddd-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-498">1,000.00</span></span> |

<span data-ttu-id="4cddd-499">يتم إنشاء إدخال دفتر يومية نفقات الفوائد من جدول إطفاء الدين الخاص بالالتزام.</span><span class="sxs-lookup"><span data-stu-id="4cddd-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="4cddd-500">نفقات الفوائد – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="4cddd-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="4cddd-501">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-501">Account type</span></span> | <span data-ttu-id="4cddd-502">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-502">Account number</span></span> | <span data-ttu-id="4cddd-503">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-503">Layer</span></span>  | <span data-ttu-id="4cddd-504">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-504">Account description</span></span>      | <span data-ttu-id="4cddd-505">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-505">Debit</span></span> | <span data-ttu-id="4cddd-506">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="4cddd-507">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-507">Ledger</span></span>       | <span data-ttu-id="4cddd-508">8</span><span class="sxs-lookup"><span data-stu-id="4cddd-508">8</span></span>              | <span data-ttu-id="4cddd-509">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-509">Custom</span></span> | <span data-ttu-id="4cddd-510">مصروفات الفائدة</span><span class="sxs-lookup"><span data-stu-id="4cddd-510">Interest expense</span></span>         | <span data-ttu-id="4cddd-511">94.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-511">94.97</span></span> |        |
| <span data-ttu-id="4cddd-512">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-512">Ledger</span></span>       | <span data-ttu-id="4cddd-513">7</span><span class="sxs-lookup"><span data-stu-id="4cddd-513">7</span></span>              | <span data-ttu-id="4cddd-514">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-514">Custom</span></span> | <span data-ttu-id="4cddd-515">التزام التأجير التمويلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-515">Finance lease obligation</span></span> |       | <span data-ttu-id="4cddd-516">94.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-516">94.97</span></span>  |

<span data-ttu-id="4cddd-517">يتم إنشاء إدخال دفتر يومية نفقات الإهلاك من جدول إهلاك الأصول.</span><span class="sxs-lookup"><span data-stu-id="4cddd-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="4cddd-518">‏‏مصروفات الإهلاك – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="4cddd-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="4cddd-519">نوع الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-519">Account type</span></span> | <span data-ttu-id="4cddd-520">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-520">Account number</span></span> | <span data-ttu-id="4cddd-521">الطبقة</span><span class="sxs-lookup"><span data-stu-id="4cddd-521">Layer</span></span>  | <span data-ttu-id="4cddd-522">وصف الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-522">Account description</span></span>      | <span data-ttu-id="4cddd-523">مدين</span><span class="sxs-lookup"><span data-stu-id="4cddd-523">Debit</span></span>  | <span data-ttu-id="4cddd-524">دائن‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="4cddd-525">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-525">Ledger</span></span>       | <span data-ttu-id="4cddd-526">10</span><span class="sxs-lookup"><span data-stu-id="4cddd-526">10</span></span>             | <span data-ttu-id="4cddd-527">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-527">Custom</span></span> | <span data-ttu-id="4cddd-528">مصروفات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-528">Depreciation expense</span></span>     | <span data-ttu-id="4cddd-529">949.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-529">949.75</span></span> |        |
| <span data-ttu-id="4cddd-530">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4cddd-530">Ledger</span></span>       | <span data-ttu-id="4cddd-531">11</span><span class="sxs-lookup"><span data-stu-id="4cddd-531">11</span></span>             | <span data-ttu-id="4cddd-532">مخصص</span><span class="sxs-lookup"><span data-stu-id="4cddd-532">Custom</span></span> | <span data-ttu-id="4cddd-533">مجمع الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="4cddd-534">949.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-534">949.75</span></span> |

<span data-ttu-id="4cddd-535">بعد إنشاء جميع إدخالات دفتر اليومية هذه وترحيلها، فإنك ستشاهد قيم "الطبقة المخصصة 1" التالية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="4cddd-536">لاحظ أن العمود الأخير يتضمن الرسوم البنكية ومصروفات ضريبة القيمة المضافة (VAT) والتخفيض النقدي من الطبقة السابقة، ولكنه لا يتضمن إدخالات دفتر اليومية للتقارير القانونية.</span><span class="sxs-lookup"><span data-stu-id="4cddd-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="4cddd-537">وبالتالي، يمكنك تحقيق القدرات الحقيقية المزدوجة للتقارير.</span><span class="sxs-lookup"><span data-stu-id="4cddd-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="4cddd-538">وفي هذه المرحلة، يجب على الشركة فقط تشغيل ميزان المراجعة الخاص بها، ودمج الطبقة الحالية والطبقة المخصصة لإنشاء ميزان المراجعة بمعايير IFRS.</span><span class="sxs-lookup"><span data-stu-id="4cddd-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="4cddd-539">رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="4cddd-539">Account No</span></span> | <span data-ttu-id="4cddd-540">الوصف</span><span class="sxs-lookup"><span data-stu-id="4cddd-540">Description</span></span>              | <span data-ttu-id="4cddd-541">الدفتر القانوني\-الطبقة الحالية\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-542">الدفتر القانوني\-الطبقة الحالية\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-543">الدفتر القانوني\-الطبقة الحالية\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-544">الطبقة الحالية \- الإجمالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="4cddd-545">دفتر الإلغاء\-الطبقة المخصصة\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-546">دفتر IFRS 16\-الطبقة المخصصة\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-547">دفتر IFRS 16\-الطبقة المخصصة\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-548">دفتر IFRS 16\-الطبقة المخصصة\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-549">دفتر IFRS 16\-الطبقة المخصصة\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4cddd-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="4cddd-550">الطبقة المخصصة \+ الطبقة الحالية \- الإجمالي</span><span class="sxs-lookup"><span data-stu-id="4cddd-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="4cddd-551">1</span><span class="sxs-lookup"><span data-stu-id="4cddd-551">1</span></span>          | <span data-ttu-id="4cddd-552">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="4cddd-552">Lease expense</span></span>            | <span data-ttu-id="4cddd-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="4cddd-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-554">1,000\.00</span></span>               |   | <span data-ttu-id="4cddd-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="4cddd-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="4cddd-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-556">0\.00</span></span>                                   |
| <span data-ttu-id="4cddd-557">2</span><span class="sxs-lookup"><span data-stu-id="4cddd-557">2</span></span>          | <span data-ttu-id="4cddd-558">رسوم بنكية</span><span class="sxs-lookup"><span data-stu-id="4cddd-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="4cddd-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="4cddd-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4cddd-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-561">3\.00</span></span>                                   |
| <span data-ttu-id="4cddd-562">3</span><span class="sxs-lookup"><span data-stu-id="4cddd-562">3</span></span>          | <span data-ttu-id="4cddd-563">مصروفات ضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="4cddd-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="4cddd-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="4cddd-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4cddd-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-566">5\.00</span></span>                                   |
| <span data-ttu-id="4cddd-567">4</span><span class="sxs-lookup"><span data-stu-id="4cddd-567">4</span></span>          | <span data-ttu-id="4cddd-568">حساب مقاصة.</span><span class="sxs-lookup"><span data-stu-id="4cddd-568">Clearing account</span></span>         | <span data-ttu-id="4cddd-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="4cddd-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="4cddd-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-571">0\.00</span></span>                   |   | <span data-ttu-id="4cddd-572">1,000</span><span class="sxs-lookup"><span data-stu-id="4cddd-572">1,000</span></span>                                           |                                                | <span data-ttu-id="4cddd-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="4cddd-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="4cddd-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-574">0\.00</span></span>                                   |
| <span data-ttu-id="4cddd-575">5</span><span class="sxs-lookup"><span data-stu-id="4cddd-575">5</span></span>          | <span data-ttu-id="4cddd-576">الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="4cddd-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="4cddd-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="4cddd-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-578">1,008\.00</span></span>                                         | <span data-ttu-id="4cddd-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4cddd-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-580">0\.00</span></span>                                   |
| <span data-ttu-id="4cddd-581">6</span><span class="sxs-lookup"><span data-stu-id="4cddd-581">6</span></span>          | <span data-ttu-id="4cddd-582">حق استخدام الأصل</span><span class="sxs-lookup"><span data-stu-id="4cddd-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="4cddd-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="4cddd-584">22,794</span><span class="sxs-lookup"><span data-stu-id="4cddd-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="4cddd-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="4cddd-585">22,793\.90</span></span>                              |
| <span data-ttu-id="4cddd-586">7</span><span class="sxs-lookup"><span data-stu-id="4cddd-586">7</span></span>          | <span data-ttu-id="4cddd-587">التزام التأجير التمويلي</span><span class="sxs-lookup"><span data-stu-id="4cddd-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="4cddd-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="4cddd-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="4cddd-589">\-22,794</span></span>                                       | <span data-ttu-id="4cddd-590">1,000</span><span class="sxs-lookup"><span data-stu-id="4cddd-590">1,000</span></span>                                          | <span data-ttu-id="4cddd-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="4cddd-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="4cddd-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="4cddd-593">8</span><span class="sxs-lookup"><span data-stu-id="4cddd-593">8</span></span>          | <span data-ttu-id="4cddd-594">مصروفات الفائدة</span><span class="sxs-lookup"><span data-stu-id="4cddd-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="4cddd-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="4cddd-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="4cddd-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="4cddd-597">94\.97</span></span>                                  |
| <span data-ttu-id="4cddd-598">9</span><span class="sxs-lookup"><span data-stu-id="4cddd-598">9</span></span>          | <span data-ttu-id="4cddd-599">نقدي</span><span class="sxs-lookup"><span data-stu-id="4cddd-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="4cddd-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="4cddd-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4cddd-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="4cddd-603">10</span><span class="sxs-lookup"><span data-stu-id="4cddd-603">10</span></span>         | <span data-ttu-id="4cddd-604">مصروفات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="4cddd-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="4cddd-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-606">949\.75</span></span>                                        | <span data-ttu-id="4cddd-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-607">949\.75</span></span>                                 |
| <span data-ttu-id="4cddd-608">11</span><span class="sxs-lookup"><span data-stu-id="4cddd-608">11</span></span>         | <span data-ttu-id="4cddd-609">مجمع الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4cddd-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="4cddd-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="4cddd-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="4cddd-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-611">\-949\.75</span></span>                                      | <span data-ttu-id="4cddd-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="4cddd-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]