---
title: بدء تحسين التخطيط
description: يشرح هذا الموضوع كيفية بدء استخدام وظيفة تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339868"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="5989b-103">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="5989b-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5989b-104">لا تدعم وظيفة تحسين التخطيط كافة الميزات المتوفرة في مشغل التخطيط المضمن في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5989b-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5989b-105">لذلك ، فانه من المهم تقييم ما إذا كانت مجموعة الميزات المتوفرة حاليا في تحسين التخطيط ستفي بمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="5989b-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="5989b-106">بشكل افتراضي ، وظيفة تحسين التخطيط ليست قيد التشغيل في Dynamics Lifecycle Services (LCS) بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="5989b-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="5989b-107">لذلك ، لديك فرصه لإجراء التقييم الخاص بك قبل تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="5989b-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="5989b-108">في نهاية المطاف ، سيحل تحسين التخطيط محل محرك التخطيط الحالي لـ Supply Chain Management المضمن.</span><span class="sxs-lookup"><span data-stu-id="5989b-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="5989b-109">قبل تشغيل تحسين التخطيط، نوصي بشده بتقييم نتائج تحليل ملائمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="5989b-110">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5989b-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="5989b-111">التوفر</span><span class="sxs-lookup"><span data-stu-id="5989b-111">Availability</span></span>
<span data-ttu-id="5989b-112">يتوفر تحسين التخطيط حاليا في مناطق Azure التالية: الولايات المتحدة وكندا وأوروبا والمملكة المتحدة وأستراليا.</span><span class="sxs-lookup"><span data-stu-id="5989b-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="5989b-113">إذا حاولت تثبيت الوظيفة الاضافيه من منطقه أخرى ، فسوف يُظهر لك LCS رسالة بأن هذه المنطقة الجغرافية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="5989b-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="5989b-114">لاحظ أن تحسين التخطيط لا يدعم عمليات النشر المحلية لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5989b-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="5989b-115">الترخيص</span><span class="sxs-lookup"><span data-stu-id="5989b-115">Licensing</span></span>

<span data-ttu-id="5989b-116">إذا كان بإمكانك تشغيل التخطيط الرئيسي باستخدام الترخيص الحالي ، فلن تحتاج إلى شراء ترخيص إضافي للبدء في استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="5989b-117">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="5989b-117">Install the add-in</span></span>

