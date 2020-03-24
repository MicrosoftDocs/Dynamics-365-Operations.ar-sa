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
ms.openlocfilehash: 1ba4d09240888f0c533fb07614e75ffecea0742c
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124083"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="8cb4c-103">دعم العملة المزدوجة لضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="8cb4c-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cb4c-104">يوضح هذا الموضوع كيفية توسيع ميزة محاسبة العملة المزدوجة لضرائب المبيعات وأثر العمليات الحسابية لضريبة المبيعات والتسويات. </span><span class="sxs-lookup"><span data-stu-id="8cb4c-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="8cb4c-105">تم تقديم ميزة العملة المزدوجة لـ Dynamics 365 Finance في الإصدار 8.1 (أكتوبر 2018).</span><span class="sxs-lookup"><span data-stu-id="8cb4c-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="8cb4c-106">ويتم تغيير الطريقة التي يتم بها حساب إدخالات المحاسبة في عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="8cb4c-107">في الإصدارات السابقة، تم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="8cb4c-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="8cb4c-108">تم حساب إجمالي الحركة بعملة الحركة > مبلغ الحركة التي تم تحويلها إلى عملة المحاسبة > يتم تحويل مبلغ عملة المحاسبة إلى عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="8cb4c-109">بعد تمكين ميزة العملة المزدوجة، يتم تحويل الحركات إلى عملة التقارير بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="8cb4c-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="8cb4c-110">مبلغ عملة الحركة > مبلغ عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="8cb4c-111">لمزيد من المعلومات حول العملة المزدوجة، يُرجى الرجوع إلى [العملة المزدوجة](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="8cb4c-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="8cb4c-112">وكنتيجة لدعم العملات المزدوجة، يتوفر ميزتان جديدتان في إدارة الميزات:</span><span class="sxs-lookup"><span data-stu-id="8cb4c-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="8cb4c-113">تحويل ضريبة المبيعات (الإصدار في إصدار 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="8cb4c-114">الرصيد التلقائي لتسوية الضريبة بعملة التقارير (الإصدار في إصدار 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="8cb4c-115">ويضمن دعم العمل المزدوجة لضرائب المبيعات التي يتم حسابها بدقة في عملة الضريبة، وأنه يتم حساب رصيد تسوية ضريبة المبيعات بدقة في كل من عملة المحاسبة وعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="8cb4c-116">يتم تمكين الميزات الجديدة حاليًا لعملاء المعاينة الخاصة.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="8cb4c-117">لتمكين الميزات، قم برفع طلب الخدمة من خلال القنوات المطابقة إلى Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="8cb4c-118">تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="8cb4c-118">Sales tax conversion</span></span>

<span data-ttu-id="8cb4c-119">توفر المعلمة **تحويل ضريبة المبيعات** خيارين لتحويل مبلغ الضريبة من عملة الحركة إلى عملة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="8cb4c-120">عملة المحاسبة: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة المحاسبة > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="8cb4c-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="8cb4c-121">سيتم استخدام نوع سعر الصرف لعملة المحاسبة (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="8cb4c-122">عملة التقارير: سيكون المسار "المبلغ بعملة الحركة > المبلغ بعملة التقارير > المبلغ بعملة الضريبة".</span><span class="sxs-lookup"><span data-stu-id="8cb4c-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="8cb4c-123">سيتم استخدام نوع سعر الصرف لعملة التقارير (المكون في إعداد دفتر الأستاذ) لتحويل العملة.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="8cb4c-124">مثال</span><span class="sxs-lookup"><span data-stu-id="8cb4c-124">Example</span></span>

<span data-ttu-id="8cb4c-125">ومن الأمثلة البسيطة لشرح هذه الوظيفة هي:</span><span class="sxs-lookup"><span data-stu-id="8cb4c-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="8cb4c-126">إعداد العملة لدفتر الأستاذ والضريبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="8cb4c-127">عملة الحركة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-127">Transaction currency</span></span> | <span data-ttu-id="8cb4c-128">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-128">Accounting currency</span></span> | <span data-ttu-id="8cb4c-129">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-129">Reporting currency</span></span> | <span data-ttu-id="8cb4c-130">عملة الضريبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="8cb4c-131">يورو</span><span class="sxs-lookup"><span data-stu-id="8cb4c-131">EUR</span></span>                  | <span data-ttu-id="8cb4c-132">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="8cb4c-132">USD</span></span>                 | <span data-ttu-id="8cb4c-133">GBP</span><span class="sxs-lookup"><span data-stu-id="8cb4c-133">GBP</span></span>                | <span data-ttu-id="8cb4c-134">GBP</span><span class="sxs-lookup"><span data-stu-id="8cb4c-134">GBP</span></span>          |

