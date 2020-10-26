---
title: بدء تحسين التخطيط
description: يشرح هذا الموضوع كيفية بدء استخدام وظيفة تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973466"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="14b61-103">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="14b61-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14b61-104">وكما  [سبق ان تم الإعلان عنه](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios)، تتم جدوله تحسين التخطيط لاستبدال محرك التخطيط الرئيسي الموجود المضمن.</span><span class="sxs-lookup"><span data-stu-id="14b61-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="14b61-105">إذا كنت تستخدم حاليا مشغل التخطيط الرئيسي المضمن، فعليك البدء في تخطيط الترحيل لتخطيط تحسين الأداء الآن.</span><span class="sxs-lookup"><span data-stu-id="14b61-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="14b61-106">من المهم بدء عمليه الترحيل فورا لان العمليات قد تكون متاثره عند فرض الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="14b61-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="14b61-107">لتجنب مشكلات الدقائق الاخيره عند فرض الإهلاك، فاننا نشجعك بشده علي إكمال الترحيل قبل 1 ديسمبر 2020.</span><span class="sxs-lookup"><span data-stu-id="14b61-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="14b61-108">لا تدعم وظيفة تحسين التخطيط كافة الميزات المتوفرة في محرك التخطيط المضمن في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="14b61-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="14b61-109">لذلك ، فانه من المهم تقييم ما إذا كانت مجموعة الميزات المتوفرة حاليا في تحسين التخطيط ستفي بمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="14b61-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="14b61-110">لا يتم تشغيل وظيفة تحسين التخطيط في الوقت الحالي بشكل افتراضي في Dynamics Lifecycle Services (LCS)، بحيث يكون لديك الفرصة لاجراء التقييم الخاص بك قبل تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="14b61-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="14b61-111">أنت بحاجه لطلب استثناء من الترحيل إلى تحسين أداء التخطيط في حاله عدم تضمين عمليه التخطيط الرئيسية للإنتاج (التخطيط الرئيسي الذي تم إنشاؤه من خلال أوامر الإنتاج المخططة) وأنت تطلب من محرك التخطيط الرئيسي المضمن في الإصدر 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="14b61-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="14b61-112">ويتم البدء في الإصدار 10.0.16، ويتم عرض الخطا في البيئات عند تشغيل تخطيط رئيسي مضمن دون إنشاء أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="14b61-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="14b61-113">يجب استخدام تحسين التخطيط لكافة عمليات التوزيع الجديدة التي لا تقوم بإنشاء أوامر إنتاج مخططه اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="14b61-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="14b61-114">وسوف يتلقى مالكو البيئات الموجودة التي يقومون بتشغيل محرك التخطيط الرئيسي المضمن بدون إنشاء أوامر الإنتاج المخططة، رسالة تحتوي علي تفاصيل حول عمليه الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="14b61-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="14b61-115">نوصي بالعمل مع شريك لتقييم الترحيل وتخطيطه لتحسين أداء التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="14b61-116">قبل تشغيل تحسين التخطيط، نوصي بشده بتقييم نتائج تحليل ملائمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="14b61-117">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="14b61-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="14b61-118">التوفر</span><span class="sxs-lookup"><span data-stu-id="14b61-118">Availability</span></span>
<span data-ttu-id="14b61-119">يتوفر تحسين التخطيط حاليا في مناطق Azure التالية: الولايات المتحدة وكندا وأوروبا والمملكة المتحدة وأستراليا.</span><span class="sxs-lookup"><span data-stu-id="14b61-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="14b61-120">إذا حاولت تثبيت الوظيفة الإضافية  من منطقه أخرى ، فسوف يُظهر لك LCS رسالة بأن هذه المنطقة الجغرافية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="14b61-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="14b61-121">لاحظ أن تحسين التخطيط لا يدعم عمليات النشر المحلية لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="14b61-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="14b61-122">الترخيص</span><span class="sxs-lookup"><span data-stu-id="14b61-122">Licensing</span></span>

<span data-ttu-id="14b61-123">إذا كان بإمكانك تشغيل التخطيط الرئيسي باستخدام الترخيص الحالي ، فلن تحتاج إلى شراء ترخيص إضافي للبدء في استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="14b61-124">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="14b61-124">Install the add-in</span></span>

