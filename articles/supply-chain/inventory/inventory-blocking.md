---
title: "حظر المخزون"
description: "توفر هذه المقالة نظرة عامة حول حظر المخزون، الذي يشكل جزءًا من عملية فحص الجودة في Microsoft Dynamics 365 for Finance and Operations. يمكنك استخدام حظر المخزون لمنع معالجة الأصناف أو استهلاكها."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: eb6291e2f012f148b247b747f84155b96cf09677
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="inventory-blocking"></a><span data-ttu-id="d5501-104">حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="d5501-104">Inventory blocking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5501-105">توفر هذه المقالة نظرة عامة حول حظر المخزون، الذي يشكل جزءًا من عملية فحص الجودة في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5501-105">This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d5501-106">يمكنك استخدام حظر المخزون لمنع معالجة الأصناف أو استهلاكها.</span><span class="sxs-lookup"><span data-stu-id="d5501-106">You can use inventory blocking to prevent items from being processed or consumed.</span></span>

<span data-ttu-id="d5501-107">يمكنك حظر أصناف المخزون بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="d5501-107">You can block inventory items in the following ways:</span></span>
-   <span data-ttu-id="d5501-108">يدويًا</span><span class="sxs-lookup"><span data-stu-id="d5501-108">Manually</span></span>
-   <span data-ttu-id="d5501-109">بإنشاء أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="d5501-109">By creating a quality order</span></span>
-   <span data-ttu-id="d5501-110">باستخدام عملية إنشاء أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="d5501-110">By using a process that generates a quality order</span></span>
-   <span data-ttu-id="d5501-111">من خلال استخدام حظر حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="d5501-111">By using inventory status blocking</span></span>

## <a name="blocking-items-manually"></a><span data-ttu-id="d5501-112">حظر الأصناف يدويًا</span><span class="sxs-lookup"><span data-stu-id="d5501-112">Blocking items manually</span></span>
<span data-ttu-id="d5501-113">يمكنك حظر كمية صنف ما بإنشاء حركة في صفحة **حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="d5501-113">You can block a quantity of an item by creating a transaction on the **Inventory blocking** page.</span></span> <span data-ttu-id="d5501-114">يمكن حظر فقط الأصناف المتاحة كمخزون فعلي يدويًا.</span><span class="sxs-lookup"><span data-stu-id="d5501-114">Only items that are available as on-hand inventory can be blocked manually.</span></span> <span data-ttu-id="d5501-115">وبالنسبة للكميات المحظورة يدوياً، يجب عليك تحديد ما إذا كانت أنشطة التخطيط تتضمن إيصالات الاستلام المتوقعة ككمية فعلية متوقعة.</span><span class="sxs-lookup"><span data-stu-id="d5501-115">For manually blocked quantities, you must decide whether planning activities include expected receipts as an expected on-hand quantity.</span></span> <span data-ttu-id="d5501-116">عمليات الاستلام المتوقعة هي الأصناف المحظورة المتوقع أن تكون متوفرة كمخزون فعلى بعد الفحص.</span><span class="sxs-lookup"><span data-stu-id="d5501-116">Expected receipts are blocked items that you expect to be available as on-hand inventory after inspection is completed.</span></span> <span data-ttu-id="d5501-117">يمكنك الاحتفاظ بالتاريخ المتوقع.</span><span class="sxs-lookup"><span data-stu-id="d5501-117">You can maintain the expected date.</span></span> <span data-ttu-id="d5501-118">وبشكل افتراضي، يتم تحديد خيار **إيصالات الاستلام المتوقعة** للأصناف التي يتم حظرها من خلال أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="d5501-118">By default, the **Expected receipts** option is selected for items that are blocked through a quality order.</span></span> <span data-ttu-id="d5501-119">يمكنك إلغاء حظر يدوي في كمية عن طريق حذف الحركة الموجودة في صفحة **حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="d5501-119">You can cancel a manual block on a quantity by deleting the transaction on the **Inventory blocking** page.</span></span>