<span data-ttu-id="8cb4c-135">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="8cb4c-135">Exchange rate</span></span>

| <span data-ttu-id="8cb4c-136">من العملة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-136">From currency</span></span> | <span data-ttu-id="8cb4c-137">للعملة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-137">To currency</span></span> | <span data-ttu-id="8cb4c-138">عامل</span><span class="sxs-lookup"><span data-stu-id="8cb4c-138">Factor</span></span> | <span data-ttu-id="8cb4c-139">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="8cb4c-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="8cb4c-140">يورو</span><span class="sxs-lookup"><span data-stu-id="8cb4c-140">EUR</span></span>           | <span data-ttu-id="8cb4c-141">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="8cb4c-141">USD</span></span>         | <span data-ttu-id="8cb4c-142">1</span><span class="sxs-lookup"><span data-stu-id="8cb4c-142">1</span></span>      | <span data-ttu-id="8cb4c-143">1.11</span><span class="sxs-lookup"><span data-stu-id="8cb4c-143">1.11</span></span>          |
| <span data-ttu-id="8cb4c-144">يورو</span><span class="sxs-lookup"><span data-stu-id="8cb4c-144">EUR</span></span>           | <span data-ttu-id="8cb4c-145">GBP</span><span class="sxs-lookup"><span data-stu-id="8cb4c-145">GBP</span></span>         | <span data-ttu-id="8cb4c-146">1</span><span class="sxs-lookup"><span data-stu-id="8cb4c-146">1</span></span>      | <span data-ttu-id="8cb4c-147">0.83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-147">0.83</span></span>          |
| <span data-ttu-id="8cb4c-148">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="8cb4c-148">USD</span></span>           | <span data-ttu-id="8cb4c-149">GBP</span><span class="sxs-lookup"><span data-stu-id="8cb4c-149">GBP</span></span>         | <span data-ttu-id="8cb4c-150">1</span><span class="sxs-lookup"><span data-stu-id="8cb4c-150">1</span></span>      | <span data-ttu-id="8cb4c-151">0.75</span><span class="sxs-lookup"><span data-stu-id="8cb4c-151">0.75</span></span>          |

<span data-ttu-id="8cb4c-152">حساب مبلغ الضريبة في خيارات محددة مختلفة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="8cb4c-153">مبلغ الضريبة = 100 يورو</span><span class="sxs-lookup"><span data-stu-id="8cb4c-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="8cb4c-154">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="8cb4c-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="8cb4c-155">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="8cb4c-156">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-156">Accounting currency (USD)</span></span> | <span data-ttu-id="8cb4c-157">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="8cb4c-158">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="8cb4c-159">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-159">Accounting currency</span></span>             | <span data-ttu-id="8cb4c-160">100</span><span class="sxs-lookup"><span data-stu-id="8cb4c-160">100</span></span>                        | <span data-ttu-id="8cb4c-161">111</span><span class="sxs-lookup"><span data-stu-id="8cb4c-161">111</span></span>                       | <span data-ttu-id="8cb4c-162">83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-162">83</span></span>                       | <span data-ttu-id="8cb4c-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="8cb4c-163">**83.25**</span></span>          |
| <span data-ttu-id="8cb4c-164">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-164">Reporting currency</span></span>              | <span data-ttu-id="8cb4c-165">100</span><span class="sxs-lookup"><span data-stu-id="8cb4c-165">100</span></span>                        | <span data-ttu-id="8cb4c-166">111</span><span class="sxs-lookup"><span data-stu-id="8cb4c-166">111</span></span>                       | <span data-ttu-id="8cb4c-167">83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-167">83</span></span>                       | <span data-ttu-id="8cb4c-168">**83**</span><span class="sxs-lookup"><span data-stu-id="8cb4c-168">**83**</span></span>             |

<span data-ttu-id="8cb4c-169">يمكن تكوين هذه المعلمة استنادًا إلى الحاجة إلى التوافق من هيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="8cb4c-170">اعتبار الترقية</span><span class="sxs-lookup"><span data-stu-id="8cb4c-170">Upgrade Consideration</span></span>

