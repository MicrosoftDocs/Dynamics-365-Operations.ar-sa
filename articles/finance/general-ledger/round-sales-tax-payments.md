---
title: مدفوعات ضريبة المبيعات وقواعد التقريب
description: توضح هذه المقالة كيفية عمل إعداد قاعدة التقريب في هيئات ضريبة المبيعات‬ وتقريب موازنة ضريبة المبيعات أثناء وظيفة تسوية ضريبة المبيعات وترحيلها‬.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7be9be728a6515bb1fc1c9bc90938a3d33ea8da8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204944"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="08219-103">مدفوعات ضريبة المبيعات وقواعد التقريب</span><span class="sxs-lookup"><span data-stu-id="08219-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08219-104">توضح هذه المقالة كيفية عمل إعداد قاعدة التقريب في هيئات ضريبة المبيعات‬ وتقريب موازنة ضريبة المبيعات أثناء وظيفة تسوية ضريبة المبيعات وترحيلها‬.</span><span class="sxs-lookup"><span data-stu-id="08219-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="08219-105">بشكل دوري، يلزم الإبلاغ عن ضريبة المبيعات ودفعها للسلطات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="08219-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="08219-106">‏‫ويمكن القيام بهذا عن طريق إجراء عملية تسوية وترحيل ضريبة المبيعات في صفحة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="08219-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="08219-107">وستتم تسوية ضريبة المبيعات لفترة في مقابل حسابات ضريبة المبيعات، وسيتم ترحيل رصيد ضريبة المبيعات إلى حساب تسوية ضريبة المبيعات.‬</span><span class="sxs-lookup"><span data-stu-id="08219-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="08219-108">ويتم تقريب رصيد ضريبة المبيعات، الذي يتم ترحيله في حساب تسوية ضريبة المبيعات، حسب ما تتطلبه السلطات الضريبية من خلال إعداد قاعدة تقريب في صفحة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="08219-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="08219-109">يتم ترحيل الفرق التقريبي إلى الحساب الضريبي لضريبة المبيعات المحدد في حقل الحسابات للحركات التلقائية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="08219-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="08219-110">يوضح المثال أدناه كيفية عمل قاعدة التقريب في سلطة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="08219-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="08219-111">أمثلة</span><span class="sxs-lookup"><span data-stu-id="08219-111">Examples</span></span>

