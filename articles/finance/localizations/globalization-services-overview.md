---
title: خدمات العولمة في Dynamics 365
description: يقدم هذا الموضوع نظرة عامة على خدمات العولمة في Microsoft Dynamics 365.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893037"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="045d9-103">خدمات العولمة في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="045d9-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="045d9-104">يمكن تكوين خدمات العولمة التالية لتوسيع الإمكانيات الموجودة في بعض خدمات Microsoft Dynamics 365 عبر الإنترنت:</span><span class="sxs-lookup"><span data-stu-id="045d9-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="045d9-105">تدعم خدمة **Regulatory Configuration Service (RCS)** تكوين أنواع مختلفة من المستندات والتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="045d9-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="045d9-106">توفر RCS إصدارًا محسنًا لمصمم التقارير الإلكترونية حيث مستودع التكوين هو خدمة مستقلة.</span><span class="sxs-lookup"><span data-stu-id="045d9-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="045d9-107">لمزيد من المعلومات، راجع [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="045d9-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="045d9-108">تجمع **الفوترة الإلكترونية** تنسيقات قابلة للتكوين الخاصة بعمليات التحويل والتوقيعات الرقمية وعمليات التكامل القابلة للتكوين للاتصال بخدمات الويب الخارجية، بما في ذلك معالجة الشهادات والردود..</span><span class="sxs-lookup"><span data-stu-id="045d9-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="045d9-109">لمزيد من المعلومات، راجع [الفوترة الإلكترونية‎](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="045d9-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="045d9-110">يوفر **حساب الضريبة** مرونة محسنة من خلال دعم معرفات ضرائب متعددة وتحديد كود الضريبة ومصمم حساب الضريبة ومشغل وقت التشغيل للتوافق مع اللوائح الضريبية المعقدة على مستوى العالم.</span><span class="sxs-lookup"><span data-stu-id="045d9-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="045d9-111">لمزيد من المعلومات، راجع [حساب الضريبة](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="045d9-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="045d9-112">توفر خدمات العولمة هذه تكاملاً جاهزًا مع خدمات Dynamics 365 عبر الإنترنت التالية.</span><span class="sxs-lookup"><span data-stu-id="045d9-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="045d9-113">الخدمة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="045d9-113">Online service</span></span> | <span data-ttu-id="045d9-114">خدمة التكوين التنظيمية</span><span class="sxs-lookup"><span data-stu-id="045d9-114">RCS</span></span> | <span data-ttu-id="045d9-115">الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="045d9-115">Electronic Invoicing</span></span> | <span data-ttu-id="045d9-116">(إصدار أولي) حساب الضرائب</span><span class="sxs-lookup"><span data-stu-id="045d9-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="045d9-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="045d9-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="045d9-118">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-118">Yes</span></span> | <span data-ttu-id="045d9-119">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-119">Yes</span></span> | <span data-ttu-id="045d9-120">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-120">Yes</span></span> | 
| <span data-ttu-id="045d9-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="045d9-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="045d9-122">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-122">Yes</span></span> | <span data-ttu-id="045d9-123">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-123">Yes</span></span> | <span data-ttu-id="045d9-124">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-124">Yes</span></span> | 
| <span data-ttu-id="045d9-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="045d9-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="045d9-126">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-126">Yes</span></span> | <span data-ttu-id="045d9-127">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-127">Yes</span></span> | <span data-ttu-id="045d9-128">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="045d9-128">Not applicable</span></span> | 
| <span data-ttu-id="045d9-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="045d9-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="045d9-130">نعم</span><span class="sxs-lookup"><span data-stu-id="045d9-130">Yes</span></span> | <span data-ttu-id="045d9-131">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="045d9-131">Not applicable</span></span> | <span data-ttu-id="045d9-132">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="045d9-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="045d9-133">نظرًا للاختلافات في توفر المواقع الجغرافية الخاصة بـ Azure لخدمة RCS، قد يتسبب تكوين هذه الخدمة في تحويل بيانات العميل خارج المواقع الجغرافية التي تم تحديدها لخدمه Dynamics 365 عبر الإنترنت القابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="045d9-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="045d9-134">لمزيد من المعلومات، راجع [Dynamics 365 وPower Platform: التوافر وموقع البيانات واللغة والترجمة](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="045d9-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>