---
title: استكشاف أخطاء عمليات سير عمل التدبير والتوريد وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع سير عمل التدبير والتوريد.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421794"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="362a3-103">استكشاف أخطاء عمليات سير عمل التدبير والتوريد وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="362a3-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="362a3-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع سير عمل التدبير والتوريد.</span><span class="sxs-lookup"><span data-stu-id="362a3-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="362a3-105">حدث خطأ عند إعادة إرسال أمر شراء إلى سير العمل بعد التغيير: "يُسمح بإجراء تغييرات على أمر الشراء X فقط في حالة المسودة عند تنشيط إدارة التغييرات"</span><span class="sxs-lookup"><span data-stu-id="362a3-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="362a3-106">تحدث هذه المشكلة فقط إذا كانت حالة أمر الشراء *مؤكد* قبل إجراء التغييرات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="362a3-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="362a3-107">إذا طلبت تغييرات بينما حالة أمر الشراء *موافق عليه*، فيمكن معالجة سير العمل بنجاح.</span><span class="sxs-lookup"><span data-stu-id="362a3-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="362a3-108">وصف الخطأ</span><span class="sxs-lookup"><span data-stu-id="362a3-108">Error description</span></span>

<span data-ttu-id="362a3-109">يحدث الخطأ التالي في سير العمل عند إعادة إرسال أمر الشراء بعد إجراء تغيير:</span><span class="sxs-lookup"><span data-stu-id="362a3-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="362a3-110">متوقف (خطـ): استثناء X++: يُسمح بإدخال تغييرات على أمر الشراء PO0000569 فقط بالحالة "مسودة" عند تنشيط إدارة التغييرات عند</span><span class="sxs-lookup"><span data-stu-id="362a3-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="362a3-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="362a3-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="362a3-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="362a3-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="362a3-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="362a3-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="362a3-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="362a3-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="362a3-115">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="362a3-115">Issue resolution</span></span>

<span data-ttu-id="362a3-116">قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="362a3-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="362a3-117">لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="362a3-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="362a3-118">لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="362a3-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="362a3-119">سيتم حل هذه المشكلة من خلال [مقالة قاعدة معارف (KB)‏ Microsoft هذه](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="362a3-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="362a3-120">هناك زيادة أو نقص في التوزيع في توزيع محاسبي واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="362a3-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="362a3-121">قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="362a3-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="362a3-122">لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="362a3-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="362a3-123">لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="362a3-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="362a3-124">إذا تم إلغاء كمية متبقية من التسليم على أمر شراء تم فيه تشغيل إدارة التغييرات، ينتقل أمر الشراء إلى الحالة "مؤكد".</span><span class="sxs-lookup"><span data-stu-id="362a3-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="362a3-125">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="362a3-125">Issue description</span></span>

<span data-ttu-id="362a3-126">بالنسبة لأمر شراء يخضع لإدارة التغييرات، إذا كان التغيير الوحيد المطلوب إلغاء كمية متبقية من التسليم على بند أو أكثر، فسينتقل أمر الشراء بشكل مباشر إلى الحالة *مؤكد* عندما يكون موافقًا عليه، ولن يتم إنشاء دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="362a3-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="362a3-127">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="362a3-127">Issue resolution</span></span>

<span data-ttu-id="362a3-128">لا يؤثر إلغاء الكمية المتبقية من التسليم على محتويات دفتر يومية التأكيد.</span><span class="sxs-lookup"><span data-stu-id="362a3-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="362a3-129">يجب استخدام هذه الوظيفة عند استلام البند بشكل جزئي، ويجب إلغاء جودة الكمية المتبقية في خطوة المعالجة بعد تأكيد أمر الشراء مع المورّد.</span><span class="sxs-lookup"><span data-stu-id="362a3-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="362a3-130">إذا كان يجب أني ينعكس ذلك على تأكيد أمر الشراء، فيجب تعديل الكمية في بند أمر الشراء حتى يكون التأكيد مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="362a3-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="362a3-131">بدلاً من ذلك، إذا لم يتم استلام أي شيء على البند، فيمكن إزالة الكمية.</span><span class="sxs-lookup"><span data-stu-id="362a3-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="362a3-132">في هذه الحالة، ستكون إعادة التأكيد مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="362a3-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="362a3-133">تظهر أوامر الشراء الملغاة في قائمة مسودة في مساحة عمل تجهيز أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="362a3-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="362a3-134">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="362a3-134">Issue description</span></span>

<span data-ttu-id="362a3-135">بعد إلغاء أوامر الشراء التي كانت في الحالة *مؤكد*، يستمر ظهور أوامر الشراء الملغاة في قائمة أوامر الشراء في حالة المسودة في مساحة عمل **تجهيز أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="362a3-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="362a3-136">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="362a3-136">Issue resolution</span></span>

<span data-ttu-id="362a3-137">تحدث هذه المشكلة فقط مع أوامر الشراء التي تخضع لإدارة التغييرات.</span><span class="sxs-lookup"><span data-stu-id="362a3-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="362a3-138">وهي تحدث لأن الإلغاء يُعتبر كتغيير يجب الموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="362a3-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="362a3-139">يمكن إجراء الموافقة بشكل تلقائي بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="362a3-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="362a3-140">وبالتالي، تقضي العملية بأن يتم إرسال أمر الشراء الملغى إلى سير عمل الموافقة بحيث يمكنه الانتقال إلى الحالة *موافق عليه*.</span><span class="sxs-lookup"><span data-stu-id="362a3-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="362a3-141">وفي هذه المرحلة، سيتوقف ظهور أمر الشراء في قائمة أوامر الشراء بحالة المسودة في مساحة عمل **تجهيز أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="362a3-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

