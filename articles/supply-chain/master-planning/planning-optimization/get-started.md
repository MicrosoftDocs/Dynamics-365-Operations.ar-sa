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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a41f69958d84fb67b7cd8b6b4c7de38da23552f3
ms.sourcegitcommit: 2b76d4443b2867205db156648125a894f395a495
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2021
ms.locfileid: "5091075"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="409ce-103">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="409ce-104">وكما  [سبق ان تم الإعلان عنه](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios)، تتم جدوله تحسين التخطيط لاستبدال محرك التخطيط الرئيسي الموجود المضمن.</span><span class="sxs-lookup"><span data-stu-id="409ce-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="409ce-105">إذا كنت تستخدم حاليا مشغل التخطيط الرئيسي المضمن، فعليك البدء في تخطيط الترحيل لتخطيط تحسين الأداء الآن.</span><span class="sxs-lookup"><span data-stu-id="409ce-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="409ce-106">من المهم بدء عمليه الترحيل فورا لان العمليات قد تكون متاثره عند فرض الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="409ce-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="409ce-107">لتجنب مشكلات الدقائق الاخيره عند فرض الإهلاك، فاننا نشجعك بشده علي إكمال الترحيل قبل 1 ديسمبر 2020.</span><span class="sxs-lookup"><span data-stu-id="409ce-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="409ce-108">لا تدعم وظيفة تحسين التخطيط كافة الميزات المتوفرة في محرك التخطيط المضمن في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="409ce-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="409ce-109">لذلك ، فانه من المهم تقييم ما إذا كانت مجموعة الميزات المتوفرة حاليا في تحسين التخطيط ستفي بمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="409ce-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="409ce-110">لا يتم تشغيل وظيفة تحسين التخطيط في الوقت الحالي بشكل افتراضي في Dynamics Lifecycle Services (LCS)، بحيث يكون لديك الفرصة لاجراء التقييم الخاص بك قبل تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="409ce-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="409ce-111">أنت بحاجه لطلب استثناء من الترحيل إلى تحسين أداء التخطيط في حاله عدم تضمين عمليه التخطيط الرئيسية للإنتاج (التخطيط الرئيسي الذي تم إنشاؤه من خلال أوامر الإنتاج المخططة) وأنت تطلب من محرك التخطيط الرئيسي المضمن في الإصدر 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="409ce-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="409ce-112">ويتم البدء في الإصدار 10.0.16، ويتم عرض الخطا في البيئات عند تشغيل تخطيط رئيسي مضمن دون إنشاء أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="409ce-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="409ce-113">يجب استخدام تحسين التخطيط لكافة عمليات التوزيع الجديدة التي لا تقوم بإنشاء أوامر إنتاج مخططه اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="409ce-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="409ce-114">وسوف يتلقى مالكو البيئات الموجودة التي يقومون بتشغيل محرك التخطيط الرئيسي المضمن بدون إنشاء أوامر الإنتاج المخططة، رسالة تحتوي علي تفاصيل حول عمليه الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="409ce-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="409ce-115">نوصي بالعمل مع شريك لتقييم الترحيل وتخطيطه لتحسين أداء التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="409ce-116">قبل تشغيل تحسين التخطيط، نوصي بشده بتقييم نتائج تحليل ملائمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="409ce-117">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="409ce-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="409ce-118">التوفر</span><span class="sxs-lookup"><span data-stu-id="409ce-118">Availability</span></span>

<span data-ttu-id="409ce-119">يتوفر تحسين التخطيط حاليا في مناطق Azure التالية: الولايات المتحدة وكندا وأوروبا والمملكة المتحدة وأستراليا ودول آسيا المطلة على المحيط الهادئ.</span><span class="sxs-lookup"><span data-stu-id="409ce-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="409ce-120">إذا حاولت تثبيت الوظيفة الإضافية  من منطقه أخرى ، فسوف يُظهر لك LCS رسالة بأن هذه المنطقة الجغرافية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="409ce-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="409ce-121">لاحظ أن تحسين التخطيط لا يدعم عمليات النشر المحلية لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="409ce-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="409ce-122">الترخيص</span><span class="sxs-lookup"><span data-stu-id="409ce-122">Licensing</span></span>

