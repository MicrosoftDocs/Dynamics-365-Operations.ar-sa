---
title: "تعريفات الترحيل"
description: "توفر هذه المقالة أمثلة تعرض كيفية استخدام تعريفات الترحيل لمخصصات الموازنة والتزامات أوامر الشراء."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1bbd9230219f11407bc7afbd59670c6287b77c02
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definition-examples"></a><span data-ttu-id="d6549-103">أمثلة تعريفات الترحيل</span><span class="sxs-lookup"><span data-stu-id="d6549-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d6549-104">توفر هذه المقالة أمثلة تعرض كيفية استخدام تعريفات الترحيل لمخصصات الموازنة والتزامات أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d6549-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="d6549-105">قبل قراءة هذا الموضوع, يجب أن تكون على دراية بتعريفات الترحيل وتعريفات ترحيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="d6549-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="d6549-106">وللحصول على معلومات، راجع [تعريفات الترحيل](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="d6549-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="d6549-107">ويمكن إعداد الأمثلة التالية في صفحة **تعريفات الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="d6549-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="d6549-108">يحتوي كل مثال على هذه الأقسام:</span><span class="sxs-lookup"><span data-stu-id="d6549-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="d6549-109">تعريف الترحيل – معايير المطابقة</span><span class="sxs-lookup"><span data-stu-id="d6549-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="d6549-110">تعريف الترحيل – الإدخالات المنشأة</span><span class="sxs-lookup"><span data-stu-id="d6549-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="d6549-111">الحركات المشتملة على الحسابات وقيم الأبعاد والمبالغ</span><span class="sxs-lookup"><span data-stu-id="d6549-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="d6549-112">إدخالات دفتر الأستاذ التي تم إنشاؤها من تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="d6549-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="d6549-113">عندما يحدث تطابق بين الحسابات وقيم الأبعاد في جزء **مطابقة المعايير** لتعريف الترحيل والحسابات وقيم الأبعاد في الحركة، يتم إنشاء إدخالات دفتر الأستاذ على أساس جزء **الإدخالات المنشأة** لتعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="d6549-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="d6549-114">لإقران تعريف ترحيل بنوع حركة معين، استخدم صفحة **تعريفات ترحيل الحركة**.</span><span class="sxs-lookup"><span data-stu-id="d6549-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="d6549-115">وبعد ربط تعريف ترحيل بنوع حركة وتحديد **‬‏‫استخدام تعريفات الترحيل** في صفحة **‬‏‫معلمات دفتر الأستاذ العام‬‏‫**، يجب على كافة الحركات من نوع الحركة المحددة استخدام تعريفات الترحيل.‬</span><span class="sxs-lookup"><span data-stu-id="d6549-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="d6549-116">مثال: التزامات أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="d6549-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="d6549-117">عندما تقوم بتمكين معالجة الالتزامات بتحديد **تمكين عملية الالتزام** في صفحة **معلمات دفتر الأستاذ العام**، يجب استخدام تعريفات الترحيل لتسجيل الالتزامات في دفتر الأستاذ العام لأي حسابات ينبغي حجزها.</span><span class="sxs-lookup"><span data-stu-id="d6549-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="d6549-118">وفي معظم الحالات، يتم حجز كافة حسابات المصروفات في الميزانية العمومية.</span><span class="sxs-lookup"><span data-stu-id="d6549-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="d6549-119">ويتم إعداد تعريفات الترحيل للالتزامات التي تم إعدادها لوحدة **الشراء** في صفحة **تعريفات الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="d6549-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="d6549-120">وبعد ذلك، في منطقة **المشتريات** في صفحة **تعريفات ترحيل الحركة**، يمكنك تحديد نوع حركة **أمر الشراء** لإقران تعريف الترحيل بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d6549-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="d6549-121">ويجب موازنة كافة حركات الإيصال لالتزامات أوامر الشراء الشراء (أي، الديون يجب أن تساوي الائتمانات) في كل بعد من الأبعاد الفريدة في الإيصال.</span><span class="sxs-lookup"><span data-stu-id="d6549-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="d6549-122">تعريف الترحيل – معايير المطابقة</span><span class="sxs-lookup"><span data-stu-id="d6549-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="d6549-123">بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-123">Account structure</span></span>       | <span data-ttu-id="d6549-124">تطابق رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-124">Match account number</span></span> | <span data-ttu-id="d6549-125">الأولوية</span><span class="sxs-lookup"><span data-stu-id="d6549-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="d6549-126">بنية الحساب - الأرباح والخسائر</span><span class="sxs-lookup"><span data-stu-id="d6549-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="d6549-127">1</span><span class="sxs-lookup"><span data-stu-id="d6549-127">1</span></span>        |

<span data-ttu-id="d6549-128">* تعني قيمة فارغة في حقل **مطالقة رقم الحساب** أن كافة الحسابات المطابقة في بنية الحساب المحدد عبارة عن جزء من قاعدة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="d6549-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="d6549-129">تعريف الترحيل – الإدخالات المنشأة</span><span class="sxs-lookup"><span data-stu-id="d6549-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="d6549-130">بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-130">Account structure</span></span> | <span data-ttu-id="d6549-131">رقم الحساب الذي تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="d6549-131">Generated account number</span></span>                    | <span data-ttu-id="d6549-132">مدين/دائن تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="d6549-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="d6549-133">الرصيد</span><span class="sxs-lookup"><span data-stu-id="d6549-133">Balance</span></span>           | <span data-ttu-id="d6549-134">300143 - -(حساب الالتزامات)</span><span class="sxs-lookup"><span data-stu-id="d6549-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="d6549-135">متشابه</span><span class="sxs-lookup"><span data-stu-id="d6549-135">Same</span></span>                   |
| <span data-ttu-id="d6549-136">الرصيد</span><span class="sxs-lookup"><span data-stu-id="d6549-136">Balance</span></span>           | <span data-ttu-id="d6549-137">300144 - -(حجز لحساب الالتزامات)</span><span class="sxs-lookup"><span data-stu-id="d6549-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="d6549-138">موازنة</span><span class="sxs-lookup"><span data-stu-id="d6549-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="d6549-139">الحركات المشتملة على الحسابات وقيم الأبعاد والمبالغ</span><span class="sxs-lookup"><span data-stu-id="d6549-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="d6549-140">تأتي الحسابات وقيم الأبعاد إما من التوزيعات المحاسبية التي تقوم بإدخالها لبند أمر شراء، أو من الحسابات والأبعاد التي يتم إنشاؤها تلقائياً استناداً إلى الإعدادات الافتراضية للموردين، والأصناف، والفئات، وقوالب الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="d6549-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="d6549-141">الحساب + الأبعاد</span><span class="sxs-lookup"><span data-stu-id="d6549-141">Account + dimensions</span></span>           | <span data-ttu-id="d6549-142">مدين</span><span class="sxs-lookup"><span data-stu-id="d6549-142">Debit</span></span>  | <span data-ttu-id="d6549-143">يضع في الحساب مبلغاً دائناً</span><span class="sxs-lookup"><span data-stu-id="d6549-143">Credit</span></span> | <span data-ttu-id="d6549-144">تعليق</span><span class="sxs-lookup"><span data-stu-id="d6549-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="d6549-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="d6549-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="d6549-146">250.00</span><span class="sxs-lookup"><span data-stu-id="d6549-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="d6549-147">إدخالات دفتر الأستاذ التي تم إنشاؤها من تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="d6549-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="d6549-148">يتم إنشاء إدخالات دفتر الأستاذ التي تم إنشاؤها لتسجيل الالتزامات.</span><span class="sxs-lookup"><span data-stu-id="d6549-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="d6549-149">الحساب + الأبعاد</span><span class="sxs-lookup"><span data-stu-id="d6549-149">Account + dimensions</span></span>           | <span data-ttu-id="d6549-150">مدين</span><span class="sxs-lookup"><span data-stu-id="d6549-150">Debit</span></span>  | <span data-ttu-id="d6549-151">يضع في الحساب مبلغاً دائناً</span><span class="sxs-lookup"><span data-stu-id="d6549-151">Credit</span></span> | <span data-ttu-id="d6549-152">تعليق</span><span class="sxs-lookup"><span data-stu-id="d6549-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="d6549-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="d6549-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="d6549-154">250.00</span><span class="sxs-lookup"><span data-stu-id="d6549-154">250.00</span></span> |        |         |
| <span data-ttu-id="d6549-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="d6549-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="d6549-156">250.00</span><span class="sxs-lookup"><span data-stu-id="d6549-156">250.00</span></span> |         |

<span data-ttu-id="d6549-157">في هذا المثال، يتطابق أي حساب هو جزء من "بنية الحساب" - الأرباح والخسائر مع معايير تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="d6549-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="d6549-158">ولذلك، عندما يتم تقييم 606500-OU\_1-OU\_3566-Training، يتم إنشاء الإدخالات التي تم إنشاؤها للحسابات التي تم تحديدها في جزء **الإدخالات التي تم إنشاؤها** لتعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="d6549-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="d6549-159">مثال: مخصصات الموازنة</span><span class="sxs-lookup"><span data-stu-id="d6549-159">Example: Budget appropriations</span></span>
<span data-ttu-id="d6549-160">عندما تقوم بتمكين مخصصات الموازنة من خلال تحديد **تمكين مخصصات الموازنة** في صفحة **معلمات دفتر الأستاذ العام**، يجب استخدام تعريفات الترحيل لتسجيل إدخالات سجل الموازنة لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="d6549-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="d6549-161">وعندما يكون تكوين رقابة الموازنة نشطاً وقيد التشغيل، يمكن استخدام تعريفات الترحيل وتعريفات ترحيل الحركة لدعم تسجيل إدخالات المخصصات، والمراجعات، والتحويلات، والمشاريع، والأصول الثابتة، والتنبؤات بالتوريد والطلب لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="d6549-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="d6549-162">ولإعداد تعريف ترحيل لإدخالات سجل الموازنة ويحتوي على نوع الموازنة **الموازنة الأصلية**، وتم تمكين المخصصات له، حدد وحدة **الموازنة** في صفحة **تعريفات الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="d6549-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="d6549-163">وبعد ذلك، في منطقة **الموازنة** في صفحة **تعريفات ترحيل الحركة**، يمكنك استخدام أكواد الموازنة لإقران تعريف الترحيل بإدخالات سجل الموازنة التي تحتوي على نوع الموازنة **الموازنة الأصلية**.</span><span class="sxs-lookup"><span data-stu-id="d6549-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="d6549-164">وعند تمكين ملفات تعريف الترحيل ومخصصات الموازنة، يتم تسجيل إدخالات سجل الموازنة لرقابة الموازنة وفي دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="d6549-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="d6549-165">تعريف الترحيل – معايير المطابقة</span><span class="sxs-lookup"><span data-stu-id="d6549-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="d6549-166">بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-166">Account structure</span></span>       | <span data-ttu-id="d6549-167">تطابق رقم الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-167">Match account number</span></span> | <span data-ttu-id="d6549-168">الأولوية</span><span class="sxs-lookup"><span data-stu-id="d6549-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="d6549-169">بنية الحساب - الأرباح والخسائر</span><span class="sxs-lookup"><span data-stu-id="d6549-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="d6549-170">1</span><span class="sxs-lookup"><span data-stu-id="d6549-170">1</span></span>        |

<span data-ttu-id="d6549-171">* تعني قيمة فارغة في حقل **مطالقة رقم الحساب** أن كافة الحسابات المطابقة في بنية الحساب المحدد عبارة عن جزء من قاعدة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="d6549-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="d6549-172">تعريف الترحيل – الإدخالات المنشأة</span><span class="sxs-lookup"><span data-stu-id="d6549-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="d6549-173">بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-173">Account structure</span></span> | <span data-ttu-id="d6549-174">رقم الحساب الذي تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="d6549-174">Generated account number</span></span>              | <span data-ttu-id="d6549-175">مدين/دائن تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="d6549-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="d6549-176">بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-176">Account structure</span></span> | <span data-ttu-id="d6549-177">300145 - -(حساب الإيرادات المقدرة)</span><span class="sxs-lookup"><span data-stu-id="d6549-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="d6549-178">متشابه</span><span class="sxs-lookup"><span data-stu-id="d6549-178">Same</span></span>                   |
| <span data-ttu-id="d6549-179">بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="d6549-179">Account structure</span></span> | <span data-ttu-id="d6549-180">300146--(حساب المخصصات)</span><span class="sxs-lookup"><span data-stu-id="d6549-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="d6549-181">موازنة</span><span class="sxs-lookup"><span data-stu-id="d6549-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="d6549-182">الحركات المشتملة على الحسابات وقيم الأبعاد والمبالغ</span><span class="sxs-lookup"><span data-stu-id="d6549-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="d6549-183">تقوم بإدخال الحسابات وقيم الأبعاد والمبالغ الخاصة بإدخال حساب الموازنة في صفحة **إدخال سجل الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="d6549-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="d6549-184">الحساب + الأبعاد</span><span class="sxs-lookup"><span data-stu-id="d6549-184">Account + dimensions</span></span>           | <span data-ttu-id="d6549-185">مدين</span><span class="sxs-lookup"><span data-stu-id="d6549-185">Debit</span></span> | <span data-ttu-id="d6549-186">يضع في الحساب مبلغاً دائناً</span><span class="sxs-lookup"><span data-stu-id="d6549-186">Credit</span></span> | <span data-ttu-id="d6549-187">تعليق</span><span class="sxs-lookup"><span data-stu-id="d6549-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="d6549-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="d6549-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="d6549-189">250.00</span><span class="sxs-lookup"><span data-stu-id="d6549-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="d6549-190">إدخالات دفتر الأستاذ التي تم إنشاؤها من تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="d6549-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="d6549-191">يتم إنشاء إدخالات دفتر الأستاذ التي تم إنشاؤها لتسجيل الموازنة الأصلية في كل بعد من الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="d6549-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="d6549-192">الحساب + الأبعاد</span><span class="sxs-lookup"><span data-stu-id="d6549-192">Account + dimensions</span></span>           | <span data-ttu-id="d6549-193">مدين</span><span class="sxs-lookup"><span data-stu-id="d6549-193">Debit</span></span>  | <span data-ttu-id="d6549-194">يضع في الحساب مبلغاً دائناً</span><span class="sxs-lookup"><span data-stu-id="d6549-194">Credit</span></span> | <span data-ttu-id="d6549-195">تعليق</span><span class="sxs-lookup"><span data-stu-id="d6549-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="d6549-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="d6549-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="d6549-197">250.00</span><span class="sxs-lookup"><span data-stu-id="d6549-197">250.00</span></span> |         |
| <span data-ttu-id="d6549-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="d6549-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="d6549-199">250.00</span><span class="sxs-lookup"><span data-stu-id="d6549-199">250.00</span></span> |        |         |

<span data-ttu-id="d6549-200">في هذا المثال، يتطابق أي حساب هو جزء من "بنية الحساب" - الأرباح والخسائر مع معايير تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="d6549-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="d6549-201">ولذلك، عندما يتم تقييم 606400-OU\_1-OU\_3566-Training، يتم إنشاء إدخالات دفتر الأستاذ التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="d6549-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






