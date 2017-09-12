---
title: "طرق حساب ضريبة المبيعات في حقل الأصل"
description: "توضح هذه المقالة الخيارات في حقل الأصل في صفحة أكواد ضريبة المبيعات وكيف يتم حساب ضريبة المبيعات استنادًا إلى الخيار المحدد لكود ضريبة المبيعات."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: f5683b8b3e5457a05e5039876eed40357ae84e4b
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="ac06e-103">طرق حساب ضريبة المبيعات في حقل الأصل</span><span class="sxs-lookup"><span data-stu-id="ac06e-103">Sales tax calculation methods in the Origin field</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="ac06e-104">توضح هذه المقالة الخيارات في حقل الأصل في صفحة أكواد ضريبة المبيعات وكيف يتم حساب ضريبة المبيعات استنادًا إلى الخيار المحدد لكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="ac06e-105">بالنسبة لكل كود ضريبة مبيعات تقوم بإنشائه في صفحة أكواد ضريبة المبيعات، يجب تحديد طريقة الحساب لتطبيقها على مبلغ الوعاء الضريبي في حقل الأصل.</span><span class="sxs-lookup"><span data-stu-id="ac06e-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="ac06e-106">النسبة المئوية للمبلغ الصافي</span><span class="sxs-lookup"><span data-stu-id="ac06e-106">Percentage of net amount</span></span>
<span data-ttu-id="ac06e-107">النسبة المئوية لطريقة حساب المبلغ الصافي هي القيمة الافتراضية في حقل الأصل.</span><span class="sxs-lookup"><span data-stu-id="ac06e-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="ac06e-108">يتم حساب ضريبة المبيعات كنسبة مئوية لمبلغ الشراء أو المبيعات، مع استبعاد أية ضرائب مبيعات أخرى.</span><span class="sxs-lookup"><span data-stu-id="ac06e-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="ac06e-109">مثال</span><span class="sxs-lookup"><span data-stu-id="ac06e-109">Example</span></span>

<span data-ttu-id="ac06e-110">معدل الضريبة 25%.</span><span class="sxs-lookup"><span data-stu-id="ac06e-110">The tax rate is 25%.</span></span> <span data-ttu-id="ac06e-111">ويوضح بند الفاتورة كمية مكونة من 10 أصناف بسعر 1.00 دولار لكل صنف، ويسمح بخصم بند قدره 10% للعميل.</span><span class="sxs-lookup"><span data-stu-id="ac06e-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="ac06e-112">المبلغ الصافي: (10 × 1.00) - 10% = 9.00 ضريبة المبيعات: 9.00 × 25% = 2.25 المبلغ الإجمالي: 9.00 + 2.25 = 11.25</span><span class="sxs-lookup"><span data-stu-id="ac06e-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="ac06e-113"> النسبة المئوية لإجمالي المبلغ</span><span class="sxs-lookup"><span data-stu-id="ac06e-113">Percentage of gross amount</span></span>
<span data-ttu-id="ac06e-114">إذا قمت بتحديد النسبة المئوية لطريقة القيمة الإجمالية، فإنه يتم حساب ضريبة المبيعات كنسبة مئوية لإجمالي مبلغ المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="ac06e-115">والمبلغ الإجمالي هو صافي مبلغ البند بالإضافة إلى كافة الضرائب والرسوم للبند ما عدا ضريبة واحدة بالأصل = النسبة المئوية للمبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="ac06e-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="ac06e-116">مثال</span><span class="sxs-lookup"><span data-stu-id="ac06e-116">Example</span></span>

