---
title: ملفات تعريف ترحيل المورد
description: تتحكم ملفات تعريف ترحيل المورد‬ في ترحيل حركات المورِّدين إلى دفتر الأستاذ العام.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81f8b472e7ac7578c184716dcb4e5f3d7aeb65d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512158"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="600bf-103">ملفات تعريف ترحيل المورد</span><span class="sxs-lookup"><span data-stu-id="600bf-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="600bf-104">تتحكم ملفات تعريف ترحيل المورد‬ في ترحيل حركات المورِّدين إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="600bf-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="600bf-105">ملفات تعريف ترحيل المورد</span><span class="sxs-lookup"><span data-stu-id="600bf-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="600bf-106">تمكنك ملفات تعريف ترحيل المورد من تعيين حسابات دفتر الأستاذ العام وإعدادات الوثيقة لكافة الموردين أو مجموعة من الموردين أو مورد واحد.</span><span class="sxs-lookup"><span data-stu-id="600bf-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="600bf-107">وسيتم استخدام هذه الإعدادات عندما تقوم بإنشاء أوامر شراء وفواتير الموردين والمدفوعات نقدية.</span><span class="sxs-lookup"><span data-stu-id="600bf-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="600bf-108">وفي بعض الحركات، يمكنك تحديد ملف تعريف ترحيل يختلف عن إعداد ملفات تعريف الترحيل للحركات بهذه الصفحة وله الأسبقية عليه.</span><span class="sxs-lookup"><span data-stu-id="600bf-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="600bf-109">ويتم تحديد ملف تعريف الترحيل الافتراضي في علامة التبويب السريعة دفتر الأستاذ وضريبة المبيعات في صفحة معلمات الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="600bf-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="600bf-110">ويتم بعد ذلك تضمين ملف تعريف الترحيل الافتراضي تلقائياً في رأس المستندات الجديدة، حيث يمكنك تغييره إلى ملف تعريف ترحيل مختلف، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="600bf-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="600bf-111">كما يمكنك إقران تعريفات الترحيل بأنواع ترحيل الحركة في صفحة تعريفات ترحيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="600bf-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="600bf-112">وتتحكم تعريفات الترحيل في ترحيل حركات المورد إلى إلى دفتر الأستاذ العام بدلاً من ملفات تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="600bf-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="600bf-113">إنشاء ملف تعريف ترحيل</span><span class="sxs-lookup"><span data-stu-id="600bf-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="600bf-114">**الإعداد**</span><span class="sxs-lookup"><span data-stu-id="600bf-114">**Setup**</span></span>

<span data-ttu-id="600bf-115">تتيح تحديد حسابات دفتر الأستاذ المستخدمة في ترحيل الحركات التي تستخدم ملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="600bf-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="600bf-116">حدد كود حساب ورقم حساب أو مجموعة، كلما أمكن، لملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="600bf-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="600bf-117">في عملية الترحيل، يتم تحديد موقع ملف التعريف الأكثر ملاءمةً لكل حركة من خلال البحث عن كود الحساب أو رقم الحساب أو مجموعة الحساب والرقم الأكثر تحديدًا بالأولوية التالية:</span><span class="sxs-lookup"><span data-stu-id="600bf-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="600bf-118">قيمة حقل **كود الحساب**</span><span class="sxs-lookup"><span data-stu-id="600bf-118">**Account code** field value</span></span> | <span data-ttu-id="600bf-119">قيمة حقل **رقم الحساب/المجموعة**</span><span class="sxs-lookup"><span data-stu-id="600bf-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="600bf-120">أولوية البحث</span><span class="sxs-lookup"><span data-stu-id="600bf-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="600bf-121">**الجدول**</span><span class="sxs-lookup"><span data-stu-id="600bf-121">**Table**</span></span>                    | <span data-ttu-id="600bf-122">حساب مورد معين</span><span class="sxs-lookup"><span data-stu-id="600bf-122">Specific vendor account</span></span>                     | <span data-ttu-id="600bf-123">1</span><span class="sxs-lookup"><span data-stu-id="600bf-123">1</span></span>               |
| <span data-ttu-id="600bf-124">**مجموعة**</span><span class="sxs-lookup"><span data-stu-id="600bf-124">**Group**</span></span>                    | <span data-ttu-id="600bf-125">مجموعة الموردين التي يتم تعيينها للمورد</span><span class="sxs-lookup"><span data-stu-id="600bf-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="600bf-126">2</span><span class="sxs-lookup"><span data-stu-id="600bf-126">2</span></span>               |
| <span data-ttu-id="600bf-127">**الكل**</span><span class="sxs-lookup"><span data-stu-id="600bf-127">**All**</span></span>                      | <span data-ttu-id="600bf-128">فارغ</span><span class="sxs-lookup"><span data-stu-id="600bf-128">Blank</span></span>                                       | <span data-ttu-id="600bf-129">3</span><span class="sxs-lookup"><span data-stu-id="600bf-129">3</span></span>               |

