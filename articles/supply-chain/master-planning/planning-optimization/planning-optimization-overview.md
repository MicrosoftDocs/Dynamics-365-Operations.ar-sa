---
title: نظرة عامة على تحسين التخطيط‬
description: يقدم هذا الموضوع نظرة عامة على وظيفة تحسين التخطيط.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ccf00b6fcd1e3a6002086360b1a4c5c464ba054
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076145"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="1d6c5-103">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="1d6c5-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1d6c5-104">تتيح الوظيفة الاضافيه لتحسين أداء التخطيط لـ Microsoft Dynamics 365 Supply Chain Management إمكانية حساب التخطيط الرئيسي لكي يحدث خارج Dynamics 365 Supply Chain Management وقاعدة بيانات SQL ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="1d6c5-105">تتضمن الفوائد المرتبطة بوظيفة "تحسين التخطيط" أداءً محسناً وأقل تأثير على قاعدة بيانات SQL أثناء تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="1d6c5-106">يمكن اجراء عمليات تشغيل التخطيط السريع حتى اثناء ساعات العمل ، بحيث يمكن للمخططات التعامل فورا مع الطلبات أو تغييرات المعلمات.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="1d6c5-107">لاستخدام أمثليه التخطيط ، يجب تثبيت الوظيفة الاضافيه لتحسين التخطيط من مشروعك في Microsoft Dynamics Lifecycle Services (LCS) وتشغيل وظيفة تحسين التخطيط في إدارة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="1d6c5-108">لمزيد من المعلومات، راجع [الشروع في العمل مع تحسين التخطيط](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="1d6c5-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="1d6c5-109">يبين الرسم التوضيحي التالي ميزه تحسين أداء التخطيط اثناء ساعات العمل.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![فائده من تشغيل تحسين التخطيط اثناء ساعات العمل.](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="1d6c5-111">تحسين الأداء</span><span class="sxs-lookup"><span data-stu-id="1d6c5-111">Improved performance</span></span>

<span data-ttu-id="1d6c5-112">يمكن استخدام أمثليه التخطيط في السيناريوهات التي تتضمن خطط رئيسيه طويلة الأمد.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="1d6c5-113">وقد تم تصميمه خصيصا للحسابات السريعة الكبيرة التي تتضمن كميات كبيره من البيانات.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="1d6c5-114">نظرًا لأنها مبنية على أنها خدمة متعددة العناصر قابلة للتوسعة بشكل كبير ، يمكن أن تعمل مثيلات متعددة معًا في وقت واحد لحساب الخطة.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="1d6c5-115">بالإضافة إلى ذلك ، تقوم خدمة التخطيط بإزالة حمل التخطيط الرئيسي من نظامك وتعمل مع دفق بيانات يقلل من حمل الخادم.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="1d6c5-116">يمكن ان يساعدك تحسين التخطيط في تحقيق الأهداف التالية:</span><span class="sxs-lookup"><span data-stu-id="1d6c5-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="1d6c5-117">تحسين أداء التخطيط من خلال وقت تشغيل أقصر.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="1d6c5-118">تقليل التاثير علي العمليات الأخرى اثناء تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="1d6c5-119">القيام بالمزيد من عمليات التخطيط المتكررة.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-119">Do more frequent planning runs.</span></span> <span data-ttu-id="1d6c5-120">(لا تقتصر على عمليات التشغيل اليومية.)</span><span class="sxs-lookup"><span data-stu-id="1d6c5-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="1d6c5-121">الثقة في أن نمو الأعمال في المستقبل لن يثقل كاهل نظام التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="1d6c5-122">البنية وتدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="1d6c5-122">Architecture and data flow</span></span>

<span data-ttu-id="1d6c5-123">عند تثبيت الوظيفة الاضافيه لتحسين أداء التخطيط من LCS ، يتم تاسيس اتصال أمن بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="1d6c5-124">وتوجد الخدمة في نفس بلد أو منطقه مركز البيانات مثل مثيل أداره سلسله التوريد المرتبط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="1d6c5-125">بعد اعداد تحسين أداء التخطيط ، وعند تشغيل التخطيط الرئيسي ، يتم إرسال البيانات الرئيسية وبيانات الحركات من أداره سلسله التوريد إلى خدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="1d6c5-126">إذا تم إلغاء تثبيت الوظيفة الاضافيه لتحسين أداء التخطيط ، تتم أزاله كافة البيانات المرتبطة في خدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="1d6c5-127">تدفق البيانات عالي المستوي لأعاده إنشاء</span><span class="sxs-lookup"><span data-stu-id="1d6c5-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="1d6c5-128">يرسل عميل Supply Chain Management اشاره لطلب تشغيل تخطيط من تحسين أداء التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="1d6c5-129">يقوم تحسين التخطيط بطلب البيانات المطلوبة عن طريق الموصل المتكامل.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="1d6c5-130">وترسل قاعده بيانات SQL المعلومات المطلوبة حول الاعداد والشكل الرئيسي وبيانات الحركات لتخطيط التحسين بواسطة الموصل.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="1d6c5-131">يترجم الموصل المعلومات بين أداره سلسله التوريد وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="1d6c5-132">تحتفظ خدمه تحسين التخطيط بالبيانات المتعلقة بالتخطيط في الذاكرة وتقوم بالعمليات الحسابية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="1d6c5-133">يتم إرسال نتيجة التخطيط إلى قاعده بيانات أداره سلسله التوريد عبر الرابط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="1d6c5-134">وتتضمن النتائج معلومات مثل الأوامر المخططة ومعلومات تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="1d6c5-135">يقوم تحسين التخطيط بإرسال اشاره لتوفير أداره السلسلة للاشاره إلى اكتمال تشغيل التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="1d6c5-136">ويرسل أيضا إيه رسائل وتحذيرات ذات صله.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="1d6c5-137">يبين الرسم التوضيحي التالي تدفق البيانات.</span><span class="sxs-lookup"><span data-stu-id="1d6c5-137">The following illustration shows the data flow.</span></span>

![تدفق البيانات لعمليات تشغيل إعادة الإنشاء](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="1d6c5-139">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="1d6c5-139">Related resources</span></span>

[<span data-ttu-id="1d6c5-140">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1d6c5-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1d6c5-141">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1d6c5-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1d6c5-142">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="1d6c5-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1d6c5-143">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="1d6c5-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1d6c5-144">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="1d6c5-144">Cancel a planning job</span></span>](cancel-planning-job.md)
