---
title: أنواع ترحيل الإيجار
description: يصف هذا الموضوع أنواع الترحيل المستخدمة لحركات تأجير الأصول.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881122"
---
# <a name="lease-posting-types"></a><span data-ttu-id="28393-103">أنواع ترحيل الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28393-104">يصف هذا الموضوع أنواع الترحيل المستخدمة لحركات تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="28393-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="28393-105">أصل الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-105">Lease asset</span></span>

<span data-ttu-id="28393-106">يقترن الحساب بحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="28393-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="28393-107">يصبح هذا الحساب مدينًا عند التقييم الأولي للإيجار ضمن مقاييس المحاسبة لعقد الإيجار الجديد وموضوع صياغة مقاييس المحاسبة 842 (ASC 842) ومقياس Financial Reporting الدولي 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="28393-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="28393-108">بالنسبة لعقد الإيجار المعدل، قد يكون هذا الحساب إما مدينًا أو دائنًا، اعتمادًا إما على زيادة التعديل أو تقليل التزامات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="28393-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="28393-109">**أمثلة إدخالات دفتر اليومية:** التقييم الأولي</span><span class="sxs-lookup"><span data-stu-id="28393-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="28393-110">**المدين:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="28393-111">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="28393-112">التزامات الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-112">Lease liability</span></span>

<span data-ttu-id="28393-113">يقترن الحساب بالتزامات الإيجار التي تحدث عند خصم الدفعات ضمن مقاييس IFRS 16 وASC 842 الجديدة.</span><span class="sxs-lookup"><span data-stu-id="28393-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="28393-114">تتم إضافة هذا الحساب عندما التقدير الأولي للإيجار ضمن المقاييس الجديدة.</span><span class="sxs-lookup"><span data-stu-id="28393-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="28393-115">ويتم خصم دفعات الإيجار وإضافتها لاستحقاقات الفائدة.</span><span class="sxs-lookup"><span data-stu-id="28393-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="28393-116">**أمثلة إدخالات دفتر اليومية:** التقييم الأولي</span><span class="sxs-lookup"><span data-stu-id="28393-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="28393-117">**المدين:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="28393-118">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="28393-119">**مثال على إدخالات دفتر اليومية:** استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="28393-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="28393-120">**المدين:** نفقات الفوائد XXX</span><span class="sxs-lookup"><span data-stu-id="28393-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="28393-121">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="28393-122">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="28393-123">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="28393-124">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="28393-125">التزامات الإيجار قصير الأجل</span><span class="sxs-lookup"><span data-stu-id="28393-125">Short-term lease liability</span></span>

<span data-ttu-id="28393-126">يقترن الحساب بإيجار قصير الأجل عندما يتم ترحيل إدخال دفتر يومية إعادة تصنيف الإيجار قصير الأجل.</span><span class="sxs-lookup"><span data-stu-id="28393-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="28393-127">يكون هذا الحساب دائنًا بالنسبة للالتزام قصير الأجل من جدول إطفاء الدين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="28393-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="28393-128">ومع ذلك، يتم خصم نفس المبلغ في اليوم الأول من الشهر التالي.</span><span class="sxs-lookup"><span data-stu-id="28393-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="28393-129">**مثال على إدخالات دفتر اليومية:** إعادة تصنيف التزامات الإيجار قصيرة الأجل</span><span class="sxs-lookup"><span data-stu-id="28393-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="28393-130">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="28393-131">**ائتمان:** التزامات الإيجار قصيرة الأجل XXX</span><span class="sxs-lookup"><span data-stu-id="28393-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="28393-132">**الائتمان:** التزامات الإيجار قصيرة الأجل XXX</span><span class="sxs-lookup"><span data-stu-id="28393-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="28393-133">**الدائن:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="28393-134">مصروفات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="28393-134">Depreciation expense</span></span>

