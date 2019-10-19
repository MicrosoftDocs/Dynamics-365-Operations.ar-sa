---
title: إعداد معدلات الفائدة لكود فائدة
description: تحتوي أكواد الفائدة على إعدادات تحدد متى يتم فرض فائدة، وكيف يتم حسابها على الحسابات المتأخرة.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188983"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="ef656-103">إعداد معدلات الفائدة لكود فائدة</span><span class="sxs-lookup"><span data-stu-id="ef656-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef656-104">تحتوي أكواد الفائدة على إعدادات تحدد متى يتم فرض فائدة، وكيف يتم حسابها على الحسابات المتأخرة.</span><span class="sxs-lookup"><span data-stu-id="ef656-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="ef656-105">يمكنك إعداد كود فائدة واحد، وتطبيقه على ملفات تعريف متعددة لترحيل العملاء، أو على أكواد الفوترة، أو على بنود فاتورة محددة.</span><span class="sxs-lookup"><span data-stu-id="ef656-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="ef656-106">وعندما يتم تغيير تفاصيل كود الفائدة، تقوم جميع الميزات التي تستخدم الكود تلقائيًا بتنفيذ التغييرات على حركات جديدة.</span><span class="sxs-lookup"><span data-stu-id="ef656-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="ef656-107">بالنسبة لكل كود من أكواد الفائدة، يمكنك إعداد نوعين من الأسعار:</span><span class="sxs-lookup"><span data-stu-id="ef656-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="ef656-108">معدلات لإيرادات الفوائد - وهي تمثل الإيرادات التي تم الحصول عليها عن طريق تغيير الفائدة على الفواتير أو إشعارات الفائدة‬.</span><span class="sxs-lookup"><span data-stu-id="ef656-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="ef656-109">معدلات لمدفوعات الفوائد - وهي تمثل التكلفة التي يتم دفعها للفائدة على الإشعارات الدائنة‬.</span><span class="sxs-lookup"><span data-stu-id="ef656-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="ef656-110">ويمكن أن يوجد كل من نوعي المعدلات في نفس الوقت، وفي نفس كود الفائدة.</span><span class="sxs-lookup"><span data-stu-id="ef656-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="ef656-111">يمكن أن تستند معدلات الفائدة إلى ثلاثة أنواع من أنواع الحسابات:</span><span class="sxs-lookup"><span data-stu-id="ef656-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="ef656-112">الفائدة حسب النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="ef656-112">Interest by percentage.</span></span>
-   <span data-ttu-id="ef656-113">الفائدة حسب المبلغ.</span><span class="sxs-lookup"><span data-stu-id="ef656-113">Interest by amount.</span></span>
-   <span data-ttu-id="ef656-114">الفائدة حسب النطاق، والتي ينتج عنها نسبة مئوية واحدة أو مبلغ واحد.</span><span class="sxs-lookup"><span data-stu-id="ef656-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="ef656-115">وعند استخدام كود فائدة لحساب الفائدة، يتم إنشاء إشعار فائدة منفصلة لكل معدل من معدلات الفائدة التي تكون مفعلة أثناء الفترة التي يتجاوز فيها الدفع تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="ef656-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="ef656-116">تستخدم علامة التبويب **إيرادات** في صفحة **كود الفائدة** لإعداد أسعار الفائدة للفائدة التي تكسبها من خلال فرض فائدة.</span><span class="sxs-lookup"><span data-stu-id="ef656-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="ef656-117">استخدم علامة التبويب **المدفوعات** لإعداد معدلات فائدة للفائدة التي تقوم بدفعها.</span><span class="sxs-lookup"><span data-stu-id="ef656-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="ef656-118">معدلات الفائدة استنادًا إلى النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="ef656-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="ef656-119">يمكنك إعداد معدلات الفائدة التي تقوم بحساب نسبة مئوية محددة.</span><span class="sxs-lookup"><span data-stu-id="ef656-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="ef656-120">ينطبق مبلغ الفائدة على كافة العملات.</span><span class="sxs-lookup"><span data-stu-id="ef656-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="ef656-121">ويمكن إدخال حدود مبلغ الفائدة الاختيارية.</span><span class="sxs-lookup"><span data-stu-id="ef656-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="ef656-122">يتم تحديد <strong>النسبة المئوية</strong>\*\* <strong>في حقل \*\*حسال الفائدة بالاستناد إلى</strong> في صفحة <strong>إعداد أكواد الفائدة</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef656-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="ef656-123">على سبيل المثال، لإعداد كود فائدة يقوم بتقييم فائدة بقيمة 5 بالمائة لكل فترة مكونة من شهرين يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة، فقد تقوم بإدخال 2 في حقل **حساب الفائدة كل** وتحديد **الشهر‏‎**.</span><span class="sxs-lookup"><span data-stu-id="ef656-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="ef656-124">معدلات الفائدة استنادًا إلى المبالغ</span><span class="sxs-lookup"><span data-stu-id="ef656-124">Interest rates based on amounts</span></span>
<span data-ttu-id="ef656-125">يمكنك إعداد معدلات الفائدة التي تقوم بحساب مبلغ محدد لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="ef656-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="ef656-126">يتم تحديد مبلغ فائدة لكل عملة في كود الفائدة.</span><span class="sxs-lookup"><span data-stu-id="ef656-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="ef656-127">ويمكن إدخال حدود مبلغ الفائدة الاختيارية.</span><span class="sxs-lookup"><span data-stu-id="ef656-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="ef656-128">**المبلغ** يتم تحديده في حقل **حساب الفائدة بالاستناد إلى** في صفحة **إعداد أكواد الفائدة‬**.</span><span class="sxs-lookup"><span data-stu-id="ef656-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="ef656-129">على سبيل المثال، لإعداد كود فائدة يقوم بتقييم فائدة بقيمة 25.00 لكل فترة مكونة من 20 يومًا يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة، فقد تقوم بإدخال 20 في حقل **حساب الفائدة كل** وتحديد **يوم**.</span><span class="sxs-lookup"><span data-stu-id="ef656-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="ef656-130">معدلات الفائدة استنادًا إلى النطاقات</span><span class="sxs-lookup"><span data-stu-id="ef656-130">Interest rates based on ranges</span></span>
<span data-ttu-id="ef656-131">يمكنك إعداد معدلات الفائدة التي تتنوع اعتمادًا على المبلغ المتأخر، أو عدد الأيام التي تأخر تسديد المبلغ فيها، أو عدد الأشهر التي تأخر تسديد المبلغ خلالها.</span><span class="sxs-lookup"><span data-stu-id="ef656-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="ef656-132">يمكنك استخدام علامة التبويب **الأرباح حسب العملة‬** لتحديد إعدادات الفائدة المحددة لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="ef656-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="ef656-133">وهذا أيضًا هو المكان الذي ستحدد فيه النطاق.</span><span class="sxs-lookup"><span data-stu-id="ef656-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="ef656-134">استخدم الزر **نطاقات** لإضافة البنود التي تمثل النطاقات التي تريد إعدادها.</span><span class="sxs-lookup"><span data-stu-id="ef656-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="ef656-135">تمثل القيمة **من** بداية النطاق، ويمثل رقم **قيمة الفائدة** نسبة مئوية أو مبلغ، استنادًا إلى التحديد في حقل **حساب الفائدة بالاستناد إلى‬** في صفحة **إعداد أكواد الفائدة**.</span><span class="sxs-lookup"><span data-stu-id="ef656-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="ef656-136">مثال 1: الفائدة حسب النطاق = المبلغ</span><span class="sxs-lookup"><span data-stu-id="ef656-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="ef656-137">تقوم بإعداد كود فائدة يقوم بتقييم الفائدة مرةً واحدة لكل فترة مكونة من ثلاثة أشهر يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="ef656-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ef656-138">ثم تريد تأسيس الحساب على قيمة فائدة نسبة مئوية، وفقًا لفترات المبالغ التي تم تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="ef656-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="ef656-139">وستكون قيمة الفائدة هي 1 بالمائة لمبالغ الفاتورة حتى 100000، و2 بالمائة للمبالغ من 100100 إلى 500000، و3 بالمائة للمبالغ الأكبر من 500000.</span><span class="sxs-lookup"><span data-stu-id="ef656-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="ef656-140">ومن ثم، تقوم بإعداد قيمة حقل كود الفائدة كما يلي.</span><span class="sxs-lookup"><span data-stu-id="ef656-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ef656-141">**اسم الحقل**</span><span class="sxs-lookup"><span data-stu-id="ef656-141">**Field name**</span></span>                  | <span data-ttu-id="ef656-142">**قيمة الحقل**</span><span class="sxs-lookup"><span data-stu-id="ef656-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ef656-143">**كود الفائدة**</span><span class="sxs-lookup"><span data-stu-id="ef656-143">**Interest code**</span></span>               | <span data-ttu-id="ef656-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="ef656-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="ef656-145">**حساب الفائدة كل**</span><span class="sxs-lookup"><span data-stu-id="ef656-145">**Calculate interest every**</span></span>    | <span data-ttu-id="ef656-146">3/شهر</span><span class="sxs-lookup"><span data-stu-id="ef656-146">3/Month</span></span>         |
| <span data-ttu-id="ef656-147">**الفائدة حسب النطاق**</span><span class="sxs-lookup"><span data-stu-id="ef656-147">**Interest by range**</span></span>           | <span data-ttu-id="ef656-148">المبلغ</span><span class="sxs-lookup"><span data-stu-id="ef656-148">Amount</span></span>          |
| <span data-ttu-id="ef656-149">**حساب الفائدة بالاستناد إلى**</span><span class="sxs-lookup"><span data-stu-id="ef656-149">**Calculate interest based on**</span></span> | <span data-ttu-id="ef656-150">النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="ef656-150">Percentage</span></span>      |

