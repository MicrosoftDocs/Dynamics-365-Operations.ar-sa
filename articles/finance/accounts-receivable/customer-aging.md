---
title: تقرير تقادم العميل
description: ويعرض تقرير فتره التاخر للعميل الارصده المستحقة من العملاء أو التي تم فرزها حسب فتره التاريخ أو فتره التقادم.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2020
ms.locfileid: "4440115"
---
# <a name="customer-aging-report"></a><span data-ttu-id="02281-103">تقرير تقادم العميل</span><span class="sxs-lookup"><span data-stu-id="02281-103">Customer aging report</span></span> 

<span data-ttu-id="02281-104">ويعرض تقرير **فتره تقادم العميل** الارصده المستحقة من العملاء أو التي تم فرزها حسب فتره التاريخ أو فتره التقادم.</span><span class="sxs-lookup"><span data-stu-id="02281-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="02281-105">عند إنشاء هذا التقرير، تظهر المعلمات الافتراضية التالية.</span><span class="sxs-lookup"><span data-stu-id="02281-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="02281-106">يمكنك استخدام هذه المعلمات لتصفية البيانات التي ستظهر في التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="02281-107">لمزيدٍ من المعلومات، راجع [إعداد المجموعات](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="02281-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02281-108">الحقل</span><span class="sxs-lookup"><span data-stu-id="02281-108">Field</span></span></p></th>
<th><p><span data-ttu-id="02281-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="02281-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02281-110"><strong>تصنيف الفوترة</strong></span><span class="sxs-lookup"><span data-stu-id="02281-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-111">حدد واحدًا أو أكثر من تصنيفات الفوترة المراد تضمينها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="02281-112">**ملاحظة:** يتوفر عنصر التحكم هذا فقط إذا تم تحديد مفتاح تكوين <STRONG>القطاع العام</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="02281-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-113"><strong>تضمين حركات من دون تصنيف فوترة</strong></span><span class="sxs-lookup"><span data-stu-id="02281-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-114">في حاله تحديد خانه الاختيار هذه، سيتم عرض كافة الحركات التي لم يتم تعيين تصنيف فوتره لها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="02281-115">**ملاحظة:** يتوفر عنصر التحكم هذا فقط إذا تم تحديد مفتاح تكوين <STRONG>القطاع العام</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="02281-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-116"><strong>فترة التأخر اعتبارًا من</strong></span><span class="sxs-lookup"><span data-stu-id="02281-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-117">ادخل التاريخ المستخدم في مستودع فتره التقادم الحالي.</span><span class="sxs-lookup"><span data-stu-id="02281-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-118"><strong>الرصيد اعتبارًا من</strong></span><span class="sxs-lookup"><span data-stu-id="02281-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-119">أدخل التاريخ المراد عرض أرصدة العملاء له.</span><span class="sxs-lookup"><span data-stu-id="02281-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="02281-120">ويعرف هذا أيضا بتاريخ الانقطاع الخاص بالحركات.</span><span class="sxs-lookup"><span data-stu-id="02281-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-121"><strong>تاريخ البدء</strong></span><span class="sxs-lookup"><span data-stu-id="02281-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-122">أدخل التاريخ الذي يقع ضمن الفاصل الأول للفترة أو فترة التقادم للتضمين في التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-123"><strong>المعايير</strong></span><span class="sxs-lookup"><span data-stu-id="02281-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-124">حدد نوع التاريخ الذي يستند إليه التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="02281-125"><strong>تاريخ الحركة</strong> - تاريخ الترحيل الخاص بالحركات المحددة.</span><span class="sxs-lookup"><span data-stu-id="02281-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="02281-126">علي سبيل المثال، قد يكون هذا هو تاريخ الفاتورة الذي يعد أساس حساب تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="02281-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="02281-127"><strong>تاريخ الاستحقاق</strong> - تاريخ استحقاق الحركات استنادًا إلى شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="02281-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="02281-128"><strong>تاريخ المستند</strong> - تاريخ المستند المحدد بواسطة المستخدم الذي يمثل أساس احتساب تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="02281-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-129"><strong>تعريف فترة التأخر</strong></span><span class="sxs-lookup"><span data-stu-id="02281-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-130">حدد تعريف فترة تأخر.</span><span class="sxs-lookup"><span data-stu-id="02281-130">Select an aging period definition.</span></span> <span data-ttu-id="02281-131">لا يتم استخدام الحقل <strong>الفاصل</strong> في حالة تحديد فترة التقادم.</span><span class="sxs-lookup"><span data-stu-id="02281-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="02281-132">لا يمكن استخدام تعريفات فترات التقادم التي تحتوي علي أكثر من ست فترات تقادم في التقرير المطبوع.</span><span class="sxs-lookup"><span data-stu-id="02281-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="02281-133">**ملاحظه:** يمكن اعداد فترات التقادم في صفحه <STRONG>تعريفات فترات التقادم</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="02281-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-134"><strong>طباعة وصف فترة التأخر</strong></span><span class="sxs-lookup"><span data-stu-id="02281-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-135">حدد <strong>نعم</strong> لتضمين أوصاف فترة التقادم أعلى كل عمود من أعمدة فترة التقادم في التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="02281-136">حدد <strong>لا </strong> لطباعه التقرير بدون رؤوس الاعمده.</span><span class="sxs-lookup"><span data-stu-id="02281-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-137"><strong>الفترة</strong></span><span class="sxs-lookup"><span data-stu-id="02281-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-138">حدد فترة للاستخدام عن طريق إدخال رقم وحدات اليوم أو الشهر في كل فترة.</span><span class="sxs-lookup"><span data-stu-id="02281-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="02281-139">على سبيل المثال، لعرض معلومات التقادم بالأسبوع، أدخل 7 في هذا الحقل وحدد <strong>اليوم</strong> في الحقل <strong>اليوم/الشهر</strong>.</span><span class="sxs-lookup"><span data-stu-id="02281-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="02281-140">**ملاحظة:** يتم استخدام المعلومات التي تقوم بإدخالها في هذا الحقل فقط إذا لم تحدد فترة التقادم.</span><span class="sxs-lookup"><span data-stu-id="02281-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="02281-141">وبخلاف ذلك، يتم تحديد اتجاه الطباعة في تعريف فتره التقادم.</span><span class="sxs-lookup"><span data-stu-id="02281-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-142"><strong>اليوم/الشهر</strong></span><span class="sxs-lookup"><span data-stu-id="02281-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-143">حدد الوحدة، إما أن تكون <strong>اليوم</strong> أو <strong>الشهر</strong>، التي يتم استخدامها لتحديد الفترة في الحقل <strong>الفاصل</strong>.</span><span class="sxs-lookup"><span data-stu-id="02281-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-144"><strong>اتجاه الطباعة</strong></span><span class="sxs-lookup"><span data-stu-id="02281-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-145">حدد ما إذا كان سيتم حساب الارصده وطباعه تقرير فتره التقادم للفترات الماضية أو المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="02281-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="02281-146">يتم تقييم التواريخ بالنسبة إلى التاريخ المحدد في الحقل <strong>الرصيد بداية من</strong>.</span><span class="sxs-lookup"><span data-stu-id="02281-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="02281-147">حدد، بعد ذلك، <strong>للخلف</strong> لعرض معلومات عن الفترات الماضية.</span><span class="sxs-lookup"><span data-stu-id="02281-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="02281-148">وحدد <strong>للأمام</strong> لعرض معلومات عن الفترات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="02281-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="02281-149">
  
<STRONG>ملاحظة:</STRONG> يتم استخدام المعلومات التي تقوم بإدخالها في هذا الحقل فقط إذا لم تحدد فترة التقادم.</span><span class="sxs-lookup"><span data-stu-id="02281-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-150"><strong>تفاصيل</strong></span><span class="sxs-lookup"><span data-stu-id="02281-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-151">حدد لسرد الحركات المضمَّنة في هذه الأرصدة المعروضة في التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-152"><strong>تضمين المبالغ بعملة الحركة</strong></span><span class="sxs-lookup"><span data-stu-id="02281-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-153">حدد هذا الحقل لتضمين المبالغ بعمله الحركة بالاضافه إلى المبالغ الموجودة بعمله المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="02281-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="02281-154">في حاله عدم تحديد خانه الاختيار هذه، يتم عرض المبالغ الموجودة في التقرير فقط بعمله المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="02281-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-155"><strong>رصيد سالب</strong></span><span class="sxs-lookup"><span data-stu-id="02281-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-156">حدد هذا الحقل لتضمين حسابات العملاء التي تشتمل علي ارصده سالبه.</span><span class="sxs-lookup"><span data-stu-id="02281-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02281-157"><strong>استثناء الحسابات ذات الرصيد الصفري</strong></span><span class="sxs-lookup"><span data-stu-id="02281-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-158">حدد لاستثناء حسابات العملاء التي تشتمل علي ارصده صفرية.</span><span class="sxs-lookup"><span data-stu-id="02281-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02281-159"><strong>تحديد موضع عملية الدفع</strong></span><span class="sxs-lookup"><span data-stu-id="02281-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="02281-160">حدد لعرض المدفوعات التي لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="02281-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="02281-161">ويتم عرضها في العمود الأول من التقرير.</span><span class="sxs-lookup"><span data-stu-id="02281-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

