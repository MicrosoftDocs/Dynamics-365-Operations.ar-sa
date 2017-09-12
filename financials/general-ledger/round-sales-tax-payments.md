---
title: "مدفوعات ضريبة المبيعات وقواعد التقريب"
description: "توضح هذه المقالة كيفية عمل إعداد قاعدة التقريب في هيئات ضريبة المبيعات‬ وتقريب موازنة ضريبة المبيعات أثناء وظيفة تسوية ضريبة المبيعات وترحيلها‬."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 8de01b77fcbeb65321e60614b6a11d264460208f
ms.contentlocale: ar-sa
ms.lasthandoff: 08/01/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="93ebc-103">مدفوعات ضريبة المبيعات وقواعد التقريب</span><span class="sxs-lookup"><span data-stu-id="93ebc-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="93ebc-104">توضح هذه المقالة كيفية عمل إعداد قاعدة التقريب في هيئات ضريبة المبيعات‬ وتقريب موازنة ضريبة المبيعات أثناء وظيفة تسوية ضريبة المبيعات وترحيلها‬.</span><span class="sxs-lookup"><span data-stu-id="93ebc-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="93ebc-105">بشكل دوري، يلزم الإبلاغ عن ضريبة المبيعات ودفعها للسلطات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="93ebc-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="93ebc-106">‏‫ويمكن القيام بهذا عن طريق إجراء عملية تسوية وترحيل ضريبة المبيعات في صفحة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="93ebc-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="93ebc-107">وستتم تسوية ضريبة المبيعات لفترة في مقابل حسابات ضريبة المبيعات، وسيتم ترحيل رصيد ضريبة المبيعات إلى حساب تسوية ضريبة المبيعات.‬</span><span class="sxs-lookup"><span data-stu-id="93ebc-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="93ebc-108">ويتم تقريب رصيد ضريبة المبيعات، الذي يتم ترحيله في حساب تسوية ضريبة المبيعات، حسب ما تتطلبه السلطات الضريبية من خلال إعداد قاعدة تقريب في صفحة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="93ebc-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="93ebc-109">يتم ترحيل الفرق التقريبي إلى الحساب الضريبي لضريبة المبيعات المحدد في حقل الحسابات للحركات التلقائية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="93ebc-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="93ebc-110">يوضح المثال أدناه كيفية عمل قاعدة التقريب في سلطة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="93ebc-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="93ebc-111">مثال:</span><span class="sxs-lookup"><span data-stu-id="93ebc-111">Example:</span></span>

