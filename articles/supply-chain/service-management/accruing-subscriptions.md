---
title: الاشتراكات المستحقة
description: باستخدام اشتراكات الخدمة، يمكنك استحقاق الإيراد في الفترات التالية بتاريخ فوترة حركة الرسوم.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ebd65655db56ee1169f24dbc79fbfb5130f06a5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978811"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="2115a-103">الاشتراكات المستحقة</span><span class="sxs-lookup"><span data-stu-id="2115a-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2115a-104">باستخدام اشتراكات الخدمة، يمكنك استحقاق الإيراد في الفترات التالية بتاريخ فوترة حركة الرسوم.</span><span class="sxs-lookup"><span data-stu-id="2115a-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="2115a-105">يتم إنشاء فترات الاستحقاق لفترة الفاتورة التي قمت بإعدادها لرسوم الاشتراك، وتستند فترات الاستحقاق إلى كود فترة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="2115a-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="2115a-106">يمكنك استحقاق الإيراد المستحق وعكسه.</span><span class="sxs-lookup"><span data-stu-id="2115a-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="2115a-107">إلغاء الاستحقاقات للمبالغ الدائنة</span><span class="sxs-lookup"><span data-stu-id="2115a-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="2115a-108">إذا استدنت مبالغ اشتراك مفوترة، فيمكنك استخدام طريقتين لإلغاء مبالغ الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="2115a-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="2115a-109">يمكنك إلغاء كل حركة إيراد مستحق بشكل فردي قبل إنشاء مقترح إشعار دائن للحركة.</span><span class="sxs-lookup"><span data-stu-id="2115a-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="2115a-110">تعد هذه هي الطريقة اليدوية.</span><span class="sxs-lookup"><span data-stu-id="2115a-110">This is the manual method.</span></span> <span data-ttu-id="2115a-111">(يدوي)</span><span class="sxs-lookup"><span data-stu-id="2115a-111">(manual)</span></span>

  - <span data-ttu-id="2115a-112">يمكنك أن تلغي المبالغ المستحقة في التاريخ التي يتم فيه ترحيل إشعار الدائن أو تاريخ الترحيل الأصلي للاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="2115a-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="2115a-113">لمزيد من المعلومات، راجع [محددات الاشتراك (نموذج)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="2115a-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="2115a-114">متطلبات الإعداد</span><span class="sxs-lookup"><span data-stu-id="2115a-114">Setup requirements</span></span>

<span data-ttu-id="2115a-115">لاستحقاق الإيراد، تأكد من تلبية متطلبات البيانات التالية.</span><span class="sxs-lookup"><span data-stu-id="2115a-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="2115a-116">إعداد الحساب</span><span class="sxs-lookup"><span data-stu-id="2115a-116">Account setup</span></span>

<span data-ttu-id="2115a-117">يجب إعداد حسابات **الأعمال تحت التنفيذ-الاشتراك** و **إيراد مستحق-الاشتراك** في وحدة **المشروع** .</span><span class="sxs-lookup"><span data-stu-id="2115a-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="2115a-118">عندما ترحل إيرادًا مستحقًا، يتم خصم المبلغ المستحق من حساب **الأعمال تحت التنفيذ - الاشتراك** وخصم المبلغ الفعلي من حساب **إيراد مستحق - الاشتراك** .</span><span class="sxs-lookup"><span data-stu-id="2115a-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="2115a-119">إعداد حسابات لاستحقاق إيراد الاشتراك</span><span class="sxs-lookup"><span data-stu-id="2115a-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="2115a-120">انقر فوق **إدارة المشروع‬ والمحاسبة** \> **إعداد** \> **ترحيل** \> **إعداد ترحيل دفتر الأستاذ** .</span><span class="sxs-lookup"><span data-stu-id="2115a-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup** .</span></span>

2.  <span data-ttu-id="2115a-121">انقر فوق علامة تبويب **حسابات الإيراد** ، ثم حدد **الأعمال تحت التنفيذ - الاشتراك** أو **إيراد مستحق - الاشتراك** لإعداد الحسابات.</span><span class="sxs-lookup"><span data-stu-id="2115a-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="2115a-122">إعداد مجموعة الاشتراك</span><span class="sxs-lookup"><span data-stu-id="2115a-122">Subscription group setup</span></span>

<span data-ttu-id="2115a-123">لكي تتمكن من استحقاق الإيراد للاشتراكات، يجب تحديد خانة الاختيار **الإيراد المستحق** .</span><span class="sxs-lookup"><span data-stu-id="2115a-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="2115a-124">هي موجودة في نموذج **مجموعات المشتركين** للمجموعة التي يرتبط بها الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="2115a-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="2115a-125">انقر فوق **إدارة الخدمة** \> **إعداد** \> **اشتراكات الخدمة** \> **مجموعات الاشتراك** .</span><span class="sxs-lookup"><span data-stu-id="2115a-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups** .</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="2115a-126">تمكين استحقاق الإيراد لمجموعة الاشتراك</span><span class="sxs-lookup"><span data-stu-id="2115a-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="2115a-127">انقر فوق **إدارة الخدمة** \> **إعداد** \> **اشتراكات الخدمة** \> **مجموعات الاشتراك** .</span><span class="sxs-lookup"><span data-stu-id="2115a-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups** .</span></span>

