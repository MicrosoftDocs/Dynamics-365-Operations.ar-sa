---
title: دعم العملة المزدوجة للضريبة
description: يوضح هذا الموضوع كيفية توسيع ميزة محاسبة العملة المزدوجة في مجال الضرائب وأثر حساب الضريبة والترحيل
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3f7ca56fef636431e152b2db424f1f972a507721
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212195"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="617e5-103">دعم العملة المزدوجة لضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="617e5-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="617e5-104">يوضح هذا الموضوع كيفية توسيع ميزة محاسبة العملة المزدوجة لضرائب المبيعات وأثر العمليات الحسابية لضريبة المبيعات والتسويات. </span><span class="sxs-lookup"><span data-stu-id="617e5-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="617e5-105">تم تقديم ميزة العملة المزدوجة لـ Dynamics 365 Finance في الإصدار 8.1 (أكتوبر 2018).</span><span class="sxs-lookup"><span data-stu-id="617e5-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="617e5-106">ويتم تغيير الطريقة التي يتم بها حساب إدخالات المحاسبة في عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="617e5-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="617e5-107">في الإصدارات السابقة، تم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="617e5-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="617e5-108">تم حساب إجمالي الحركة بعملة الحركة > مبلغ الحركة التي تم تحويلها إلى عملة المحاسبة > يتم تحويل مبلغ عملة المحاسبة إلى عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="617e5-109">بعد تمكين ميزة العملة المزدوجة، يتم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="617e5-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="617e5-110">مبلغ عملة الحركة > مبلغ عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="617e5-111">لمزيد من المعلومات حول العملة المزدوجة، يُرجى الرجوع إلى [العملة المزدوجة](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="617e5-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="617e5-112">وكنتيجة لدعم العملات المزدوجة، يتوفر ميزتان جديدتان في إدارة الميزات:</span><span class="sxs-lookup"><span data-stu-id="617e5-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="617e5-113">تحويل ضريبة المبيعات (الجديد في إصدار 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="617e5-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="617e5-114">ويضمن دعم العمل المزدوجة لضرائب المبيعات التي يتم حسابها بدقة في عملة الضريبة، وأنه يتم حساب رصيد تسوية ضريبة المبيعات بدقة في كل من عملة المحاسبة وعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="617e5-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="617e5-115">تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="617e5-115">Sales tax conversion</span></span>

