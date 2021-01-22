---
title: عملاء التعويض
description: تشرح هذه المقالة كيفية إنشاء حركات التعويض لمجموعة من العملاء. إذا كان للعميل رصيد دائن، يمكن تعويض العميل لمبلغ الرصيد.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bceeaf99437f6ef66bd3b4e1710b469c262e693e
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022533"
---
# <a name="reimburse-customers"></a><span data-ttu-id="cad97-104">عملاء التعويض</span><span class="sxs-lookup"><span data-stu-id="cad97-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cad97-105">تشرح هذه المقالة كيفية إنشاء حركات التعويض لمجموعة من العملاء.</span><span class="sxs-lookup"><span data-stu-id="cad97-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="cad97-106">إذا كان للعميل رصيد دائن، يمكن تعويض العميل لمبلغ الرصيد.</span><span class="sxs-lookup"><span data-stu-id="cad97-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="cad97-107">يعرض الجدول التالي المتطلبات الأساسية التي يجب أن تكون موجودة قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="cad97-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="cad97-108">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="cad97-108">Prerequisite</span></span>                                                            | <span data-ttu-id="cad97-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="cad97-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad97-110">تحديد الحد الأدنى لمبلغ التعويض للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="cad97-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="cad97-111">في صفحة **معلمات الحسابات المدينة** ، في المنطقة **عام** ، في حقل **الحد الأدنى للتعويض** ، أدخل الحد الأدنى للمبلغ الذي يمكن تعويضه للمدفوعات الزائدة للعميل.</span><span class="sxs-lookup"><span data-stu-id="cad97-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="cad97-112">اختياري: قم بإضافة حساب مورد لكل عميل يمكن تعويضه.</span><span class="sxs-lookup"><span data-stu-id="cad97-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="cad97-113">في صفحة **العملاء** ، في علامة التبويب السريعة **التفاصيل المتنوعة** ، في حقل **حساب المورد** ، حدد حساب المورد للعميل.</span><span class="sxs-lookup"><span data-stu-id="cad97-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="cad97-114">عند إنشاء حركات التعويض، يتم إنشاء فاتورة مورد لمبلغ الرصيد الدائن.</span><span class="sxs-lookup"><span data-stu-id="cad97-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="cad97-115">تقوم عملية التعويض بإزالة الرصيد الدائن لحساب العميل وإنشاء رصيد مستحق لحساب المورد المقابل للعميل.</span><span class="sxs-lookup"><span data-stu-id="cad97-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="cad97-116">في الحسابات المدينة، قم بتشغيل عملية **التعويض**.</span><span class="sxs-lookup"><span data-stu-id="cad97-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="cad97-117">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="cad97-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="cad97-118">لتعويض حسابات العميل المحددة، انقر فوق **تحديد** ، وقم بتحديد حسابات العميل في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="cad97-118">To reimburse specific customer accounts, click **Select** , and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="cad97-119">لتعويض كل حسابات العميل، انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cad97-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="cad97-120">يتم تحويل المبالغ الدائنة لحسابات المورد الخاصة بالعملاءوتتم معالجتها كمدفوعات عادية.</span><span class="sxs-lookup"><span data-stu-id="cad97-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="cad97-121">إذا لم يكن لدى العميل حساب مورد، فسيتم إنشاء حساب مورد لمرة واحدة تلقائيًا للعميل.</span><span class="sxs-lookup"><span data-stu-id="cad97-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="cad97-122">لعرض حركات التعويض التي تم إنشاؤها، استخدم صفحة **التعويض**.</span><span class="sxs-lookup"><span data-stu-id="cad97-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="cad97-123">في الحسابات الدائنة، قم بإنشاء عملية دفع فواتير المورد التي تم إنشاؤها بواسطة عملية التعويض.</span><span class="sxs-lookup"><span data-stu-id="cad97-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>



