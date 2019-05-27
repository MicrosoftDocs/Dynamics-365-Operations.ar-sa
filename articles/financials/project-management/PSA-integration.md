---
title: Project Service Automation
description: يوفر هذا الموضوع معلومات حول حل تكامل Project Service Automation إلى Finance and Operations. يستخدم حل التكامل هذا ميزة "تكامل البيانات" لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Project Service Automation عبر Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557296"
---
# <a name="project-service-automation"></a><span data-ttu-id="9a73a-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9a73a-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9a73a-105">يستخدم حل تكامل Project Service Automation مع Finance and Operations ميزة "تكامل البيانات" لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Project Service Automation عبر Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a73a-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="9a73a-106">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق المشاريع وعقود المشاريع وبنود عقود المشاريع والمراحل الرئيسية لبنود عقود المشاريع ومهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="9a73a-107">إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="9a73a-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="9a73a-108">إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.</span><span class="sxs-lookup"><span data-stu-id="9a73a-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="9a73a-109">إذا كنت تستخدم Finance and Operations 7.3.0، فيجب تثبيت KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="9a73a-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="9a73a-110">سوف يسمح لك هذا بإجراء تكامل للمشاريع ثابتة السعر.</span><span class="sxs-lookup"><span data-stu-id="9a73a-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="9a73a-111">إذا كنت تستخدم Finance and Operations 7.3.0، وتعمل على إحضار حركات الرسوم من Project Service Automation، فيجب تثبيت KB 4345320 لتضمين تلك الرسوم في فاتورة المشروع.</span><span class="sxs-lookup"><span data-stu-id="9a73a-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="9a73a-112">إذا كنت تستخدم الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations، ستتمكن من استخدام ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="9a73a-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="9a73a-113">إذا كنت تستخدم الإصدار 8.0.1 من Microsoft Dynamics 365 for Finance and Operations أو إصدار لاحق، فستتمكن من مزامنة القيم الفعلية.</span><span class="sxs-lookup"><span data-stu-id="9a73a-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="9a73a-114">قبل أن تتمكن من دمج Project Service Automation مع Finance and Operations، يجب عليك تكوين محددات تكامل Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9a73a-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="9a73a-115">لمزيد من المعلومات، راجع [محددات تكامل Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9a73a-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="9a73a-116">يتيح حل التكامل هذا مزامنة مباشرة في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="9a73a-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="9a73a-117">الحفاظ على عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-118">إنشاء مشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-119">الحفاظ بنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-120">الحفاظ على المراحل الرئيسية لبنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-121">الحفاظ على مهام المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-122">الحفاظ على فئات حركات المصروفات في Finance and Operations، ومزامنتهم مباشرةً من Finance and Operations إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9a73a-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="9a73a-123">إنشاء تقديرات عدد ساعات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-124">إنشاء تقديرات مصروفات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9a73a-125">إنشاء قيم فعلية للوقت والمصروفات والرسوم في Project Service Automation، وإنشاء حركات المشروع في دفتر يومية تكامل Project Service Automation لتمكين ترحيلها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="9a73a-126">مزامنة البيانات</span><span class="sxs-lookup"><span data-stu-id="9a73a-126">Data synchronization</span></span>

<span data-ttu-id="9a73a-127">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات كجزء من التكامل بين Project Service Automation و Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a73a-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="9a73a-128">لا تتوافر جميع القوالب في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="9a73a-128">Not all templates are currently available.</span></span> <span data-ttu-id="9a73a-129">سوف يتم إصدار القوالب بمجرد اكتمالها.</span><span class="sxs-lookup"><span data-stu-id="9a73a-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="9a73a-130">[![تكامل Project Service Automation مع Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="9a73a-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="9a73a-131">متطلبات النظام لـ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a73a-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="9a73a-132">لاستخدام حل تكامل Project Service Automation مع Finance and Operations، يجب عليك تثبيت Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 مع platform update 12 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="9a73a-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="9a73a-133">متطلبات النظام لـ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9a73a-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="9a73a-134">لاستخدام حل تكامل Project Service Automation إلى Finance and Operations، يجب عليك تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="9a73a-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="9a73a-135">الإصدار 9.0.0.0 من Microsoft Dynamics 365 for Project Service Automation أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="9a73a-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="9a73a-136">حل العميل المتوقع إلى النقدية لتطبيق Microsoft Dynamics 365 for Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="9a73a-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="9a73a-137">حل Project Service Automation إلى Finance and Operations للإصدار 1.0.0.0 أو إصدار لاحق من Microsoft Dynamics 365 for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9a73a-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="9a73a-138">تثبيت حل تكامل Project Service Automation إلى Finance and Operations في مثيل Project Service Automation الخاص بك</span><span class="sxs-lookup"><span data-stu-id="9a73a-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="9a73a-139">قم بتنزيل حل تكامل Project Service Automation إلى Finance and Operations من [مركز التنزيل لـ Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=57016)، واتبع الإرشادات المضمنة مع الحل.</span><span class="sxs-lookup"><span data-stu-id="9a73a-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
