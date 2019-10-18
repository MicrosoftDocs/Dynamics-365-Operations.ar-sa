---
title: نظرة عامة حول Project Service Automation
description: يوفر هذا الموضوع معلومات حل تكامل Dynamics 365 Project Service Automation إلى Dynamics 365 Finance .
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250543"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="71975-103">نظرة عامة حول Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="71975-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="71975-104">يستخدم حل تكامل Project Service Automation مع Finance ميزة "تكامل البيانات" لمزامنة البيانات عبر مثيلات Dynamics 365 Finance وDynamics 365 Project Service Automation عبر Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="71975-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="71975-105">تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق المشاريع وعقود المشاريع وبنود عقود المشاريع والمراحل الرئيسية لبنود عقود المشاريع ومهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="71975-106">إذا كنت تستخدم الإصدار 7.3.0، فيجب تثبيت قاعدة المعارف 4074835.</span><span class="sxs-lookup"><span data-stu-id="71975-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="71975-107">سوف يسمح لك هذا بإجراء تكامل للمشاريع ثابتة السعر.</span><span class="sxs-lookup"><span data-stu-id="71975-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="71975-108">إذا كنت تستخدم الإصدار 7.3.0، وتعمل على إحضار حركات الرسوم من Project Service Automation، فيجب تثبيت KB 4345320 لتضمين تلك الرسوم في فاتورة المشروع.</span><span class="sxs-lookup"><span data-stu-id="71975-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="71975-109">إذا كنت تستخدم الإصدار 8.0، ستتمكن من استخدام ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="71975-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="71975-110">إذا كنت تستخدم الإصدار 8.0.1 أو إصدار لاحق، فستتمكن من مزامنة القيم الفعلية.</span><span class="sxs-lookup"><span data-stu-id="71975-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="71975-111">قبل أن تتمكن من دمج Project Service Automation مع Finance، يجب عليك تكوين محددات تكامل Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="71975-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="71975-112">لمزيد من المعلومات، راجع [محددات تكامل Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="71975-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="71975-113">يتيح حل التكامل هذا مزامنة مباشرة في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="71975-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="71975-114">الحفاظ على عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-115">إنشاء مشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-116">الحفاظ على بنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-117">الحفاظ على النقاط الرئيسية ببنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-118">الحفاظ على مهام المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-119">الحفاظ على فئات حركات المصروفات في Finance، ومزامنتهم مباشرةً من Finance إلى Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="71975-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="71975-120">إنشاء تقديرات عدد ساعات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-121">إنشاء تقديرات المصروفات للمشروع‬ات في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="71975-122">إنشاء قيم فعلية للوقت والمصروفات والرسوم في Project Service Automation، وإنشاء حركات المشروع في دفتر يومية تكامل Project Service Automation لتمكين ترحيلها في Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="71975-123">مزامنة البيانات</span><span class="sxs-lookup"><span data-stu-id="71975-123">Data synchronization</span></span>

<span data-ttu-id="71975-124">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات كجزء من التكامل بين Project Service Automation و Finance.</span><span class="sxs-lookup"><span data-stu-id="71975-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="71975-125">لا تتوافر جميع القوالب في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="71975-125">Not all templates are currently available.</span></span> <span data-ttu-id="71975-126">سوف يتم إصدار القوالب بمجرد اكتمالها.</span><span class="sxs-lookup"><span data-stu-id="71975-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="71975-127">[![تكامل Project Service Automation مع Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="71975-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="71975-128">متطلبات النظام لـ Finance</span><span class="sxs-lookup"><span data-stu-id="71975-128">System requirements for Finance</span></span>

<span data-ttu-id="71975-129">لاستخدام حل تكامل Project Service Automation مع Finance، يجب عليك تثبيت , Enterprise edition 7.3 مع platform update 12 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="71975-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="71975-130">متطلبات النظام لـ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="71975-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="71975-131">لاستخدام حل تكامل Project Service Automation إلى Finance، يجب عليك تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="71975-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="71975-132">الإصدار 9.0.0.0 من Dynamics 365 Project Service Automation أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="71975-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="71975-133">حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="71975-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="71975-134">حل Project Service Automation إلى Finance للإصدار 1.0.0.0 أو إصدار لاحق من Dynamics 365 Project Service Automation .</span><span class="sxs-lookup"><span data-stu-id="71975-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="71975-135">تثبيت حل تكامل Project Service Automation إلى Finance في مثيل Project Service Automation الخاص بك</span><span class="sxs-lookup"><span data-stu-id="71975-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="71975-136">قم بتنزيل حل تكامل Project Service Automation إلى Finance من [مركز التنزيل لـ Microsoft](https://www.microsoft.com/download/details.aspx?id=57016)، واتبع الإرشادات المضمنة مع الحل.</span><span class="sxs-lookup"><span data-stu-id="71975-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