<span data-ttu-id="5989b-118">لاستخدام أمثليه التخطيط، قم بتثبيت الوظيفة الإضافية لتحسين التخطيط لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5989b-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5989b-119">يمكنك الوصول إلى الوظيفة الإضافية من مشروع LCS وتشغيل وظيفة تحسين التخطيط من واجهه مستخدم Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="5989b-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="5989b-120">يُعد متطلب تحسين التخطيط بيئة ذات توفر عالي الطبقة 2 أو أعلى بتمكين LCS (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="5989b-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="5989b-121">إذا حاولت تثبيت الوظيفة الاضافيه في بيئة OneBox، لن يكتمل التثبيت وستحتاج إلى إلغاء التثبيت.</span><span class="sxs-lookup"><span data-stu-id="5989b-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="5989b-122">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5989b-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="5989b-123">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="5989b-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="5989b-124">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="5989b-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="5989b-125">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="5989b-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="5989b-126">حدد **تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="5989b-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="5989b-127">اتبع دليل التثبيت، ووافق علي البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="5989b-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="5989b-128">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="5989b-128">Select **Install**.</span></span>
1. <span data-ttu-id="5989b-129">في علامة التبويب السريعة **الوظائف الإضافية للبيئة‬**، ينبغي رؤية "جارِ تثبيت تحسين التخطيط".</span><span class="sxs-lookup"><span data-stu-id="5989b-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="5989b-130">بعد بضع دقائق ينبغي تغيير **جارٍ التثبيت** إلى **تم التثبيت** (قد تحتاج إلى تحديث الصفحة).</span><span class="sxs-lookup"><span data-stu-id="5989b-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="5989b-131">عندما يتم التثبيت، ستكون جاهزًا لتنشيط تحسين التخطيط في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5989b-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="5989b-132">تكامل تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="5989b-132">Planning Optimization integration</span></span>

<span data-ttu-id="5989b-133">لتكوين ما إذا كان يجب استخدام الوظيفة الإضافية لتحسين التخطيط للتخطيط الرئيسي، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **معلمات تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="5989b-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="5989b-134">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="5989b-134">Connection status</span></span>

<span data-ttu-id="5989b-135">تشير حالة الاتصال إلى الحالة الحالية للاتصال بين Supply Chain Management وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="5989b-136">ويوضح الجدول التالي القيم المحتملة.</span><span class="sxs-lookup"><span data-stu-id="5989b-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="5989b-137">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="5989b-137">Connection status</span></span> | <span data-ttu-id="5989b-138">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5989b-138">Description</span></span> | <span data-ttu-id="5989b-139">هل يمكن استخدام تحسين التخطيط؟</span><span class="sxs-lookup"><span data-stu-id="5989b-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="5989b-140">متصل</span><span class="sxs-lookup"><span data-stu-id="5989b-140">Connected</span></span> | <span data-ttu-id="5989b-141">تم إنشاء اتصال بين خدمة تحسين التخطيط وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5989b-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="5989b-142">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="5989b-142">Yes</span></span> |
| <span data-ttu-id="5989b-143">تمكين الاتصال</span><span class="sxs-lookup"><span data-stu-id="5989b-143">Enabling connection</span></span> | <span data-ttu-id="5989b-144">يتم حاليا تنفيذ طلب لتشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5989b-145">لا</span><span class="sxs-lookup"><span data-stu-id="5989b-145">No</span></span> |
| <span data-ttu-id="5989b-146">غير متصل</span><span class="sxs-lookup"><span data-stu-id="5989b-146">Disconnected</span></span> | <span data-ttu-id="5989b-147">لا يوجد اتصال بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="5989b-148">يمكن تشغيل الاتصال من LCS، كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="5989b-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="5989b-149">لا</span><span class="sxs-lookup"><span data-stu-id="5989b-149">No</span></span> |
| <span data-ttu-id="5989b-150">تعطيل الاتصال</span><span class="sxs-lookup"><span data-stu-id="5989b-150">Disabling connection</span></span> | <span data-ttu-id="5989b-151">يتم حاليا تنفيذ طلب لإيقاف تشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5989b-152">لا</span><span class="sxs-lookup"><span data-stu-id="5989b-152">No</span></span> |
| <span data-ttu-id="5989b-153">حالة البدء</span><span class="sxs-lookup"><span data-stu-id="5989b-153">Getting status</span></span> | <span data-ttu-id="5989b-154">يقوم النظام بالانتظار للحصول على معلومات الحالة من خدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="5989b-155">لا</span><span class="sxs-lookup"><span data-stu-id="5989b-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="5989b-156">خيار استخدام تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="5989b-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="5989b-157">يحدد إعداد خيار **استخدام تحسين التخطيط** محرك التخطيط الذي يتم استخدامه للتخطيط الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="5989b-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="5989b-158">**نعم** – يُستخدم تحسين التخطيط للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="5989b-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="5989b-159">**لا** – يُستخدم محرك تخطيط Supply Chain Management المضمن للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="5989b-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="5989b-160">إذا تم تشغيل وظائف دفعة التخطيط الموجودة التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن أثناء تعيين خيار **استخدام تحسين التخطيط** إلى **نعم**، فسوف تفشل هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="5989b-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="5989b-161">التكامل مع الإعداد</span><span class="sxs-lookup"><span data-stu-id="5989b-161">Integration with the setup</span></span>

<span data-ttu-id="5989b-162">إذا كانت معاينه تحسين التخطيط قيد التشغيل، يتم إجراء التخطيط الرئيسي باستخدام الوظيفة الإضافية لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5989b-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="5989b-163">في هذه الحالة، تتاثر نتائج التخطيط الرئيسي وميزاته.</span><span class="sxs-lookup"><span data-stu-id="5989b-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5989b-164">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5989b-164">Additional resources</span></span>

[<span data-ttu-id="5989b-165">شروط وأحكام المعاينة</span><span class="sxs-lookup"><span data-stu-id="5989b-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="5989b-166">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="5989b-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5989b-167">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="5989b-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5989b-168">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="5989b-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5989b-169">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="5989b-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="5989b-170">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="5989b-170">Cancel a planning job</span></span>](cancel-planning-job.md)
