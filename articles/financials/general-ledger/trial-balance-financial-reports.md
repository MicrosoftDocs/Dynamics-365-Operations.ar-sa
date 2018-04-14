---
title: "التقارير المالية لميزان المراجعة"
description: "توضح هذه المقالة التقارير الافتراضية لموازين المراجعة. كما توضح العناصر الأساسية التي تقترن بهذه التقارير وكيف يمكنك تعديل التقارير لتناسب متطلبات العمل الخاص بك."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7363ac8d83c5d8f9da550f76ad888a666149cd6e
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="d81b7-104">التقارير المالية لميزان المراجعة</span><span class="sxs-lookup"><span data-stu-id="d81b7-104">Trial balance financial reports</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d81b7-105">توضح هذه المقالة التقارير الافتراضية لموازين المراجعة.</span><span class="sxs-lookup"><span data-stu-id="d81b7-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="d81b7-106">كما توضح العناصر الأساسية التي تقترن بهذه التقارير وكيف يمكنك تعديل التقارير لتناسب متطلبات العمل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d81b7-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="d81b7-107">تقارير ميزان المراجعة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="d81b7-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="d81b7-108">تتوفر ثلاثة تقارير لميزان المراجعة في التقارير المالية في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d81b7-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="d81b7-109">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-109">Default report</span></span>                                 | <span data-ttu-id="d81b7-110">مهامه</span><span class="sxs-lookup"><span data-stu-id="d81b7-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81b7-111">ميزان المراجعة المفصل - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="d81b7-112">يوفر معلومات الرصيد لكافة الحسابات المشتملة على الأرصدة الدائنة والمدينة، وصافي هذه الأرصدة، إلى جانب تاريخ الحركة، والإيصال، ووصف دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="d81b7-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="d81b7-113">ميزان المراجعة الملخص - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="d81b7-114">يوفر معلومات الرصيد لكافة الحسابات المشتملة على أرصدة افتتاح وإغلاق والأرصدة الدائنة والمدينة جنبًا إلى جنب مع صافي الفرق الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="d81b7-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="d81b7-115">ميزان المراجعة الملخص لعام بعد عام – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="d81b7-116">يوفر معلومات الرصيد لكافة الحسابات المشتملة على أرصدة افتتاح وإغلاق والأرصدة الدائنة والمدينة جنبًا إلى جنب مع صافي الفرق للسنة الحالية والسنة الماضية.</span><span class="sxs-lookup"><span data-stu-id="d81b7-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="d81b7-117">اللبنات الأساسية</span><span class="sxs-lookup"><span data-stu-id="d81b7-117">Building blocks</span></span>
<span data-ttu-id="d81b7-118">تستخدم التقارير المالية لميزان المراجعة اللبنات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="d81b7-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="d81b7-119">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-119">Default report</span></span>                                 | <span data-ttu-id="d81b7-120">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="d81b7-120">Row definition</span></span>          | <span data-ttu-id="d81b7-121">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="d81b7-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="d81b7-122">ميزان المراجعة المفصل - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="d81b7-123">ميزان المراجعة - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-123">Trial Balance - Default</span></span> | <span data-ttu-id="d81b7-124">ميزان المراجعة المفصل - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="d81b7-125">ميزان المراجعة الملخص - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="d81b7-126">ميزان المراجعة - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-126">Trial Balance - Default</span></span> | <span data-ttu-id="d81b7-127">ميزان المراجعة الملخص - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="d81b7-128">ميزان المراجعة الملخص لعام بعد عام – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="d81b7-129">ميزان المراجعة - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-129">Trial Balance - Default</span></span> | <span data-ttu-id="d81b7-130">ميزان المراجعة الملخص لعام بعد عام – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d81b7-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="d81b7-131">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="d81b7-131">Row definition</span></span>

<span data-ttu-id="d81b7-132">‏‫تعريف الصف، ميزان المراجعة – الافتراضي، يحتوي على صف واحد يسحب كافة الحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="d81b7-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="d81b7-133">ولذلك، يمكن لأي شخص إنشاء التقرير دون الحاجة إلى إجراء أي تعديلات.</span><span class="sxs-lookup"><span data-stu-id="d81b7-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="d81b7-134">وعند عرض التقرير، يمكنك التنقل في صف واحد الحصول على تفاصيل حول كل حساب.</span><span class="sxs-lookup"><span data-stu-id="d81b7-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="d81b7-135">ويمكنك تعديل تعريف الصف بحيث يتضمن المزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="d81b7-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="d81b7-136">لتعديل ميزان المراجعة – تعريف الصف الافتراضي بحيث يتضمن الصفوف لكافة الحسابات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d81b7-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="d81b7-137">انقر فوق **تحرير**، ثم انقر فوق **إدراج الصفوف من الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="d81b7-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="d81b7-138">يتيح لك أمر **إدراج الصفوف من الأبعاد** اختيار الأبعاد التي تريد توفرها في تعريف الصف الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d81b7-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="d81b7-139">وفي تعريف الصف هذا، ستقوم باستخدام **الحساب الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="d81b7-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="d81b7-140">وتأكد من أن **الحساب الرئيسي** يحتوي على كافة علامات العطف (&)، وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d81b7-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="d81b7-141">يحتوي تعريف الصف الآن على كافة الحسابات الرئيسية للكيان القانوني الافتراضي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d81b7-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="d81b7-142">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="d81b7-142">Column definition</span></span>

