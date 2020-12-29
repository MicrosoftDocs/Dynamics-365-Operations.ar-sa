---
title: نظرة عامة على الاستحقاقات
description: تصف هذه المقالة الاستحقاقات، وتوفر معلومات حول كيفية إعدادها وإنشاء الحركات.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439908"
---
# <a name="accruals-overview"></a><span data-ttu-id="53479-103">نظرة عامة على الاستحقاقات</span><span class="sxs-lookup"><span data-stu-id="53479-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53479-104">تصف هذه المقالة الاستحقاقات، وتوفر معلومات حول كيفية إعدادها وإنشاء الحركات.</span><span class="sxs-lookup"><span data-stu-id="53479-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="53479-105">يتم استخدام الاستحقاقات في محاسبة الاستحقاق لتعقب الإيراد الذي تم التعرف عليه في الفترة التي تم اكتسابه فيها أو عند استلام الدفع ولتعقب المصروفات (تكاليف) التي تم التعرف عليها عند حدوثها، وليس عند سداد الدفعة.</span><span class="sxs-lookup"><span data-stu-id="53479-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="53479-106">أنظمة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="53479-106">Accrual schemes</span></span>
<span data-ttu-id="53479-107">تُستخدم أنظمة الاستحقاق لإعداد التكاليف والإيرادات المؤجلة، ويمكن استخدام نفس نظام الاستحقاق لكلٍّ من الإيرادات والتكاليف.</span><span class="sxs-lookup"><span data-stu-id="53479-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="53479-108">وتقوم استحقاقات دفتر الأستاذ بإعادة توزيع تكاليف أو إيرادات بند دفتر اليومية بحيث يتم التعرف على التكاليف والإيرادات في الفترات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="53479-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="53479-109">وفي صفحة **نظام الاستحقاق**، يمكنك تحديد الحسابات المدينة والدائنة التي سيتم استخدامها عند تطبيق نظام الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="53479-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="53479-110">**المدين** – سيحل الحساب الرئيسي الذي تحدده محل الحساب الرئيسي المدين في بند إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="53479-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="53479-111">كما سيتم استخدام هذا الحساب لعكس التأجيل، استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="53479-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="53479-112">**الدائن** – سيحل الحساب الرئيسي الذي تحدده محل الحساب الرئيسي الدائن في بند إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="53479-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="53479-113">كما سيتم استخدام هذا الحساب لعكس التأجيل، استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="53479-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="53479-114">بعد تحديد الحسابات التي تريد استخدامها، يمكنك تحديد كيفية إنشاء رقم الإيصال عند إنشاء حركات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="53479-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="53479-115">كما يمكنك تحديد عدد مرات تكرار الحركات، وعدد المرات التي تم فيها إنشاء الحركات، وعندما يتم ترحيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="53479-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="53479-116">وبعد إنشاء نظام الاستحقاق، يمكنك استخدام بعض دفاتر اليومية باستخدام مهمة استحقاقات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="53479-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="53479-117">استحقاقات دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="53479-117">Ledger accruals</span></span>
<span data-ttu-id="53479-118">عندما تقوم بإدخال دفتر يومية، يمكنك النقر فوق **استحقاقات دفتر الأستاذ** في قائمة **المهام**.</span><span class="sxs-lookup"><span data-stu-id="53479-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="53479-119">وبعد ذلك، عند تحديد نظام الاستحقاق، سترى المبلغ الأساسي من دفتر اليومية الذي سوف يمتد على الفترة، حسبما يقرره نظام الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="53479-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="53479-120">على سبيل المثال، إذا كنت تدفع التأمين للموظف لمدة عام كامل في كانون الثاني/يناير، والمبلغ هو 12000، يجب عليك التعرف على هذه المصروفات كل شهر.</span><span class="sxs-lookup"><span data-stu-id="53479-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="53479-121">ويمكنك تحديد تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="53479-121">You can select the start date.</span></span> <span data-ttu-id="53479-122">كما يمكنك تحديد ما إذا كان المبلغ المستحق يستند إلى الحساب أو الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="53479-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="53479-123">‏‫وبعد إجراء التحديدات، انقر فوق **الحركات** لعرض كافة الحركات التي تم إنشاؤها استناداً إلى نظام الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="53479-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="53479-124">على سبيل المثال، إذا وزعت 12000 على مصاريف التأمين على مدار السنة، سترى 1000 لكل شهر.‬</span><span class="sxs-lookup"><span data-stu-id="53479-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="53479-125">‏‫وبعد ترحيل دفتر اليومية، يمكنك عرض الحركات باستخدام صفحة استعلام **حركات الإيصال**.</span><span class="sxs-lookup"><span data-stu-id="53479-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="53479-126">وإذا كان لا يمكن تطبيق نظام استحقاق (على سبيل المثال، عندما يتم تضمين فاتورة أمر المبيعات أو فاتورة أمر الشراء)، يمكنك إضافة المبلغ المدفوع مقدمًا وخصم مبلغ المصروفات.‬</span><span class="sxs-lookup"><span data-stu-id="53479-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="53479-127">يمكنك حينئذٍ تحديد **المقابل** عندما تقوم بتطبيق نظام الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="53479-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="53479-128">للحصول على مزيد من المعلومات، راجع [إنشاء أنظمة استحقاق](tasks/create-accrual-schemes.md) و[إنشاء حركات استحقاق دفتر الأستاذ](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="53479-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>