<span data-ttu-id="600bf-130">إذا كنت ترغب في حصول حركات المورد على نفس ملف تعريف الترحيل، فقم بإعداد ملف تعريف ترحيل واحد فقط مع الكل في حقل كود الحساب.</span><span class="sxs-lookup"><span data-stu-id="600bf-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="600bf-131">وحدد القيم التالية لإعداد ملف تعريف الترحيل الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="600bf-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="600bf-132">الحقل</span><span class="sxs-lookup"><span data-stu-id="600bf-132">Field</span></span></th>
<th><span data-ttu-id="600bf-133">الوصف</span><span class="sxs-lookup"><span data-stu-id="600bf-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="600bf-134"><strong>ملف تعريف الترحيل</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="600bf-135">أدخل كودًا لملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="600bf-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="600bf-136">على سبيل المثال، يمكن إنشاء ملفي تعريف ترحيل للحصول على حساب واحد لأرصدة المورد بالعملة الوطنية وحساب آخر لأرصدة المورد بالعملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="600bf-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="600bf-137">ويمكن أن تطلق على أحدهما اسم "وطني" والآخر "أجنبي".</span><span class="sxs-lookup"><span data-stu-id="600bf-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="600bf-138"><strong>الوصف</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="600bf-139">يتيح إدخال وصف لملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="600bf-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="600bf-140"><strong>كود الحساب</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="600bf-141">حدد ما إذا كان ملف التعريف الترحيل ينطبق على مورد محدد أم مجموعة موردين أو كافة الموردين أم لا:</span><span class="sxs-lookup"><span data-stu-id="600bf-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="600bf-142"><strong>الجدول</strong> – ينطبق ملف تعريف الترحيل على مورد واحد.</span><span class="sxs-lookup"><span data-stu-id="600bf-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="600bf-143">حدد حساب المورد في حقل رقم الحساب/المجموعة.</span><span class="sxs-lookup"><span data-stu-id="600bf-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="600bf-144"><strong>المجموعة</strong> – ينطبق ملف تعريف الترحيل على مجموعة موردين.</span><span class="sxs-lookup"><span data-stu-id="600bf-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="600bf-145">حدد مجموعة الموردين في حقل رقم الحساب/المجموعة.</span><span class="sxs-lookup"><span data-stu-id="600bf-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="600bf-146"><strong>الكل</strong> – ينطبق ملف تعريف الترحيل على كافة الموردين.</span><span class="sxs-lookup"><span data-stu-id="600bf-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="600bf-147">اترك حقل رقم الحساب/المجموعة فارغًا.</span><span class="sxs-lookup"><span data-stu-id="600bf-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="600bf-148"><strong>رقم الحساب/المجموعة</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="600bf-149">في حالة تحديد الجدول في حقل كود الحساب، حدد رقم حساب المورد المرتبط بملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="600bf-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="600bf-150">وفي حالة تحديد مجموعة، حدد مجموعة موردين.</span><span class="sxs-lookup"><span data-stu-id="600bf-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="600bf-151">وفي حالة تحديد الكل، اترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="600bf-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="600bf-152"><strong>حساب ملخص</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="600bf-153">حدد حساب دفتر الأستاذ الذي سيتم استخدامه كحساب الموردين الملخص الذي يرتبط به ملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="600bf-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="عملة ورقية" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="600bf-155"><strong>ملاحظة</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="600bf-156">إذا تم تحديد هيار تبديل استخدام تعريفات ملفات تعريف الترحيل في صفحة معلمات دفتر الأستاذ العام، فإنه يتم استخدام تعريف ترحيل الحركة لفواتير الموردين بدلاً من الحساب الملخص.</span><span class="sxs-lookup"><span data-stu-id="600bf-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="600bf-157"><strong>تسوية الحساب</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="600bf-158">حدد حساب دفتر الأستاذ الخاص بالسيولة المستخدم لتنبؤات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="600bf-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="600bf-159">تتوفر هذه الحقول فقط عندما يتم تمكين التنبؤ بالتدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="600bf-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="600bf-160"><strong>الدفعات المقدمة لضريبة المبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="600bf-161">حدد حساب لضريبة المبيعات للمدفوعات التي يتم استلامها مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="600bf-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="عملة ورقية" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="600bf-163"><strong>ملاحظة</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="600bf-164">يتم تحديد ملف تعريف الترحيل المستخدم عند وضع علامة على الدفعة كدفعة مقدمة بملف تعريف الترحيل في حقل إيصال دفتر يومية الدفعة المقدمة في منطقة دفتر الأستاذ وضريبة المبيعات في صفحة معلمات الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="600bf-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="600bf-165"><strong>الوصول</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="600bf-166">حدد رقم حساب دفتر الأستاذ الذي يتم ترحيل معلومات حول فواتير المورد غير المعتمدة إليه.</span><span class="sxs-lookup"><span data-stu-id="600bf-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="600bf-167">ويتم إدخال المعلومات في دفتر يومية سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="600bf-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="600bf-168">على سبيل المثال، يقوم مستخدم بإدخال معلومات أساسية للغاية حول فواتير المورد عند استلامها في سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="600bf-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="600bf-169">وعند ترحيل سجل الفواتير، يتم ترحيل الحركات إلى الحساب الذي يتم إدخاله هنا في حقل الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="600bf-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="600bf-170">وعند اعتماد الفواتير، يتم تحويل الدين من حساب الوصول إلى حساب ملخص المورد.</span><span class="sxs-lookup"><span data-stu-id="600bf-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="600bf-171"><strong>الحساب المقابل</strong></span><span class="sxs-lookup"><span data-stu-id="600bf-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="600bf-172">حدد حساب دفتر الأستاذ المستخدم لمقابلة فواتير المورد غير المعتمدة التي يتم تحديثها من خلال استخدام سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="600bf-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="600bf-173">ويعمل الحساب المقابل كحساب مقابل للحركات التي تم ترحيلها إلى حسابات الوصول.</span><span class="sxs-lookup"><span data-stu-id="600bf-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="600bf-174">ولذلك، يحتوي الحساب على مشتريات الموردين التي لم يتم اعتمادها بعد.</span><span class="sxs-lookup"><span data-stu-id="600bf-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="600bf-175">**تقييدات الجداول**</span><span class="sxs-lookup"><span data-stu-id="600bf-175">**Table restrictions**</span></span>

