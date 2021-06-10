---
title: تعقب صنف أو مادة خام
description: يوضح هذا الإجراء كيفية استخدام تتبع صنف لتحديد الموقع الذي تم أو يتم به استخدام الأصناف أو المواد الخام.
author: sherry-zheng
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46e46d75ecab3ec2e94372aecfd2c29783756446
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102845"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="c000c-103">تعقب صنف أو مادة خام</span><span class="sxs-lookup"><span data-stu-id="c000c-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c000c-104">يوضح هذا الإجراء كيفية استخدام تتبع صنف لتحديد الموقع الذي تم أو يتم به استخدام الأصناف أو المواد الخام.</span><span class="sxs-lookup"><span data-stu-id="c000c-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="c000c-105">باستخدام هذا الإجراء، يمكنك تحديد صف وتتبعه للخلف المصدر ثم تتبعه للأمام من خلال إنتاج المنتج النهائي وبيعه.</span><span class="sxs-lookup"><span data-stu-id="c000c-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="c000c-106">يمكن استخدام العملية للتحقق من العملاء المتأثرين وأوامر المبيعات المتأثرة والمزيد غير ذلك.</span><span class="sxs-lookup"><span data-stu-id="c000c-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="c000c-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="c000c-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="c000c-108">تتبع صنف للخلف استخدام عدد مجموعة معروف</span><span class="sxs-lookup"><span data-stu-id="c000c-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="c000c-109">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة المخزون > الاستعلامات والتقارير > أبعاد التعقب > تتبع الصنف**.</span><span class="sxs-lookup"><span data-stu-id="c000c-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="c000c-110">في حقل **الصنف**، حدد 'P9100'.</span><span class="sxs-lookup"><span data-stu-id="c000c-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="c000c-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c000c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c000c-112">في الحقل **للأمام أو للخلف**، حدد "للخلف".</span><span class="sxs-lookup"><span data-stu-id="c000c-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="c000c-113">في الحقل **رقم الدفعة**، حدد "كـ-12-344-01".</span><span class="sxs-lookup"><span data-stu-id="c000c-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="c000c-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c000c-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c000c-115">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c000c-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="c000c-116">تحديد صنف وتتبعه إلى الأمام وإجراء تحليل</span><span class="sxs-lookup"><span data-stu-id="c000c-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="c000c-117">تمثل عقدة الشجرة العليا الكمية المتاحة للصنف والمجموعة المحددين.</span><span class="sxs-lookup"><span data-stu-id="c000c-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="c000c-118">إنك بحاجة إلى توسيع عقد الشجرة للبحث عن الصنف الذي سيتم تنفيذ التتبع الأمامي له.</span><span class="sxs-lookup"><span data-stu-id="c000c-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="c000c-119">في الشجرة، قم بتوسيع "العقد الموضحة أدناه، ثم حدد العقدة الأخيرة".</span><span class="sxs-lookup"><span data-stu-id="c000c-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="c000c-120">قم بتوسيع: "P9100 / 1 / 10 / as-12-344-01 ● 2 برميل ● 7.00 جالون \P9100 ● مُنتقى ● أمر المبيعات 000072 ● 12/22/2015 ● -1 برميل ● -4.00 جالون ● موقع=1، مستودع=10، رقم الدفعة =as-12-344-01  \P9100 ● الإنتاج B-000050 ● 12/9/2015● 7 برميل ● 27.00 جالون ● الموقع=1,المستودع=10، رقم الدفعة =as-12-344-01 ● منتجات مساعدة: P9101" ثم حدد العقدة.</span><span class="sxs-lookup"><span data-stu-id="c000c-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="c000c-121">في الشجرة، قم بتوسيع "العقدة الموضحة أدناه، ثم حدد هذه العقدة".</span><span class="sxs-lookup"><span data-stu-id="c000c-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="c000c-122">بدءًا من العقدة التي قمت بتحديدها للتو، قم بتوسيع "M9103 ● خط إنتاج B-000050 ● 12/9/2015 ● -160.00 رطل ● حجم=70, لون=موافق, موقع=1, المستودع=10, رقم الدفعة=App01' ثم حدد العقدة.</span><span class="sxs-lookup"><span data-stu-id="c000c-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="c000c-123">انقر فوق **تتبع من العقدة**.</span><span class="sxs-lookup"><span data-stu-id="c000c-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="c000c-124">انقر فوق **التالي**</span><span class="sxs-lookup"><span data-stu-id="c000c-124">Click **Forward**.</span></span>
5. <span data-ttu-id="c000c-125">في **جزء الإجراءات**، انقر فوق **تتبع**.</span><span class="sxs-lookup"><span data-stu-id="c000c-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="c000c-126">هناك خيارات تتبع عديدة توفر معلومات حول العملاء المتأثرين بالصنف الذي تتبعه وأوامر المبيعات المتعلقة بالصنف الذي لم يتم شحنه.</span><span class="sxs-lookup"><span data-stu-id="c000c-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="c000c-127">انقر فوق **العملاء**.</span><span class="sxs-lookup"><span data-stu-id="c000c-127">Click **Customers**.</span></span>
7. <span data-ttu-id="c000c-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c000c-128">Close the page.</span></span>
8. <span data-ttu-id="c000c-129">في **جزء الإجراءات**، انقر فوق **تتبع**.</span><span class="sxs-lookup"><span data-stu-id="c000c-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="c000c-130">انقر فوق **أوامر المبيعات المشحونة**.</span><span class="sxs-lookup"><span data-stu-id="c000c-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="c000c-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c000c-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]