## <a name="periods"></a><span data-ttu-id="2115a-128">الفترات</span><span class="sxs-lookup"><span data-stu-id="2115a-128">Periods</span></span>

<span data-ttu-id="2115a-129">يجب إعداد كود فترة الفوترة.</span><span class="sxs-lookup"><span data-stu-id="2115a-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="2115a-130">وما لم ترغب في استحقاق الإيراد في نفس الفترات الزمنية مثل استخدام الفوترة، فيجب أيضًا إعداد فترة الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="2115a-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="2115a-131">يوفر الجدول التالي نظرة عامة حول فترات الاستحقاق التي يمكن إعدادها لكل فترة فوترة:</span><span class="sxs-lookup"><span data-stu-id="2115a-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2115a-132">فترة الفوترة</span><span class="sxs-lookup"><span data-stu-id="2115a-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="2115a-133">فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="2115a-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2115a-134"><strong>السنوات</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2115a-135"><strong>السنوات</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="2115a-136"><strong>ربع السنة</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="2115a-137"><strong>الشهر</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="2115a-138"><strong>اليوم</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2115a-139"><strong>ربع السنة</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2115a-140"><strong>ربع السنة</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="2115a-141"><strong>الشهر</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="2115a-142"><strong>اليوم</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2115a-143"><strong>الشهر</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2115a-144"><strong>الشهر</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="2115a-145"><strong>اليوم</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2115a-146"><strong>أسبوعيًا</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2115a-147"><strong>اليوم</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2115a-148"><strong>اليوم</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2115a-149"><strong>اليوم</strong></span><span class="sxs-lookup"><span data-stu-id="2115a-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2115a-150">يعد إعداد فترة الفوترة جزء إلزامياً في إعداد مجموعة الاشتراك الكلي.</span><span class="sxs-lookup"><span data-stu-id="2115a-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="2115a-151">يمكنك أن تقرر ما إذا كان يجب أيضا إعداد فترة استحقاق لمجموعة المشتركين أم لا.</span><span class="sxs-lookup"><span data-stu-id="2115a-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="2115a-152">إذا قمت بإعداد فترة استحقاق لمجموعة الاشتراك، فسيتم اقتراح هذه الفترة في الحقل **كود الفترة** .</span><span class="sxs-lookup"><span data-stu-id="2115a-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="2115a-153">يوجد هذا الحقل في نموذج **إيراد اشتراك مستحق** ، عند استحقاق إيراد اشتراك.</span><span class="sxs-lookup"><span data-stu-id="2115a-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="2115a-154">ومن ناحية أخرى، فإن فترة الاستحقاق هي معلومات اختيارية لمجموعة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="2115a-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2115a-155">استخدام المسار التالي لفتح النموذج <STRONG>إيراد اشتراك مستحق</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2115a-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="2115a-156">انقر فوق <STRONG>إدارة الخدمة</STRONG> &gt; <STRONG>دوري</STRONG> &gt; <STRONG>اشتراكات الخدمة</STRONG> &gt; <STRONG>إيراد اشتراك مستحق</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2115a-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="2115a-157">الحركات</span><span class="sxs-lookup"><span data-stu-id="2115a-157">Transactions</span></span>

<span data-ttu-id="2115a-158">يمكنك التحكم في عدد حركات دفتر الأستاذ التي تم إنشاؤها عند ترحيل الإيراد المستحق.</span><span class="sxs-lookup"><span data-stu-id="2115a-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="2115a-159">في عمليات الاشتراك، حدد ما إذا كان يجب إنشاء حركات دفتر الأستاذ بصورة إجمالية أم لكل سطر.</span><span class="sxs-lookup"><span data-stu-id="2115a-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="2115a-160">تحديد مستوى تفاصيل الترحيل لعرض الحركات المستحقة</span><span class="sxs-lookup"><span data-stu-id="2115a-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="2115a-161">انقر فوق **إدارة المشاريع‬ والمحاسبة** \> **الإعدادات** \> **محددات إدارة المشاريع‬ والمحاسبة** .</span><span class="sxs-lookup"><span data-stu-id="2115a-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters** .</span></span>

2.  <span data-ttu-id="2115a-162">في علامة تبويب **مالي** ، في حقل **فاتورة** ، حدد **إجمالي** أو **سطر** .</span><span class="sxs-lookup"><span data-stu-id="2115a-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line** .</span></span>


## <a name="see-also"></a><span data-ttu-id="2115a-163">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="2115a-163">See also</span></span>

[<span data-ttu-id="2115a-164">إيراد اشتراك مستحق</span><span class="sxs-lookup"><span data-stu-id="2115a-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


