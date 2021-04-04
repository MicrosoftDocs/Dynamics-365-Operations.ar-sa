---
title: خيارات تنفيذ شبكة تسليم المحتويات
description: يراجع هذا الموضوع الخيارات المختلفة لتطبيق شبكة تسليم المحتوى (CDN) التي يمكن استخدامها مع بيئات Microsoft Dynamics 365 Commerce. تتضمن هذه الخيارات المثيلات الأصلية المقدمة من Commerce لـ Azure Front Door والمثيلات المملوكة للعملاء الخاصة بـ Azure Front Door
author: BrianShook
manager: AnnBe
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae0769b7e19f80244186c51454444c499c5e497f
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582793"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="6544c-104">خيارات تنفيذ شبكة تسليم المحتويات</span><span class="sxs-lookup"><span data-stu-id="6544c-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6544c-105">يراجع هذا الموضوع الخيارات المختلفة لتطبيق شبكة تسليم المحتوى (CDN) التي يمكن استخدامها مع بيئات Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6544c-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="6544c-106">تتضمن هذه الخيارات المثيلات الأصلية المقدمة من Commerce لـ Azure Front Door والمثيلات المملوكة للعملاء الخاصة بـ Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="6544c-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="6544c-107">يتوفر لدي عملاء Commerce العديد من الخيارات عندما يفكرون في أي خدمة CDN يمكن استخدامها مع بيئة Commerce الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="6544c-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="6544c-108">تم إصدار Commerce مع دعم أساسي من Azure Front Door التي تغطي متطلبات المضيف الأساسية والمخصصة للمجال.</span><span class="sxs-lookup"><span data-stu-id="6544c-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="6544c-109">بالنسبة للشركات التي ترغب في مزيد من التحكم وإمكانات أمان أكثر تحديدا، مثل جدار حماية تطبيق ويب (WAF)، قد يكون أفضل خيار هو استخدام المثيل الذي يملكه العميل من Azure Front Door أو CDN خارجية.</span><span class="sxs-lookup"><span data-stu-id="6544c-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="6544c-110">يمكن استخدام خيارات التنفيذ الثلاثة التالية لـ CDN مع بيئات Commerce:</span><span class="sxs-lookup"><span data-stu-id="6544c-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="6544c-111">مثيل Azure Front Door الذي يوفره Commerce.</span><span class="sxs-lookup"><span data-stu-id="6544c-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="6544c-112">المثيل المملوك للعميل من Azure Front Door (لمزيد من التحكم وميزات الأمان الإضافية)</span><span class="sxs-lookup"><span data-stu-id="6544c-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="6544c-113">خدمة CDN الخارجية</span><span class="sxs-lookup"><span data-stu-id="6544c-113">An external CDN service</span></span>

