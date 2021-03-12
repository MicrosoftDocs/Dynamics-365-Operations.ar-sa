---
title: أنواع ترحيل الإيجار
description: يصف هذا الموضوع أنواع الترحيل المستخدمة لحركات تأجير الأصول.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b79b02f7e241783d19a315ccff5bb6874a238c38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995408"
---
# <a name="lease-posting-types"></a><span data-ttu-id="0d87a-103">أنواع ترحيل الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d87a-104">يصف هذا الموضوع أنواع الترحيل المستخدمة لحركات تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="0d87a-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="0d87a-105">أصل الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-105">Lease asset</span></span>

<span data-ttu-id="0d87a-106">يقترن الحساب بحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="0d87a-107">يصبح هذا الحساب مدينًا عند التقييم الأولي للإيجار ضمن مقاييس المحاسبة لعقد الإيجار الجديد وموضوع صياغة مقاييس المحاسبة 842 (ASC 842) ومقياس Financial Reporting الدولي 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="0d87a-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="0d87a-108">بالنسبة لعقد الإيجار المعدل، قد يكون هذا الحساب إما مدينًا أو دائنًا، اعتمادًا إما على زيادة التعديل أو تقليل التزامات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="0d87a-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="0d87a-109">**أمثلة إدخالات دفتر اليومية:** التقييم الأولي</span><span class="sxs-lookup"><span data-stu-id="0d87a-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="0d87a-110">**المدين:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="0d87a-111">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="0d87a-112">التزامات الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-112">Lease liability</span></span>

<span data-ttu-id="0d87a-113">يقترن الحساب بالتزامات الإيجار التي تحدث عند خصم الدفعات ضمن مقاييس IFRS 16 وASC 842 الجديدة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="0d87a-114">تتم إضافة هذا الحساب عندما التقدير الأولي للإيجار ضمن المقاييس الجديدة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="0d87a-115">ويتم خصم دفعات الإيجار وإضافتها لاستحقاقات الفائدة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="0d87a-116">**أمثلة إدخالات دفتر اليومية:** التقييم الأولي</span><span class="sxs-lookup"><span data-stu-id="0d87a-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="0d87a-117">**المدين:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="0d87a-118">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="0d87a-119">**مثال على إدخالات دفتر اليومية:** استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="0d87a-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="0d87a-120">**المدين:** نفقات الفوائد XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="0d87a-121">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="0d87a-122">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="0d87a-123">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-124">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="0d87a-125">التزامات الإيجار قصير الأجل</span><span class="sxs-lookup"><span data-stu-id="0d87a-125">Short-term lease liability</span></span>

<span data-ttu-id="0d87a-126">يقترن الحساب بإيجار قصير الأجل عندما يتم ترحيل إدخال دفتر يومية إعادة تصنيف الإيجار قصير الأجل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="0d87a-127">يكون هذا الحساب دائنًا بالنسبة للالتزام قصير الأجل من جدول إطفاء الدين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="0d87a-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="0d87a-128">ومع ذلك، يتم خصم نفس المبلغ في اليوم الأول من الشهر التالي.</span><span class="sxs-lookup"><span data-stu-id="0d87a-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="0d87a-129">**مثال على إدخالات دفتر اليومية:** إعادة تصنيف التزامات الإيجار قصيرة الأجل</span><span class="sxs-lookup"><span data-stu-id="0d87a-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="0d87a-130">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-131">**ائتمان:** التزامات الإيجار قصيرة الأجل XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-132">**الائتمان:** التزامات الإيجار قصيرة الأجل XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-133">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="0d87a-134">مصروفات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="0d87a-134">Depreciation expense</span></span>

