---
title: التوزيعات المحاسبية وإدخالات دفتر اليومية بدفتر الأستاذ الفرعي لفواتير الموردين
description: تستخدم التوزيعات المحاسبية لتحديد كيفية حساب مبلغ، مثل كيفية حساب المصروفات أو الضرائب أو التكاليف في فاتورة الموّرد. وسيكون لكل مبلغ يجب أن يحسب عند تسجيل فاتورة الموّرد في دفتر اليومية توزيع محاسبي واحد أو أكثر.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440092"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="3225a-104">التوزيعات المحاسبية وإدخالات دفتر اليومية بدفتر الأستاذ الفرعي لفواتير الموردين</span><span class="sxs-lookup"><span data-stu-id="3225a-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3225a-105">تستخدم التوزيعات المحاسبية لتحديد كيفية حساب مبلغ، مثل كيفية حساب المصروفات أو الضرائب أو التكاليف في فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="3225a-106">وسيكون لكل مبلغ يجب أن يحسب عند تسجيل فاتورة الموّرد في دفتر اليومية توزيع محاسبي واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="3225a-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="3225a-107">التوزيعات المحاسبية</span><span class="sxs-lookup"><span data-stu-id="3225a-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="3225a-108">يمكنك استخدام الأزرار التالية في صفحة فاتورة المورد لعرض وربما تعديل التوزيعات المحاسبية لكل مبلغ على فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="3225a-109">**توزيع المبالغ** – عرض وتعديل التوزيعات المحاسبية لسطر واحد لأية سطور فرعية، مثل الضرائب أو التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3225a-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="3225a-110">يمكنك أيضًا عرض وتعديل التوزيعات المحاسبية لبند فرعي مباشرةً من صفحة حركات ضريبة المبيعات أو صفحة حركات الرسوم.</span><span class="sxs-lookup"><span data-stu-id="3225a-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="3225a-111">تعديل مبالغ رأس فاتورة الموّرد، مثل التكاليف أو المبالغ التقريبية للعملة.</span><span class="sxs-lookup"><span data-stu-id="3225a-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="3225a-112">تعديل مبالغ سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="3225a-113">**عرض التوزيعات** – عرض التوزيعات المحاسبية لكافة البنود في المستند.</span><span class="sxs-lookup"><span data-stu-id="3225a-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="3225a-114">لا يمكنك تعديل التوزيعات المحاسبية من طريقة العرض هذه.</span><span class="sxs-lookup"><span data-stu-id="3225a-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="3225a-115">اعرض مبالغ السطر والرأس.</span><span class="sxs-lookup"><span data-stu-id="3225a-115">View header and line amounts.</span></span>

