---
title: نموذج بيانات خريطة الإبلاغ الإلكتروني لمصادر البيانات المحددة
description: يصف هذا الموضوع كيفيه تعيين نموذج بيانات "التقرير الكتروني" (ER) إلى مصادر بيانات Microsoft المحددة Dynamics 365 Finance.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e2ba94c9ec3ecc33f0c697d9f18f763749e4ba1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093738"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="ce1fa-103">نموذج بيانات خريطة الإبلاغ الإلكتروني لمصادر البيانات المحددة</span><span class="sxs-lookup"><span data-stu-id="ce1fa-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce1fa-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تعيين أحد نماذج بيانات التقارير الإلكترونية لمصادر بيانات محددة.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="ce1fa-105">سيتم استخدام تعيين هذا المخطط لاحقاً كمصدر بيانات في تنسيق تكوين سيتم استخدامه لإدارة مستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="ce1fa-106">في هذا المثال، تقوم بتعيين نموذج بيانات لشركة عينة، وهي .Litware, Inc لمصادر البيانات.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="ce1fa-107">ولإكمال هذه الخطوات، عليك أولاً إكمال الخطوات المضمنة في الإجراء "تحديد مصادر البيانات لتعيين النموذج".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="ce1fa-108">فتح شجرة تكوينات التقرير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="ce1fa-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="ce1fa-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ce1fa-110">انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="ce1fa-111">تحديد تعيين نموذج تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="ce1fa-111">Select created model mapping</span></span>
1. <span data-ttu-id="ce1fa-112">في الشجرة، حدد "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="ce1fa-113">تأكد أن تكوين النموذج "المدفوعات (نموذج مبسط)" قد تم إنشاؤه مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="ce1fa-114">وإلا، فتوقف الآن وعد بعد إكمال دليل المهمة "إنشاء تكوين جديد باستخدام نموذج بيانات المجال المحدد".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="ce1fa-115">انقر فوق "مصمم النموذج".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-115">Click Model designer.</span></span>
3. <span data-ttu-id="ce1fa-116">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="ce1fa-117">حدِّد السجل "تعيين CT".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="ce1fa-118">تعيين CT</span><span class="sxs-lookup"><span data-stu-id="ce1fa-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="ce1fa-119">ربط مصادر البيانات التي تم إنشاؤها بعناصر نماذج البيانات</span><span class="sxs-lookup"><span data-stu-id="ce1fa-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="ce1fa-120">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-120">Click Designer.</span></span>
2. <span data-ttu-id="ce1fa-121">في الشجرة، حدد "تاريخ ووقت المعالجة (ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="ce1fa-122">في الشجرة، حدد "تاريخ المعالجة (ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="ce1fa-123">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-123">Click Bind.</span></span>
5. <span data-ttu-id="ce1fa-124">في الشجرة، حدد "هوية رسالة الدفع (MessageIdentification)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="ce1fa-125">في الشجرة، قم بتوسيع "الحركات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="ce1fa-126">في الشجرة، حدد "الحركات/رقم دفعة دفتر اليومية (JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="ce1fa-127">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-127">Click Bind.</span></span>
9. <span data-ttu-id="ce1fa-128">في الشجرة، حدد "المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="ce1fa-129">في الشجرة، حدد "الحركات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="ce1fa-130">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-130">Click Bind.</span></span>
12. <span data-ttu-id="ce1fa-131">في الشجرة، قم بتوسيع "المدفوعات=الحركات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="ce1fa-132">في الشجرة، قم بتوسيع "المدفوعات=الحركات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="ce1fa-133">في الشجرة، قم بتوسيع "المدفوعات=الحركات/الدائن/الحساب".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="ce1fa-134">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الحساب/رمز العملة (العملة)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="ce1fa-135">في الشجرة، قم بتوسيع "Transactions\vendBankAccountInTransactionCompany()"</span><span class="sxs-lookup"><span data-stu-id="ce1fa-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="ce1fa-136">في الشجرة، حدد "المدفوعات\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="ce1fa-137">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-137">Click Bind.</span></span>
19. <span data-ttu-id="ce1fa-138">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الحساب/رمز IBAN (رمز IBAN)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="ce1fa-139">في الشجرة، حدد الحركات\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="ce1fa-140">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-140">Click Bind.</span></span>
22. <span data-ttu-id="ce1fa-141">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الحساب/الرقم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="ce1fa-142">في الشجرة، حدد "الحركات\vendBankAccountInTransactionCompany()\رقم حساب البنك (AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="ce1fa-143">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-143">Click Bind.</span></span>
25. <span data-ttu-id="ce1fa-144">في الشجرة، قم بتوسيع "المدفوعات=الحركات/الدائن/الوكيل".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="ce1fa-145">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الوكيل/الاسم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="ce1fa-146">في الشجرة، حدد "Transactions\vendBankAccountInTransactionCompany()\Name".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="ce1fa-147">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-147">Click Bind.</span></span>
29. <span data-ttu-id="ce1fa-148">في الشجرة، حدد 'المدفوعات/الحركات/الدائن/الوكيل/رقم التوجيه/(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="ce1fa-149">في الشجرة، حدد "الحركات/vendBankAccountInTransactionCompany()\رقم التوجيه(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="ce1fa-150">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-150">Click Bind.</span></span>
32. <span data-ttu-id="ce1fa-151">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الوكيل/رمز SWIFT (SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="ce1fa-152">في الشجرة، حدد "الحركات/vendBankAccountInTransactionCompany()\رمز SWIFT(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="ce1fa-153">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-153">Click Bind.</span></span>
35. <span data-ttu-id="ce1fa-154">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الاسم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="ce1fa-155">في الشجرة، قم بتوسيع "الحركات/\findVendTable()'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="ce1fa-156">في الشجرة، حدد "Transactions\findVendTable()\name()'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="ce1fa-157">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-157">Click Bind.</span></span>
39. <span data-ttu-id="ce1fa-158">في الشجرة، حدد "المدفوعات= الحركات/رمز العملة (العملة)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="ce1fa-159">في الشجرة، قم بتوسيع "الحركات\>العلاقات".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="ce1fa-160">في الشجرة، قم بتوسيع "الحركات\>العلاقات\جدول العملات (العملة)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="ce1fa-161">في الشجرة، حدد "الحركات\>العلاقات\جدول العملات(العملة)\رمز العملة(CurrencyCodeISO)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="ce1fa-162">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-162">Click Bind.</span></span>
44. <span data-ttu-id="ce1fa-163">في الشجرة، قم بتوسيع "المدفوعات=الحركات/المدين".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="ce1fa-164">في الشجرة، قم بتوسيع "المدفوعات=الحركات/المدين/الحساب".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="ce1fa-165">في الشجرة، حدد "المدفوعات= الحركات/المدين/الحساب/رمز العملة (العملة)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="ce1fa-166">في الشجرة، حدد "حساب البنك(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="ce1fa-167">في الشجرة، قم بتوسيع "حساب البنك(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="ce1fa-168">في الشجرة، حدد "حساب البنك(BankAccount)\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="ce1fa-169">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-169">Click Bind.</span></span>
51. <span data-ttu-id="ce1fa-170">في الشجرة، حدد "حساب البنك(BankAccount)\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="ce1fa-171">في الشجرة، حدد "المدفوعات= الحركات/المدين/الحساب/رمز IBAN (رمز IBAN)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="ce1fa-172">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-172">Click Bind.</span></span>
54. <span data-ttu-id="ce1fa-173">في الشجرة، حدد "المدفوعات= الحركات/الدائن/الحساب/الرقم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="ce1fa-174">في الشجرة، حدد 'حساب البنك(BankAccount)\رقم حساب البنك(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="ce1fa-175">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-175">Click Bind.</span></span>
57. <span data-ttu-id="ce1fa-176">في الشجرة، قم بتوسيع "المدفوعات=الحركات/المدين/الوكيل".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="ce1fa-177">في الشجرة، حدد "المدفوعات= الحركات/المدين/الوكيل/الاسم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="ce1fa-178">في الشجرة، حدد "حساب البنك (BankAccount)/الاسم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="ce1fa-179">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-179">Click Bind.</span></span>
61. <span data-ttu-id="ce1fa-180">في الشجرة، حدد 'المدفوعات/الحركات/المدين/الوكيل/رقم التوجيه/(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="ce1fa-181">في الشجرة، حدد 'حساب البنك(BankAccount)\رقم التوجيه(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="ce1fa-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-182">Click Bind.</span></span>
64. <span data-ttu-id="ce1fa-183">في الشجرة، حدد "المدفوعات= الحركات/المدين/الوكيل/رمز SWIFT (SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="ce1fa-184">في الشجرة، حدد "حساب البنك(BankAccount)\رمز SWIFT(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="ce1fa-185">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-185">Click Bind.</span></span>
67. <span data-ttu-id="ce1fa-186">في الشجرة، حدد "المدفوعات= الحركات/المدين/الاسم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="ce1fa-187">في الشجرة، حدد "معلومات الشركة(الشركة)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="ce1fa-188">في الشجرة، قم بتوسيع "معلومات الشركة(الشركة)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="ce1fa-189">في الشجرة، حدد "معلومات الشركة(الشركة)/الاسم".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="ce1fa-190">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-190">Click Bind.</span></span>
72. <span data-ttu-id="ce1fa-191">في الشجرة، حدد "المدفوعات= الحركات/الوصف".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="ce1fa-192">في الشجرة، حدد "الحركات/الوصف(Txt)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="ce1fa-193">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-193">Click Bind.</span></span>
75. <span data-ttu-id="ce1fa-194">في الشجرة، حدد "المدفوعات= الحركات/رمز الهوية من نهاية إلى نهاية(End2EndID)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="ce1fa-195">في الشجرة، حدد "الحركات\$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="ce1fa-196">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-196">Click Bind.</span></span>
78. <span data-ttu-id="ce1fa-197">في الشجرة، حدد 'المدفوعات= الحركات/المبلغ المحدد(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="ce1fa-198">في الشجرة، حدد "الحركات\$المبلغ".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="ce1fa-199">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-199">Click Bind.</span></span>
81. <span data-ttu-id="ce1fa-200">في الشجرة، حدد 'المدفوعات الحركات/تاريخ الحركة(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="ce1fa-201">في الشجرة، حدد "الحركات/التاريخ(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="ce1fa-202">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="ce1fa-203">التحقق من صحة تعيين تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="ce1fa-203">Validate created mapping</span></span>
1. <span data-ttu-id="ce1fa-204">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-204">Click Validate.</span></span>
    * <span data-ttu-id="ce1fa-205">تحقق من صحة التعيين الجديد للتأكد من صحة كافة عمليات الربط‬.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="ce1fa-206">‏‫انقر فوق السهم لتوسيع قسم قائمة الأخطاء أو طيه.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="ce1fa-207">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-207">Click Save.</span></span>
4. <span data-ttu-id="ce1fa-208">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-208">Close the page.</span></span>
5. <span data-ttu-id="ce1fa-209">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-209">Close the page.</span></span>
6. <span data-ttu-id="ce1fa-210">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="ce1fa-211">تغيير حالة الإصدار الحالي لتكوين النموذج.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="ce1fa-212">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-212">Click Change status.</span></span>
    * <span data-ttu-id="ce1fa-213">قم بتغيير حالة تكوين النموذج المصمم - من "مسودة" إلى "مكتمل" لجعله متوفرًا لتصميم تنسيق الدفع.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="ce1fa-214">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-214">Click Complete.</span></span>
    * <span data-ttu-id="ce1fa-215">حدد "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-215">Select Complete.</span></span>  
3. <span data-ttu-id="ce1fa-216">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ce1fa-217">على سبيل المثال، "الإصدار 1".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="ce1fa-218">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-218">Click OK.</span></span>
5. <span data-ttu-id="ce1fa-219">حدد الإصدار المكتمل للتكوين الحالي.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="ce1fa-220">لاحظ أنه يتم حفظ التكوين الذي يتم إنشاؤه باسم "الإصدار المكتمل 1".</span><span class="sxs-lookup"><span data-stu-id="ce1fa-220">Note that the created configuration is saved as completed version 1.</span></span>  