<span data-ttu-id="28393-135">يكون الحساب مقترنًا بالمصروفات المرتبطة بإهلاك حق استخدام الأصل ضمن مقاييس IFRS 16 والتأجير التمويلي ضمن IAS 17 وASC 840.</span><span class="sxs-lookup"><span data-stu-id="28393-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="28393-136">يكون هذا الحساب مديًنا عندما يتم إهلاك حق استخدام الأصول كل شهر.</span><span class="sxs-lookup"><span data-stu-id="28393-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="28393-137">**مثال على إدخالات دفتر اليومية:** استحقاق الإهلاك</span><span class="sxs-lookup"><span data-stu-id="28393-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="28393-138">**المدين:** ‏‏مصروفات الإهلاك XXX</span><span class="sxs-lookup"><span data-stu-id="28393-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="28393-139">**الائتمان:** الإهلاك التراكمي XXX</span><span class="sxs-lookup"><span data-stu-id="28393-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="28393-140">الربح/الخسارة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="28393-141">يقترن الحساب بأية مكاسب أو خسائر تنشأ من تعديلات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="28393-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="28393-142">قد يتم الحصول على الربح أثناء تعديل إذا كان التعديل يقلل من التزامات الإيجار بواسطة مبلغ يتجاوز قيمة الحمل لحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="28393-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="28393-143">على سبيل المثال، يحتوي الإيجار على قيمة الحمل الحالية لالتزامات الإيجار بقيمة 150.000 دولار أمريكي وقيمة الحمل لحق استخدام لأصل بقيمة 100.000 دولار.</span><span class="sxs-lookup"><span data-stu-id="28393-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="28393-144">ويتم تعديل عقد الإيجار، وينتج عن هذا التعديل قيمة جديدة حالية للحد الأدنى لدفعات الإيجار المستقبلية (PVFMLP) بقيمة 40.000 دولار.</span><span class="sxs-lookup"><span data-stu-id="28393-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="28393-145">وبالتالي، سيتم خصم التزامات الإيجار بقيمة 110.000 دولار (150.000 دولار - 40.000 دولار).</span><span class="sxs-lookup"><span data-stu-id="28393-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="28393-146">ونظرًا لأن حق استخدام الأصل بقيمة 100.000 دولار فقط، فإن الانخفاض بقيمة 110.000 دولار سيؤدي إلى تقليل الأصل إلى بعد 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="28393-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="28393-147">وبالتالي، توضح إرشادات المحاسبة أنه يجب حجز الباقي إلى حساب الأرباح.</span><span class="sxs-lookup"><span data-stu-id="28393-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="28393-148">وفي هذه الحالة، سيكون إدخال دفتر اليومية النهائي مدينًا بالنسبة لالتزامات الإيجار بقيمة 110.000 دولار والائتمان لأصل عقد الإيجار بقيمة 100.000 دولار والائتمان لحساب الأرباح بقيمة 10.000.</span><span class="sxs-lookup"><span data-stu-id="28393-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="28393-149">**مثال على إدخالات دفتر اليومية:** تعديل الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="28393-150">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="28393-151">**الائتمان:** أصول الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="28393-152">**الائتمان:** الربح XXX</span><span class="sxs-lookup"><span data-stu-id="28393-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="28393-153">مجمع الإهلاك</span><span class="sxs-lookup"><span data-stu-id="28393-153">Accumulated depreciation</span></span>

<span data-ttu-id="28393-154">يقترن الحساب بحساب الأصل المقابل الخاص بحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="28393-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="28393-155">يصبح هذا الحساب دائنًا عند ترحيل مصروفات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="28393-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="28393-156">**مثال على إدخالات دفتر اليومية:** استحقاق الإهلاك</span><span class="sxs-lookup"><span data-stu-id="28393-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="28393-157">**المدين:** ‏‏مصروفات الإهلاك XXX</span><span class="sxs-lookup"><span data-stu-id="28393-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="28393-158">**الائتمان:** الإهلاك التراكمي XXX</span><span class="sxs-lookup"><span data-stu-id="28393-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="28393-159">الدفعة المتغيرة</span><span class="sxs-lookup"><span data-stu-id="28393-159">Variable payment</span></span>

<span data-ttu-id="28393-160">يقترن الحساب بدفعات الإيجار المتغيرة التي يتم إنتاجها بواسطة إعادة تقييم المؤشر ضمن الإيجارات ASC 842 وASC 840 وIAS 17.</span><span class="sxs-lookup"><span data-stu-id="28393-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="28393-161">في جدول دفعات الإيجار، فإنه يتم تضمين الدفعات المتغيرة في العمود **الدفع المتغير**.</span><span class="sxs-lookup"><span data-stu-id="28393-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="28393-162">يكون هذا الحساب مدينًا عندما يتم إنشاء فاتورة مقابل بند جدول الدفع الذي يحتوي على دفع متغير.</span><span class="sxs-lookup"><span data-stu-id="28393-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="28393-163">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="28393-164">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="28393-165">**المدين:** الدفع المتغير XXX</span><span class="sxs-lookup"><span data-stu-id="28393-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="28393-166">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="28393-167">أصل الإيجار المؤجل (التزام)</span><span class="sxs-lookup"><span data-stu-id="28393-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="28393-168">يرتبط الحساب بأصل الإيجار المؤجل أو الالتزام الذي يتم إنتاجه بواسطة إيجار معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="28393-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="28393-169">يكون هذا الحساب مدينًا عند ترحيل فاتورة مقابل إيجار معالجة الإيجار المؤجل، وذلك إذا كان مبلغ دفعات الإيجار أكبر من مصروفات الإيجار القسط الثابت للفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="28393-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="28393-170">وتتم الإضافة إلى ذلك إذا كانت دفعات الإيجار أقل من المصروفات إيجار القسم الثابت في الفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="28393-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="28393-171">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار (إيجار معاملة الإيجار المؤجل)</span><span class="sxs-lookup"><span data-stu-id="28393-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="28393-172">**المدين:** مصروفات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="28393-173">**الائتمان:** التزام الإيجار المؤجل XXX</span><span class="sxs-lookup"><span data-stu-id="28393-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="28393-174">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="28393-175">مصروفات الإيجار‬‬</span><span class="sxs-lookup"><span data-stu-id="28393-175">Lease expense</span></span>

