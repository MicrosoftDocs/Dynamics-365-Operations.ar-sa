---
title: تكامل البيانات في وقت قريب من الحقيقي‬ بين Finance and Operations وCommon Data Service
description: يصف هذا الموضوع نظرة عامة على التكامل بين Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b7d9e6be6fb2fef85bcf1182f89b8e370abea3d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184475"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="3a447-103">تكامل البيانات في وقت قريب من الحقيقي مع Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3a447-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="3a447-104">في العالم الرقمي الحالي، تستخدم الأنظمة البيئية للأعمال تطبيقات Microsoft Dynamics 365 كوحدة متكاملة.</span><span class="sxs-lookup"><span data-stu-id="3a447-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="3a447-105">نظرًا لتدفق البيانات من الأشخاص والعملاء والعمليات وأجهزة إنترنت الأشياء (IoT) إلى مصدر واحد، فهناك فرصة لحلقات الملاحظات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="3a447-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="3a447-106">لتحقيق هذه التجربة، يعتبر التكامل بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى أمرًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="3a447-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="3a447-107">تم بناء بعض التطبيقات بالاستناد إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3a447-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="3a447-108">يسمح التكامل بين بيانات تطبيقات Finance and Operations وCommon Data Service لتطبيقات أخرى بالتواصل بطريقة متماسكة وسلسة مع Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a447-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="3a447-109">توفر تطبيقات Finance and Operations وCommon Data Service إمكانية مزامنة البيانات في وقت قريب من الحقيقي بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى من خلال إطار عمل الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="3a447-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="3a447-110">تعتبر هذه التغطية واسعة النطاق وتشمل 28 مجالاً من التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3a447-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="3a447-111">الهدف هو توفير تجربة مستخدم "One Dynamics 365" من خلال تدفقات البيانات السلسة التي تربط العمليات التجارية عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="3a447-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![رسم تخطيطي للنظرة عامة على البنية الهندسية](media/dual-write-overview.jpg)

<span data-ttu-id="3a447-113">تتوفر مقترحات القيمة التالية للعملاء:</span><span class="sxs-lookup"><span data-stu-id="3a447-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="3a447-114">التدرج الهرمي للمؤسسات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3a447-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="3a447-115">مفهوم الشركة في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3a447-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="3a447-116">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="3a447-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="3a447-117">أصل المورّد المتكامل</span><span class="sxs-lookup"><span data-stu-id="3a447-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="3a447-118">أصل المنتج الموحد</span><span class="sxs-lookup"><span data-stu-id="3a447-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="3a447-119">متطلبات النظام</span><span class="sxs-lookup"><span data-stu-id="3a447-119">System requirements</span></span>

<span data-ttu-id="3a447-120">تحتاج تدفقات البيانات المتزامنة وثنائية الاتجاه وفي الوقت الحقيقي تقريبًا الإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="3a447-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="3a447-121">Microsoft Dynamics 365 for Finance and Operations الإصدار 10.0.4 (يوليو 2019) مع platform update 28 أو أعلى</span><span class="sxs-lookup"><span data-stu-id="3a447-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="3a447-122">Microsoft Dynamics 365 for Customer Engagement، إصدار Platform 9.1 (4.2) أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="3a447-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="3a447-123">تعليمات الإعداد</span><span class="sxs-lookup"><span data-stu-id="3a447-123">Setup instructions</span></span>

<span data-ttu-id="3a447-124">اتبع هذه الخطوات لإعداد التكامل بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="3a447-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="3a447-125">فيما يتعلق بإعداد نظام الكتابة المزدوجة، راجع [الدليل المفصل خطوة بخطوة](https://aka.ms/dualwrite-docs) حول الإعلان عن معاينة الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="3a447-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="3a447-126">يمكنك تنزيل الحل وتثبيته من مجموعة [تكامل Finance and Operations وCommon Data Service وCustomer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer.</span><span class="sxs-lookup"><span data-stu-id="3a447-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="3a447-127">تحتوي الحزمة على خمسة حلول:</span><span class="sxs-lookup"><span data-stu-id="3a447-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="3a447-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="3a447-128">Dynamics365Company</span></span>
    + <span data-ttu-id="3a447-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="3a447-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="3a447-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="3a447-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="3a447-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="3a447-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="3a447-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="3a447-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="3a447-133">اتبع ترتيب التنفيذ من أجل [مزامنة البيانات المرجعية الأولية](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="3a447-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="3a447-134">إذا واجهت مشكلات تتعلق بمزامنة الكتابة المزدوجة، فراجع [دليل استكشاف أخطاء تكامل البيانات وإصلاحها](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="3a447-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a447-135">لا يمكنك تشغيل الكتابة المزدوجة‏‎ جنبًا إلى جنب مع حل [العميل المتوقع إلى النقدية‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="3a447-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="3a447-136">إذا كنت تقوم بتشغيل حل "العميل المتوقع إلى النقدية‬"، فيجب إلغاء تثبيته.</span><span class="sxs-lookup"><span data-stu-id="3a447-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="3a447-137">يجب أيضًا تعطيل قوالب الكتابة المزدوجة للعميل والمورد التي تشكل جزءًا من الحل "العميل المتوقع إلى النقدية‬".</span><span class="sxs-lookup"><span data-stu-id="3a447-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
