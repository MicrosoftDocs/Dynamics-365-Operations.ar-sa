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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2020
ms.locfileid: "4421814"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="dba15-103">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="dba15-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dba15-104">وكما  [سبق ان تم الإعلان عنه](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios)، تتم جدوله تحسين التخطيط لاستبدال محرك التخطيط الرئيسي الموجود المضمن.</span><span class="sxs-lookup"><span data-stu-id="dba15-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="dba15-105">إذا كنت تستخدم حاليا مشغل التخطيط الرئيسي المضمن، فعليك البدء في تخطيط الترحيل لتخطيط تحسين الأداء الآن.</span><span class="sxs-lookup"><span data-stu-id="dba15-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="dba15-106">من المهم بدء عمليه الترحيل فورا لان العمليات قد تكون متاثره عند فرض الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="dba15-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="dba15-107">لتجنب مشكلات الدقائق الاخيره عند فرض الإهلاك، فاننا نشجعك بشده علي إكمال الترحيل قبل 1 ديسمبر 2020.</span><span class="sxs-lookup"><span data-stu-id="dba15-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="dba15-108">لا تدعم وظيفة تحسين التخطيط كافة الميزات المتوفرة في محرك التخطيط المضمن في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dba15-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="dba15-109">لذلك ، فانه من المهم تقييم ما إذا كانت مجموعة الميزات المتوفرة حاليا في تحسين التخطيط ستفي بمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="dba15-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="dba15-110">لا يتم تشغيل وظيفة تحسين التخطيط في الوقت الحالي بشكل افتراضي في Dynamics Lifecycle Services (LCS)، بحيث يكون لديك الفرصة لاجراء التقييم الخاص بك قبل تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="dba15-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="dba15-111">أنت بحاجه لطلب استثناء من الترحيل إلى تحسين أداء التخطيط في حاله عدم تضمين عمليه التخطيط الرئيسية للإنتاج (التخطيط الرئيسي الذي تم إنشاؤه من خلال أوامر الإنتاج المخططة) وأنت تطلب من محرك التخطيط الرئيسي المضمن في الإصدر 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="dba15-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="dba15-112">ويتم البدء في الإصدار 10.0.16، ويتم عرض الخطا في البيئات عند تشغيل تخطيط رئيسي مضمن دون إنشاء أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="dba15-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="dba15-113">يجب استخدام تحسين التخطيط لكافة عمليات التوزيع الجديدة التي لا تقوم بإنشاء أوامر إنتاج مخططه اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dba15-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="dba15-114">وسوف يتلقى مالكو البيئات الموجودة التي يقومون بتشغيل محرك التخطيط الرئيسي المضمن بدون إنشاء أوامر الإنتاج المخططة، رسالة تحتوي علي تفاصيل حول عمليه الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="dba15-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="dba15-115">نوصي بالعمل مع شريك لتقييم الترحيل وتخطيطه لتحسين أداء التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="dba15-116">قبل تشغيل تحسين التخطيط، نوصي بشده بتقييم نتائج تحليل ملائمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="dba15-117">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dba15-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="dba15-118">التوفر</span><span class="sxs-lookup"><span data-stu-id="dba15-118">Availability</span></span>
<span data-ttu-id="dba15-119">يتوفر تحسين التخطيط حاليا في مناطق Azure التالية: الولايات المتحدة وكندا وأوروبا والمملكة المتحدة وأستراليا.</span><span class="sxs-lookup"><span data-stu-id="dba15-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="dba15-120">إذا حاولت تثبيت الوظيفة الإضافية  من منطقه أخرى ، فسوف يُظهر لك LCS رسالة بأن هذه المنطقة الجغرافية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="dba15-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="dba15-121">لاحظ أن تحسين التخطيط لا يدعم عمليات النشر المحلية لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dba15-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="dba15-122">الترخيص</span><span class="sxs-lookup"><span data-stu-id="dba15-122">Licensing</span></span>

<span data-ttu-id="dba15-123">إذا كان بإمكانك تشغيل التخطيط الرئيسي باستخدام الترخيص الحالي ، فلن تحتاج إلى شراء ترخيص إضافي للبدء في استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="dba15-124">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="dba15-124">Install the add-in</span></span>

<span data-ttu-id="dba15-125">لاستخدام أمثليه التخطيط، قم بتثبيت الوظيفة الإضافية لتحسين التخطيط لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dba15-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="dba15-126">يمكنك الوصول إلى الوظيفة الإضافية من مشروع LCS وتشغيل وظيفة تحسين التخطيط من واجهه مستخدم Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="dba15-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="dba15-127">يُعد متطلب تحسين التخطيط بيئة ذات توفر عالي الطبقة 2 أو أعلى بتمكين LCS (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="dba15-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="dba15-128">إذا حاولت تثبيت الوظيفة الإضافية  في بيئة OneBox، لن يكتمل التثبيت وستحتاج إلى إلغاء التثبيت.</span><span class="sxs-lookup"><span data-stu-id="dba15-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="dba15-129">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="dba15-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="dba15-130">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="dba15-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="dba15-131">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="dba15-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="dba15-132">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="dba15-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="dba15-133">حدد **تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="dba15-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="dba15-134">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="dba15-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="dba15-135">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="dba15-135">Select **Install**.</span></span>
1. <span data-ttu-id="dba15-136">في علامة التبويب السريعة **الوظائف الإضافية للبيئة‬**، ينبغي رؤية "جارِ تثبيت تحسين التخطيط".</span><span class="sxs-lookup"><span data-stu-id="dba15-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="dba15-137">بعد بضع دقائق ينبغي تغيير **جارٍ التثبيت** إلى **تم التثبيت** (قد تحتاج إلى تحديث الصفحة).</span><span class="sxs-lookup"><span data-stu-id="dba15-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="dba15-138">عندما يتم التثبيت، ستكون جاهزًا لتنشيط تحسين التخطيط في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dba15-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="dba15-139">الغرض الأساسي من تثبيت الوظيفة الاضافيه لتحسين أداء التخطيط هو الاتصال بالخدمة والبيئة.</span><span class="sxs-lookup"><span data-stu-id="dba15-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="dba15-140">ولذلك ، يجب عليك تثبيت الوظيفة الاضافيه بشكل منفصل علي كل بيئة حيث سيتم استخدام أمثليه التخطيط ، بغض النظر عن إيه تعليمات برمجيه تم نقلها بين البيئات.</span><span class="sxs-lookup"><span data-stu-id="dba15-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="dba15-141">تكامل تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="dba15-141">Planning Optimization integration</span></span>