<span data-ttu-id="0d87a-135">يكون الحساب مقترنًا بالمصروفات المرتبطة بإهلاك حق استخدام الأصل ضمن مقاييس IFRS 16 والتأجير التمويلي ضمن IAS 17 وASC 840.</span><span class="sxs-lookup"><span data-stu-id="0d87a-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="0d87a-136">يكون هذا الحساب مديًنا عندما يتم إهلاك حق استخدام الأصول كل شهر.</span><span class="sxs-lookup"><span data-stu-id="0d87a-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="0d87a-137">**مثال على إدخالات دفتر اليومية:** استحقاق الإهلاك</span><span class="sxs-lookup"><span data-stu-id="0d87a-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="0d87a-138">**المدين:** ‏‏مصروفات الإهلاك XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="0d87a-139">**الائتمان:** الإهلاك التراكمي XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="0d87a-140">الربح/الخسارة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="0d87a-141">يقترن الحساب بأية مكاسب أو خسائر تنشأ من تعديلات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="0d87a-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="0d87a-142">قد يتم الحصول على الربح أثناء تعديل إذا كان التعديل يقلل من التزامات الإيجار بواسطة مبلغ يتجاوز قيمة الحمل لحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="0d87a-143">على سبيل المثال، يحتوي الإيجار على قيمة الحمل الحالية لالتزامات الإيجار بقيمة 150.000 دولار أمريكي وقيمة الحمل لحق استخدام لأصل بقيمة 100.000 دولار.</span><span class="sxs-lookup"><span data-stu-id="0d87a-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="0d87a-144">ويتم تعديل عقد الإيجار، وينتج عن هذا التعديل قيمة جديدة حالية للحد الأدنى لدفعات الإيجار المستقبلية (PVFMLP) بقيمة 40.000 دولار.</span><span class="sxs-lookup"><span data-stu-id="0d87a-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="0d87a-145">وبالتالي، سيتم خصم التزامات الإيجار بقيمة 110.000 دولار (150.000 دولار - 40.000 دولار).</span><span class="sxs-lookup"><span data-stu-id="0d87a-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="0d87a-146">ونظرًا لأن حق استخدام الأصل بقيمة 100.000 دولار فقط، فإن الانخفاض بقيمة 110.000 دولار سيؤدي إلى تقليل الأصل إلى بعد 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="0d87a-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="0d87a-147">وبالتالي، توضح إرشادات المحاسبة أنه يجب حجز الباقي إلى حساب الأرباح.</span><span class="sxs-lookup"><span data-stu-id="0d87a-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="0d87a-148">وفي هذه الحالة، سيكون إدخال دفتر اليومية النهائي مدينًا بالنسبة لالتزامات الإيجار بقيمة 110.000 دولار والائتمان لأصل عقد الإيجار بقيمة 100.000 دولار والائتمان لحساب الأرباح بقيمة 10.000.</span><span class="sxs-lookup"><span data-stu-id="0d87a-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="0d87a-149">**مثال على إدخالات دفتر اليومية:** تعديل الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="0d87a-150">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-151">**الائتمان:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="0d87a-152">**الائتمان:** الربح XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="0d87a-153">مجمع الإهلاك</span><span class="sxs-lookup"><span data-stu-id="0d87a-153">Accumulated depreciation</span></span>

<span data-ttu-id="0d87a-154">يقترن الحساب بحساب الأصل المقابل الخاص بحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="0d87a-155">يصبح هذا الحساب دائنًا عند ترحيل مصروفات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="0d87a-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="0d87a-156">**مثال على إدخالات دفتر اليومية:** استحقاق الإهلاك</span><span class="sxs-lookup"><span data-stu-id="0d87a-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="0d87a-157">**المدين:** ‏‏مصروفات الإهلاك XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="0d87a-158">**الائتمان:** الإهلاك التراكمي XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="0d87a-159">الأرباح المحتجزة</span><span class="sxs-lookup"><span data-stu-id="0d87a-159">Retained earnings</span></span>

<span data-ttu-id="0d87a-160">الحساب المرتبط بالأرباح المحتجزة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="0d87a-161">قد يكون هذا الحساب مدينًا أو دائنًا في إدخال دفتر يومية تسوية الانتقال باستخدام أسلوب الأثر الرجعي الكامل أو خيار التسوية التراكمي أ.</span><span class="sxs-lookup"><span data-stu-id="0d87a-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="0d87a-162">يتم حجز الفرق بين حق استخدام الأصل الأولي والتزامات الإيجار إلى الإيرادات المحتجزة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="0d87a-163">في الحالات النادرة، قد تتأثر كذلك الإيرادات المحتجزة أثناء تعديل عقد الإيجار، وذلك في حالة تغيير تصنيف عقد الإيجار من المالية إلى العمل لكتابة حق استخدام الأصل بحيث يساوي التزامات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="0d87a-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="0d87a-164">**مثال على إدخالات دفتر اليومية:** تسوية الانتقال (أسلوب الأثر الرجعي الكامل أو خيار التسوية التراكمي أ)</span><span class="sxs-lookup"><span data-stu-id="0d87a-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="0d87a-165">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-166">**الائتمان:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="0d87a-167">**الائتمان:** الإيرادات المحتجزة XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="0d87a-168">الدفعة المتغيرة</span><span class="sxs-lookup"><span data-stu-id="0d87a-168">Variable payment</span></span>

