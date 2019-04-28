---
title: خيارات إعداد التقارير في Talent
description: يتناول هذا الموضوع كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Dynamics 365 for Talent أو إنشاء تقارير جديدة.
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
ms.openlocfilehash: 7e00a6e4fc01f72e1ef2347e08754997135215ed
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/12/2019
ms.locfileid: "950049"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="43b3a-103">خيارات إعداد التقارير في Talent</span><span class="sxs-lookup"><span data-stu-id="43b3a-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="43b3a-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="43b3a-104">**Environment details**</span></span>

<span data-ttu-id="43b3a-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="43b3a-105">This issue applies to all environments.</span></span>

<span data-ttu-id="43b3a-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="43b3a-106">**Symptom**</span></span>

<span data-ttu-id="43b3a-107">يُريد العميل تخصيص تقارير Dynamics 365 for Talent أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="43b3a-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="43b3a-108">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="43b3a-108">**Issue**</span></span>

<span data-ttu-id="43b3a-109">يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="43b3a-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="43b3a-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="43b3a-110">**Solution**</span></span>

- <span data-ttu-id="43b3a-111">يمكن الإبلاغ عن بيانات Core HR التي تتدفق إلى Common Data Service عبر موصل PowerApps Common Data Service إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="43b3a-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="43b3a-112">لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Core HR.</span><span class="sxs-lookup"><span data-stu-id="43b3a-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="43b3a-113">لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير ولوحات معلومات Power BI باستخدام PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="43b3a-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="43b3a-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Talent.</span><span class="sxs-lookup"><span data-stu-id="43b3a-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="43b3a-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="43b3a-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="43b3a-116">يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Talent من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="43b3a-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="43b3a-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="43b3a-117">**Long-term solution**</span></span>

<span data-ttu-id="43b3a-118">ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="43b3a-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