## <a name="blocking-items-by-creating-a-quality-order"></a><span data-ttu-id="d5501-120">حظر الأصناف بإنشاء أمر جودة</span><span class="sxs-lookup"><span data-stu-id="d5501-120">Blocking items by creating a quality order</span></span>
<span data-ttu-id="d5501-121">يمكنك تحديد العناصر التي يجب فحصها قبل إنشاء أمر جودة في صفحة **أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="d5501-121">You can specify items that must be inspected by creating a quality order on the **Quality orders** page.</span></span> <span data-ttu-id="d5501-122">عند إنشاء أمر جودة، يتم حظر الكمية التي تحددها لصنف.</span><span class="sxs-lookup"><span data-stu-id="d5501-122">When you create a quality order, the quantity that you specify for an item is blocked.</span></span> <span data-ttu-id="d5501-123">وتتحكم خطة أخذ العينات المرتبطة بأمر جودة فقط في كمية الأصناف التي يجب فحصها، وليس الكمية التي يتم حظرها.</span><span class="sxs-lookup"><span data-stu-id="d5501-123">The sampling plan that is associated with a quality order controls only the quantity of items that must be inspected, not the quantity that is blocked.</span></span> <span data-ttu-id="d5501-124">والكمية التي يتم إدخالها في أمر الجودة هي الكمية التي يتم حظرها، بغض النظر عن الكمية التي تحدد خطة أخذ العينات وجوب إرسالها للفحص.</span><span class="sxs-lookup"><span data-stu-id="d5501-124">The quantity that is entered on the quality order is the quantity that is blocked, regardless of the quantity that the sampling plan specifies should be sent for inspection.</span></span>

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a><span data-ttu-id="d5501-125">حظر الأصناف باستخدام عملية إنشاء أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="d5501-125">Blocking items by using a process that generates a quality order</span></span>
<span data-ttu-id="d5501-126">إذا كانت عملية جودة تحدد صنفًا يجب فحصه، فإنه يتم حظر كمية الصنف تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="d5501-126">If a quality process specifies that an item must be inspected, a quantity of the item is blocked automatically.</span></span> <span data-ttu-id="d5501-127">ولذلك، عندما يتم إنشاء أمر جودة تلقائياً، تتحكم خطة أخذ عينات الصنف المقترنة بأمر الجودة في كلٍّ من كمية الأصناف المحظورة والكمية التي يجب فحصها.</span><span class="sxs-lookup"><span data-stu-id="d5501-127">Therefore, when a quality order is generated automatically, the item sampling plan that is associated with the quality order controls the both quantity of items that is blocked and the quantity that must be inspected.</span></span> <span data-ttu-id="d5501-128">إذا تم تحديد خيار **الحظر الكامل** في صفحة **أخذ عينات الأصناف**، فإنه يتم حظر الكمية الكاملة لبند أمر شراء مثلاً أثناء الفحص، بغض النظر عن كمية أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="d5501-128">If the **Full blocking** option on the **Item sampling** page is selected, the full quantity of, for example, a purchase order line is blocked during inspection, regardless of the item sampling quantity.</span></span>
### <a name="example"></a><span data-ttu-id="d5501-129">مثال</span><span class="sxs-lookup"><span data-stu-id="d5501-129">Example</span></span>

<span data-ttu-id="d5501-130">في المثال التالي، يتم إنشاء أمر جودة عند ترحيل إيصال تعبئة خاص بأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d5501-130">In the following example, a quality order is generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="d5501-131">في صفحة **عمليات اقتران الجودة‬**، حددت أنت ترحيل إيصال التعبئة الخاص بأمر الشراء بأنها العملية التي تقوم بتنشيط أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="d5501-131">On the **Quality associations** page, you specified that posting of a purchase order packing slip is the process that activates a quality order.</span></span>

