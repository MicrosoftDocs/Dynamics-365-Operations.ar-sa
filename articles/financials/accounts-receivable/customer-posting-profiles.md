---
title: "ملفات تعريف ترحيل العميل"
description: "تتحكم ملفات تعريف ترحيل العميل‬ في ترحيل حركات العميل إلى دفتر الأستاذ العام."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: d0795a9cb1839c45cf264b0d0f7cffacdc01ea9d
ms.contentlocale: ar-sa
ms.lasthandoff: 02/23/2018

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="5b17a-103">ملفات تعريف ترحيل العميل</span><span class="sxs-lookup"><span data-stu-id="5b17a-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5b17a-104">تتحكم ملفات تعريف ترحيل العميل‬ في ترحيل حركات العميل إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="5b17a-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="5b17a-105">ملفات تعريف ترحيل العميل</span><span class="sxs-lookup"><span data-stu-id="5b17a-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="5b17a-106">تمكنك ملفات تعريف ترحيل العميل من تعيين حسابات دفتر الأستاذ العام وإعدادات الوثيقة لكافة العملاء أو مجموعة من العملاء أو عميل واحد.</span><span class="sxs-lookup"><span data-stu-id="5b17a-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="5b17a-107">سيتم استخدام هذه الإعدادات عند إنشاء أوامر المبيعات، وفواتير النص الحر، والمدفوعات النقدية، وخطابات التحصيل، وإشعارات الفائدة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="5b17a-108">وفي بعض الحركات، يمكنك تحديد ملف تعريف ترحيل يختلف عن إعداد ملفات تعريف الترحيل للحركات بهذه الصفحة وله الأسبقية عليه.</span><span class="sxs-lookup"><span data-stu-id="5b17a-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="5b17a-109">ويتم تحديد ملف تعريف الترحيل الافتراضي في علامة التبويب السريعة دفتر الأستاذ وضريبة المبيعات في صفحة معلمات الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="5b17a-110">ويتم بعد ذلك تضمين ملف تعريف الترحيل الافتراضي تلقائياً في رأس المستندات الجديدة، حيث يمكنك تغييره إلى ملف تعريف ترحيل مختلف، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="5b17a-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="5b17a-111">كما يمكنك إقران تعريفات الترحيل بأنواع ترحيل الحركة في صفحة تعريفات ترحيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="5b17a-112">وتتحكم تعريفات الترحيل في ترحيل حركات العميل إلى إلى دفتر الأستاذ العام بدلاً من ملفات تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="5b17a-113">إنشاء ملف تعريف ترحيل</span><span class="sxs-lookup"><span data-stu-id="5b17a-113">Creating a posting profile</span></span>
<span data-ttu-id="5b17a-114">تتيح تحديد حسابات دفتر الأستاذ المستخدمة في ترحيل الحركات التي تستخدم ملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="5b17a-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="5b17a-115">حدد كود حساب ورقم حساب أو مجموعة، كلما أمكن، لملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="5b17a-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="5b17a-116">في عملية الترحيل، يتم تحديد موقع ملف التعريف الأكثر ملاءمةً لكل حركة من خلال البحث عن كود الحساب أو رقم الحساب أو مجموعة الحساب والرقم الأكثر تحديدًا بالأولوية التالية:</span><span class="sxs-lookup"><span data-stu-id="5b17a-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="5b17a-117">قيمة حقل **كود الحساب**</span><span class="sxs-lookup"><span data-stu-id="5b17a-117">**Account code** field value</span></span> | <span data-ttu-id="5b17a-118">قيمة حقل **رقم الحساب/المجموعة**</span><span class="sxs-lookup"><span data-stu-id="5b17a-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="5b17a-119">أولوية البحث</span><span class="sxs-lookup"><span data-stu-id="5b17a-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="5b17a-120">**الجدول**</span><span class="sxs-lookup"><span data-stu-id="5b17a-120">**Table**</span></span>                    | <span data-ttu-id="5b17a-121">حساب العميل المحدد</span><span class="sxs-lookup"><span data-stu-id="5b17a-121">Specific customer account</span></span>                       | <span data-ttu-id="5b17a-122">1</span><span class="sxs-lookup"><span data-stu-id="5b17a-122">1</span></span>               |
| <span data-ttu-id="5b17a-123">**مجموعة**</span><span class="sxs-lookup"><span data-stu-id="5b17a-123">**Group**</span></span>                    | <span data-ttu-id="5b17a-124">مجموعة العملاء التي تم تعيينها للعميل</span><span class="sxs-lookup"><span data-stu-id="5b17a-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="5b17a-125">2</span><span class="sxs-lookup"><span data-stu-id="5b17a-125">2</span></span>               |
| <span data-ttu-id="5b17a-126">**الكل**</span><span class="sxs-lookup"><span data-stu-id="5b17a-126">**All**</span></span>                      | <span data-ttu-id="5b17a-127">فارغ</span><span class="sxs-lookup"><span data-stu-id="5b17a-127">Blank</span></span>                                           | <span data-ttu-id="5b17a-128">3</span><span class="sxs-lookup"><span data-stu-id="5b17a-128">3</span></span>               |