<span data-ttu-id="409ce-123">إذا كان بإمكانك تشغيل التخطيط الرئيسي باستخدام الترخيص الحالي ، فلن تحتاج إلى شراء ترخيص إضافي للبدء في استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="409ce-124">تثبيت وتمكين تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="409ce-125">لاستخدام تحسين التخطيط، يجب التاكد من ان النظام يحتوي علي كافة المتطلبات المسبقة، ثم تمكين مفتاح الترخيص الخاص بها وتثبيت الوظيفة الاضافيه لتحسين أداء التخطيط Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="409ce-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="409ce-126">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="409ce-126">Prerequisites</span></span>

<span data-ttu-id="409ce-127">قبل أن تتمكن من تثبيت الوظيفة الإضافة لتحسين التخطيط، يجب إتمام المهام المتطلبات التالية:</span><span class="sxs-lookup"><span data-stu-id="409ce-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="409ce-128">يجب تشغيل Supply Chain Management على بيئة ذات توفر عالي الطبقة 2 أو أعلى بتمكين LCS (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="409ce-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="409ce-129">إذا حاولت تثبيت الوظيفة الإضافية  في بيئة OneBox، لن يكتمل التثبيت وستحتاج إلى إلغاء التثبيت.</span><span class="sxs-lookup"><span data-stu-id="409ce-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="409ce-130">يجب اعداد النظام Power Platform للتكامل.</span><span class="sxs-lookup"><span data-stu-id="409ce-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="409ce-131">لمزيد من المعلومات، راجع [المتطلبات الاساسيه لاعداد الوظائف الاضافيه](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins)[واعداد الوظائف الاضافيه](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span><span class="sxs-lookup"><span data-stu-id="409ce-131">For more information, see [Prerequisites for setting up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) and [Set up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="409ce-132">تمكين ترخيص تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="409ce-133">لاستخدام تحسين التخطيط، يجب تمكين مفتاح التكوين الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="409ce-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="409ce-134">وللقيام بذلك:</span><span class="sxs-lookup"><span data-stu-id="409ce-134">To do so:</span></span>

1. <span data-ttu-id="409ce-135">وضع النظام في وضع الصيانة كما هو موضح في [وضع الصيانة](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="409ce-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="409ce-136">انتقل إلى **إدارة النظام \> الإعداد \> تكوين الترخيص**.</span><span class="sxs-lookup"><span data-stu-id="409ce-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="409ce-137">في علامة التبويب **مفاتيح التكوين**، حدد خانه الاختيار **لتحسين أداء التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="409ce-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="409ce-138">إيقاف تشغيل وضع الصيانة كما هو موضح في [وضع الصيانة](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="409ce-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="409ce-139">تثبيت الوظيفة الإضافية لتحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="409ce-140">يجب تثبيت الوظيفة الإضافية من مشروع LCS وتشغيل وظيفة تحسين التخطيط من واجهه مستخدم Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="409ce-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="409ce-141">لتثبيت الوظيفة الإضافية لتحسين التخطيط:</span><span class="sxs-lookup"><span data-stu-id="409ce-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="409ce-142">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="409ce-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="409ce-143">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="409ce-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="409ce-144">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="409ce-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="409ce-145">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="409ce-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="409ce-146">حدد **تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="409ce-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="409ce-147">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="409ce-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="409ce-148">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="409ce-148">Select **Install**.</span></span>
1. <span data-ttu-id="409ce-149">في علامة التبويب السريعة **الوظائف الإضافية للبيئة‬**، ينبغي رؤية "جارِ تثبيت تحسين التخطيط".</span><span class="sxs-lookup"><span data-stu-id="409ce-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="409ce-150">بعد بضع دقائق ينبغي تغيير **جارٍ التثبيت** إلى **تم التثبيت** (قد تحتاج إلى تحديث الصفحة).</span><span class="sxs-lookup"><span data-stu-id="409ce-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="409ce-151">عندما يتم التثبيت، ستكون جاهزًا لتنشيط تحسين التخطيط في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="409ce-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="409ce-152">الغرض الأساسي من تثبيت الوظيفة الاضافيه لتحسين أداء التخطيط هو الاتصال بالخدمة والبيئة.</span><span class="sxs-lookup"><span data-stu-id="409ce-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="409ce-153">ولذلك ، يجب عليك تثبيت الوظيفة الاضافيه بشكل منفصل علي كل بيئة حيث سيتم استخدام أمثليه التخطيط ، بغض النظر عن إيه تعليمات برمجيه تم نقلها بين البيئات.</span><span class="sxs-lookup"><span data-stu-id="409ce-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="409ce-154">تكامل أمثليه التخطيط مع النظام الخاص بك</span><span class="sxs-lookup"><span data-stu-id="409ce-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="409ce-155">لتكوين ما إذا كان يجب استخدام الوظيفة الإضافية لتحسين التخطيط للتخطيط الرئيسي، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **معلمات تحسين التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="409ce-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="409ce-156">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="409ce-156">Connection status</span></span>

<span data-ttu-id="409ce-157">تشير حالة الاتصال إلى الحالة الحالية للاتصال بين Supply Chain Management وخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="409ce-158">ويوضح الجدول التالي القيم المحتملة.</span><span class="sxs-lookup"><span data-stu-id="409ce-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="409ce-159">حالة الاتصال</span><span class="sxs-lookup"><span data-stu-id="409ce-159">Connection status</span></span> | <span data-ttu-id="409ce-160">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="409ce-160">Description</span></span> | <span data-ttu-id="409ce-161">هل يمكن استخدام تحسين التخطيط؟</span><span class="sxs-lookup"><span data-stu-id="409ce-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="409ce-162">متصل</span><span class="sxs-lookup"><span data-stu-id="409ce-162">Connected</span></span> | <span data-ttu-id="409ce-163">تم إنشاء اتصال بين خدمة تحسين التخطيط وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="409ce-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="409ce-164">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="409ce-164">Yes</span></span> |
| <span data-ttu-id="409ce-165">تمكين الاتصال</span><span class="sxs-lookup"><span data-stu-id="409ce-165">Enabling connection</span></span> | <span data-ttu-id="409ce-166">يتم حاليا تنفيذ طلب لتشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="409ce-167">لا</span><span class="sxs-lookup"><span data-stu-id="409ce-167">No</span></span> |
| <span data-ttu-id="409ce-168">غير متصل</span><span class="sxs-lookup"><span data-stu-id="409ce-168">Disconnected</span></span> | <span data-ttu-id="409ce-169">لا يوجد اتصال بخدمه تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="409ce-170">يمكن تشغيل الاتصال من LCS، كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="409ce-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="409ce-171">لا</span><span class="sxs-lookup"><span data-stu-id="409ce-171">No</span></span> |
| <span data-ttu-id="409ce-172">تعطيل الاتصال</span><span class="sxs-lookup"><span data-stu-id="409ce-172">Disabling connection</span></span> | <span data-ttu-id="409ce-173">يتم حاليا تنفيذ طلب لإيقاف تشغيل الاتصال بخدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="409ce-174">لا</span><span class="sxs-lookup"><span data-stu-id="409ce-174">No</span></span> |
| <span data-ttu-id="409ce-175">حالة البدء</span><span class="sxs-lookup"><span data-stu-id="409ce-175">Getting status</span></span> | <span data-ttu-id="409ce-176">يقوم النظام بالانتظار للحصول على معلومات الحالة من خدمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="409ce-177">لا</span><span class="sxs-lookup"><span data-stu-id="409ce-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="409ce-178">خيار استخدام تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="409ce-179">يحدد إعداد خيار **استخدام تحسين التخطيط** محرك التخطيط الذي يتم استخدامه للتخطيط الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="409ce-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="409ce-180">**نعم** – يُستخدم تحسين التخطيط للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="409ce-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="409ce-181">**لا** – يُستخدم محرك تخطيط Supply Chain Management المضمن للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="409ce-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="409ce-182">إذا تم تشغيل وظائف دفعة التخطيط الموجودة التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن أثناء تعيين خيار **استخدام تحسين التخطيط** إلى **نعم**، فسوف تفشل هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="409ce-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="409ce-183">التكامل مع الإعداد</span><span class="sxs-lookup"><span data-stu-id="409ce-183">Integration with the setup</span></span>

<span data-ttu-id="409ce-184">إذا كان تحسين التخطيط قيد التشغيل، يتم إجراء التخطيط الرئيسي باستخدام الوظيفة الإضافية لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="409ce-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="409ce-185">في هذه الحالة، تتاثر نتائج التخطيط الرئيسي وميزاته.</span><span class="sxs-lookup"><span data-stu-id="409ce-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="409ce-186">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="409ce-186">Additional resources</span></span>

[<span data-ttu-id="409ce-187">شروط وأحكام المعاينة</span><span class="sxs-lookup"><span data-stu-id="409ce-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="409ce-188">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="409ce-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="409ce-189">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="409ce-190">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="409ce-191">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="409ce-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="409ce-192">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="409ce-192">Cancel a planning job</span></span>](cancel-planning-job.md)
