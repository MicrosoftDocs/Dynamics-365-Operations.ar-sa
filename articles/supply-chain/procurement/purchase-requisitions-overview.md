---
title: "نظرة عامة على طلب الشراء"
description: "يوضح هذا الموضوع سير عمل طلب الشراء والحالات المختلفة التي يمكن أن يكون بها طلب شراء."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b96a89bcabdaa3e3a3be3786dda15f9725f5a50d
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-requisition-overview"></a><span data-ttu-id="1dc45-103">نظرة عامة على طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-103">Purchase requisition overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1dc45-104">يوضح هذا الموضوع سير عمل طلب الشراء والحالات المختلفة التي يمكن أن يكون بها طلب شراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-104">This topic describes the purchase requisition workflow and the different statuses that a purchase requisition can have.</span></span>

<span data-ttu-id="1dc45-105">استنادًا إلى إعداد مؤسستك، يمكنك إنشاء طلبات شراء للمنتجات التي تستخدمها مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="1dc45-105">Depending on the setup of your organization, you can create purchase requisitions for products that your organization uses.</span></span> <span data-ttu-id="1dc45-106">ويعتبر طلب الشراء مستندًا داخليًا حيث يخول قسم الشراء ليقوم بشراء الأصناف أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="1dc45-106">A purchase requisition is an internal document that authorizes the Purchasing department to buy items or services.</span></span>  

<span data-ttu-id="1dc45-107">بعد الموافقة على طلب شراء، يمكن استخدامه لإنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-107">After a purchase requisition is approved, it can be used to generate a purchase order.</span></span> <span data-ttu-id="1dc45-108">تعتبر أوامر الشراء مستندات خارجية حيث يقدمها قسم الشراء إلى الموردين.</span><span class="sxs-lookup"><span data-stu-id="1dc45-108">Purchase orders are the external documents that the Purchasing department submits to vendors.</span></span>

## <a name="creating-purchase-requisitions"></a><span data-ttu-id="1dc45-109">إنشاء طلبات الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-109">Creating purchase requisitions</span></span>
<span data-ttu-id="1dc45-110">ويمكنك إنشاء طلب شراء في صفحة **طلبات الشراء الخاصة بي**، وتحديد الأصناف والخدمات التي تحتاجها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-110">You can create a purchase requisition on the **My purchase requisitions** page, and select the items and services that you require.</span></span> <span data-ttu-id="1dc45-111">ويمكنك تحديد الأصناف من كتالوج التدبير الذي قامت بإنشائه المؤسسة الخاصة بك، أو يمكنك طلب الأصناف غير الموجودة في كتالوج عن طريق تحديد فئة تدبير وإدخال تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="1dc45-111">You can select items from a procurement catalog that your organization has created, or you can request items that aren't found in a catalog by selecting a procurement category and entering the product details.</span></span>  

<span data-ttu-id="1dc45-112">وقبل أن تتمكن من تقديم طلب شراء للمراجعة، يجب تكوين عمليات سير العمل في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1dc45-112">Before you can submit a purchase requisition for review, workflows must be configured in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1dc45-113">يمكنك استخدام سير العمل لنقل طلب شراء من خلال عملية المراجعة، من الحالة الأولية **مسودة** إلى الحالة النهائية **معتمدة**.</span><span class="sxs-lookup"><span data-stu-id="1dc45-113">You use a workflow to move a purchase requisition through the review process, from an initial status of **Draft** to a final status of **Approved**.</span></span>

### <a name="purchase-requisition-statuses"></a><span data-ttu-id="1dc45-114">حالات طلبات الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-114">Purchase requisition statuses</span></span>

<span data-ttu-id="1dc45-115">عند إنشاء طلب شراء، يتم تعيين حالة له.</span><span class="sxs-lookup"><span data-stu-id="1dc45-115">When you create a purchase requisition, a status is assigned to it.</span></span> <span data-ttu-id="1dc45-116">كما يتم تعيين حالة لكل بند تقوم بإضافته إلى طلب شراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-116">A status is also assigned to every line that you add to a purchase requisition.</span></span> <span data-ttu-id="1dc45-117">وعند إرسال طلب شراء إلى سير عمل للمراجعة، يتم تحديث حالة طلب الشراء وحالة كل بند لأن البنود تتحرك من خلال عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="1dc45-117">When you submit a purchase requisition to a workflow for review, the status of the purchase requisition and the status of each line are updated as the lines move through the workflow process.</span></span>  