<span data-ttu-id="ac06e-117">فرضت هيئة الضرائب رسوم جمركية خاصة على أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="ac06e-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="ac06e-118">تتم إضافة مبالغ الرسم الجمركي إلى المبلغ الصافي قبل حساب ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="ac06e-119">فيما يلي أكواد ضريبة المبيعات:</span><span class="sxs-lookup"><span data-stu-id="ac06e-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="ac06e-120">الرسم الجمركي 1 = 10%، باستخدام النسبة المئوية لطريقة حساب المبلغ الصافي</span><span class="sxs-lookup"><span data-stu-id="ac06e-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="ac06e-121">الرسم الجمركي 2 = 20%، باستخدام النسبة المئوية لطريقة حساب المبلغ الصافي</span><span class="sxs-lookup"><span data-stu-id="ac06e-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="ac06e-122">ضريبة المبيعات = 25%، باستخدام النسبة المئوية لطريقة حساب المبلغ الإجمالي</span><span class="sxs-lookup"><span data-stu-id="ac06e-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="ac06e-123">إذا كان المبلغ الصافي يساوي 10.00، فعندئذٍ الرسم الجمركي 1 يساوي 1.00 (10.00 x‏ 10%) والرسم الجمركي 2 = 2.00 (10.00 x‏ 20%).</span><span class="sxs-lookup"><span data-stu-id="ac06e-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="ac06e-124">المبالغ ستكون كما يلي: المبلغ الإجمالي: صافي المبلغ + مبلغ الرسم الجمركي 1 + مبلغ الرسم الجمركي 2 (10.00 + 1.00 + 2.00) = 13.00 ضريبة المبيعات = 13.00 × 25% = 3.25 إجمالي الرسوم الجمركية وضريبة المبيعات: 1.00 + 2.00 + 3.25 = 6.25 المبلغ الإجمالي: 10.00 + 6.25 = 16.25</span><span class="sxs-lookup"><span data-stu-id="ac06e-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>
| <span data-ttu-id="ac06e-125">**ملاحظة**</span><span class="sxs-lookup"><span data-stu-id="ac06e-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac06e-126">كود ضريبة واحدة فقط بالأصل = يمكن استخدام النسبة المئوية لإجمالي المبلغ لحركة.</span><span class="sxs-lookup"><span data-stu-id="ac06e-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="ac06e-127">وإذا تم تحديد أكثر من كود ضريبة واحدة لحركة، فسيتم عرض خطأ يفيد بأنه لا يمكن حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |

 
<a name="percentage-of-sales-tax"></a><span data-ttu-id="ac06e-128">النسبة المئوية لضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="ac06e-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="ac06e-129">عند تحديد النسبة المئوية لضريبة المبيعات في حقل الأصل، فإنه يتم حساب ضريبة المبيعات كنسبة مئوية لضريبة المبيعات التي تم تحديدها في ضريبة المبيعات في حقل ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="ac06e-130">ويتم حساب ضريبة المبيعات التي تم تحديدها في ضريبة المبيعات في حقل ضريبة المبيعات أولاً.</span><span class="sxs-lookup"><span data-stu-id="ac06e-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="ac06e-131">ثم يتم حساب ضريبة المبيعات الثانية بعد ذلك بناءً على مبلغ ضريبة المبيعات الأولى.</span><span class="sxs-lookup"><span data-stu-id="ac06e-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="ac06e-132">مثال</span><span class="sxs-lookup"><span data-stu-id="ac06e-132">Example</span></span>

<span data-ttu-id="ac06e-133">فيما يلي أكواد ضريبة المبيعات:</span><span class="sxs-lookup"><span data-stu-id="ac06e-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="ac06e-134">الرسم الجمركي 1 = 10%، النسبة المئوية لطريقة حساب المبلغ الصافي</span><span class="sxs-lookup"><span data-stu-id="ac06e-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="ac06e-135">الرسم الجمركي 2 = 20%، باستخدام النسبة المئوية لطريقة حساب ضريبة المبيعات، مع وجود الرسم الجمركي 1 في ضريبة المبيعات في حقل ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="ac06e-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="ac06e-136">ضريبة المبيعات = 25%، باستخدام النسبة المئوية لطريقة حساب المبلغ الإجمالي</span><span class="sxs-lookup"><span data-stu-id="ac06e-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="ac06e-137">المبلغ الصافي: الرسم الجمركي 1 بمبلغ 10.00: 10.00 x‏ 10% = الرسم الجمركي 2: 1.00 × 20% = 0.20 القيمة الإجمالية: 10.00 + 1.00 + 0.20 = 11.20 ضريبة المبيعات: 11.20 x‏ 25% = 2.80 الرسوم الإجمالية وضريبة المبيعات: 1.00 + 0.20 + 2.80 = 4.00 المبلغ الإجمالي: 10.00 + 4.00 = 14.00</span><span class="sxs-lookup"><span data-stu-id="ac06e-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>
| <span data-ttu-id="ac06e-138">**ملاحظة**</span><span class="sxs-lookup"><span data-stu-id="ac06e-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac06e-139">ضريبة متعددة المستويات في عمليات حساب الضرائب غير ممكنة.</span><span class="sxs-lookup"><span data-stu-id="ac06e-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="ac06e-140">زلا يمكن حساب ضريبة استناداً إلى ضريبة يتم حسابها بالفعل استناداً إلى ضريبة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ac06e-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="ac06e-141">ويمكن حساب ضريبة بمستوى واحدة في أكواد الضريبة في حركة.</span><span class="sxs-lookup"><span data-stu-id="ac06e-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="ac06e-142"> المبلغ لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="ac06e-142">Amount per unit</span></span>
<span data-ttu-id="ac06e-143">عند تحديد مبلغ لكل وحدة في حقل الأصل، يتم حساب ضريبة المبيعات كمبلغ ثابت لكل وحدة مضروبًا في الكمية التي تم إدخالها في بند المستند.</span><span class="sxs-lookup"><span data-stu-id="ac06e-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="ac06e-144">ويجب تحديد الوحدة في حقل الوحدة.</span><span class="sxs-lookup"><span data-stu-id="ac06e-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="ac06e-145">يتم تحديد المبلغ لكل وحدة في صفحة قيم أكواد ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="ac06e-146">مثال</span><span class="sxs-lookup"><span data-stu-id="ac06e-146">Example</span></span>

