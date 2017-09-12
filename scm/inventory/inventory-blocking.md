---
title: "حظر المخزون"
description: "توفر هذه المقالة نظرة عامة حول حظر المخزون، الذي يشكل جزءًا من عملية فحص الجودة في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. يمكنك استخدام حظر المخزون لمنع معالجة الأصناف أو استهلاكها."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: eed2f3e203808f378ce954b6cc308859fea89e60
ms.contentlocale: ar-sa
ms.lasthandoff: 09/12/2017

---

# <a name="inventory-blocking"></a><span data-ttu-id="9bcfb-104">حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="9bcfb-104">Inventory blocking</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9bcfb-105">توفر هذه المقالة نظرة عامة حول حظر المخزون، الذي يشكل جزءًا من عملية فحص الجودة في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-105">This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="9bcfb-106">يمكنك استخدام حظر المخزون لمنع معالجة الأصناف أو استهلاكها.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-106">You can use inventory blocking to prevent items from being processed or consumed.</span></span>

<span data-ttu-id="9bcfb-107">يمكنك حظر أصناف المخزون بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="9bcfb-107">You can block inventory items in the following ways:</span></span>
-   <span data-ttu-id="9bcfb-108">يدويًا</span><span class="sxs-lookup"><span data-stu-id="9bcfb-108">Manually</span></span>
-   <span data-ttu-id="9bcfb-109">بإنشاء أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-109">By creating a quality order</span></span>
-   <span data-ttu-id="9bcfb-110">باستخدام عملية إنشاء أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="9bcfb-110">By using a process that generates a quality order</span></span>
-   <span data-ttu-id="9bcfb-111">من خلال استخدام حظر حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="9bcfb-111">By using inventory status blocking</span></span>

## <a name="blocking-items-manually"></a><span data-ttu-id="9bcfb-112">حظر الأصناف يدويًا</span><span class="sxs-lookup"><span data-stu-id="9bcfb-112">Blocking items manually</span></span>
<span data-ttu-id="9bcfb-113">يمكنك حظر كمية صنف ما بإنشاء حركة في صفحة **حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-113">You can block a quantity of an item by creating a transaction on the **Inventory blocking** page.</span></span> <span data-ttu-id="9bcfb-114">يمكن حظر فقط الأصناف المتاحة كمخزون فعلي يدويًا.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-114">Only items that are available as on-hand inventory can be blocked manually.</span></span> <span data-ttu-id="9bcfb-115">وبالنسبة للكميات المحظورة يدوياً، يجب عليك تحديد ما إذا كانت أنشطة التخطيط تتضمن إيصالات الاستلام المتوقعة ككمية فعلية متوقعة.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-115">For manually blocked quantities, you must decide whether planning activities include expected receipts as an expected on-hand quantity.</span></span> <span data-ttu-id="9bcfb-116">عمليات الاستلام المتوقعة هي الأصناف المحظورة المتوقع أن تكون متوفرة كمخزون فعلى بعد الفحص.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-116">Expected receipts are blocked items that you expect to be available as on-hand inventory after inspection is completed.</span></span> <span data-ttu-id="9bcfb-117">يمكنك الاحتفاظ بالتاريخ المتوقع.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-117">You can maintain the expected date.</span></span> <span data-ttu-id="9bcfb-118">وبشكل افتراضي، يتم تحديد خيار **إيصالات الاستلام المتوقعة** للأصناف التي يتم حظرها من خلال أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-118">By default, the **Expected receipts** option is selected for items that are blocked through a quality order.</span></span> <span data-ttu-id="9bcfb-119">يمكنك إلغاء حظر يدوي في كمية عن طريق حذف الحركة الموجودة في صفحة **حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-119">You can cancel a manual block on a quantity by deleting the transaction on the **Inventory blocking** page.</span></span>

## <a name="blocking-items-by-creating-a-quality-order"></a><span data-ttu-id="9bcfb-120">حظر الأصناف بإنشاء أمر جودة</span><span class="sxs-lookup"><span data-stu-id="9bcfb-120">Blocking items by creating a quality order</span></span>
<span data-ttu-id="9bcfb-121">يمكنك تحديد العناصر التي يجب فحصها قبل إنشاء أمر جودة في صفحة **أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-121">You can specify items that must be inspected by creating a quality order on the **Quality orders** page.</span></span> <span data-ttu-id="9bcfb-122">عند إنشاء أمر جودة، يتم حظر الكمية التي تحددها لصنف.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-122">When you create a quality order, the quantity that you specify for an item is blocked.</span></span> <span data-ttu-id="9bcfb-123">وتتحكم خطة أخذ العينات المرتبطة بأمر جودة فقط في كمية الأصناف التي يجب فحصها، وليس الكمية التي يتم حظرها.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-123">The sampling plan that is associated with a quality order controls only the quantity of items that must be inspected, not the quantity that is blocked.</span></span> <span data-ttu-id="9bcfb-124">والكمية التي يتم إدخالها في أمر الجودة هي الكمية التي يتم حظرها، بغض النظر عن الكمية التي تحدد خطة أخذ العينات وجوب إرسالها للفحص.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-124">The quantity that is entered on the quality order is the quantity that is blocked, regardless of the quantity that the sampling plan specifies should be sent for inspection.</span></span>

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a><span data-ttu-id="9bcfb-125">حظر الأصناف باستخدام عملية إنشاء أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="9bcfb-125">Blocking items by using a process that generates a quality order</span></span>
<span data-ttu-id="9bcfb-126">إذا كانت عملية جودة تحدد صنفًا يجب فحصه، فإنه يتم حظر كمية الصنف تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-126">If a quality process specifies that an item must be inspected, a quantity of the item is blocked automatically.</span></span> <span data-ttu-id="9bcfb-127">ولذلك، عندما يتم إنشاء أمر جودة تلقائياً، تتحكم خطة أخذ عينات الصنف المقترنة بأمر الجودة في كلٍّ من كمية الأصناف المحظورة والكمية التي يجب فحصها.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-127">Therefore, when a quality order is generated automatically, the item sampling plan that is associated with the quality order controls the both quantity of items that is blocked and the quantity that must be inspected.</span></span> <span data-ttu-id="9bcfb-128">إذا تم تحديد خيار **الحظر الكامل** في صفحة **أخذ عينات الأصناف**، فإنه يتم حظر الكمية الكاملة لبند أمر شراء مثلاً أثناء الفحص، بغض النظر عن كمية أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-128">If the **Full blocking** option on the **Item sampling** page is selected, the full quantity of, for example, a purchase order line is blocked during inspection, regardless of the item sampling quantity.</span></span>
### <a name="example"></a><span data-ttu-id="9bcfb-129">مثال</span><span class="sxs-lookup"><span data-stu-id="9bcfb-129">Example</span></span>

