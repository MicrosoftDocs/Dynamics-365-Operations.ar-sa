---
title: التقارير المالية لميزان المراجعة
description: توضح هذه المقالة التقارير الافتراضية لموازين المراجعة. كما توضح العناصر الأساسية التي تقترن بهذه التقارير وكيف يمكنك تعديل التقارير لتناسب متطلبات العمل الخاص بك.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103648"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="434ba-104">التقارير المالية لميزان المراجعة</span><span class="sxs-lookup"><span data-stu-id="434ba-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="434ba-105">توضح هذه المقالة التقارير الافتراضية لموازين المراجعة.</span><span class="sxs-lookup"><span data-stu-id="434ba-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="434ba-106">كما توضح العناصر الأساسية التي تقترن بهذه التقارير وكيف يمكنك تعديل التقارير لتناسب متطلبات العمل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="434ba-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="434ba-107">تقارير ميزان المراجعة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="434ba-107">Default trial balance reports</span></span>

<span data-ttu-id="434ba-108">تتوفر ثلاثة تقارير لميزان المراجعة في التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="434ba-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="434ba-109">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-109">Default report</span></span>                                 | <span data-ttu-id="434ba-110">مهامه</span><span class="sxs-lookup"><span data-stu-id="434ba-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="434ba-111">ميزان المراجعة المفصل - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="434ba-112">يوفر معلومات الرصيد لكافة الحسابات المشتملة على الأرصدة الدائنة والمدينة، وصافي هذه الأرصدة، إلى جانب تاريخ الحركة، والإيصال، ووصف دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="434ba-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="434ba-113">ميزان المراجعة الملخص - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="434ba-114">يوفر معلومات الرصيد لكافة الحسابات المشتملة على أرصدة افتتاح وإغلاق والأرصدة الدائنة والمدينة جنبًا إلى جنب مع صافي الفرق الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="434ba-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="434ba-115">ميزان المراجعة الملخص لعام بعد عام – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="434ba-116">يوفر معلومات الرصيد لكافة الحسابات المشتملة على أرصدة افتتاح وإغلاق والأرصدة الدائنة والمدينة جنبًا إلى جنب مع صافي الفرق للسنة الحالية والسنة الماضية.</span><span class="sxs-lookup"><span data-stu-id="434ba-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="434ba-117">اللبنات الأساسية</span><span class="sxs-lookup"><span data-stu-id="434ba-117">Building blocks</span></span>
<span data-ttu-id="434ba-118">تستخدم التقارير المالية لميزان المراجعة اللبنات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="434ba-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="434ba-119">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-119">Default report</span></span>                                 | <span data-ttu-id="434ba-120">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="434ba-120">Row definition</span></span>          | <span data-ttu-id="434ba-121">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="434ba-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="434ba-122">ميزان المراجعة المفصل - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="434ba-123">ميزان المراجعة - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-123">Trial Balance - Default</span></span> | <span data-ttu-id="434ba-124">ميزان المراجعة المفصل - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="434ba-125">ميزان المراجعة الملخص - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="434ba-126">ميزان المراجعة - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-126">Trial Balance - Default</span></span> | <span data-ttu-id="434ba-127">ميزان المراجعة الملخص - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="434ba-128">ميزان المراجعة الملخص لعام بعد عام – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="434ba-129">ميزان المراجعة - الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-129">Trial Balance - Default</span></span> | <span data-ttu-id="434ba-130">ميزان المراجعة الملخص لعام بعد عام – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="434ba-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="434ba-131">عند تشغيل التقرير **ميزان المراجعة** Financial reporting، تأكد من تحديد خانات الاختيار لـ **عرض الصفوف بدون مبالغ** و **عرض التقارير بدون صفوف نشطة** في علامة التبويب **إعدادات**.</span><span class="sxs-lookup"><span data-stu-id="434ba-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="434ba-132">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="434ba-132">Row definition</span></span>

<span data-ttu-id="434ba-133">‏‫تعريف الصف، ميزان المراجعة – الافتراضي، يحتوي على صف واحد يسحب كافة الحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="434ba-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="434ba-134">ولذلك، يمكن لأي شخص إنشاء التقرير دون الحاجة إلى إجراء أي تعديلات.</span><span class="sxs-lookup"><span data-stu-id="434ba-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="434ba-135">وعند عرض التقرير، يمكنك التنقل في صف واحد الحصول على تفاصيل حول كل حساب.</span><span class="sxs-lookup"><span data-stu-id="434ba-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="434ba-136">ويمكنك تعديل تعريف الصف بحيث يتضمن المزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="434ba-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="434ba-137">لتعديل ميزان المراجعة – تعريف الصف الافتراضي بحيث يتضمن الصفوف لكافة الحسابات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="434ba-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="434ba-138">انقر فوق **تحرير**، ثم انقر فوق **إدراج الصفوف من الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="434ba-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="434ba-139">يتيح لك أمر **إدراج الصفوف من الأبعاد** اختيار الأبعاد التي تريد توفرها في تعريف الصف الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="434ba-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="434ba-140">وفي تعريف الصف هذا، ستقوم باستخدام **الحساب الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="434ba-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="434ba-141">وتأكد من أن **الحساب الرئيسي** يحتوي على كافة علامات العطف (&)، وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="434ba-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="434ba-142">يحتوي تعريف الصف الآن على كافة الحسابات الرئيسية للكيان القانوني الافتراضي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="434ba-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="434ba-143">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="434ba-143">Column definition</span></span>

