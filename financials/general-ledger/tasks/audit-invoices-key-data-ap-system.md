--- 
title: "تدقيق الفواتير والبيانات الأساسية في الحسابات الدائنة"
description: "عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 095001a74566e0246951ad9631a8076c72b84f1c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="ecae7-103">تدقيق الفواتير والبيانات الأساسية في الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="ecae7-103">Audit invoices and key data in accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecae7-104">عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع.</span><span class="sxs-lookup"><span data-stu-id="ecae7-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="ecae7-105">قبل أن تبدأ، تأكد من تحديد مفتاح تكوين مطابقة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="ecae7-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="ecae7-106">في صفحة "محددات الحسابات الدائنة"، تأكد من تحديد الخيار "تمكين التحقق من صحة مطابقة الفاتورة‬"، ومن تعيين الحقل "ترحيل الفاتورة التي بها اختلافات إلى "طلب موافقة‬" ومن تعيين الحقل "سياسة مطابقة البند" إلى "سياسة المطابقة الثلاثية‬".</span><span class="sxs-lookup"><span data-stu-id="ecae7-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="ecae7-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="ecae7-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="ecae7-108">قد ينفذ دور مدير الحسابات الدائنة أو دور مدير الحسابات‬ هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ecae7-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="ecae7-109">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="ecae7-109">Create a purchase order</span></span>
1. <span data-ttu-id="ecae7-110">انتقل إلى "كافة أوامر الشراء".</span><span class="sxs-lookup"><span data-stu-id="ecae7-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="ecae7-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ecae7-111">Click New.</span></span>
3. <span data-ttu-id="ecae7-112">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ecae7-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ecae7-113">في الحقل "حساب المورّد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ecae7-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="ecae7-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ecae7-114">Click OK.</span></span>
6. <span data-ttu-id="ecae7-115">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ecae7-115">Click Add line.</span></span>
7. <span data-ttu-id="ecae7-116">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ecae7-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="ecae7-117">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="ecae7-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="ecae7-118">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="ecae7-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="ecae7-119">ترحيل إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ecae7-119">Post a product receipt</span></span>
1. <span data-ttu-id="ecae7-120">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="ecae7-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="ecae7-121">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="ecae7-121">Click Product receipt.</span></span>
3. <span data-ttu-id="ecae7-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ecae7-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ecae7-123">في الحقل "إيصال استلام المنتجات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ecae7-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="ecae7-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ecae7-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="ecae7-125">تسجيل فاتورة مورّد ومطابقتها مع إيصالات استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ecae7-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="ecae7-126">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="ecae7-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="ecae7-127">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="ecae7-127">Click Invoice.</span></span>
3. <span data-ttu-id="ecae7-128">في الحقل "الرقم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ecae7-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="ecae7-129">انقر فوق افتراضي من: "الكمية المطلوبة" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="ecae7-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="ecae7-130">في الحقل "الكمية الافتراضية للبنود"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="ecae7-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="ecae7-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ecae7-131">Click OK.</span></span>
7. <span data-ttu-id="ecae7-132">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="ecae7-132">Click Yes.</span></span>
8. <span data-ttu-id="ecae7-133">انقر فوق "مطابقة إيصالات استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="ecae7-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="ecae7-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ecae7-134">Click OK.</span></span>
10. <span data-ttu-id="ecae7-135">في جزء الإجراءات، انقر فوق "مراجعة".</span><span class="sxs-lookup"><span data-stu-id="ecae7-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="ecae7-136">انقر فوق "تفاصيل المطابقة".</span><span class="sxs-lookup"><span data-stu-id="ecae7-136">Click Matching details.</span></span>


