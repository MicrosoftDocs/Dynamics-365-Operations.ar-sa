---
title: طباعة المستندات
description: في Microsoft Dynamics 365 for Finance and Operations، يمكنك طباعة المستندات باستخدام طابعة محلية أو أحد الأجهزة المتصلة بشبكة الاتصال. يقدم هذا المقال نظرة عامة على كيفية طباعة المستندات.
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc45865b55b4794202408ca19a0776440382fdd
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850061"
---
# <a name="document-printing"></a><span data-ttu-id="4b36c-104">طباعة المستندات</span><span class="sxs-lookup"><span data-stu-id="4b36c-104">Document printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b36c-105">في Microsoft Dynamics 365 for Finance and Operations، يمكنك طباعة المستندات باستخدام طابعة محلية أو أحد الأجهزة المتصلة بشبكة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="4b36c-105">In Microsoft Dynamics 365 for Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="4b36c-106">يقدم هذا المقال نظرة عامة على كيفية طباعة المستندات.</span><span class="sxs-lookup"><span data-stu-id="4b36c-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="4b36c-107">نظرة عامة على الطباعة</span><span class="sxs-lookup"><span data-stu-id="4b36c-107">Printing overview</span></span>

<span data-ttu-id="4b36c-108">يوفر Microsoft Dynamics 365 for Finance and Operations خدمات متكاملة وتطبيقات العميل التي تجعل من السهل إنشاء وتخزين وتوزيع المستندات التي تدعم نشاط الشركة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-108">Microsoft Dynamics 365 for Finance and Operations provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="4b36c-109">في Finance and Operations، يمكنك طباعة المستندات باستخدام طابعة محلية أو أحد الأجهزة المتصلة بشبكة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="4b36c-109">In Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="4b36c-110">بالإضافة إلى ذلك، يمكنك تصدير صفحات Finance and Operations والتقارير مباشرةً من العميل، كملفات PDF أو مستندات Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="4b36c-110">In addition, you can export Finance and Operations pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="4b36c-111">وأخيراً، يتيح لك حمل العمل الموزع طباعة مستندات العمل مباشرةً من جهاز محمول باستخدام موارد الشبكة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="4b36c-112">على الرغم من أنه قد تختلف متطلبات الطباعة، يجب على كل الصناعات عادةً إنشاء نسخ من مستندات الأعمال باستخدام Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b36c-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using Finance and Operations.</span></span> <span data-ttu-id="4b36c-113">تمثل طباعة المستندات على أجهزة الشبكة من التطبيقات المضيفة مجموعة فريدة من التحديات.</span><span class="sxs-lookup"><span data-stu-id="4b36c-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="4b36c-114">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="4b36c-114">Here are some examples:</span></span>

- <span data-ttu-id="4b36c-115">قد تكون برامج تشغيل الطباعة غير متوفرة على جهاز المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4b36c-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="4b36c-116">قد لا يكون الجهاز الخاص بالمستخدم متصلاً بشبكة الشركة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="4b36c-117">باستخدام مضيف مخصص واتباع خطوات بسيطة قليلة، يمكن لمسؤولي النظام تكوين عمليات النشر حتى يستطيع المستخدمون الطباعة مباشرةً من تطبيقات العمل على أجهزة الشبكة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="printing-scenarios-in-finance-and-operations-applications"></a><span data-ttu-id="4b36c-118">سيناريوهات الطباعة في تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b36c-118">Printing scenarios in Finance and Operations applications</span></span>

<span data-ttu-id="4b36c-119">يصف الجدول التالي ثلاثة سيناريوهات رئيسية للطباعة في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b36c-119">The following table describes the three primary printing scenarios in Finance and Operations applications.</span></span>