<span data-ttu-id="1dc45-118">ويمكنك تكوين عملية سير عمل طلب الشراء لتوجيه طلب شراء خلال عملية المراجعة كمستند واحد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-118">You can configure the purchase requisition workflow process to route a purchase requisition through the review process as a single document.</span></span> <span data-ttu-id="1dc45-119">وبدلاً من ذلك، يمكن توجيه بنود طلب الشراء بشكل فردي إلى المراجعين المناسبين.</span><span class="sxs-lookup"><span data-stu-id="1dc45-119">Alternatively, the lines on a purchase requisition can be routed individually to the appropriate reviewers.</span></span> <span data-ttu-id="1dc45-120">وفي حالة مراجعة بنود طلب الشراء كلُّ على حدة، يمكن تحديث حالة كل بند طلب شراء نظرًا لتحرك البند خلال عملية المراجعة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-120">If the purchase requisition lines are reviewed individually, the status of each purchase requisition line can be updated as the line moves through the review process.</span></span> <span data-ttu-id="1dc45-121">وعند اكتمال مراجعة جميع البنود في عملية المراجعة وعد بقاء أي خطوات مراجعة لطلب الشراء، يتم تحديث حالة الشراء بالكامل.</span><span class="sxs-lookup"><span data-stu-id="1dc45-121">When all lines have completed the review process and no review steps remain for the purchase requisition, the status of the whole purchase requisition is updated.</span></span>

### <a name="purchase-requisition-workflow"></a><span data-ttu-id="1dc45-122">سير عمل طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-122">Purchase requisition workflow</span></span>

<span data-ttu-id="1dc45-123">يوضح الرسم التخطيطي التالي الحالات التي تم تعيينها لطلب شراء وبند طلب شراء عند تحركها خلال عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="1dc45-123">The following diagram shows the statuses that are assigned to a purchase requisition and a purchase requisition line as they move through the workflow process.</span></span>  

