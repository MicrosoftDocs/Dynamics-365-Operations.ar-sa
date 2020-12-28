---
title: استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645108"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="f33e6-103">استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="f33e6-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f33e6-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f33e6-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="f33e6-105">أتلقى رسالة الخطأ " لا يمكن إزالة الحجوزات نظرًا لوجود عمل مُنشأ يعتمد على الحجوزات".‬</span><span class="sxs-lookup"><span data-stu-id="f33e6-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f33e6-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-106">Issue description</span></span>

<span data-ttu-id="f33e6-107">لا يمكنك إلغاء حجز المخزون في بند مبيعات ، نظرا لوجود عمل مفتوح للبند.</span><span class="sxs-lookup"><span data-stu-id="f33e6-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f33e6-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-108">Issue resolution</span></span>

<span data-ttu-id="f33e6-109">التحقق من وجود عمل مجموعه التعبئة المفتوحة لإحضار الصنف من محطه تعبئة إلى موقع آخر (مثل *باب الخليج*).</span><span class="sxs-lookup"><span data-stu-id="f33e6-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="f33e6-110">قم بمراجعه السجلات الموجودة في الصفحتين **سجل محفوظات إنشاء العمل** و **وتفاصيل العمل** لتحديد ما يقوم بحجز المخزون فعليا ، ثم قم بإكمال العمل أو حذفه لتحرير الحجز.</span><span class="sxs-lookup"><span data-stu-id="f33e6-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="f33e6-111">أتلقى رسالة الخطا التالية: "تعذر تحديث كميه المخزون- %1 بسبب عدم كفاية حركات المخزون للصنف %2 ...."</span><span class="sxs-lookup"><span data-stu-id="f33e6-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f33e6-112">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-112">Issue description</span></span>

<span data-ttu-id="f33e6-113">قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة.</span><span class="sxs-lookup"><span data-stu-id="f33e6-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="f33e6-114">فيما يلي نص رسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="f33e6-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="f33e6-115">تعذر تحديثكميه المخزون - %1 بسبب عدم كفاية حركات المخزون الخاصة بالصنف %2 ذي حجم الابعاد = %3، اللون = %4، الإضافات = %5، الموقع = %6، المستودع = %7، الموقع = %8، حاله المخزون = متاح، لوح الترخيص = %9، رقم المجموعة = %10 لمعرف المرجع %11 في معرف الشحنة %12.</span><span class="sxs-lookup"><span data-stu-id="f33e6-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f33e6-116">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-116">Issue resolution</span></span>

<span data-ttu-id="f33e6-117">تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية.</span><span class="sxs-lookup"><span data-stu-id="f33e6-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="f33e6-118">علي سبيل المثال ، قد تقوم هذه الحركات بفتح أوامر الجودة أو سجلات حظر المخزون أو أوامر المخرجات.</span><span class="sxs-lookup"><span data-stu-id="f33e6-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="f33e6-119">أتلقى رسالة الخطا التالية: "الفعلي... لا يمكن حجزه لان 0.00 فقط متاح في المخزون. "</span><span class="sxs-lookup"><span data-stu-id="f33e6-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f33e6-120">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-120">Issue description</span></span>

<span data-ttu-id="f33e6-121">قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة.</span><span class="sxs-lookup"><span data-stu-id="f33e6-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="f33e6-122">فيما يلي نص رسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="f33e6-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="f33e6-123">موقع الفعلي = %1، المستودع = %2، حاله المخزون = متاح، رقم المجموعة = %3، المالك = %4 : لا يمكن حجز %5 نظرا لتوفر 0.00 فقط في المخزون.</span><span class="sxs-lookup"><span data-stu-id="f33e6-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f33e6-124">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-124">Issue resolution</span></span>

<span data-ttu-id="f33e6-125">قد يكون سبب هذه المشكلة هو فتح العمل.</span><span class="sxs-lookup"><span data-stu-id="f33e6-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="f33e6-126">قم اما بإكمال العمل أو الاستلام دون إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="f33e6-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="f33e6-127">تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية.</span><span class="sxs-lookup"><span data-stu-id="f33e6-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="f33e6-128">علي سبيل المثال ، قد تكون هذه الحركات أوامر جودة مفتوحة أو سجلات حظر المخزون أو أوامر المخرجات.</span><span class="sxs-lookup"><span data-stu-id="f33e6-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="f33e6-129">أتلقى رسالة الخطا التالية: "لتعيينها إلى موجه ، يجب ان تحدد سطور التحميل الابعاد فوق الموقع.</span><span class="sxs-lookup"><span data-stu-id="f33e6-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="f33e6-130">لتعيين هذه الابعاد ، قم بحجز بند التحميل وأعاده إنشائه. "</span><span class="sxs-lookup"><span data-stu-id="f33e6-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f33e6-131">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-131">Issue description</span></span>

<span data-ttu-id="f33e6-132">عند استخدام صنف يحتوي علي "مجموعه أعلى" تدرج هرمي للحجز (مع وضع البعد **رقم المجموعة** *فوق* بعد **الموقع**)، لا يعمل الأمر **إصدار إلى مستودع** في الصفحة **منضدة تخطيط التحميل** الخاصة بالكمية الجزئية.</span><span class="sxs-lookup"><span data-stu-id="f33e6-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="f33e6-133">تظهر رسالة الخطا هذه ، ولا يتم إنشاء اي عمل للكمية الجزئية.</span><span class="sxs-lookup"><span data-stu-id="f33e6-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="f33e6-134">عند استخدام صنف يحتوي علي "مجموعه أعلى" تدرج هرمي للحجز (مع وضع البعد **رقم المجموعة** *أسفل* بعد **الموقع**)، لا يعمل الأمر إصدار إلى مستودع في الصفحة **منضدة تخطيط التحميل** الخاصة بالكمية الجزئية.</span><span class="sxs-lookup"><span data-stu-id="f33e6-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f33e6-135">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f33e6-135">Issue resolution</span></span>

<span data-ttu-id="f33e6-136">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="f33e6-136">This behavior is by design.</span></span> <span data-ttu-id="f33e6-137">إذا قمت بوضع بعد فوق بعد **الموقع** في التدرج الهرمي للحجز ، فيجب تحديده قبل إصدار المستودع.</span><span class="sxs-lookup"><span data-stu-id="f33e6-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="f33e6-138">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه اثناء الإصدارات إلى المستودع من منضدة تخطيط التحميل.</span><span class="sxs-lookup"><span data-stu-id="f33e6-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="f33e6-139">لا يمكن إصدار الكميات الجزئية في حاله عدم تحديد واحده أو أكثر من الابعاد الموجودة اعلي **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="f33e6-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="f33e6-140">لمزيد من المعلومات، راجع [سياسة مرنة لحجز البعد على مستوى المستودع](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="f33e6-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