| <span data-ttu-id="4b36c-120">سيناريو</span><span class="sxs-lookup"><span data-stu-id="4b36c-120">Scenario</span></span>                        | <span data-ttu-id="4b36c-121">الهدف</span><span class="sxs-lookup"><span data-stu-id="4b36c-121">Goal</span></span>                                                      | <span data-ttu-id="4b36c-122">الحل</span><span class="sxs-lookup"><span data-stu-id="4b36c-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="4b36c-123">1. طباعة ما تشاهده</span><span class="sxs-lookup"><span data-stu-id="4b36c-123">1. Printing what you see</span></span>        | <span data-ttu-id="4b36c-124">قم بطباعة ما يظهر في المستعرض حاليًا.</span><span class="sxs-lookup"><span data-stu-id="4b36c-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="4b36c-125">يتم إنشاء إصدار "تسهل طباعته" من صفحة ويب للمستعرض.</span><span class="sxs-lookup"><span data-stu-id="4b36c-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="4b36c-126">2. الطباعة التفاعلية</span><span class="sxs-lookup"><span data-stu-id="4b36c-126">2. Interactive printing</span></span>         | <span data-ttu-id="4b36c-127">قم بطباعة مستند دقة على جهاز متصل محليًا.</span><span class="sxs-lookup"><span data-stu-id="4b36c-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="4b36c-128">يمكنك تصدير نسخة PDF من التقرير وتنزيلها إلى المستعرض.</span><span class="sxs-lookup"><span data-stu-id="4b36c-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="4b36c-129">3. الطباعة على جهاز شبكة</span><span class="sxs-lookup"><span data-stu-id="4b36c-129">3. Printing on a network device</span></span> | <span data-ttu-id="4b36c-130">أرسل مستند دقة إلى جهاز طابعة مجال.</span><span class="sxs-lookup"><span data-stu-id="4b36c-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="4b36c-131">يتم إرسال مستند دقة إلى تطبيق عميل يتم تشغيله على خادم تتم استضافته في المجال الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="4b36c-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="4b36c-132">نظراً لأن الحل يختلف، استنادًا التي السيناريو، توفر تطبيقات Finance and Operations الخدمات المضمنة والأدوات لمساعدة المستخدمين على تحقيق الأهداف الخاصة بها:</span><span class="sxs-lookup"><span data-stu-id="4b36c-132">Because the solution varies, depending on the scenario, Finance and Operations applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="4b36c-133">**السيناريو 1** مدعوم بواسطة عرض المستعرض لعميل HTML5.</span><span class="sxs-lookup"><span data-stu-id="4b36c-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="4b36c-134">**السيناريو 2** يستخدم تطبيقات العميل وخدمات Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="4b36c-134">**Scenario 2** uses client applications and Microsoft Office 365 services.</span></span>
- <span data-ttu-id="4b36c-135">**السيناريو 3** يحتاج إلى الدعم من تطبيقات العميل ومن الخدمات المستضافة في Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4b36c-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="4b36c-136">بالإضافة إلى النظام الأساسي الذي يتم نشره لاشتراك Azure، تزود تطبيقات Finance and Operations العملاء بتطبيق Azure متكامل وأصيل يساعدهم على استخدام الأجهزة المستضافة من قِبل المجال لطباعة المستندات بسهولة أكبر.</span><span class="sxs-lookup"><span data-stu-id="4b36c-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="4b36c-137">نظرة عامة على الخدمة</span><span class="sxs-lookup"><span data-stu-id="4b36c-137">Service overview</span></span>
<span data-ttu-id="4b36c-138">بينما تنتظر المستندات التي يتم إنتاجها بواسطة التطبيقات المستضافة الطباعة على أحد الأجهزة المتصلة بشبكة، يتم تخزينها في تخزين Azure blob.</span><span class="sxs-lookup"><span data-stu-id="4b36c-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="4b36c-139">يستخدم [وكيل توجيه المستند](install-document-routing-agent.md) مصادقة Azure لتأسيس قناة آمنة لخدمات Azure.</span><span class="sxs-lookup"><span data-stu-id="4b36c-139">The [Document Routing Agent](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="4b36c-140">**تسلسل عمليات التنفيذ**</span><span class="sxs-lookup"><span data-stu-id="4b36c-140">**Execution sequence**</span></span>

1. <span data-ttu-id="4b36c-141">يتم إنشاء التقرير بواسطة Microsoft SQL Server Reporting Services (SSRS) ويتم تخزينه في مخزن الكائن الثنائي كبير الحجم‬‬ من Azure.</span><span class="sxs-lookup"><span data-stu-id="4b36c-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="4b36c-142">يتم تخزين إعدادات الطابعة التي تم توصيلها مع المستند.</span><span class="sxs-lookup"><span data-stu-id="4b36c-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="4b36c-143">يستعلم "وكيل توجيه المستند" قائمة انتظار ناقل خدمة Azure للحصول على الوظائف النشطة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="4b36c-144">يتم تنزيل المستند بواسطة "وكيل توجيه المستند" وتخزينه في طابعة الشبكة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="4b36c-145">يتيح الحل المستند إلى العميل للعملاء إدارة مقياس احتياجات الطباعة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="4b36c-146">يستطيع العملاء الذين لديهم أحمال عمل طباعة ثقيلة الحجم تثبيت العديد من "وكلاء توجيه المستندات" لزيادة عدد عمليات الطباعة المتزامنة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="4b36c-147">بدلاً من ذلك، يتطلب بعض العملاء عمليات تثبيت قليلة جداً لـ "وكيل توجيه المستند" لمعالجة احتياجات الطباعة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="4b36c-148">مكونات الخدمة للطباعة على الشبكة</span><span class="sxs-lookup"><span data-stu-id="4b36c-148">Service components for network printing</span></span>

<span data-ttu-id="4b36c-149">يوضح المخطط التالي المكونات الأساسية التي تساعد في دعم عمليات الطباعة على الشبكة.</span><span class="sxs-lookup"><span data-stu-id="4b36c-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="4b36c-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="4b36c-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="4b36c-151">لاحظ أنه يمكن تسجيل طابعة واحدة مع عدة وكلاء توجيه مستندات.</span><span class="sxs-lookup"><span data-stu-id="4b36c-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="4b36c-152">لحل تفضيلات الطابعة، تستخدم الخدمة المستضافة مسار الشبكة الذي يحدد كل طابعة شبكة بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="4b36c-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="4b36c-153">وكنتيجة لذلك، حتى في حالة تسجيل طابعة بواسطة العديد من العملاء، فإنها تظهر كتحديد واحد في قائمة الطابعات المتوفرة في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b36c-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in Finance and Operations applications.</span></span>