<span data-ttu-id="8cb4c-171">سيتم تطبيق هذه الميزة على الحركات الجديدة فقط.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="8cb4c-172">بالفعل لحركة الضريبة المحفوظة في جدول TAXTRANS ولكن لم تتم تسويتها بعد، لن يقوم النظام بإعادة حساب مبلغ الضريبة بعملة الضريبة نظرًا لأن سعر الصرف في النقطة الزمنية لضريبة الترحيل مفقود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="8cb4c-173">لمنع السيناريو السابق، نوصي بتغيير قيمة هذه المعلمة في فترة تسوية ضرائب جديدة (نظيفة) لا تحتوي على أية حركات ضريبة لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="8cb4c-174">لتغيير هذه القيمة في منتصف فترة تسوية ضريبة، يُرجى تشغيل برنامج "تسوية ضريبة المبيعات وترحيها" لفترة تسوية الضرائب الحالية قبل تغيير قيمة المعلمة هذه.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="8cb4c-175">تتبع مبلغ ضريبة عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="8cb4c-176">تمت إضافة ثلاثة حقول جديدة إلى الجداول المرتبطة بالضريبة لتتبع المبالغ بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="8cb4c-177">وتكون هذه الحقول داخل الجدولين TAXUNCOMMITTED وTAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="8cb4c-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="8cb4c-178">TaxAmountRep: مبلغ الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="8cb4c-179">TaxBaseAmountRep: المبلغ الأساسي بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="8cb4c-180">TaxInCostPriceRep: المبلغ غير الخاضع للخصم بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="8cb4c-181">بالنسبة للضريبة المحفوظة في جدول TAXUNCOMMITTED ولكن لم يتم ترحيلها بعد، سيقوم النظام بإعادة حساب مبلغ الضريبة بعملة التقارير في وقت الترحيل والحفظ في جدول TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="8cb4c-182">لن يتضمن هذا الإصدار تغييرات في التقارير والنماذج التي تعرض مبلغ الضريبة بعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="8cb4c-183">سيتم تسليم التغييرات التي تم إجراؤها على التقارير والنماذج في الإصدار المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="8cb4c-184">الرصيد التلقائي لتسوية الضريبة بعملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="8cb4c-185">في حالة عدم موازنة التسوية الضريبية بعملة التقارير لسبب معين، مثل مسار تحويل ضريبة المبيعات "بعملة المحاسبة" أو تغيير سعر الصرف في فترة تسوية ضريبة واحدة، ثم سيقوم النظام تلقائيًا بإنشاء الإدخالات المحاسبية لتعديل نسبة فرق المبلغ الضريبي ومقارنتها بحساب مكسب/خسارة السعر المحقق، وتم تكوينها في إعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="8cb4c-186">باستخدام المثال السابق لشرح هذه الميزة، افترض أن البيانات الموجودة في الجدول TAXTRANS في وقت الترحيل كما يلي.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="8cb4c-187">معلمات تحويل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="8cb4c-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="8cb4c-188">عملة الحركة (يورو)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="8cb4c-189">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-189">Accounting currency (USD)</span></span> | <span data-ttu-id="8cb4c-190">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="8cb4c-191">عملة الضريبة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="8cb4c-192">عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-192">Accounting currency</span></span>             | <span data-ttu-id="8cb4c-193">100</span><span class="sxs-lookup"><span data-stu-id="8cb4c-193">100</span></span>                        | <span data-ttu-id="8cb4c-194">111</span><span class="sxs-lookup"><span data-stu-id="8cb4c-194">111</span></span>                       | <span data-ttu-id="8cb4c-195">83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-195">83</span></span>                       | <span data-ttu-id="8cb4c-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="8cb4c-196">**83.25**</span></span>          |
| <span data-ttu-id="8cb4c-197">عملة التقارير</span><span class="sxs-lookup"><span data-stu-id="8cb4c-197">Reporting currency</span></span>              | <span data-ttu-id="8cb4c-198">100</span><span class="sxs-lookup"><span data-stu-id="8cb4c-198">100</span></span>                        | <span data-ttu-id="8cb4c-199">111</span><span class="sxs-lookup"><span data-stu-id="8cb4c-199">111</span></span>                       | <span data-ttu-id="8cb4c-200">83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-200">83</span></span>                       | <span data-ttu-id="8cb4c-201">**83**</span><span class="sxs-lookup"><span data-stu-id="8cb4c-201">**83**</span></span>             |

