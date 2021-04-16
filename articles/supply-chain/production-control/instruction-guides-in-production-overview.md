---
title: توفير دلائل الحقيقة المختلطة للعمال العاملين في الإنتاج
description: يوضح هذا الموضوع كيفيه تكامل الوحدة النمطية لإداره الإنتاج في Microsoft Dynamics 365 Supply Chain Management مع Dynamics 365 Guides.
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 59fe3996013737198d4fbc86d64f8ef9dbe035e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829344"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="36e7f-103">توفير دلائل الحقيقة المختلطة للعمال العاملين في الإنتاج</span><span class="sxs-lookup"><span data-stu-id="36e7f-103">Provide mixed-reality Guides for workers in production</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="36e7f-104">سيستفيد العاملون في عمليات الإنتاج من الإرشادات ذات الصلة التي يتم توفيرها في الوقت المناسب في سياق عملهم.</span><span class="sxs-lookup"><span data-stu-id="36e7f-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="36e7f-105">يتم تطبيق *الإرشادات* في العديد من مجالات العمل، بما في ذلك: التجميع والخدمة والعمليات والشهادات والأمان.</span><span class="sxs-lookup"><span data-stu-id="36e7f-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="36e7f-106">عبر كافة وظائف الاعمال الاساسيه هذه، يمكن ان تساعد إرشادات التدريب الحالية علي تمكين العاملين من تحقيق المزيد والعمل بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="36e7f-107">مقدمة</span><span class="sxs-lookup"><span data-stu-id="36e7f-107">Introduction</span></span>

