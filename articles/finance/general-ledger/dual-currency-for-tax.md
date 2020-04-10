---
title: دعم العملة المزدوجة للضريبة
description: يوضح هذا الموضوع كيفية توسيع ميزة محاسبة العملة المزدوجة في مجال الضرائب وأثر حساب الضريبة والترحيل
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 863403dc3b2444f00f0cac27a494fc49d3d70de7
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161582"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="eb6c1-103">دعم العملة المزدوجة لضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="eb6c1-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb6c1-104">يوضح هذا الموضوع كيفية توسيع ميزة محاسبة العملة المزدوجة لضرائب المبيعات وأثر العمليات الحسابية لضريبة المبيعات والتسويات. </span><span class="sxs-lookup"><span data-stu-id="eb6c1-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="eb6c1-105">تم تقديم ميزة العملة المزدوجة لـ Dynamics 365 Finance في الإصدار 8.1 (أكتوبر 2018).</span><span class="sxs-lookup"><span data-stu-id="eb6c1-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="eb6c1-106">ويتم تغيير الطريقة التي يتم بها حساب إدخالات المحاسبة في عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="eb6c1-107">في الإصدارات السابقة، تم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="eb6c1-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="eb6c1-108">تم حساب إجمالي الحركة بعملة الحركة > مبلغ الحركة التي تم تحويلها إلى عملة المحاسبة > يتم تحويل مبلغ عملة المحاسبة إلى عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="eb6c1-109">بعد تمكين ميزة العملة المزدوجة، يتم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="eb6c1-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="eb6c1-110">مبلغ عملة الحركة > مبلغ عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="eb6c1-111">لمزيد من المعلومات حول العملة المزدوجة، يُرجى الرجوع إلى [العملة المزدوجة](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="eb6c1-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="eb6c1-112">وكنتيجة لدعم العملات المزدوجة، يتوفر ميزتان جديدتان في إدارة الميزات:</span><span class="sxs-lookup"><span data-stu-id="eb6c1-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="eb6c1-113">تحويل ضريبة المبيعات (الإصدار في إصدار 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="eb6c1-114">الرصيد التلقائي لتسوية الضريبة بعملة التقارير (الإصدار في إصدار 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="eb6c1-115">ويضمن دعم العمل المزدوجة لضرائب المبيعات التي يتم حسابها بدقة في عملة الضريبة، وأنه يتم حساب رصيد تسوية ضريبة المبيعات بدقة في كل من عملة المحاسبة وعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="eb6c1-116">تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="eb6c1-116">Sales tax conversion</span></span>