<span data-ttu-id="ef656-151">وتقوم بإعداد معلومات النطاق كما يلي.</span><span class="sxs-lookup"><span data-stu-id="ef656-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="ef656-152">**من القيمة**</span><span class="sxs-lookup"><span data-stu-id="ef656-152">**From value**</span></span> | <span data-ttu-id="ef656-153">**قيمة الفائدة**</span><span class="sxs-lookup"><span data-stu-id="ef656-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ef656-154">0</span><span class="sxs-lookup"><span data-stu-id="ef656-154">0</span></span>              | <span data-ttu-id="ef656-155">1</span><span class="sxs-lookup"><span data-stu-id="ef656-155">1</span></span>                  |
| <span data-ttu-id="ef656-156">1,001</span><span class="sxs-lookup"><span data-stu-id="ef656-156">1,001</span></span>          | <span data-ttu-id="ef656-157">2</span><span class="sxs-lookup"><span data-stu-id="ef656-157">2</span></span>                  |
| <span data-ttu-id="ef656-158">5,001</span><span class="sxs-lookup"><span data-stu-id="ef656-158">5,001</span></span>          | <span data-ttu-id="ef656-159">3</span><span class="sxs-lookup"><span data-stu-id="ef656-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="ef656-160">مثال 2: الفائدة حسب النطاق = الأيام</span><span class="sxs-lookup"><span data-stu-id="ef656-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="ef656-161">تقوم بإعداد كود فائدة يقوم بتقييم الفائدة مرةً واحدة لكل فترة مكونة من 15 يومًا يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="ef656-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ef656-162">ثم تريد تأسيس الحساب على قيمة فائدة مبلغ، وفقًا لفترات الأيام التي تم تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="ef656-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="ef656-163">ستكون قيمة الفائدة 1000 لكل 15 يومًا أثناء فترة 60 يومًا الأولى، و1500 لكل فترة مكونة من 15 يومًا خلال الأيام من 61 إلى 90، و2000 لكل 15 يومًا بداية من اليوم 91 فصاعدًا.</span><span class="sxs-lookup"><span data-stu-id="ef656-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="ef656-164">ومن ثم، تقوم بإعداد قيمة حقل كود الفائدة كما يلي.</span><span class="sxs-lookup"><span data-stu-id="ef656-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ef656-165">**اسم الحقل**</span><span class="sxs-lookup"><span data-stu-id="ef656-165">**Field name**</span></span>                  | <span data-ttu-id="ef656-166">**قيمة الحقل**</span><span class="sxs-lookup"><span data-stu-id="ef656-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ef656-167">**كود الفائدة**</span><span class="sxs-lookup"><span data-stu-id="ef656-167">**Interest code**</span></span>               | <span data-ttu-id="ef656-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="ef656-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="ef656-169">**حساب الفائدة كل**</span><span class="sxs-lookup"><span data-stu-id="ef656-169">**Calculate interest every**</span></span>    | <span data-ttu-id="ef656-170">15/يوم</span><span class="sxs-lookup"><span data-stu-id="ef656-170">15/Day</span></span>          |
| <span data-ttu-id="ef656-171">**الفائدة حسب النطاق**</span><span class="sxs-lookup"><span data-stu-id="ef656-171">**Interest by range**</span></span>           | <span data-ttu-id="ef656-172">أيام</span><span class="sxs-lookup"><span data-stu-id="ef656-172">Days</span></span>            |
| <span data-ttu-id="ef656-173">**حساب الفائدة بالاستناد إلى**</span><span class="sxs-lookup"><span data-stu-id="ef656-173">**Calculate interest based on**</span></span> | <span data-ttu-id="ef656-174">المبلغ</span><span class="sxs-lookup"><span data-stu-id="ef656-174">Amount</span></span>          |

