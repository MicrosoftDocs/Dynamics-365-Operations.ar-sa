---
title: تسوية الشحن في إدارة النقل
description: يوضح هذا الموضوع عملية تسوية الشحن.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af7bbb500de25e0a796147fae42cd7d943be9df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205215"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="63ec3-103">تسوية الشحن في إدارة النقل</span><span class="sxs-lookup"><span data-stu-id="63ec3-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63ec3-104">يوضح هذا الموضوع عملية تسوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="63ec3-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="63ec3-105">يمكن تسوية الشحن يدويًا، أو يمكن إعدادها بحيث تحدث تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="63ec3-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="63ec3-106">لاستخدام تسوية الشحن التلقائية، يجب إعداد السجل الرئيسي للتدقيق‬ حيث يمكنك تعريف المعايير التي تحدد فواتير الشحن التي تتم مطابقتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="63ec3-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="63ec3-107">عملية تسوية الشحن</span><span class="sxs-lookup"><span data-stu-id="63ec3-107">The freight reconciliation process</span></span>

<span data-ttu-id="63ec3-108">يتم حساب أسعار الشحن بواسطة محرك الشحن الذي يقترن بشركة الشحن ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="63ec3-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="63ec3-109">عندما يتم تأكيد الحمل, يتم إنشاء فاتورة الشحن وتُنقل إليها أسعار الشحن.</span><span class="sxs-lookup"><span data-stu-id="63ec3-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="63ec3-110">,يتم تقسيم أسعار الشحن كتكاليف متنوعة في المستند المصدر ذي الصلة (أمر الشراء و/أو أمر المبيعات و/أو أمر التحويل)، بالاستناد إلى الإعداد المستخدم لعملية الفوترة العادية.</span><span class="sxs-lookup"><span data-stu-id="63ec3-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="63ec3-111">بإمكان عملية تسوية الشحن (وتُعرف أيضًا بعملية المطابقة) أن تبدأ فور وصول فاتورة الشحن من شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="63ec3-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="63ec3-112">يمكنك تلقي الفاتورة إلكترونيًا أو على الورق.</span><span class="sxs-lookup"><span data-stu-id="63ec3-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="63ec3-113">في حالة تلقي الفاتورة على الورق، يمكنك إنشاء فاتورة إلكترونية باستخدام فاتورة الشحن كقالب.</span><span class="sxs-lookup"><span data-stu-id="63ec3-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="63ec3-114">[![عملية تسوية الشحن](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="63ec3-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="63ec3-115">التسوية اليدوية</span><span class="sxs-lookup"><span data-stu-id="63ec3-115">Manual reconciliation</span></span>

<span data-ttu-id="63ec3-116">إذا كنت تعمل على تسوية الشحن يدويًا، فيجب عليك مطابقة كل بند في الفاتورة مع بند أو بنود فاتورة الشحن للحمل الجاري فوترته.</span><span class="sxs-lookup"><span data-stu-id="63ec3-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="63ec3-117">ستجري هذه مطابقة في صفحة **مطابقة فاتورة الشحن والفاتورة‬**.</span><span class="sxs-lookup"><span data-stu-id="63ec3-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="63ec3-118">إذا لم يتطابق المبلغ في بند الفاتورة مع مبلغ فاتورة الشحن، فيجب تحديد سبب تسوية للفرق.</span><span class="sxs-lookup"><span data-stu-id="63ec3-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="63ec3-119">في حال وجود أسباب متعددة للتسوية، يمكنك تقسيم المبلغ غير المتطابق فيما بينها.</span><span class="sxs-lookup"><span data-stu-id="63ec3-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="63ec3-120">يحدد سبب التسوية كيفية ترحيل مبالغ الفروقات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="63ec3-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="63ec3-121">عندما يتم حساب تسوية مبلغ الفاتورة بالكامل، يتم إرساله للموافق عليه، ثم يتم ترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="63ec3-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="63ec3-122">يعرض الشكل التوضيحي التالي كيفية إنشاء فاتورة شحن وإجراء تسوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="63ec3-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="63ec3-123">[![مهام تسوية الشحن](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="63ec3-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="63ec3-124">التسوية التلقائية</span><span class="sxs-lookup"><span data-stu-id="63ec3-124">Automatic reconciliation</span></span>

<span data-ttu-id="63ec3-125">لاستخدام التسوية التلقائية، يجب تحديد جدول للتسوية، والفواتير وشركات الشحن التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="63ec3-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="63ec3-126">تتم مطابقة بنود الفواتير وفواتير الشحن وفقًا لإعداد السجل الرئيسي للتدقيق‬ ونوع فاتورة الشحن.</span><span class="sxs-lookup"><span data-stu-id="63ec3-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="63ec3-127">بعد تشغيل التسوية التلقائية، يجب معالجة الفواتير التي يتعذر على النظام مطابقتها.</span><span class="sxs-lookup"><span data-stu-id="63ec3-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="63ec3-128">بعد ذلك، يجب معالجة هذه الفواتير يدويًا قبل أن تتمكن من ترحيل كافة الفواتير للدفع.</span><span class="sxs-lookup"><span data-stu-id="63ec3-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="63ec3-129">مطابقه فواتير الشحن مع فواتير الشحن باستخدام التسوية التلقائية أو اليدوية</span><span class="sxs-lookup"><span data-stu-id="63ec3-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="63ec3-130">*المطابقة* هي عمليه البحث عن كمبيالات الشحن المطابقة لكل فاتورة شحن.</span><span class="sxs-lookup"><span data-stu-id="63ec3-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="63ec3-131">ويمكن القيام بذلك بمطابقه بنود الفاتورة واحدا تلو الآخر (المطابقة اليدوية)، أو بمطابقه كافة الفواتير المتوفرة في مره واحده (المطابقة التلقائية).</span><span class="sxs-lookup"><span data-stu-id="63ec3-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="63ec3-132">المطابقة التلقائية</span><span class="sxs-lookup"><span data-stu-id="63ec3-132">Auto matching</span></span>

<span data-ttu-id="63ec3-133">عند مطابقه فواتير شحن متعددة بنفس فاتورة الشحن، فان عمليه المطابقة التلقائية تعمل كما يلي:</span><span class="sxs-lookup"><span data-stu-id="63ec3-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="63ec3-134">ويتم فرز كافة فواتير الشحن غير المطابقة حسب المبلغ، بأكبر مبلغ أولا.</span><span class="sxs-lookup"><span data-stu-id="63ec3-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="63ec3-135">تتم مطابقه فواتير الشحن واحدا تلو الآخر، حتى لا يكون لفاتورة الشحن مبلغا موجبا متبقيا.</span><span class="sxs-lookup"><span data-stu-id="63ec3-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="63ec3-136">اعتمادا علي اعداد التدقيق الرئيسي والمبلغ المتبقي في فواتير الشحن، يتم تعيين المبلغ المتبقي.</span><span class="sxs-lookup"><span data-stu-id="63ec3-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="63ec3-137">المطابقة اليدوية</span><span class="sxs-lookup"><span data-stu-id="63ec3-137">Manual matching</span></span>

<span data-ttu-id="63ec3-138">ستتوفر كافة فواتير الشحن التي لها مبالغ موجبه للمطابقة.</span><span class="sxs-lookup"><span data-stu-id="63ec3-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="63ec3-139">وبشكل مشابه للمطابقة التلقائية، سيكون المستخدم قادرا فقط علي مطابقه فواتير الشحن التي لها مبالغ سالبه للشحن كمبيالة لم تتم مطابقتها بالكامل.</span><span class="sxs-lookup"><span data-stu-id="63ec3-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="63ec3-140">مثال</span><span class="sxs-lookup"><span data-stu-id="63ec3-140">Example</span></span>

<span data-ttu-id="63ec3-141">لنفترض ان لديك فاتورة شحن (FB) لمبلغ 1500 وقامت بإنشاء ثلاث فواتير شحن لفاتورة الشحن مع بند فاتورة واحد لكل فاتورة بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="63ec3-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="63ec3-142">فاتورة الشحن الاصليه (FB): المبلغ 1500</span><span class="sxs-lookup"><span data-stu-id="63ec3-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="63ec3-143">الفاتورة 1 (Inv1): المبلغ 1000</span><span class="sxs-lookup"><span data-stu-id="63ec3-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="63ec3-144">الفاتورة 2 (Inv2): المبلغ 600</span><span class="sxs-lookup"><span data-stu-id="63ec3-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="63ec3-145">الفاتورة 3 (Inv3): المبلغ 100</span><span class="sxs-lookup"><span data-stu-id="63ec3-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="63ec3-146">نتيجة المطابقة التلقائية</span><span class="sxs-lookup"><span data-stu-id="63ec3-146">Automatic matching result</span></span>

<span data-ttu-id="63ec3-147">سيتم تنفيذ المطابقة التلقائية بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="63ec3-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="63ec3-148">فرز كافة فواتير الشحن تنازليا حسب المبلغ: Inv1-> Inv2-> Inv3.</span><span class="sxs-lookup"><span data-stu-id="63ec3-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="63ec3-149">مطابقه Inv1 مع FB.</span><span class="sxs-lookup"><span data-stu-id="63ec3-149">Match Inv1 with FB.</span></span> <span data-ttu-id="63ec3-150">تمت مطابقه Inv1 1000 وفبه له مبلغ 500 متبقي، التالي يتم تعيين الحالة إلى مطابقه بشكل *جزئي*.</span><span class="sxs-lookup"><span data-stu-id="63ec3-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="63ec3-151">مطابقه Inv2 مع FB.</span><span class="sxs-lookup"><span data-stu-id="63ec3-151">Match Inv2 with FB.</span></span> <span data-ttu-id="63ec3-152">تمت مطابقه Inv2 500 وFB له مبلغ 0 متبقي، التالي يتم تعيين الحالة إلى مطابقه بشكل *جزئي*.</span><span class="sxs-lookup"><span data-stu-id="63ec3-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="63ec3-153">ونظرا لان FB الآن متطابق تماما، فلن تتم معالجه Inv3.</span><span class="sxs-lookup"><span data-stu-id="63ec3-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="63ec3-154">نتيجة المطابقة اليدوية</span><span class="sxs-lookup"><span data-stu-id="63ec3-154">Manual matching result</span></span>

<span data-ttu-id="63ec3-155">للمطابقة اليدوية، تختلف النتائج بناء علي ترتيب المطابقة، كما هو موضح في المثال التالي من حالات.</span><span class="sxs-lookup"><span data-stu-id="63ec3-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="63ec3-156">حاله المطابقة اليدوية 1</span><span class="sxs-lookup"><span data-stu-id="63ec3-156">Manual matching case 1</span></span>

<span data-ttu-id="63ec3-157">أحدي الطرق للقيام بالمطابقة اليدوية لهذا المثال هي المتابعة كما يلي:</span><span class="sxs-lookup"><span data-stu-id="63ec3-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="63ec3-158">مطابقه Inv1 مع FB.</span><span class="sxs-lookup"><span data-stu-id="63ec3-158">Match FB with Inv1.</span></span> <span data-ttu-id="63ec3-159">FB له مبلغ 500 متبقي، التالي يتم تعيين الحالة إلى مطابقه بشكل *جزئي*.</span><span class="sxs-lookup"><span data-stu-id="63ec3-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="63ec3-160">مطابقه Inv2 مع FB.</span><span class="sxs-lookup"><span data-stu-id="63ec3-160">Match Inv2 with FB.</span></span> <span data-ttu-id="63ec3-161">تمت مطابقه Inv2 500 وFB له مبلغ 0 متبقي، التالي يتم تعيين الحالة إلى مطابقه بشكل *جزئي*.</span><span class="sxs-lookup"><span data-stu-id="63ec3-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="63ec3-162">عند مطابقه Inv3 اليدوية، لن تجد إيه كمبيالات شحن غير متطابقة.</span><span class="sxs-lookup"><span data-stu-id="63ec3-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="63ec3-163">هذه الحالة بشكل أساسي هي نفسها المطابقة التلقائية</span><span class="sxs-lookup"><span data-stu-id="63ec3-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="63ec3-164">حاله المطابقة اليدوية 2</span><span class="sxs-lookup"><span data-stu-id="63ec3-164">Manual matching case 2</span></span>

<span data-ttu-id="63ec3-165">أحدي الطرق الأخرى للقيام بالمطابقة اليدوية لهذا المثال هي المتابعة كما يلي:</span><span class="sxs-lookup"><span data-stu-id="63ec3-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="63ec3-166">مطابقه Inv3 مع FB.</span><span class="sxs-lookup"><span data-stu-id="63ec3-166">Match Inv3 with FB.</span></span> <span data-ttu-id="63ec3-167">والآن FB المبلغ المتبقي 1600، وهو ما يمثل بطرح القيمة 100 في الأعلى من 1500.</span><span class="sxs-lookup"><span data-stu-id="63ec3-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="63ec3-168">ويكون لكل من FB وInv3 كميه متطابقة تبلغ 100.</span><span class="sxs-lookup"><span data-stu-id="63ec3-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="63ec3-169">مطابقه Inv1 وInv 2 مع FB واحده تلو الأخرى.</span><span class="sxs-lookup"><span data-stu-id="63ec3-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="63ec3-170">فب متطابق بالكامل.</span><span class="sxs-lookup"><span data-stu-id="63ec3-170">FB is fully matched.</span></span>

<span data-ttu-id="63ec3-171">كما يوضح هذا المثال، يجب القيام يدويا بمطابقه فواتير الشحن ذات المبالغ السالبة.</span><span class="sxs-lookup"><span data-stu-id="63ec3-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="63ec3-172">سيؤكد ذلك دائما انه من الممكن مطابقه فواتير الشحن بالمبالغ السالبة إلى فاتورة الشحن غير المتطابقة بالكامل لأنها تتيح لك التحكم في التسلسل المطابق.</span><span class="sxs-lookup"><span data-stu-id="63ec3-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]