<span data-ttu-id="08219-112">تعرض ضريبة المبيعات الإجمالية لفترة رصيد دائن بمبلغ -98,765.43.</span><span class="sxs-lookup"><span data-stu-id="08219-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="08219-113">قام الكيان القانوني بجمع ضرائب مبيعات أكثر مما دفع.</span><span class="sxs-lookup"><span data-stu-id="08219-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="08219-114">ولذلك، تدين الكيان القانوني بأموال لهيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="08219-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="08219-115">ويرغب الكيان القانوني في استخدام أسلوب التقريب الذي يقرب الرصيد إلى أقرب 1.00.</span><span class="sxs-lookup"><span data-stu-id="08219-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="08219-116">ويقوم المستخدم المسؤول عن محاسبة ضرائب المبيعات بإجراء الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="08219-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="08219-117">انقر فوق **الضريبة** > **الضرائب غير المباشرة** > **ضريبة المبيعات** > **سلطات ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="08219-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="08219-118">في علامة التبويب السريعة **عام**، في حقل **نموذج التقريب**، حدد **عادي**.</span><span class="sxs-lookup"><span data-stu-id="08219-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="08219-119">في حقل **تقريب العلامات العشرية**، أدخل 1.00.</span><span class="sxs-lookup"><span data-stu-id="08219-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="08219-120">عندما يحين وقت ضرائب المبيعات إلى سلطة الضرائب، اذهب إلى **الضرائب** > **الإقرارات** > **ضريبة المبيعات** > **تسوية وترحيل ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="08219-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="08219-121">في حساب تسوية ضريبة المبيعات، يمكنك أن ترى أن مبلع الالتزام الضريبي بقيمة **98,765.43** قد تم تقريبه إلى **98,765**.</span><span class="sxs-lookup"><span data-stu-id="08219-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="08219-122">يوضح الجدول التالي كيف يتم تقريب مبلغ 98,765.43 باستخدام كل أسلوب تقريب يتوفر في حقل **نموذج التقريب** في صفحة **سلطات ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="08219-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="08219-123">إذا تم تعيين قيمة التقريب إلى 0.00، فمن ثم:</span><span class="sxs-lookup"><span data-stu-id="08219-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="08219-124">للتقريب العادي، يكون سلوك التقريب هو نفسه الخاص بـ **تقريب العلامات العشرية = 0.01.**</span><span class="sxs-lookup"><span data-stu-id="08219-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="08219-125">مع **خيارات نموذج التقريب**، **انحداري** و **التقريب** و **ميزة خاصة**، يكون السلوك متماثلا كما في **تقريب العلامة العشرية= 1.00**.</span><span class="sxs-lookup"><span data-stu-id="08219-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="08219-126">خيار نموذج التقريب</span><span class="sxs-lookup"><span data-stu-id="08219-126">Rounding form option</span></span>                | <span data-ttu-id="08219-127">قيمة التقريب = 0.01</span><span class="sxs-lookup"><span data-stu-id="08219-127">Round-off value = 0.01</span></span> | <span data-ttu-id="08219-128">قيمة التقريب = 0.10</span><span class="sxs-lookup"><span data-stu-id="08219-128">Round-off value = 0.10</span></span> | <span data-ttu-id="08219-129">قيمة التقريب = 1.00</span><span class="sxs-lookup"><span data-stu-id="08219-129">Round-off value = 1.00</span></span> | <span data-ttu-id="08219-130">قيمة التقريب = 100.00</span><span class="sxs-lookup"><span data-stu-id="08219-130">Round-off value = 100.00</span></span> | <span data-ttu-id="08219-131">قيمة التقريب = 0.00</span><span class="sxs-lookup"><span data-stu-id="08219-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="08219-132">عادي</span><span class="sxs-lookup"><span data-stu-id="08219-132">Normal</span></span>                              | <span data-ttu-id="08219-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="08219-133">98,765.43</span></span>              | <span data-ttu-id="08219-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="08219-134">98,765.40</span></span>              | <span data-ttu-id="08219-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="08219-135">98,765.00</span></span>              | <span data-ttu-id="08219-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="08219-136">98,800.00</span></span>                | <span data-ttu-id="08219-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="08219-137">98,765.43</span></span>                |
| <span data-ttu-id="08219-138">انحداري</span><span class="sxs-lookup"><span data-stu-id="08219-138">Downward</span></span>                            | <span data-ttu-id="08219-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="08219-139">98,765.43</span></span>              | <span data-ttu-id="08219-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="08219-140">98,765.40</span></span>              | <span data-ttu-id="08219-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="08219-141">98,765.00</span></span>              | <span data-ttu-id="08219-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="08219-142">98,700.00</span></span>                | <span data-ttu-id="08219-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="08219-143">98,765.00</span></span>                |
| <span data-ttu-id="08219-144">التقريب</span><span class="sxs-lookup"><span data-stu-id="08219-144">Rounding-up</span></span>                         | <span data-ttu-id="08219-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="08219-145">98,765.43</span></span>              | <span data-ttu-id="08219-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="08219-146">98,765.50</span></span>              | <span data-ttu-id="08219-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="08219-147">98,766.00</span></span>              | <span data-ttu-id="08219-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="08219-148">98,800.00</span></span>                | <span data-ttu-id="08219-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="08219-149">98,766.00</span></span>                |
| <span data-ttu-id="08219-150">ميزة خاصة، لرصيد دائن</span><span class="sxs-lookup"><span data-stu-id="08219-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="08219-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="08219-151">98,765.43</span></span>              | <span data-ttu-id="08219-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="08219-152">98,765.40</span></span>              | <span data-ttu-id="08219-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="08219-153">98,765.00</span></span>              | <span data-ttu-id="08219-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="08219-154">98,700.00</span></span>                | <span data-ttu-id="08219-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="08219-155">98,765.00</span></span>                |
| <span data-ttu-id="08219-156">ميزة خاصة، لرصيد مدين</span><span class="sxs-lookup"><span data-stu-id="08219-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="08219-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="08219-157">98,765.43</span></span>              | <span data-ttu-id="08219-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="08219-158">98,765.50</span></span>              | <span data-ttu-id="08219-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="08219-159">98,766.00</span></span>              | <span data-ttu-id="08219-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="08219-160">98,800.00</span></span>                | <span data-ttu-id="08219-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="08219-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="08219-162">تقريب عادي، ودقة التقريب هي 0.01</span><span class="sxs-lookup"><span data-stu-id="08219-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="08219-163">تقريب</span><span class="sxs-lookup"><span data-stu-id="08219-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="08219-164">عملية الحساب</span><span class="sxs-lookup"><span data-stu-id="08219-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="08219-165">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="08219-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="08219-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="08219-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="08219-167">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="08219-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="08219-168">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="08219-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="08219-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="08219-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="08219-170">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="08219-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="08219-171">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="08219-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="08219-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="08219-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="08219-173">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="08219-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="08219-174">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="08219-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="08219-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="08219-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="08219-176">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="08219-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="08219-177">إذا قمت بتحديد ميزة خاصة، يكون التقريب دائماً في صالح الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="08219-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="08219-178">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="08219-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="08219-179">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="08219-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="08219-180">إنشاء دفع ضريبة مبيعات</span><span class="sxs-lookup"><span data-stu-id="08219-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="08219-181">إنشاء حركات ضريبة المبيعات في المستندات</span><span class="sxs-lookup"><span data-stu-id="08219-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="08219-182">عرض حركات ضرائب المبيعات المُرَّحلة</span><span class="sxs-lookup"><span data-stu-id="08219-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="08219-183">الدالة round</span><span class="sxs-lookup"><span data-stu-id="08219-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]