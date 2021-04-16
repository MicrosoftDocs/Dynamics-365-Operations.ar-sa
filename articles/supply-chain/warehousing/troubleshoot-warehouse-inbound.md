---
title: استكشاف أخطاء ‏‫عمليات المستودعات الواردة‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الواردة في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828216"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="ea08e-103">استكشاف أخطاء ‏‫عمليات المستودعات الواردة‬ وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="ea08e-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea08e-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الواردة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ea08e-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="ea08e-105">أتلقى رسالة الخطا التالية: "تم إنشاء أمر الجودة %1.</span><span class="sxs-lookup"><span data-stu-id="ea08e-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="ea08e-106">تعذر العثور على ملف تعريف نظام المجموعة، فيُرجى التحقق من التكوين."</span><span class="sxs-lookup"><span data-stu-id="ea08e-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ea08e-107">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-107">Issue description</span></span>

<span data-ttu-id="ea08e-108">ترتبط رسالة الخطا هذه بعمليه استلام يتم فيها تشغيل أداره الجودة (QMS).</span><span class="sxs-lookup"><span data-stu-id="ea08e-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="ea08e-109">استنادا إلى التكوينات الموجودة في البيئة الخاصة بك ، قد تساعدك التفاصيل الاضافيه حول العملية التي تقوم بإنشاء رسالة الخطا علي إصلاح المشكلة.</span><span class="sxs-lookup"><span data-stu-id="ea08e-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ea08e-110">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-110">Issue resolution</span></span>

<span data-ttu-id="ea08e-111">أولا ، قم بمراجعه [اعداد انتقاء الكتلة](set-up-cluster-picking.md)، وتاكد من اعداد ملفات تعريف المجموعة بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="ea08e-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="ea08e-112">لا يمكنك استخدام عنصر قائمه جهاز المحمول لانتقاء نظام المجموعة ما لم يتم اعداد ملفات تعريف نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ea08e-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="ea08e-113">اعتمادا علي البيئة الخاصة بك ، قد يتوجب عليك أيضا مراجعه التكوينات الأخرى ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="ea08e-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="ea08e-114">لا يعمل استلام لوحه الترخيص المختلط لأي كود ترتيب باستثناء الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="ea08e-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ea08e-115">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-115">Issue description</span></span>

<span data-ttu-id="ea08e-116">عند تعيين حقل **الاجراء** الخاص بكود الترتيب إلى *دائن* أو *خردة*، يمكنك استخدام العنصر الموجود في قائمه [استلام لوح الترخيص المختلط ](mixed-license-plate-receiving.md) لمعالجه الأصناف المرتجعة فقط.</span><span class="sxs-lookup"><span data-stu-id="ea08e-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ea08e-117">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-117">Issue resolution</span></span>

<span data-ttu-id="ea08e-118">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه.</span><span class="sxs-lookup"><span data-stu-id="ea08e-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="ea08e-119">حاليا، [يتم دعم أكواد الترتيب](../service-management/set-up-disposition-codes.md) فقط حيث تم تعيين حقل **الاجراء** إلى *دائن* أو *الخردة* لاستلام لوحه الترخيص المختلط.</span><span class="sxs-lookup"><span data-stu-id="ea08e-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="ea08e-120">عند تشغيل المهمة الدورية لتحديث إيصالات استلام المنتجات ، يتم تاكيد أوامر الشراء غير المؤكدة.</span><span class="sxs-lookup"><span data-stu-id="ea08e-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ea08e-121">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-121">Issue description</span></span>

<span data-ttu-id="ea08e-122">بعد تشغيل المهمة الدورية *تحديث إيصالات استلام المنتجات*، يقوم النظام تلقائيا بتاكيد أوامر الشراء غير المؤكدة التي لها حاله حركه المخزون *المسجلة*.</span><span class="sxs-lookup"><span data-stu-id="ea08e-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ea08e-123">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-123">Issue resolution</span></span>

<span data-ttu-id="ea08e-124">تعمل ميزه معالجه التحميل الواردة الجديدة، *عبر استلام كميات التحميل*، علي إصلاح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="ea08e-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="ea08e-125">لتشغيل هذه الميزة، انتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="ea08e-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="ea08e-126">إقران حركات مخزون أمر الشراء بحمل العمل</span><span class="sxs-lookup"><span data-stu-id="ea08e-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="ea08e-127">استلام زائد لكميات حمل العمل</span><span class="sxs-lookup"><span data-stu-id="ea08e-127">Over receipt of load quantities</span></span>

