---
title: "قابلية التوسعة‬ في Attract"
description: "يصف هذا الموضوع كيف يمكنك توسيع تطبيق Microsoft Dynamics 365 for Talent - Attract باستخدام Microsoft Power platform."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.contentlocale: ar-sa
ms.lasthandoff: 11/12/2018

---

# <a name="extensibility-in-attract"></a><span data-ttu-id="dd1cd-103">قابلية التوسعة‬ في Attract</span><span class="sxs-lookup"><span data-stu-id="dd1cd-103">Extensibility in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dd1cd-104">تم بناء Microsoft Dynamics 365 for Talent استنادًا إلى النظام الأساسي Common Data Service (CDS) للتطبيقات، ويمكن توسعته بطرق مختلفة باستخدام Microsoft Power Platform والقدرات التي تقدمها Common Data Service للتطبيقات.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-104">Microsoft Dynamics 365 for Talent is built on top of the Common Data Service (CDS) for Apps platform, and can be extended in various ways by using the Microsoft Power Platform and the capabilities that Common Data Service for Apps offers.</span></span> <span data-ttu-id="dd1cd-105">لذلك، يمكنك تكوين وتخصيص النظام باستخدام Microsoft PowerApps وMicrosoft Flow.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-105">Therefore, you can configure and personalize the system by using Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="dd1cd-106">ويمكنك أيضًا الحصول على تحليلات إضافية حول الأشخاص باستخدام Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-106">You can also get additional analytics about people by using Microsoft Power BI.</span></span> <span data-ttu-id="dd1cd-107">علاوة على ذلك، ثمة أنشطة مخصصة جديدة، مثل أنشطة PowerApps ومحتوى الويب (iframe)، تجعل عملية التوظيف قابلة للتكيف أكثر من أي وقت مضى.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-107">Furthermore, new custom activities, such as the PowerApps and Web content (iframe) activities, make the hiring process more adaptable than ever.</span></span> <span data-ttu-id="dd1cd-108">باستخدام هذه الأنشطة، يمكن تخصيص عملية التوظيف بحيث تتلاءم مع احتياجات وعمليات الأعمال لديك، ويمكنك أن تتأكد من حصول كل من فريق التوظيف والمرشحين على تجربة سلسة ومخصصة.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-108">By using these activities, you can tailor the hiring process to your business needs and processes, and can make sure that both the hiring team and candidates have a seamless, customized experience.</span></span>

## <a name="take-advantage-of-the-microsoft-power-platform"></a><span data-ttu-id="dd1cd-109">استفد من Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="dd1cd-109">Take advantage of the Microsoft Power platform</span></span> 

<span data-ttu-id="dd1cd-110">نظرًا وجود كافة البيانات من Attract في Common Data Service للتطبيقات، يمكنك استخدام الأدوات من Microsoft Power Platform لدمج احتياجات العمل الفريدة لديك في Attract.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-110">Because all the data from Attract resides in Common Data Service for Apps, you can use tools from the Microsoft Power platform to incorporate your unique business needs into Attract.</span></span>

### <a name="powerapps"></a><span data-ttu-id="dd1cd-111">PowerApps</span><span class="sxs-lookup"><span data-stu-id="dd1cd-111">PowerApps</span></span>

<span data-ttu-id="dd1cd-112">يمكنك استخدام PowerApps لإنشاء تطبيقات تتصل ببياناتك في Attract بسهولة، وتستخدم تعبيرات مثل التعبيرات في Microsoft Excel لإضافة المنطق.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-112">You can use PowerApps to easily build apps that connect to your Attract data, and that use expressions like the expressions in Microsoft Excel to add logic.</span></span> <span data-ttu-id="dd1cd-113">يمكنك تشغيل التطبيقات التي تقوم بإنشائها باستخدام PowerApps على الويب وعلى أجهزة Apple iOS وGoogle Android.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-113">Apps that you build by using PowerApps can run on the web, and on Apple iOS and Google Android devices.</span></span>