<span data-ttu-id="9bcfb-130">في المثال التالي، يتم إنشاء أمر جودة عند ترحيل إيصال تعبئة خاص بأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-130">In the following example, a quality order is generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="9bcfb-131">في صفحة **عمليات اقتران الجودة‬**، حددت أنت ترحيل إيصال التعبئة الخاص بأمر الشراء بأنها العملية التي تقوم بتنشيط أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-131">On the **Quality associations** page, you specified that posting of a purchase order packing slip is the process that activates a quality order.</span></span>

|<span data-ttu-id="9bcfb-132">إعداد</span><span class="sxs-lookup"><span data-stu-id="9bcfb-132">Setup</span></span>                                                                     |<span data-ttu-id="9bcfb-133">إجراء المستخدم</span><span class="sxs-lookup"><span data-stu-id="9bcfb-133">User action</span></span>                 |<span data-ttu-id="9bcfb-134">النتيجة</span><span class="sxs-lookup"><span data-stu-id="9bcfb-134">Result</span></span>             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| <span data-ttu-id="9bcfb-135">تحدد اقتران الجودة أن أمر الجودة يجب إنشاؤه عند ترحيل إيصال تعبئة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-135">A quality association specifies that a quality order must be generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="9bcfb-136">ويحدد إعداد أخذ عينات الصنف لأمر الجودة أنه يمكن فحص 10 بالمائة من الكمية الموجودة في بند أمر الشراء الذي يجب فحصه.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-136">The item sampling setup of the quality order specifies that 10 percent of the quantity on the purchase order line must be inspected.</span></span> <span data-ttu-id="9bcfb-137">علاوةً على ذلك، ونظرًا لتحديد **الحظر الكامل** في إعداد أخذ عينات الصنف، يجب حظر الكمية الكاملة لسطر أمر الشراء أثناء الفحص، بغض النظر عن الكمية التي يتم إرسالها للفحص.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-137">Furthermore, because the **Full blocking** option selected in the item sampling setup, the full quantity of the purchase order line must be blocked during inspection, regardless of the quantity that is sent for inspection.</span></span> | <span data-ttu-id="9bcfb-138">تم ترحيل إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-138">The packing slip is posted.</span></span> | <span data-ttu-id="9bcfb-139">تم إنشاء أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-139">A quality order is generated.</span></span> <span data-ttu-id="9bcfb-140">تم إرسال عشرة بالمائة من كمية أمر الشراء للصنف للفحص.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-140">Ten percent of the purchase order quantity for the item is sent to inspection.</span></span> <span data-ttu-id="9bcfb-141">تم حظر الكمية الكاملة من سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-141">The full quantity of the purchase order line is blocked.</span></span> |

## <a name="blocking-items-by-using-inventory-status-blocking"></a><span data-ttu-id="9bcfb-142">حظر الأصناف من خلال استخدام حظر حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="9bcfb-142">Blocking items by using inventory status blocking</span></span>
<span data-ttu-id="9bcfb-143">يمكنك تحديد حالات المخزون التي هي حالات حظر باستخدام معلمة **حظر المخزون** في صفحة **حالات المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-143">You can specify which inventory statuses are blocking statuses by using the **Inventory blocking** parameter on the **Inventory statuses** page.</span></span> <span data-ttu-id="9bcfb-144">لا يمكنك استخدام حالات المخزون كحالات حظر لأوامر الإنتاج، أو أوامر المبيعات، أو أوامر التحويل، أو الحركات الصادرة، أو عمليات دمج المشاريع.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-144">You can't use inventory statuses as blocking statuses for production orders, sales orders, transfer orders, outbound transactions, or project integrations.</span></span> <span data-ttu-id="9bcfb-145">وبالنسبة للعمل الصادر، استخدم أصنافًا بحالة مخزون متوفر.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-145">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="9bcfb-146">إذا كانت الأصناف حالة **معطلة** والتخطيط الرئيسي يعمل على هذه الأصناف، تعتبر الأصناف مفقودة، ويتم تزويد المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="9bcfb-146">If items have a status of **Broken**, and master planning is run on those items, the items are considered missing, and inventory is automatically replenished.</span></span>



<a name="see-also"></a><span data-ttu-id="9bcfb-147">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="9bcfb-147">See also</span></span>
--------

[<span data-ttu-id="9bcfb-148">إنشاء وصيانة حظر المخزون (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="9bcfb-148">Create and maintain an inventory blocking (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-maintain-inventory-blocking)

[<span data-ttu-id="9bcfb-149">عمليات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="9bcfb-149">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="9bcfb-150">فحص جودة البضائع (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="9bcfb-150">Inspect the quality of goods (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/inventory/tasks/inspect-quality-goods)