<span data-ttu-id="14b61-125">لاستخدام أمثليه التخطيط، قم بتثبيت الوظيفة الإضافية لتحسين التخطيط لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="14b61-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="14b61-126">يمكنك الوصول إلى الوظيفة الإضافية من مشروع LCS وتشغيل وظيفة تحسين التخطيط من واجهه مستخدم Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="14b61-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="14b61-127">يُعد متطلب تحسين التخطيط بيئة ذات توفر عالي الطبقة 2 أو أعلى بتمكين LCS (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="14b61-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="14b61-128">إذا حاولت تثبيت الوظيفة الإضافية  في بيئة OneBox، لن يكتمل التثبيت وستحتاج إلى إلغاء التثبيت.</span><span class="sxs-lookup"><span data-stu-id="14b61-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="14b61-129">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="14b61-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="14b61-130">انتقل إلى **التفاصيل الكاملة** .</span><span class="sxs-lookup"><span data-stu-id="14b61-130">Go to **Full details** .</span></span>
1. <span data-ttu-id="14b61-131">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة** .</span><span class="sxs-lookup"><span data-stu-id="14b61-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="14b61-132">حدد **تثبيت وظيفة إضاية جديدة** .</span><span class="sxs-lookup"><span data-stu-id="14b61-132">Select **Install a new add-in** .</span></span>
1. <span data-ttu-id="14b61-133">حدد **تحسين التخطيط** .</span><span class="sxs-lookup"><span data-stu-id="14b61-133">Select **Planning Optimization** .</span></span>
1. <span data-ttu-id="14b61-134">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="14b61-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="14b61-135">حدد **تثبيت** .</span><span class="sxs-lookup"><span data-stu-id="14b61-135">Select **Install** .</span></span>
1. <span data-ttu-id="14b61-136">في علامة التبويب السريعة **الوظائف الإضافية للبيئة‬** ، ينبغي رؤية "جارِ تثبيت تحسين التخطيط".</span><span class="sxs-lookup"><span data-stu-id="14b61-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="14b61-137">بعد بضع دقائق ينبغي تغيير **جارٍ التثبيت** إلى **تم التثبيت** (قد تحتاج إلى تحديث الصفحة).</span><span class="sxs-lookup"><span data-stu-id="14b61-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="14b61-138">عندما يتم التثبيت، ستكون جاهزًا لتنشيط تحسين التخطيط في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="14b61-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="14b61-139">تكامل تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="14b61-139">Planning Optimization integration</span></span>

<span data-ttu-id="14b61-140">لتكوين ما إذا كان يجب استخدام الوظيفة الإضافية لتحسين التخطيط للتخطيط الرئيسي، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **معلمات تحسين التخطيط** .</span><span class="sxs-lookup"><span data-stu-id="14b61-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters** .</span></span>

#### <a name="connection-status"></a><span data-ttu-id="14b61-141">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="14b61-141">Connection status</span></span>

<span data-ttu-id="14b61-142">تشير حالة الاتصال إلى الحالة الحالية للاتصال بين Supply Chain Management وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="14b61-143">ويوضح الجدول التالي القيم المحتملة.</span><span class="sxs-lookup"><span data-stu-id="14b61-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="14b61-144">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="14b61-144">Connection status</span></span> | <span data-ttu-id="14b61-145">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="14b61-145">Description</span></span> | <span data-ttu-id="14b61-146">هل يمكن استخدام تحسين التخطيط؟</span><span class="sxs-lookup"><span data-stu-id="14b61-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="14b61-147">متصل</span><span class="sxs-lookup"><span data-stu-id="14b61-147">Connected</span></span> | <span data-ttu-id="14b61-148">تم إنشاء اتصال بين خدمة تحسين التخطيط وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="14b61-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="14b61-149">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="14b61-149">Yes</span></span> |
| <span data-ttu-id="14b61-150">تمكين الاتصال</span><span class="sxs-lookup"><span data-stu-id="14b61-150">Enabling connection</span></span> | <span data-ttu-id="14b61-151">يتم حاليا تنفيذ طلب لتشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="14b61-152">لا</span><span class="sxs-lookup"><span data-stu-id="14b61-152">No</span></span> |
| <span data-ttu-id="14b61-153">غير متصل</span><span class="sxs-lookup"><span data-stu-id="14b61-153">Disconnected</span></span> | <span data-ttu-id="14b61-154">لا يوجد اتصال بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="14b61-155">يمكن تشغيل الاتصال من LCS، كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="14b61-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="14b61-156">لا</span><span class="sxs-lookup"><span data-stu-id="14b61-156">No</span></span> |
| <span data-ttu-id="14b61-157">تعطيل الاتصال</span><span class="sxs-lookup"><span data-stu-id="14b61-157">Disabling connection</span></span> | <span data-ttu-id="14b61-158">يتم حاليا تنفيذ طلب لإيقاف تشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="14b61-159">لا</span><span class="sxs-lookup"><span data-stu-id="14b61-159">No</span></span> |
| <span data-ttu-id="14b61-160">حالة البدء</span><span class="sxs-lookup"><span data-stu-id="14b61-160">Getting status</span></span> | <span data-ttu-id="14b61-161">يقوم النظام بالانتظار للحصول على معلومات الحالة من خدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="14b61-162">لا</span><span class="sxs-lookup"><span data-stu-id="14b61-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="14b61-163">خيار استخدام تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="14b61-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="14b61-164">يحدد إعداد خيار **استخدام تحسين التخطيط** محرك التخطيط الذي يتم استخدامه للتخطيط الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="14b61-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="14b61-165">**نعم** – يُستخدم تحسين التخطيط للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="14b61-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="14b61-166">**لا** – يُستخدم محرك تخطيط Supply Chain Management المضمن للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="14b61-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="14b61-167">إذا تم تشغيل وظائف دفعة التخطيط الموجودة التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن أثناء تعيين خيار **استخدام تحسين التخطيط** إلى **نعم** ، فسوف تفشل هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="14b61-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes** , those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="14b61-168">التكامل مع الإعداد</span><span class="sxs-lookup"><span data-stu-id="14b61-168">Integration with the setup</span></span>

<span data-ttu-id="14b61-169">إذا كانت معاينه تحسين التخطيط قيد التشغيل، يتم إجراء التخطيط الرئيسي باستخدام الوظيفة الإضافية لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="14b61-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="14b61-170">في هذه الحالة، تتاثر نتائج التخطيط الرئيسي وميزاته.</span><span class="sxs-lookup"><span data-stu-id="14b61-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14b61-171">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="14b61-171">Additional resources</span></span>

[<span data-ttu-id="14b61-172">شروط وأحكام المعاينة</span><span class="sxs-lookup"><span data-stu-id="14b61-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="14b61-173">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="14b61-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="14b61-174">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="14b61-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="14b61-175">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="14b61-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="14b61-176">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="14b61-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="14b61-177">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="14b61-177">Cancel a planning job</span></span>](cancel-planning-job.md)
