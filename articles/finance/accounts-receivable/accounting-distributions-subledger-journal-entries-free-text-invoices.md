---
title: التوزيعات المحاسبية وإدخالات دفتر اليومية بدفتر الأستاذ الفرعي لفواتير النص الحر
description: تُستخدم التوزيعات المحاسبية لتحديد كيفية حساب مبلغ، مثل كيفية حساب الإيراد أو الضريبة أو التكاليف في فاتورة ذات نص حر. وهناك توزيع محاسبي واحد أو أكثر لكل مبلغ يجب أن يحسب عند تسجيل فاتورة الموّرد في دفتر اليومية.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 515d0a9c35507fad04b776e1f0b6225ac5a162d3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189236"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="87acb-104">التوزيعات المحاسبية وإدخالات دفتر اليومية بدفتر الأستاذ الفرعي لفواتير النص الحر</span><span class="sxs-lookup"><span data-stu-id="87acb-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87acb-105">تُستخدم التوزيعات المحاسبية لتحديد كيفية حساب مبلغ، مثل كيفية حساب الإيراد أو الضريبة أو التكاليف في فاتورة ذات نص حر.</span><span class="sxs-lookup"><span data-stu-id="87acb-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="87acb-106">وهناك توزيع محاسبي واحد أو أكثر لكل مبلغ يجب أن يحسب عند تسجيل فاتورة الموّرد في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="87acb-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="87acb-107">التوزيعات المحاسبية</span><span class="sxs-lookup"><span data-stu-id="87acb-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="87acb-108">يمكنك استخدام الأزرار التالية في صفحة فاتورة النص الحر لعرض وربما تغيير التوزيعات المحاسبية لكل مبلغ على فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="87acb-109">**توزيع المبالغ**—عرض وتغيير التوزيعات المحاسبية لبند واحد لأية بنود فرعية، مثل الضرائب أو التكاليف.</span><span class="sxs-lookup"><span data-stu-id="87acb-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="87acb-110">يمكنك أيضًا عرض وتغيير التوزيعات المحاسبية لبند فرعي مباشرةً من صفحة حركات ضريبة المبيعات أو صفحة حركات الرسوم.</span><span class="sxs-lookup"><span data-stu-id="87acb-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="87acb-111">تغيير مبالغ رأس فاتورة النص الحر، مثل التكاليف أو المبالغ التقريبية للعملة.</span><span class="sxs-lookup"><span data-stu-id="87acb-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="87acb-112">تغيير مبالغ بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="87acb-113">**عرض التوزيعات** – عرض التوزيعات المحاسبية لكافة البنود في المستند.</span><span class="sxs-lookup"><span data-stu-id="87acb-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="87acb-114">لا يمكنك تغيير التوزيعات المحاسبية من طريقة العرض هذه.</span><span class="sxs-lookup"><span data-stu-id="87acb-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="87acb-115">اعرض مبالغ السطر والرأس.</span><span class="sxs-lookup"><span data-stu-id="87acb-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="87acb-116">توزيع المبالغ</span><span class="sxs-lookup"><span data-stu-id="87acb-116">Distributing amounts</span></span>
<span data-ttu-id="87acb-117">عندما تقوم بإدخال فاتورة النص الحر، سيتم توزيع كل مبلغ كما يلي.</span><span class="sxs-lookup"><span data-stu-id="87acb-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87acb-118">نوع المبلغ النقدي</span><span class="sxs-lookup"><span data-stu-id="87acb-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="87acb-119">التي تحدد من أين يتم عرض الحساب الرئيسي‬</span><span class="sxs-lookup"><span data-stu-id="87acb-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="87acb-120">ترتيب الأولوية التي تحدد أين يتم عرض الأبعاد المالية الافتراضية</span><span class="sxs-lookup"><span data-stu-id="87acb-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87acb-121">بند فاتورة النص الحر</span><span class="sxs-lookup"><span data-stu-id="87acb-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="87acb-122">حساب دفتر الأستاذ في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="87acb-123">إذا كان الحساب الرئيسي حساب توزيع، استخدم القيمة الافتراضية من تعريف حساب التوزيع.</span><span class="sxs-lookup"><span data-stu-id="87acb-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="87acb-124">إذا لم يكن الحساب الرئيسي هو حساب توزيع، فاستخدم القالب الافتراضي للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-125">استخدم القيم الافتراضية للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-126">استخدم القيم الافتراضية للبعد المالي من حساب دفتر الأستاذ في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="87acb-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87acb-127">بند فاتورة النص الحر لمجموعة نموذج القيمة ورقم الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="87acb-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="87acb-128"><strong>ملاحظة </strong></span><span class="sxs-lookup"><span data-stu-id="87acb-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87acb-129">سيكون الحساب الرئيسي في بند فاتورة النص الحر هو حساب التخلص من الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="87acb-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="87acb-130">حساب دفتر الأستاذ في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="87acb-131">استخدم القيم الافتراضية للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-132">استخدم القيم الافتراضية للبعد المالي من حساب دفتر الأستاذ في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="87acb-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87acb-133">مبلغ خصم فاتورة النص الحر</span><span class="sxs-lookup"><span data-stu-id="87acb-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="87acb-134">الحساب الرئيسي لحقل خصومات العميل في صفحة الخصومات النقدية.</span><span class="sxs-lookup"><span data-stu-id="87acb-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="87acb-135">إذا كان الحساب الرئيسي حساب توزيع، استخدم القيمة الافتراضية من تعريف حساب التوزيع.</span><span class="sxs-lookup"><span data-stu-id="87acb-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="87acb-136">إذا لم يكن الحساب الرئيسي هو حساب توزيع، فاستخدم القالب الافتراضي للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-137">استخدم القيم الافتراضية للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-138">استخدم القيم الافتراضية للبعد المالي من حساب دفتر الأستاذ في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="87acb-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87acb-139">مبلغ ضريبة مبيعات فاتورة النص الحر</span><span class="sxs-lookup"><span data-stu-id="87acb-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="87acb-140">حقل ضريبة المبيعات المستحقة في صفحة مجموعات ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="87acb-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="87acb-141">استخدم الأبعاد المالية التي يتم تحديدها في مبلغ بند فاتورة النص الحر أو التوزيعات لمبلغ بند المصاريف.</span><span class="sxs-lookup"><span data-stu-id="87acb-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="87acb-142">استخدم القيم الافتراضية للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-143">استخدم القيم الافتراضية للبعد المالي من حساب دفتر الأستاذ في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="87acb-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87acb-144">مبلغ بند رسوم فاتورة النص الحر</span><span class="sxs-lookup"><span data-stu-id="87acb-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="87acb-145">حقل الحساب الدائن في صفحة كود المصاريف.</span><span class="sxs-lookup"><span data-stu-id="87acb-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="87acb-146">إذا كان الحساب الرئيسي حساب توزيع، استخدم القيمة الافتراضية من تعريف حساب التوزيع.</span><span class="sxs-lookup"><span data-stu-id="87acb-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="87acb-147">إذا لم يكن الحساب الرئيسي هو حساب توزيع، فاستخدم القالب الافتراضي للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-148">استخدم القيم الافتراضية للبعد المالي في بند فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="87acb-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="87acb-149">استخدم القيم الافتراضية للبعد المالي من حساب دفتر الأستاذ في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="87acb-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="87acb-150">توزيع الضرائب</span><span class="sxs-lookup"><span data-stu-id="87acb-150">Distributing taxes</span></span>
<span data-ttu-id="87acb-151">يتعذر إنشاء توزيعات محاسبية للضرائب إلا بعد أن يتم حساب الضرائب.</span><span class="sxs-lookup"><span data-stu-id="87acb-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="87acb-152">لحساب ضرائب المبيعات، يجب إكمال إحدى المهام التالية في نموذج فاتورة النص الحر:</span><span class="sxs-lookup"><span data-stu-id="87acb-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="87acb-153">عرض ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="87acb-153">View the sales tax.</span></span>
-   <span data-ttu-id="87acb-154">عرض إجمالي الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="87acb-154">View the invoice total.</span></span>
-   <span data-ttu-id="87acb-155">عرض التدفق النقدي.</span><span class="sxs-lookup"><span data-stu-id="87acb-155">View the cash flow.</span></span>
-   <span data-ttu-id="87acb-156">اعرض التوزيعات المحاسبية لفاتورة النص الحر بالكامل.</span><span class="sxs-lookup"><span data-stu-id="87acb-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="87acb-157">عرض دفتر اليومية بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="87acb-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="87acb-158"> دفاتر يومية دفتر الأستاذ الفرعي لفواتير النص الحر</span><span class="sxs-lookup"><span data-stu-id="87acb-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="87acb-159">قبل ترحيل فاتورة النص الحر، يمكنك عرض الإدخال الكامل للمحاسبة، التي تتضمن مدينين ودائنين، للتحقق من أنه جاري ترحيل الفاتورة للحسابات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="87acb-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="87acb-160">يسمى عرض هذا الإدخال المحاسبي الكامل دفتر يومية بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="87acb-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="87acb-161">إذا كان إدخال دفتر يومية بدفتر الأستاذ الفرعي غير صحيح عند معاينته قبل تسجيل فاتورة النص الحر في دفتر اليومية، لا يمكنك تغيير إدخال دفتر يومية بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="87acb-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="87acb-162">وبدلاً من ذلك، يجب عليك تغيير التوزيعات المحاسبية أو ملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="87acb-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="87acb-163">يتم استخدام التوزيعات المحاسبية لتعريف أحد جوانب الإدخال المحاسبي أو المدين أو الدائن.</span><span class="sxs-lookup"><span data-stu-id="87acb-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="87acb-164">يتم إنشاء إدخال حساب دفتر يومية بدفتر الأستاذ الفرعي المقابلة من ملفات تعريف الترحيل، مثل حساب العميل أو الضريبة.</span><span class="sxs-lookup"><span data-stu-id="87acb-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>


