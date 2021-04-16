---
title: استكشاف الأخطاء وإصلاحها في التدرجات الهرمية للحجوزات الدُفعية والتسلسلية
description: يصف هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع التدرجات الهرمية للحجز التي تستخدم أبعاد الدُفعات أو التسلسلية.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838168"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="73909-103">استكشاف الأخطاء وإصلاحها في التدرجات الهرمية للحجوزات الدُفعية والتسلسلية</span><span class="sxs-lookup"><span data-stu-id="73909-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73909-104">يصف هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع التدرجات الهرمية للحجز التي تستخدم أبعاد الدُفعات أو التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="73909-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="73909-105">لمزيد من المعلومات، راجع [سياسة مرنة لحجز البعد على مستوى المستودع](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="73909-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="73909-106">يحدد التسلسل الهرمي للحجز الخاص بالصنف متطلبات أبعاد التخزين التي يجب الوفاء بها لتعيين موقع لأمر الطلب.</span><span class="sxs-lookup"><span data-stu-id="73909-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="73909-107">يمكن وصف هذه الابعاد *كابعاد أعلى الموقع*، وذلك لكافة الابعاد التي يجب تحقيقها قبل تعيين الموقع، و *الابعاد أسفل الموقع*، للابعاد التي يمكن تخصيصها بعد تعيين موقع لأمر الطلب.</span><span class="sxs-lookup"><span data-stu-id="73909-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="73909-108">وتعرف التدرجات الهرمية للحجز هذه باسم التردجات الهرمية لحجز *الدفعة-أعلى* و *الدفعة-أسفل* أو التدرجات الهرمية لحجز *التسلسل-أعلى* و *التسلسل-أسفل*.</span><span class="sxs-lookup"><span data-stu-id="73909-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="73909-109">يمكن تخصيص المخزون بنجاح فقط في حالة عدم وجود فجوات في الأبعاد أعلاه الموقع.</span><span class="sxs-lookup"><span data-stu-id="73909-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="73909-110">على سبيل المثال، في تدرج هرمي حجز *دفعة-أعلى*، تتوقع أبعاد **الموقع** و **المستودع** و **رقم الدفعة** ليتم تحديدها في أمر الطلب.</span><span class="sxs-lookup"><span data-stu-id="73909-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="73909-111">في حاله فقد أي من هذه الأبعاد، ستفشل عملية التوزيع.</span><span class="sxs-lookup"><span data-stu-id="73909-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="73909-112">وعلى النقيض، في تدرج هرمي حجز *الدفعة-أعلى* أو *التسلسل-أسفل*، قد يتم تحديد دفعة أو رقم مسلسل في أمر الطلب، ولكن لا تتطلب عمليه التخصيص ذلك.</span><span class="sxs-lookup"><span data-stu-id="73909-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="73909-113">أتلقى رسالة الخطا التالية: "لتعيينها إلى موجه ، يجب ان تحدد سطور التحميل الابعاد فوق الموقع.</span><span class="sxs-lookup"><span data-stu-id="73909-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="73909-114">لتعيين هذه الابعاد ، قم بحجز بند التحميل وأعاده إنشائه. "</span><span class="sxs-lookup"><span data-stu-id="73909-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="73909-115">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="73909-115">Issue description</span></span>

<span data-ttu-id="73909-116">عند استخدام صنف يحتوي على تدرج هرمي حجز *الدفعة-أعلى*، لا يعمل أمر **إصدار للمستودع** في صفحة **تحميل منضدة التخطيط** إذا حاولت تحرير حمولة لكمية جزئية.</span><span class="sxs-lookup"><span data-stu-id="73909-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="73909-117">تظهر رسالة الخطا هذه ، ولا يتم إنشاء اي عمل للكمية الجزئية.</span><span class="sxs-lookup"><span data-stu-id="73909-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="73909-118">ومع ذلك، عند استخدام صنف يحتوي على تدرج هي حجز *الدفعة-أسفل*، يمكنك تحرير حمولة لكمية جزئية من صفحة **تحميل منضدة التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="73909-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="73909-119">سبب المشكلة</span><span class="sxs-lookup"><span data-stu-id="73909-119">Issue cause</span></span>

<span data-ttu-id="73909-120">إذا البعد أعلى بعد **الموقع** في التدرج الهرمي للحجز، فيجب تحديده قبل إصدار المستودع.</span><span class="sxs-lookup"><span data-stu-id="73909-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="73909-121">لا يمكن إصدار الكميات الجزئية في حاله عدم تحديد واحده أو أكثر من الابعاد الموجودة اعلي **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="73909-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="73909-122">يتم تشغيل مطالبة الحجز التلقائي لرقم الدُفعة على الرغم من وجود مخزون متوفر.</span><span class="sxs-lookup"><span data-stu-id="73909-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="73909-123">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="73909-123">Issue description</span></span>

<span data-ttu-id="73909-124">عند استخدامك صنف يحتوي على تدرج هي حجز *الدفعة-أعلى* في أحد المستودعات التي لم تقم بتمكين عمليات المستودع، وتم تمكين الحجز التلقائي، يتم عرض مطالبة الحجز التلقائي لرقم الدُفعة حتى في حالة توفر دفعة واحدة فقط للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="73909-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="73909-125">ومع ذلك، عند استخدام نفس العنصر في مستودع حيث يتم تمكين عمليات المستودع، لا يتم عرض مطالبة الحجز التلقائي.</span><span class="sxs-lookup"><span data-stu-id="73909-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="73909-126">سبب المشكلة</span><span class="sxs-lookup"><span data-stu-id="73909-126">Issue cause</span></span>

<span data-ttu-id="73909-127">في حالة تحديد تدرج هرمي حجز كـ *دفعة أعلى* أو *تسلسل أسفل*، يجب دائمًا تحديد البُعد المشار إليه (**رقم الدفعة** أو **الرقم المسلسل**) في أوامر الطلبات.</span><span class="sxs-lookup"><span data-stu-id="73909-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="73909-128">قد تتمكن عمليات المستودع من إكمال المعلومات في حالة توفر دفعة واحدة أو رقم تسلسلي.</span><span class="sxs-lookup"><span data-stu-id="73909-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="73909-129">ومع ذلك، نظرًا لعدم تمكين المستودع لعمليات المستودع، يجب على المستخدم دائمًا تحديد جميع الأبعاد أعلى **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="73909-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="73909-130">لا تأخذ قوالب التقسيم التي تحتوي على معيار مراعاة التقسيم المتاح في اعتبارها المخزون الفعلي الحالي للعناصر الممكّنة للدُفعات.</span><span class="sxs-lookup"><span data-stu-id="73909-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="73909-131">لمزيد من المعلومات، راجع [تقسيم المستودع](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="73909-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="73909-132">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="73909-132">Issue description</span></span>

<span data-ttu-id="73909-133">لا تأخذ قوالب التقسيم التي تحتوي على معيار *مراعاة التقسيم المتاح* في اعتبارها المخزون الفعلي الحالي لعناصر *الدفعة-أعلاه*.</span><span class="sxs-lookup"><span data-stu-id="73909-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="73909-134">تأخذها في الاعتبار فقط إذا تم تحديد رقم الدُفعة في بند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="73909-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="73909-135">ومع ذلك، عند استخدام عناصر *الدفعة-أدناه*، تتم مراعاة المخزون الفعلي الحالي كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="73909-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="73909-136">سبب المشكلة</span><span class="sxs-lookup"><span data-stu-id="73909-136">Issue cause</span></span>

<span data-ttu-id="73909-137">يمكن تحديد رأس قالب التقسيم لاستراتيجية الطلب *المطلوب* أو *المحجوز* أو *الصادر*.</span><span class="sxs-lookup"><span data-stu-id="73909-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="73909-138">بالنسبة لاستراتيجية الطلب *المطلوب*، تنطبق نفس متطلبات التسلسل الهرمي للحجز التي تنطبق على الحجز أو التحرير لعمليات المستودع.</span><span class="sxs-lookup"><span data-stu-id="73909-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="73909-139">ولذلك، بالنسبة للأصناف التي تحتوي على تدرجات هرمية حجز *الدفعة-أعلاه* و *التسلسل-أدناه*، يجب تحديد الدُفعة أو الرقم التسلسلي في أمر الطلب (المبيعات أو التحويل).</span><span class="sxs-lookup"><span data-stu-id="73909-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="73909-140">بدلاً من ذلك، يمكن استخدام استراتيجية الطلب *المحجوز* لتحديد الدُفعة أو الرقم التسلسلي قبل إنشاء طلب تقسيم المستودع.</span><span class="sxs-lookup"><span data-stu-id="73909-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