<span data-ttu-id="ef656-175">وتقوم بإعداد معلومات النطاق كما يلي.</span><span class="sxs-lookup"><span data-stu-id="ef656-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="ef656-176">**من القيمة**</span><span class="sxs-lookup"><span data-stu-id="ef656-176">**From value**</span></span> | <span data-ttu-id="ef656-177">**قيمة الفائدة**</span><span class="sxs-lookup"><span data-stu-id="ef656-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ef656-178">0</span><span class="sxs-lookup"><span data-stu-id="ef656-178">0</span></span>              | <span data-ttu-id="ef656-179">10</span><span class="sxs-lookup"><span data-stu-id="ef656-179">10</span></span>                 |
| <span data-ttu-id="ef656-180">61</span><span class="sxs-lookup"><span data-stu-id="ef656-180">61</span></span>             | <span data-ttu-id="ef656-181">15</span><span class="sxs-lookup"><span data-stu-id="ef656-181">15</span></span>                 |
| <span data-ttu-id="ef656-182">91</span><span class="sxs-lookup"><span data-stu-id="ef656-182">91</span></span>             | <span data-ttu-id="ef656-183">20</span><span class="sxs-lookup"><span data-stu-id="ef656-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="ef656-184">مثال 3: الفائدة حسب النطاق = الشهور</span><span class="sxs-lookup"><span data-stu-id="ef656-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="ef656-185">تقوم بإعداد كود فائدة يقوم بتقييم الفائدة مرةً واحدة لكل شهر يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="ef656-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ef656-186">ثم تريد تأسيس الحساب على قيمة فائدة نسبة مئوية، وفقًا لفترات الأشهر التي تم تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="ef656-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="ef656-187">ستكون قيمة الفائدة 1.5 بالمائة لكل شهر لمدة الثلاثة أشهر الأولى المتأخرة، و2 بالمائة لكل شهر للثلاثة أشهر الثانية، و2.5 بالمائة لكل شهر بعد الستة أشهر الأولى.</span><span class="sxs-lookup"><span data-stu-id="ef656-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="ef656-188">ومن ثم، تقوم بإعداد قيمة حقل كود الفائدة كما يلي.</span><span class="sxs-lookup"><span data-stu-id="ef656-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ef656-189">**اسم الحقل**</span><span class="sxs-lookup"><span data-stu-id="ef656-189">**Field name**</span></span>                  | <span data-ttu-id="ef656-190">**قيمة الحقل**</span><span class="sxs-lookup"><span data-stu-id="ef656-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ef656-191">**كود الفائدة**</span><span class="sxs-lookup"><span data-stu-id="ef656-191">**Interest code**</span></span>               | <span data-ttu-id="ef656-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="ef656-192">1M%ByMth</span></span>        |
| <span data-ttu-id="ef656-193">**حساب الفائدة كل**</span><span class="sxs-lookup"><span data-stu-id="ef656-193">**Calculate interest every**</span></span>    | <span data-ttu-id="ef656-194">1/شهر</span><span class="sxs-lookup"><span data-stu-id="ef656-194">1/Month</span></span>         |
| <span data-ttu-id="ef656-195">**الفائدة حسب النطاق**</span><span class="sxs-lookup"><span data-stu-id="ef656-195">**Interest by range**</span></span>           | <span data-ttu-id="ef656-196">الشهور</span><span class="sxs-lookup"><span data-stu-id="ef656-196">Months</span></span>          |
| <span data-ttu-id="ef656-197">**حساب الفائدة بالاستناد إلى**</span><span class="sxs-lookup"><span data-stu-id="ef656-197">**Calculate interest based on**</span></span> | <span data-ttu-id="ef656-198">النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="ef656-198">Percentage</span></span>      |

