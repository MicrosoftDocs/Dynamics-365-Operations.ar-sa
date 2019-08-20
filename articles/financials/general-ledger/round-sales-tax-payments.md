---
title: مدفوعات ضريبة المبيعات وقواعد التقريب
description: توضح هذه المقالة كيفية عمل إعداد قاعدة التقريب في هيئات ضريبة المبيعات‬ وتقريب موازنة ضريبة المبيعات أثناء وظيفة تسوية ضريبة المبيعات وترحيلها‬.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834988"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="6248d-103">مدفوعات ضريبة المبيعات وقواعد التقريب</span><span class="sxs-lookup"><span data-stu-id="6248d-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6248d-104">توضح هذه المقالة كيفية عمل إعداد قاعدة التقريب في هيئات ضريبة المبيعات‬ وتقريب موازنة ضريبة المبيعات أثناء وظيفة تسوية ضريبة المبيعات وترحيلها‬.</span><span class="sxs-lookup"><span data-stu-id="6248d-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="6248d-105">بشكل دوري، يلزم الإبلاغ عن ضريبة المبيعات ودفعها للسلطات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="6248d-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="6248d-106">‏‫ويمكن القيام بهذا عن طريق إجراء عملية تسوية وترحيل ضريبة المبيعات في صفحة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6248d-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="6248d-107">وستتم تسوية ضريبة المبيعات لفترة في مقابل حسابات ضريبة المبيعات، وسيتم ترحيل رصيد ضريبة المبيعات إلى حساب تسوية ضريبة المبيعات.‬</span><span class="sxs-lookup"><span data-stu-id="6248d-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="6248d-108">ويتم تقريب رصيد ضريبة المبيعات، الذي يتم ترحيله في حساب تسوية ضريبة المبيعات، حسب ما تتطلبه السلطات الضريبية من خلال إعداد قاعدة تقريب في صفحة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6248d-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="6248d-109">يتم ترحيل الفرق التقريبي إلى الحساب الضريبي لضريبة المبيعات المحدد في حقل الحسابات للحركات التلقائية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6248d-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="6248d-110">يوضح المثال أدناه كيفية عمل قاعدة التقريب في سلطة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6248d-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="6248d-111">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6248d-111">Examples</span></span>

