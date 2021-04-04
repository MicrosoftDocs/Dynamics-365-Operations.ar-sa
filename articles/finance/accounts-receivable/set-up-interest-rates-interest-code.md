---
title: إعداد معدلات الفائدة لكود فائدة
description: تحتوي أكواد الفائدة على إعدادات تحدد متى يتم فرض فائدة، وكيف يتم حسابها على الحسابات المتأخرة.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d9ff856e34eb894c5d0ab5fe17c8e95f62fff57
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555355"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="61e3c-103">إعداد معدلات الفائدة لكود فائدة</span><span class="sxs-lookup"><span data-stu-id="61e3c-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61e3c-104">تحتوي أكواد الفائدة على إعدادات تحدد متى يتم فرض فائدة، وكيف يتم حسابها على الحسابات المتأخرة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="61e3c-105">يمكنك إعداد كود فائدة واحد، وتطبيقه على ملفات تعريف متعددة لترحيل العملاء، أو على أكواد الفوترة، أو على بنود فاتورة محددة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="61e3c-106">وعندما يتم تغيير تفاصيل كود الفائدة، تقوم جميع الميزات التي تستخدم الكود تلقائيًا بتنفيذ التغييرات على حركات جديدة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="61e3c-107">بالنسبة لكل كود من أكواد الفائدة، يمكنك إعداد نوعين من الأسعار:</span><span class="sxs-lookup"><span data-stu-id="61e3c-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="61e3c-108">معدلات لإيرادات الفوائد - وهي تمثل الإيرادات التي تم الحصول عليها عن طريق تغيير الفائدة على الفواتير أو إشعارات الفائدة‬.</span><span class="sxs-lookup"><span data-stu-id="61e3c-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="61e3c-109">معدلات لمدفوعات الفوائد - وهي تمثل التكلفة التي يتم دفعها للفائدة على الإشعارات الدائنة‬.</span><span class="sxs-lookup"><span data-stu-id="61e3c-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="61e3c-110">ويمكن أن يوجد كل من نوعي المعدلات في نفس الوقت، وفي نفس كود الفائدة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="61e3c-111">يمكن أن تستند معدلات الفائدة إلى ثلاثة أنواع من أنواع الحسابات:</span><span class="sxs-lookup"><span data-stu-id="61e3c-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="61e3c-112">الفائدة حسب النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="61e3c-112">Interest by percentage.</span></span>
-   <span data-ttu-id="61e3c-113">الفائدة حسب المبلغ.</span><span class="sxs-lookup"><span data-stu-id="61e3c-113">Interest by amount.</span></span>
-   <span data-ttu-id="61e3c-114">الفائدة حسب النطاق، والتي ينتج عنها نسبة مئوية واحدة أو مبلغ واحد.</span><span class="sxs-lookup"><span data-stu-id="61e3c-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="61e3c-115">وعند استخدام كود فائدة لحساب الفائدة، يتم إنشاء إشعار فائدة منفصلة لكل معدل من معدلات الفائدة التي تكون مفعلة أثناء الفترة التي يتجاوز فيها الدفع تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="61e3c-116">تستخدم علامة التبويب **إيرادات** في صفحة **كود الفائدة** لإعداد أسعار الفائدة للفائدة التي تكسبها من خلال فرض فائدة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="61e3c-117">استخدم علامة التبويب **المدفوعات** لإعداد معدلات فائدة للفائدة التي تقوم بدفعها.</span><span class="sxs-lookup"><span data-stu-id="61e3c-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="61e3c-118">معدلات الفائدة استنادًا إلى النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="61e3c-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="61e3c-119">يمكنك إعداد معدلات الفائدة التي تقوم بحساب نسبة مئوية محددة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="61e3c-120">ينطبق مبلغ الفائدة على كافة العملات.</span><span class="sxs-lookup"><span data-stu-id="61e3c-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="61e3c-121">ويمكن إدخال حدود مبلغ الفائدة الاختيارية.</span><span class="sxs-lookup"><span data-stu-id="61e3c-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="61e3c-122">يتم تحديد **النسبة المئوية** في حقل **حساب الفائدة بالاستناد إلى** في صفحة **إعداد أكواد الفائدة**.</span><span class="sxs-lookup"><span data-stu-id="61e3c-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="61e3c-123">على سبيل المثال، لإعداد كود فائدة يقوم بتقييم فائدة بقيمة 5 بالمائة لكل فترة مكونة من شهرين يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة، فقد تقوم بإدخال 2 في حقل **حساب الفائدة كل** وتحديد **الشهر‏‎**.</span><span class="sxs-lookup"><span data-stu-id="61e3c-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="61e3c-124">تتم إضافة الخوارزمية الجديدة الخاصة بحساب إشعار الفائدة باستخدام إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="61e3c-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="61e3c-125">لاستخدام هذه الخوارزمية، قم بتمكين ميزة **(GBL) السماح بحساب الفائدة لكل يوم حسب النسبة المئوية السنوية مقسومة على 365**.</span><span class="sxs-lookup"><span data-stu-id="61e3c-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="61e3c-126">للحصول على المعلومات حول كيفية تمكين الميزة، راجع [نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="61e3c-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="61e3c-127">معادلة حساب مبلغ إشعار الفائدة هي:</span><span class="sxs-lookup"><span data-stu-id="61e3c-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="61e3c-128">مبلغ إشعار الفائدة = المبلغ المستحق \* الفائدة السنوية % / 365 \* عدد الأيام المتأخرة</span><span class="sxs-lookup"><span data-stu-id="61e3c-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="61e3c-129">هذه الميزة متوفرة في الإصدار 10.0.18 أو الإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="61e3c-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="61e3c-130">معدلات الفائدة استنادًا إلى المبالغ</span><span class="sxs-lookup"><span data-stu-id="61e3c-130">Interest rates based on amounts</span></span>
<span data-ttu-id="61e3c-131">يمكنك إعداد معدلات الفائدة التي تقوم بحساب مبلغ محدد لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="61e3c-132">يتم تحديد مبلغ فائدة لكل عملة في كود الفائدة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="61e3c-133">ويمكن إدخال حدود مبلغ الفائدة الاختيارية.</span><span class="sxs-lookup"><span data-stu-id="61e3c-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="61e3c-134">**المبلغ** يتم تحديده في حقل **حساب الفائدة بالاستناد إلى** في صفحة **إعداد أكواد الفائدة‬**.</span><span class="sxs-lookup"><span data-stu-id="61e3c-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="61e3c-135">على سبيل المثال، لإعداد كود فائدة يقوم بتقييم فائدة بقيمة 25.00 لكل فترة مكونة من 20 يومًا يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة، فقد تقوم بإدخال 20 في حقل **حساب الفائدة كل** وتحديد **يوم**.</span><span class="sxs-lookup"><span data-stu-id="61e3c-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="61e3c-136">معدلات الفائدة استنادًا إلى النطاقات</span><span class="sxs-lookup"><span data-stu-id="61e3c-136">Interest rates based on ranges</span></span>
<span data-ttu-id="61e3c-137">يمكنك إعداد معدلات الفائدة التي تتنوع اعتمادًا على المبلغ المتأخر، أو عدد الأيام التي تأخر تسديد المبلغ فيها، أو عدد الأشهر التي تأخر تسديد المبلغ خلالها.</span><span class="sxs-lookup"><span data-stu-id="61e3c-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="61e3c-138">يمكنك استخدام علامة التبويب **الأرباح حسب العملة‬** لتحديد إعدادات الفائدة المحددة لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="61e3c-139">وهذا أيضًا هو المكان الذي ستحدد فيه النطاق.</span><span class="sxs-lookup"><span data-stu-id="61e3c-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="61e3c-140">استخدم الزر **نطاقات** لإضافة البنود التي تمثل النطاقات التي تريد إعدادها.</span><span class="sxs-lookup"><span data-stu-id="61e3c-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="61e3c-141">تمثل القيمة **من** بداية النطاق، ويمثل رقم **قيمة الفائدة** نسبة مئوية أو مبلغ، استنادًا إلى التحديد في حقل **حساب الفائدة بالاستناد إلى‬** في صفحة **إعداد أكواد الفائدة**.</span><span class="sxs-lookup"><span data-stu-id="61e3c-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="61e3c-142">مثال 1: الفائدة حسب النطاق = المبلغ</span><span class="sxs-lookup"><span data-stu-id="61e3c-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="61e3c-143">تقوم بإعداد كود فائدة يقوم بتقييم الفائدة مرةً واحدة لكل فترة مكونة من ثلاثة أشهر يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="61e3c-144">ثم تريد تأسيس الحساب على قيمة فائدة نسبة مئوية، وفقًا لفترات المبالغ التي تم تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="61e3c-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="61e3c-145">وستكون قيمة الفائدة هي 1 بالمائة لمبالغ الفاتورة حتى 100000، و2 بالمائة للمبالغ من 100100 إلى 500000، و3 بالمائة للمبالغ الأكبر من 500000.</span><span class="sxs-lookup"><span data-stu-id="61e3c-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="61e3c-146">ومن ثم، تقوم بإعداد قيمة حقل كود الفائدة كما يلي.</span><span class="sxs-lookup"><span data-stu-id="61e3c-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="61e3c-147">**اسم الحقل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-147">**Field name**</span></span>                  | <span data-ttu-id="61e3c-148">**قيمة الحقل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="61e3c-149">**كود الفائدة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-149">**Interest code**</span></span>               | <span data-ttu-id="61e3c-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="61e3c-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="61e3c-151">**حساب الفائدة كل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-151">**Calculate interest every**</span></span>    | <span data-ttu-id="61e3c-152">3/شهر</span><span class="sxs-lookup"><span data-stu-id="61e3c-152">3/Month</span></span>         |
| <span data-ttu-id="61e3c-153">**الفائدة حسب النطاق**</span><span class="sxs-lookup"><span data-stu-id="61e3c-153">**Interest by range**</span></span>           | <span data-ttu-id="61e3c-154">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61e3c-154">Amount</span></span>          |
| <span data-ttu-id="61e3c-155">**حساب الفائدة بالاستناد إلى**</span><span class="sxs-lookup"><span data-stu-id="61e3c-155">**Calculate interest based on**</span></span> | <span data-ttu-id="61e3c-156">النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="61e3c-156">Percentage</span></span>      |

