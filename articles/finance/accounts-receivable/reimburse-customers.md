---
title: عملاء التعويض
description: تشرح هذه المقالة كيفية إنشاء حركات التعويض لمجموعة من العملاء. إذا كان للعميل رصيد دائن، يمكن تعويض العميل لمبلغ الرصيد.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd8b32e04743fdde3cc339e1535f8ae58c518aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816282"
---
# <a name="reimburse-customers"></a><span data-ttu-id="d8fed-104">عملاء التعويض</span><span class="sxs-lookup"><span data-stu-id="d8fed-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8fed-105">تشرح هذه المقالة كيفية إنشاء حركات التعويض لمجموعة من العملاء.</span><span class="sxs-lookup"><span data-stu-id="d8fed-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="d8fed-106">إذا كان للعميل رصيد دائن، يمكن تعويض العميل لمبلغ الرصيد.</span><span class="sxs-lookup"><span data-stu-id="d8fed-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="d8fed-107">يعرض الجدول التالي المتطلبات الأساسية التي يجب أن تكون موجودة قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="d8fed-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="d8fed-108">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="d8fed-108">Prerequisite</span></span>                                                            | <span data-ttu-id="d8fed-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="d8fed-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="d8fed-110">تحديد الحد الأدنى لمبلغ التعويض للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="d8fed-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="d8fed-111">في صفحة **معلمات الحسابات المدينة**، في المنطقة **عام**، في حقل **الحد الأدنى للتعويض**، أدخل الحد الأدنى للمبلغ الذي يمكن تعويضه للمدفوعات الزائدة للعميل.</span><span class="sxs-lookup"><span data-stu-id="d8fed-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="d8fed-112">اختياري: قم بإضافة حساب مورد لكل عميل يمكن تعويضه.</span><span class="sxs-lookup"><span data-stu-id="d8fed-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="d8fed-113">في صفحة **العملاء**، في علامة التبويب السريعة **التفاصيل المتنوعة**، في حقل **حساب المورد**، حدد حساب المورد للعميل.</span><span class="sxs-lookup"><span data-stu-id="d8fed-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="d8fed-114">عند إنشاء حركات التعويض، يتم إنشاء فاتورة مورد لمبلغ الرصيد الدائن.</span><span class="sxs-lookup"><span data-stu-id="d8fed-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="d8fed-115">تقوم عملية التعويض بإزالة الرصيد الدائن لحساب العميل وإنشاء رصيد مستحق لحساب المورد المقابل للعميل.</span><span class="sxs-lookup"><span data-stu-id="d8fed-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="d8fed-116">في الحسابات المدينة، قم بتشغيل العملية **التعويض** (**الحسابات المدينة \> المهام الدورية \> التعويض**).</span><span class="sxs-lookup"><span data-stu-id="d8fed-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="d8fed-117">لتجميع كافة الحركات، بغض النظر عن أبعاد دفتر الأستاذ، قم بتعيين الخيار **تلخيص العميل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d8fed-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="d8fed-118">لتجميع الحركات التي لها نفس أبعاد دفتر الأستاذ فقط، قم بتعيين الخيار على **لا**.</span><span class="sxs-lookup"><span data-stu-id="d8fed-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="d8fed-119">حدد **تضمين العملاء الذين لديهم حركات مدينة مستحقة** لتحديد العملاء الذين لديهم مبالغ مدينة لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="d8fed-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="d8fed-120">لتعويض حسابات العملاء المحددة، على علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم حدد حسابات العملاء في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="d8fed-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="d8fed-121">يتم تحويل المبالغ الدائنة لحسابات المورد الخاصة بالعملاءوتتم معالجتها كمدفوعات عادية.</span><span class="sxs-lookup"><span data-stu-id="d8fed-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="d8fed-122">إذا لم يكن لدى العميل حساب مورد، فسيتم إنشاء حساب مورد لمرة واحدة تلقائيًا للعميل.</span><span class="sxs-lookup"><span data-stu-id="d8fed-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="d8fed-123">لعرض حركات التعويض التي تم إنشاؤها، استخدم التقرير **التعويض** (**الحسابات المدينة \> الاستعلامات والتقارير \> تقرير التعويض**).</span><span class="sxs-lookup"><span data-stu-id="d8fed-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="d8fed-124">في الحسابات الدائنة، قم بإنشاء عملية دفع فواتير المورد التي تم إنشاؤها بواسطة عملية التعويض.</span><span class="sxs-lookup"><span data-stu-id="d8fed-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="d8fed-125">للحصول على معلومات حول كيفية دفع الموردين، راجع [نظرة عامة على دفع المورد](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="d8fed-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]