<span data-ttu-id="93ebc-112">تعرض ضريبة المبيعات الإجمالية لفترة رصيد دائن بمبلغ -98,765.43.</span><span class="sxs-lookup"><span data-stu-id="93ebc-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="93ebc-113">قام الكيان القانوني بجمع ضرائب مبيعات أكثر مما دفع.</span><span class="sxs-lookup"><span data-stu-id="93ebc-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="93ebc-114">ولذلك، تدين الكيان القانوني بأموال لهيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="93ebc-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="93ebc-115">ويرغب الكيان القانوني في استخدام أسلوب التقريب الذي يقرب الرصيد إلى أقرب 1.00.</span><span class="sxs-lookup"><span data-stu-id="93ebc-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="93ebc-116">ويقوم المستخدم المسؤول عن محاسبة ضرائب المبيعات بإجراء الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="93ebc-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="93ebc-117">النقر فوق ضريبة‬ &gt; ضرائب غير مباشرة &gt; ضريبة مبيعات &gt; هيئات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="93ebc-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="93ebc-118">في علامة التبويب السريع "عام"، حدد "عادي" في حقل نموذج التقريب.</span><span class="sxs-lookup"><span data-stu-id="93ebc-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="93ebc-119">في حقل "تقريب العلامات العشرية‬"، أدخل 1.00.</span><span class="sxs-lookup"><span data-stu-id="93ebc-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="93ebc-120">وعند حلول وقت دفع ضرائب المبيعات إلى هيئة الضرائب، افتح صفحة تسوية وترحيل ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="93ebc-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="93ebc-121">(انقر فوق ضريبة‬ &gt; إقرارات &gt; ضريبة مبيعات &gt; تسوية وترحيل ضريبة المبيعات.)</span><span class="sxs-lookup"><span data-stu-id="93ebc-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="93ebc-122">في حساب تسوية ضريبة المبيعات، يتم تقريب مبلغ المسؤولية الضريبية من 98,765.43 إلى 98,765.</span><span class="sxs-lookup"><span data-stu-id="93ebc-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="93ebc-123">يوضح الجدول التالي كيف يتم تقريب مبلغ 98,765.43 باستخدام كل أسلوب تقريب يتوفر في حقل نموذج التقريب في صفحة سلطات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="93ebc-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="93ebc-124">خيار نموذج التقريب</span><span class="sxs-lookup"><span data-stu-id="93ebc-124">Rounding form option</span></span>                | <span data-ttu-id="93ebc-125">قيمة التقريب = 0.01</span><span class="sxs-lookup"><span data-stu-id="93ebc-125">Round-off value = 0.01</span></span> | <span data-ttu-id="93ebc-126">قيمة التقريب = 0.10</span><span class="sxs-lookup"><span data-stu-id="93ebc-126">Round-off value = 0.10</span></span> | <span data-ttu-id="93ebc-127">قيمة التقريب = 1.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-127">Round-off value = 1.00</span></span> | <span data-ttu-id="93ebc-128">قيمة التقريب = 100.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="93ebc-129">عادي</span><span class="sxs-lookup"><span data-stu-id="93ebc-129">Normal</span></span>                              | <span data-ttu-id="93ebc-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="93ebc-130">98,765.43</span></span>              | <span data-ttu-id="93ebc-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="93ebc-131">98,765.40</span></span>              | <span data-ttu-id="93ebc-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-132">98,765.00</span></span>              | <span data-ttu-id="93ebc-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-133">98,800.00</span></span>                |
| <span data-ttu-id="93ebc-134">انحداري</span><span class="sxs-lookup"><span data-stu-id="93ebc-134">Downward</span></span>                            | <span data-ttu-id="93ebc-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="93ebc-135">98,765.43</span></span>              | <span data-ttu-id="93ebc-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="93ebc-136">98,765.40</span></span>              | <span data-ttu-id="93ebc-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-137">98,765.00</span></span>              | <span data-ttu-id="93ebc-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-138">98,700.00</span></span>                |
| <span data-ttu-id="93ebc-139">التقريب</span><span class="sxs-lookup"><span data-stu-id="93ebc-139">Rounding-up</span></span>                         | <span data-ttu-id="93ebc-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="93ebc-140">98,765.43</span></span>              | <span data-ttu-id="93ebc-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="93ebc-141">98,765.50</span></span>              | <span data-ttu-id="93ebc-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-142">98,766.00</span></span>              | <span data-ttu-id="93ebc-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-143">98,800.00</span></span>                |
| <span data-ttu-id="93ebc-144">ميزة خاصة، لرصيد دائن</span><span class="sxs-lookup"><span data-stu-id="93ebc-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="93ebc-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="93ebc-145">98,765.43</span></span>              | <span data-ttu-id="93ebc-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="93ebc-146">98,765.40</span></span>              | <span data-ttu-id="93ebc-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-147">98,765.00</span></span>              | <span data-ttu-id="93ebc-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-148">98,700.00</span></span>                |
| <span data-ttu-id="93ebc-149">ميزة خاصة، لرصيد مدين</span><span class="sxs-lookup"><span data-stu-id="93ebc-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="93ebc-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="93ebc-150">98,765.43</span></span>              | <span data-ttu-id="93ebc-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="93ebc-151">98,765.50</span></span>              | <span data-ttu-id="93ebc-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-152">98,766.00</span></span>              | <span data-ttu-id="93ebc-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="93ebc-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="93ebc-154">إذا قمت بتحديد ميزة خاصة، يكون التقريب دائماً في صالح الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="93ebc-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="93ebc-155">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="93ebc-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="93ebc-156">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="93ebc-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="93ebc-157">إنشاء دفع ضريبة مبيعات</span><span class="sxs-lookup"><span data-stu-id="93ebc-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="93ebc-158">إنشاء حركات المبيعات في المستندات</span><span class="sxs-lookup"><span data-stu-id="93ebc-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="93ebc-159">عرض حركات ضرائب المبيعات المُرَّحلة</span><span class="sxs-lookup"><span data-stu-id="93ebc-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



