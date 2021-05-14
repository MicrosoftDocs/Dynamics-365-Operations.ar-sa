---
title: لم يتم حساب الضريبة أو قيمه مبلغ الضريبة صفرا
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها التي يمكن ان تساعد عندما يكون مبلغ الضريبة يساوي 0 (صفر) أو إذا لم يتم حساب الضريبة.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947590"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="a7e70-103">لم يتم حساب الضريبة أو قيمه مبلغ الضريبة صفرا</span><span class="sxs-lookup"><span data-stu-id="a7e70-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7e70-104">قد يكون للحركة مبلغ بند ليس 0 (صفر)، ولكن اما انه لم يتم حساب الضريبة أو ان مبلغ الضريبة المحسوب هو 0.</span><span class="sxs-lookup"><span data-stu-id="a7e70-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="a7e70-105">لاستكشاف هذه المشكلة وإصلاحها، اتبع الخطوات الواردة في الأقسام التالية عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="a7e70-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="a7e70-106">التحقق من ان أكواد الضريبة محدده بشكل صحيح بواسطة الحركة</span><span class="sxs-lookup"><span data-stu-id="a7e70-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="a7e70-107">في حاله عدم تحديد الحركة لأكواد الضرائب الصحيحة، أو في حاله عدم تحديد إيه أكواد ضريبة، لن يتم حساب الضرائب عليها.</span><span class="sxs-lookup"><span data-stu-id="a7e70-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="a7e70-108">اتبع هذه الخطوات للتحقق من تحديد أكواد الضرائب بشكل صحيح بواسطة المعاملة.</span><span class="sxs-lookup"><span data-stu-id="a7e70-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="a7e70-109">في بند الحركة، في علامة التبويب السريعة **تفاصيل البند**، في علامة التبويب **إعداد**، في قسم **ضريبة المبيعات**، تحقق من تحديد مجموعات الضرائب الصحيحة في حقلي **مجموعة ضريب مبيعات الصنف** و **مجموعة ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="a7e70-110">إذا لم يتم تحديد مجموعات الضرائب الصحيحة، فقم بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="a7e70-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="a7e70-111">[![مجموعة ضريبة مبيعات الصنف وحقول مجموعة ضريبة المبيعات](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="a7e70-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="a7e70-112">انتقل إلى **الضريبة** \> **الضرائب غير المباشرة** \> **ضريبة المبيعات** \> **مجموعات ضرائب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="a7e70-113">حدد مجموعة ضريبة المبيعات المناسبة، ثم على علامة التبويب السريعة **الإعداد**، قم بتدوين رمز الضريبة في حقل **رمز ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="a7e70-114">[![صفحة مجموعات ضرائب المبيعات](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="a7e70-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="a7e70-115">انتقل إلى **الضريبة** \> **الضرائب غير المباشرة** \> **ضريبة المبيعات** \> **مجموعات ضرائب مبيعات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="a7e70-116">حدد مجموعة ضريبة مبيعات الصنف المناسبة، ثم في علامة التبويب السريعة **الإعداد**، تحقق من أن رمز الضريبة في حقل **رمز ضريبة المبيعات** يتطابق مع رمز ضريبة مجموعة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a7e70-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="a7e70-117">[![صفحة مجموعات ضرائب مبيعات الأصناف](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="a7e70-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="a7e70-118">إذا لم تكن أكواد الضريبة متطابقة، فقم بتحديث كود ضريبة المبيعات لأحدي المجموعات.</span><span class="sxs-lookup"><span data-stu-id="a7e70-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="a7e70-119">التحقق من ان أكواد الضريبة المحددة لا معفاه وانها تحتوي علي قيمه السعر الضريبي الصحيحة</span><span class="sxs-lookup"><span data-stu-id="a7e70-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="a7e70-120">في حاله اعفاء أكواد الضريبة، أو إذا كان معدل الضريبة 0 (صفر)، ستكون نتيجة حساب الضريبة 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="a7e70-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="a7e70-121">اتبع الخطوات التالية لتحديد ما إذا كانت أكواد الضرائب المحددة معفاه وللتحقق من انه يتم تطبيق معدل الضريبة الصحيح عليها.</span><span class="sxs-lookup"><span data-stu-id="a7e70-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="a7e70-122">انتقل إلى **الضريبة** \> **الضرائب غير المباشرة** \> **ضريبة المبيعات** \> **مجموعات ضرائب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="a7e70-123">حدد مجموعه ضريبة المبيعات المناسبة، ثم في علامة التبويب السريعة **الإعداد**، تحقق من إلغاء تحديد خانه الاختيار **إعفاء**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="a7e70-124">وفي حاله تحديدها، قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="a7e70-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="a7e70-125">[![خانه اختيار الاعفاء في صفحة مجموعات ضريبة المبيعات](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="a7e70-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="a7e70-126">انتقل إلى **الضريبة** \> **الضرائب غير المباشرة** \> **ضريبة المبيعات** \> **رموز ضرائب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="a7e70-127">حدد كود ضريبة المبيعات المناسب، ثم تحقق من ان قيمه سعر الضريبة في حقل **القيمة** ليست 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="a7e70-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="a7e70-128">إذا كانت القيمة هي 0، فقم بتحديث الحقل بحيث يتم تعيينه علي معدل الضريبة الصحيح.</span><span class="sxs-lookup"><span data-stu-id="a7e70-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="a7e70-129">[![حقل القيمة في صفحة قيم رمز ضريبة المبيعات](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="a7e70-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="a7e70-130">تحديد ما إذا كان الصفر هو مبلغ الضريبة الصحيح ام لا</span><span class="sxs-lookup"><span data-stu-id="a7e70-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="a7e70-131">في بعض وحدات السيناريو، يكون مبلغ الضريبة 0 (صفر) صحيحا.</span><span class="sxs-lookup"><span data-stu-id="a7e70-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="a7e70-132">اتبع الخطوات التالية لتحديد ما إذا كانت قيمه 0 هي مبلغ الضريبة الصحيح لحركك.</span><span class="sxs-lookup"><span data-stu-id="a7e70-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="a7e70-133">انتقل إلى **دفتر الأستاذ العام** \> **إعداد دفتر الأستاذ** \> **معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="a7e70-134">في علامة التبويب **ضريبة المبيعات**، في حقل **طريقة الحساب**، تحقق من تحديد **الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="a7e70-135">[![حقل طريقة الحساب في صفحة معلمات دفتر الأستاذ العام](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="a7e70-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="a7e70-136">انتقل إلى **الضريبة** \> **الضرائب غير المباشرة** \> **ضريبة المبيعات** \> **رموز ضرائب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="a7e70-137">حدد رمز ضريبة المبيعات المناسب، وحدد **حساب** \> **القاعدة الهامشية**، وتحقق من أن القاعدة الهامشية معينة على **صافي مبلغ رصيد الفاتورة** أو **إجمالي الفاتورة بما في ذلك مبالغ ضريبة المبيعات الأخرى**.</span><span class="sxs-lookup"><span data-stu-id="a7e70-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="a7e70-138">لمزيد من المعلومات، راجع [إجمالي الفاتورة متضمنًا مبالغ ضريبة المبيعات الأخرى‬](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="a7e70-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="a7e70-139">في حاله تعيين القيم الصحيحة في الخطوتين 2 و 4، حدد ما إذا كان المبلغ الإجمالي للحركة هو 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="a7e70-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="a7e70-140">إذا كان المبلغ الإجمالي هو 0، فان مبلغ الضريبة 0 هو النتيجة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="a7e70-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="a7e70-141">نظرا لان حساب الضريبة يعتمد علي المبلغ الإجمالي لرصيد الفاتورة، وان هذا المبلغ ليس بندا ببند، سيتم تخصيص مبلغ الضريبة 0 لكل بند بعد حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="a7e70-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="a7e70-142">حدد ما إذا كان التخصيص موجودًا</span><span class="sxs-lookup"><span data-stu-id="a7e70-142">Determine whether customization exists</span></span>

<span data-ttu-id="a7e70-143">إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="a7e70-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="a7e70-144">في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.</span><span class="sxs-lookup"><span data-stu-id="a7e70-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