<span data-ttu-id="600bf-176">في اللحركات التي تحتوي على ملف تعريف الترحيل المحدد، حدد ما إذا كان ستتم تسوية الحركات تلقائياً، وسيتم حساب الفائدة، وسيتم إصدار خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="600bf-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="600bf-177">كما يمكنك تحديد الحساب الذي يُستخدم عند إغلاق الحركات المشتملة على ملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="600bf-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="600bf-178">وحدد القيم التالية لإعداد ملف تعريف الترحيل الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="600bf-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="600bf-179">الحقل</span><span class="sxs-lookup"><span data-stu-id="600bf-179">Field</span></span>          | <span data-ttu-id="600bf-180">الوصف</span><span class="sxs-lookup"><span data-stu-id="600bf-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600bf-181">**التسوية**</span><span class="sxs-lookup"><span data-stu-id="600bf-181">**Settlement**</span></span> | <span data-ttu-id="600bf-182">حدد هذا الخيار لتمكين التسوية التلقائية للحركات التي تتضمن ملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="600bf-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="600bf-183">وإذا تم إلغاء تحديد هذا الخيار، يجب يدوياً تسوية الحركات باستخدام صفحة تسوية الحركات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="600bf-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="600bf-184">**إلغاء**</span><span class="sxs-lookup"><span data-stu-id="600bf-184">**Cancel**</span></span>     | <span data-ttu-id="600bf-185">حدد هذا الخيار إذا أردت التمكن من إلغاء الحركات التي تتضمن ملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="600bf-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="600bf-186">**إغلاق**</span><span class="sxs-lookup"><span data-stu-id="600bf-186">**Close**</span></span>      | <span data-ttu-id="600bf-187">حدد ملف تعريف ترحيل للتغيير إليه عند إغلاق الحركات بملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="600bf-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="600bf-188">ويتم اعتبار الحركة مغلقة عند تسويتها بالكامل.</span><span class="sxs-lookup"><span data-stu-id="600bf-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |





