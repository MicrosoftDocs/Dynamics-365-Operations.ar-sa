---
title: ملفات تعريف ترحيل المورد
description: تتحكم ملفات تعريف ترحيل المورد‬ في ترحيل حركات المورِّدين إلى دفتر الأستاذ العام.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37fb7d2623451313475a6c234e820c7c6295be40
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835474"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="c6ad5-103">ملفات تعريف ترحيل المورد</span><span class="sxs-lookup"><span data-stu-id="c6ad5-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6ad5-104">تتحكم ملفات تعريف ترحيل المورد‬ في ترحيل حركات المورِّدين إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="c6ad5-105">ملفات تعريف ترحيل المورد</span><span class="sxs-lookup"><span data-stu-id="c6ad5-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="c6ad5-106">تمكنك ملفات تعريف ترحيل المورد من تعيين حسابات دفتر الأستاذ العام وإعدادات الوثيقة لكل الموردين أو مجموعة من الموردين أو مورد واحد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="c6ad5-107">وسيتم استخدام هذه الإعدادات عندما تقوم بإنشاء أوامر شراء وفواتير الموردين والمدفوعات النقدية.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="c6ad5-108">ويمكنك في بعض الحركات تحديد ملف تعريف ترحيل يختلف عن إعداد ملفات تعريف الترحيل للحركات بهذه الصفحة وله الأسبقية عليه.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="c6ad5-109">ويتم تحديد ملف تعريف الترحيل الافتراضي في علامة التبويب السريعة **دفتر الأستاذ وضريبة المبيعات** في صفحة **معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="c6ad5-110">يتم بعد ذلك تضمين ملف تعريف الترحيل الافتراضي تلقائيًا في رأس المستندات الجديدة، حيث يمكنك تغييره إلى ملف تعريف ترحيل مختلف، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="c6ad5-111">كما يمكنك إقران تعريفات الترحيل بأنواع ترحيل الحركة في صفحة **تعريفات ترحيل الحركة**.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="c6ad5-112">وتتحكم تعريفات الترحيل في ترحيل حركات المورد إلى إلى دفتر الأستاذ العام بدلاً من ملفات تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="c6ad5-113">إنشاء ملف تعريف ترحيل</span><span class="sxs-lookup"><span data-stu-id="c6ad5-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="c6ad5-114">**الإعداد**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-114">**Setup**</span></span>

<span data-ttu-id="c6ad5-115">تتيح تحديد حسابات دفتر الأستاذ المستخدمة في ترحيل الحركات التي تستخدم ملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="c6ad5-116">حدد كود حساب ورقم حساب أو مجموعة، كلما أمكن، لملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="c6ad5-117">في عملية الترحيل، يتم تحديد موقع ملف التعريف الأكثر ملاءمة لكل حركة من خلال البحث عن كود الحساب أو رقم الحساب أو مجموعة الحساب ومجموعة الأرقام الأكثر تحديدًا بالأولوية التالية.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="c6ad5-118">قيمة حقل **كود الحساب**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-118">**Account code** field value</span></span> | <span data-ttu-id="c6ad5-119">قيمة حقل **رقم الحساب/المجموعة**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="c6ad5-120">أولوية البحث</span><span class="sxs-lookup"><span data-stu-id="c6ad5-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="c6ad5-121">**الجدول**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-121">**Table**</span></span>                    | <span data-ttu-id="c6ad5-122">حساب مورد معين</span><span class="sxs-lookup"><span data-stu-id="c6ad5-122">Specific vendor account</span></span>                     | <span data-ttu-id="c6ad5-123">1</span><span class="sxs-lookup"><span data-stu-id="c6ad5-123">1</span></span>               |
| <span data-ttu-id="c6ad5-124">**مجموعة**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-124">**Group**</span></span>                    | <span data-ttu-id="c6ad5-125">مجموعة الموردين التي يتم تعيينها للمورد</span><span class="sxs-lookup"><span data-stu-id="c6ad5-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="c6ad5-126">2</span><span class="sxs-lookup"><span data-stu-id="c6ad5-126">2</span></span>               |
| <span data-ttu-id="c6ad5-127">**الكل**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-127">**All**</span></span>                      | <span data-ttu-id="c6ad5-128">فارغ</span><span class="sxs-lookup"><span data-stu-id="c6ad5-128">Blank</span></span>                                       | <span data-ttu-id="c6ad5-129">3</span><span class="sxs-lookup"><span data-stu-id="c6ad5-129">3</span></span>               |

<span data-ttu-id="c6ad5-130">إذا كنت ترغب في حصول حركات المورد على نفس ملف تعريف الترحيل، فقم بإعداد ملف تعريف ترحيل واحد فقط مع **الكل** في حقل **كود الحساب**.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="c6ad5-131">وحدد القيم التالية لإعداد ملف تعريف الترحيل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c6ad5-132">الحقل</span><span class="sxs-lookup"><span data-stu-id="c6ad5-132">Field</span></span></th>
<th><span data-ttu-id="c6ad5-133">الوصف</span><span class="sxs-lookup"><span data-stu-id="c6ad5-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6ad5-134"><strong>ملف تعريف الترحيل</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="c6ad5-135">أدخل كودًا لملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="c6ad5-136">على سبيل المثال، يمكن إنشاء ملفي تعريف ترحيل للحصول على حساب واحد لأرصدة المورد بالعملة الوطنية وحساب آخر لأرصدة المورد بالعملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="c6ad5-137">ويمكن أن تطلق على أحدهما اسم "وطني" والآخر "أجنبي".</span><span class="sxs-lookup"><span data-stu-id="c6ad5-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6ad5-138"><strong>الوصف</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="c6ad5-139">يتيح إدخال وصف لملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6ad5-140"><strong>كود الحساب</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="c6ad5-141">حدد ما إذا كان ملف التعريف الترحيل ينطبق على مورد محدد أم مجموعة موردين أو كافة الموردين أم لا:</span><span class="sxs-lookup"><span data-stu-id="c6ad5-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="c6ad5-142"><strong>الجدول</strong> – ينطبق ملف تعريف الترحيل على مورد واحد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="c6ad5-143">حدد حساب المورد في حقل <strong>رقم الحساب/المجموعة</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="c6ad5-144"><strong>المجموعة</strong> – ينطبق ملف تعريف الترحيل على مجموعة موردين.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="c6ad5-145">حدد مجموعة الموردين في حقل <strong>رقم الحساب/المجموعة</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="c6ad5-146"><strong>الكل</strong> – ينطبق ملف تعريف الترحيل على كافة الموردين.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="c6ad5-147">اترك حقل <strong>رقم الحساب/المجموعة</strong> فارغًا.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6ad5-148"><strong>رقم الحساب/المجموعة</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="c6ad5-149">في حالة تحديد <strong>الجدول</strong> في حقل <strong>كود الحساب</strong>، حدد رقم حساب المورد المرتبط بملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="c6ad5-150">وفي حالة تحديد <strong>مجموعة</strong>، حدد مجموعة موردين.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="c6ad5-151">وفي حالة تحديد <strong>الكل</strong>، اترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6ad5-152"><strong>حساب ملخص</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="c6ad5-153">حدد حساب دفتر الأستاذ الذي سيتم استخدامه كحساب الموردين الملخص الذي يرتبط به ملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="c6ad5-154">سيتم وضع علامة على <strong>‏‫عدم السماح بالإدخال اليدوي</strong> لهذا الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="c6ad5-155">إذا قمت فيما بعد بإزالة هذا الحساب من ملف تعريف الترحيل، فلتحقق من صحة إعداد <strong>عدم السماح بالإدخال اليدوي</strong>في صفحة <strong>الحسابات الرئيسية </strong>.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="c6ad5-156"><strong>ملاحظة:</strong> إذا تم تحديد خيار <strong>استخدام تعريفات الترحيل</strong> في صفحة <strong>معلمات دفتر الأستاذ العام</strong>، فإنه يتم استخدام تعريف ترحيل الحركة لفواتير الموردين بدلاً من الحساب الملخص.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6ad5-157"><strong>تسوية الحساب</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="c6ad5-158">حدد حساب دفتر الأستاذ الخاص بالسيولة المستخدم لتنبؤات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="c6ad5-159">تتوفر هذه الحقول فقط عندما يتم تمكين التنبؤ بالتدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6ad5-160"><strong>الدفعات المقدمة لضريبة المبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="c6ad5-161">حدد حساب لضريبة المبيعات للمدفوعات التي يتم استلامها مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="c6ad5-162"><strong>ملاحظة:</strong> يتم تحديد ملف تعريف الترحيل المستخدم عند وضع علامة على الدفعة كدفعة مقدمة بملف تعريف <strong>الترحيل</strong> في حقل <strong>إيصال دفتر يومية الدفعة المقدمة</strong> في منطقة <strong>دفتر الأستاذ وضريبة المبيعات</strong> في صفحة <strong>معلمات الحسابات الدائنة</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6ad5-163"><strong>الوصول</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="c6ad5-164">حدد رقم حساب دفتر الأستاذ الذي يتم ترحيل معلومات حول فواتير المورد غير المعتمدة إليه.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="c6ad5-165">ويتم إدخال المعلومات في دفتر يومية سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="c6ad5-166">على سبيل المثال، يقوم مستخدم بإدخال معلومات أساسية للغاية حول فواتير المورد عند استلامها في سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="c6ad5-167">وعند ترحيل سجل الفواتير، يتم ترحيل الحركات إلى الحساب الذي يتم إدخاله هنا في حقل <strong>الحساب المقابل</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="c6ad5-168">وعند اعتماد الفواتير، يتم تحويل الدين من حساب الوصول إلى حساب ملخص المورد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6ad5-169"><strong>الحساب المقابل</strong></span><span class="sxs-lookup"><span data-stu-id="c6ad5-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="c6ad5-170">حدد حساب دفتر الأستاذ المستخدم لمقابلة فواتير المورد غير المعتمدة التي يتم تحديثها من خلال استخدام سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="c6ad5-171">ويعمل الحساب المقابل كحساب مقابل للحركات التي تم ترحيلها إلى حسابات الوصول.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="c6ad5-172">ولذلك، يحتوي الحساب على مشتريات الموردين التي لم يتم اعتمادها بعد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="c6ad5-173">**تقييدات الجداول**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-173">**Table restrictions**</span></span>

<span data-ttu-id="c6ad5-174">في اللحركات التي تحتوي على ملف تعريف الترحيل المحدد، حدد ما إذا كان ستتم تسوية الحركات تلقائياً، وسيتم حساب الفائدة، وسيتم إصدار خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="c6ad5-175">كما يمكنك تحديد الحساب الذي يُستخدم عند إغلاق الحركات المشتملة على ملف تعريف الترحيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="c6ad5-176">حدد القيم التالية لإعداد ملف تعريف الترحيل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="c6ad5-177">الحقل</span><span class="sxs-lookup"><span data-stu-id="c6ad5-177">Field</span></span>          | <span data-ttu-id="c6ad5-178">الوصف</span><span class="sxs-lookup"><span data-stu-id="c6ad5-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ad5-179">**التسوية**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-179">**Settlement**</span></span> | <span data-ttu-id="c6ad5-180">حدد هذا الخيار لتمكين التسوية التلقائية للحركات التي تتضمن ملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="c6ad5-181">في حالة إلغاء تحديد هذا الخيار، يجب تسوية الحركات يدوياً باستخدام صفحة **تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="c6ad5-182">**إلغاء**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-182">**Cancel**</span></span>     | <span data-ttu-id="c6ad5-183">حدد هذا الخيار إذا أردت التمكن من إلغاء الحركات التي تتضمن ملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="c6ad5-184">**إغلاق**</span><span class="sxs-lookup"><span data-stu-id="c6ad5-184">**Close**</span></span>      | <span data-ttu-id="c6ad5-185">حدد ملف تعريف ترحيل للتغيير إليه عند إغلاق الحركات بملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="c6ad5-186">ويتم اعتبار الحركة مغلقة عند تسويتها بالكامل.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]