<span data-ttu-id="617e5-116">توفر المعلمة **تحويل ضريبة المبيعات** خيارين لتحويل مبلغ الضريبة من عملة الحركة إلى عملة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="617e5-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="617e5-117">عملة المحاسبة: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة المحاسبة > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="617e5-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="617e5-118">سيتم استخدام نوع سعر الصرف لعملة المحاسبة (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="617e5-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="617e5-119">عملة التقارير: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة التقارير > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="617e5-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="617e5-120">سيتم استخدام نوع سعر الصرف لعملة التقارير (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="617e5-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="617e5-121">مثال</span><span class="sxs-lookup"><span data-stu-id="617e5-121">Example</span></span>

<span data-ttu-id="617e5-122">ومن الأمثلة البسيطة لشرح هذه الوظيفة هي:</span><span class="sxs-lookup"><span data-stu-id="617e5-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="617e5-123">إعداد العملة لدفتر الأستاذ والضريبة</span><span class="sxs-lookup"><span data-stu-id="617e5-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="617e5-124">عملة الحركة</span><span class="sxs-lookup"><span data-stu-id="617e5-124">Transaction currency</span></span> | <span data-ttu-id="617e5-125">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="617e5-125">Accounting currency</span></span> | <span data-ttu-id="617e5-126">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-126">Reporting currency</span></span> | <span data-ttu-id="617e5-127">عملة الضريبة</span><span class="sxs-lookup"><span data-stu-id="617e5-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="617e5-128">يورو</span><span class="sxs-lookup"><span data-stu-id="617e5-128">EUR</span></span>                  | <span data-ttu-id="617e5-129">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="617e5-129">USD</span></span>                 | <span data-ttu-id="617e5-130">GBP</span><span class="sxs-lookup"><span data-stu-id="617e5-130">GBP</span></span>                | <span data-ttu-id="617e5-131">GBP</span><span class="sxs-lookup"><span data-stu-id="617e5-131">GBP</span></span>          |

<span data-ttu-id="617e5-132">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="617e5-132">Exchange rate</span></span>

| <span data-ttu-id="617e5-133">من العملة</span><span class="sxs-lookup"><span data-stu-id="617e5-133">From currency</span></span> | <span data-ttu-id="617e5-134">للعملة</span><span class="sxs-lookup"><span data-stu-id="617e5-134">To currency</span></span> | <span data-ttu-id="617e5-135">عامل</span><span class="sxs-lookup"><span data-stu-id="617e5-135">Factor</span></span> | <span data-ttu-id="617e5-136">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="617e5-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="617e5-137">يورو</span><span class="sxs-lookup"><span data-stu-id="617e5-137">EUR</span></span>           | <span data-ttu-id="617e5-138">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="617e5-138">USD</span></span>         | <span data-ttu-id="617e5-139">1</span><span class="sxs-lookup"><span data-stu-id="617e5-139">1</span></span>      | <span data-ttu-id="617e5-140">1.11</span><span class="sxs-lookup"><span data-stu-id="617e5-140">1.11</span></span>          |
| <span data-ttu-id="617e5-141">يورو</span><span class="sxs-lookup"><span data-stu-id="617e5-141">EUR</span></span>           | <span data-ttu-id="617e5-142">GBP</span><span class="sxs-lookup"><span data-stu-id="617e5-142">GBP</span></span>         | <span data-ttu-id="617e5-143">1</span><span class="sxs-lookup"><span data-stu-id="617e5-143">1</span></span>      | <span data-ttu-id="617e5-144">0.83</span><span class="sxs-lookup"><span data-stu-id="617e5-144">0.83</span></span>          |
| <span data-ttu-id="617e5-145">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="617e5-145">USD</span></span>           | <span data-ttu-id="617e5-146">GBP</span><span class="sxs-lookup"><span data-stu-id="617e5-146">GBP</span></span>         | <span data-ttu-id="617e5-147">1</span><span class="sxs-lookup"><span data-stu-id="617e5-147">1</span></span>      | <span data-ttu-id="617e5-148">0.75</span><span class="sxs-lookup"><span data-stu-id="617e5-148">0.75</span></span>          |

<span data-ttu-id="617e5-149">حساب مبلغ الضريبة في خيارات محددة مختلفة</span><span class="sxs-lookup"><span data-stu-id="617e5-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="617e5-150">مبلغ الضريبة = 100 يورو</span><span class="sxs-lookup"><span data-stu-id="617e5-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="617e5-151">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="617e5-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="617e5-152">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="617e5-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="617e5-153">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="617e5-153">Accounting currency (USD)</span></span> | <span data-ttu-id="617e5-154">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="617e5-155">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="617e5-156">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="617e5-156">Accounting currency</span></span>             | <span data-ttu-id="617e5-157">100</span><span class="sxs-lookup"><span data-stu-id="617e5-157">100</span></span>                        | <span data-ttu-id="617e5-158">111</span><span class="sxs-lookup"><span data-stu-id="617e5-158">111</span></span>                       | <span data-ttu-id="617e5-159">83</span><span class="sxs-lookup"><span data-stu-id="617e5-159">83</span></span>                       | <span data-ttu-id="617e5-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="617e5-160">**83.25**</span></span>          |
| <span data-ttu-id="617e5-161">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-161">Reporting currency</span></span>              | <span data-ttu-id="617e5-162">100</span><span class="sxs-lookup"><span data-stu-id="617e5-162">100</span></span>                        | <span data-ttu-id="617e5-163">111</span><span class="sxs-lookup"><span data-stu-id="617e5-163">111</span></span>                       | <span data-ttu-id="617e5-164">83</span><span class="sxs-lookup"><span data-stu-id="617e5-164">83</span></span>                       | <span data-ttu-id="617e5-165">**83**</span><span class="sxs-lookup"><span data-stu-id="617e5-165">**83**</span></span>             |

<span data-ttu-id="617e5-166">يمكن تكوين هذه المعلمة استنادًا إلى الحاجة إلى التوافق من هيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="617e5-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="617e5-167">اعتبار الترقية</span><span class="sxs-lookup"><span data-stu-id="617e5-167">Upgrade Consideration</span></span>

<span data-ttu-id="617e5-168">سيتم تطبيق هذه الميزة على الحركات الجديدة فقط.</span><span class="sxs-lookup"><span data-stu-id="617e5-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="617e5-169">بالفعل لحركة الضريبة المحفوظة في جدول TAXTRANS ولكن لم تتم تسويتها بعد، لن يقوم النظام بإعادة حساب مبلغ الضريبة بعملة الضريبة نظرًا لأن سعر الصرف في النقطة الزمنية لضريبة الترحيل مفقود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="617e5-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="617e5-170">لمنع السيناريو السابق، نوصي بتغيير قيمة هذه المعلمة في فترة تسوية ضرائب جديدة (نظيفة) لا تحتوي على أية حركات ضريبة لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="617e5-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="617e5-171">لتغيير هذه القيمة في منتصف فترة تسوية ضريبة، يُرجى تشغيل برنامج "تسوية ضريبة المبيعات وترحيها" لفترة تسوية الضرائب الحالية قبل تغيير قيمة المعلمة هذه.</span><span class="sxs-lookup"><span data-stu-id="617e5-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="617e5-172">تتبع مبلغ ضريبة عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="617e5-173">تمت إضافة ثلاثة حقول جديدة إلى الجداول المرتبطة بالضريبة لتتبع المبالغ بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="617e5-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="617e5-174">وتكون هذه الحقول داخل الجدولين TAXUNCOMMITTED وTAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="617e5-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="617e5-175">TaxAmountRep: مبلغ الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="617e5-176">TaxBaseAmountRep: المبلغ الأساسي بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="617e5-177">TaxInCostPriceRep: المبلغ غير الخاضع للخصم بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="617e5-178">بالنسبة للضريبة المحفوظة في جدول TAXUNCOMMITTED ولكن لم يتم ترحيلها بعد، سيقوم النظام بإعادة حساب مبلغ الضريبة بعملة التقارير في وقت الترحيل والحفظ في جدول TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="617e5-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="617e5-179">لن يتضمن هذا الإصدار تغييرات في التقارير والنماذج التي تعرض مبلغ الضريبة بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="617e5-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="617e5-180">سيتم تسليم التغييرات التي تم إجراؤها على التقارير والنماذج في الإصدار المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="617e5-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="617e5-181">الرصيد التلقائي لتسوية الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="617e5-182">في حالة عدم موازنة التسوية الضريبية بعملة التقارير لسبب معين، مثل مسار تحويل ضريبة المبيعات "بعملة المحاسبة" أو تغيير سعر الصرف في فترة تسوية ضريبة واحدة، ثم سيقوم النظام تلقائيًا بإنشاء الإدخالات المحاسبية لتعديل نسبة فرق المبلغ الضريبي ومقارنتها بحساب مكسب/خسارة السعر المحقق، وتم تكوينها في إعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="617e5-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="617e5-183">باستخدام المثال السابق لشرح هذه الميزة، افترض أن البيانات الموجودة في الجدول TAXTRANS في وقت الترحيل كما يلي.</span><span class="sxs-lookup"><span data-stu-id="617e5-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="617e5-184">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="617e5-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="617e5-185">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="617e5-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="617e5-186">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="617e5-186">Accounting currency (USD)</span></span> | <span data-ttu-id="617e5-187">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="617e5-188">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="617e5-189">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="617e5-189">Accounting currency</span></span>             | <span data-ttu-id="617e5-190">100</span><span class="sxs-lookup"><span data-stu-id="617e5-190">100</span></span>                        | <span data-ttu-id="617e5-191">111</span><span class="sxs-lookup"><span data-stu-id="617e5-191">111</span></span>                       | <span data-ttu-id="617e5-192">83</span><span class="sxs-lookup"><span data-stu-id="617e5-192">83</span></span>                       | <span data-ttu-id="617e5-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="617e5-193">**83.25**</span></span>          |
| <span data-ttu-id="617e5-194">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="617e5-194">Reporting currency</span></span>              | <span data-ttu-id="617e5-195">100</span><span class="sxs-lookup"><span data-stu-id="617e5-195">100</span></span>                        | <span data-ttu-id="617e5-196">111</span><span class="sxs-lookup"><span data-stu-id="617e5-196">111</span></span>                       | <span data-ttu-id="617e5-197">83</span><span class="sxs-lookup"><span data-stu-id="617e5-197">83</span></span>                       | <span data-ttu-id="617e5-198">**83**</span><span class="sxs-lookup"><span data-stu-id="617e5-198">**83**</span></span>             |

<span data-ttu-id="617e5-199">عند تشغيل برنامج تسوية ضريبة المبيعات في نهاية الشهر، سيكون إدخال المحاسبة كما يلي:.</span><span class="sxs-lookup"><span data-stu-id="617e5-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="617e5-200">السيناريو: تحويل ضريبة المبيعات = "عملة المحاسبة"</span><span class="sxs-lookup"><span data-stu-id="617e5-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="617e5-201">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="617e5-201">Main account</span></span>           | <span data-ttu-id="617e5-202">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="617e5-203">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="617e5-203">Accounting currency (USD)</span></span> | <span data-ttu-id="617e5-204">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="617e5-205">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="617e5-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="617e5-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="617e5-206">-83.25</span></span>                     | <span data-ttu-id="617e5-207">-111</span><span class="sxs-lookup"><span data-stu-id="617e5-207">-111</span></span>                      | <span data-ttu-id="617e5-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="617e5-208">-83.25</span></span>                   |
| <span data-ttu-id="617e5-209">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="617e5-209">Tax Settlement</span></span>         | <span data-ttu-id="617e5-210">83.25</span><span class="sxs-lookup"><span data-stu-id="617e5-210">83.25</span></span>                      | <span data-ttu-id="617e5-211">111</span><span class="sxs-lookup"><span data-stu-id="617e5-211">111</span></span>                       | <span data-ttu-id="617e5-212">83.25</span><span class="sxs-lookup"><span data-stu-id="617e5-212">83.25</span></span>                    |
| <span data-ttu-id="617e5-213">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="617e5-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="617e5-214">0</span><span class="sxs-lookup"><span data-stu-id="617e5-214">0</span></span>                          | <span data-ttu-id="617e5-215">0</span><span class="sxs-lookup"><span data-stu-id="617e5-215">0</span></span>                         | <span data-ttu-id="617e5-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="617e5-216">-0.25</span></span>                    |
| <span data-ttu-id="617e5-217">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="617e5-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="617e5-218">0</span><span class="sxs-lookup"><span data-stu-id="617e5-218">0</span></span>                          | <span data-ttu-id="617e5-219">0</span><span class="sxs-lookup"><span data-stu-id="617e5-219">0</span></span>                         | <span data-ttu-id="617e5-220">0.25</span><span class="sxs-lookup"><span data-stu-id="617e5-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="617e5-221">السيناريو: تحويل ضريبة المبيعات = "عملة التقارير"</span><span class="sxs-lookup"><span data-stu-id="617e5-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="617e5-222">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="617e5-222">Main account</span></span>           | <span data-ttu-id="617e5-223">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="617e5-224">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="617e5-224">Accounting currency (USD)</span></span> | <span data-ttu-id="617e5-225">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="617e5-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="617e5-226">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="617e5-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="617e5-227">-83</span><span class="sxs-lookup"><span data-stu-id="617e5-227">-83</span></span>                        | <span data-ttu-id="617e5-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="617e5-228">-110.67</span></span>                   | <span data-ttu-id="617e5-229">-83</span><span class="sxs-lookup"><span data-stu-id="617e5-229">-83</span></span>                      |
| <span data-ttu-id="617e5-230">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="617e5-230">Tax Settlement</span></span>         | <span data-ttu-id="617e5-231">83</span><span class="sxs-lookup"><span data-stu-id="617e5-231">83</span></span>                         | <span data-ttu-id="617e5-232">110.67</span><span class="sxs-lookup"><span data-stu-id="617e5-232">110.67</span></span>                    | <span data-ttu-id="617e5-233">83</span><span class="sxs-lookup"><span data-stu-id="617e5-233">83</span></span>                       |
| <span data-ttu-id="617e5-234">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="617e5-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="617e5-235">0</span><span class="sxs-lookup"><span data-stu-id="617e5-235">0</span></span>                          | <span data-ttu-id="617e5-236">0.33</span><span class="sxs-lookup"><span data-stu-id="617e5-236">0.33</span></span>                      | <span data-ttu-id="617e5-237">0</span><span class="sxs-lookup"><span data-stu-id="617e5-237">0</span></span>                        |
| <span data-ttu-id="617e5-238">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="617e5-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="617e5-239">0</span><span class="sxs-lookup"><span data-stu-id="617e5-239">0</span></span>                          | <span data-ttu-id="617e5-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="617e5-240">-0.33</span></span>                     | <span data-ttu-id="617e5-241">0</span><span class="sxs-lookup"><span data-stu-id="617e5-241">0</span></span>                        |



<span data-ttu-id="617e5-242">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="617e5-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="617e5-243">العملة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="617e5-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="617e5-244">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="617e5-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]