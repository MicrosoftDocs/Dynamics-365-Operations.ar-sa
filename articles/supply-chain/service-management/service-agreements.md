---
title: اتفاقيات الخدمة
description: تسمح لك اتفاقيات الخدمة بتحديد الموارد المستخدمة في زيارة خدمة عادية وكيفية فوترة هذه الموارد للعميل.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6425dcf1c89f625d997be0dd4a52aaecb6e6d65
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568271"
---
# <a name="service-agreements"></a><span data-ttu-id="14797-103">اتفاقيات الخدمة</span><span class="sxs-lookup"><span data-stu-id="14797-103">Service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14797-104">تسمح لك اتفاقيات الخدمة بتحديد الموارد المستخدمة في زيارة خدمة عادية وكيفية فوترة هذه الموارد للعميل.</span><span class="sxs-lookup"><span data-stu-id="14797-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="14797-105">يتم إرفاق كل اتفاقية خدمة بمشروع يتم من خلاله ترحيل الحركات وفوترتها.</span><span class="sxs-lookup"><span data-stu-id="14797-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="14797-106">ومع ذلك، يُمكنك أيضًا فوترة حركات أمر الخدمة مباشرة من خلال المشروع من دون أن تحتاج أولاً إلى توصيل أمر الخدمة باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="14797-107">قد تقرر القيام بذلك إذا كان أمر الخدمة من أجل زيارة خدمة لمرة واحدة فقط وكانت الحاجة إلى معالجة حركات الخدمة بسرعة تفوق الحاجة إلى الاحتفاظ بمعلومات اتفاقية الخدمة التفصيلية حول العميل عبر فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="14797-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="14797-108">اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="14797-108">Service agreement</span></span>

<span data-ttu-id="14797-109">في كل اتفاقية خدمة، يجب عليك تحديد مشروع ومعرّف اتفاقية خدمة ومجموعة اتفاقية خدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="14797-110">ويُمكنك استخدام مجموعة اتفاقيات الخدمة لفرز اتفاقيات الخدمة وتنظيمها.</span><span class="sxs-lookup"><span data-stu-id="14797-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="14797-111">يشتمل رأس اتفاقية الخدمة على الإعدادات التي تنطبق على كافة بنود الاتفاقية المرفقة:</span><span class="sxs-lookup"><span data-stu-id="14797-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="14797-112">ما إذا كانت اتفاقية الخدمة معلقة أم لا.</span><span class="sxs-lookup"><span data-stu-id="14797-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="14797-113">في حالة تعليق اتفاقية الخدمة، فلا يُمكنك إنشاء أوامر خدمة من اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="14797-114">مدة اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="14797-115">كيفية تجميع بنود اتفاقية الخدمة إلى أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="14797-116">ما إذا كانت اتفاقية الخدمة قالبًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="14797-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="14797-117">في رأس اتفاقية الخدمة، يمكنك أيضًا إعداد جميع كائنات الخدمة ومهام الخدمة التي يمكن استخدامها مع اتفاقية الخدمة عن طريق إدخال مهام الخدمة أو كائنات الخدمة المعينة التي يجب إرفاقها بمختلف البنود.</span><span class="sxs-lookup"><span data-stu-id="14797-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="14797-118">من رأس اتفاقية الخدمة، يمكنك أيضًا نسخ بنود اتفاقية الخدمة أو بنود قالب الخدمة إلى اتفاقية الخدمة الحالية.</span><span class="sxs-lookup"><span data-stu-id="14797-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="14797-119">يمكنك تعليق اتفاقيات الخدمات وإيقاف بنود اتفاقية الخدمة الفردية.</span><span class="sxs-lookup"><span data-stu-id="14797-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="14797-120">إذا حددت خانة الاختيار **معلق‬** على اتفاقية خدمة، فلا يمكنك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="14797-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="14797-121">إنشاء أوامر خدمة تلقائيًا أو يدويًا من اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="14797-122">إذا حددت خانة الاختيار **متوقف** على بند اتفاقية خدمة، فلا يمكنك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="14797-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="14797-123">إنشاء أوامر خدمة تلقائيًا أو يدويًا من بند اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="14797-124">نسخ بند اتفاقية الخدمة إلى اتفاقية خدمة أو أمر خدمة آخر.</span><span class="sxs-lookup"><span data-stu-id="14797-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="14797-125">إذا كانت اتفاقية الخدمة معلقة، فسيتم إيقاف كافة البنود المرفقة، بصرف النظر عن حالتها الفردية.</span><span class="sxs-lookup"><span data-stu-id="14797-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="14797-126">بنود اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="14797-126">Service-agreement lines</span></span>

<span data-ttu-id="14797-127">يصف كل بند من بنود اتفاقية الخدمة بالتفصيل محتوى عمل الخدمة المقترح.</span><span class="sxs-lookup"><span data-stu-id="14797-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="14797-128">وتشتمل البنود على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="14797-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="14797-129">نوع الحركة ووصفها.</span><span class="sxs-lookup"><span data-stu-id="14797-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="14797-130">الموظف الذي يقوم بعمل الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="14797-131">الكائنات التي يجب إجراء الخدمة عليها من أجل اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="14797-132">تكرار إجراء العمل وتكرار تسجيل الصنف المقترن والمصروفات وحركات الرسوم.</span><span class="sxs-lookup"><span data-stu-id="14797-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="14797-133">الإطار الزمني الذي يمكن تجميع بنود أمر الخدمة فيه إلى أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="14797-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="14797-134">مهام الخدمة المستخدمة لتجميع مجموعات بنود الاتفاقية مع بعضها البعض إلى مهام عمل ولتقديم ملخص لفنيي الخدمة والعملاء حول مهمة الخدمة التي سيتم تقديمها.</span><span class="sxs-lookup"><span data-stu-id="14797-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="14797-135">ما إذا تم إيقاف بند أم لا.</span><span class="sxs-lookup"><span data-stu-id="14797-135">Whether a line is stopped.</span></span> <span data-ttu-id="14797-136">في حالة إيقاف بند، سيتعذر عليك إنشاء أوامر خدمة لذلك الصنف.</span><span class="sxs-lookup"><span data-stu-id="14797-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="14797-137">إعدادات المشروع، مثل الفئة وخاصية البند.</span><span class="sxs-lookup"><span data-stu-id="14797-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14797-138">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="14797-138">Related topics</span></span>

[<span data-ttu-id="14797-139">إنشاء اتفاقيات خدمات</span><span class="sxs-lookup"><span data-stu-id="14797-139">Create service agreements</span></span>](create-service-agreements.md)
