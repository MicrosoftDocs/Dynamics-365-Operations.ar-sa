---
title: بدء تحسين التخطيط
description: يشرح هذا الموضوع كيفية بدء استخدام وظيفة تحسين التخطيط.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773891"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="d5d1e-103">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="d5d1e-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="d5d1e-104">لا تدعم وظيفة تحسين التخطيط كافة الميزات المتوفرة في مشغل التخطيط المضمن في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d5d1e-105">لذلك ، فانه من المهم تقييم ما إذا كانت مجموعه الميزات المتوفرة حاليا في تحسين التخطيط ستفي بمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="d5d1e-106">بشكل افتراضي ، وظيفة تحسين التخطيط ليست قيد التشغيل في Dynamics Lifecycle Services (LCS) بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="d5d1e-107">لذلك ، لديك فرصه لاجراء التقييم الخاص بك قبل تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="d5d1e-108">في نهاية المطاف ، سيحل تحسين التخطيط محل محرك التخطيط الحالي لـ Supply Chain Management المضمن.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="d5d1e-109">قبل تشغيل تحسين التخطيط، نوصي بشده بتقييم نتائج تحليل ملائمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="d5d1e-110">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d5d1e-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="d5d1e-111">الترخيص</span><span class="sxs-lookup"><span data-stu-id="d5d1e-111">Licensing</span></span>

<span data-ttu-id="d5d1e-112">إذا كان بإمكانك تشغيل التخطيط الرئيسي باستخدام الترخيص الحالي ، فلن تحتاج إلى شراء ترخيص إضافي للبدء في استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="d5d1e-113">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="d5d1e-113">Install the add-in</span></span>

<span data-ttu-id="d5d1e-114">لاستخدام أمثليه التخطيط، قم بتثبيت الوظيفة الاضافيه لتحسين التخطيط لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d5d1e-115">يمكنك الوصول إلى الوظيفة الاضافيه من مشروع LCS وتشغيل وظيفة تحسين التخطيط من واجهه مستخدم Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="d5d1e-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="d5d1e-116">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="d5d1e-117">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="d5d1e-118">حدد **الاحتفاظ**، أو قم بالتمرير لأسفل إلى علامة التبويب السريع **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="d5d1e-119">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="d5d1e-120">حدد **تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="d5d1e-121">اتبع دليل التثبيت، ووافق علي البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="d5d1e-122">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="d5d1e-123">تكامل تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="d5d1e-123">Planning Optimization integration</span></span>

<span data-ttu-id="d5d1e-124">لتكوين ما إذا كان يجب استخدام الوظيفة الاضافيه لتحسين التخطيط للتخطيط الرئيسي، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **تكامل تحسين التخطيط** \>**تخطيط التكامل**.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="d5d1e-125">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="d5d1e-125">Connection status</span></span>

<span data-ttu-id="d5d1e-126">تشير حاله الاتصال إلى الحالة الحالية للاتصال بين Supply Chain Management وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="d5d1e-127">ويوضح الجدول التالي القيم المحتملة.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="d5d1e-128">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="d5d1e-128">Connection status</span></span> | <span data-ttu-id="d5d1e-129">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="d5d1e-129">Description</span></span> | <span data-ttu-id="d5d1e-130">هل يمكن استخدام تحسين التخطيط؟</span><span class="sxs-lookup"><span data-stu-id="d5d1e-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="d5d1e-131">متصل</span><span class="sxs-lookup"><span data-stu-id="d5d1e-131">Connected</span></span> | <span data-ttu-id="d5d1e-132">تم إنشاء اتصال بين خدمة تحسين التخطيط وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="d5d1e-133">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="d5d1e-133">Yes</span></span> |
| <span data-ttu-id="d5d1e-134">تمكين الاتصال</span><span class="sxs-lookup"><span data-stu-id="d5d1e-134">Enabling connection</span></span> | <span data-ttu-id="d5d1e-135">يتم حاليا تنفيذ طلب لتشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="d5d1e-136">لا</span><span class="sxs-lookup"><span data-stu-id="d5d1e-136">No</span></span> |
| <span data-ttu-id="d5d1e-137">غير متصل</span><span class="sxs-lookup"><span data-stu-id="d5d1e-137">Disconnected</span></span> | <span data-ttu-id="d5d1e-138">لا يوجد اتصال بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="d5d1e-139">يمكن تشغيل الاتصال من LCS، كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="d5d1e-140">لا</span><span class="sxs-lookup"><span data-stu-id="d5d1e-140">No</span></span> |
| <span data-ttu-id="d5d1e-141">تعطيل الاتصال</span><span class="sxs-lookup"><span data-stu-id="d5d1e-141">Disabling connection</span></span> | <span data-ttu-id="d5d1e-142">يتم حاليا تنفيذ طلب لإيقاف تشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="d5d1e-143">لا</span><span class="sxs-lookup"><span data-stu-id="d5d1e-143">No</span></span> |
| <span data-ttu-id="d5d1e-144">حالة البدء</span><span class="sxs-lookup"><span data-stu-id="d5d1e-144">Getting status</span></span> | <span data-ttu-id="d5d1e-145">يقوم النظام بالانتظار للحصول على معلومات الحالة من خدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="d5d1e-146">لا</span><span class="sxs-lookup"><span data-stu-id="d5d1e-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="d5d1e-147">خيار استخدام تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="d5d1e-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="d5d1e-148">يحدد إعداد خيار **استخدام تحسين التخطيط** محرك التخطيط الذي يتم استخدامه للتخطيط الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="d5d1e-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="d5d1e-149">**نعم** – يُستخدم تحسين التخطيط للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="d5d1e-150">**لا** – يُستخدم محرك تخطيط Supply Chain Management المضمن للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="d5d1e-151">إذا تم تشغيل وظائف دفعة التخطيط الموجودة التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن أثناء تعيين خيار **استخدام تحسين التخطيط** إلى **نعم**، فسوف تفشل هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="d5d1e-152">التكامل مع الإعداد</span><span class="sxs-lookup"><span data-stu-id="d5d1e-152">Integration with the setup</span></span>

<span data-ttu-id="d5d1e-153">إذا كانت معاينه تحسين التخطيط قيد التشغيل، يتم اجراء التخطيط الرئيسي باستخدام الوظيفة الاضافيه لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="d5d1e-154">في هذه الحالة، تتاثر نتائج التخطيط الرئيسي وميزاته.</span><span class="sxs-lookup"><span data-stu-id="d5d1e-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d5d1e-155">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="d5d1e-155">Related resources</span></span>

[<span data-ttu-id="d5d1e-156">شروط وأحكام المعاينة</span><span class="sxs-lookup"><span data-stu-id="d5d1e-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="d5d1e-157">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="d5d1e-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="d5d1e-158">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="d5d1e-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="d5d1e-159">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="d5d1e-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="d5d1e-160">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="d5d1e-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="d5d1e-161">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="d5d1e-161">Cancel a planning job</span></span>](cancel-planning-job.md)