<span data-ttu-id="8cb4c-202">عند تشغيل برنامج تسوية ضريبة المبيعات في نهاية الشهر، سيكون إدخال المحاسبة كما يلي:.</span><span class="sxs-lookup"><span data-stu-id="8cb4c-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="8cb4c-203">السيناريو: تحويل ضريبة المبيعات = "عملة المحاسبة"</span><span class="sxs-lookup"><span data-stu-id="8cb4c-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="8cb4c-204">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="8cb4c-204">Main account</span></span>           | <span data-ttu-id="8cb4c-205">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="8cb4c-206">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-206">Accounting currency (USD)</span></span> | <span data-ttu-id="8cb4c-207">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="8cb4c-208">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="8cb4c-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="8cb4c-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="8cb4c-209">-83.25</span></span>                     | <span data-ttu-id="8cb4c-210">-111</span><span class="sxs-lookup"><span data-stu-id="8cb4c-210">-111</span></span>                      | <span data-ttu-id="8cb4c-211">-83.25</span><span class="sxs-lookup"><span data-stu-id="8cb4c-211">-83.25</span></span>                   |
| <span data-ttu-id="8cb4c-212">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-212">Tax Settlement</span></span>         | <span data-ttu-id="8cb4c-213">83.25</span><span class="sxs-lookup"><span data-stu-id="8cb4c-213">83.25</span></span>                      | <span data-ttu-id="8cb4c-214">111</span><span class="sxs-lookup"><span data-stu-id="8cb4c-214">111</span></span>                       | <span data-ttu-id="8cb4c-215">83.25</span><span class="sxs-lookup"><span data-stu-id="8cb4c-215">83.25</span></span>                    |
| <span data-ttu-id="8cb4c-216">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="8cb4c-217">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-217">0</span></span>                          | <span data-ttu-id="8cb4c-218">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-218">0</span></span>                         | <span data-ttu-id="8cb4c-219">-0.25</span><span class="sxs-lookup"><span data-stu-id="8cb4c-219">-0.25</span></span>                    |
| <span data-ttu-id="8cb4c-220">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="8cb4c-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="8cb4c-221">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-221">0</span></span>                          | <span data-ttu-id="8cb4c-222">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-222">0</span></span>                         | <span data-ttu-id="8cb4c-223">0.25</span><span class="sxs-lookup"><span data-stu-id="8cb4c-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="8cb4c-224">السيناريو: تحويل ضريبة المبيعات = "عملة التقارير"</span><span class="sxs-lookup"><span data-stu-id="8cb4c-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="8cb4c-225">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="8cb4c-225">Main account</span></span>           | <span data-ttu-id="8cb4c-226">عملة الحركة (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="8cb4c-227">عملة المحاسبة (دولار أمريكي)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-227">Accounting currency (USD)</span></span> | <span data-ttu-id="8cb4c-228">عملة التقارير (جنيه إسترليني)</span><span class="sxs-lookup"><span data-stu-id="8cb4c-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="8cb4c-229">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="8cb4c-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="8cb4c-230">-83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-230">-83</span></span>                        | <span data-ttu-id="8cb4c-231">-110.67</span><span class="sxs-lookup"><span data-stu-id="8cb4c-231">-110.67</span></span>                   | <span data-ttu-id="8cb4c-232">-83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-232">-83</span></span>                      |
| <span data-ttu-id="8cb4c-233">تسوية الضريبة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-233">Tax Settlement</span></span>         | <span data-ttu-id="8cb4c-234">83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-234">83</span></span>                         | <span data-ttu-id="8cb4c-235">110.67</span><span class="sxs-lookup"><span data-stu-id="8cb4c-235">110.67</span></span>                    | <span data-ttu-id="8cb4c-236">83</span><span class="sxs-lookup"><span data-stu-id="8cb4c-236">83</span></span>                       |
| <span data-ttu-id="8cb4c-237">الأرباح/الخسائر المحققة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="8cb4c-238">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-238">0</span></span>                          | <span data-ttu-id="8cb4c-239">0.33</span><span class="sxs-lookup"><span data-stu-id="8cb4c-239">0.33</span></span>                      | <span data-ttu-id="8cb4c-240">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-240">0</span></span>                        |
| <span data-ttu-id="8cb4c-241">الضريبة مستحقة الدفع/مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="8cb4c-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="8cb4c-242">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-242">0</span></span>                          | <span data-ttu-id="8cb4c-243">-0.33</span><span class="sxs-lookup"><span data-stu-id="8cb4c-243">-0.33</span></span>                     | <span data-ttu-id="8cb4c-244">0</span><span class="sxs-lookup"><span data-stu-id="8cb4c-244">0</span></span>                        |



<span data-ttu-id="8cb4c-245">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="8cb4c-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="8cb4c-246">العملة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="8cb4c-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="8cb4c-247">نظرة عامة على ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="8cb4c-247">Sales tax overview</span></span>](indirect-taxes-overview.md)