<span data-ttu-id="d81b7-143">يستخدم تقرير ميزان المراجعة تعريف عمود مختلفًا.</span><span class="sxs-lookup"><span data-stu-id="d81b7-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="d81b7-144">وتحتوي تعريفات الأعمدة هذه على أنواع مختلفة من الأعمدة لتوفير مستويات مختلفة من التفاصيل والبيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="d81b7-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="d81b7-145">**ميزان المراجعة المفصل - أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="d81b7-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="d81b7-146">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="d81b7-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d81b7-147">**ACCT** – أكواد الحساب</span><span class="sxs-lookup"><span data-stu-id="d81b7-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d81b7-148">**ATTR (3)** – السمات:</span><span class="sxs-lookup"><span data-stu-id="d81b7-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="d81b7-149">تاريخ الحركة</span><span class="sxs-lookup"><span data-stu-id="d81b7-149">Transaction Date</span></span>
        -   <span data-ttu-id="d81b7-150">الإيصال</span><span class="sxs-lookup"><span data-stu-id="d81b7-150">Voucher</span></span>
        -   <span data-ttu-id="d81b7-151">وصف دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="d81b7-151">Journal Description</span></span>
    -   <span data-ttu-id="d81b7-152">**FD** – البيانات المالية التي تحتوي على الديون فقط</span><span class="sxs-lookup"><span data-stu-id="d81b7-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="d81b7-153">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط</span><span class="sxs-lookup"><span data-stu-id="d81b7-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="d81b7-154">**CALC** – صافي الفرق</span><span class="sxs-lookup"><span data-stu-id="d81b7-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="d81b7-155">**ميزان المراجعة الملخص - أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="d81b7-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="d81b7-156">**ACCT** – أكواد الحساب</span><span class="sxs-lookup"><span data-stu-id="d81b7-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d81b7-157">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="d81b7-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d81b7-158">**ATTR** – سمة:</span><span class="sxs-lookup"><span data-stu-id="d81b7-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="d81b7-159">الإيصال</span><span class="sxs-lookup"><span data-stu-id="d81b7-159">Voucher</span></span>
    -   <span data-ttu-id="d81b7-160">**FD** – البيانات المالية لوازنة البدء</span><span class="sxs-lookup"><span data-stu-id="d81b7-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="d81b7-161">**FD** – البيانات المالية التي تحتوي على الديون فقط</span><span class="sxs-lookup"><span data-stu-id="d81b7-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="d81b7-162">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط</span><span class="sxs-lookup"><span data-stu-id="d81b7-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="d81b7-163">**CALC** – صافي الفرق</span><span class="sxs-lookup"><span data-stu-id="d81b7-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="d81b7-164">**CALC** – رصيد الإقفال</span><span class="sxs-lookup"><span data-stu-id="d81b7-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="d81b7-165">**ميزان المراجعة الملخص لعام بعد عام – الافتراضي:**</span><span class="sxs-lookup"><span data-stu-id="d81b7-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="d81b7-166">**ACCT** – أكواد الحساب</span><span class="sxs-lookup"><span data-stu-id="d81b7-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d81b7-167">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="d81b7-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d81b7-168">**ATTR** – سمة</span><span class="sxs-lookup"><span data-stu-id="d81b7-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="d81b7-169">الإيصال</span><span class="sxs-lookup"><span data-stu-id="d81b7-169">Voucher</span></span>
    -   <span data-ttu-id="d81b7-170">**FD** – البيانات المالية لموازنة البدء للسنة الحالية</span><span class="sxs-lookup"><span data-stu-id="d81b7-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="d81b7-171">**FD** – البيانات المالية التي تحتوي على الديون فقط للسنة الحالية</span><span class="sxs-lookup"><span data-stu-id="d81b7-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="d81b7-172">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط للسنة الحالية</span><span class="sxs-lookup"><span data-stu-id="d81b7-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="d81b7-173">**CALC** – صافي الفرق</span><span class="sxs-lookup"><span data-stu-id="d81b7-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="d81b7-174">**CALC** – رصيد الإقفال</span><span class="sxs-lookup"><span data-stu-id="d81b7-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="d81b7-175">**FD** – البيانات المالية التي تحتوي على الديون فقط للسنة الأخيرة</span><span class="sxs-lookup"><span data-stu-id="d81b7-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="d81b7-176">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط للسنة الأخيرة</span><span class="sxs-lookup"><span data-stu-id="d81b7-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="see-also"></a><span data-ttu-id="d81b7-177">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d81b7-177">See also</span></span>
--------

[<span data-ttu-id="d81b7-178">التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="d81b7-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="d81b7-179">عرض التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="d81b7-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="d81b7-180">مدونة التقارير المالية في Dynamics</span><span class="sxs-lookup"><span data-stu-id="d81b7-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