<span data-ttu-id="36e7f-108">يمكنك توفير الإرشادات بطرق مختلفه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="36e7f-109">أحد الانظمه الفعالة يستخدم [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="36e7f-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="36e7f-110">Dynamics 365 Guides من الممكن ان يساعد في زيادة الموظفين مع التعلم التبادلي.</span><span class="sxs-lookup"><span data-stu-id="36e7f-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="36e7f-111">يمكنك تحديد العمليات القياسية بالإرشادات خطوه بخطوه التي ترشد الموظفين إلى الادوات والأجزاء التي تحتاجها وتعرض على الموظفين كيفيه استخدام هذه الادوات في مواقف العمل الفعلية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="36e7f-112">يمكنك إرفاق خطوط إرشاد لجوانب متعددة من التحكم في الإنتاج بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="36e7f-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="36e7f-113">الموارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-113">Resources</span></span>](#resources)
- [<span data-ttu-id="36e7f-114">مجموعات الموارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="36e7f-115">المنتجات الصادرة</span><span class="sxs-lookup"><span data-stu-id="36e7f-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="36e7f-116">التركيبات</span><span class="sxs-lookup"><span data-stu-id="36e7f-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="36e7f-117">إصدارات التركيبة</span><span class="sxs-lookup"><span data-stu-id="36e7f-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="36e7f-118">قائمة مكونات الصنف (BOMs)</span><span class="sxs-lookup"><span data-stu-id="36e7f-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="36e7f-119">إصدارات BOM</span><span class="sxs-lookup"><span data-stu-id="36e7f-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="36e7f-120">المسارات</span><span class="sxs-lookup"><span data-stu-id="36e7f-120">Routes</span></span>](#routes)
- [<span data-ttu-id="36e7f-121">إصدارات المسارات</span><span class="sxs-lookup"><span data-stu-id="36e7f-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="36e7f-122">‏‏علاقات عمليات المسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="36e7f-123">يمكنك أيضا إرفاق الدلائل باداره الأصول.</span><span class="sxs-lookup"><span data-stu-id="36e7f-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="36e7f-124">لمزيد من المعلومات حول هذا الخيار، راجع [دمج Dynamics 365 Supply Chain Management (إدارة الأصول) مع Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="36e7f-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="36e7f-125">عندما يقوم عامل البند الأول باختيار وظيفة في حاله العمل من خلال Supply Chain Management، يمكن للعامل رؤية [الدلائل ذات الصلة](#logic) على بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="36e7f-126">عندما يختار العامل دليلا معينا، يتم عرض شفره QR لذلك الدليل علي الشاشة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="36e7f-127">ثم يستخدم العامل HoloLens الخاص بهم لمسح شفره الاستجابة السريعة، والتي تعرض الدلائل وتظهر الإرشادات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="36e7f-128">تصف الأقسام الفرعية التالية قليل من السيناريوهات المحددة حيث يمكن للشركات عبر الصناعات الاطلاع علي أكبر قيمه عند استخدام الدلائل لتقديم الإرشادات الخاصة بالتصنيع.</span><span class="sxs-lookup"><span data-stu-id="36e7f-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="36e7f-129">التجميع</span><span class="sxs-lookup"><span data-stu-id="36e7f-129">Assembly</span></span>

<span data-ttu-id="36e7f-130">![استخدام الدلائل في مهام التجميع](media/instruction-guides-hero-assembly.png "استخدام الدلائل في مهام الخدمة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="36e7f-131">الإرشادات في عمليات التجميع تظهر العمال الادوات والأجزاء التي تحتاجها وكيفيه استخدامها في مواقف العمل الحقيقي.</span><span class="sxs-lookup"><span data-stu-id="36e7f-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="36e7f-132">ويمكن لمديري الإنتاج إنشاء الدئلال وتعيينها، علي سبيل المثال، بالنسبة [لمسارات الإنتاج ](routes-operations.md)أو [علاقات العمليات](routes-operations.md#operation-relations) أو [ قائمة مكونات الصنف](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="36e7f-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="36e7f-133">سيقوم العاملون بالعثور علي الإرشادات المناسبة حول خبره العملية الخاصة بحاله العمل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="36e7f-134">الخدمة</span><span class="sxs-lookup"><span data-stu-id="36e7f-134">Service</span></span>

<span data-ttu-id="36e7f-135">![استخدام الدلائل في مهام الخدمة](media/instruction-guides-hero-service.png "استخدام الدلائل في مهام الخدمة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="36e7f-136">تجهيز الفنيين الذين لهم تعليمات ارشاديه في موقع الوظيفة، مما يؤدي إلى إزاله الحاجة إلى جدوله زيارات اضافيه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="36e7f-137">يمكن لمديري الخدمة تعيين الدلائل، علي سبيل المثال، [لمنتجات ](../../commerce/product.md)محدده تقودها من خلال إجراءات تقييم الجودة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="36e7f-138">الكمية</span><span class="sxs-lookup"><span data-stu-id="36e7f-138">Quality</span></span>

<span data-ttu-id="36e7f-139">![استخدام الدلائل في مهام ضمان الجودة](media/instruction-guides-hero-quality.png "استخدام الدلائل في مهام ضمان الجودة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="36e7f-140">تقوم بتمهيد العمليات الجديدة والتاكد من زيادة التناسق عن طريق تحويل معرفة الموظف إلى أداه قابلة للتكرار.</span><span class="sxs-lookup"><span data-stu-id="36e7f-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="36e7f-141">يمكن لمديري ضمان الجودة تعيين خطوط إرشاد، علي سبيل المثال، [لمنتجات ](../../commerce/product.md)محدده تقودها من خلال إجراءات تقييم الجودة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="36e7f-142">الشهادات</span><span class="sxs-lookup"><span data-stu-id="36e7f-142">Certifications</span></span>

<span data-ttu-id="36e7f-143">![استخدام الدلائل للمهام المتعلقة بالشهادات](media/instruction-guides-hero-certification.png "استخدام الدلائل للمهام المتعلقة بالشهادات")</span><span class="sxs-lookup"><span data-stu-id="36e7f-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="36e7f-144">تاكد من ان كل موظف يفي بالمعايير العالية بسرعة وذلك من خلال تحديد من يحتاج إلى المساعدة و أين.</span><span class="sxs-lookup"><span data-stu-id="36e7f-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="36e7f-145">أمان</span><span class="sxs-lookup"><span data-stu-id="36e7f-145">Safety</span></span>

<span data-ttu-id="36e7f-146">![استخدام الدلائل في تعليمات أمان العمل](media/instruction-guides-hero-safety.png "استخدام الدلائل في تعليمات أمان العمل")</span><span class="sxs-lookup"><span data-stu-id="36e7f-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="36e7f-147">توفير الإرشادات التي تقود الإجراءات الخطيرة فعليا قبل المحاولة في البيئة الفعلية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="36e7f-148">من خلال منهج الحقيقة المختلطة، يمكن للعاملين تجربه إجراءات خطيره فعليا.</span><span class="sxs-lookup"><span data-stu-id="36e7f-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="36e7f-149">ويمكن لمديري الإنتاج تقديم إرشادات معالجه مخصصه لمعالجه المواد الخطرة أو لإجراءات معالجه دقيقة عن طريق تعيين الإرشادات إلى [عناصر ](../../commerce/product.md)المنتجات [والمسارات ](routes-operations.md)[والعمليات](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="36e7f-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="36e7f-150">الشروع في العمل بالإرشادات والدلائل</span><span class="sxs-lookup"><span data-stu-id="36e7f-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="36e7f-151">لتمكين الإرشادات في عمليات الإنتاج، توفر Supply Chain Management تكاملا خارج الصندوق مع Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="36e7f-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="36e7f-152">يتطلب مثيل تطبيق Guides المرخص والمثبت لبناء وصيانة وتعيين إرشادات الحقيقة المختلطة لأصول الإنتاج والعمل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="36e7f-153">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="36e7f-153">Prerequisites</span></span>

<span data-ttu-id="36e7f-154">لاستخدام هذه الميزة، يجب ان يتضمن النظام ما يلي:</span><span class="sxs-lookup"><span data-stu-id="36e7f-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="36e7f-155">الإصدار 10.0.15 من Dynamics 365 Supply Chain Management أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="36e7f-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="36e7f-156">[قم بتشغيل الكتابة المزدوجة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) لتطبيقات Supply Chain Management apps.</span><span class="sxs-lookup"><span data-stu-id="36e7f-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="36e7f-157">الإصدار [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 400.0.1.48 إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="36e7f-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="36e7f-158">تشغيل الميزة</span><span class="sxs-lookup"><span data-stu-id="36e7f-158">Turn on the feature</span></span>

<span data-ttu-id="36e7f-159">لجعل الميزة متوفرة علي النظام، يجب تمكين مفاتيح التكوين الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="36e7f-160">وتحتاج فقط للقيام بذلك مره واحده.</span><span class="sxs-lookup"><span data-stu-id="36e7f-160">You only need to do this once.</span></span> <span data-ttu-id="36e7f-161">للقيام بذلك، يجب علي المسؤول القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="36e7f-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="36e7f-162">وضع النظام في وضع الصيانة كما هو موضح في [وضع الصيانة](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="36e7f-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="36e7f-163">انتقل إلى **إدارة النظام \> الإعداد \> تكوين الترخيص**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="36e7f-164">قم بتوسيع مقطع **الحقيقة المختلطة** ثم حدد خانه الاختيار **دليل الحقيقة المختلطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="36e7f-165">قم بتوسيع مقطع **إدارة الإنتاج**، ثم حدد خانة الاختيار **إرشادات الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="36e7f-166">إيقاف تشغيل وضع الصيانة كما هو موضح في [وضع الصيانة](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="36e7f-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="36e7f-167">تكوين كيفيه ظهور الدلائل في صالة الإنتاج</span><span class="sxs-lookup"><span data-stu-id="36e7f-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="36e7f-168">لتكوين طريقه ظهور الدلائل في صالة الإنتاج، انتقل إلى **الحقيقة المختلطة \>Dynamics 365 Guides\>تكوين تكامل الدلائل**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="36e7f-169">![تكوين تكامل الدليل للتصنيع](media/instruction-guides-configure-integration.png "تكوين تكامل الدليل للتصنيع")</span><span class="sxs-lookup"><span data-stu-id="36e7f-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="36e7f-170">قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="36e7f-170">Set the following fields:</span></span>

- <span data-ttu-id="36e7f-171">**Microsoft Dataverse URL** - تحديد محدد موقع المعلومات (URL) لبيئة Microsoft Dataverse التي تقوم فيها بإنشاء Guides.</span><span class="sxs-lookup"><span data-stu-id="36e7f-171">**Microsoft Dataverse URL** - Specify the URL for the Microsoft Dataverse environment where you create your Guides.</span></span> <span data-ttu-id="36e7f-172">التنسيق هو "contoso.crm4.dynamics.com"، حيث تتم تسميه الجزء الأول من عنوان URL عاده بعد مؤسستك (مثل "شركه الأصدقاء") ، والجزء الثاني خاص بمنطقه البيانات الخاصة بالبيئة الخاصة بك (مثل "crm4") ، والجزء الأخير هو المجال (مثل "dynamics.com").</span><span class="sxs-lookup"><span data-stu-id="36e7f-172">The format is "contoso.crm4.dynamics.com", where the first part of the URL is typically named after your organization (such as "contoso."), the second part is specific to the data region of your environment (such as "crm4."), and the last part is the domain (such as "dynamics.com").</span></span> <span data-ttu-id="36e7f-173">وهناك طريقه واحده للعثور علي URL الصحيح[وهو الانتقال إلى home.dynamics.com ](https://home.dynamics.com/)ثم فتح تطبيق Guides الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-173">One way to find the right URL is to go to [home.dynamics.com](https://home.dynamics.com/) and then open your Guides app.</span></span> <span data-ttu-id="36e7f-174">عند فتح Guides، ستشاهد عنوان الربط في شريط العنوان للمستعرض الخاص بك (فقط ياخذ محدد موقع المعلومات (URL) الأساسي ، والذي يجب ان يشبه المثال السابق).</span><span class="sxs-lookup"><span data-stu-id="36e7f-174">When Guides opens, you will see the URL in the address bar of your browser (only take the base URL, which should resemble the previous example).</span></span> <span data-ttu-id="36e7f-175">تستخدم هذه القيمة لإنشاء عناوين الأدلة الخاصة بك وسيتم ترميزها في أكواد QR."</span><span class="sxs-lookup"><span data-stu-id="36e7f-175">This value is used to compose addresses for your guides and will be encoded into the QR codes."</span></span>
- <span data-ttu-id="36e7f-176">**حجم كود QR** - تعيين حجم كود QR المقدم.</span><span class="sxs-lookup"><span data-stu-id="36e7f-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="36e7f-177">نوصي باختيار الحجم الذي سيملا معظم شاشه العرض، ولكن ليس المزيد.</span><span class="sxs-lookup"><span data-stu-id="36e7f-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="36e7f-178">وعاده ما تكون *15* قيمه جيده.</span><span class="sxs-lookup"><span data-stu-id="36e7f-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="36e7f-179">**مستوى تصحيح الخطأ لكود QR** - تعيين مستوى تفاصيل كود QR.</span><span class="sxs-lookup"><span data-stu-id="36e7f-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="36e7f-180">مستوى تفاصيل أعلى تساعد في زيادة موثوقيه الكود، ولكن يجب ان يكون **حجم كود QR الخاص بك** كبيرا بما فيه الكفاية لدعم مستوي التفاصيل المطلوب من قبل مستوي التصحيح المحدد.</span><span class="sxs-lookup"><span data-stu-id="36e7f-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>

> [!TIP]
> - <span data-ttu-id="36e7f-181">تحتاج احجام أكواد QR الكبيرة جدا بالنسبة لشاشه العرض وقتا أطول ليتم عرضها ثم يتم قياسها لتلائم الشاشة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="36e7f-182">ولا توفر هذه الخيارات بعض المزايا.</span><span class="sxs-lookup"><span data-stu-id="36e7f-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="36e7f-183">ان احجام أكواد QR الصغيرة جدا قد تقلل من قدرة HoloLens على قراءه الكود بشكل صحيح في بعض البيئات.</span><span class="sxs-lookup"><span data-stu-id="36e7f-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="36e7f-184">نوصي باختبار الإعدادات لكل جهاز من الاجهزه التي ستقوم بعرض أكواد QR لمستخدمي HoloLens.</span><span class="sxs-lookup"><span data-stu-id="36e7f-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="36e7f-185">اختر الإعدادات التي توفر امكانيه القراءة الكافية في بيئة صالة الإنتاج الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="36e7f-186">الحصول علي نظره عامه علي كافة تعيينات الدليل</span><span class="sxs-lookup"><span data-stu-id="36e7f-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="36e7f-187">استخدم الصفحة **كافة الادله** للاطلاع علي قائمه بكافة الادله المتوفرة في مؤسستك وكافة التعيينات لعمليات الإنتاج وموارده.</span><span class="sxs-lookup"><span data-stu-id="36e7f-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="36e7f-188">لفتحه، انتقل إلى **الحقيقة المختلطة\>الأدلة \>كافة الادله**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="36e7f-189">تظهر القائمة في الأعلى كافة الدلائل المتوفرة ويمكنك استخدام الحقل هنا لتصفيه القائمة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="36e7f-190">تعرض القائمة الموجودة في الأسفل كافة تعيينات الدليل وتوفر شريط أدوات لإدارتها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="36e7f-191">![إداره الأدلة](media/instruction-guides-allguides.png "إداره الأدلة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="36e7f-192">تصف الأقسام التالية أنواع الكائنات التي يمكنك تعيين أدلة لها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="36e7f-193">يوفر كل دليل معين إرشادات يتم إرفاقها تلقائيا بوظائف الإنتاج المرتبطة وستكون متوفرة في حاله العمل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="36e7f-194">اقران دليل بمورد</span><span class="sxs-lookup"><span data-stu-id="36e7f-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="36e7f-195">إضافه دليل إلى [مورد](operations-resources.md) لتقديم الدليل في سياق وظائف الإنتاج ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="36e7f-196">سيناريوهات نموذجية باستخدام الموارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-196">Typical scenario using resources</span></span>

<span data-ttu-id="36e7f-197">علي سبيل المثال، يمكنك إرفاق دليل بأمان الجهاز العام أو إرشادات المعالجة إلى مورد من النوع جهاز.</span><span class="sxs-lookup"><span data-stu-id="36e7f-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="36e7f-198">بعد ذلك، سيتوفر الدليل علي كل وظيفة يتم تنفيذها علي الجهاز.</span><span class="sxs-lookup"><span data-stu-id="36e7f-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="36e7f-199">إضافة دليل إلى مورد</span><span class="sxs-lookup"><span data-stu-id="36e7f-199">Add a Guide to a resource</span></span>

<span data-ttu-id="36e7f-200">لإضافة دليل إلى مورد:</span><span class="sxs-lookup"><span data-stu-id="36e7f-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="36e7f-201">الانتقال إلى **التحكم بالإنتاج \> الإعداد \> الموارد \> الموارد**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="36e7f-202">من جزء القائمة، حدد المورد الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-203">قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="36e7f-204">حدد **إضافه** من شريط الادوات **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="36e7f-205">تتم إضافة سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="36e7f-206">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="36e7f-207">إذا كان لديك عدد كبير من الادله، فيمكنك تصفيه القائمة للبحث عن القائمة التي تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="36e7f-208">![إداره الأدلة](media/instruction-guides-allguides.png "إداره الأدلة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="36e7f-209">اقران دليل بمجموعة موارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="36e7f-210">يمكنك أضافه دليل إلى [مجموعات الموارد](tasks/define-discrete-manufacturing-resource-group.md)، إذا كنت تستخدمها لأداره مجموعات الاجهزه أو خطوط الإنتاج أو خلايا العمل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="36e7f-211">سيناريوهات نموذجية باستخدام مجموعات الموارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="36e7f-212">**المثال رقم 1:** لقد قمت بتحديد مجموعه موارد لعده أجهزه من نفس الموديل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="36e7f-213">بدلا من تعيين دليل إرشادات المعالجة ذات الصلة لموديل الجهاز لكل مورد ذي صله، يمكنك بدلا من ذلك تعيين الدليل إلى مجموعه الموارد التي تعكس موديل الجهاز هذا.</span><span class="sxs-lookup"><span data-stu-id="36e7f-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="36e7f-214">**المثال 2:** لقد قمت بتحديد مجموعه موارد لخليه عمل تحتوي علي أجهزه مختلفه ولديك دليل يوفر إرشادات عامه حول كيفيه الحفاظ علي خليه العمل.</span><span class="sxs-lookup"><span data-stu-id="36e7f-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="36e7f-215">ينطبق الدليل علي اي نشاط إنتاج في خليه العمل هذه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="36e7f-216">إضافة دليل إلى مجموعة موارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="36e7f-217">لإضافة دليل إلى مجموعة موارد:</span><span class="sxs-lookup"><span data-stu-id="36e7f-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="36e7f-218">الانتقال إلى **التحكم بالإنتاج \> الإعداد \> الموارد \> مجموعات الموارد**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="36e7f-219">من جزء القائمة، حدد مجموعة الموارد التي ترغب في تعيين دليل اليها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-220">قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="36e7f-221">حدد **إضافه** من شريط الادوات **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="36e7f-222">تتم إضافة سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="36e7f-223">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="36e7f-224">إذا كان لديك عدد كبير من الادله، فيمكنك تصفيه القائمة للبحث عن القائمة التي تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="36e7f-225">![إضافة دليل إلى مجموعة موارد](media/instruction-guides-resourcegroup.png "إضافة دليل إلى مجموعة موارد")</span><span class="sxs-lookup"><span data-stu-id="36e7f-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="36e7f-226">اقران دليل بمنتج مطروح</span><span class="sxs-lookup"><span data-stu-id="36e7f-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="36e7f-227">يمكنك إضافه دليل إلى اي [منتج تم إصداره](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="36e7f-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="36e7f-228">سيناريو نموذجي باستخدام المنتجات التي تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="36e7f-228">Typical scenario using released products</span></span>

<span data-ttu-id="36e7f-229">تساعد دلائل مستوى المنتج عمال صالة الإنتاج بالمعلومات المتعلقة بتشغيل أو معالجه منتج أو صنف تم إصداره بعينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="36e7f-230">إضافة دليل إلى منتج تم إصداره</span><span class="sxs-lookup"><span data-stu-id="36e7f-230">Add a Guide to a released product</span></span>

<span data-ttu-id="36e7f-231">لإضافة دليل إلى منتج تم إصداره:</span><span class="sxs-lookup"><span data-stu-id="36e7f-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="36e7f-232">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات التي تم إصدارها**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="36e7f-233">افتح المنتج الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-234">في جزء الاجراء ، افتح علامة التبويب **المهندس** ومن المجموعة **عرض**، حدد **الدلائل المقترنة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="36e7f-235">تفتح صفحه **الادله** المرتبطة لمنتجك المحدد.</span><span class="sxs-lookup"><span data-stu-id="36e7f-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="36e7f-236">حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="36e7f-237">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-238">![إضافة دليل إلى منتج تم إصداره:](media/instruction-guides-ReleasedProduct-AddGuides.png "إضافة دليل إلى منتج تم إصداره")</span><span class="sxs-lookup"><span data-stu-id="36e7f-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="36e7f-239">اقران دليل بمعادلة</span><span class="sxs-lookup"><span data-stu-id="36e7f-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="36e7f-240">يمكنك إضافه دليل إلى اي [معادلة](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="36e7f-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="36e7f-241">سيناريوهات نموذجية باستخدام المعادلات</span><span class="sxs-lookup"><span data-stu-id="36e7f-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="36e7f-242">توفر الدلائل على مستوى المعادلات لعمال صالة الإنتاج إرشادات تعامل موجهة في سياق المعادلة أو الوصفة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="36e7f-243">يمكن أيضا تعيين الادله إلى إصدارات معادلة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="36e7f-244">يمكنك تعيين الإرشاد المناسب لعمليات الإنتاج استنادا إلى المعادلة إلى المسار أو إصدار المسار أو علاقات مسار العمليات.</span><span class="sxs-lookup"><span data-stu-id="36e7f-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="36e7f-245">لا يمكن إرفاق الادله حاليا بسطور المعادلة الفردية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="36e7f-246">إضافة دليل إلى معادلة</span><span class="sxs-lookup"><span data-stu-id="36e7f-246">Add a Guide to a formula</span></span>

<span data-ttu-id="36e7f-247">لإضافة دليل إلى معادلة:</span><span class="sxs-lookup"><span data-stu-id="36e7f-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="36e7f-248">انتقل إلى **إدارة معلومات المنتج \> قوائم مكونات الصنف والمعادلات‬ \> المعادلات**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="36e7f-249">افتح المعادلة التي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-250">افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="36e7f-251">قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="36e7f-252">حدد **إضافه** من شريط الادوات **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="36e7f-253">تتم إضافة سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="36e7f-254">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-255">![إضافة دليل إلى معادلة:](media/instruction-guides-Formula.png "إضافة دليل إلى معادلة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="36e7f-256">اقران دليل بإصدار معادلة</span><span class="sxs-lookup"><span data-stu-id="36e7f-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="36e7f-257">يمكنك إضافه دليل إلى اي [إصدار معادلة](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="36e7f-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="36e7f-258">سيناريوهات نموذجية باستخدام إصدارات المعادلات</span><span class="sxs-lookup"><span data-stu-id="36e7f-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="36e7f-259">توفر الادله المرفقة بالإصدار الفردي من المعادلة لعمال صالة الإنتاج تعليمات إرشادية خلال إنتاج هذا الإصدار من وصفة المعادلة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="36e7f-260">يمكنك تعيين الإرشاد المناسب لعمليات الإنتاج استنادا إلى إصدار المعادلة إلى مسار أو إصدار المسار أو علاقات عملية المسار.</span><span class="sxs-lookup"><span data-stu-id="36e7f-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="36e7f-261">لا يمكن إرفاق الادله حاليا بسطور المعادلة الفردية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="36e7f-262">إضافة دليل إلى إصدار معادلة</span><span class="sxs-lookup"><span data-stu-id="36e7f-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="36e7f-263">لإضافة دليل إلى إصدار معادلة:</span><span class="sxs-lookup"><span data-stu-id="36e7f-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="36e7f-264">انتقل إلى **إدارة معلومات المنتج \> قوائم مكونات الصنف والمعادلات‬ \> المعادلات**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="36e7f-265">افتح المعادلة التي تتضمن إصدارا تريد تعيين دليل له.</span><span class="sxs-lookup"><span data-stu-id="36e7f-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-266">افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="36e7f-267">في علامة التبويب السريعة **إصدارات المعادلة**، حدد الإصدار الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-268">في شريط الادوات **إصدارات المعادلة**، حدد **الأدلة المقترنة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="36e7f-269">![فتح الادله المقترنة بإصدار معادلة محدد](media/instruction-guides-FormulaVersion.png "فتح الادله المقترنة بإصدار معادلة محدد")</span><span class="sxs-lookup"><span data-stu-id="36e7f-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="36e7f-270">تفتح صفحه **الادله المقترنة** لإصدار المعادلة الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="36e7f-271">حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="36e7f-272">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-273">![إضافة دليل إلى معادلة](media/instruction-guides-FormulaVersionAddGuide.png "إضافة دليل إلى معادلة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="36e7f-274">إقران دليل بقائمه مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="36e7f-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="36e7f-275">يمكنك أضافه دليل إلى أيه [قائمة مكونات صنف](bill-of-material-bom.md) (BOM).</span><span class="sxs-lookup"><span data-stu-id="36e7f-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="36e7f-276">سيناريو نموذجي باستخدام قائمه مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="36e7f-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="36e7f-277">توفر الادله المرتبطة بقائمة مكونات الصنف لعمال صالة الإنتاج إرشادات حول كيفيه تجهيز المواد من قائمة BOM ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="36e7f-278">يمكن أيضا تعيين الادله إلى إصدارات قائمة BOM.</span><span class="sxs-lookup"><span data-stu-id="36e7f-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="36e7f-279">لا يمكن إرفاق الادله حاليا بسطور BOM.</span><span class="sxs-lookup"><span data-stu-id="36e7f-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="36e7f-280">إضافة دليل إلى قائمه مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="36e7f-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="36e7f-281">لإضافة دليل إلى قائمه مكونات الصنف:</span><span class="sxs-lookup"><span data-stu-id="36e7f-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="36e7f-282">انتقل إلى **إدارة معلومات الإنتاج \> قائمة مكونات الصنف والمعادلات \> قوائم مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="36e7f-283">افتح قائمة مكونات الصنف التي ترغب في تعيين دليل اليها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-284">افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="36e7f-285">قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="36e7f-286">حدد **إضافه** من شريط الادوات **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="36e7f-287">تتم إضافة سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="36e7f-288">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-289">![إضافة دليل إلى قائمة BOM](media/instruction-guides-BOM.png "إضافة دليل إلى قائمة BOM")</span><span class="sxs-lookup"><span data-stu-id="36e7f-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="36e7f-290">إقران دليل بإصدار قائمه مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="36e7f-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="36e7f-291">يمكنك أضافه دليل إلى أي [إصدار قائمة مكونات صنف](bill-of-material-bom.md#bom-and-formula-versions) (BOM).</span><span class="sxs-lookup"><span data-stu-id="36e7f-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="36e7f-292">سيناريو نموذجي باستخدام إصدارات قائمه مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="36e7f-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="36e7f-293">توفر الادله المرتبطة بإصدار قائمة مكونات الصنف الفرديه للعاملين في صالة الإنتاج إرشادات توضح كيفيه تجهيز ومعالجه المواد لإصدار قائمة مكونات الصنف تختلف عن قائمة مكونات الصنف العامة أو الإصدارات الأخرى الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="36e7f-294">لا يمكن إرفاق الادله حاليا بسطور BOM.</span><span class="sxs-lookup"><span data-stu-id="36e7f-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="36e7f-295">إضافة دليل إلى إصدار قائمه مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="36e7f-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="36e7f-296">لإضافة دليل إلى إصدار قائمه مكونات الصنف:</span><span class="sxs-lookup"><span data-stu-id="36e7f-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="36e7f-297">انتقل إلى **إدارة معلومات الإنتاج \> قائمة مكونات الصنف والمعادلات \> قوائم مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="36e7f-298">افتح قائمة BOM التي تتضمن إصدارا تريد تعيين دليل له.</span><span class="sxs-lookup"><span data-stu-id="36e7f-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-299">افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="36e7f-300">في علامة التبويب السريعة **إصدارات BOM**، حدد الإصدار الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-301">في شريط الادوات **إصدارات BOM**، حدد **الأدلة المقترنة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="36e7f-302">![فتح الادله المقترنة بإصدار BOM محدد](media/instruction-guides-BOMVersion.png "فتح الادله المقترنة بإصدار BOM محدد")</span><span class="sxs-lookup"><span data-stu-id="36e7f-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="36e7f-303">تفتح صفحه **الادله المقترنة** لإصدار BOM الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="36e7f-304">حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="36e7f-305">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-306">![إضافة دليل إلى إصدار BOM](media/instruction-guides-BOMVersionAddGuide.png "إضافة دليل إلى إصدار BOM")</span><span class="sxs-lookup"><span data-stu-id="36e7f-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="36e7f-307">اقران دليل بمسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-307">Associate a Guide to a route</span></span>

<span data-ttu-id="36e7f-308">يمكنك إضافه دليل إلى اي [مسار](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="36e7f-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="36e7f-309">سيناريوهات نموذجية باستخدام المسارات</span><span class="sxs-lookup"><span data-stu-id="36e7f-309">Typical scenario using routes</span></span>

<span data-ttu-id="36e7f-310">وتستخدم المسارات بشكل نموذجي لتحديد كيفيه إنتاج منتج معين تم إصداره علي أساس قائمة مكونات الصنف أو إصدار قائمة مكونات الصنف ومع مجموعه من الموارد أو مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="36e7f-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="36e7f-311">قم بتعيين دليل لأحد المسارات لتوفير إرشادات خطوه بخطوه لعمليه الإنتاج المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="36e7f-312">إضافة دليل إلى مسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-312">Add a Guide to a route</span></span>

<span data-ttu-id="36e7f-313">لإضافة دليل إلى مسار:</span><span class="sxs-lookup"><span data-stu-id="36e7f-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="36e7f-314">الانتقال إلى **التحكم في الإنتاج \>كافة المسارات**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="36e7f-315">افتح المسار الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-316">قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="36e7f-317">حدد **إضافه** من شريط الادوات **الادله المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="36e7f-318">تتم إضافة سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="36e7f-319">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-320">![إضافة دليل إلى مسار](media/instruction-guides-Route.png "إضافة دليل إلى مسار")</span><span class="sxs-lookup"><span data-stu-id="36e7f-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="36e7f-321">اقران دليل بإصدار مسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="36e7f-322">يمكنك إضافه دليل إلى اي [إصدار مسار](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="36e7f-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="36e7f-323">سيناريوهات نموذجية باستخدام إصدارات المسارات</span><span class="sxs-lookup"><span data-stu-id="36e7f-323">Typical scenario using route versions</span></span>

<span data-ttu-id="36e7f-324">وعاده ما يتم استخدام إصدارات المسارات لتحديد متغيرات عمليات الإنتاج وفقا لمسار موجود.</span><span class="sxs-lookup"><span data-stu-id="36e7f-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="36e7f-325">يمكنك تعيين أدله مختلفه لكل إصدار مسار.</span><span class="sxs-lookup"><span data-stu-id="36e7f-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="36e7f-326">إضافة دليل إلى إصدار مسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-326">Add a Guide to a route version</span></span>

<span data-ttu-id="36e7f-327">لإضافة دليل إلى إصدار مسار:</span><span class="sxs-lookup"><span data-stu-id="36e7f-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="36e7f-328">الانتقال إلى **التحكم في الإنتاج \>كافة المسارات**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="36e7f-329">افتح المسار الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-330">في علامة التبويب السريعة **الإصدارات**، حدد الإصدار الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-331">في شريط الادوات **الإصدارات**، حدد **الأدلة المقترنة**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="36e7f-332">![فتح الادله المقترنة بإصدار مسار محدد](media/instruction-guides-RouteVersion.png "فتح الادله المقترنة بإصدار مسار محدد")</span><span class="sxs-lookup"><span data-stu-id="36e7f-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="36e7f-333">تفتح صفحه **الادله المقترنة** لإصدار BOM الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="36e7f-334">حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="36e7f-335">بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="36e7f-336">![إضافة دليل إلى إصدار مسار](media/instruction-guides-RouteVersionAddGuide.png "إضافة دليل إلى إصدار مسار")</span><span class="sxs-lookup"><span data-stu-id="36e7f-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="36e7f-337">اقران دليل بعلاقة عملية مسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="36e7f-338">يمكنك إضافه دليل إلى اي [علاقة عملية مسار](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="36e7f-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="36e7f-339">سيناريو نموذجي باستخدام علاقات عملية المسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="36e7f-340">تعد علاقات العملية الطريقة الأكثر تحديدا لأضافه إرشادات لعمليه المنتج والعمليات المرتبطة بها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="36e7f-341">يمكنك تحديد الإرشادات لكل عمليه في المسار وتحديد دليل مختلف لأي نوع من سياق العلاقة المحدد للتوجيه، مثل الأصناف المحددة والتكوينات والمزيد.</span><span class="sxs-lookup"><span data-stu-id="36e7f-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="36e7f-342">كما يمكنك تحديد المراحل الموجودة في العملية التي تنطبق عليها الإرشادات (مثل الاعداد أو الإدراج في قائمة الانتظار أو العمليات أو النقل).</span><span class="sxs-lookup"><span data-stu-id="36e7f-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="36e7f-343">إذا قمت بتحديد الادله للعديد من علاقات العمليات الخاصة بأحد المسارات، فمن بين تلك الادله، يتم عرض الدليل فقط من العلاقة الأكثر تحديدا في صالة الإنتاج للوظيفة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="36e7f-344">إضافة دليل بعلاقة عملية مسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="36e7f-345">لإضافة دليل بعلاقة عملية مسار:</span><span class="sxs-lookup"><span data-stu-id="36e7f-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="36e7f-346">الانتقال إلى **التحكم في الإنتاج \>كافة المسارات**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="36e7f-347">افتح المسار الذي ترغب في تعيين دليل اليه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="36e7f-348">في جزء الاجراء، افتح علامة التبويب **المسار** ومن المجموعة **صيانة**، حدد **تفاصيل المسار**.</span><span class="sxs-lookup"><span data-stu-id="36e7f-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="36e7f-349">تفتح صفحه **تفاصيل المسار** للمسار المحدد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="36e7f-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="36e7f-350">في الشبكة العليا، حدد العملية التي ترغب في توفير إرشادات لها.</span><span class="sxs-lookup"><span data-stu-id="36e7f-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="36e7f-351">في الشبكة السفلي، حدد علاقة محدده (أو العلاقة العامة **الكل**).</span><span class="sxs-lookup"><span data-stu-id="36e7f-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="36e7f-352">![تحديد عمليه وبعد ذلك علاقة](media/instruction-guides-RouteOperationRelation.png "تحديد عمليه وبعد ذلك علاقة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="36e7f-353">فوق الشبكة السفلى، افتح علامة التبويب **الدلائل المقترنة**. ![علامة التبويب الدلائل المقترنة](media/instruction-guides-RouteOperationRelation-AddGuide.png "علامة التبويب الدلائل المقترنة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="36e7f-354">حدد **أضافه** من شريط الادوات الموجود اعلي الشبكة السفلية لأضافه سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="36e7f-355">بالنسبة للصف الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="36e7f-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="36e7f-356">في باقي الصف، حدد خانه الاختيار لكل سياق يجب ان يتوفر فيه الدليل المحدد.</span><span class="sxs-lookup"><span data-stu-id="36e7f-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="36e7f-357">يمكنك أضافه دليل واحد أو أكثر لكل مرحله من العملية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="36e7f-358">حدد الأدلة من واجهه تنفيذ صالة الإنتاج</span><span class="sxs-lookup"><span data-stu-id="36e7f-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="36e7f-359">عندما يقوم أحد العاملين بفتح قائمه الوظائف في واجهه تنفيذ صالة الإنتاج، تقوم Supply Chain Management بالبحث عن الدلائل ذات الصلة للوظائف المعروضة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="36e7f-360">استخدم زر **الأدلة** لعرض الادله ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="36e7f-361">![زر الأدلة في واجهه تنفيذ صالة الإنتاج](media/instruction-guides-Shopfloor1.png "زر الأدلة في واجهه تنفيذ صالة الإنتاج")</span><span class="sxs-lookup"><span data-stu-id="36e7f-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="36e7f-362">ثم ضع في HoloLens وقم بالوصول إلى الدليل الخاص بواسطة الاطلاع على كود QR وتنشيط الدليل المعني.</span><span class="sxs-lookup"><span data-stu-id="36e7f-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="36e7f-363">![كود QR للوصول إلى الأدلة باستخدام HoloLens](media/instruction-guides-Shopfloor2.png "كود QR للوصول إلى الأدلة باستخدام HoloLens")</span><span class="sxs-lookup"><span data-stu-id="36e7f-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="36e7f-364">حل المنطق لتحديد الأدلة</span><span class="sxs-lookup"><span data-stu-id="36e7f-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="36e7f-365">يمكنك أضافه أدله إلى بيانات الإنتاج التالية:</span><span class="sxs-lookup"><span data-stu-id="36e7f-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="36e7f-366">الموارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-366">Resources</span></span>](#resources)
- [<span data-ttu-id="36e7f-367">مجموعات الموارد</span><span class="sxs-lookup"><span data-stu-id="36e7f-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="36e7f-368">المنتجات الصادرة</span><span class="sxs-lookup"><span data-stu-id="36e7f-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="36e7f-369">التركيبات</span><span class="sxs-lookup"><span data-stu-id="36e7f-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="36e7f-370">إصدارات التركيبة</span><span class="sxs-lookup"><span data-stu-id="36e7f-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="36e7f-371">قائمة مكونات الصنف (BOMs)</span><span class="sxs-lookup"><span data-stu-id="36e7f-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="36e7f-372">إصدارات BOM</span><span class="sxs-lookup"><span data-stu-id="36e7f-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="36e7f-373">المسارات</span><span class="sxs-lookup"><span data-stu-id="36e7f-373">Routes</span></span>](#routes)
- [<span data-ttu-id="36e7f-374">إصدارات المسارات</span><span class="sxs-lookup"><span data-stu-id="36e7f-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="36e7f-375">‏‏علاقات عمليات المسار</span><span class="sxs-lookup"><span data-stu-id="36e7f-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="36e7f-376">عندما تقوم Supply Chain Management بإنشاء وظائف لصاله الإنتاج، فانها ستقوم بتجميع الدلائل ذات الصلة من تلك المصادر.</span><span class="sxs-lookup"><span data-stu-id="36e7f-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="36e7f-377">دوّن القواعد الهامه التالية.</span><span class="sxs-lookup"><span data-stu-id="36e7f-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="36e7f-378">إذا قمت بإرفاق إصدار قائمة مكونات الصنف أو إصدار التركيبة بمسار أو أمر إنتاج، سيتم عرض إيه دلائل مرفقه بهذا الإصدار، وكذلك الادله المرتبطة بقائمة مكونات الصنف الاصليه أو المعادلة الخاصة بهذا الإصدار، في الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="36e7f-379">إذا قمت بإرفاق إصدار مسار بأمر إنتاج، سيتم عرض إيه دلائل مرفقه بهذا الإصدار، وكذلك الادله المرتبطة بالمسار الاصلي لهذا الإصدار، في الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="36e7f-380">إذا قمت بتحديد العديد من علاقات مسارات العمليات التي تتضمن *جميع* دلائل العلاقة والتعيين، سيتم عرض الادله التي من أكثر علاقة محدده للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="36e7f-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="36e7f-381">![مخطط حول حل الدلائل ذات الصلة](media/instruction-guides-Resolve.png "مخطط حول حل الدلائل ذات الصلة")</span><span class="sxs-lookup"><span data-stu-id="36e7f-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]