<span data-ttu-id="dd1cd-114">على سبيل المثال، يمكنك أن تجعل معارض الوظائف التي تقام في الجامعات أكثر سهولة بالنسبة إلى مسؤولي التعيين عن طريق إنشاء تطبيق منخفض المرتبة يسمح لهم بفحص السير الذاتية وإعداد المرشحين لمنصب ما في Attract.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-114">For example, you can make university career fairs easier for recruiters by building a lightweight app that lets them scan resumes and feed candidates to a position in Attract.</span></span> <span data-ttu-id="dd1cd-115">أو يمكنك إنشاء تطبيق يساعد في تلبية متطلبات التوافق الخاصة بمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-115">Alternatively, you can build an app that helps meet your organization's compliance needs.</span></span> <span data-ttu-id="dd1cd-116">للحصول على مزيد من المعلومات حول PowerApps وكيفية استخدامه لإنشاء التطبيقات، راجع [دمج البيانات في Common Data Service للتطبيقات](https://docs.microsoft.com/en-us/powerapps).</span><span class="sxs-lookup"><span data-stu-id="dd1cd-116">For more information about PowerApps and how to use it to build apps, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).</span></span>

### <a name="microsoft-flow"></a><span data-ttu-id="dd1cd-117">Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="dd1cd-117">Microsoft Flow</span></span> 