<span data-ttu-id="6248d-112">تعرض ضريبة المبيعات الإجمالية لفترة رصيد دائن بمبلغ -98,765.43.</span><span class="sxs-lookup"><span data-stu-id="6248d-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="6248d-113">قام الكيان القانوني بجمع ضرائب مبيعات أكثر مما دفع.</span><span class="sxs-lookup"><span data-stu-id="6248d-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="6248d-114">ولذلك، تدين الكيان القانوني بأموال لهيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="6248d-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="6248d-115">ويرغب الكيان القانوني في استخدام أسلوب التقريب الذي يقرب الرصيد إلى أقرب 1.00.</span><span class="sxs-lookup"><span data-stu-id="6248d-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="6248d-116">ويقوم المستخدم المسؤول عن محاسبة ضرائب المبيعات بإجراء الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6248d-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="6248d-117">النقر فوق ضريبة‬ &gt; ضرائب غير مباشرة &gt; ضريبة مبيعات &gt; هيئات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6248d-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="6248d-118">في علامة التبويب السريع "عام"، حدد "عادي" في حقل نموذج التقريب.</span><span class="sxs-lookup"><span data-stu-id="6248d-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="6248d-119">في حقل "تقريب العلامات العشرية‬"، أدخل 1.00.</span><span class="sxs-lookup"><span data-stu-id="6248d-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="6248d-120">وعند حلول وقت دفع ضرائب المبيعات إلى هيئة الضرائب، افتح صفحة تسوية وترحيل ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6248d-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="6248d-121">(انقر فوق ضريبة‬ &gt; إقرارات &gt; ضريبة مبيعات &gt; تسوية وترحيل ضريبة المبيعات.)</span><span class="sxs-lookup"><span data-stu-id="6248d-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="6248d-122">في حساب تسوية ضريبة المبيعات، يتم تقريب مبلغ المسؤولية الضريبية من 98,765.43 إلى 98,765.</span><span class="sxs-lookup"><span data-stu-id="6248d-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="6248d-123">يوضح الجدول التالي كيف يتم تقريب مبلغ 98,765.43 باستخدام كل أسلوب تقريب يتوفر في حقل نموذج التقريب في صفحة سلطات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6248d-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="6248d-124">خيار نموذج التقريب</span><span class="sxs-lookup"><span data-stu-id="6248d-124">Rounding form option</span></span>                | <span data-ttu-id="6248d-125">قيمة التقريب = 0.01</span><span class="sxs-lookup"><span data-stu-id="6248d-125">Round-off value = 0.01</span></span> | <span data-ttu-id="6248d-126">قيمة التقريب = 0.10</span><span class="sxs-lookup"><span data-stu-id="6248d-126">Round-off value = 0.10</span></span> | <span data-ttu-id="6248d-127">قيمة التقريب = 1.00</span><span class="sxs-lookup"><span data-stu-id="6248d-127">Round-off value = 1.00</span></span> | <span data-ttu-id="6248d-128">قيمة التقريب = 100.00</span><span class="sxs-lookup"><span data-stu-id="6248d-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="6248d-129">عادي</span><span class="sxs-lookup"><span data-stu-id="6248d-129">Normal</span></span>                              | <span data-ttu-id="6248d-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6248d-130">98,765.43</span></span>              | <span data-ttu-id="6248d-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="6248d-131">98,765.40</span></span>              | <span data-ttu-id="6248d-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="6248d-132">98,765.00</span></span>              | <span data-ttu-id="6248d-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6248d-133">98,800.00</span></span>                |
| <span data-ttu-id="6248d-134">انحداري</span><span class="sxs-lookup"><span data-stu-id="6248d-134">Downward</span></span>                            | <span data-ttu-id="6248d-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6248d-135">98,765.43</span></span>              | <span data-ttu-id="6248d-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="6248d-136">98,765.40</span></span>              | <span data-ttu-id="6248d-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="6248d-137">98,765.00</span></span>              | <span data-ttu-id="6248d-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="6248d-138">98,700.00</span></span>                |
| <span data-ttu-id="6248d-139">التقريب</span><span class="sxs-lookup"><span data-stu-id="6248d-139">Rounding-up</span></span>                         | <span data-ttu-id="6248d-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6248d-140">98,765.43</span></span>              | <span data-ttu-id="6248d-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="6248d-141">98,765.50</span></span>              | <span data-ttu-id="6248d-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="6248d-142">98,766.00</span></span>              | <span data-ttu-id="6248d-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6248d-143">98,800.00</span></span>                |
| <span data-ttu-id="6248d-144">ميزة خاصة، لرصيد دائن</span><span class="sxs-lookup"><span data-stu-id="6248d-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="6248d-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6248d-145">98,765.43</span></span>              | <span data-ttu-id="6248d-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="6248d-146">98,765.40</span></span>              | <span data-ttu-id="6248d-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="6248d-147">98,765.00</span></span>              | <span data-ttu-id="6248d-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="6248d-148">98,700.00</span></span>                |
| <span data-ttu-id="6248d-149">ميزة خاصة، لرصيد مدين</span><span class="sxs-lookup"><span data-stu-id="6248d-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="6248d-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6248d-150">98,765.43</span></span>              | <span data-ttu-id="6248d-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="6248d-151">98,765.50</span></span>              | <span data-ttu-id="6248d-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="6248d-152">98,766.00</span></span>              | <span data-ttu-id="6248d-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6248d-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="6248d-154">بدون تقريب على الإطلاق، بما أن التقريب هو 0.00</span><span class="sxs-lookup"><span data-stu-id="6248d-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="6248d-155">round(1.0151, 0.00) = 1.0151 دائرية (1.0149 أو 0.00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="6248d-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="6248d-156">تقريب عادي، ودقة التقريب هي 0.01</span><span class="sxs-lookup"><span data-stu-id="6248d-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="6248d-157">تقريب</span><span class="sxs-lookup"><span data-stu-id="6248d-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="6248d-158">عملية الحساب</span><span class="sxs-lookup"><span data-stu-id="6248d-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6248d-159">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="6248d-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="6248d-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="6248d-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="6248d-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="6248d-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6248d-162">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="6248d-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6248d-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="6248d-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="6248d-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="6248d-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6248d-165">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="6248d-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6248d-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="6248d-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="6248d-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="6248d-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6248d-168">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="6248d-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6248d-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="6248d-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="6248d-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="6248d-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="6248d-171">إذا قمت بتحديد ميزة خاصة، يكون التقريب دائماً في صالح الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="6248d-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="6248d-172">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="6248d-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="6248d-173">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6248d-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="6248d-174">إنشاء دفع ضريبة مبيعات</span><span class="sxs-lookup"><span data-stu-id="6248d-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="6248d-175">إنشاء حركات المبيعات في المستندات</span><span class="sxs-lookup"><span data-stu-id="6248d-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="6248d-176">عرض حركات ضرائب المبيعات المُرَّحلة</span><span class="sxs-lookup"><span data-stu-id="6248d-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="6248d-177">الدالة round</span><span class="sxs-lookup"><span data-stu-id="6248d-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