|<span data-ttu-id="d5501-132">إعداد</span><span class="sxs-lookup"><span data-stu-id="d5501-132">Setup</span></span>                                                                     |<span data-ttu-id="d5501-133">إجراء المستخدم</span><span class="sxs-lookup"><span data-stu-id="d5501-133">User action</span></span>                 |<span data-ttu-id="d5501-134">النتيجة</span><span class="sxs-lookup"><span data-stu-id="d5501-134">Result</span></span>             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| <span data-ttu-id="d5501-135">تحدد اقتران الجودة أن أمر الجودة يجب إنشاؤه عند ترحيل إيصال تعبئة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d5501-135">A quality association specifies that a quality order must be generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="d5501-136">ويحدد إعداد أخذ عينات الصنف لأمر الجودة أنه يمكن فحص 10 بالمائة من الكمية الموجودة في بند أمر الشراء الذي يجب فحصه.</span><span class="sxs-lookup"><span data-stu-id="d5501-136">The item sampling setup of the quality order specifies that 10 percent of the quantity on the purchase order line must be inspected.</span></span> <span data-ttu-id="d5501-137">علاوةً على ذلك، ونظرًا لتحديد **الحظر الكامل** في إعداد أخذ عينات الصنف، يجب حظر الكمية الكاملة لسطر أمر الشراء أثناء الفحص، بغض النظر عن الكمية التي يتم إرسالها للفحص.</span><span class="sxs-lookup"><span data-stu-id="d5501-137">Furthermore, because the **Full blocking** option selected in the item sampling setup, the full quantity of the purchase order line must be blocked during inspection, regardless of the quantity that is sent for inspection.</span></span> | <span data-ttu-id="d5501-138">تم ترحيل إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="d5501-138">The packing slip is posted.</span></span> | <span data-ttu-id="d5501-139">تم إنشاء أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="d5501-139">A quality order is generated.</span></span> <span data-ttu-id="d5501-140">تم إرسال عشرة بالمائة من كمية أمر الشراء للصنف للفحص.</span><span class="sxs-lookup"><span data-stu-id="d5501-140">Ten percent of the purchase order quantity for the item is sent to inspection.</span></span> <span data-ttu-id="d5501-141">تم حظر الكمية الكاملة من سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d5501-141">The full quantity of the purchase order line is blocked.</span></span> |

## <a name="blocking-items-by-using-inventory-status-blocking"></a><span data-ttu-id="d5501-142">حظر الأصناف من خلال استخدام حظر حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="d5501-142">Blocking items by using inventory status blocking</span></span>
<span data-ttu-id="d5501-143">يمكنك تحديد حالات المخزون التي هي حالات حظر باستخدام معلمة **حظر المخزون** في صفحة **حالات المخزون**.</span><span class="sxs-lookup"><span data-stu-id="d5501-143">You can specify which inventory statuses are blocking statuses by using the **Inventory blocking** parameter on the **Inventory statuses** page.</span></span> <span data-ttu-id="d5501-144">لا يمكنك استخدام حالات المخزون كحالات حظر لأوامر الإنتاج، أو أوامر المبيعات، أو أوامر التحويل، أو الحركات الصادرة، أو عمليات دمج المشاريع.</span><span class="sxs-lookup"><span data-stu-id="d5501-144">You can't use inventory statuses as blocking statuses for production orders, sales orders, transfer orders, outbound transactions, or project integrations.</span></span> <span data-ttu-id="d5501-145">وبالنسبة للعمل الصادر، استخدم أصنافًا بحالة مخزون متوفر.</span><span class="sxs-lookup"><span data-stu-id="d5501-145">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="d5501-146">إذا كانت الأصناف حالة **معطلة** والتخطيط الرئيسي يعمل على هذه الأصناف، تعتبر الأصناف مفقودة، ويتم تزويد المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="d5501-146">If items have a status of **Broken**, and master planning is run on those items, the items are considered missing, and inventory is automatically replenished.</span></span>



<a name="additional-resources"></a><span data-ttu-id="d5501-147">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d5501-147">Additional resources</span></span>
--------

[<span data-ttu-id="d5501-148">إنشاء وصيانة حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="d5501-148">Create and maintain an inventory blocking</span></span>](tasks/create-maintain-inventory-blocking.md)

[<span data-ttu-id="d5501-149">عمليات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="d5501-149">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="d5501-150">فحص جودة البضائع (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="d5501-150">Inspect the quality of goods (Task guide)</span></span>](tasks/inspect-quality-goods.md)

