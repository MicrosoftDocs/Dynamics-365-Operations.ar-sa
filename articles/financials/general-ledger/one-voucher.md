---
title: "إيصال واحد"
description: "إيصال واحد لدفاتر اليومية المالية (دفتر اليومية العام، ودفتر يومية الأصول الثابتة، ودفتر يومية دفع المورد، وهكذا) يتيح لك إدخال حركات دفتر أستاذ فرعي متعددة في سياق إيصال واحد."
author: kweekley
manager: AnnBe
ms.date: 03/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3831a6b5ec458495134b4b490d33a9acd76b6d2e
ms.openlocfilehash: 76ea8470786bd50896400a65564d698d96119d6f
ms.contentlocale: ar-sa
ms.lasthandoff: 03/20/2018

---

# <a name="one-voucher"></a><span data-ttu-id="65776-103">إيصال واحد</span><span class="sxs-lookup"><span data-stu-id="65776-103">One voucher</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
>  <span data-ttu-id="65776-104">ستتوفر هذه الوظيفة في الإصدار 8.0 من Dynamics 365 for Finance and Operations، الذي سيتوفر في إصدار الربيع '18.</span><span class="sxs-lookup"><span data-stu-id="65776-104">This functionality will be available in Dynamics 365 for Finance and Operations version 8.0, which will be available in the Spring '18 release.</span></span>   

<a name="what-is-one-voucher"></a><span data-ttu-id="65776-105">ما المقصود بـ "إيصال واحد"؟</span><span class="sxs-lookup"><span data-stu-id="65776-105">What is "One voucher"?</span></span>
======================

