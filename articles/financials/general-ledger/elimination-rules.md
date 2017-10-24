---
title: "قواعد الاستبعاد"
description: "يقدم هذا الموضوع معلومات حول قواعد الاستبعاد، والخيارات المختلفة للتبليغ عن عمليات الاستبعاد."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f8fe754a27a825ace862d5eac992c42ef973f10
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="elimination-rules"></a><span data-ttu-id="d9885-103">قواعد الاستبعاد</span><span class="sxs-lookup"><span data-stu-id="d9885-103">Elimination rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d9885-104">يقدم هذا الموضوع معلومات حول قواعد الاستبعاد، والخيارات المختلفة للتبليغ عن عمليات الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="d9885-105">تكون حركات الاستبعاد مطلوبة عندما يقوم الكيان القانوني الرئيسي بالتعامل مع واحد أو أكثر من الكيانات القانونية الفرعية ويستخدم تقارير مالية مجمعة.</span><span class="sxs-lookup"><span data-stu-id="d9885-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="d9885-106">يجب أن تتضمن البيانات المالية المجمعة الحركات التي تحدث بين المؤسسة المجمعة والكيانات الأخرى خارج تلك المؤسسات.</span><span class="sxs-lookup"><span data-stu-id="d9885-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="d9885-107">ولذلك، يجب إزالة الحركات بين الكيانات القانونية في نفس المؤسسة، أو استبعادها، من دفتر الأستاذ العام بحيث لا تظهر في التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="d9885-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="d9885-108">وهناك عدة طرق للإبلاغ عن عمليات الاستبعاد:</span><span class="sxs-lookup"><span data-stu-id="d9885-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="d9885-109">يمكنك إنشاء قاعدة استبعاد ومعالجتها في شركة التجميع أو الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="d9885-110">ويمكن استخدام التقارير المالية لعرض حسابات عمليات الاستبعاد وأبعاد في صف أو عمود محدد.</span><span class="sxs-lookup"><span data-stu-id="d9885-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="d9885-111">يمكن استخدام كيان قانوني منفصل لترحيل إدخالات الحركات اليدوية لتعقب عمليات الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="d9885-112">يركز هذا الموضوع على قواعد الاستبعاد التي تمت معالجتها في شركة التجميع أو الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="d9885-113">يمكنك إعداد قواعد الاستبعاد لإنشاء حركات استبعاد في كيان قانوني محدد على انه كيان قانوني الوجهة لعمليات الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="d9885-114">كما يُعرف الكيان القانوني الوجهة بالكيان القانوني لعملية الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="d9885-115">يمكن إنشاء دفاتر يومية الاستبعاد إما أثناء عملية التجميع أو عن طريق استخدام مُقترح دفتر يومية الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="d9885-116">قبل إعداد قواعد الاستبعاد، يجب التعرف أولاً على المصطلحات التالية:</span><span class="sxs-lookup"><span data-stu-id="d9885-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="d9885-117">**الكيان القانوني المصدر** – الكيان القانوني الذي يتم ترحيل المبالغ التي تمت إزالتها إليه.</span><span class="sxs-lookup"><span data-stu-id="d9885-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="d9885-118">**الكيان القانوني الوجهة** – الكيان القانوني الذي يتم ترحيل قواعد الاستبعاد إليه.</span><span class="sxs-lookup"><span data-stu-id="d9885-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="d9885-119">**الكيان القانوني لعملية الاستبعاد** – الكيان القانوني الذي يتم تحديده على أنه كيان قانوني وجهة لعمليات الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="d9885-120">**الكيان القانوني المجمع** – الكيان القانوني الذي تم إنشاؤه لتقديم تقارير حول النتائج المالية لمجموعة من الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="d9885-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="d9885-121">يتم تجميع البيانات المالية الواردة من الكيانات القانونية داخل هذا الكيان القانوني، ثم يتم إنشاء تقرير مالي باستخدام البيانات التي تم جمعها.</span><span class="sxs-lookup"><span data-stu-id="d9885-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="d9885-122">يعرض الجدول التالي أنواع الحركات التي قد لا يمكن استبعادها.</span><span class="sxs-lookup"><span data-stu-id="d9885-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9885-123">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="d9885-123">Transaction type</span></span></th>
<th><span data-ttu-id="d9885-124">مثال</span><span class="sxs-lookup"><span data-stu-id="d9885-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9885-125">إدخال أمر التوريد وإصدار الفواتير (معالجة مركزية)</span><span class="sxs-lookup"><span data-stu-id="d9885-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="d9885-126">بيع منتج إلى عميل نيابةً عن كيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9885-127">إدخال أمر التوريد (على مستوى الشركات الشقيقة/الشركة الواحدة) وإصدار الفواتير</span><span class="sxs-lookup"><span data-stu-id="d9885-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="d9885-128">بيع المنتجات بين الكيانات القانونية في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9885-129">أوامر الشراء (معالجة مركزية)</span><span class="sxs-lookup"><span data-stu-id="d9885-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="d9885-130">شراء مخزون وإمدادات وخدمات وأصول ثابتة ومنتجات أخرى من أحد الموردين نيابةً عن كيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9885-131">إدارة المخزون (على مستوى الشركات الشقيقة/الشركة الواحدة)</span><span class="sxs-lookup"><span data-stu-id="d9885-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="d9885-132">تحويل مخزون كيان قانوني إلى الأصول الثابتة لكيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="d9885-133">تحويل مخزون كيان قانوني إلى مخزون كيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9885-134">تتبع مخزون بالطريق</span><span class="sxs-lookup"><span data-stu-id="d9885-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="d9885-135">نقل الأصناف بين المستودعات في نفس الكيان القانوني، ولكن في مواقع جغرافية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="d9885-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9885-136">معالجة فواتير مركزية للحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="d9885-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="d9885-137">تسجيل فاتورة نيابةً عن كيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9885-138">معالجة دفع مركزية للحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="d9885-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="d9885-139">دفع فاتورة نيابةً عن كيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9885-140">الإدارة النقدية والخزانة (المعالجة المركزية)</span><span class="sxs-lookup"><span data-stu-id="d9885-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="d9885-141">معالجة مدفوعات الضرائب، والضرائب المستردة ورسوم الفائدة والقروض والسُلف وحصص الأرباح المدفوعة والعوائد/العمولات المدفوعة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="d9885-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="d9885-142">دفع المصروفات نيابةً عن كيان قانوني آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="d9885-143">يتم إدخال الفاتورة في الدفاتر الخاصة بالكيان القانوني الوجهة، و ينبغي عليك إجراء تسوية بين الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="d9885-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="d9885-144">على سبيل المثال، يقوم كيان قانوني بدفع تقرير المصروفات الخاص بموظف في كيان قانوني آخر.</span><span class="sxs-lookup"><span data-stu-id="d9885-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="d9885-145">في هذه الحالة، يحتوي تقرير مصروفات الموظف على مصروفات مرتبطة بكيان قانوني آخر.</span><span class="sxs-lookup"><span data-stu-id="d9885-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="d9885-146">تحويل النقدية من كيان قانوني إلى آخر في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d9885-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9885-147">الحسابات المدينة (معالجة مركزية)</span><span class="sxs-lookup"><span data-stu-id="d9885-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="d9885-148">استلام مبلغ نقدي لفاتورة عميل في كيان قانوني آخر، وإيداع الشيك في الحساب البنكي لهذا الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="d9885-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9885-149">كشف الرواتب (معالجة مركزية، على مستوى الشركات الشقيقة/الشركة الواحدة)</span><span class="sxs-lookup"><span data-stu-id="d9885-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="d9885-150">دفع الرواتب الخاصة بكيان قانوني آخر.</span><span class="sxs-lookup"><span data-stu-id="d9885-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="d9885-151">على سبيل المثال، يقوم كيان قانوني بدفع كشف الرواتب الخاص بموظفيه، لكنه يطلب رسوم قيام أحد الموظفين بالعمل لكيان قانوني آخر أثناء وجود هذا الدفع قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d9885-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="d9885-152">أو في حالة قيام أحد الموظفين بالعمل نصف الوقت لكيان قانوني أ ونصف الوقت لكيان قانوني ب، وتكون الميزات شاملة المدفوع بأكمله.</span><span class="sxs-lookup"><span data-stu-id="d9885-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="d9885-153">في هذه الحالات، يتضمن الدفع للموظف الدفع من كلا الكيانين القانونيين.</span><span class="sxs-lookup"><span data-stu-id="d9885-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="d9885-154">فلا يتم ترحيل المرتبات فحسب، بل يتم كذلك ترحيل الضرائب والميزات والخصومات واستحقاقات المرتبات.</span><span class="sxs-lookup"><span data-stu-id="d9885-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="d9885-155">تحويل العمالة من قسم أو فرع إلى قسم أو فرع آخر.</span><span class="sxs-lookup"><span data-stu-id="d9885-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9885-156">الأصول الثابتة (على مستوى الشركات الشقيقة/الشركة الواحدة)</span><span class="sxs-lookup"><span data-stu-id="d9885-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="d9885-157">تحويل الأصول الثابتة لمخزون أو إلى الأصول الثابتة لكيان قانوني آخر.</span><span class="sxs-lookup"><span data-stu-id="d9885-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9885-158">التوزيعات (على مستوى الشركات الشقيقة/الشركة الواحدة)</span><span class="sxs-lookup"><span data-stu-id="d9885-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="d9885-159">معالجة توزيعات الشركة.</span><span class="sxs-lookup"><span data-stu-id="d9885-159">You process corporate allocations.</span></span> <span data-ttu-id="d9885-160">تُعد التوزيعات أنشطة لأي حساب يتم توزيعه، بغض النظر عن الوحدة النمطية المنشأة.</span><span class="sxs-lookup"><span data-stu-id="d9885-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="d9885-161">مثال</span><span class="sxs-lookup"><span data-stu-id="d9885-161">Example</span></span>
<span data-ttu-id="d9885-162">يقوم الكيان القانوني الخاص بك (الكيان القانوني أ) ببيع أدوات لكيان قانوني آخر في الشركة (الكيان القانوني ب). يوضح المثال التالي كيفية استبعاد الحركات التي تحدث بين الكيانين القانونيين.</span><span class="sxs-lookup"><span data-stu-id="d9885-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="d9885-163">يبيع الكيان القانوني أ أدوات تقدَّر بـ 10.00 إلى الكيان القانوني ب بمبلغ 10.00.</span><span class="sxs-lookup"><span data-stu-id="d9885-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="d9885-164">يبيع الكيان القانوني أ أدوات تقدَّر بـ 10.00 إلى الكيان القانوني ب بمبلغ 10.00، بالإضافة إلى مبلغ 2.00 في تكاليف الشحن الفعلية.</span><span class="sxs-lookup"><span data-stu-id="d9885-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="d9885-165">يبيع الكيان القانوني أ أدوات تقدر بـ 10.00 إلى الكيان القانوني ب بمبلغ 15.00 ويعتمد هامشًا على عملية البيع.</span><span class="sxs-lookup"><span data-stu-id="d9885-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="d9885-166">يبيع الكيان القانوني أ أدوات تقدَّر بـ 10.00 إلى الكيان القانوني ب بمبلغ 15.00 ويعتمد نصف الهامش على عملية البيع.</span><span class="sxs-lookup"><span data-stu-id="d9885-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="d9885-167">يعتمد الكيان القانوني ب النصف الآخر من الهامش على عملية البيع.</span><span class="sxs-lookup"><span data-stu-id="d9885-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="d9885-168">ولذلك، يتم تقسيم الإيراد.</span><span class="sxs-lookup"><span data-stu-id="d9885-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="d9885-169">ويوفر تقسيم الإيراد حافزًا للطلب من كيان قانوني آخر في المؤسسة بدلاً من مؤسسة خارجية.</span><span class="sxs-lookup"><span data-stu-id="d9885-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="d9885-170">تقوم كل هذه الحركات بإنشاء حركات بين الشركات الشقيقة والتي يتم ترحيلها إلى حسابات "مستحقة حتى" والحسابات "مستحقة من".</span><span class="sxs-lookup"><span data-stu-id="d9885-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="d9885-171">علاوة على ذلك، ربما تشتمل هذه الحركات على مبلغ فرق السعر سواء بالارتفاع أو الانخفاض عندما لا يتساوى مبلغ مبيعات الشركات الشقيقة مع تكلفة البضائع المبيعة.</span><span class="sxs-lookup"><span data-stu-id="d9885-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="d9885-172">إعداد قواعد الاستبعاد</span><span class="sxs-lookup"><span data-stu-id="d9885-172">Set up elimination rules</span></span>
<span data-ttu-id="d9885-173">عند إعداد قواعد الاستبعاد في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition نوصي بإنشاء بعد مالي بشكل خاص لأغراض الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="d9885-174">يطلق عليه معظم العملاء "الشريك التجاري" أو شيء من هذا القبيل.</span><span class="sxs-lookup"><span data-stu-id="d9885-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="d9885-175">إذا قررت عدم استخدام بعد مالي، فمن ثم عليك التأكد أن لديك الحسابات الرئيسية الخاصة بالحركات فيما بين الشركات الشقيقة فقط.</span><span class="sxs-lookup"><span data-stu-id="d9885-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="d9885-176">يمكنك العثور على إعداد عمليات الاستبعاد في إعداد منطقة الوحدة النمطية لعمليات الدمج.</span><span class="sxs-lookup"><span data-stu-id="d9885-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="d9885-177">بعد قيامك بإدخال وصف للقاعدة، يجب عليك اختيار الشركة التي سيتم ترحيل دفتر يومية الاستبعاد إليها.</span><span class="sxs-lookup"><span data-stu-id="d9885-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="d9885-178">ويجب أن تحتوي هذه الشركة على **‏‫يُستخدم لعملية الاستبعاد المالي‬** محددة في إعداد الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="d9885-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="d9885-179">يمكنك تعيين تاريخ سريان قاعدة الاستبعاد، وموعد انتهائها، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="d9885-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="d9885-180">يجب عليك تعيين **نشط** إلى **نعم** إذا كنت تريد أن يكون متوفراً في عملية مقترح الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="d9885-181">حدد اسم دفتر يومية الذي يحتوي على نوع من **الاستبعاد**.</span><span class="sxs-lookup"><span data-stu-id="d9885-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="d9885-182">بعد تعريف الأساسيات، يمكنك تعريف قواعد المعالجة الفعلية بالنقر فوق **سطور**.</span><span class="sxs-lookup"><span data-stu-id="d9885-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="d9885-183">هناك خياران للاستبعاد، استبعاد مبلغ صافي التغيير أو تحديد مبلغ ثابت.</span><span class="sxs-lookup"><span data-stu-id="d9885-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="d9885-184">حدد حساب مصدرك.</span><span class="sxs-lookup"><span data-stu-id="d9885-184">Select your source account.</span></span> <span data-ttu-id="d9885-185">يمكنك استخدام علامة النجمة (\*) كحرف بدل.</span><span class="sxs-lookup"><span data-stu-id="d9885-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="d9885-186">على سبيل المثال، قد يحدد الرقم 1\* جميع الحسابات التي تبدأ بالرقم 1 كمصدر للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="d9885-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="d9885-187">بعد أن قمت بتحديد حسابات مصدرك، تُحدد **مواصفات الحساب** الحساب من شركة الوجهة الذي يتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="d9885-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="d9885-188">حدد **مصدر** إذا أردت استخدام نفس الحساب الرئيسي المحدد في حساب **المصدر**.</span><span class="sxs-lookup"><span data-stu-id="d9885-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="d9885-189">إذا قمت بتحديد **مُعرّف من قبل المستخدم**، فمن ثم يجب عليك تحديد حساب وجهة.</span><span class="sxs-lookup"><span data-stu-id="d9885-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="d9885-190">تعمل مواصفات الأبعاد بنفس الطريقة.</span><span class="sxs-lookup"><span data-stu-id="d9885-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="d9885-191">إذا قمت بتحديد **مصدر**، فإنه يستخدم نفس الأبعاد فيشركة الوجهة كشركة مصدر.</span><span class="sxs-lookup"><span data-stu-id="d9885-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="d9885-192">إذا قمت بتحديد **مُعرّف من قبل المستخدم**، فسوف تحتاج إلى تحديد الأبعاد في الشركة الوجهة بواسطة النقر على عنصر قائمة **الأبعاد الوجهة**.</span><span class="sxs-lookup"><span data-stu-id="d9885-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="d9885-193">حدد أبعاد مصدر والأبعاد المالية والقيم التي يتم استخدامها كمصدر للاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="d9885-194">معالجة حركات الاستبعاد</span><span class="sxs-lookup"><span data-stu-id="d9885-194">Process elimination transactions</span></span>
<span data-ttu-id="d9885-195">هناك طريقتان لمعالجة حركات الاستبعاد، أثناء عملية التوحيد عبر الإنترنت أو عن طريق إنشاء دفتر يومية استبعاد وتشغيل عملية مقترح الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="d9885-196">يركز هذا القسم على إنشاء دفتر يومية وتشغيل عملية الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="d9885-197">في شركة مُعرّفة كشركة استبعاد، حدد **دفتر يومية الاستبعاد** في الوحدة النمطية لعمليات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="d9885-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="d9885-198">بعد تحديد اسم دفتر اليومية، انقر فوق **سطور**.</span><span class="sxs-lookup"><span data-stu-id="d9885-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="d9885-199">يمكنك تشغيل المقترح عن طريق تحديد قائمة **المقترحات**، وتحديد **مُقترح الاستبعاد**.</span><span class="sxs-lookup"><span data-stu-id="d9885-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="d9885-200">حدد الشركة التي تُعد مصدرًا للبيانات الموحدة، ثم اختر القاعدة التي ترغب في معالجتها.</span><span class="sxs-lookup"><span data-stu-id="d9885-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="d9885-201">أدخل تاريخ بدء لبدء البحث عن مبالغ الاستبعاد، وتحديد موعد لإنهاء تاريخ البحث عن مبالغ الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="d9885-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="d9885-202">يمثل حقل **تاريخ ترحيل دفتر الأستاذ العام** التاريخ المستخدم لترحيب دفتر اليومية إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="d9885-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="d9885-203">بعد النقر فوق **موافق**، يمكنك مراجعة المبالغ وترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="d9885-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