<span data-ttu-id="61e3c-157">وتقوم بإعداد معلومات النطاق كما يلي.</span><span class="sxs-lookup"><span data-stu-id="61e3c-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="61e3c-158">**من القيمة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-158">**From value**</span></span> | <span data-ttu-id="61e3c-159">**قيمة الفائدة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="61e3c-160">0</span><span class="sxs-lookup"><span data-stu-id="61e3c-160">0</span></span>              | <span data-ttu-id="61e3c-161">1</span><span class="sxs-lookup"><span data-stu-id="61e3c-161">1</span></span>                  |
| <span data-ttu-id="61e3c-162">1,001</span><span class="sxs-lookup"><span data-stu-id="61e3c-162">1,001</span></span>          | <span data-ttu-id="61e3c-163">2</span><span class="sxs-lookup"><span data-stu-id="61e3c-163">2</span></span>                  |
| <span data-ttu-id="61e3c-164">5,001</span><span class="sxs-lookup"><span data-stu-id="61e3c-164">5,001</span></span>          | <span data-ttu-id="61e3c-165">3</span><span class="sxs-lookup"><span data-stu-id="61e3c-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="61e3c-166">مثال 2: الفائدة حسب النطاق = الأيام</span><span class="sxs-lookup"><span data-stu-id="61e3c-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="61e3c-167">تقوم بإعداد كود فائدة يقوم بتقييم الفائدة مرةً واحدة لكل فترة مكونة من 15 يومًا يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="61e3c-168">ثم تريد تأسيس الحساب على قيمة فائدة مبلغ، وفقًا لفترات الأيام التي تم تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="61e3c-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="61e3c-169">ستكون قيمة الفائدة 1000 لكل 15 يومًا أثناء فترة 60 يومًا الأولى، و1500 لكل فترة مكونة من 15 يومًا خلال الأيام من 61 إلى 90، و2000 لكل 15 يومًا بداية من اليوم 91 فصاعدًا.</span><span class="sxs-lookup"><span data-stu-id="61e3c-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="61e3c-170">ومن ثم، تقوم بإعداد قيمة حقل كود الفائدة كما يلي.</span><span class="sxs-lookup"><span data-stu-id="61e3c-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="61e3c-171">**اسم الحقل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-171">**Field name**</span></span>                  | <span data-ttu-id="61e3c-172">**قيمة الحقل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="61e3c-173">**كود الفائدة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-173">**Interest code**</span></span>               | <span data-ttu-id="61e3c-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="61e3c-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="61e3c-175">**حساب الفائدة كل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-175">**Calculate interest every**</span></span>    | <span data-ttu-id="61e3c-176">15/يوم</span><span class="sxs-lookup"><span data-stu-id="61e3c-176">15/Day</span></span>          |
| <span data-ttu-id="61e3c-177">**الفائدة حسب النطاق**</span><span class="sxs-lookup"><span data-stu-id="61e3c-177">**Interest by range**</span></span>           | <span data-ttu-id="61e3c-178">أيام</span><span class="sxs-lookup"><span data-stu-id="61e3c-178">Days</span></span>            |
| <span data-ttu-id="61e3c-179">**حساب الفائدة بالاستناد إلى**</span><span class="sxs-lookup"><span data-stu-id="61e3c-179">**Calculate interest based on**</span></span> | <span data-ttu-id="61e3c-180">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61e3c-180">Amount</span></span>          |

