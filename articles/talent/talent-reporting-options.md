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
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897938"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="d3660-103">خيارات إعداد التقارير في Talent</span><span class="sxs-lookup"><span data-stu-id="d3660-103">Reporting options in Talent</span></span>

<span data-ttu-id="d3660-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="d3660-104">**Environment details**</span></span>

<span data-ttu-id="d3660-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="d3660-105">This issue applies to all environments.</span></span>

<span data-ttu-id="d3660-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="d3660-106">**Symptom**</span></span>

<span data-ttu-id="d3660-107">يُريد العميل تخصيص تقارير Dynamics 365 Talent أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="d3660-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="d3660-108">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="d3660-108">**Issue**</span></span>

<span data-ttu-id="d3660-109">يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="d3660-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="d3660-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="d3660-110">**Solution**</span></span>

- <span data-ttu-id="d3660-111">يمكن الإبلاغ عن بيانات Core HR التي تتدفق إلى Common Data Service عبر موصل Power AppsCommon Data Service إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d3660-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="d3660-112">لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Core HR.</span><span class="sxs-lookup"><span data-stu-id="d3660-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="d3660-113">لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .</span><span class="sxs-lookup"><span data-stu-id="d3660-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="d3660-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Talent.</span><span class="sxs-lookup"><span data-stu-id="d3660-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="d3660-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="d3660-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="d3660-116">يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Talent من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d3660-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="d3660-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="d3660-117">**Long-term solution**</span></span>

<span data-ttu-id="d3660-118">ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3660-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
