---
title: Project Service Automation
description: "يستخدم هذا الحل ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations و Microsoft Dynamics 365 for Project Service Automation عبر Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="32261-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="32261-103">Project Service Automation</span></span>

<span data-ttu-id="32261-104">يستخدم حل تكامل Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations و Microsoft Dynamics 365 for Project Service Automation عبر Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="32261-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="32261-105">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق المشاريع وعقود المشاريع وبنود عقود المشاريع والمراحل الرئيسية لبنود عقود المشاريع ومهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات من  Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="32261-106">إذا كنت تستخدم Dynamics 365 for Finance and Operations، إصدار Enterprise edition 7.3.0، فيجب عليك تثبيت قاعدة المعارف 4074835.</span><span class="sxs-lookup"><span data-stu-id="32261-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="32261-107">سوف يسمح لك هذا بتكامل المشاريع ثابتة السعر.</span><span class="sxs-lookup"><span data-stu-id="32261-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="32261-108">إذا كنت تستخدم  Dynamics 365 for Finance and Operations إصدار 8.0، فسوف تكون قادرًا على استخدام ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.</span><span class="sxs-lookup"><span data-stu-id="32261-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="32261-109">إذا كنت تستخدم Dynamics 365 for Finance and Operations إصدار 8.0.1، فسوف تكون قادرًا على مزامنة القيم الفعلية.</span><span class="sxs-lookup"><span data-stu-id="32261-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="32261-110">إذا كنت تستخدم Dynamics 365 for Finance and Operations، إصدار Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، فسوف تكون قادرًا على استخدام القوالب لتكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="32261-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="32261-111">إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.</span><span class="sxs-lookup"><span data-stu-id="32261-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="32261-112">قبل أن تتمكن من دمج Project Service Automation مع Finance and Operations، يجب عليك تكوين محددات تكامل Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="32261-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="32261-113">للحصول على المزيد من المعلومات، راجع محددات تكامل Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="32261-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="32261-114">يتيح حل التكامل هذا مزامنة مباشرة في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="32261-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="32261-115">الحفاظ على عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="32261-116">إنشاء مشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="32261-117">الحفاظ بنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="32261-118">الحفاظ على المراحل الرئيسية لبنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="32261-119">الحفاظ على مهام المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="32261-120">الحفاظ على فئات حركات المصروفات في Finance and Operations، ومزامنتهم مباشرةً من Finance and Operations إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="32261-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="32261-121">إنشاء تقديرات عدد ساعات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="32261-122">إنشاء تقديرات مصروفات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="32261-123">مزامنة البيانات</span><span class="sxs-lookup"><span data-stu-id="32261-123">Data synchronization</span></span>
<span data-ttu-id="32261-124">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات كجزء من التكامل بين Project Service Automation و Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32261-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="32261-125">لا تتوافر جميع القوالب في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="32261-125">Not all templates are currently available.</span></span> <span data-ttu-id="32261-126">سوف يتم إصدار القوالب بمجرد اكتمالها.</span><span class="sxs-lookup"><span data-stu-id="32261-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="32261-127">[![تكامل Project Service Automation مع Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="32261-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="32261-128">متطلبات النظام لـ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="32261-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="32261-129">لاستخدام Project Service Automation لحل تكامل Finance and Operations، يجب عليك تثبيت Microsoft Dynamics 365 for Finance and Operations إصدار Enterprise edition 7.3 مع تحديث النظام الأساسي 12 أو إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="32261-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="32261-130">متطلبات النظام لـ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="32261-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="32261-131">لاستخدام حل تكامل Project Service Automation إلى Finance and Operations، يجب عليك تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="32261-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="32261-132">Microsoft Dynamics 365 for Project Service Automation إصدار 9.0.0.0 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="32261-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="32261-133">حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="32261-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="32261-134">حل Project Service Automation to Operations لـ Dynamics 365 for Project Service Automation إصدار 1.0.0.0 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="32261-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="32261-135">تثبيت حل تكامل Project Service Automation إلى Finance and Operations في مثيل Project Service Automation الخاص بك</span><span class="sxs-lookup"><span data-stu-id="32261-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