<span data-ttu-id="434ba-144">يستخدم تقرير ميزان المراجعة تعريف عمود مختلفًا.</span><span class="sxs-lookup"><span data-stu-id="434ba-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="434ba-145">وتحتوي تعريفات الأعمدة هذه على أنواع مختلفة من الأعمدة لتوفير مستويات مختلفة من التفاصيل والبيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="434ba-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="434ba-146">**ميزان المراجعة المفصل - أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="434ba-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="434ba-147">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="434ba-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="434ba-148">**ACCT** – أكواد الحساب</span><span class="sxs-lookup"><span data-stu-id="434ba-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="434ba-149">**ATTR (3)** – السمات:</span><span class="sxs-lookup"><span data-stu-id="434ba-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="434ba-150">تاريخ الحركة</span><span class="sxs-lookup"><span data-stu-id="434ba-150">Transaction Date</span></span>
        -   <span data-ttu-id="434ba-151">الإيصال</span><span class="sxs-lookup"><span data-stu-id="434ba-151">Voucher</span></span>
        -   <span data-ttu-id="434ba-152">وصف دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="434ba-152">Journal Description</span></span>
    -   <span data-ttu-id="434ba-153">**FD** – البيانات المالية التي تحتوي على الديون فقط</span><span class="sxs-lookup"><span data-stu-id="434ba-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="434ba-154">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط</span><span class="sxs-lookup"><span data-stu-id="434ba-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="434ba-155">**CALC** – صافي الفرق</span><span class="sxs-lookup"><span data-stu-id="434ba-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="434ba-156">**ميزان المراجعة الملخص - أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="434ba-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="434ba-157">**ACCT** – أكواد الحساب</span><span class="sxs-lookup"><span data-stu-id="434ba-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="434ba-158">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="434ba-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="434ba-159">**ATTR** – سمة:</span><span class="sxs-lookup"><span data-stu-id="434ba-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="434ba-160">الإيصال</span><span class="sxs-lookup"><span data-stu-id="434ba-160">Voucher</span></span>
    -   <span data-ttu-id="434ba-161">**FD** – البيانات المالية لوازنة البدء</span><span class="sxs-lookup"><span data-stu-id="434ba-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="434ba-162">**FD** – البيانات المالية التي تحتوي على الديون فقط</span><span class="sxs-lookup"><span data-stu-id="434ba-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="434ba-163">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط</span><span class="sxs-lookup"><span data-stu-id="434ba-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="434ba-164">**CALC** – صافي الفرق</span><span class="sxs-lookup"><span data-stu-id="434ba-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="434ba-165">**CALC** – رصيد الإقفال</span><span class="sxs-lookup"><span data-stu-id="434ba-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="434ba-166">**ميزان المراجعة الملخص لعام بعد عام – الافتراضي:**</span><span class="sxs-lookup"><span data-stu-id="434ba-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="434ba-167">**ACCT** – أكواد الحساب</span><span class="sxs-lookup"><span data-stu-id="434ba-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="434ba-168">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="434ba-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="434ba-169">**ATTR** – سمة</span><span class="sxs-lookup"><span data-stu-id="434ba-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="434ba-170">الإيصال</span><span class="sxs-lookup"><span data-stu-id="434ba-170">Voucher</span></span>
    -   <span data-ttu-id="434ba-171">**FD** – البيانات المالية لموازنة البدء للسنة الحالية</span><span class="sxs-lookup"><span data-stu-id="434ba-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="434ba-172">**FD** – البيانات المالية التي تحتوي على الديون فقط للسنة الحالية</span><span class="sxs-lookup"><span data-stu-id="434ba-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="434ba-173">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط للسنة الحالية</span><span class="sxs-lookup"><span data-stu-id="434ba-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="434ba-174">**CALC** – صافي الفرق</span><span class="sxs-lookup"><span data-stu-id="434ba-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="434ba-175">**CALC** – رصيد الإقفال</span><span class="sxs-lookup"><span data-stu-id="434ba-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="434ba-176">**FD** – البيانات المالية التي تحتوي على الديون فقط للسنة الأخيرة</span><span class="sxs-lookup"><span data-stu-id="434ba-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="434ba-177">**FD** – البيانات المالية التي تحتوي على الائتمانات فقط للسنة الأخيرة</span><span class="sxs-lookup"><span data-stu-id="434ba-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="434ba-178">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="434ba-178">Additional resources</span></span>

[<span data-ttu-id="434ba-179">نظرة عامة على التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="434ba-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="434ba-180">عرض التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="434ba-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="434ba-181">مدونة التقارير المالية في Dynamics</span><span class="sxs-lookup"><span data-stu-id="434ba-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
