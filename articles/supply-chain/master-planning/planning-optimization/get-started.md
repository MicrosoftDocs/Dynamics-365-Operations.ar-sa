---
title: بدء تحسين التخطيط
description: يشرح هذا الموضوع كيفية بدء استخدام وظيفة تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
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
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213505"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="1d957-103">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1d957-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d957-104">لا تدعم وظيفة تحسين التخطيط كافة الميزات المتوفرة في مشغل التخطيط المضمن في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d957-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1d957-105">لذلك ، فانه من المهم تقييم ما إذا كانت مجموعة الميزات المتوفرة حاليا في تحسين التخطيط ستفي بمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="1d957-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="1d957-106">بشكل افتراضي ، وظيفة تحسين التخطيط ليست قيد التشغيل في Dynamics Lifecycle Services (LCS) بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="1d957-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="1d957-107">لذلك ، لديك فرصه لإجراء التقييم الخاص بك قبل تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="1d957-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="1d957-108">في نهاية المطاف ، سيحل تحسين التخطيط محل محرك التخطيط الحالي لـ Supply Chain Management المضمن.</span><span class="sxs-lookup"><span data-stu-id="1d957-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="1d957-109">قبل تشغيل تحسين التخطيط، نوصي بشده بتقييم نتائج تحليل ملائمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="1d957-110">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1d957-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="1d957-111">الترخيص</span><span class="sxs-lookup"><span data-stu-id="1d957-111">Licensing</span></span>

<span data-ttu-id="1d957-112">إذا كان بإمكانك تشغيل التخطيط الرئيسي باستخدام الترخيص الحالي ، فلن تحتاج إلى شراء ترخيص إضافي للبدء في استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="1d957-113">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="1d957-113">Install the add-in</span></span>

<span data-ttu-id="1d957-114">لاستخدام أمثليه التخطيط، قم بتثبيت الوظيفة الإضافية لتحسين التخطيط لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d957-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1d957-115">يمكنك الوصول إلى الوظيفة الإضافية من مشروع LCS وتشغيل وظيفة تحسين التخطيط من واجهه مستخدم Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="1d957-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="1d957-116">يُعد متطلب تحسين التخطيط بيئة ذات توفر عالي بتمكين LCS (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="1d957-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="1d957-117">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="1d957-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="1d957-118">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="1d957-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="1d957-119">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="1d957-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="1d957-120">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="1d957-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="1d957-121">حدد **تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="1d957-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="1d957-122">اتبع دليل التثبيت، ووافق علي البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="1d957-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="1d957-123">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="1d957-123">Select **Install**.</span></span>
1. <span data-ttu-id="1d957-124">في علامة التبويب السريعة **الوظائف الإضافية للبيئة‬**، ينبغي رؤية "جارِ تثبيت تحسين التخطيط".</span><span class="sxs-lookup"><span data-stu-id="1d957-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="1d957-125">بعد بضع دقائق ينبغي تغيير **جارٍ التثبيت** إلى **تم التثبيت** (قد تحتاج إلى تحديث الصفحة).</span><span class="sxs-lookup"><span data-stu-id="1d957-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="1d957-126">عندما يتم التثبيت، ستكون جاهزًا لتنشيط تحسين التخطيط في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d957-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="1d957-127">تكامل تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="1d957-127">Planning Optimization integration</span></span>

<span data-ttu-id="1d957-128">لتكوين ما إذا كان يجب استخدام الوظيفة الإضافية لتحسين التخطيط للتخطيط الرئيسي، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **معلمات تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="1d957-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="1d957-129">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="1d957-129">Connection status</span></span>

<span data-ttu-id="1d957-130">تشير حالة الاتصال إلى الحالة الحالية للاتصال بين Supply Chain Management وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="1d957-131">ويوضح الجدول التالي القيم المحتملة.</span><span class="sxs-lookup"><span data-stu-id="1d957-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="1d957-132">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="1d957-132">Connection status</span></span> | <span data-ttu-id="1d957-133">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="1d957-133">Description</span></span> | <span data-ttu-id="1d957-134">هل يمكن استخدام تحسين التخطيط؟</span><span class="sxs-lookup"><span data-stu-id="1d957-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="1d957-135">متصل</span><span class="sxs-lookup"><span data-stu-id="1d957-135">Connected</span></span> | <span data-ttu-id="1d957-136">تم إنشاء اتصال بين خدمة تحسين التخطيط وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d957-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="1d957-137">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="1d957-137">Yes</span></span> |
| <span data-ttu-id="1d957-138">تمكين الاتصال</span><span class="sxs-lookup"><span data-stu-id="1d957-138">Enabling connection</span></span> | <span data-ttu-id="1d957-139">يتم حاليا تنفيذ طلب لتشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1d957-140">لا</span><span class="sxs-lookup"><span data-stu-id="1d957-140">No</span></span> |
| <span data-ttu-id="1d957-141">غير متصل</span><span class="sxs-lookup"><span data-stu-id="1d957-141">Disconnected</span></span> | <span data-ttu-id="1d957-142">لا يوجد اتصال بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="1d957-143">يمكن تشغيل الاتصال من LCS، كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="1d957-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="1d957-144">لا</span><span class="sxs-lookup"><span data-stu-id="1d957-144">No</span></span> |
| <span data-ttu-id="1d957-145">تعطيل الاتصال</span><span class="sxs-lookup"><span data-stu-id="1d957-145">Disabling connection</span></span> | <span data-ttu-id="1d957-146">يتم حاليا تنفيذ طلب لإيقاف تشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1d957-147">لا</span><span class="sxs-lookup"><span data-stu-id="1d957-147">No</span></span> |
| <span data-ttu-id="1d957-148">حالة البدء</span><span class="sxs-lookup"><span data-stu-id="1d957-148">Getting status</span></span> | <span data-ttu-id="1d957-149">يقوم النظام بالانتظار للحصول على معلومات الحالة من خدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="1d957-150">لا</span><span class="sxs-lookup"><span data-stu-id="1d957-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="1d957-151">خيار استخدام تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1d957-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="1d957-152">يحدد إعداد خيار **استخدام تحسين التخطيط** محرك التخطيط الذي يتم استخدامه للتخطيط الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="1d957-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="1d957-153">**نعم** – يُستخدم تحسين التخطيط للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1d957-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="1d957-154">**لا** – يُستخدم محرك تخطيط Supply Chain Management المضمن للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1d957-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="1d957-155">إذا تم تشغيل وظائف دفعة التخطيط الموجودة التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن أثناء تعيين خيار **استخدام تحسين التخطيط** إلى **نعم**، فسوف تفشل هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="1d957-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="1d957-156">التكامل مع الإعداد</span><span class="sxs-lookup"><span data-stu-id="1d957-156">Integration with the setup</span></span>

<span data-ttu-id="1d957-157">إذا كانت معاينه تحسين التخطيط قيد التشغيل، يتم إجراء التخطيط الرئيسي باستخدام الوظيفة الإضافية لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1d957-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="1d957-158">في هذه الحالة، تتاثر نتائج التخطيط الرئيسي وميزاته.</span><span class="sxs-lookup"><span data-stu-id="1d957-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1d957-159">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="1d957-159">Related resources</span></span>

[<span data-ttu-id="1d957-160">شروط وأحكام المعاينة</span><span class="sxs-lookup"><span data-stu-id="1d957-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="1d957-161">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="1d957-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1d957-162">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1d957-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1d957-163">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="1d957-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1d957-164">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="1d957-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1d957-165">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="1d957-165">Cancel a planning job</span></span>](cancel-planning-job.md)
