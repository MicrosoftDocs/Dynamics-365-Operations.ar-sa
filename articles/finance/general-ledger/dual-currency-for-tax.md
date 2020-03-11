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
ms.openlocfilehash: c9318f518135bf7aa545cdb5ddd2e68c54a6d211
ms.sourcegitcommit: bcc8cba8905ed51797d36e1712d7360452cfc5c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/27/2020
ms.locfileid: "3090554"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="6b68b-103">دعم العملة المزدوجة لضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b68b-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6b68b-104">يوضح هذا الموضوع كيفية توسيع ميزة محاسبة العملة المزدوجة لضرائب المبيعات وأثر العمليات الحسابية لضريبة المبيعات والتسويات. </span><span class="sxs-lookup"><span data-stu-id="6b68b-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="6b68b-105">تم تقديم ميزة العملة المزدوجة لـ Dynamics 365 Finance في الإصدار 8.1 (أكتوبر 2018).</span><span class="sxs-lookup"><span data-stu-id="6b68b-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="6b68b-106">ويتم تغيير الطريقة التي يتم بها حساب إدخالات المحاسبة في عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6b68b-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="6b68b-107">في الإصدارات السابقة، تم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="6b68b-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="6b68b-108">تم حساب إجمالي الحركة بعملة الحركة > مبلغ الحركة التي تم تحويلها إلى عملة المحاسبة > يتم تحويل مبلغ عملة المحاسبة إلى عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="6b68b-109">بعد تمكين ميزة العملة المزدوجة، يتم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="6b68b-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="6b68b-110">مبلغ عملة الحركة > مبلغ عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="6b68b-111">لمزيد من المعلومات حول العملة المزدوجة، يُرجى الرجوع إلى [العملة المزدوجة](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="6b68b-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="6b68b-112">وكنتيجة لدعم العملات المزدوجة، يتوفر ميزتان جديدتان في إدارة الميزات:</span><span class="sxs-lookup"><span data-stu-id="6b68b-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="6b68b-113">تحويل ضريبة المبيعات (الإصدار في إصدار 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="6b68b-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="6b68b-114">الرصيد التلقائي لتسوية الضريبة بعملة التقارير (الإصدار في إصدار 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="6b68b-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="6b68b-115">ويضمن دعم العمل المزدوجة لضرائب المبيعات التي يتم حسابها بدقة في عملة الضريبة، وأنه يتم حساب رصيد تسوية ضريبة المبيعات بدقة في كل من عملة المحاسبة وعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6b68b-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="6b68b-116">يتم تمكين الميزات الجديدة حاليًا لعملاء المعاينة الخاصة.</span><span class="sxs-lookup"><span data-stu-id="6b68b-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="6b68b-117">لتمكين الميزات، قم برفع طلب الخدمة من خلال القنوات المطابقة إلى Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6b68b-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="6b68b-118">تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b68b-118">Sales tax conversion</span></span>

<span data-ttu-id="6b68b-119">توفر المعلمة **تحويل ضريبة المبيعات** خيارين لتحويل مبلغ الضريبة من عملة الحركة إلى عملة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="6b68b-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="6b68b-120">عملة المحاسبة: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة المحاسبة > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="6b68b-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="6b68b-121">سيتم استخدام نوع سعر الصرف لعملة المحاسبة (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="6b68b-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="6b68b-122">عملة التقارير: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة التقارير > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="6b68b-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="6b68b-123">سيتم استخدام نوع سعر الصرف لعملة التقارير (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="6b68b-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="6b68b-124">مثال</span><span class="sxs-lookup"><span data-stu-id="6b68b-124">Example</span></span>

<span data-ttu-id="6b68b-125">ومن الأمثلة البسيطة لشرح هذه الوظيفة هي:</span><span class="sxs-lookup"><span data-stu-id="6b68b-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="6b68b-126">إعداد العملة لدفتر الأستاذ والضريبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="6b68b-127">عملة الحركة</span><span class="sxs-lookup"><span data-stu-id="6b68b-127">Transaction currency</span></span> | <span data-ttu-id="6b68b-128">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-128">Accounting currency</span></span> | <span data-ttu-id="6b68b-129">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-129">Reporting currency</span></span> | <span data-ttu-id="6b68b-130">عملة الضريبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="6b68b-131">يورو</span><span class="sxs-lookup"><span data-stu-id="6b68b-131">EUR</span></span>                  | <span data-ttu-id="6b68b-132">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="6b68b-132">USD</span></span>                 | <span data-ttu-id="6b68b-133">GBP</span><span class="sxs-lookup"><span data-stu-id="6b68b-133">GBP</span></span>                | <span data-ttu-id="6b68b-134">GBP</span><span class="sxs-lookup"><span data-stu-id="6b68b-134">GBP</span></span>          |

<span data-ttu-id="6b68b-135">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="6b68b-135">Exchange rate</span></span>

| <span data-ttu-id="6b68b-136">من العملة</span><span class="sxs-lookup"><span data-stu-id="6b68b-136">From currency</span></span> | <span data-ttu-id="6b68b-137">للعملة</span><span class="sxs-lookup"><span data-stu-id="6b68b-137">To currency</span></span> | <span data-ttu-id="6b68b-138">عامل</span><span class="sxs-lookup"><span data-stu-id="6b68b-138">Factor</span></span> | <span data-ttu-id="6b68b-139">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="6b68b-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="6b68b-140">يورو</span><span class="sxs-lookup"><span data-stu-id="6b68b-140">EUR</span></span>           | <span data-ttu-id="6b68b-141">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="6b68b-141">USD</span></span>         | <span data-ttu-id="6b68b-142">1</span><span class="sxs-lookup"><span data-stu-id="6b68b-142">1</span></span>      | <span data-ttu-id="6b68b-143">1.11</span><span class="sxs-lookup"><span data-stu-id="6b68b-143">1.11</span></span>          |
| <span data-ttu-id="6b68b-144">يورو</span><span class="sxs-lookup"><span data-stu-id="6b68b-144">EUR</span></span>           | <span data-ttu-id="6b68b-145">GBP</span><span class="sxs-lookup"><span data-stu-id="6b68b-145">GBP</span></span>         | <span data-ttu-id="6b68b-146">1</span><span class="sxs-lookup"><span data-stu-id="6b68b-146">1</span></span>      | <span data-ttu-id="6b68b-147">0.83</span><span class="sxs-lookup"><span data-stu-id="6b68b-147">0.83</span></span>          |
| <span data-ttu-id="6b68b-148">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="6b68b-148">USD</span></span>           | <span data-ttu-id="6b68b-149">GBP</span><span class="sxs-lookup"><span data-stu-id="6b68b-149">GBP</span></span>         | <span data-ttu-id="6b68b-150">1</span><span class="sxs-lookup"><span data-stu-id="6b68b-150">1</span></span>      | <span data-ttu-id="6b68b-151">0.75</span><span class="sxs-lookup"><span data-stu-id="6b68b-151">0.75</span></span>          |

<span data-ttu-id="6b68b-152">حساب مبلغ الضريبة في خيارات محددة مختلفة</span><span class="sxs-lookup"><span data-stu-id="6b68b-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="6b68b-153">مبلغ الضريبة = 100 يورو</span><span class="sxs-lookup"><span data-stu-id="6b68b-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="6b68b-154">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b68b-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="6b68b-155">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="6b68b-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="6b68b-156">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="6b68b-156">Accounting currency (USD)</span></span> | <span data-ttu-id="6b68b-157">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="6b68b-158">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="6b68b-159">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-159">Accounting currency</span></span>             | <span data-ttu-id="6b68b-160">100</span><span class="sxs-lookup"><span data-stu-id="6b68b-160">100</span></span>                        | <span data-ttu-id="6b68b-161">111</span><span class="sxs-lookup"><span data-stu-id="6b68b-161">111</span></span>                       | <span data-ttu-id="6b68b-162">83</span><span class="sxs-lookup"><span data-stu-id="6b68b-162">83</span></span>                       | <span data-ttu-id="6b68b-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="6b68b-163">**83.25**</span></span>          |
| <span data-ttu-id="6b68b-164">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-164">Reporting currency</span></span>              | <span data-ttu-id="6b68b-165">100</span><span class="sxs-lookup"><span data-stu-id="6b68b-165">100</span></span>                        | <span data-ttu-id="6b68b-166">111</span><span class="sxs-lookup"><span data-stu-id="6b68b-166">111</span></span>                       | <span data-ttu-id="6b68b-167">83</span><span class="sxs-lookup"><span data-stu-id="6b68b-167">83</span></span>                       | <span data-ttu-id="6b68b-168">**83**</span><span class="sxs-lookup"><span data-stu-id="6b68b-168">**83**</span></span>             |

<span data-ttu-id="6b68b-169">يمكن تكوين هذه المعلمة استنادًا إلى الحاجة إلى التوافق من هيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="6b68b-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="6b68b-170">اعتبار الترقية</span><span class="sxs-lookup"><span data-stu-id="6b68b-170">Upgrade Consideration</span></span>

<span data-ttu-id="6b68b-171">سيتم تطبيق هذه الميزة على الحركات الجديدة فقط.</span><span class="sxs-lookup"><span data-stu-id="6b68b-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="6b68b-172">بالفعل لحركة الضريبة المحفوظة في جدول TAXTRANS ولكن لم تتم تسويتها بعد، لن يقوم النظام بإعادة حساب مبلغ الضريبة بعملة الضريبة نظرًا لأن سعر الصرف في النقطة الزمنية لضريبة الترحيل مفقود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="6b68b-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="6b68b-173">لمنع السيناريو السابق، نوصي بتغيير قيمة هذه المعلمة في فترة تسوية ضرائب جديدة (نظيفة) لا تحتوي علي أية حركات ضريبة لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="6b68b-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="6b68b-174">لتغيير هذه القيمة في منتصف فترة تسوية ضريبة، يُرجى تشغيل برنامج "تسوية ضريبة المبيعات وترحيها" لفترة تسوية الضرائب الحالية قبل تغيير قيمة المعلمة هذه.</span><span class="sxs-lookup"><span data-stu-id="6b68b-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="6b68b-175">تتبع مبلغ ضريبة عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="6b68b-176">تمت إضافة ثلاثة حقول جديدة إلى الجداول المرتبطة بالضريبة لتتبع المبالغ بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6b68b-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="6b68b-177">وتكون هذه الحقول داخل الجدولين TAXUNCOMMITTED وTAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="6b68b-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="6b68b-178">TaxAmountRep: مبلغ الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="6b68b-179">TaxBaseAmountRep: المبلغ الأساسي بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="6b68b-180">TaxInCostPriceRep: المبلغ غير الخاضع للخصم بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="6b68b-181">بالنسبة للضريبة المحفوظة في جدول TAXUNCOMMITTED ولكن لم يتم ترحيلها بعد، سيقوم النظام بإعادة حساب مبلغ الضريبة بعملة التقارير في وقت الترحيل والحفظ في جدول TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="6b68b-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="6b68b-182">لن يتضمن هذا الإصدار تغييرات في التقارير والنماذج التي تعرض مبلغ الضريبة بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6b68b-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="6b68b-183">سيتم تسليم التغييرات التي تم إجراؤها على التقارير والنماذج في الإصدار المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="6b68b-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="6b68b-184">الرصيد التلقائي لتسوية الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="6b68b-185">في حالة عدم موازنة التسوية الضريبية بعملة التقارير لسبب معين، مثل مسار تحويل ضريبة المبيعات "بعملة المحاسبة" أو تغيير سعر الصرف في فترة تسوية ضريبة واحدة، ثم سيقوم النظام تلقائيًا بإنشاء الإدخالات المحاسبية لتعديل نسبة فرق المبلغ الضريبي ومقارنتها بحساب مكسب/خسارة السعر المحقق، وتم تكوينها في إعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="6b68b-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="6b68b-186">باستخدام المثال السابق لشرح هذه الميزة، افترض أن البيانات الموجودة في الجدول TAXTRANS في وقت الترحيل كما يلي.</span><span class="sxs-lookup"><span data-stu-id="6b68b-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="6b68b-187">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b68b-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="6b68b-188">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="6b68b-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="6b68b-189">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="6b68b-189">Accounting currency (USD)</span></span> | <span data-ttu-id="6b68b-190">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="6b68b-191">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="6b68b-192">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-192">Accounting currency</span></span>             | <span data-ttu-id="6b68b-193">100</span><span class="sxs-lookup"><span data-stu-id="6b68b-193">100</span></span>                        | <span data-ttu-id="6b68b-194">111</span><span class="sxs-lookup"><span data-stu-id="6b68b-194">111</span></span>                       | <span data-ttu-id="6b68b-195">83</span><span class="sxs-lookup"><span data-stu-id="6b68b-195">83</span></span>                       | <span data-ttu-id="6b68b-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="6b68b-196">**83.25**</span></span>          |
| <span data-ttu-id="6b68b-197">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="6b68b-197">Reporting currency</span></span>              | <span data-ttu-id="6b68b-198">100</span><span class="sxs-lookup"><span data-stu-id="6b68b-198">100</span></span>                        | <span data-ttu-id="6b68b-199">111</span><span class="sxs-lookup"><span data-stu-id="6b68b-199">111</span></span>                       | <span data-ttu-id="6b68b-200">83</span><span class="sxs-lookup"><span data-stu-id="6b68b-200">83</span></span>                       | <span data-ttu-id="6b68b-201">**83**</span><span class="sxs-lookup"><span data-stu-id="6b68b-201">**83**</span></span>             |

<span data-ttu-id="6b68b-202">عند تشغيل برنامج تسوية ضريبة المبيعات في نهاية الشهر، سيكون إدخال المحاسبة كما يلي:.</span><span class="sxs-lookup"><span data-stu-id="6b68b-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="6b68b-203">السيناريو: تحويل ضريبة المبيعات = "عملة المحاسبة"</span><span class="sxs-lookup"><span data-stu-id="6b68b-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="6b68b-204">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="6b68b-204">Main account</span></span>           | <span data-ttu-id="6b68b-205">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="6b68b-206">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="6b68b-206">Accounting currency (USD)</span></span> | <span data-ttu-id="6b68b-207">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="6b68b-208">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="6b68b-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="6b68b-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="6b68b-209">-83.25</span></span>                     | <span data-ttu-id="6b68b-210">-111</span><span class="sxs-lookup"><span data-stu-id="6b68b-210">-111</span></span>                      | <span data-ttu-id="6b68b-211">-83.25</span><span class="sxs-lookup"><span data-stu-id="6b68b-211">-83.25</span></span>                   |
| <span data-ttu-id="6b68b-212">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-212">Tax Settlement</span></span>         | <span data-ttu-id="6b68b-213">83.25</span><span class="sxs-lookup"><span data-stu-id="6b68b-213">83.25</span></span>                      | <span data-ttu-id="6b68b-214">111</span><span class="sxs-lookup"><span data-stu-id="6b68b-214">111</span></span>                       | <span data-ttu-id="6b68b-215">83.25</span><span class="sxs-lookup"><span data-stu-id="6b68b-215">83.25</span></span>                    |
| <span data-ttu-id="6b68b-216">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="6b68b-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="6b68b-217">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-217">0</span></span>                          | <span data-ttu-id="6b68b-218">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-218">0</span></span>                         | <span data-ttu-id="6b68b-219">-0.25</span><span class="sxs-lookup"><span data-stu-id="6b68b-219">-0.25</span></span>                    |
| <span data-ttu-id="6b68b-220">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="6b68b-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="6b68b-221">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-221">0</span></span>                          | <span data-ttu-id="6b68b-222">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-222">0</span></span>                         | <span data-ttu-id="6b68b-223">0.25</span><span class="sxs-lookup"><span data-stu-id="6b68b-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="6b68b-224">السيناريو: تحويل ضريبة المبيعات = "عملة التقارير"</span><span class="sxs-lookup"><span data-stu-id="6b68b-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="6b68b-225">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="6b68b-225">Main account</span></span>           | <span data-ttu-id="6b68b-226">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="6b68b-227">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="6b68b-227">Accounting currency (USD)</span></span> | <span data-ttu-id="6b68b-228">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="6b68b-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="6b68b-229">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="6b68b-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="6b68b-230">-83</span><span class="sxs-lookup"><span data-stu-id="6b68b-230">-83</span></span>                        | <span data-ttu-id="6b68b-231">-110.67</span><span class="sxs-lookup"><span data-stu-id="6b68b-231">-110.67</span></span>                   | <span data-ttu-id="6b68b-232">-83</span><span class="sxs-lookup"><span data-stu-id="6b68b-232">-83</span></span>                      |
| <span data-ttu-id="6b68b-233">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="6b68b-233">Tax Settlement</span></span>         | <span data-ttu-id="6b68b-234">83</span><span class="sxs-lookup"><span data-stu-id="6b68b-234">83</span></span>                         | <span data-ttu-id="6b68b-235">110.67</span><span class="sxs-lookup"><span data-stu-id="6b68b-235">110.67</span></span>                    | <span data-ttu-id="6b68b-236">83</span><span class="sxs-lookup"><span data-stu-id="6b68b-236">83</span></span>                       |
| <span data-ttu-id="6b68b-237">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="6b68b-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="6b68b-238">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-238">0</span></span>                          | <span data-ttu-id="6b68b-239">0.33</span><span class="sxs-lookup"><span data-stu-id="6b68b-239">0.33</span></span>                      | <span data-ttu-id="6b68b-240">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-240">0</span></span>                        |
| <span data-ttu-id="6b68b-241">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="6b68b-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="6b68b-242">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-242">0</span></span>                          | <span data-ttu-id="6b68b-243">-0.33</span><span class="sxs-lookup"><span data-stu-id="6b68b-243">-0.33</span></span>                     | <span data-ttu-id="6b68b-244">0</span><span class="sxs-lookup"><span data-stu-id="6b68b-244">0</span></span>                        |



<span data-ttu-id="6b68b-245">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="6b68b-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6b68b-246">العملة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="6b68b-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="6b68b-247">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b68b-247">Sales tax overview</span></span>](indirect-taxes-overview.md)
