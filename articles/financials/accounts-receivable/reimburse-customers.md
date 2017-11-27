---
title: "عملاء التعويض"
description: "تشرح هذه المقالة كيفية إنشاء حركات التعويض لمجموعة من العملاء. إذا كان للعميل رصيد دائن، يمكن تعويض العميل لمبلغ الرصيد."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 01c9dcebe82544624c6dd0feb3672d1c5bdfe2d1
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="reimburse-customers"></a><span data-ttu-id="cfbf6-104">عملاء التعويض</span><span class="sxs-lookup"><span data-stu-id="cfbf6-104">Reimburse customers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cfbf6-105">تشرح هذه المقالة كيفية إنشاء حركات التعويض لمجموعة من العملاء.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="cfbf6-106">إذا كان للعميل رصيد دائن، يمكن تعويض العميل لمبلغ الرصيد.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="cfbf6-107">يعرض الجدول التالي المتطلبات الأساسية التي يجب أن تكون موجودة قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="cfbf6-108">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="cfbf6-108">Prerequisite</span></span>                                                            | <span data-ttu-id="cfbf6-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="cfbf6-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbf6-110">تحديد الحد الأدنى لمبلغ التعويض للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="cfbf6-111">في صفحة **معلمات الحسابات المدينة**، في المنطقة **عام**، في حقل **الحد الأدنى للتعويض**، أدخل الحد الأدنى للمبلغ الذي يمكن تعويضه للمدفوعات الزائدة للعميل.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="cfbf6-112">اختياري: قم بإضافة حساب مورد لكل عميل يمكن تعويضه.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="cfbf6-113">في صفحة **العملاء**، في علامة التبويب السريعة **التفاصيل المتنوعة**، في حقل **حساب المورد**، حدد حساب المورد للعميل.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="cfbf6-114">عند إنشاء حركات التعويض، يتم إنشاء فاتورة مورد لمبلغ الرصيد الدائن.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="cfbf6-115">تقوم عملية التعويض بإزالة الرصيد الدائن لحساب العميل وإنشاء رصيد مستحق لحساب المورد المقابل للعميل.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="cfbf6-116">في الحسابات المدينة، قم بتشغيل عملية **التعويض**.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="cfbf6-117">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="cfbf6-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="cfbf6-118">لتعويض حسابات العميل المحددة، انقر فوق **تحديد**، وقم بتحديد حسابات العميل في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="cfbf6-119">لتعويض كل حسابات العميل، انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="cfbf6-120">يتم تحويل المبالغ الدائنة لحسابات المورد الخاصة بالعملاءوتتم معالجتها كمدفوعات عادية.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="cfbf6-121">إذا لم يكن لدى العميل حساب مورد، فسيتم إنشاء حساب مورد لمرة واحدة تلقائيًا للعميل.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="cfbf6-122">لعرض حركات التعويض التي تم إنشاؤها، استخدم صفحة **التعويض**.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="cfbf6-123">في الحسابات الدائنة، قم بإنشاء عملية دفع فواتير المورد التي تم إنشاؤها بواسطة عملية التعويض.</span><span class="sxs-lookup"><span data-stu-id="cfbf6-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





