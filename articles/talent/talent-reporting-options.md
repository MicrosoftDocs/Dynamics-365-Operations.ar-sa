---
title: خيارات إعداد التقارير في Talent
description: يتناول هذا الموضوع كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Dynamics 365 Talent أو إنشاء تقارير جديدة.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ecbeb03b535f19131ddc6649d005702876bab65c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772955"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="1e92e-103">خيارات إعداد التقارير في Talent</span><span class="sxs-lookup"><span data-stu-id="1e92e-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e92e-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="1e92e-104">**Environment details**</span></span>

<span data-ttu-id="1e92e-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="1e92e-105">This issue applies to all environments.</span></span>

<span data-ttu-id="1e92e-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="1e92e-106">**Symptom**</span></span>

<span data-ttu-id="1e92e-107">يُريد العميل تخصيص تقارير Dynamics 365 Talent أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="1e92e-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="1e92e-108">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="1e92e-108">**Issue**</span></span>

<span data-ttu-id="1e92e-109">يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="1e92e-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="1e92e-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="1e92e-110">**Solution**</span></span>

- <span data-ttu-id="1e92e-111">يمكن الإبلاغ عن بيانات Core HR التي تتدفق إلى Common Data Service عبر موصل Power AppsCommon Data Service إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="1e92e-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="1e92e-112">لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Core HR.</span><span class="sxs-lookup"><span data-stu-id="1e92e-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="1e92e-113">لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .</span><span class="sxs-lookup"><span data-stu-id="1e92e-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="1e92e-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Talent.</span><span class="sxs-lookup"><span data-stu-id="1e92e-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="1e92e-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="1e92e-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="1e92e-116">يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Talent من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="1e92e-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="1e92e-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="1e92e-117">**Long-term solution**</span></span>

<span data-ttu-id="1e92e-118">ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1e92e-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