<span data-ttu-id="dba15-142">لتكوين ما إذا كان يجب استخدام الوظيفة الإضافية لتحسين التخطيط للتخطيط الرئيسي، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **معلمات تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="dba15-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="dba15-143">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="dba15-143">Connection status</span></span>

<span data-ttu-id="dba15-144">تشير حالة الاتصال إلى الحالة الحالية للاتصال بين Supply Chain Management وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="dba15-145">ويوضح الجدول التالي القيم المحتملة.</span><span class="sxs-lookup"><span data-stu-id="dba15-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="dba15-146">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="dba15-146">Connection status</span></span> | <span data-ttu-id="dba15-147">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="dba15-147">Description</span></span> | <span data-ttu-id="dba15-148">هل يمكن استخدام تحسين التخطيط؟</span><span class="sxs-lookup"><span data-stu-id="dba15-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="dba15-149">متصل</span><span class="sxs-lookup"><span data-stu-id="dba15-149">Connected</span></span> | <span data-ttu-id="dba15-150">تم إنشاء اتصال بين خدمة تحسين التخطيط وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dba15-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="dba15-151">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="dba15-151">Yes</span></span> |
| <span data-ttu-id="dba15-152">تمكين الاتصال</span><span class="sxs-lookup"><span data-stu-id="dba15-152">Enabling connection</span></span> | <span data-ttu-id="dba15-153">يتم حاليا تنفيذ طلب لتشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="dba15-154">لا</span><span class="sxs-lookup"><span data-stu-id="dba15-154">No</span></span> |
| <span data-ttu-id="dba15-155">غير متصل</span><span class="sxs-lookup"><span data-stu-id="dba15-155">Disconnected</span></span> | <span data-ttu-id="dba15-156">لا يوجد اتصال بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="dba15-157">يمكن تشغيل الاتصال من LCS، كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="dba15-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="dba15-158">لا</span><span class="sxs-lookup"><span data-stu-id="dba15-158">No</span></span> |
| <span data-ttu-id="dba15-159">تعطيل الاتصال</span><span class="sxs-lookup"><span data-stu-id="dba15-159">Disabling connection</span></span> | <span data-ttu-id="dba15-160">يتم حاليا تنفيذ طلب لإيقاف تشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="dba15-161">لا</span><span class="sxs-lookup"><span data-stu-id="dba15-161">No</span></span> |
| <span data-ttu-id="dba15-162">حالة البدء</span><span class="sxs-lookup"><span data-stu-id="dba15-162">Getting status</span></span> | <span data-ttu-id="dba15-163">يقوم النظام بالانتظار للحصول على معلومات الحالة من خدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="dba15-164">لا</span><span class="sxs-lookup"><span data-stu-id="dba15-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="dba15-165">خيار استخدام تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="dba15-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="dba15-166">يحدد إعداد خيار **استخدام تحسين التخطيط** محرك التخطيط الذي يتم استخدامه للتخطيط الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="dba15-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="dba15-167">**نعم** – يُستخدم تحسين التخطيط للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dba15-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="dba15-168">**لا** – يُستخدم محرك تخطيط Supply Chain Management المضمن للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dba15-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="dba15-169">إذا تم تشغيل وظائف دفعة التخطيط الموجودة التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن أثناء تعيين خيار **استخدام تحسين التخطيط** إلى **نعم**، فسوف تفشل هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="dba15-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="dba15-170">التكامل مع الإعداد</span><span class="sxs-lookup"><span data-stu-id="dba15-170">Integration with the setup</span></span>

<span data-ttu-id="dba15-171">إذا كان تحسين التخطيط قيد التشغيل، يتم إجراء التخطيط الرئيسي باستخدام الوظيفة الإضافية لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="dba15-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="dba15-172">في هذه الحالة، تتاثر نتائج التخطيط الرئيسي وميزاته.</span><span class="sxs-lookup"><span data-stu-id="dba15-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dba15-173">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dba15-173">Additional resources</span></span>

[<span data-ttu-id="dba15-174">شروط وأحكام المعاينة</span><span class="sxs-lookup"><span data-stu-id="dba15-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="dba15-175">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="dba15-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="dba15-176">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="dba15-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="dba15-177">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="dba15-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="dba15-178">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="dba15-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="dba15-179">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="dba15-179">Cancel a planning job</span></span>](cancel-planning-job.md)