<span data-ttu-id="3225a-116">إذا كانت فاتورة الموّرد تشير إلى أمر شراء، يمكنك تقسيم وتعديل التوزيعات المحاسبية للأسطر التي تحتوي على صنف غير مخزن.</span><span class="sxs-lookup"><span data-stu-id="3225a-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="3225a-117">إذا لم يكن سطر فاتورة الموّرد يشير إلى سطر أمر شراء، يمكنك أيضًا حذف توزيع محاسبي.</span><span class="sxs-lookup"><span data-stu-id="3225a-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="3225a-118">لا يمكنك تقسيم أو حذف بنود للضرائب والتكاليف وخصومات البنود.</span><span class="sxs-lookup"><span data-stu-id="3225a-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="3225a-119">يمكنك تعديل حساب دفتر الأستاذ، ولكن لا يمكنك تغيير المبالغ أو النسب المئوية.</span><span class="sxs-lookup"><span data-stu-id="3225a-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="3225a-120">إذا كان السطر الأصلي يحتوي على صنف غير مخزن بينما التوزيعات المحاسبية منقسمة، سيتم تقسيم السطر الفرعي تلقائيًا ليتناسب مع الأبعاد المالية للسطر الأصلي.</span><span class="sxs-lookup"><span data-stu-id="3225a-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="3225a-121">لا يمكن تقسيم التوزيعات المحاسبية للسطر الفرعي أو حذفها، ولكن وفقًا لإعداد السطر الفرعي، قد تتمكن من تعديل حساب دفتر الأستاذ للتوزيعات المحاسبية للسطر الفرعي.</span><span class="sxs-lookup"><span data-stu-id="3225a-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="3225a-122">توزيع المبالغ</span><span class="sxs-lookup"><span data-stu-id="3225a-122">Distributing amounts</span></span>
<span data-ttu-id="3225a-123">عندما تقوم بإدخال فاتورة الموّرد، سيتم توزيع كل مبلغ كما يلي.</span><span class="sxs-lookup"><span data-stu-id="3225a-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3225a-124">سطر نوع فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="3225a-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="3225a-125">ترتيب الأولويات التي تحدد من أين يتم عرض الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="3225a-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="3225a-126">ترتيب الأولوية التي تحدد أين يتم عرض الأبعاد المالية الافتراضية</span><span class="sxs-lookup"><span data-stu-id="3225a-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3225a-127">منتج مخزّن</span><span class="sxs-lookup"><span data-stu-id="3225a-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-128">التوزيعات المحاسبية لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-129">حقل الحساب الرئيسي عند تحديد نفقات الشراء للمنتج في صفحة الترحيل.</span><span class="sxs-lookup"><span data-stu-id="3225a-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-130">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-131">استخدم القيم الافتراضية للبعد المالي في فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3225a-132">فئة تدبير أو منتج غير مخزن</span><span class="sxs-lookup"><span data-stu-id="3225a-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-133">التوزيع المحاسبي لسطر أمر الشراء، في حالة إشارة سطر فاتورة الموّرد إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-134">حقل الحساب الرئيسي عند تحديد نفقات الشراء للمصاريف في صفحة الترحيل.</span><span class="sxs-lookup"><span data-stu-id="3225a-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-135">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-136">إذا كان الحساب الرئيسي حساب توزيع، استخدم القيمة الافتراضية من تعريف حساب التوزيع.</span><span class="sxs-lookup"><span data-stu-id="3225a-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3225a-137">استخدم القيم الافتراضية للبعد المالي في فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="3225a-138">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-139">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3225a-140">الأصل الثابت</span><span class="sxs-lookup"><span data-stu-id="3225a-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-141">التوزيع المحاسبي لسطر أمر الشراء، في حالة إشارة سطر فاتورة الموّرد إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-142">إذا تم تحديد الاستحواذ في حقل نوع الحركة في نموذج فاتورة المورد، حقل الحساب الرئيسي عند تحديد الاستحواذ في صفحة ملفات تعريف ترحيل الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3225a-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="3225a-143">إذا تم تحديد تسوية الاستحواذ في حقل نوع الحركة في نموذج فاتورة المورد، حقل الحساب الرئيسي عند تحديد تسوية الاستحواذ في صفحة ملفات تعريف ترحيل الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3225a-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-144">استخدم التوزيع المحاسبي لسطر أمر شراء، في حالة إشارة سطر الفاتورة إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-145">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-146">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3225a-147">مشروع محدد في سطر فاتورة الموّرد</span><span class="sxs-lookup"><span data-stu-id="3225a-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-148">التوزيع المحاسبي لسطر أمر شراء، في حالة إشارة سطر الفاتورة إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-149">إذا تم تحديد رصيد في حقل ترحيل التكاليف - الصنف في صفحة مجموعات المشاريع، حقل الحساب الرئيسي عند تحديد التكلفة في صفحة إعداد ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3225a-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="3225a-150">إذا تم تحديد الأرباح والخسائر في حقل ترحيل التكاليف - الصنف في صفحة مجموعات المشاريع، حقل الحساب الرئيسي عند تحديد التكلفة - الصنف في صفحة إعداد ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3225a-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-151">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3225a-152">خصم البند</span><span class="sxs-lookup"><span data-stu-id="3225a-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-153">التوزيع المحاسبي لسطر أمر شراء، في حالة إشارة سطر الفاتورة إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-154">حقل الحساب الرئيسي عند تحديد الخصم في صفحة الترحيل.</span><span class="sxs-lookup"><span data-stu-id="3225a-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="3225a-155">إذا لم يتم تحديد حساب رئيسي لخصم لملف تعريف الترحيل، فإن التوزيع المحاسبي للسعر المفصل يكون في سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-156">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-157">استخدم الأبعاد المالية من التوزيعات المحاسبية للسعر المفصل في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-158">استخدم قيم الأبعاد المالية لسطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-159">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3225a-160">تكاليف الشراء التي تم إدخالها في علامة التبويب السعر والخصم لبند أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="3225a-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-161">التوزيع المحاسبي لسطر أمر شراء، في حالة إشارة سطر الفاتورة إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-162">التوزيع المحاسبي للسعر المفصل في سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-163">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-164">استخدم الأبعاد المالية من التوزيعات المحاسبية للسعر المفصل في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3225a-165">تكلفة السطر</span><span class="sxs-lookup"><span data-stu-id="3225a-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-166">التوزيع المحاسبي لسطر أمر شراء، في حالة إشارة سطر الفاتورة إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-167">إذا تم تحديد حساب دفتر الأستاذ في حقل نوع المدين في نموذج كود المصاريف، حقل الحساب المدين في صفحة كود المصاريف.</span><span class="sxs-lookup"><span data-stu-id="3225a-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="3225a-168">إذا كان الصنف محددًا في حقل نوع المدين في نموذج كود المصاريف، التوزيعات المحاسبية للسعر المفصل في بند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-169">إذا تم تحديد العميل/المورد في حقل نوع المدين في نموذج كود المصاريف، حقل حساب الدائن في صفحة كود المصاريف.</span><span class="sxs-lookup"><span data-stu-id="3225a-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-170">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-171">استخدم الأبعاد المالية من التوزيعات المحاسبية للسعر المفصل في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-172">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-173">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3225a-174">الضريبة، بالشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="3225a-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="3225a-175">يتم تحديد خيار تطبيق قواعد ضرائب الولايات المتحدة في صفحة معلمات دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="3225a-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="3225a-176">التوزيع المحاسبي لسطر أمر شراء، في حالة إشارة سطر الفاتورة إلى سطر أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-177">التوزيعات المحاسبية للسعر المفصل أو التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3225a-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-178">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-179">استخدم الأبعاد المالية من التوزيعات المحاسبية للسعر المفصل في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-180">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3225a-181">الضريبة، بالشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="3225a-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="3225a-182">يتم إلغاء تحديد خيار تطبيق قواعد ضرائب الولايات المتحدة في صفحة معلمات دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="3225a-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="3225a-183">يتم إلغاء تحديد حقل استخدام الضريبة لمجموعة ضريبة المبيعات في صفحة مجموعات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3225a-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="3225a-184">إذا كان مبلغ الضريبة قابلاً للاسترداد، حقل ضريبة المبيعات المدينة في صفحة مجموعات ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3225a-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="3225a-185">إذا كان مبلغ الضريبة غير قابل للاسترداد، السعر المفصل أو التوزيع المحاسبي للتكلفة.</span><span class="sxs-lookup"><span data-stu-id="3225a-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-186">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-187">استخدم الأبعاد المالية من السعر المفصل أو التوزيعات الحسابية للتكلفة في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-188">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-189">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3225a-190">الضريبة، بالشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="3225a-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="3225a-191">يتم إلغاء تحديد خيار تطبيق قواعد ضرائب الولايات المتحدة في صفحة معلمات دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="3225a-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="3225a-192">يتم تحديد حقل استخدام الضريبة لمجموعة ضريبة المبيعات في صفحة مجموعات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3225a-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="3225a-193">إذا كان مبلغ الضريبة قابلاً للاسترداد، حقل ضريبة المبيعات المدينة في صفحة مجموعات ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3225a-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="3225a-194">إذا كان مبلغ الضريبة غير قابل للاسترداد، حقل استخدام مصاريف الضريبة في صفحة مجموعات ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3225a-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-195">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-196">استخدم الأبعاد المالية من السعر المفصل أو التوزيعات الحسابية للتكلفة في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-197">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-198">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3225a-199">تكلفة الرأس</span><span class="sxs-lookup"><span data-stu-id="3225a-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-200">إذا تم تحديد حساب دفتر الأستاذ في حقل نوع المدين في نموذج كود المصاريف، حقل الحساب المدين في صفحة كود المصاريف.</span><span class="sxs-lookup"><span data-stu-id="3225a-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="3225a-201">إذا تم تحديد العميل/المورد في حقل نوع المدين في نموذج كود المصاريف، حقل حساب الدائن في صفحة كود المصاريف.</span><span class="sxs-lookup"><span data-stu-id="3225a-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-202">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-203">إذا كان الحساب الرئيسي حساب توزيع، استخدم القيمة الافتراضية من تعريف حساب التوزيع.</span><span class="sxs-lookup"><span data-stu-id="3225a-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3225a-204">استخدم قيم القالب الافتراضي للبعد المالي من رأس فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="3225a-205">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-206">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3225a-207">خصم الرأس</span><span class="sxs-lookup"><span data-stu-id="3225a-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="3225a-208">حقل الحساب الرئيسي لنوع ترحيل خصم فاتورة المورد في صفحة حسابات الحركات التلقائية.</span><span class="sxs-lookup"><span data-stu-id="3225a-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3225a-209">في حالة إشارة سطر فاتورة إلى سطر أمر شراء، استخدم التوزيع المحاسبي لسطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3225a-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3225a-210">استخدم الأبعاد المالية من التوزيعات المحاسبية للسعر المفصل في سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-211">استخدم قيم الأبعاد المالية من سطر فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3225a-212">استخدم القيم الافتراضية للبعد المالي من الحساب الرئيسي في صفحة مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3225a-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="3225a-213">توزيع الضرائب</span><span class="sxs-lookup"><span data-stu-id="3225a-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="3225a-214">يتعذر إنشاء توزيعات محاسبية للضرائب إلا بعد أن يتم حساب الضرائب.</span><span class="sxs-lookup"><span data-stu-id="3225a-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="3225a-215">لحساب ضرائب المبيعات، يجب إكمال إحدى المهام التالية في صفحة فاتورة المورد:</span><span class="sxs-lookup"><span data-stu-id="3225a-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="3225a-216">عرض إجمالي الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="3225a-216">View the invoice total.</span></span>
-   <span data-ttu-id="3225a-217">عرض ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3225a-217">View the sales tax.</span></span>
-   <span data-ttu-id="3225a-218">عرض دفتر اليومية بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="3225a-218">View the subledger journal.</span></span>
-   <span data-ttu-id="3225a-219">عرض التوزيعات المحاسبية لفاتورة المورّد الكاملة.</span><span class="sxs-lookup"><span data-stu-id="3225a-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="3225a-220">وضع فاتورة المورّد قيد الانتظار.</span><span class="sxs-lookup"><span data-stu-id="3225a-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="3225a-221">ترحيل فاتورة الموّرد.</span><span class="sxs-lookup"><span data-stu-id="3225a-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="3225a-222">دفاتر يومية دفتر الأستاذ الفرعي لفواتير الموّرد</span><span class="sxs-lookup"><span data-stu-id="3225a-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="3225a-223">قبل ترحيل فاتورة الموّرد، يمكنك عرض الإدخال الكامل للمحاسبة، التي تتضمن مدينين ودائنين، للتحقق من أنه جاري ترحيل الفاتورة للحسابات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="3225a-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="3225a-224">يسمى عرض هذا الإدخال المحاسبي الكامل دفتر يومية بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="3225a-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="3225a-225">إذا كان إدخال دفتر يومية بدفتر الأستاذ الفرعي غير صحيح عند معاينته قبل تسجيل فاتورة الموّرد في دفتر اليومية، لا يمكنك تعديل إدخال دفتر يومية بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="3225a-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="3225a-226">بدلاً من ذلك، يجب عليك تعديل التوزيعات المحاسبية أو ملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="3225a-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="3225a-227">يتم استخدام التوزيعات المحاسبية لتعريف أحد جوانب الإدخال المحاسبي أو المدين أو الدائن.</span><span class="sxs-lookup"><span data-stu-id="3225a-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="3225a-228">يتم إنشاء إدخال حساب دفتر يومية بدفتر الأستاذ الفرعي المقابلة عن طريق استخدام ملفات تعريف الترحيل، مثل من حساب الموّرد أو الضرائب.</span><span class="sxs-lookup"><span data-stu-id="3225a-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





