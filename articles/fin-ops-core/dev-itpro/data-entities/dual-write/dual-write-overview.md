---
title: تكامل البيانات في وقت قريب من الحقيقي مع Common Data Service
description: يوفر هذا الموضوع نظرة عامة على التكامل بين Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019622"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="f8738-103">تكامل البيانات في وقت قريب من الحقيقي مع Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f8738-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f8738-104">في العالم الرقمي الحالي، تستخدم الأنظمة البيئية للأعمال تطبيقات Microsoft Dynamics 365 كوحدة متكاملة.</span><span class="sxs-lookup"><span data-stu-id="f8738-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="f8738-105">نظرًا لتدفق البيانات من الأشخاص والعملاء والعمليات وأجهزة إنترنت الأشياء (IoT) إلى مصدر واحد، فهناك فرصة لحلقات الملاحظات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="f8738-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="f8738-106">لتحقيق هذه التجربة، يعتبر التكامل بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى أمرًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="f8738-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="f8738-107">تم بناء بعض التطبيقات بالاستناد إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f8738-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="f8738-108">يمكِّن التكامل بين بيانات تطبيقات Finance and Operations وCommon Data Service التطبيقات الأخرى من التواصل مع Finance and Operations  بطريقة سلسة ومتماسكة.</span><span class="sxs-lookup"><span data-stu-id="f8738-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="f8738-109">توفر تطبيقات Finance and Operations وCommon Data Service إمكانية مزامنة البيانات في وقت قريب من الحقيقي بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى من خلال إطار عمل الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="f8738-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="f8738-110">تعتبر هذه التغطية واسعة النطاق وتشمل 28 مجالاً من التطبيق.</span><span class="sxs-lookup"><span data-stu-id="f8738-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="f8738-111">الهدف هو توفير تجربة مستخدم "One Dynamics 365" من خلال تدفقات البيانات السلسة التي تربط العمليات التجارية عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="f8738-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![رسم تخطيطي للنظرة عامة على البنية الهندسية](media/dual-write-overview.jpg)

<span data-ttu-id="f8738-113">تتوفر مقترحات القيمة التالية:</span><span class="sxs-lookup"><span data-stu-id="f8738-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="f8738-114">التدرج الهرمي للمؤسسات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f8738-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="f8738-115">مفهوم الشركة في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f8738-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="f8738-116">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="f8738-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="f8738-117">دفتر الأستاذ المتكامل</span><span class="sxs-lookup"><span data-stu-id="f8738-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="f8738-118">تجربه المنتج الموحدة</span><span class="sxs-lookup"><span data-stu-id="f8738-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="f8738-119">أصل المورّد المتكامل</span><span class="sxs-lookup"><span data-stu-id="f8738-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="f8738-120">المواقع والمستودعات المتكاملة</span><span class="sxs-lookup"><span data-stu-id="f8738-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="f8738-121">أصل الضريبة المتكامل</span><span class="sxs-lookup"><span data-stu-id="f8738-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="f8738-122">متطلبات النظام</span><span class="sxs-lookup"><span data-stu-id="f8738-122">System requirements</span></span>

<span data-ttu-id="f8738-123">تحتاج تدفقات البيانات المتزامنة وثنائية الاتجاه وفي الوقت الحقيقي تقريبًا الإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="f8738-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="f8738-124">Microsoft Dynamics 365 for Finance and Operations الإصدار 10.0.4 (يوليو 2019) مع platform update 28 أو أعلى</span><span class="sxs-lookup"><span data-stu-id="f8738-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="f8738-125">Microsoft Dynamics 365 for Customer Engagement، إصدار Platform 9.1 (4.2) أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="f8738-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="f8738-126">تعليمات الإعداد</span><span class="sxs-lookup"><span data-stu-id="f8738-126">Setup instructions</span></span>

<span data-ttu-id="f8738-127">اتبع الخطوات التالية لإعداد التكامل بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="f8738-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="f8738-128">فيما يتعلق بإعداد نظام الكتابة المزدوجة، راجع [الدليل المفصل خطوة بخطوة](https://aka.ms/dualwrite-docs) حول الإعلان عن معاينة الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="f8738-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="f8738-129">تحميل وتثبيت الحل من [Fin Ops وتكامل CDS/CE عبر الكتابة المزدوجة](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) مجموعة Yammer .</span><span class="sxs-lookup"><span data-stu-id="f8738-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="f8738-130">تحتوي الحزمة على خمسة حلول:</span><span class="sxs-lookup"><span data-stu-id="f8738-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="f8738-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="f8738-131">Dynamics365Company</span></span>
    + <span data-ttu-id="f8738-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f8738-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="f8738-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="f8738-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="f8738-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="f8738-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="f8738-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="f8738-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="f8738-136">اتبع ترتيب التنفيذ من أجل [مزامنة البيانات المرجعية الأولية](initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f8738-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="f8738-137">إذا واجهت مشكلات تتعلق بمزامنة الكتابة المزدوجة، فراجع [دليل استكشاف أخطاء تكامل البيانات وإصلاحها](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="f8738-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8738-138">لا يمكنك تشغيل الكتابة المزدوجة‏‎ جنبًا إلى جنب مع حل [العميل المتوقع إلى النقدية‬](../../../../supply-chain/sales-marketing/prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="f8738-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="f8738-139">إذا كنت تقوم بتشغيل حل "العميل المتوقع إلى النقدية‬"، فيجب إلغاء تثبيته.</span><span class="sxs-lookup"><span data-stu-id="f8738-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="f8738-140">يجب أيضًا تعطيل قوالب الكتابة المزدوجة للعميل والمورد التي تشكل جزءًا من الحل "العميل المتوقع إلى النقدية‬".</span><span class="sxs-lookup"><span data-stu-id="f8738-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