<span data-ttu-id="5b17a-129">إذا كنت ترغب في حصول حركات العميل على نفس ملف تعريف الترحيل، فقم بإعداد ملف تعريف ترحيل واحد فقط مع الكل في حقل كود الحساب.</span><span class="sxs-lookup"><span data-stu-id="5b17a-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="5b17a-130">وحدد القيم التالية لإعداد ملف تعريف الترحيل الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="5b17a-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b17a-131">الحقل</span><span class="sxs-lookup"><span data-stu-id="5b17a-131">Field</span></span></th>
<th><span data-ttu-id="5b17a-132">الوصف</span><span class="sxs-lookup"><span data-stu-id="5b17a-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b17a-133"><strong>ملف تعريف الترحيل</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="5b17a-134">أدخل كودًا لملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="5b17a-135">على سبيل المثال، يمكن إنشاء ملفي تعريف ترحيل للحصول على حساب واحد لأرصدة العميل بالعملة الوطنية وحساب آخر لأرصدة العميل بالعملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="5b17a-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="5b17a-136">ويمكن أن تطلق على أحدهما اسم "وطني" والآخر "أجنبي".</span><span class="sxs-lookup"><span data-stu-id="5b17a-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17a-137"><strong>الوصف</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="5b17a-138">يتيح إدخال وصف لملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="5b17a-139">هذا يُستخدم فقط لتحسين تحديد ملف تعريف الترحيل عند عرضه في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b17a-140"><strong>كود الحساب</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="5b17a-141">حدد ما إذا كان ملف تعريف الترحيل ينطبق على عميل واحد أو مجموعة عملاء أو جميع العملاء أم لا:</span><span class="sxs-lookup"><span data-stu-id="5b17a-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="5b17a-142"><strong>الجدول</strong> – ينطبق ملف تعريف الترحيل على عميل واحد.</span><span class="sxs-lookup"><span data-stu-id="5b17a-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="5b17a-143">حدد حساب العميل في حقل رقم الحساب/المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="5b17a-144"><strong>المجموعة</strong> – ينطبق ملف تعريف الترحيل على مجموعة عملاء.</span><span class="sxs-lookup"><span data-stu-id="5b17a-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="5b17a-145">حدد مجموعة العملاء في حقل رقم الحساب/المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="5b17a-146"><strong>الكل</strong> – ينطبق ملف تعريف الترحيل على كافة العملاء.</span><span class="sxs-lookup"><span data-stu-id="5b17a-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="5b17a-147">اترك حقل رقم الحساب/المجموعة فارغًا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17a-148"><strong>رقم الحساب/المجموعة</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="5b17a-149">في حالة تحديد الجدول في حقل كود الحساب، حدد رقم حساب العميل المرتبط بملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="5b17a-150">وإذا قمت بتحديد مجموعة، فقم بتحديد مجموعة العملاء.</span><span class="sxs-lookup"><span data-stu-id="5b17a-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="5b17a-151">وفي حالة تحديد الكل، اترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b17a-152"><strong>حساب ملخص</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="5b17a-153">حدد حساب دفتر الأستاذ الذي سيتم استخدامه كحساب العميل الملخص للعملاء المرتبطين بملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17a-154"><strong>تسوية الحساب</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="5b17a-155">حدد حساب دفتر الأستاذ الخاص بالسيولة المستخدم لتنبؤات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="5b17a-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="5b17a-156">سيظهر هذا الحقل فقط إذا تم تمكين تنبؤات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="5b17a-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b17a-157"><strong>الدفعات المقدمة لضريبة المبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="5b17a-158">حدد حساب لضريبة المبيعات للمدفوعات التي يتم استلامها مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b17a-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="ملاحظة</span><span class="sxs-lookup"><span data-stu-id="5b17a-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="5b17a-160"><strong>ملاحظة</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b17a-161">استخدم صفحة معلمات الحسابات المدينة لتحديد ملف تعريف الترحيل المطلوب استخدامه عند وضع علامة على دفعة كدفعة مقدمة.</span><span class="sxs-lookup"><span data-stu-id="5b17a-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17a-162"><strong>التزامات حساب الخصم</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="5b17a-163">حدد حساب دفتر الأستاذ الخاص بالتزامات الخصم.</span><span class="sxs-lookup"><span data-stu-id="5b17a-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b17a-164"><strong>تسلسل خطاب التحصيل</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="5b17a-165">حدد معرف تسلسل خطابات التحصيل لاستخدامه للعملاء الذين تم تعيين ملف تعريف الترحيل لهم.</span><span class="sxs-lookup"><span data-stu-id="5b17a-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17a-166"><strong>كود الفائدة</strong></span><span class="sxs-lookup"><span data-stu-id="5b17a-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="5b17a-167">حدد كود الفائدة لاستخدامه لحساب الفائدة للعملاء الذين تم تعيين ملف تعريف الترحيل لهم.</span><span class="sxs-lookup"><span data-stu-id="5b17a-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="5b17a-168">**تقييدات الجداول**</span><span class="sxs-lookup"><span data-stu-id="5b17a-168">**Table restrictions**</span></span>

