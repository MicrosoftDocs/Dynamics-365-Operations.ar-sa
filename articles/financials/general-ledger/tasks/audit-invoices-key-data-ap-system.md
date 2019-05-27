---
title: " تدقيق الفواتير والبيانات الأساسية في نظام الحسابات الدائنة "
description: عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568838"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="81425-103"> تدقيق الفواتير والبيانات الأساسية في نظام الحسابات الدائنة </span><span class="sxs-lookup"><span data-stu-id="81425-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81425-104">عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع.</span><span class="sxs-lookup"><span data-stu-id="81425-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="81425-105">قبل أن تبدأ، تأكد من تحديد مفتاح تكوين مطابقة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="81425-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="81425-106">في صفحة "محددات الحسابات الدائنة"، تأكد من تحديد الخيار "تمكين التحقق من صحة مطابقة الفاتورة‬"، ومن تعيين الحقل "ترحيل الفاتورة التي بها اختلافات إلى "طلب موافقة‬" ومن تعيين الحقل "سياسة مطابقة البند" إلى "سياسة المطابقة الثلاثية‬".</span><span class="sxs-lookup"><span data-stu-id="81425-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="81425-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="81425-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="81425-108">قد ينفذ دور مدير الحسابات الدائنة أو دور مدير الحسابات‬ هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="81425-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="81425-109">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="81425-109">Create a purchase order</span></span>
1. <span data-ttu-id="81425-110">انتقل إلى **كافة أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="81425-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="81425-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="81425-111">Click **New**.</span></span>
3. <span data-ttu-id="81425-112">في حقل **حساب المورّد**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="81425-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="81425-113">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="81425-113">Click **OK**.</span></span>
5. <span data-ttu-id="81425-114">انقر فوق **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="81425-114">Click **Add line**.</span></span>
6. <span data-ttu-id="81425-115">في حقل **رقم الصنف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="81425-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="81425-116">في جزء الإجراءات، انقر فوق **شراء‬**.</span><span class="sxs-lookup"><span data-stu-id="81425-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="81425-117">انقر فوق **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="81425-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="81425-118">ترحيل إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="81425-118">Post a product receipt</span></span>
1. <span data-ttu-id="81425-119">في جزء الإجراءات، **انقر فوق استلام**.</span><span class="sxs-lookup"><span data-stu-id="81425-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="81425-120">انقر فوق **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="81425-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="81425-121">في حقل **إيصال استلام المنتجات**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="81425-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="81425-122">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="81425-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="81425-123">تسجيل فاتورة مورّد ومطابقتها مع إيصالات استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="81425-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="81425-124">في جزء الإجراءات، انقر فوق **فاتورة > فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="81425-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="81425-125">في حقل **الرقم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="81425-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="81425-126">انقر فوق **افتراضي من: الكمية المطلوبة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="81425-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="81425-127">في حقل **الكمية الافتراضية للبنود**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="81425-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="81425-128">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="81425-128">Click **OK**.</span></span>
6. <span data-ttu-id="81425-129">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="81425-129">Click **Yes**.</span></span>
7. <span data-ttu-id="81425-130">انقر فوق **مطابقة إيصالات استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="81425-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="81425-131">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="81425-131">Click **OK**.</span></span>
9. <span data-ttu-id="81425-132">في جزء الإجراءات، انقر فوق **مراجعة**.</span><span class="sxs-lookup"><span data-stu-id="81425-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="81425-133">انقر فوق **تفاصيل المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="81425-133">Click **Matching details**.</span></span>