<span data-ttu-id="ea08e-128">لمزيد من المعلومات ، راجع [ترحيل كميات المنتج المسجلة مقابل أوامر الشراء](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="ea08e-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="ea08e-129">عندما أقوم بتسجيل الطلبات الواردة، أتلقى رسالة الخطأ التالية: "الكمية غير صالحة."</span><span class="sxs-lookup"><span data-stu-id="ea08e-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ea08e-130">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-130">Issue description</span></span>

<span data-ttu-id="ea08e-131">في حالة تعيين حقل **سياسة تجميع لوحات الترخيص** إلى *محدد من قِبل المستخدم* بالنسبة لعنصر قائمة جهاز محمول يتم استخدامه لتسجيل الطلبات الواردة، تتلقى رسالة خطأ ("الكمية غير صالحة")، ولا يمكنك إكمال التسجيل.</span><span class="sxs-lookup"><span data-stu-id="ea08e-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="ea08e-132">سبب المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-132">Issue cause</span></span>

<span data-ttu-id="ea08e-133">وعند استخدام *محدد من قِبل المستخدم* كنهج لتجميع لوح الترخيص، يقوم النظام بتقسيم المخزون الوارد إلى لوحات ترخيص منفصلة، كما هو مشار اليه بواسطة مجموعه تسلسل الوحدات.</span><span class="sxs-lookup"><span data-stu-id="ea08e-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="ea08e-134">إذا تم استخدام أرقام دُفعات أو أرقام تسلسلية لتتبع العنصر الذي يتم استلامه، فيجب تحديد كميات كل دفعة أو مسلسل لكل لوحة ترخيص مسجلة.</span><span class="sxs-lookup"><span data-stu-id="ea08e-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="ea08e-135">إذا تجاوزت الكمية المحددة للوحة الترخيص الكمية التي يجب استلامها للأبعاد الحالية، فستتلقى رسالة الخطأ.</span><span class="sxs-lookup"><span data-stu-id="ea08e-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ea08e-136">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ea08e-136">Issue resolution</span></span>

<span data-ttu-id="ea08e-137">عند تسجيل عنصر باستخدام عنصر قائمة جهاز محمول حيث يتم تعيين حقل **سياسة تجميع لوحات الترخيص** إلى *محدد من قِبل المستخدم*، قد يطلب منك النظام تأكيد أو إدخال أرقام لوحة الترخيص أو أرقام الدُفعات أو الأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="ea08e-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="ea08e-138">في صفحة تأكيد لوحة الترخيص، سيعرض النظام الكمية المخصصة للوحة الترخيص الحالية.</span><span class="sxs-lookup"><span data-stu-id="ea08e-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="ea08e-139">في صفحات التأكيد على الدُفعة أو التسلسل، سيعرض النظام الكمية التي يجب استلامها على لوحة الترخيص الحالية.</span><span class="sxs-lookup"><span data-stu-id="ea08e-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="ea08e-140">سيتضمن أيضًا حقلاً حيث يمكنك إدخال الكمية للتسجيل في تلك المجموعة من لوحة الترخيص والدُفعة أو الرقم التسلسلي.</span><span class="sxs-lookup"><span data-stu-id="ea08e-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="ea08e-141">في هذه الحالة، تأكد من أن الكمية التي يتم تسجيلها للوحة الترخيص لا تتجاوز الكمية التي لا يزال يتعين استلامها.</span><span class="sxs-lookup"><span data-stu-id="ea08e-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="ea08e-142">بدلاً من ذلك، إذا تم إنشاء عدد كبير جدًا من لوحات الترخيص عند تسجيل الأمر الوارد، فإن قيمة **سياسة تجميع لوحات الترخيص** يمكن تغييرها إلى *تجميع لوحات الترخيص*، أو يمكن تعيين مجموعة تسلسل وحدة جديدة للعنصر، أو خيار **تجميع لوحات الترخيص** لمجموعة تسلسل الوحدة يمكن تعطيله.</span><span class="sxs-lookup"><span data-stu-id="ea08e-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