<span data-ttu-id="dd1cd-118">يمكنك استخدام Microsoft Flow لإنشاء مهام سير عمل تلقائية تستخدم بيانات Attract.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-118">You can use Microsoft Flow to create automated workflows that run on top of Attract data.</span></span> <span data-ttu-id="dd1cd-119">يمكنك الاتصال بسهولة بمئات من الخدمات والتطبيقات الشائعة من دون الحاجة إلى كتابة تعليمات برمجية.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-119">You can easily connect to hundreds of popular apps and services without having to write code.</span></span> <span data-ttu-id="dd1cd-120">من خلال إنشاء مهام سير عمل تتفاعل مع كيانات وظائف Attract والمرشحين واستمارات التقديم في Common Data Service للتطبيقات، يمكنك أتمتة إجراءات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-120">By building flows that interact with the Attract Job, Candidate, and Application entities in Common Data Service for Apps, you can automate various actions.</span></span> <span data-ttu-id="dd1cd-121">على سبيل المثال، عندما يقبل أحد المرشحين العرض المقدم له، يمكن إرسال إعلام إلى فريق الإعداد أو يمكن الإعلان عن الخبر على Twitter.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-121">For example, when a candidate accepts an offer, a notification can be sent to an onboarding team, or the news can be announced on Twitter.</span></span> <span data-ttu-id="dd1cd-122">لمزيد من المعلومات حول مهام سير العمل، راجع [وثائق Microsoft Flow](https://docs.microsoft.com/en-us/flow/).</span><span class="sxs-lookup"><span data-stu-id="dd1cd-122">For more information about flows, see the [Microsoft Flow documentation](https://docs.microsoft.com/en-us/flow/).</span></span>

### <a name="power-bi"></a><span data-ttu-id="dd1cd-123">Power BI</span><span class="sxs-lookup"><span data-stu-id="dd1cd-123">Power BI</span></span>

<span data-ttu-id="dd1cd-124">يسمح لك Power BI بإنشاء وعرض التقارير المخصصة ولوحات المعلومات التي توفر لك معلومات أكثر عمقًا حول بيانات Attract.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-124">Power BI lets you build and view custom reports and dashboards that give you deeper insight into your Attract data.</span></span> <span data-ttu-id="dd1cd-125">للحصول على مزيد من المعلومات حول Power BI وكيفية إنشاء تقارير ولوحات المعلومات تفاعلية، راجع [وثائق Power BI](https://docs.microsoft.com/en-us/power-bi/).</span><span class="sxs-lookup"><span data-stu-id="dd1cd-125">For more information about Power BI and how to build interactive reports and dashboards, see the [Power BI documentation](https://docs.microsoft.com/en-us/power-bi/).</span></span>

### <a name="custom-activities"></a><span data-ttu-id="dd1cd-126">الأنشطة المخصصة</span><span class="sxs-lookup"><span data-stu-id="dd1cd-126">Custom activities</span></span> 

<span data-ttu-id="dd1cd-127">يمكنك إضافة أنشطة مخصصة، مثل أنشطة تطبيقات PowerApps ومحتوى الويب (iframe)، على مستوى قالب عملية الوظيفة أو أثناء إنشاء وظيفة جديدة.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-127">You can add custom activities, such as the PowerApps apps and Web content (iframe) activities, at the level of the job process template or while you're creating a new job.</span></span> <span data-ttu-id="dd1cd-128">تسمح لك هذه الأنشطة بتخصيص عملية التوظيف وإحضار منطق العمل الفريد لمؤسستك إلى Attract.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-128">These activities let you customize the hiring process and bring business logic that is unique to your organization into Attract.</span></span>

#### <a name="powerapps-activity"></a><span data-ttu-id="dd1cd-129">نشاط PowerApps</span><span class="sxs-lookup"><span data-stu-id="dd1cd-129">PowerApps activity</span></span> 

<span data-ttu-id="dd1cd-130">يسمح نشاط PowerApps لمنشئ الوظيفة أو قالب عملية الوظيفة بتضمين تطبيقات PowerApps في سير عمل التوظيف.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-130">The PowerApps activity lets the creator of a job or job process template embed a PowerApps app in the hiring flow.</span></span> <span data-ttu-id="dd1cd-131">بعد إنشاء ونشر التطبيق، يمكنك إدخال معرّف التطبيق ف تكوينات النشاط.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-131">After you create and publish the app, you can enter its app ID in the activity configurations.</span></span> <span data-ttu-id="dd1cd-132">باستخدام تطبيقات PowerApps، يمكنك قراءة وكتابة البيانات إلى Common Data Service للتطبيقات.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-132">By using a PowerApps app, you can read and write data into Common Data Service for Apps.</span></span> <span data-ttu-id="dd1cd-133">حتى أنه يمكنك ربط التطبيق بسير عمل.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-133">You can even link the app to a flow.</span></span> <span data-ttu-id="dd1cd-134">على سبيل المثال، لديك تطبيق يستخدمه مسؤولو التعيين لملء نموذج أثناء إجرائهم مقابلات عبر الهاتف.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-134">For example, you have an app that recruiters use to fill in a form while they conduct phone interviews.</span></span> <span data-ttu-id="dd1cd-135">في هذه الحالة، يمكنك ربط التطبيق بسير عمل يقيّم ما إذا كان من الممكن نقل مقدم الطلب إلى مرحلة متقدمة في عملية تقديم طلب الحصول على الوظيفة‬.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-135">In this case, you can link the app to a flow that evaluates whether an applicant can be advanced further in the job application process.</span></span> <span data-ttu-id="dd1cd-136">يمكن عرض هذا النوع من النشاط فقط بواسطة أعضاء فريق التوظيف.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-136">This type of activity can be viewed only by members of the hiring team.</span></span> <span data-ttu-id="dd1cd-137">للحصول على مزيد من المعلومات حول كيفية تكوين نشاط PowerApps، راجع [الأنشطة في Attract‎](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="dd1cd-137">For more information about how to configure the PowerApps activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="dd1cd-138">يتوفر نشاط PowerApps فقط مع المكون الإضافي Comprehensive hiring.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-138">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

#### <a name="web-content-iframe-activity"></a><span data-ttu-id="dd1cd-139">نشاط محتوى الويب (iframe)</span><span class="sxs-lookup"><span data-stu-id="dd1cd-139">Web content (iframe) activity</span></span>

<span data-ttu-id="dd1cd-140">يسمح لك نشاط محتوى الويب (iframe) بتضمين حل ويب مخصص أنشأته في عملية التوظيف أو مدخل المرشح.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-140">The Web content (iframe) activity lets you embed a custom web solution that you've built in the hiring process or the Candidate portal.</span></span> <span data-ttu-id="dd1cd-141">يمكنك قراءة وكتابة البيانات مباشرة من Common Data Service للتطبيقات.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-141">You can read and write data directly from Common Data Service for Apps.</span></span> <span data-ttu-id="dd1cd-142">ويمكنك أيضًا تخصيص الحل بحيث يقوم بتشغيل مهام سير العمل أو الاستفادة من وظائف Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-142">You can also customize the solution so that it triggers flows or takes advantage of Microsoft Azure functions.</span></span> <span data-ttu-id="dd1cd-143">للحصول على مزيد من المعلومات حول كيفية تكوين نشاط محتوى الويب، راجع [الأنشطة في Attract‎](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="dd1cd-143">For more information about how to configure the Web content activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="dd1cd-144">يتوفر نشاط محتوى الويب فقط مع المكون الإضافي Comprehensive hiring.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-144">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>