<span data-ttu-id="eb6c1-117">توفر المعلمة **تحويل ضريبة المبيعات** خيارين لتحويل مبلغ الضريبة من عملة الحركة إلى عملة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="eb6c1-118">عملة المحاسبة: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة المحاسبة > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="eb6c1-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="eb6c1-119">سيتم استخدام نوع سعر الصرف لعملة المحاسبة (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="eb6c1-120">عملة التقارير: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة التقارير > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="eb6c1-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="eb6c1-121">سيتم استخدام نوع سعر الصرف لعملة التقارير (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="eb6c1-122">مثال</span><span class="sxs-lookup"><span data-stu-id="eb6c1-122">Example</span></span>

<span data-ttu-id="eb6c1-123">ومن الأمثلة البسيطة لشرح هذه الوظيفة هي:</span><span class="sxs-lookup"><span data-stu-id="eb6c1-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="eb6c1-124">إعداد العملة لدفتر الأستاذ والضريبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="eb6c1-125">عملة الحركة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-125">Transaction currency</span></span> | <span data-ttu-id="eb6c1-126">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-126">Accounting currency</span></span> | <span data-ttu-id="eb6c1-127">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-127">Reporting currency</span></span> | <span data-ttu-id="eb6c1-128">عملة الضريبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="eb6c1-129">يورو</span><span class="sxs-lookup"><span data-stu-id="eb6c1-129">EUR</span></span>                  | <span data-ttu-id="eb6c1-130">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="eb6c1-130">USD</span></span>                 | <span data-ttu-id="eb6c1-131">GBP</span><span class="sxs-lookup"><span data-stu-id="eb6c1-131">GBP</span></span>                | <span data-ttu-id="eb6c1-132">GBP</span><span class="sxs-lookup"><span data-stu-id="eb6c1-132">GBP</span></span>          |

<span data-ttu-id="eb6c1-133">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="eb6c1-133">Exchange rate</span></span>

| <span data-ttu-id="eb6c1-134">من العملة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-134">From currency</span></span> | <span data-ttu-id="eb6c1-135">للعملة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-135">To currency</span></span> | <span data-ttu-id="eb6c1-136">عامل</span><span class="sxs-lookup"><span data-stu-id="eb6c1-136">Factor</span></span> | <span data-ttu-id="eb6c1-137">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="eb6c1-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="eb6c1-138">يورو</span><span class="sxs-lookup"><span data-stu-id="eb6c1-138">EUR</span></span>           | <span data-ttu-id="eb6c1-139">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="eb6c1-139">USD</span></span>         | <span data-ttu-id="eb6c1-140">1</span><span class="sxs-lookup"><span data-stu-id="eb6c1-140">1</span></span>      | <span data-ttu-id="eb6c1-141">1.11</span><span class="sxs-lookup"><span data-stu-id="eb6c1-141">1.11</span></span>          |
| <span data-ttu-id="eb6c1-142">يورو</span><span class="sxs-lookup"><span data-stu-id="eb6c1-142">EUR</span></span>           | <span data-ttu-id="eb6c1-143">GBP</span><span class="sxs-lookup"><span data-stu-id="eb6c1-143">GBP</span></span>         | <span data-ttu-id="eb6c1-144">1</span><span class="sxs-lookup"><span data-stu-id="eb6c1-144">1</span></span>      | <span data-ttu-id="eb6c1-145">0.83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-145">0.83</span></span>          |
| <span data-ttu-id="eb6c1-146">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="eb6c1-146">USD</span></span>           | <span data-ttu-id="eb6c1-147">GBP</span><span class="sxs-lookup"><span data-stu-id="eb6c1-147">GBP</span></span>         | <span data-ttu-id="eb6c1-148">1</span><span class="sxs-lookup"><span data-stu-id="eb6c1-148">1</span></span>      | <span data-ttu-id="eb6c1-149">0.75</span><span class="sxs-lookup"><span data-stu-id="eb6c1-149">0.75</span></span>          |

<span data-ttu-id="eb6c1-150">حساب مبلغ الضريبة في خيارات محددة مختلفة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="eb6c1-151">مبلغ الضريبة = 100 يورو</span><span class="sxs-lookup"><span data-stu-id="eb6c1-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="eb6c1-152">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="eb6c1-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="eb6c1-153">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="eb6c1-154">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-154">Accounting currency (USD)</span></span> | <span data-ttu-id="eb6c1-155">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="eb6c1-156">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="eb6c1-157">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-157">Accounting currency</span></span>             | <span data-ttu-id="eb6c1-158">100</span><span class="sxs-lookup"><span data-stu-id="eb6c1-158">100</span></span>                        | <span data-ttu-id="eb6c1-159">111</span><span class="sxs-lookup"><span data-stu-id="eb6c1-159">111</span></span>                       | <span data-ttu-id="eb6c1-160">83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-160">83</span></span>                       | <span data-ttu-id="eb6c1-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="eb6c1-161">**83.25**</span></span>          |
| <span data-ttu-id="eb6c1-162">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-162">Reporting currency</span></span>              | <span data-ttu-id="eb6c1-163">100</span><span class="sxs-lookup"><span data-stu-id="eb6c1-163">100</span></span>                        | <span data-ttu-id="eb6c1-164">111</span><span class="sxs-lookup"><span data-stu-id="eb6c1-164">111</span></span>                       | <span data-ttu-id="eb6c1-165">83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-165">83</span></span>                       | <span data-ttu-id="eb6c1-166">**83**</span><span class="sxs-lookup"><span data-stu-id="eb6c1-166">**83**</span></span>             |

<span data-ttu-id="eb6c1-167">يمكن تكوين هذه المعلمة استنادًا إلى الحاجة إلى التوافق من هيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="eb6c1-168">اعتبار الترقية</span><span class="sxs-lookup"><span data-stu-id="eb6c1-168">Upgrade Consideration</span></span>

<span data-ttu-id="eb6c1-169">سيتم تطبيق هذه الميزة على الحركات الجديدة فقط.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="eb6c1-170">بالفعل لحركة الضريبة المحفوظة في جدول TAXTRANS ولكن لم تتم تسويتها بعد، لن يقوم النظام بإعادة حساب مبلغ الضريبة بعملة الضريبة نظرًا لأن سعر الصرف في النقطة الزمنية لضريبة الترحيل مفقود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="eb6c1-171">لمنع السيناريو السابق، نوصي بتغيير قيمة هذه المعلمة في فترة تسوية ضرائب جديدة (نظيفة) لا تحتوي على أية حركات ضريبة لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="eb6c1-172">لتغيير هذه القيمة في منتصف فترة تسوية ضريبة، يُرجى تشغيل برنامج "تسوية ضريبة المبيعات وترحيها" لفترة تسوية الضرائب الحالية قبل تغيير قيمة المعلمة هذه.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="eb6c1-173">تتبع مبلغ ضريبة عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="eb6c1-174">تمت إضافة ثلاثة حقول جديدة إلى الجداول المرتبطة بالضريبة لتتبع المبالغ بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="eb6c1-175">وتكون هذه الحقول داخل الجدولين TAXUNCOMMITTED وTAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="eb6c1-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="eb6c1-176">TaxAmountRep: مبلغ الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="eb6c1-177">TaxBaseAmountRep: المبلغ الأساسي بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="eb6c1-178">TaxInCostPriceRep: المبلغ غير الخاضع للخصم بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="eb6c1-179">بالنسبة للضريبة المحفوظة في جدول TAXUNCOMMITTED ولكن لم يتم ترحيلها بعد، سيقوم النظام بإعادة حساب مبلغ الضريبة بعملة التقارير في وقت الترحيل والحفظ في جدول TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="eb6c1-180">لن يتضمن هذا الإصدار تغييرات في التقارير والنماذج التي تعرض مبلغ الضريبة بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="eb6c1-181">سيتم تسليم التغييرات التي تم إجراؤها على التقارير والنماذج في الإصدار المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="eb6c1-182">الرصيد التلقائي لتسوية الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="eb6c1-183">في حالة عدم موازنة التسوية الضريبية بعملة التقارير لسبب معين، مثل مسار تحويل ضريبة المبيعات "بعملة المحاسبة" أو تغيير سعر الصرف في فترة تسوية ضريبة واحدة، ثم سيقوم النظام تلقائيًا بإنشاء الإدخالات المحاسبية لتعديل نسبة فرق المبلغ الضريبي ومقارنتها بحساب مكسب/خسارة السعر المحقق، وتم تكوينها في إعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="eb6c1-184">باستخدام المثال السابق لشرح هذه الميزة، افترض أن البيانات الموجودة في الجدول TAXTRANS في وقت الترحيل كما يلي.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="eb6c1-185">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="eb6c1-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="eb6c1-186">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="eb6c1-187">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-187">Accounting currency (USD)</span></span> | <span data-ttu-id="eb6c1-188">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="eb6c1-189">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="eb6c1-190">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-190">Accounting currency</span></span>             | <span data-ttu-id="eb6c1-191">100</span><span class="sxs-lookup"><span data-stu-id="eb6c1-191">100</span></span>                        | <span data-ttu-id="eb6c1-192">111</span><span class="sxs-lookup"><span data-stu-id="eb6c1-192">111</span></span>                       | <span data-ttu-id="eb6c1-193">83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-193">83</span></span>                       | <span data-ttu-id="eb6c1-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="eb6c1-194">**83.25**</span></span>          |
| <span data-ttu-id="eb6c1-195">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="eb6c1-195">Reporting currency</span></span>              | <span data-ttu-id="eb6c1-196">100</span><span class="sxs-lookup"><span data-stu-id="eb6c1-196">100</span></span>                        | <span data-ttu-id="eb6c1-197">111</span><span class="sxs-lookup"><span data-stu-id="eb6c1-197">111</span></span>                       | <span data-ttu-id="eb6c1-198">83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-198">83</span></span>                       | <span data-ttu-id="eb6c1-199">**83**</span><span class="sxs-lookup"><span data-stu-id="eb6c1-199">**83**</span></span>             |

<span data-ttu-id="eb6c1-200">عند تشغيل برنامج تسوية ضريبة المبيعات في نهاية الشهر، سيكون إدخال المحاسبة كما يلي:.</span><span class="sxs-lookup"><span data-stu-id="eb6c1-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="eb6c1-201">السيناريو: تحويل ضريبة المبيعات = "عملة المحاسبة"</span><span class="sxs-lookup"><span data-stu-id="eb6c1-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="eb6c1-202">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="eb6c1-202">Main account</span></span>           | <span data-ttu-id="eb6c1-203">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="eb6c1-204">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-204">Accounting currency (USD)</span></span> | <span data-ttu-id="eb6c1-205">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="eb6c1-206">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="eb6c1-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="eb6c1-207">-83.25</span><span class="sxs-lookup"><span data-stu-id="eb6c1-207">-83.25</span></span>                     | <span data-ttu-id="eb6c1-208">-111</span><span class="sxs-lookup"><span data-stu-id="eb6c1-208">-111</span></span>                      | <span data-ttu-id="eb6c1-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="eb6c1-209">-83.25</span></span>                   |
| <span data-ttu-id="eb6c1-210">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-210">Tax Settlement</span></span>         | <span data-ttu-id="eb6c1-211">83.25</span><span class="sxs-lookup"><span data-stu-id="eb6c1-211">83.25</span></span>                      | <span data-ttu-id="eb6c1-212">111</span><span class="sxs-lookup"><span data-stu-id="eb6c1-212">111</span></span>                       | <span data-ttu-id="eb6c1-213">83.25</span><span class="sxs-lookup"><span data-stu-id="eb6c1-213">83.25</span></span>                    |
| <span data-ttu-id="eb6c1-214">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="eb6c1-215">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-215">0</span></span>                          | <span data-ttu-id="eb6c1-216">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-216">0</span></span>                         | <span data-ttu-id="eb6c1-217">-0.25</span><span class="sxs-lookup"><span data-stu-id="eb6c1-217">-0.25</span></span>                    |
| <span data-ttu-id="eb6c1-218">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="eb6c1-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="eb6c1-219">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-219">0</span></span>                          | <span data-ttu-id="eb6c1-220">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-220">0</span></span>                         | <span data-ttu-id="eb6c1-221">0.25</span><span class="sxs-lookup"><span data-stu-id="eb6c1-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="eb6c1-222">السيناريو: تحويل ضريبة المبيعات = "عملة التقارير"</span><span class="sxs-lookup"><span data-stu-id="eb6c1-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="eb6c1-223">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="eb6c1-223">Main account</span></span>           | <span data-ttu-id="eb6c1-224">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="eb6c1-225">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-225">Accounting currency (USD)</span></span> | <span data-ttu-id="eb6c1-226">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="eb6c1-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="eb6c1-227">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="eb6c1-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="eb6c1-228">-83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-228">-83</span></span>                        | <span data-ttu-id="eb6c1-229">-110.67</span><span class="sxs-lookup"><span data-stu-id="eb6c1-229">-110.67</span></span>                   | <span data-ttu-id="eb6c1-230">-83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-230">-83</span></span>                      |
| <span data-ttu-id="eb6c1-231">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-231">Tax Settlement</span></span>         | <span data-ttu-id="eb6c1-232">83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-232">83</span></span>                         | <span data-ttu-id="eb6c1-233">110.67</span><span class="sxs-lookup"><span data-stu-id="eb6c1-233">110.67</span></span>                    | <span data-ttu-id="eb6c1-234">83</span><span class="sxs-lookup"><span data-stu-id="eb6c1-234">83</span></span>                       |
| <span data-ttu-id="eb6c1-235">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="eb6c1-236">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-236">0</span></span>                          | <span data-ttu-id="eb6c1-237">0.33</span><span class="sxs-lookup"><span data-stu-id="eb6c1-237">0.33</span></span>                      | <span data-ttu-id="eb6c1-238">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-238">0</span></span>                        |
| <span data-ttu-id="eb6c1-239">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="eb6c1-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="eb6c1-240">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-240">0</span></span>                          | <span data-ttu-id="eb6c1-241">-0.33</span><span class="sxs-lookup"><span data-stu-id="eb6c1-241">-0.33</span></span>                     | <span data-ttu-id="eb6c1-242">0</span><span class="sxs-lookup"><span data-stu-id="eb6c1-242">0</span></span>                        |



<span data-ttu-id="eb6c1-243">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="eb6c1-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="eb6c1-244">العملة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="eb6c1-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="eb6c1-245">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="eb6c1-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

