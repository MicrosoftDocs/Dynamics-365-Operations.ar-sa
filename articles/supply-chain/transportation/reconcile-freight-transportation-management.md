---
title: تسوية الشحن في إدارة النقل
description: يوضح هذا الموضوع عملية تسوية الشحن.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb3ba06f4fa8cc4af952619d06a58e605ff87e2a
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251559"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="6ce20-103">تسوية الشحن في إدارة النقل</span><span class="sxs-lookup"><span data-stu-id="6ce20-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ce20-104">يوضح هذا الموضوع عملية تسوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="6ce20-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="6ce20-105">يمكن تسوية الشحن يدويًا، أو يمكن إعدادها بحيث تحدث تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6ce20-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="6ce20-106">لاستخدام تسوية الشحن التلقائية، يجب إعداد السجل الرئيسي للتدقيق‬ حيث يمكنك تعريف المعايير التي تحدد فواتير الشحن التي تتم مطابقتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6ce20-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="6ce20-107">عملية تسوية الشحن</span><span class="sxs-lookup"><span data-stu-id="6ce20-107">The freight reconciliation process</span></span>
<span data-ttu-id="6ce20-108">يتم حساب أسعار الشحن بواسطة محرك الشحن الذي يقترن بشركة الشحن ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="6ce20-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="6ce20-109">عندما يتم تأكيد الحمل, يتم إنشاء فاتورة الشحن وتُنقل إليها أسعار الشحن.</span><span class="sxs-lookup"><span data-stu-id="6ce20-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="6ce20-110">,يتم تقسيم أسعار الشحن كتكاليف متنوعة في المستند المصدر ذي الصلة (أمر الشراء و/أو أمر المبيعات و/أو أمر التحويل)، بالاستناد إلى الإعداد المستخدم لعملية الفوترة العادية.</span><span class="sxs-lookup"><span data-stu-id="6ce20-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="6ce20-111">بإمكان عملية تسوية الشحن (وتُعرف أيضًا بعملية المطابقة) أن تبدأ فور وصول فاتورة الشحن من شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="6ce20-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="6ce20-112">يمكنك تلقي الفاتورة إلكترونيًا أو على الورق.</span><span class="sxs-lookup"><span data-stu-id="6ce20-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="6ce20-113">في حالة تلقي الفاتورة على الورق، يمكنك إنشاء فاتورة إلكترونية باستخدام فاتورة الشحن كقالب.</span><span class="sxs-lookup"><span data-stu-id="6ce20-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="6ce20-114">[![عملية تسوية الشحن](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="6ce20-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="6ce20-115">التسوية اليدوية</span><span class="sxs-lookup"><span data-stu-id="6ce20-115">Manual reconciliation</span></span>
<span data-ttu-id="6ce20-116">إذا كنت تعمل على تسوية الشحن يدويًا، فيجب عليك مطابقة كل بند في الفاتورة مع بند أو بنود فاتورة الشحن للحمل الجاري فوترته.</span><span class="sxs-lookup"><span data-stu-id="6ce20-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="6ce20-117">ستجري هذه مطابقة في صفحة **مطابقة فاتورة الشحن والفاتورة‬**.</span><span class="sxs-lookup"><span data-stu-id="6ce20-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="6ce20-118">إذا لم يتطابق المبلغ في بند الفاتورة مع مبلغ فاتورة الشحن، فيجب تحديد سبب تسوية للفرق.</span><span class="sxs-lookup"><span data-stu-id="6ce20-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="6ce20-119">في حال وجود أسباب متعددة للتسوية، يمكنك تقسيم المبلغ غير المتطابق فيما بينها.</span><span class="sxs-lookup"><span data-stu-id="6ce20-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="6ce20-120">يحدد سبب التسوية كيفية ترحيل مبالغ الفروقات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6ce20-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="6ce20-121">عندما يتم حساب تسوية مبلغ الفاتورة بالكامل، يتم إرساله للموافق عليه، ثم يتم ترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6ce20-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="6ce20-122">يعرض الشكل التوضيحي التالي كيفية إنشاء فاتورة شحن وإجراء تسوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="6ce20-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="6ce20-123">[![مهام تسوية عمليات الشحن](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="6ce20-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="6ce20-124">التسوية التلقائية</span><span class="sxs-lookup"><span data-stu-id="6ce20-124">Automatic reconciliation</span></span>
<span data-ttu-id="6ce20-125">لاستخدام التسوية التلقائية، يجب تحديد جدول للتسوية، والفواتير وشركات الشحن التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="6ce20-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="6ce20-126">تتم مطابقة بنود الفواتير وفواتير الشحن وفقًا لإعداد السجل الرئيسي للتدقيق‬ ونوع فاتورة الشحن.</span><span class="sxs-lookup"><span data-stu-id="6ce20-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="6ce20-127">بعد تشغيل التسوية التلقائية، يجب معالجة الفواتير التي يتعذر على النظام مطابقتها.</span><span class="sxs-lookup"><span data-stu-id="6ce20-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="6ce20-128">بعد ذلك، يجب معالجة هذه الفواتير يدويًا قبل أن تتمكن من ترحيل كافة الفواتير للدفع.</span><span class="sxs-lookup"><span data-stu-id="6ce20-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



