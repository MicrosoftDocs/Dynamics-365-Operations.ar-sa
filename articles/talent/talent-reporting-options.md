---
title: "خيارات إعداد التقارير في Talent"
description: "يتناول هذا الموضوع كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Microsoft Dynamics 365 for Talent أو إنشاء تقارير جديدة."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="fb10a-103">خيارات إعداد التقارير في Talent</span><span class="sxs-lookup"><span data-stu-id="fb10a-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb10a-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="fb10a-104">**Environment details**</span></span>

<span data-ttu-id="fb10a-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="fb10a-105">This issue applies to all environments.</span></span>

<span data-ttu-id="fb10a-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="fb10a-106">**Symptom**</span></span>

<span data-ttu-id="fb10a-107">يُريد العميل تخصيص تقارير Microsoft Dynamics 365 for Talent أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="fb10a-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="fb10a-108">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="fb10a-108">**Issue**</span></span>

<span data-ttu-id="fb10a-109">لا يمكن للمستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="fb10a-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="fb10a-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="fb10a-110">**Solution**</span></span>

- <span data-ttu-id="fb10a-111">يمكن الإبلاغ عن بيانات Core HR التي تتبع Common Data Service للتطبيقات من خلال موصل PowerApps CDS إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="fb10a-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="fb10a-112">لاحظ أن Common Data Service للتطبيقات تحتوي على مجموعة فرعية من بيانات Core HR.</span><span class="sxs-lookup"><span data-stu-id="fb10a-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="fb10a-113">للحصول على المزيد من المعلومات حول Power Bi ولوحات المعلومات، راجع [إنشاء تقارير Power Bi ولوحات المعلومات باستخدام PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="fb10a-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="fb10a-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Talent.</span><span class="sxs-lookup"><span data-stu-id="fb10a-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="fb10a-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="fb10a-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="fb10a-116">يمكن تصدير البيانات إلى  Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Talent من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="fb10a-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="fb10a-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="fb10a-117">**Long-term solution**</span></span>

<span data-ttu-id="fb10a-118">سوفر تتوفر خيارات Power BI، وسوف تكون المزيد من البيانات والكيانات جزءًا من Common Data Service للتطبيقات.</span><span class="sxs-lookup"><span data-stu-id="fb10a-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