<span data-ttu-id="5b17a-169">في اللحركات التي تحتوي على ملف تعريف الترحيل المحدد، حدد ما إذا كان ستتم تسوية الحركات تلقائياً، وسيتم حساب الفائدة، وسيتم إصدار خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="5b17a-170">كما يمكنك تحديد الحساب الذي يُستخدم عند إغلاق الحركات المشتملة على ملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="5b17a-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="5b17a-171">وحدد القيم التالية لإعداد ملف تعريف الترحيل الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="5b17a-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="5b17a-172">الحقل</span><span class="sxs-lookup"><span data-stu-id="5b17a-172">Field</span></span>                 | <span data-ttu-id="5b17a-173">الوصف</span><span class="sxs-lookup"><span data-stu-id="5b17a-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b17a-174">**التسوية**</span><span class="sxs-lookup"><span data-stu-id="5b17a-174">**Settlement**</span></span>        | <span data-ttu-id="5b17a-175">حدد هذا التبديل لتمكين التسوية التلقائية للحركات التي تتضمن ملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="5b17a-176">وإذا تم مسح هذا التبديل، يجب يدوياً تسوية الحركات باستخدام صفحة تسوية الحركات المفتوحة أو صفحة إدخال مدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="5b17a-177">**الفائدة**</span><span class="sxs-lookup"><span data-stu-id="5b17a-177">**Interest**</span></span>          | <span data-ttu-id="5b17a-178">حدد هذا التبديل إذا كان يجب حساب الفائدة في الأرصدة المعلقة لحسابات العملاء التي تستخدم ملف التعريف هذا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="5b17a-179">وفي حالة إلغاء تحديد هذا التبديل، فلن يتم حساب الفائدة لهؤلاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="5b17a-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="5b17a-180">**خطاب التحصيل**</span><span class="sxs-lookup"><span data-stu-id="5b17a-180">**Collection letter**</span></span> | <span data-ttu-id="5b17a-181">حدد هذا التبديل إذا كان يجب إنشاء هطابات التحصيل لحسابات العملاء التي تستخدم ملف التعريف هذا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="5b17a-182">وفي حالة إلغاء تحديد هذا التبديل، لن يتم إنشاء خطابات التحصيل لهؤلاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="5b17a-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="5b17a-183">**إغلاق**</span><span class="sxs-lookup"><span data-stu-id="5b17a-183">**Close**</span></span>             | <span data-ttu-id="5b17a-184">حدد ملف تعريف ترحيل للتغيير إليه عند إغلاق الحركات بملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="5b17a-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="5b17a-185">ويتم اعتبار الحركة مغلقة عند تسويتها بالكامل.</span><span class="sxs-lookup"><span data-stu-id="5b17a-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="5b17a-186">للحصول على مزيد من المعلومات، راجع [نظرة عامة على دفع العميل‬](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b17a-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