<span data-ttu-id="ac06e-147">يتم إعداد كود ضريبة المبيعات على النحو التالي: 1.20 دولار أمريكي للوحدة = يتم حساب مربع في 25 مربعًا لبند فاتورة المبيعات لصنف وهي عبارة عن ضريبة مبيعات على النحو التالي 25 × 1.20 = 30.00</span><span class="sxs-lookup"><span data-stu-id="ac06e-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>
| <span data-ttu-id="ac06e-148">**ملاحظة**</span><span class="sxs-lookup"><span data-stu-id="ac06e-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac06e-149">إذا تم إدخال الحركة في وحدة مختلفة عن الوحدة المحددة في كود ضريبة المبيعات، فإنه يتم تحويلها تلقائياً استناداً إلى تحويلات الوحدات التي يتم إعدادها في صفحة تحويلات الوحدات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="ac06e-150"> المبلغ لكل وحدة، خيار إضافي</span><span class="sxs-lookup"><span data-stu-id="ac06e-150">Amount per unit, additional option</span></span>

<span data-ttu-id="ac06e-151">في علامة التبويب العملية الحسابية، يمكنك تحديد ما إذا كان يتم حساب مبلغ لكل ضريبة محسوبة للوحدة قبل أكواد ضريبة أخرى وتتم إضافته إلى المبلغ الصافي قبل أكواد الضريبة الأخرى بالأصل = يتم حساب النسبة المئوية للمبلغ الصافي.</span><span class="sxs-lookup"><span data-stu-id="ac06e-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="ac06e-152">أمثلة</span><span class="sxs-lookup"><span data-stu-id="ac06e-152">Examples</span></span>

<span data-ttu-id="ac06e-153">افترض أننا نحسب كودي ضريبة في حركة:</span><span class="sxs-lookup"><span data-stu-id="ac06e-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="ac06e-154">الرسم الجمركي: الأصل = المبلغ كل وحدة وضريبة مبيعات، يتم تعيين القيمة إلى 5.00 لكل وحدة = قطع</span><span class="sxs-lookup"><span data-stu-id="ac06e-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="ac06e-155">ضريبة المبيعات: الأصل = كما هو موضح في الأمثلة التالية، يتم تعيين القيمة إلى 25%</span><span class="sxs-lookup"><span data-stu-id="ac06e-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="ac06e-156">نبيع قطعة واحدة من الصنف بسعر وحدة بمبلغ 10.00</span><span class="sxs-lookup"><span data-stu-id="ac06e-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="ac06e-157">مثال 1</span><span class="sxs-lookup"><span data-stu-id="ac06e-157">Example 1</span></span>

<span data-ttu-id="ac06e-158">ضريبة المبيعات: الأصل = النسبة المئوية لطريقة حساب المبلغ الإجمالي. لا يترك خيار "الحساب قبل ضريبة المبيعات‬" أي تأثير، لأنه يتم حساب ضريبة المبيعات كنسبة مئوية للمبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="ac06e-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="ac06e-159">الرسم الجمركي: 1 × 5.00 = 5.00 المبلغ الإجمالي: 10.00 + 5.00 = 15.00 ضريبة المبيعات: 15.00 × 25% = 3.75 ضريبة المبيعات الإجمالية: 5.00 + 3.75 = 8.75 المبلغ الإجمالي: 10.00 + 8.75 = 18.75</span><span class="sxs-lookup"><span data-stu-id="ac06e-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="ac06e-160">مثال 2</span><span class="sxs-lookup"><span data-stu-id="ac06e-160">Example 2</span></span>

<span data-ttu-id="ac06e-161">ضريبة المبيعات: الأصل = النسبة المئوية لصافي المبلغ. لا يتم تحديد خيار "الحساب قبل ضريبة المبيعات‬" لحساب الرسم الجمركي.</span><span class="sxs-lookup"><span data-stu-id="ac06e-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="ac06e-162">المبلغ الصافي: 10.00 الرسم الجمركي: 1 × 5.00 = 5.00 ضريبة المبيعات: 10.00 × 25% = 2.50 إجمالي ضريبة المبيعات: 5.00 + 2.50 = 7.50 المبلغ الإجمالي: 10.00 + 7.50 = 17.50</span><span class="sxs-lookup"><span data-stu-id="ac06e-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="ac06e-163">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="ac06e-163">Example 3</span></span>

