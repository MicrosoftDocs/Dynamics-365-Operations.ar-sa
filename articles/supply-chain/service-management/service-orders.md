---
title: أوامر الخدمة
description: يمثل أمر الخدمة الزيارة التي قام بها فني الخدمة إلى موقع العميل في تاريخ معين.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b049b166edf2b5a318a4b1af85e7f74cfe433f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421053"
---
# <a name="service-orders"></a><span data-ttu-id="515b9-103">أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="515b9-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="515b9-104">يمثل أمر الخدمة الزيارة التي قام بها فني الخدمة إلى موقع العميل في تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="515b9-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="515b9-105">يتكون كل أمر من أوامر الخدمة من بند واحد أو أكثر من بنود الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="515b9-106">وتمثل بنود أمر الخدمة ساعات العمل التي يجب أن ينفذها فني الخدمة، والأصناف والمصاريف والرسوم.</span><span class="sxs-lookup"><span data-stu-id="515b9-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="515b9-107">يمكنك إرفاق المهام والكائنات ببند أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="515b9-108">بعد ذلك يمكنك تجميع بنود أوامر الخدمة حسب المهام أو كائن.</span><span class="sxs-lookup"><span data-stu-id="515b9-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="515b9-109">كما يمكن أيضًا إرفاق الأصناف التي تم إدراجها في المخزون ببنود أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="515b9-110">إنشاء أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="515b9-110">Create service orders</span></span>

<span data-ttu-id="515b9-111">ويمكنك إنشاء أوامر الخدمات استنادًا إلى اتفاقية الخدمة والبنود الواردة في تلك الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="515b9-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="515b9-112">ومع ذلك، يمكنك إنشاء أوامر الخدمة المرتبطة باتفاقية خدمة فقط في الفترة المحددة في الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="515b9-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="515b9-113">على سبيل المثال، إذا كانت اتفاقية خدمة ما صالحة لسنة التقويم 2011، يمكنك إنشاء أوامر الخدمة للاتفاقية من 1 يناير 2011، و31 ديسمبر عام 2011.</span><span class="sxs-lookup"><span data-stu-id="515b9-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="515b9-114">ويمكنك أيضًا إنشاء أوامر الخدمة فرديا، دون إقرانها باتفاقية.</span><span class="sxs-lookup"><span data-stu-id="515b9-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="515b9-115">يمكن استخدام أوامر الخدمة هذه لمعالجة زيارات الخدمة الطارئة أو لمرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="515b9-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="515b9-116">على سبيل المثال، في شهر مارس يريد العميل تلقي خدمة على آلتين، بالإضافة للآلات المخصصة في اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="515b9-117">في هذه المهمة، يمكنك إنشاء أوامر الخدمة ولكن دون إقرانها باتفاقية.</span><span class="sxs-lookup"><span data-stu-id="515b9-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="515b9-118">لإنشاء أوامر الخدمة التي لا ترتبط باتفاقية خدمة، يجب عليك تحديد خانة الاختيار <STRONG>السماح بدون اتفاقية خدمات</STRONG> في النموذج <STRONG>محددات إدارة الخدمة</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="515b9-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="515b9-119">**سيناريو**</span><span class="sxs-lookup"><span data-stu-id="515b9-119">**Scenario**</span></span>