<span data-ttu-id="6544c-114">تقدم كافة خيارات تنفيذ CDN الثلاثة فقط محتوي HTML ديناميكي من المجالات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="6544c-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="6544c-115">تعالج Commerce تلقائيًا كافة JavaScript وصور أوراق الأنماط المتتالية (CSS) والصور والفيديو والمحتوي الثابت الآخر من خدمات CDN التي تديرها Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6544c-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="6544c-116">يحدد الخيار الذي تختاره إمكانات التشغيل وإمكانات التحكم وإمكانات الأمان الإضافية المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6544c-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="6544c-117">يعرض الشكل التوضيحي التالي نظرة عامة على بنية Commerce.</span><span class="sxs-lookup"><span data-stu-id="6544c-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![نظرة عامة حول بنية Commerce](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="6544c-119">لمزيد من المعلومات حول كيفية إعداد مثيل لـ Azure Front Door لموقع Commerce الخاصة بك، راجع [إضافة دعم CDN](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="6544c-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="6544c-120">استخدام مثيل Azure Front Door الذي يوفره Commerce</span><span class="sxs-lookup"><span data-stu-id="6544c-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="6544c-121">يسرد الجدول التالي مزايا وعيوب استخدام مثيل Azure Front Door الذي توفره Commerce لإدارة نقاط نهاية المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6544c-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="6544c-122">المزايا</span><span class="sxs-lookup"><span data-stu-id="6544c-122">Pros</span></span> | <span data-ttu-id="6544c-123">العيوب</span><span class="sxs-lookup"><span data-stu-id="6544c-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="6544c-124">يتم تضمين المثيل في تكلفة Commerce.</span><span class="sxs-lookup"><span data-stu-id="6544c-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="6544c-125">ونظرا لأن المثيل تتم إدارته بواسطة فريق Commerce، ستتكون الصيانة المطلوبة أقل، كما توجد خطوات إعداد مشتركة.</span><span class="sxs-lookup"><span data-stu-id="6544c-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="6544c-126">تتميز البنية المستضافة على Azure بأنها قابلية لتغيير الحجم وآمنة وموثوق بها.</span><span class="sxs-lookup"><span data-stu-id="6544c-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="6544c-127">تتطلب شهادة طبقة مآخذ التوصيل الآمنه (SSL) الإعداد لمرة واحدة ويتم تجديدها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6544c-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="6544c-128">يراقب فريق Commerce المثيل بحثًا عن الأخطاء والأمور غير العادية.</span><span class="sxs-lookup"><span data-stu-id="6544c-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="6544c-129">لا يتم دعم جدار حماية WAF.</span><span class="sxs-lookup"><span data-stu-id="6544c-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="6544c-130">لا توجد تخصيصات أو عمليات ضبط محددة للإعدادات.</span><span class="sxs-lookup"><span data-stu-id="6544c-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="6544c-131">يعتمد المثيل على فريق Commerce في إجراء التحديثات أو التغييرات.</span><span class="sxs-lookup"><span data-stu-id="6544c-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="6544c-132">يلزم وجود مثيل Azure Front Door منفصل لمجالات apex، ويلزم إجراء عمل إضافي لدمج مجالات apex مع Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="6544c-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="6544c-133">لا يتم توفير أي بيانات تتبع استخدام حول الاستجابات في الثانية (RPS) أو معدل الخطأ للعميل.</span><span class="sxs-lookup"><span data-stu-id="6544c-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="6544c-134">يبين الرسم التوضيحي التالي بنية مثيل Azure Front Door الذي يوفره Commerce.</span><span class="sxs-lookup"><span data-stu-id="6544c-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![مثيل Azure Front Door الذي يوفره Commerce](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="6544c-136">استخدام مثيل Azure Front Door المملوك للعميل</span><span class="sxs-lookup"><span data-stu-id="6544c-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="6544c-137">يسرد الجدول التالي مزايا وعيوب استخدام مثيل Azure Front Door المملوك للعميل لإدارة نقاط نهاية المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6544c-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="6544c-138">المزايا</span><span class="sxs-lookup"><span data-stu-id="6544c-138">Pros</span></span> | <span data-ttu-id="6544c-139">العيوب</span><span class="sxs-lookup"><span data-stu-id="6544c-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="6544c-140">الإعداد أمن ويسهل إدارته.</span><span class="sxs-lookup"><span data-stu-id="6544c-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="6544c-141">تتميز البنية المستضافة على Azure بأنها قابلية لتغيير الحجم وآمنة وموثوق بها.</span><span class="sxs-lookup"><span data-stu-id="6544c-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="6544c-142">يسمح المثيل بتكامل جدار حماية WAF وعناصر تحكم قاعدة الدرجات المتعددة للأمان الأفضل الذي يتم ضبطه خصيصًا للموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="6544c-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="6544c-143">يسمح المثيل بالتحكم الدقيق بشهادات SSL (المملوكة للعميل والمدارة بواسطة Azure Front Door) وربط المجال.</span><span class="sxs-lookup"><span data-stu-id="6544c-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="6544c-144">يقدم المثيل حل مجال apex إذا كان مقترنًا مباشرة بخدمة Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="6544c-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="6544c-145">يتم توفير بيانات تتبع الاستخدام والتنبيه.</span><span class="sxs-lookup"><span data-stu-id="6544c-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="6544c-146">تتطلب شهادة SSL الإعداد لمرة واحدة ويتم تجديدها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6544c-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="6544c-147">تتم إدارة المثيل ذاتيًا.</span><span class="sxs-lookup"><span data-stu-id="6544c-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="6544c-148">مطلوب زيادة المعرفة الأولية.</span><span class="sxs-lookup"><span data-stu-id="6544c-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="6544c-149">يبين الرسم التوضيحي التالي البنية الأساسية لـ Commerce التي تشمل مثيل Azure Front Door المملوك للعميل.</span><span class="sxs-lookup"><span data-stu-id="6544c-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![البنية الأساسية لـ Commerce التي تشمل مثيل Azure Front Door المملوك للعميل.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="6544c-151">استخدام خدمة CDN الخارجية</span><span class="sxs-lookup"><span data-stu-id="6544c-151">Use an external CDN service</span></span>

<span data-ttu-id="6544c-152">يسرد الجدول التالي المزايا والعيوب الخاصة باستخدام خدمة CDN الخارجية لإدارة نقاط نهاية المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6544c-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="6544c-153">المزايا</span><span class="sxs-lookup"><span data-stu-id="6544c-153">Pros</span></span> | <span data-ttu-id="6544c-154">العيوب</span><span class="sxs-lookup"><span data-stu-id="6544c-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="6544c-155">يكون هذا الخيار مفيدًا في حالة استضافه المجال الموجود بالفعل على خدمة CDN خارجية.</span><span class="sxs-lookup"><span data-stu-id="6544c-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="6544c-156">قد يكون لخدمات CDN المنافسة (على سبيل المثال، Akamai) إمكانات WAF أفضل.</span><span class="sxs-lookup"><span data-stu-id="6544c-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="6544c-157">يلزم وجود عقد منفصل وتكلفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="6544c-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="6544c-158">قد تتكبد خدمة SSL تكاليف إضافية.</span><span class="sxs-lookup"><span data-stu-id="6544c-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="6544c-159">نظرًا لأن الخدمة منفصلة عن بنيه سحابة Azure، يجب إدارة البنية الأساسية الإضافية.</span><span class="sxs-lookup"><span data-stu-id="6544c-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="6544c-160">قد تتطلب الخدمة استثمارات طويلة الوقت في نقطة النهاية وإعداد الأمان.</span><span class="sxs-lookup"><span data-stu-id="6544c-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="6544c-161">الخدمة مدارة ذاتيًا.</span><span class="sxs-lookup"><span data-stu-id="6544c-161">The service is self-managed.</span></span></li><li><span data-ttu-id="6544c-162">الخدمة مراقبة ذاتيًا.</span><span class="sxs-lookup"><span data-stu-id="6544c-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="6544c-163">يبين الرسم التوضيحي التالي البنية الأساسية لـ Commerce التي تشتمل على خدمة CDN خارجية.</span><span class="sxs-lookup"><span data-stu-id="6544c-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![البنية الأساسية لـ Commerce التي تشتمل على خدمه CDN خارجية](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="6544c-165">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6544c-165">Additional resources</span></span>

[<span data-ttu-id="6544c-166">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="6544c-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
