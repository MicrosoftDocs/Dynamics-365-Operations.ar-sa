---
title: مدفوعات المورد لمبلغ جزئي
description: في بعض الأحيان، قد تسدد دفعة لأحد المورّدين تكون أقل من مبلغ الفاتورة. توضح هذه المقالة مختلف الخيارات التي يتم استخدامها لمعالجة هذه الحالة.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b0f4f6a6988f659c957664b140c4b9907ef3d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255683"
---
# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="98b27-104">دفعات المورد لمبلغ جزئي</span><span class="sxs-lookup"><span data-stu-id="98b27-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98b27-105">في بعض الأحيان، قد تسدد دفعة لأحد المورّدين تكون أقل من مبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="98b27-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="98b27-106">توضح هذه المقالة مختلف الخيارات التي يتم استخدامها لمعالجة هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="98b27-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="98b27-107">تتوقف الخيارات التي تتوفر لك على تكوين أعمالك ومتطلباتها.</span><span class="sxs-lookup"><span data-stu-id="98b27-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="98b27-108">مبالغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="98b27-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="98b27-109">يستطيع المورد أن يقدم لك خصمًا نقديًا لدفع فاتورة قبل تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="98b27-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="98b27-110">على سبيل المثال، يمكنك إدخال فاتورة بمبلغ 100.00 وتحدد خصمًا نقديًا بنسبة 2 في المائة، إذا تم دفع الفاتورة في غضون 10 أيام.</span><span class="sxs-lookup"><span data-stu-id="98b27-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="98b27-111">ومدد تاريخ الاستحقاق 30 يومًا.</span><span class="sxs-lookup"><span data-stu-id="98b27-111">The due date terms are 30 days.</span></span> <span data-ttu-id="98b27-112">‏‫وفي حالة استخدام مقترح دفع الخصم النقدي كمعيار لتحديد فاتورة، وتشغيل المقترح في أو قبل تاريخ الخصم النقدي، يتم تحديد الفاتورة للدفع، ويتم إنشاء الدفعة بمبلغ 98.00.</span><span class="sxs-lookup"><span data-stu-id="98b27-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="98b27-113">كما يمكن الحصول على خصم نقدي لدفعة فريدة تم إنشاؤها يدوياً.‬</span><span class="sxs-lookup"><span data-stu-id="98b27-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="98b27-114">المدفوعات الجزئية مع الخصومات النقدية</span><span class="sxs-lookup"><span data-stu-id="98b27-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="98b27-115">عندما تقوم بسداد دفعة جزئية، قد تخطط لسداد دفعة جزئية إضافية لتسوية الفاتورة بالكامل.</span><span class="sxs-lookup"><span data-stu-id="98b27-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="98b27-116">وللحصول على خصم نقدي لدفعة جزئية، يجب عليك تعيين خيار **حساب الخصومات النقدية لمدفوعات جزئية** إلى **نعم** في صفحة **معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="98b27-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="98b27-117">على سبيل المثال، تتلقى خصمًا نقديًا بنسبة 2 في المائة، إذا تم دفع الفاتورة في غضون 10 أيام بعد صدورها.</span><span class="sxs-lookup"><span data-stu-id="98b27-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="98b27-118">ويتم ترحيل فاتورة بمبلغ 100.00.</span><span class="sxs-lookup"><span data-stu-id="98b27-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="98b27-119">‏‫إذا قمت بسداد دفعة بمبلغ 49.00 في غضون 10 أيام، أدخل دينًا بمبلغ 49.00 في دفتر يومية مدفوعات.</span><span class="sxs-lookup"><span data-stu-id="98b27-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="98b27-120">وعند تسوية الدفعة الجزئية في صفحة **تسوية الحركات المفتوحة**، يظهر **1.00** في حقل **مبلغ الخصم النقدي المُراد الحصول عليه**.</span><span class="sxs-lookup"><span data-stu-id="98b27-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="98b27-121">إذا قمت بإدخال دفعة جزئية وتركت مبلغ الفاتورة الكامل في حقل **المبلغ المُراد تسويته**، فإنه تتم إعادة حساب حقل **مبلغ الخصم النقدي المراد الحصول عليه** تلقائياً عند ترحيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="98b27-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="98b27-122">إشعارات الدائن مع الخصومات النقدية</span><span class="sxs-lookup"><span data-stu-id="98b27-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="98b27-123">قد تقوم بإرجاع بعض الأصناف في إحدى الفواتير وتتلقى إشعار دائن.</span><span class="sxs-lookup"><span data-stu-id="98b27-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="98b27-124">إذا تم الحصول على خصم نقدي في الفاتورة الأصلية، فإنه يمكنك طرح قيمة الخصم والحصول على استرداد بالمبلغ الصحيح.</span><span class="sxs-lookup"><span data-stu-id="98b27-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="98b27-125">وإذا تم تعيين خيار **حساب الخصومات النقدية للإشعارات الدائنة** إلى **نعم** في صفحة **معلمات الحسابات الدائنة**، فإنه يتم حساب الخصم تلقائياً لإشعار الدائن.</span><span class="sxs-lookup"><span data-stu-id="98b27-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="98b27-126">على سبيل المثال، تتلقى خصمًا نقديًا بنسبة 2 في المائة، إذا تم دفع الفاتورة في غضون 10 أيام بعد صدورها.</span><span class="sxs-lookup"><span data-stu-id="98b27-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="98b27-127">ويتم ترحيل فاتورة بمبلغ 100.00.</span><span class="sxs-lookup"><span data-stu-id="98b27-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="98b27-128">وفي حالة إعادة البضائع وتلقى إشعار دائن، يمكنك إدخال إشعار الدائن لكامل مبلغ الفاتورة الأصلية 100.00، جنبًا إلى جنب مع الخصم النقدي بنسبة 2 في المائة الذي تم تحديده أيضًا في إشعار الدائن.</span><span class="sxs-lookup"><span data-stu-id="98b27-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="98b27-129">وعندما تقوم بعرض إشعار الدائن في صفحة **تسوية الحركات**، يظهر **98.00** في حقل **المبلغ المُراد تسويته** ويظهر **-2.00** في حقل **مبلغ الخصم النقدي**.</span><span class="sxs-lookup"><span data-stu-id="98b27-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="98b27-130">يتم ترحيل مبلغ الخصم إلى حساب خصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="98b27-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="98b27-131">مبالغ الدفع بالزيادة/النقصان</span><span class="sxs-lookup"><span data-stu-id="98b27-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="98b27-132">قد تقوم بسداد دفعة جزئية يكون فيها المبلغ الذي لا يزال يجب تسويته صغيرًا جداً.</span><span class="sxs-lookup"><span data-stu-id="98b27-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="98b27-133">على سبيل المثال، قيمة فاتورة المورد تساوي 1,000.00، وتدفع 999.90.</span><span class="sxs-lookup"><span data-stu-id="98b27-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="98b27-134">إذا كان المبلغ المتبقي أقل من المبلغ الذي تم تعيينه للمدفوعات بالزيادة أو النقصان في صفحة **معلمات الحسابات الدائنة**، فإنه يتم ترحيل الفرق تلقائياً حساب دفتر أستاذ الدفع بالزيادة/النقصان.</span><span class="sxs-lookup"><span data-stu-id="98b27-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="98b27-135">للحصول على مزيد من المعلومات، راجع [نظرة عامة على دفع المورّد‬](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98b27-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]