<span data-ttu-id="61e3c-181">وتقوم بإعداد معلومات النطاق كما يلي.</span><span class="sxs-lookup"><span data-stu-id="61e3c-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="61e3c-182">**من القيمة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-182">**From value**</span></span> | <span data-ttu-id="61e3c-183">**قيمة الفائدة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="61e3c-184">0</span><span class="sxs-lookup"><span data-stu-id="61e3c-184">0</span></span>              | <span data-ttu-id="61e3c-185">10</span><span class="sxs-lookup"><span data-stu-id="61e3c-185">10</span></span>                 |
| <span data-ttu-id="61e3c-186">61</span><span class="sxs-lookup"><span data-stu-id="61e3c-186">61</span></span>             | <span data-ttu-id="61e3c-187">15</span><span class="sxs-lookup"><span data-stu-id="61e3c-187">15</span></span>                 |
| <span data-ttu-id="61e3c-188">91</span><span class="sxs-lookup"><span data-stu-id="61e3c-188">91</span></span>             | <span data-ttu-id="61e3c-189">20</span><span class="sxs-lookup"><span data-stu-id="61e3c-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="61e3c-190">مثال 3: الفائدة حسب النطاق = الشهور</span><span class="sxs-lookup"><span data-stu-id="61e3c-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="61e3c-191">تقوم بإعداد كود فائدة يقوم بتقييم الفائدة مرةً واحدة لكل شهر يتجاوز فيها دفع الفاتورة تاريخ الاستحقاق للحركة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="61e3c-192">ثم تريد تأسيس الحساب على قيمة فائدة نسبة مئوية، وفقًا لفترات الأشهر التي تم تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="61e3c-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="61e3c-193">ستكون قيمة الفائدة 1.5 بالمائة لكل شهر لمدة الثلاثة أشهر الأولى المتأخرة، و2 بالمائة لكل شهر للثلاثة أشهر الثانية، و2.5 بالمائة لكل شهر بعد الستة أشهر الأولى.</span><span class="sxs-lookup"><span data-stu-id="61e3c-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="61e3c-194">ومن ثم، تقوم بإعداد قيمة حقل كود الفائدة كما يلي.</span><span class="sxs-lookup"><span data-stu-id="61e3c-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="61e3c-195">**اسم الحقل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-195">**Field name**</span></span>                  | <span data-ttu-id="61e3c-196">**قيمة الحقل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="61e3c-197">**كود الفائدة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-197">**Interest code**</span></span>               | <span data-ttu-id="61e3c-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="61e3c-198">1M%ByMth</span></span>        |
| <span data-ttu-id="61e3c-199">**حساب الفائدة كل**</span><span class="sxs-lookup"><span data-stu-id="61e3c-199">**Calculate interest every**</span></span>    | <span data-ttu-id="61e3c-200">1/شهر</span><span class="sxs-lookup"><span data-stu-id="61e3c-200">1/Month</span></span>         |
| <span data-ttu-id="61e3c-201">**الفائدة حسب النطاق**</span><span class="sxs-lookup"><span data-stu-id="61e3c-201">**Interest by range**</span></span>           | <span data-ttu-id="61e3c-202">الشهور</span><span class="sxs-lookup"><span data-stu-id="61e3c-202">Months</span></span>          |
| <span data-ttu-id="61e3c-203">**حساب الفائدة بالاستناد إلى**</span><span class="sxs-lookup"><span data-stu-id="61e3c-203">**Calculate interest based on**</span></span> | <span data-ttu-id="61e3c-204">النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="61e3c-204">Percentage</span></span>      |