<span data-ttu-id="65776-106">الوظيفة الموجودة لدفاتر اليومية المالية (دفتر اليومية العام، ودفتر يومية الأصول الثابتة، ودفتر يومية دفع المورد، وهكذا) تتيح لك إدخال حركات دفتر أستاذ فرعي متعددة في سياق إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="65776-106">The existing functionality for financial journals (general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="65776-107">نشير إلى هذه الوظيفة باسم "إيصال واحد".</span><span class="sxs-lookup"><span data-stu-id="65776-107">We refer to this functionality as "One voucher."</span></span> <span data-ttu-id="65776-108">يمكنك إنشاء إيصال واحد باستخدام أحد الأساليب التالية:</span><span class="sxs-lookup"><span data-stu-id="65776-108">You can create One voucher by using one of the following methods:</span></span>

-   <span data-ttu-id="65776-109">قم بإعداد اسم دفتر اليومية (**دفتر الأستاذ العام**\>**إعداد دفتر اليومية**\>**أسماء دفاتر اليومية**) حتى يتم تعيين الحقل **إيصال جديد** إلى **رقم إيصال واحد فقط**.</span><span class="sxs-lookup"><span data-stu-id="65776-109">Set up the journal name (**General ledger** \> **Journal setup** \>**Journal names**) so that the **New voucher** field is set to **One voucher number only**.</span></span> <span data-ttu-id="65776-110">يتم الآن تضمين كل بند تضيفه إلى دفتر اليومية في نفس الإيصال.</span><span class="sxs-lookup"><span data-stu-id="65776-110">Every line that you add to the journal is now included on the same voucher.</span></span> <span data-ttu-id="65776-111">لأنه تتم إضافة كل بند إلى نفس الإيصال، يمكن إدخال الإيصال كإيصال متعدد البنود، كحساب مقابل/حساب في نفس البند أو كمجموعة.</span><span class="sxs-lookup"><span data-stu-id="65776-111">Because every line is added to the same voucher, the voucher can be entered as a multiline voucher, as an account/offset account on the same line, or as a combination.</span></span>

<span data-ttu-id="65776-112">[![بند مفرد](./media/same-line.png)](./media/same-line.png)</span><span class="sxs-lookup"><span data-stu-id="65776-112">[![Single line](./media/same-line.png)](./media/same-line.png)</span></span>

-   <span data-ttu-id="65776-113">أدخل إيصالاً متعدد البنود لا يوجد فيه أي حساب مقابل.</span><span class="sxs-lookup"><span data-stu-id="65776-113">Enter a multiline voucher where there is no offset account.</span></span>

<span data-ttu-id="65776-114">[![الإيصال متعدد البنود](./media/Multi-line.png)](./media/Multi-line.png)</span><span class="sxs-lookup"><span data-stu-id="65776-114">[![Multiline voucher](./media/Multi-line.png)](./media/Multi-line.png)</span></span>

-   <span data-ttu-id="65776-115">أدخل إيصالاً يحتوي فيه كلُّ من الحساب والحساب المقابل على نوع حساب دفتر أستاذ فرعي، مثل المورد/المورد أو العميل/العميل أو العميل/المورد أو البنك/البنك.</span><span class="sxs-lookup"><span data-stu-id="65776-115">Enter a voucher where both the account and the offset account contain a subledger account type, such as vendor/vendor, Customer/customer, vendor/customer, or bank/bank.</span></span>

<span data-ttu-id="65776-116">[![إيصال دفتر الأستاذ الفرعي‬](./media/subledger.png)](./media/subledger.png)</span><span class="sxs-lookup"><span data-stu-id="65776-116">[![Subledger voucher](./media/subledger.png)](./media/subledger.png)</span></span>

<a name="issues-with-one-voucher"></a><span data-ttu-id="65776-117">المشكلات في إيصال واحد</span><span class="sxs-lookup"><span data-stu-id="65776-117">Issues with One voucher</span></span>
=======================

<span data-ttu-id="65776-118">تؤدي وظيفة الإيصال الواحد إلى حدوث مشكلات أثناء التسوية، وحساب ضريبة، وتسوية دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام، وإعداد التقارير المالية، والمزيد.</span><span class="sxs-lookup"><span data-stu-id="65776-118">The One voucher functionality causes issues during settlement, tax calculation, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="65776-119">(على سبيل المثال، للحصول على مزيد من المعلومات حول المشكلات التي تحدث أثناء إجراء التسوية، راجع [إيصال واحد مع سجلات متعددة العملاء أو الموردين](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) للعمل والإبلاغ بشكل صحيح، تتطلب هذه العمليات والتقارير تفاصيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="65776-119">(For example, for more information about issues that can occur during settlement, see [Single voucher with multiple customer or vendor records](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) To work and report correctly, these processes and reports require transaction details.</span></span> <span data-ttu-id="65776-120">على الرغم من أن بعض السيناريوهات قد لا تزال تعمل بشكل صحيح، استنادًا إلى إعداد المؤسسة الخاصة بك، إلا أنه غالبًا ما تحدث مشكلات عند إدخال الحركات المتعددة في إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="65776-120">Although some scenarios might still work correctly, based on your organization's setup, there are often issues when multiple transactions are entered in one voucher.</span></span>

<span data-ttu-id="65776-121">على سبيل المثال، تقوم بترحيل الإيصال متعدد البنود التالي.</span><span class="sxs-lookup"><span data-stu-id="65776-121">For example, you post the following multiline voucher.</span></span>

<span data-ttu-id="65776-122">[![مثال](./media/example.png)](./media/example.png)</span><span class="sxs-lookup"><span data-stu-id="65776-122">[![Example](./media/example.png)](./media/example.png)</span></span>

<span data-ttu-id="65776-123">تقوم بعد ذلك إنشاء تقرير **المصروفات حسب المورد** في مساحة عمل **المعلومات المالية**.</span><span class="sxs-lookup"><span data-stu-id="65776-123">You then generate the **Expenses by vendor** report in the **Financial Insights** workspace.</span></span> <span data-ttu-id="65776-124">يجمع التقرير أرصدة حسابات المصروفات ضمن مجموعة الموردين ثم المورد.</span><span class="sxs-lookup"><span data-stu-id="65776-124">The report groups expense account balances under vendor group and then vendor.</span></span> <span data-ttu-id="65776-125">عند إنشاء التقرير، يتعذر على النظام تحديد مجموعات الموردين/الموردين الذين تحملوا النفقة التي قيمتها 250.00.</span><span class="sxs-lookup"><span data-stu-id="65776-125">When generating the report, the system can't determine which vendor groups/vendors incurred the expense of 250.00.</span></span> <span data-ttu-id="65776-126">نظراً لعدم وجود تفاصيل الحركة، فسيفترض النظام أن مبلغ 250.00 تحمله المورد الأول الموجود في الإيصال.</span><span class="sxs-lookup"><span data-stu-id="65776-126">Because transaction details are missing, the system assumes the whole 250.00 was incurred by the first vendor found in the voucher.</span></span> <span data-ttu-id="65776-127">وسيظهر المبلغ 250.00، الذي تم تضمينه في رصيد الحساب الرئيسي 600120، ضمن مجموعة المورد/المورد.</span><span class="sxs-lookup"><span data-stu-id="65776-127">The 250.00, which is included in the balance for main account 600120, is then shown under that vendor group/vendor.</span></span> <span data-ttu-id="65776-128">من المحتمل جدًا ألا يكون المورد الأول في الإيصال هو المورد الصحيح، ومن ثمَّ يكون التقرير غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="65776-128">It’s very likely that the first vendor in the voucher was not the correct vendor, so the report is incorrect.</span></span>

<span data-ttu-id="65776-129">[![المصروفات](./media/expenses.png)](./media/expenses.png)</span><span class="sxs-lookup"><span data-stu-id="65776-129">[![Expenses](./media/expenses.png)](./media/expenses.png)</span></span>

<a name="the-future-of-one-voucher"></a><span data-ttu-id="65776-130">مستقبل الإيصال الواحد</span><span class="sxs-lookup"><span data-stu-id="65776-130">The future of One voucher</span></span>
=========================

<span data-ttu-id="65776-131">نظراً للمشكلات التي تم ذكرها سابقًا، ستصبح وظيفة الإيصال الواحد قديمة.</span><span class="sxs-lookup"><span data-stu-id="65776-131">Because of the issues that were stated earlier, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="65776-132">ومع ذلك، نظراً لأن هناك فجوات وظيفية تعتمد على هذه الوظيفة، لن تصبح هذه الوظيفة بأكملها قديمة مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="65776-132">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at once.</span></span> <span data-ttu-id="65776-133">بدلاً من ذلك، سنقوم باستخدام الجدول التالي:</span><span class="sxs-lookup"><span data-stu-id="65776-133">Instead, we will use the following schedule:</span></span> 

-   <span data-ttu-id="65776-134">**إصدار ربيع 2018** -سيتم إيقاف الوظيفة بشكل افتراضي من خلال معلمة دفتر أستاذ عام.</span><span class="sxs-lookup"><span data-stu-id="65776-134">**Spring 2018 release** – The functionality will be turned off by default through a General ledger parameter.</span></span> <span data-ttu-id="65776-135">ومع ذلك، يمكنك تشغيل الوظيفة إذا كان لدى مؤسستك سيناريو يقع في فجوات سيناريو الأعمال المذكورة لاحقاً في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="65776-135">However, you can turn the functionality on if your organization has a scenario that falls in the business scenario gaps that are listed later in this topic.</span></span>

    -   <span data-ttu-id="65776-136">إذا كان لدى عميل سيناريو عمل لا يتطلب إيصالاً واحدًا، فلا تقم بتشغيل هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="65776-136">If a customer has a business scenario that doesn't require One voucher, don't turn the functionality on.</span></span> <span data-ttu-id="65776-137">لن نُصلح "الأخطاء" في المناطق التي تم تحديدها لاحقاً في هذا الموضوع في حالة استخدام هذه الوظيفة على الرغم من وجود حل آخر.</span><span class="sxs-lookup"><span data-stu-id="65776-137">We won't fix "bugs" in the areas that were identified later in this topic if this functionality is used even though another solution exists.</span></span>

    -   <span data-ttu-id="65776-138">توقف عن استخدام إيصال واحد لعمليات التكامل في Microsoft Dynamics 365 Finance and Operations، ما لم تكن الوظيفة مطلوبة لأحد الفجوات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="65776-138">Stop using One voucher for integrations into Microsoft Dynamics 365 Finance and Operations, unless the functionality is required for one of the functional gaps.</span></span>

-   <span data-ttu-id="65776-139">**إصدار خريف 2018 والإصدارات الأحدث** -سيتم سد الفجوات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="65776-139">**Fall 2018 and later releases** – The functional gaps will be filled.</span></span> <span data-ttu-id="65776-140">بعد أن يتم سد الفجوات الوظيفية، سيتم إيقاف تشغيل وظيفة الإيصال الواحد بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="65776-140">After the functional gaps are filled, the One voucher functionality will be permanently turned off.</span></span>

<a name="why-use-one-voucher"></a><span data-ttu-id="65776-141">لماذا نستخدم الإيصال الواحد؟</span><span class="sxs-lookup"><span data-stu-id="65776-141">Why use One voucher?</span></span>
====================

<span data-ttu-id="65776-142">استناداً إلى محادثات مع العملاء، قمنا بتحويل القائمة التالية من السيناريوهات التي يستخدم فيها العملاء وظيفة الإيصال الواحد أو توجد فيها أسباب استخدامهم لهذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="65776-142">Based on conversations with customers, we have compiled the following list of scenarios where customers use the One voucher functionality or reasons why they use it.</span></span> <span data-ttu-id="65776-143">يمكن تحقيق بعض هذه المتطلبات في العمل باستخدام إيصال واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="65776-143">Some of these business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="65776-144">ومع ذلك، في العديد من السيناريوها، يمكن للبدائل تحقيق نفس متطلبات العمل.</span><span class="sxs-lookup"><span data-stu-id="65776-144">However, for many scenarios, alternatives can meet the same business requirements.</span></span>

<a name="scenarios-that-require-one-voucher"></a><span data-ttu-id="65776-145">السيناريوهات التي تتطلب الإيصال الواحد</span><span class="sxs-lookup"><span data-stu-id="65776-145">Scenarios that require One voucher</span></span>
----------------------------------

<span data-ttu-id="65776-146">يمكن إنجاز السيناريوهات التالية باستخدام وظيفة الإيصال الواحد فقط.</span><span class="sxs-lookup"><span data-stu-id="65776-146">The following scenarios can be accomplished only by using the One voucher functionality.</span></span> <span data-ttu-id="65776-147">سيتم سد هذه الفجوات الوظيفية من خلال ميزات أخرى في إصدار خريف 2018 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="65776-147">These functional gaps will be filled through other features in the Fall 2018 and later releases.</span></span>

-   <span data-ttu-id="65776-148">**ترحيل مدفوعات المورد أو العميل في نموذج ملخص إلى حساب بنكي**</span><span class="sxs-lookup"><span data-stu-id="65776-148">**Post vendor or customer payments in summary form to a bank account**</span></span>

    -   <span data-ttu-id="65776-149">تُبلغ مؤسسة عن قائمة بالموردين والمبالغ للبنك الخاصة بها، ويستخدم البنك هذه القائمة للدفع إلى الموردين بالنيابة عن المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="65776-149">An organization communicates a list of vendors and amounts to its bank, and the bank uses this list to pay the vendors on the organization's behalf.</span></span> <span data-ttu-id="65776-150">يقوم البنك بترحيل مبلغ المدفوعات كعملية سحب واحدة في الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="65776-150">The bank posts the sum of the payments as a single withdrawal on the bank account.</span></span>

>   <span data-ttu-id="65776-151">يتم دعم تلخيص مدفوعات المورد من خلال الإيصال الواحد فقط.</span><span class="sxs-lookup"><span data-stu-id="65776-151">Summarization of vendor payments is supported only through One voucher.</span></span> <span data-ttu-id="65776-152">يتم إدخال كل مورد كبند منفصل للحفاظ على التفاصيل في دفتر الأستاذ الفرعي للحسابات الدائنة، ولكن تتم إزاحة المبلغ الملخص لجميع المدفوعات إلى بند واحد للحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="65776-152">Each vendor is entered as a separate line to maintain detail in the Accounts payable subledger, but the summarized amount for all the payments is offset to a single line for the bank account.</span></span> <span data-ttu-id="65776-153">لذلك، يتم عرض السحب كمبلغ ملخص واحد في دفتر الأستاذ الفرعي للبنك.</span><span class="sxs-lookup"><span data-stu-id="65776-153">Therefore, the withdrawal is shown as a single summarized amount in the bank subledger.</span></span>

-   <span data-ttu-id="65776-154">تودع مؤسسة مدفوعات العملاء، أو يودع البنك مدفوعات العملاء بالنيابة عن المؤسسة، ويتم عرض الإيداع كمبلغ إجمالي في الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="65776-154">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

>   <span data-ttu-id="65776-155">وعادةً ما يتم دعم تلخيص مدفوعات العملاء من خلال وظيفة الإيداع.</span><span class="sxs-lookup"><span data-stu-id="65776-155">Summarization of customer payments is typically supported through the deposit functionality.</span></span> <span data-ttu-id="65776-156">ومع ذلك، إذا كنت تستخدم "السجل المرحلي" في طريقة الدفع، يتم دعم هذا السيناريو فقط من خلال الإيصال الواحد.</span><span class="sxs-lookup"><span data-stu-id="65776-156">However, if you're using "bridging" on the method of payment, this scenario is supported only through One voucher.</span></span> <span data-ttu-id="65776-157">يتم إدخال مدفوعات العملاء بنفس الطريقة الموضحة لتلخيص دفع المورد.</span><span class="sxs-lookup"><span data-stu-id="65776-157">The customer payments are entered in the same manner that is described for vendor payment summarization.</span></span>

-   <span data-ttu-id="65776-158">**آلية تجميع الحركات من أحد أحداث الأعمال**</span><span class="sxs-lookup"><span data-stu-id="65776-158">**Mechanism to group transactions from a business event**</span></span>

    -   <span data-ttu-id="65776-159">لدى مؤسسة حدث أعمال واحد يقوم بتشغيل حركات متعددة.</span><span class="sxs-lookup"><span data-stu-id="65776-159">An organization has a single business event that triggers multiple transactions.</span></span> <span data-ttu-id="65776-160">ومع ذلك، يريد قسم المحاسبة عرض الإدخالات المحاسبية معًا للتوصل إلى إمكانية تدقيق أفضل.</span><span class="sxs-lookup"><span data-stu-id="65776-160">However, the Accounting department wants to view the accounting entries together for better auditability.</span></span>

>   <span data-ttu-id="65776-161">إذا كان يجب على مؤسسة عرض الإدخالات المحاسبية من أحد أحداث الأعمال معًا، فيجب عليها استخدام إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="65776-161">If an organization must view the accounting entries from a business event together, it must use One voucher.</span></span> 

-   <span data-ttu-id="65776-162">**الميزات الخاصة بالبلد**</span><span class="sxs-lookup"><span data-stu-id="65776-162">**Country-specific features**</span></span>

 -   <span data-ttu-id="65776-163">تتطلب حاليًا ميزة المستند الإداري الواحد (SAD) لبولندا أن يتم استخدام إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="65776-163">The Single Administrative Document (SAD) feature for Poland currently requires that a single voucher be used.</span></span> <span data-ttu-id="65776-164">حتى يتوفر خيار تجميع لهذه الميزة، يجب عليك الاستمرار في استخدام وظيفة الإيصال الواحد.</span><span class="sxs-lookup"><span data-stu-id="65776-164">Until a grouping option is available for this feature, you must continue to use the One voucher functionality.</span></span> <span data-ttu-id="65776-165">قد تكون هناك ميزات إضافية خاصة بالبلد تتطلب وظيفة الإيصال الواحد.</span><span class="sxs-lookup"><span data-stu-id="65776-165">There may be additional country-specific features that require the One voucher functionality.</span></span>

-   <span data-ttu-id="65776-166">**دفتر يومية دفع الدفعات المقدمة للعملاء المشتمل على ضرائب في "بنود" متعددة**</span><span class="sxs-lookup"><span data-stu-id="65776-166">**Customer prepayment payment journal that has taxes on multiple "lines"**</span></span>

 -   <span data-ttu-id="65776-167">يسدد عميل دفعه مقدمة لأمر، وتشتمل بنود الأمر على ضرائب مختلفة يجب أن يتم تسجيلها للدفعة المقدمة.</span><span class="sxs-lookup"><span data-stu-id="65776-167">A customer makes a prepayment for an order, and the lines of the order have different taxes that must be recorded for the prepayment.</span></span> <span data-ttu-id="65776-168">عملية دفع الدفعة المقدمة للعميل عبارة عن حركة واحدة تحاكي بنود الأمر، حتى يمكن تسجيل الضريبة المناسبة للمبلغ الموجود في كل بند.</span><span class="sxs-lookup"><span data-stu-id="65776-168">The prepayment customer payment is one transaction that simulates the lines of the order, so that the appropriate tax can be recorded for the amount on each line.</span></span>

<span data-ttu-id="65776-169">في هذا السيناريو، العملاء الموجودون في الإيصال الواحد هم نفس العميل، نظراً لأن الحركة تحاكي بنود أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="65776-169">In this scenario, the customers in the single voucher are the same customer, because the transaction simulates the lines of a customer order.</span></span> <span data-ttu-id="65776-170">يجب إدخال الدفعة المقدمة في إيصال واحد، لأنه يجب إجراء عملية حساب الضرائب على "بنود" الدفعة الواحدة التي يُجريها العميل.</span><span class="sxs-lookup"><span data-stu-id="65776-170">The prepayment must be entered in a single voucher, because the tax calculation must be made on the "lines" of the single payment that the customer made.</span></span>

-   <span data-ttu-id="65776-171">**صيانة الأصل الثابت: إهلاك التسوية‬، وتقسيم الأصل، وحساب الإهلاك عند التخلص**</span><span class="sxs-lookup"><span data-stu-id="65776-171">**Fixed asset maintenance: Catch-up depreciation, split asset, calculate depreciation on disposal**</span></span>

<span data-ttu-id="65776-172">كما تُنشئ حركات الأصول الثابتة التالية حركات متعددة داخل إيصال واحد:</span><span class="sxs-lookup"><span data-stu-id="65776-172">The following fixed asset transactions also create multiple transactions within a single voucher:</span></span>
-   <span data-ttu-id="65776-173">يتم إجراء عملية استحواذ إضافية على أحد أصول ويتم حساب إهلاك "التسوية".</span><span class="sxs-lookup"><span data-stu-id="65776-173">An additional acquisition is made on an asset and ‘catch-up’ depreciation is calculated.</span></span>
-   <span data-ttu-id="65776-174">يتم تقسيم أصل.</span><span class="sxs-lookup"><span data-stu-id="65776-174">An asset is split.</span></span>
-   <span data-ttu-id="65776-175">يتم تمكين معلمة لحساب الإهلاك عند التخلص ثم يتم التخلص من الأصل.</span><span class="sxs-lookup"><span data-stu-id="65776-175">A parameter to calculate depreciation on disposal is enabled and then the asset is disposed.</span></span>

<a name="scenarios-that-dont-require-one-voucher"></a><span data-ttu-id="65776-176">السيناريوهات التي لا تتطلب الإيصال الواحد</span><span class="sxs-lookup"><span data-stu-id="65776-176">Scenarios that don't require One voucher</span></span>
----------------------------------------

<span data-ttu-id="65776-177">يمكن إنجاز السيناريوهات التالية بطرق أخرى ويجب ألا يتم استخدام الإيصال الواحد.</span><span class="sxs-lookup"><span data-stu-id="65776-177">The following scenarios can be accomplished through other means and should not use One voucher.</span></span>

-   <span data-ttu-id="65776-178">**ترحيل مدفوعات العميل في نموذج ملخص إلى الحساب البنكي**</span><span class="sxs-lookup"><span data-stu-id="65776-178">**Post customer payments in summary form to the bank account**</span></span>

<span data-ttu-id="65776-179">تودع مؤسسة مدفوعات العملاء، أو يودع البنك مدفوعات العملاء بالنيابة عن المؤسسة، ويتم عرض الإيداع كمبلغ إجمالي في الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="65776-179">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="65776-180">يتم دعم تلخيص مدفوعات العملاء من خلال وظيفة الإيداع عندما لا يتم استخدام سجل مرحلي في طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="65776-180">Summarization of customer payments is supported through the deposit  functionality when bridging isn't used on the method of payment.</span></span>

-   <span data-ttu-id="65776-181">**التصفية**</span><span class="sxs-lookup"><span data-stu-id="65776-181">**Netting**</span></span>

<span data-ttu-id="65776-182">في التصفية، تتم تصفية الأرصدة الخاصة بالمورد والعميل مقابل بعضها البعض لأن المورد والعميل هو نفس الطرف.</span><span class="sxs-lookup"><span data-stu-id="65776-182">In netting, the balances for a vendor and customer are netted against each other because the vendor and customer are the same party.</span></span> <span data-ttu-id="65776-183">يقلل هذا الأسلوب من صرف الأموال بين مؤسسة وطرف العميل/المورد.</span><span class="sxs-lookup"><span data-stu-id="65776-183">This approach minimizes the exchange of money between an organization and the customer/vendor party.</span></span>

<span data-ttu-id="65776-184">يمكن إنجاز التصفية عن طريق إدخال الزيادة والنقص في إيصالات منفصلة، وترحيل المقابل إلى حساب دفتر استاذ للمقاصة.</span><span class="sxs-lookup"><span data-stu-id="65776-184">Netting can be accomplished by entering the increase and decrease in separate vouchers, and posting the offset to a clearing ledger account.</span></span>

-   <span data-ttu-id="65776-185">**الترحيل في ملخص إلى دفتر الأستاذ العام**</span><span class="sxs-lookup"><span data-stu-id="65776-185">**Post in summary to the general ledger**</span></span>

<span data-ttu-id="65776-186">غالباً ما تحتاج المؤسسات إلى الترحيل إلى دفتر الأستاذ العام في ملخص لتقليل كمية البيانات.</span><span class="sxs-lookup"><span data-stu-id="65776-186">Organizations often want to post to the general ledger in summary to minimize the amount of data.</span></span> <span data-ttu-id="65776-187">ومع ذلك، لا تزال المؤسسات عادةً تتطلب أن يتم الاحتفاظ بتفاصيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="65776-187">However, the organizations typically still require that the transaction detail be maintained.</span></span> <span data-ttu-id="65776-188">عند اكتمال الترحيل في الملخص من خلال إيصال واحد، تكون تفاصيل الحركة غير معروفة ولا يمكن الاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="65776-188">When posting is done in summary through a single voucher, the transaction detail isn't known and can't be maintained.</span></span>

   -   <span data-ttu-id="65776-189">نظراً لأنه حاليًا لا يمكن الاحتفاظ بتفاصيل الحركة، نوصي بعد استخدام الإيصال الواحد للترحيل في الملخص.</span><span class="sxs-lookup"><span data-stu-id="65776-189">Because the transaction detail currently can't be maintained, we recommend that One voucher not be used to post in summary.</span></span>
   -   <span data-ttu-id="65776-190">بعد الدعم لإزالة إيصال واحد، يمكننا تنفيذ المستند المصدر وأطر عمل المحاسبة في دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="65776-190">After support for One voucher is removed, we can implement the Source document and Accounting frameworks into the journals.</span></span> <span data-ttu-id="65776-191">ستحتفظ أطر العمل هذه بتفاصيل الحركة وتدعم التلخيص في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="65776-191">These frameworks, will then maintain the transaction detail and support summarization into the general ledger.</span></span>

-   <span data-ttu-id="65776-192">**تسوية مدفوعات غير مرحلة متعددة لنفس الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="65776-192">**Settle multiple unposted payments to the same invoice**</span></span>

<span data-ttu-id="65776-193">وعادةً ما يتم العثور على هذا السيناريو في مؤسسات البيع بالتجزئة حيث يمكن للعملاء استخدام عدة طرق دفع لدفع المشتريات.</span><span class="sxs-lookup"><span data-stu-id="65776-193">This scenario is typically found in retail organizations where customers can use multiple methods of payment to pay for purchases.</span></span> <span data-ttu-id="65776-194">في هذا السيناريو، يجب أن تكون المؤسسة قادرة على تسجيل مدفوعات غير مرحلة متعددة وتسويتها مقابل فاتورة العميل.</span><span class="sxs-lookup"><span data-stu-id="65776-194">In this scenario, the organization must be able to record multiple unposted payments and settle them against the customer invoice.</span></span>

<span data-ttu-id="65776-195">تعمل ميزة جديدة تمت إضافتها في الإصدار 1611 من Microsoft Dynamics 365 for Operations ‏(نوفمبر 2016) على تمكين تسوية مدفوعات غير مرحلة متعددة مقابل فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="65776-195">A new feature that was added in Microsoft Dynamics 365 for Operations version 1611 (November 2016) enables multiple unposted payments to be settled against a single invoice.</span></span> <span data-ttu-id="65776-196">لم يعد يلزم إدخال مدفوعات العملاء المتعددة في إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="65776-196">Multiple customer payments no longer have to be entered in a single voucher.</span></span>

-   <span data-ttu-id="65776-197">**استيراد حركات كشف الحساب البنكي**</span><span class="sxs-lookup"><span data-stu-id="65776-197">**Import bank statement transactions**</span></span>

<span data-ttu-id="65776-198">البنوك غالباً ما تدفع وتتلقي المدفوعات نيابةً عن مؤسسة، ويتم تسجيل هذه الحركات في Finance and Operations من خلال ملف يتم استلامه من البنك.</span><span class="sxs-lookup"><span data-stu-id="65776-198">Banks often pay and receive payments on an organization's behalf, and these transactions are recorded in Finance and Operations through a file that is received from the bank.</span></span> <span data-ttu-id="65776-199">تحتاج المؤسسات غالباً إلى جمع هذه الحركات مع بعضها باستخدام رقم كشف الحساب البنكي في الملف.</span><span class="sxs-lookup"><span data-stu-id="65776-199">Organizations often want to group together those transactions by using the bank statement number in the file.</span></span> <span data-ttu-id="65776-200">نظراً لظهور كل حركة بالتفصيل في كشف الحساب البنكي، لا يُتطلب أي تلخيص في دفتر الأستاذ الفرعي للبنك.</span><span class="sxs-lookup"><span data-stu-id="65776-200">Because each transaction is shown in detail on the bank statement, no summarization is required in the bank subledger.</span></span>

<span data-ttu-id="65776-201">يمكن تجميع الحركات باستخدام الحقول الأخرى في دفتر اليومية، مثل رقم دفعة دفتر اليومية نفسه أو رقم المستند.</span><span class="sxs-lookup"><span data-stu-id="65776-201">Transactions can be grouped by using other fields on the journal, such as the journal batch number itself or the document number.</span></span>

-   <span data-ttu-id="65776-202">**أرصدة التحويل**</span><span class="sxs-lookup"><span data-stu-id="65776-202">**Transfer balances**</span></span>

<span data-ttu-id="65776-203">قد تحتاج مؤسسة إلى تحويل رصيد من مورد واحد إلى مورد آخر، بسبب إما حدوث خطأ أو بسبب تحمل مورد آخر للمسؤولية القانونية.</span><span class="sxs-lookup"><span data-stu-id="65776-203">An organization might have to transfer a balance from one vendor to another vendor, either because of a mistake or because another vendor has taken over the liability.</span></span> <span data-ttu-id="65776-204">تحدث عمليات تحويل هذا النوع أيضًا لأنواع الحسابات مثل العملاء والحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="65776-204">Transfers of this type also occur for account types such as customers and bank accounts.</span></span>

<span data-ttu-id="65776-205">يمكن أن يتم تنفيذ تحويلات الأرصدة من حساب (المورد، والعميل، والحساب البنكي، وهكذا) إلى حساب آخر من خلال إيصالات منفصلة، ويمكن ترحيل المقابل إلى حساب دفتر أستاذ للمقاصة.</span><span class="sxs-lookup"><span data-stu-id="65776-205">Balance transfers from one account (vendor, customer, bank account, and so on) to another account can be done through separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

-   <span data-ttu-id="65776-206">**إدخال أرصدة البدء**</span><span class="sxs-lookup"><span data-stu-id="65776-206">**Enter beginning balances**</span></span>

<span data-ttu-id="65776-207">تقوم المؤسسات بإدخال أرصدة البداية غالبًا لحسابات دفتر الأستاذ الفرعي (الموردون، والعملاء، والأصول الثابتة، وهكذا) كحركة إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="65776-207">Organizations often enter beginning balances for subledger accounts (vendors, customers, fixed assets, and so on) as one voucher transaction.</span></span> <span data-ttu-id="65776-208">يمكن إدخال أرصدة البداية لكل حساب دفتر أستاذ فرعي على شكل إيصالات منفصلة، ويمكن ترحيل المقابل إلى حساب دفتر أستاذ للمقاصة.</span><span class="sxs-lookup"><span data-stu-id="65776-208">Beginning balances for each subledger account can be entered as separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

-   <span data-ttu-id="65776-209">**تصحيح الإدخال المحاسبي لمستند عميل أو مورد مرّحل**</span><span class="sxs-lookup"><span data-stu-id="65776-209">**Correct the accounting entry of a posted customer or vendor document**</span></span>

<span data-ttu-id="65776-210">قد تحتاج مؤسسة إلى تصحيح حساب دفتر أستاذ الحسابات المدينة أو الحسابات الدائنة لإدخال محاسبة فاتورة مرّحلة، ولكن لا يمكن إلغاء هذه الفاتورة أو تصحيحها من خلال آلية أخرى.</span><span class="sxs-lookup"><span data-stu-id="65776-210">An organization might have to correct the Accounts receivable or Accounts payable ledger account for an accounting entry of a posted invoice, but that invoice can't be reversed or corrected through another mechanism.</span></span>

<span data-ttu-id="65776-211">إذا كان يجب إجراء تصحيح لحساب دفتر أستاذ الحسابات المدينة أو الحسابات الدائنة، يجب إجراء تسوية مباشرةً لحساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="65776-211">If a correction must be made to the accounts receivable or accounts payable ledger account, an adjustment must be made directly to the ledger account.</span></span> <span data-ttu-id="65776-212">لا يمكن إجراء التسوية عن طريق الترحيل من خلال المورد أو العميل.</span><span class="sxs-lookup"><span data-stu-id="65776-212">The adjustment can't be made by posting through the vendor or customer.</span></span> <span data-ttu-id="65776-213">تتطلب هذه الطريقة أن يتم إجراء التسوية خلال "وقت تعطل"، حتى يمكن حساب دفتر الأستاذ السماح بالإدخال اليدوي مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="65776-213">This approach requires that the adjustment be made during a "down time," so that the ledger account can temporarily allow manual entry.</span></span>

-   <span data-ttu-id="65776-214">**"النظام يسمح بها"**</span><span class="sxs-lookup"><span data-stu-id="65776-214">**"The system allows it"**</span></span>

<span data-ttu-id="65776-215">تستخدم المؤسسات غالباً وظيفة الإيصال الواحد فقط لأن النظام يسمح لهم باستخدامها، بدون فهم التبعات.</span><span class="sxs-lookup"><span data-stu-id="65776-215">Organizations often use the One voucher functionality merely because the system lets them use it, without understanding the implications.</span></span>