<span data-ttu-id="ef656-199">وتقوم بإعداد معلومات النطاق كما يلي.</span><span class="sxs-lookup"><span data-stu-id="ef656-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="ef656-200">**من القيمة**</span><span class="sxs-lookup"><span data-stu-id="ef656-200">**From value**</span></span> | <span data-ttu-id="ef656-201">**قيمة الفائدة**</span><span class="sxs-lookup"><span data-stu-id="ef656-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ef656-202">0</span><span class="sxs-lookup"><span data-stu-id="ef656-202">0</span></span>              | <span data-ttu-id="ef656-203">1.5</span><span class="sxs-lookup"><span data-stu-id="ef656-203">1.5</span></span>                |
| <span data-ttu-id="ef656-204">4</span><span class="sxs-lookup"><span data-stu-id="ef656-204">4</span></span>              | <span data-ttu-id="ef656-205">2</span><span class="sxs-lookup"><span data-stu-id="ef656-205">2</span></span>                  |
| <span data-ttu-id="ef656-206">7</span><span class="sxs-lookup"><span data-stu-id="ef656-206">7</span></span>              | <span data-ttu-id="ef656-207">2.5</span><span class="sxs-lookup"><span data-stu-id="ef656-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="ef656-208">الإصدارات الجديدة</span><span class="sxs-lookup"><span data-stu-id="ef656-208">New versions</span></span>
<span data-ttu-id="ef656-209">أكواد الفائدة سارية التاريخ.</span><span class="sxs-lookup"><span data-stu-id="ef656-209">Interest codes are date effective.</span></span> <span data-ttu-id="ef656-210">وإذا أردت تعديل سعر الفائدة، يمكنك إنشاء **الإصدار الجديد** الذي كان ساري المفعول اعتبارًا من تاريخ في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="ef656-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="ef656-211">لعرض إصدارات مختلفة، يمكنك استخدام اختيار قائمة **اعتبارًا من تاريخ** لتحديد تاريخ الانقطاع.</span><span class="sxs-lookup"><span data-stu-id="ef656-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="ef656-212">كما يمكنك تحديد **عرض كافة السجلات** لعرض كافة أكواد الفائدة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ef656-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