<span data-ttu-id="515b9-120">يوضح السيناريو التالي موقفًا آخر حيث يكون من المفيد إنشاء أمر خدمة غير مرتبط باتفاقية خدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="515b9-121">يستلم مرسِل الشركة مكالمة لطلب خدمة طوارئ لأحد المصاعد.</span><span class="sxs-lookup"><span data-stu-id="515b9-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="515b9-122">لا يوجد وقت لإعداد اتفاقية خدمة ومشروع للخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="515b9-123">لذلك، أنشأ المرسل أمر خدمة مباشرة في النموذج **أوامر الخدمة**، وأرفق أمر الخدمة بمشروع موجود، ثم أنشأ بنود أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="515b9-124">أنشأ المرسل أيضًا مهمة أو علاقة كائن لأمر خدمة موجود بالفعل، لتسجيل عمل غير مرتبط باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="515b9-125">للحصول على مزيد من المعلومات، راجع [إنشاء أوامر خدمة يدوياً](create-service-orders-manually.md) و [إنشاء علاقات مهام الخدمة](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="515b9-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="515b9-126">مراقبة تقدم أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="515b9-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="515b9-127">لمراقبة تقدم أمر مبيعات عبر الفرق المختلفة وعمليات العمل، يمكنك إعداد نظام مراحل وأكواد سبب لأوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="515b9-128">ولكل مرحلة، يمكنك تحديد الإجراءات المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="515b9-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="515b9-129">لمزيد من المعلومات، راجع [إنشاء أكواد السبب](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="515b9-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="515b9-130">**مثال**</span><span class="sxs-lookup"><span data-stu-id="515b9-130">**Example**</span></span>

<span data-ttu-id="515b9-131">يتم اعتماد أمر خدمة بواسطة المرسل.</span><span class="sxs-lookup"><span data-stu-id="515b9-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="515b9-132">يقوم المرسل بتحديث مرحلة أمر الخدمة ويحدد كود سبب والذي يشير إلى أنه قد تم إصدار أمر الخدمة لفني الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="515b9-133">ويتوجه الفني إلى موقع العميل ويؤدي الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="515b9-134">تحديد متطلبات الصنف لأوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="515b9-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="515b9-135">يمكنك تحديد أصناف المخزون المطلوبة لأوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="515b9-136">ومع ذلك، يجب أن يكون أمر الخدمة مرتبطًا بمشروع.</span><span class="sxs-lookup"><span data-stu-id="515b9-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="515b9-137">تتم معالجة متطلبات الصنف لأوامر الخدمة من خلال مشروع.</span><span class="sxs-lookup"><span data-stu-id="515b9-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="515b9-138">**مثال**</span><span class="sxs-lookup"><span data-stu-id="515b9-138">**Example**</span></span>

<span data-ttu-id="515b9-139">ويقوم المرسِل بمعالجة أوامر الخدمة التي تم إنشاؤها من اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="515b9-140">ويدرك المرسِل من أول أمر خدمة أن الفني يطلب قطعة غيار مهمة وغير متاحة في المخزون.</span><span class="sxs-lookup"><span data-stu-id="515b9-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="515b9-141">لذلك، يقوم المرسل بإنشاء متطلب صنف لقطعة الغيار مباشرة من أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="515b9-142">بنود النقل والترحيل</span><span class="sxs-lookup"><span data-stu-id="515b9-142">Move and post lines</span></span>

<span data-ttu-id="515b9-143">عند عودة الفني من زيارة الخدمة، وبعد ذلك يقوم بتعديل بنود أوامر الخدمة ويحدّثها.</span><span class="sxs-lookup"><span data-stu-id="515b9-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="515b9-144">أثناء قيامه بالزيارة، نفذ الفني مهمة الخدمة التي كان من المجدول تنفيذها في زيارة الخدمة التالية.</span><span class="sxs-lookup"><span data-stu-id="515b9-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="515b9-145">بالتالي، ينقل الفني البنود من زيارة الخدمة التالية إلى زيارة الخدمة الحالية.</span><span class="sxs-lookup"><span data-stu-id="515b9-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="515b9-146">بعد ذلك يرحِّل الفني أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-146">The technician then posts the service order.</span></span> <span data-ttu-id="515b9-147">لمزيد من المعلومات، راجع [ترحيل بنود أمر الخدمة](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="515b9-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="515b9-148">إلغاء أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="515b9-148">Cancel service orders</span></span>

<span data-ttu-id="515b9-149">أصبح أحد أوامر الخدمة الذي تم إنشاؤه لشهر يناير مهملاً بسبب إلغاء المهمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="515b9-150">لذلك، يقوم مرسِل الخدمة بإلغاء أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="515b9-151">لمزيد من المعلومات، راجع [إلغاء أوامر الخدمة](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="515b9-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="515b9-152">الترحيل من المشروعات</span><span class="sxs-lookup"><span data-stu-id="515b9-152">Post from projects</span></span>

<span data-ttu-id="515b9-153">يريد المرسل في نهاية كل أسبوع ترحيل كل أوامر الخدمة التي تم إرفاقها بمشروع معين.</span><span class="sxs-lookup"><span data-stu-id="515b9-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="515b9-154">لذلك، يقوم المرسل بتحديد موقع المشروع ذي الصلة في نموذج **المشاريع** ويرحِّل أوامر الخدمة التي تم إكمالها.</span><span class="sxs-lookup"><span data-stu-id="515b9-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="515b9-155">لمزيد من المعلومات، راجع [ترحيل أوامر الخدمة (نموذج الفئة)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="515b9-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="515b9-156">حذف أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="515b9-156">Delete service orders</span></span>

<span data-ttu-id="515b9-157">وأثناء النصف الثاني من السنة، يقرر العميل أن زيارات الخدمة أقل من اللازم.</span><span class="sxs-lookup"><span data-stu-id="515b9-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="515b9-158">ويجب إنشاء سلسلة زيارات جديدة ومتكررة الحدوث بشكل أكبر خلال الفترة المتبقية في اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="515b9-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="515b9-159">لذلك يجب حذف أوامر الخدمة الموجودة وإنشاء أوامر خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="515b9-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="515b9-160">لمزيد من المعلومات، راجع [حذف أوامر الخدمة](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="515b9-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="515b9-161">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="515b9-161">See also</span></span>

<span data-ttu-id="515b9-162">[أوامر الخدمة (نموذج)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="515b9-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