<span data-ttu-id="ac06e-164">ضريبة المبيعات: الأصل = النسبة المئوية لصافي المبلغ. تم تحديد خيار "الحساب قبل ضريبة المبيعات‬" لحساب الرسم الجمركي.</span><span class="sxs-lookup"><span data-stu-id="ac06e-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="ac06e-165">المبلغ الصافي: 10.00 الرسم الجمركي: 1 × 5.00 = 5.00 ضريبة المبيعات: (10.00 +
5.00) × 25% = 3.75 إجمالي ضريبة المبيعات: 5.00 + 3.57 = 8.75 المبلغ الإجمالي: 10.00 + 8.75 = 18.75</span><span class="sxs-lookup"><span data-stu-id="ac06e-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="ac06e-166">المثال الرابع</span><span class="sxs-lookup"><span data-stu-id="ac06e-166">Example 4</span></span>

<span data-ttu-id="ac06e-167">نتيجة المثال الثالث هي نفس نتيجة المثال الأول، لأن هناك رسمًا جمركيًا واحدًا فقط.</span><span class="sxs-lookup"><span data-stu-id="ac06e-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="ac06e-168">افترض أنه لديك رسمان جمركيان، ويتم تضمين أحدهما فقط في المبلغ الصافي لحساب ضريبة المبيعات: الرسم الجمركي 1: 5.00 باستخدام طريقة المبلغ لكل وحدة، ويتم تحديد خيار الحساب قبل ضريبة المبيعات، الرسم الجمركي 2: 2.50، باستخدام طريقة المبلغ لكل وحدة، ولا يتم تحديد خيار الحساب قبل ضريبة المبيعات، ضريبة المبيعات: 25%، باستخدام النسبة المئوية لطريقة المبلغ الصافي، المبلغ الصافي: 10.00 الرسم الجمركي 1: 1 × 5.00 = 5.00 الرسم الجمركي 2: 1 × 2.50 = 2.50 المبلغ الصافي الخاضع لضريبة المبيعات: 10.00 + 5.00 = 15.00 ضريبة المبيعات: 15.00 × 25% = 3.75 ضرائب المبيعات الإجمالية، بما في ذلك الرسوم: 5.00 + 2.50 + 3.75 = 11.25 المبلغ الإجمالي: 10.00 + 11.25 = 21.25 يتم حساب ضريبة المبيعات بنسبة 25% لمجموع المبلغ الصافي (10.00) + الرسم الجمركي 1 (5.00) = 15.00.</span><span class="sxs-lookup"><span data-stu-id="ac06e-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="ac06e-169">تتم إضافة الرسم الجمركي 2 إلى مبلغ الضريبة لعد حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ac06e-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="ac06e-170"> النسبة المئوية المحسوبة من المبلغ الصافي</span><span class="sxs-lookup"><span data-stu-id="ac06e-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="ac06e-171">تعالج النسبة المئوية المحسوبة للمبلغ الصافي عملية حساب الضريبة بشكل مختلف استناداً إلى إعداد معلمة المبالغ تشمل ضريبة المبيعات للمستند أو دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ac06e-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="ac06e-172">مثال 1</span><span class="sxs-lookup"><span data-stu-id="ac06e-172">Example 1</span></span>

<span data-ttu-id="ac06e-173">يتم تعيين المستند / دفتر اليومية إلى المبالغ شاملة ضريبة المبيعات = نعم مبلغ بند الحركة: 10.00 معدل الضريبة : 25% ضريبة المبيعات: مبلغ بند الحركة × معدل الضريبة (10.00 × 25%) = 2.50 المبلغ الأساسي للضريبة (مبلغ الأصل): مبلغ بند الحركة - ضريبة المبيعات (10.00 - 2.50) = 7.50</span><span class="sxs-lookup"><span data-stu-id="ac06e-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="ac06e-174">مثال 2</span><span class="sxs-lookup"><span data-stu-id="ac06e-174">Example 2</span></span>

<span data-ttu-id="ac06e-175">يتم تعيين المستند / دفتر اليومية إلى المبالغ شاملة ضريبة المبيعات = لا مبلغ بند الحركة: 10.00 معدل الضريبة : 25% ضريبة المبيعات: (مبلغ بند الحركة × معدل الضريبة) / (100 - معدل الضريبة) (10.00 × 25%) / (100% - 25%)= 3.33 المبلغ الأساسي للضريبة (مبلغ الأصل): مبلغ بند الحركة = 10.00</span><span class="sxs-lookup"><span data-stu-id="ac06e-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="see-also"></a><span data-ttu-id="ac06e-176">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="ac06e-176">See also</span></span>
--------

[<span data-ttu-id="ac06e-177">تحديد معدلات ضريبة المبيعات استنادًا إلى حقلي "القاعدة الهامشية" و"أسلوب الحساب"</span><span class="sxs-lookup"><span data-stu-id="ac06e-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="ac06e-178">المبلغ بالكامل وخيارات حساب الفترات لأكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="ac06e-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