<span data-ttu-id="28393-176">يكون الحساب مقترنًا بمصروفات الإيجار إذا تم تصنيف الإيجار على أنه عقد إيجار معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="28393-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="28393-177">يكون هذا الحساب مدينًا عندما يتم ترحيل فاتورة مقابل إيجار معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="28393-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="28393-178">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار (إيجار معاملة الإيجار المؤجل)</span><span class="sxs-lookup"><span data-stu-id="28393-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="28393-179">**المدين:** مصروفات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="28393-180">**الائتمان:** التزام الإيجار المؤجل XXX</span><span class="sxs-lookup"><span data-stu-id="28393-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="28393-181">**الدائن:** الموردون الدائنون/دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="28393-182">مصروفات انخفاض القيمة</span><span class="sxs-lookup"><span data-stu-id="28393-182">Impairment expense</span></span>

<span data-ttu-id="28393-183">يتم ترحيل الحساب مقابل الوقت الذي يكون فيه الإيجار منخفض القيمة.</span><span class="sxs-lookup"><span data-stu-id="28393-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="28393-184">عندما يكون هذا الحساب مدينًا، بينما يتم إضافة حساب حق استخدام الأصل بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="28393-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="28393-185">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="28393-186">**المدين:** مصروفات انخفاض القيمة XXX</span><span class="sxs-lookup"><span data-stu-id="28393-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="28393-187">**الائتمان:** حق استخدام الأصل XXX</span><span class="sxs-lookup"><span data-stu-id="28393-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="28393-188">دفعة الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-188">Lease payment</span></span>

<span data-ttu-id="28393-189">يتم ترحيل الحساب في مقابل ما إذا كان يتم إيقاف تشغيل المعلمة **الدفع إلى المورد**.</span><span class="sxs-lookup"><span data-stu-id="28393-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="28393-190">تتم إضافة هذا الحساب بدلاً من المورد الدائن في حالة إيقاف تشغيل المعلمة.</span><span class="sxs-lookup"><span data-stu-id="28393-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="28393-191">**مثال على إدخالات دفتر اليومية:** دفعات الإيجار</span><span class="sxs-lookup"><span data-stu-id="28393-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="28393-192">**المدين:** التزامات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="28393-193">**الائتمان:** دفعات الإيجار XXX</span><span class="sxs-lookup"><span data-stu-id="28393-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="28393-194">ترحيلات نوع المصروفات</span><span class="sxs-lookup"><span data-stu-id="28393-194">Expense type postings</span></span>

<span data-ttu-id="28393-195">يتم خصم الحساب المحدد لكل نوع من أنواع المصروفات عند إنشاء عملية دفع لنوع المصروفات ذلك.</span><span class="sxs-lookup"><span data-stu-id="28393-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="28393-196">على سبيل المثال، يتم خصم الحساب المحدد الخاص بنوع مصروفات **التأمين** كلما تم إنشاء إدخال فاتورة أو دفتر يومية دفع من جدول تكلفة تنفيذ العقد لمصروفات التأمين.</span><span class="sxs-lookup"><span data-stu-id="28393-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="28393-197">**مثال على إدخالات دفتر اليومية:** دفعات التأمين</span><span class="sxs-lookup"><span data-stu-id="28393-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="28393-198">**المدين:** حساب نوع مصروفات التأمين XXX</span><span class="sxs-lookup"><span data-stu-id="28393-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="28393-199">**الدائن:** الحساب المقابل XXX</span><span class="sxs-lookup"><span data-stu-id="28393-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="28393-200">يتم تحديد الحساب المقابل في مستوى الإيجار في البنود الخاصة بجدول دفع تكلفة تنفيذ العقد.</span><span class="sxs-lookup"><span data-stu-id="28393-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="28393-201">يمكن أن يرتبط الحساب المقابل هذا بالمورد أو بحساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="28393-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