<span data-ttu-id="0d87a-169">يقترن الحساب بدفعات الإيجار المتغيرة التي يتم إنتاجها بواسطة إعادة تقييم المؤشر ضمن الإيجارات ASC 842 وASC 840 وIAS 17.</span><span class="sxs-lookup"><span data-stu-id="0d87a-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="0d87a-170">في جدول دفعات الإيجار، فإنه يتم تضمين الدفعات المتغيرة في العمود **الدفع المتغير**.</span><span class="sxs-lookup"><span data-stu-id="0d87a-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="0d87a-171">يكون هذا الحساب مدينًا عندما يتم إنشاء فاتورة مقابل بند جدول الدفع الذي يحتوي على دفع متغير.</span><span class="sxs-lookup"><span data-stu-id="0d87a-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="0d87a-172">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="0d87a-173">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-174">**المدين:** الدفع المتغير XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="0d87a-175">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="0d87a-176">أصل الإيجار المؤجل (التزام)</span><span class="sxs-lookup"><span data-stu-id="0d87a-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="0d87a-177">يرتبط الحساب بأصل الإيجار المؤجل أو الالتزام الذي يتم إنتاجه بواسطة إيجار معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="0d87a-178">يكون هذا الحساب مدينًا عند ترحيل فاتورة مقابل إيجار معالجة الإيجار المؤجل، وذلك إذا كان مبلغ دفعات الإيجار أكبر من مصروفات الإيجار القسط الثابت للفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="0d87a-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="0d87a-179">وتتم الإضافة إلى ذلك إذا كانت دفعات الإيجار أقل من المصروفات إيجار القسم الثابت في الفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="0d87a-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="0d87a-180">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار (إيجار معاملة الإيجار المؤجل)</span><span class="sxs-lookup"><span data-stu-id="0d87a-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="0d87a-181">**المدين:** مصروفات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="0d87a-182">**الائتمان:** التزام الإيجار المؤجل XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="0d87a-183">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="0d87a-184">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="0d87a-184">Lease expense</span></span>

<span data-ttu-id="0d87a-185">يكون الحساب مقترنًا بمصروفات الإيجار إذا تم تصنيف الإيجار على أنه عقد إيجار معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="0d87a-186">يكون هذا الحساب مدينًا عندما يتم ترحيل فاتورة مقابل إيجار معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="0d87a-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="0d87a-187">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار (إيجار معاملة الإيجار المؤجل)</span><span class="sxs-lookup"><span data-stu-id="0d87a-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="0d87a-188">**المدين:** مصروفات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="0d87a-189">**الائتمان:** التزام الإيجار المؤجل XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="0d87a-190">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="0d87a-191">مصروفات انخفاض القيمة</span><span class="sxs-lookup"><span data-stu-id="0d87a-191">Impairment expense</span></span>

<span data-ttu-id="0d87a-192">يتم ترحيل الحساب مقابل الوقت الذي يكون فيه الإيجار منخفض القيمة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="0d87a-193">عندما يكون هذا الحساب مدينًا، بينما يتم إضافة حساب حق استخدام الأصل بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="0d87a-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="0d87a-194">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="0d87a-195">**المدين:** مصروفات انخفاض القيمة XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="0d87a-196">**الائتمان:** حق استخدام الأصل XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="0d87a-197">دفعة الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-197">Lease payment</span></span>

<span data-ttu-id="0d87a-198">يتم ترحيل الحساب في مقابل ما إذا كان يتم إيقاف تشغيل المعلمة **الدفع إلى المورد**.</span><span class="sxs-lookup"><span data-stu-id="0d87a-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="0d87a-199">تتم إضافة هذا الحساب بدلاً من المورد الدائن في حالة إيقاف تشغيل المعلمة.</span><span class="sxs-lookup"><span data-stu-id="0d87a-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="0d87a-200">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="0d87a-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="0d87a-201">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="0d87a-202">**الائتمان:** دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="0d87a-203">ترحيلات نوع المصروفات</span><span class="sxs-lookup"><span data-stu-id="0d87a-203">Expense type postings</span></span>

<span data-ttu-id="0d87a-204">يتم خصم الحساب المحدد لكل نوع من أنواع المصروفات عند إنشاء عملية دفع لنوع المصروفات ذلك.</span><span class="sxs-lookup"><span data-stu-id="0d87a-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="0d87a-205">على سبيل المثال، يتم خصم الحساب المحدد الخاص بنوع مصروفات **التأمين** كلما تم إنشاء إدخال فاتورة أو دفتر يومية دفع من جدول تكلفة تنفيذ العقد لمصروفات التأمين.</span><span class="sxs-lookup"><span data-stu-id="0d87a-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="0d87a-206">**مثال على إدخالات دفتر اليومية:** دفعات التأمين</span><span class="sxs-lookup"><span data-stu-id="0d87a-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="0d87a-207">**المدين:** حساب نوع مصروفات التأمين XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="0d87a-208">**الدائن:** الحساب المقابل XXX</span><span class="sxs-lookup"><span data-stu-id="0d87a-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="0d87a-209">يتم تحديد الحساب المقابل في مستوى الإيجار في البنود الخاصة بجدول دفع تكلفة تنفيذ العقد.</span><span class="sxs-lookup"><span data-stu-id="0d87a-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="0d87a-210">يمكن أن يرتبط الحساب المقابل هذا بالمورد أو بحساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="0d87a-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