<span data-ttu-id="61e3c-205">وتقوم بإعداد معلومات النطاق كما يلي.</span><span class="sxs-lookup"><span data-stu-id="61e3c-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="61e3c-206">**من القيمة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-206">**From value**</span></span> | <span data-ttu-id="61e3c-207">**قيمة الفائدة**</span><span class="sxs-lookup"><span data-stu-id="61e3c-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="61e3c-208">0</span><span class="sxs-lookup"><span data-stu-id="61e3c-208">0</span></span>              | <span data-ttu-id="61e3c-209">1.5</span><span class="sxs-lookup"><span data-stu-id="61e3c-209">1.5</span></span>                |
| <span data-ttu-id="61e3c-210">4</span><span class="sxs-lookup"><span data-stu-id="61e3c-210">4</span></span>              | <span data-ttu-id="61e3c-211">2</span><span class="sxs-lookup"><span data-stu-id="61e3c-211">2</span></span>                  |
| <span data-ttu-id="61e3c-212">7</span><span class="sxs-lookup"><span data-stu-id="61e3c-212">7</span></span>              | <span data-ttu-id="61e3c-213">2.5</span><span class="sxs-lookup"><span data-stu-id="61e3c-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="61e3c-214">الإصدارات الجديدة</span><span class="sxs-lookup"><span data-stu-id="61e3c-214">New versions</span></span>
<span data-ttu-id="61e3c-215">أكواد الفائدة سارية التاريخ.</span><span class="sxs-lookup"><span data-stu-id="61e3c-215">Interest codes are date effective.</span></span> <span data-ttu-id="61e3c-216">وإذا أردت تعديل سعر الفائدة، يمكنك إنشاء **الإصدار الجديد** الذي كان ساري المفعول اعتبارًا من تاريخ في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="61e3c-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="61e3c-217">لعرض إصدارات مختلفة، يمكنك استخدام اختيار قائمة **اعتبارًا من تاريخ** لتحديد تاريخ الانقطاع.</span><span class="sxs-lookup"><span data-stu-id="61e3c-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="61e3c-218">كما يمكنك تحديد **عرض كافة السجلات** لعرض كافة أكواد الفائدة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="61e3c-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