<span data-ttu-id="1dc45-124">[![حالات بند ورأس طلب الشراء](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)</span><span class="sxs-lookup"><span data-stu-id="1dc45-124">[![Purchase requisition header and line statuses](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)</span></span>

### <a name="purchase-requisition-header-and-line-status-relationships"></a><span data-ttu-id="1dc45-125">علاقات حالات بند ورأس طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-125">Purchase requisition header and line status relationships</span></span>

<span data-ttu-id="1dc45-126">يتم تحديد الحالة العامة لطلب الشراء بواسطة حالة بنود طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-126">The overall status of a purchase requisition is determined by the status of the purchase requisition lines.</span></span> <span data-ttu-id="1dc45-127">ولذلك، إن عملية المراجعة يجب أن تتم لجميع بنود طلب الشراء قبل أن يصبح إتمام عملية المراجعة لطلب الشراء بالكامل ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="1dc45-127">Therefore, the review process must be completed for all purchase requisition lines before the review process for the whole purchase requisition can be completed.</span></span> <span data-ttu-id="1dc45-128">يوضح الجدول التالي الحالات التي تم تعيينها لرأس وبنود طلب شراء عند تحرك طلب الشراء خلال عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="1dc45-128">The following table describes the statuses that are assigned to a purchase requisition header and lines as the purchase requisition moves through the workflow process.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1dc45-129">حالة طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-129">Purchase requisition status</span></span></th>
<th><span data-ttu-id="1dc45-130">حالة بند طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-130">Purchase requisition line status</span></span></th>
<th><span data-ttu-id="1dc45-131">الوصف</span><span class="sxs-lookup"><span data-stu-id="1dc45-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1dc45-132">المسودة</span><span class="sxs-lookup"><span data-stu-id="1dc45-132">Draft</span></span></td>
<td><span data-ttu-id="1dc45-133">المسودة</span><span class="sxs-lookup"><span data-stu-id="1dc45-133">Draft</span></span></td>
<td><span data-ttu-id="1dc45-134">تم إنشاء طلب الشراء وبند طلب الشراء، ولكن لم يتم إرساله للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-134">The purchase requisition and purchase requisition line have been created, but they haven't been submitted for review.</span></span> <span data-ttu-id="1dc45-135">يمكن تعديل طلبات الشراء وبنود طلبات الشراء التي بالحالة <strong>مسودة</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dc45-135">Purchase requisitions and purchase requisition lines that have a status of <strong>Draft</strong> can be modified.</span></span> <span data-ttu-id="1dc45-136">تكون طلبات الشراء وبنود طلبات الشراء بالحالة <strong>مسودة</strong> إذا تم استدعاؤها ولكن لم تتم إعادة إرسالها للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-136">A purchase requisition or purchase requisition line also has a status of <strong>Draft</strong> if it has been recalled but hasn't been resubmitted for review.</span></span> <span data-ttu-id="1dc45-137"><strong>ملاحظة:</strong> يمكنك إرسال أو استدعاء طلب شراء على مستوى المستند.</span><span class="sxs-lookup"><span data-stu-id="1dc45-137"><strong>Note:</strong> You can submit or recall a purchase requisition at the document level.</span></span> <span data-ttu-id="1dc45-138">ومع ذلك، لا يمكن إرسال أو استدعاء بند طلب شراء واحد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-138">However, you can't submit or recall a single purchase requisition line.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dc45-139">قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="1dc45-139">In review</span></span></td>
<td><ul>
<li><span data-ttu-id="1dc45-140">قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="1dc45-140">In review</span></span></li>
<li><span data-ttu-id="1dc45-141">تم الرفض</span><span class="sxs-lookup"><span data-stu-id="1dc45-141">Rejected</span></span></li>
</ul></td>
<td><span data-ttu-id="1dc45-142">إذا تم تكوين سير العمل لتوجيه بنود طلب الشراء للمراجعين المنفردين، يمكن أن يكون كل بند بحالة <strong>قيد المراجعة</strong> أو <strong>مرفوض</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dc45-142">If the workflow has been configured to route purchase requisition lines to individual reviewers, each line can have a status of <strong>In review</strong> or <strong>Rejected</strong>.</span></span> <span data-ttu-id="1dc45-143">ويتم تحديث حالة طلب الشراء عند اكتمال عملية المراجعة لجميع بنود طلب الشراء وعم بقاء أي خطوات مراجعة لطلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-143">The purchase requisition status is updated when the review process is completed for all purchase requisition lines and no review steps remain for the purchase requisition.</span></span>
<ul>
<li><span data-ttu-id="1dc45-144"><strong>قيد المراجعة</strong> – تم إرسال بنود طلبات الشراء للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-144"><strong>In review</strong> – The purchase requisition lines have been submitted for review.</span></span> <span data-ttu-id="1dc45-145">عند اكتمال عملية سير العمل لبند طلب شراء، تظل حالة هذا البند <strong>قيد المراجعة</strong> حتى تتم مراجعة كافة بنود طلبات الشراء المتبقية.</span><span class="sxs-lookup"><span data-stu-id="1dc45-145">When the workflow process is completed for a purchase requisition line, the status of that line remains <strong>In review</strong> until all remaining purchase requisition lines have been reviewed.</span></span></li>
<li><span data-ttu-id="1dc45-146"><strong>مرفوض‬‏‫</strong> – تم رفض بند طلب شراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-146"><strong>Rejected</strong> – A purchase requisition line has been rejected.</span></span> <span data-ttu-id="1dc45-147">ويمكن تعديل بنود طلبات الشراء التي تم رفضها وإعادة إرسالها.‬</span><span class="sxs-lookup"><span data-stu-id="1dc45-147">Purchase requisition lines that are rejected can be modified and resubmitted.</span></span></li>
</ul>
<span data-ttu-id="1dc45-148">في حالة إعادة إرسال بند طلب شراء قد تم رفضه، تبدأ عملية المراجعة لكافة البنود الموجودة في طلب الشراء الذي لا يزال قيد المراجعة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-148">If you resubmit a purchase requisition line that has been rejected, the review process starts over for all lines in the purchase requisition that are still in review.</span></span> <span data-ttu-id="1dc45-149"><strong>ملاحظة:</strong> يمكنك استدعاء طلب شراء تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="1dc45-149"><strong>Note:</strong> You can recall a purchase requisition that has already been submitted.</span></span> <span data-ttu-id="1dc45-150">وعند استدعاء طلب شراء، يتم أيضًا استدعاء كافة بنود طلبات الشراء الأخرى.</span><span class="sxs-lookup"><span data-stu-id="1dc45-150">When you recall a purchase requisition, all other purchase requisition lines are also recalled.</span></span> <span data-ttu-id="1dc45-151">يمكن حذف بنود طلبات الشراء التي تم استدعاؤها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-151">Purchase requisition lines that have been recalled can be deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dc45-152">تم الرفض</span><span class="sxs-lookup"><span data-stu-id="1dc45-152">Rejected</span></span></td>
<td><span data-ttu-id="1dc45-153">تم الرفض</span><span class="sxs-lookup"><span data-stu-id="1dc45-153">Rejected</span></span></td>
<td><span data-ttu-id="1dc45-154">تم رفض طلب الشراء وجميع بنود طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-154">The purchase requisition and all purchase requisition lines have been rejected.</span></span> <span data-ttu-id="1dc45-155">يمكن إعادة إرسال طلبات الشراء وبنود طلبات الشراء التي تم رفضها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-155">Purchase requisitions and purchase requisition lines that have been rejected can be resubmitted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dc45-156">تمت الموافقة عليه</span><span class="sxs-lookup"><span data-stu-id="1dc45-156">Approved</span></span></td>
<td><ul>
<li><span data-ttu-id="1dc45-157">تمت الموافقة عليه</span><span class="sxs-lookup"><span data-stu-id="1dc45-157">Approved</span></span></li>
<li><span data-ttu-id="1dc45-158">ملغى</span><span class="sxs-lookup"><span data-stu-id="1dc45-158">Cancelled</span></span></li>
<li><span data-ttu-id="1dc45-159">‏‏مغلق</span><span class="sxs-lookup"><span data-stu-id="1dc45-159">Closed</span></span></li>
</ul></td>
<td><span data-ttu-id="1dc45-160">اكتملت عملية مراجعة جميع بنود طلب الشراء، وليست هناك أي خطوات مراجعة أخرى لطلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-160">All purchase requisition lines have completed the review process, and there are no more review steps for the purchase requisition.</span></span>
<ul>
<li><span data-ttu-id="1dc45-161"><strong>معتمدة</strong> – قد اكتملت عملية مراجعة بند طلب الشراء وتمت الموافقة على البند.</span><span class="sxs-lookup"><span data-stu-id="1dc45-161"><strong>Approved</strong> – The review process for a purchase requisition line has been completed, and the line is approved.</span></span></li>
<li><span data-ttu-id="1dc45-162"><strong>ملغي</strong> – تم اعتماد بند طلب الشراء، ولكن تم إلغاؤه لأنه لم يعد مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="1dc45-162"><strong>Cancelled</strong> – The purchase requisition line was approved, but it has been canceled because it's no longer required.</span></span> <span data-ttu-id="1dc45-163">يمكن إلغاء بنود طلبات الشراء فقط التي تم اعتمادها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-163">Only purchase requisition lines that have been approved can be canceled.</span></span></li>
<li><span data-ttu-id="1dc45-164"><strong>مغلق</strong> – تم اعتماد بند طلب الشراء وتم إنشاء المستندات، استناداً إلى الغرض من الطلب.</span><span class="sxs-lookup"><span data-stu-id="1dc45-164"><strong>Closed</strong> – The purchase requisition line was approved, and documents have been generated, depending on the requisition purpose.</span></span>
<ul>
<li><span data-ttu-id="1dc45-165">إذا كان الغرض من الطلب هو الاستهلاك، فإنه تم إنشاء أمر شراء لبند طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-165">If the requisition purpose is consumption, a purchase order has been generated for the purchase requisition line.</span></span></li>
<li><span data-ttu-id="1dc45-166">إذا كان الغرض من الطلب هو التزويد، يتم إنشاء مستند تنفيذ واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="1dc45-166">If the requisition purpose is replenishment, one or more fulfillment documents have been generated.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dc45-167">ملغى</span><span class="sxs-lookup"><span data-stu-id="1dc45-167">Cancelled</span></span></td>
<td><span data-ttu-id="1dc45-168">ملغى</span><span class="sxs-lookup"><span data-stu-id="1dc45-168">Cancelled</span></span></td>
<td><span data-ttu-id="1dc45-169">تم إلغاء طلب الشراء وجميع بنود طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-169">The purchase requisition and all purchase requisition lines have been canceled.</span></span> <span data-ttu-id="1dc45-170"><strong>ملاحظة:</strong> إذا لم تعد تحتاج إلى صنف موجود في بند طلب شراء، يجب عليك إلغاء بند طلب الشراء في حالة الموافقة عليه مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="1dc45-170"><strong>Note:</strong> If you no longer require an item that is on a purchase requisition line, you must cancel the purchase requisition line if it has already been approved.</span></span> <span data-ttu-id="1dc45-171">يمكن إلغاء بنود طلبات الشراء فقط التي تم اعتمادها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-171">Only purchase requisition lines that have been approved can be canceled.</span></span> <span data-ttu-id="1dc45-172">إذا كانت أية بنود طلب شراء قيد المراجعة، فسيكون طلب الشراء بحالة <strong>قيد المراجعة</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dc45-172">If any purchase requisition lines are in review, the purchase requisition will have a status of <strong>In review</strong>.</span></span> <span data-ttu-id="1dc45-173">وفي هذه الحالة، يمكنك استعادة طلب الشراء وحذف بند طلب الشراء المناسب.</span><span class="sxs-lookup"><span data-stu-id="1dc45-173">In this case, you can recall the purchase requisition and delete the appropriate purchase requisition line.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dc45-174">‏‏مغلق</span><span class="sxs-lookup"><span data-stu-id="1dc45-174">Closed</span></span></td>
<td><ul>
<li><span data-ttu-id="1dc45-175">‏‏مغلق</span><span class="sxs-lookup"><span data-stu-id="1dc45-175">Closed</span></span></li>
<li><span data-ttu-id="1dc45-176">ملغى</span><span class="sxs-lookup"><span data-stu-id="1dc45-176">Cancelled</span></span></li>
</ul></td>
<td><span data-ttu-id="1dc45-177">تم إغلاق طلب الشراء، وتم إنشاء مستند تنفيذ واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="1dc45-177">The purchase requisition is closed, and one or more fulfillment documents have been generated.</span></span>
<ul>
<li><span data-ttu-id="1dc45-178"><strong>مغلق</strong> – تم اعتماد بند طلب الشراء وتم إنشاء المستندات، استناداً إلى الغرض من الطلب.</span><span class="sxs-lookup"><span data-stu-id="1dc45-178"><strong>Closed</strong> – The purchase requisition line was approved, and documents have been generated, depending on the requisition purpose.</span></span>
<ul>
<li><span data-ttu-id="1dc45-179">إذا كان الغرض من الطلب هو الاستهلاك، فإنه تم إنشاء أمر شراء لبند طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-179">If the requisition purpose is consumption, a purchase order has been generated for the purchase requisition line.</span></span></li>
<li><span data-ttu-id="1dc45-180">إذا كان الغرض من الطلب هو التزويد، يتم إنشاء مستند تنفيذ واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="1dc45-180">If the requisition purpose is replenishment, one or more fulfillment documents have been generated.</span></span></li>
</ul></li>
<li><span data-ttu-id="1dc45-181"><strong>ملغي</strong> – تم اعتماد بند طلب الشراء، ولكن تم إلغاؤه لأنه لم يعد مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="1dc45-181"><strong>Cancelled</strong> – The purchase requisition line was approved, but it has been canceled because it's no longer required.</span></span> <span data-ttu-id="1dc45-182">يمكن إلغاء بنود طلبات الشراء فقط التي تم اعتمادها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-182">Only purchase requisition lines that have been approved can be canceled.</span></span></li>
</ul><span data-ttu-id="1dc45-183">
<strong>ملاحظة:</strong> إذا لم تعد تحتاج إلى صنف في بند طلب شراء تم إغلاقه، يجب إلغاء البند في مستند التنفيذ الذي تم إنشاؤه لبند طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-183">
<strong>Note:</strong> If you no longer require an item on a purchase requisition line that has been closed, you must cancel the line on the fulfillment document that was generated for the purchase requisition line.</span></span></td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a><span data-ttu-id="1dc45-184">توزيع التكاليف على حسابات مالية متعددة</span><span class="sxs-lookup"><span data-stu-id="1dc45-184">Distributing costs to multiple financial accounts</span></span>
<span data-ttu-id="1dc45-185">يمكنك توزيع تكلفة المنتجات المضمنة في طلب شراء إلى عدة حسابات مالية.</span><span class="sxs-lookup"><span data-stu-id="1dc45-185">You can distribute the cost of a product that is included in a purchase requisition to multiple financial accounts.</span></span> <span data-ttu-id="1dc45-186">إذا كانت مؤسستك تستخدم الأبعاد، مثل مراكز التكلفة والأقسام، فيمكنك توزيع تكلفة المنتج إلى الأبعاد للحسابات المالية.</span><span class="sxs-lookup"><span data-stu-id="1dc45-186">If your organization uses dimensions, such as cost centers and departments, you can distribute the cost of a product to dimensions for financial accounts.</span></span>

## <a name="requisition-purposes"></a><span data-ttu-id="1dc45-187">أغراض الطلب</span><span class="sxs-lookup"><span data-stu-id="1dc45-187">Requisition purposes</span></span>
<span data-ttu-id="1dc45-188">أغراض الطلب تجعل عملية الوفاء بطلب الشراء أكثر مرونة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-188">Requisition purposes make the process of fulfilling requisition demand more flexible.</span></span> <span data-ttu-id="1dc45-189">عند إنشاء الطلب، يمكنك تعيين غرضًا أو غرضين له: الاستهلاك أو التجديد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-189">When you create a requisition, you can assign one of two purposes to it: consumption or replenishment.</span></span> <span data-ttu-id="1dc45-190">وتبعاً لغرض الطلب وإعداد المؤسسة الخاصة بك، يمكن الوفاء بطلب الشراء عن طريق أمر شراء أو أمر تحويل أو أمر إنتاج أو كانبان.‬</span><span class="sxs-lookup"><span data-stu-id="1dc45-190">Depending on the requisition purpose and the setup of your organization, requisition demand can be fulfilled by a purchase order, transfer order, production order, or kanban.</span></span>  

<span data-ttu-id="1dc45-191">وفي سياسات التدبير، يمكنك التحكم في أغراض الطلب المتوفرة عند إنشاء طلب للمؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1dc45-191">In the procurement policies, you can control the requisition purposes that are available when a requisition is created for your organization.</span></span>

### <a name="requisitions-that-have-a-purpose-of-consumption"></a><span data-ttu-id="1dc45-192">الطلبات التي لها غرض الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="1dc45-192">Requisitions that have a purpose of consumption</span></span>

<span data-ttu-id="1dc45-193">طلب له غرض الاستهلاك يمثل طلبًا على الأصناف أو الخدمات التي سيتم استخدامها داخليًا بالمؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1dc45-193">A requisition that has a purpose of consumption represents demand for items or services that will be used internally by your organization.</span></span> <span data-ttu-id="1dc45-194">الطلب الذي يتم إنشاؤه بواسطة هذا النوع من الطلبات يتم استيفاؤه دائمًا بأمر شراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-194">The demand that is created by this kind of requisition is always fulfilled by a purchase order.</span></span> <span data-ttu-id="1dc45-195">إذا تم إعداد Microsoft Dynamics 365 for Finance and Operations. لإنشاء أوامر شراء تلقائيًا، فسيتم إنشاء أوامر الشراء بعد الموافقة على طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-195">If Microsoft Dynamics 365 for Finance and Operations is set up to automatically generate purchase orders, purchase orders are created after the purchase requisition is approved.</span></span>

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a><span data-ttu-id="1dc45-196">الطلبات التي لها غرض تجديد</span><span class="sxs-lookup"><span data-stu-id="1dc45-196">Requisitions that have a purpose of replenishment</span></span>

<span data-ttu-id="1dc45-197">يمثل الطلب الذي له غرض تجديد مطلبًا بتجديد المخزون.</span><span class="sxs-lookup"><span data-stu-id="1dc45-197">A requisition that has a purpose of replenishment represents demand to replenish inventory.</span></span> <span data-ttu-id="1dc45-198">على سبيل المثال، تُنشئ طلبًا لتزويد الأصناف لكي يمكن بيعها في موقع معين للبيع بالتجزئة في وقت معين.</span><span class="sxs-lookup"><span data-stu-id="1dc45-198">For example, you create a requisition to replenish items so that they can be sold at a specific retail location at a specific time.</span></span> <span data-ttu-id="1dc45-199">ويمكن الوفاء بالطلب الذي تم إنشاؤه بواسطة نوع الطلب هذا من خلال أمر الشراء، أو أمر النقل، أو أمر الإنتاج، أو كانبان.</span><span class="sxs-lookup"><span data-stu-id="1dc45-199">The demand that is created by this kind of requisition can be fulfilled by a purchase order, transfer order, production order, or kanban.</span></span>  

<span data-ttu-id="1dc45-200">عندما يكون غرض الطلب التجديد، يتم التعبير عن المطلب ككمية بدلاً من مبلغ نقدي.</span><span class="sxs-lookup"><span data-stu-id="1dc45-200">When the requisition purpose is replenishment, demand is expressed as a quantity instead of a monetary amount.</span></span> <span data-ttu-id="1dc45-201">بالتالي، لا تنطبق حسابات الالتزام، ومراقبة الميزانية، وقواعد العمل الخاصة بتحديد الأصول الثابتة (BRAD)، وحسابات المشروع، وأية قواعد ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-201">Therefore, encumbrance accounting, budgetary control, business rules for fixed asset determination (BRAD), project accounting, and any related rules don't apply.</span></span> <span data-ttu-id="1dc45-202">يمكن فقط للمنتجات التي يتم تخزينها وإطلاقها للكيان القانوني المحدد تلبية مطلب طلب التجديد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-202">Only products that are stocked and released to the specified legal entity can fulfill replenishment requisition demand.</span></span> <span data-ttu-id="1dc45-203">لتحديد المنتجات التي تتوفر عندما يكون غرض الطلب هو التزويد، استخدم صفحة **قاعدة سياسة الوصول إلى فئة التتزويد**.</span><span class="sxs-lookup"><span data-stu-id="1dc45-203">To define the products that are available when the requisition purpose is replenishment, use the **Replenishment category access policy rule** page.</span></span>  

<span data-ttu-id="1dc45-204">ولاستخدام طلبات الشراء التي لها غرض التزويد، يجب عليك إعداد الجدولة الرئيسية لتضمين طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-204">To use purchase requisitions that have a purpose of replenishment, you must set up master scheduling to include requisition demand.</span></span> <span data-ttu-id="1dc45-205">ويتم تحديد أسلوب تنفيذ الطلب الذي تم إنشاؤه بواسطة نوع الطلب هذا تلقائياً فيما بعد، استنادًا إلى سياسات التوريد التي تم إعدادها للأصناف في مؤسستك والمخططة باستخدام الجدولة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="1dc45-205">The fulfillment method for the demand that is created by this kind of requisition is then determined automatically, based on the supply policies that have been set up for the items in your organization and planned by using master scheduling.</span></span>

## <a name="purchase-requisitions-and-requests-for-quotation"></a><span data-ttu-id="1dc45-206">طلبات الشراء وطلبات عرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="1dc45-206">Purchase requisitions and requests for quotation</span></span>
<span data-ttu-id="1dc45-207">في بعض الحالات، يجب عليك بدء عملية طلب عرض الأسعار (RFQ) لتحديد المورد والسعر للمنتجات المطلوبة في طلب شراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-207">In some cases, you must start a request for quotation (RFQ) process to identify the vendor and price for products that are requested in a purchase requisition.</span></span> <span data-ttu-id="1dc45-208">ويمكن إنشاء طلب عرض الأسعار عندما يكون طلب الشراء قيد المراجعة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-208">An RFQ can be generated when the purchase requisition is in review.</span></span> <span data-ttu-id="1dc45-209">وعند قبول عطاء، يتم تحويل معلومات حول المورد والسعر وغير ذلك للطلب.</span><span class="sxs-lookup"><span data-stu-id="1dc45-209">When you accept a bid, information about the vendor, price, and so on, is transferred to the requisition.</span></span>  

<span data-ttu-id="1dc45-210">‏‫ويمكنك احتجاز طلب شراء عن طريق تحديد خانة الاختيار **‬‏‫قيد الاحتجاز** في صفحة **تفاصيل طلب الشراء**.</span><span class="sxs-lookup"><span data-stu-id="1dc45-210">You can put a purchase requisition on hold by selecting the **On hold** check box on the **Purchase requisition details** page.</span></span> <span data-ttu-id="1dc45-211">ولا يمكن متابعة معالجة طلب الشراء إلا بعد إزالة الاحتجاز عن طريق إلغاء تحديد خانة الاختيار.‬</span><span class="sxs-lookup"><span data-stu-id="1dc45-211">Processing of the purchase requisition can continue only after you remove the hold by clearing the check box.</span></span>  

<span data-ttu-id="1dc45-212">**ملاحظة:** في التدبير الإلكتروني، قد يسمح طلب عرض الأسعار لطلب الشراء الخاص بك لموردين بإضافة بنود بديلة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-212">**Note:** In eProcurement, the RFQ for your purchase requisition might allow vendors to add alternate lines.</span></span> <span data-ttu-id="1dc45-213">وفي هذه الحالة، سيعكس طلب الشراء الخاص بك البدائل المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-213">In this case, your purchase requisition will reflect approved alternates.</span></span>

## <a name="demand-consolidation"></a><span data-ttu-id="1dc45-214">توحيد الطلب</span><span class="sxs-lookup"><span data-stu-id="1dc45-214">Demand consolidation</span></span>
<span data-ttu-id="1dc45-215">بواسطة تجميع بنود طلبات الشراء من طلبات شراء متعددة، يمكنك زيادة القوة التفاوضية الخاصة بك مع الموردين للحصول على أسعار أفضل وتكاليف شحن ومعالجة مخفضة، وخفض التكاليف العامة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-215">By consolidating purchase requisition lines from multiple purchase requisitions, you can increase your negotiating power with your vendors to achieve better pricing, lower shipping and handling costs, and reduced overhead costs.</span></span>  

<span data-ttu-id="1dc45-216">بنود طلب الشراء مؤهلة لتوحيد الطلبات فقط إذا كانت العبارات التالية صحيحة:</span><span class="sxs-lookup"><span data-stu-id="1dc45-216">Purchase requisition lines are eligible for demand consolidation only if the following statements are true:</span></span>

-   <span data-ttu-id="1dc45-217">تم اعتماد طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="1dc45-217">The purchase requisition has been approved.</span></span>
-   <span data-ttu-id="1dc45-218">طلب الشراء يتوافق مع معايير قاعدة نهج الشراء للمعالجة اليدوية وتوحيد الطلبات.</span><span class="sxs-lookup"><span data-stu-id="1dc45-218">The purchase requisition meets the purchasing policy rule criteria for manual processing and demand consolidation.</span></span>

<span data-ttu-id="1dc45-219">يتم سرد بنود طلبات الشراء المعتمدة التي تفي بمعايير المعالجة اليدوية في صفحة **إصدار طلبات الشراء المعتمدة**.</span><span class="sxs-lookup"><span data-stu-id="1dc45-219">Approved purchase requisition lines that meet the criteria for manual processing are listed on the **Release approved purchase requisitions** page.</span></span> <span data-ttu-id="1dc45-220">إذا كان بند طلب الشراء يتوافق أيضًا مع معايير توحيد الطلبات، يمكن إضافة البند إلى فرصة توحيد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-220">If a purchase requisition line also meets the criteria for demand consolidation, the line can be added to a consolidation opportunity.</span></span>  

<span data-ttu-id="1dc45-221">وفرصة التوحيد هي مجموعة من بنود طلبات الشراء التي تم تجميعها معًا بحيث يمكن لمحترف الشراء التفاوض على أفضل صفقة مع الموردين.</span><span class="sxs-lookup"><span data-stu-id="1dc45-221">A consolidation opportunity is a set of purchase requisition lines that are grouped together, so that the purchasing professional can negotiate the best deal with vendors.</span></span> <span data-ttu-id="1dc45-222">وتظهر بنود طلب الشراء الذي يتم تحديده لفرصة توحيد صفحة **توحيد طلبات الشراء**.</span><span class="sxs-lookup"><span data-stu-id="1dc45-222">Purchase requisition lines that you select for a consolidation opportunity appear on the **Purchase requisition consolidation** page.</span></span> <span data-ttu-id="1dc45-223">ويمكنك تعديل البنود في هذه الصفحة، إذا كانت التغييرات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-223">You can modify the lines on this page, if changes are required.</span></span> <span data-ttu-id="1dc45-224">كما يمكنك إضافة بنود جديدة إلى فرصة التوحيد أو إزالة البنود الموجودة منها.</span><span class="sxs-lookup"><span data-stu-id="1dc45-224">You can also add new lines to the consolidation opportunity or remove existing lines.</span></span>  

<span data-ttu-id="1dc45-225">وبعد إضافة بنود الطلب لفرصة التوحيد وإجراء التغييرات التي تحتاجها، يمكنك إنشاء أمر شراء لبنود طلب الشراء الموحدة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-225">After you add requisition lines to a consolidation opportunity and make any changes that you require, you can create a purchase order for the consolidated purchase requisition lines.</span></span>  

<span data-ttu-id="1dc45-226">**ملاحظة:**تنعكس التغييرات التي تجريها على بند طلب الشراء في صفحة **تويحد طلب الشراء** في أمر الشراء الذي تقوم بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="1dc45-226">**Note:** Changes that you make to a purchase requisition line on the **Purchase requisition consolidation** page are reflected on the purchase order that you create.</span></span> <span data-ttu-id="1dc45-227">ومع ذلك، يبقى البند دون تغيير في طلب الشراء، بحيث يتم الاحتفاظ بالسجل الخاص به.</span><span class="sxs-lookup"><span data-stu-id="1dc45-227">However, the line remains unchanged in the purchase requisition, so that its history is preserved.</span></span>  

<span data-ttu-id="1dc45-228">ولإنشاء أمر شراء لبنود طلب الشراء غير المؤهلة لتوحيد الطلبات أو التي لم يتم تحديدها لفرصة توحيد، يجب عليك معالجة البنود يدويًا.</span><span class="sxs-lookup"><span data-stu-id="1dc45-228">To create a purchase order for purchase requisition lines that aren't eligible for demand consolidation or aren't selected for a consolidation opportunity, you must process the lines manually.</span></span>

### <a name="consolidating-purchase-requisition-lines"></a><span data-ttu-id="1dc45-229">توحيد بنود طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-229">Consolidating purchase requisition lines</span></span>

<span data-ttu-id="1dc45-230">تبدأ عملية توحيد الطلبات التي يتم فيها اعتماد طلب شراء في سير العمل وتسجيل حجوزات الموازنة والالتزامات المسبقة، إذا تم تكوين التحكم في الموازنة للمؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1dc45-230">The process for demand consolidation starts when a purchase requisition is approved in a workflow and, if budget control is configured for your organization, when the budget reservations and pre-encumbrances have been recorded.</span></span> <span data-ttu-id="1dc45-231">ويوضح الرسم التخطيطي التالي عملية التدفق لتوحيد الطلبات.</span><span class="sxs-lookup"><span data-stu-id="1dc45-231">The following diagram shows the process flow for demand consolidation.</span></span>  

<span data-ttu-id="1dc45-232">[![تدفق العملية لتوحيد الطلبات](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)</span><span class="sxs-lookup"><span data-stu-id="1dc45-232">[![Process flow for demand consolidation](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)</span></span>  

<span data-ttu-id="1dc45-233">لدمج بنود طلب شراء معتمدة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="1dc45-233">To consolidate approved purchase requisition lines, follow these steps:</span></span>

1.  <span data-ttu-id="1dc45-234">مراجعة بنود الطلب المعتمدة التي تم احتجازها للمعالجة اليدوية والتي تكون مؤهلة لتوحيد الطلبات.</span><span class="sxs-lookup"><span data-stu-id="1dc45-234">Review approved requisition lines that have been held for manual processing, and that are eligible for demand consolidation.</span></span>
2.  <span data-ttu-id="1dc45-235">تحديد البنود لإضافتها لفرصة توحيد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-235">Select lines to add to a consolidation opportunity.</span></span>
3.  <span data-ttu-id="1dc45-236">إنشاء فرصة توحيد جديدة أو إضافة بنود طلب إلى فرصة توحيد موجودة.</span><span class="sxs-lookup"><span data-stu-id="1dc45-236">Create a new consolidation opportunity, or add requisition lines to an existing consolidation opportunity.</span></span>
4.  <span data-ttu-id="1dc45-237">تطبيق أية تغييرات مطلوبة في بنود الطلب، وإزالة أصناف بند الطلب التي لم تعد تريد تضمينها في فرصة التوحيد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-237">Make any required changes to the requisition lines, and remove requisition line items that you no longer want to include in the consolidation opportunity.</span></span>
5.  <span data-ttu-id="1dc45-238">إنشاء أوامر شراء لبنود الطلبات الموحدة أو لبنود طلبات الشراء في فرصة التوحيد.</span><span class="sxs-lookup"><span data-stu-id="1dc45-238">Create purchase orders for consolidated requisition lines or for purchase requisition lines in a consolidation opportunity.</span></span>


<a name="see-also"></a><span data-ttu-id="1dc45-239">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="1dc45-239">See also</span></span>
--------

[<span data-ttu-id="1dc45-240">إنشاء طلب للاستهلاك (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="1dc45-240">Create a requisition for consumption (Task guide)</span></span>](tasks/create-requisition-consumption.md)

[<span data-ttu-id="1dc45-241">سير عمل طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="1dc45-241">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




