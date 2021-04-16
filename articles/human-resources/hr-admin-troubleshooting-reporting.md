---
title: خيارات إعداد التقارير
description: يتناول هذا المقال كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Microsoft Dynamics 365 Human Resources أو إنشاء تقارير جديدة.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803886"
---
# <a name="reporting-options"></a><span data-ttu-id="d9f48-103">خيارات إعداد التقارير</span><span class="sxs-lookup"><span data-stu-id="d9f48-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d9f48-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="d9f48-104">**Environment details**</span></span>

<span data-ttu-id="d9f48-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="d9f48-105">This issue applies to all environments.</span></span>

<span data-ttu-id="d9f48-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="d9f48-106">**Symptom**</span></span>

<span data-ttu-id="d9f48-107">يُريد العميل تخصيص تقارير Dynamics 365 Human Resources أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="d9f48-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="d9f48-108">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="d9f48-108">**Issue**</span></span>

<span data-ttu-id="d9f48-109">يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="d9f48-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="d9f48-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="d9f48-110">**Solution**</span></span>

- <span data-ttu-id="d9f48-111">يمكن الإبلاغ عن بيانات Human Resources التي تتدفق إلى Dataverse عبر موصل Power Apps Dataverse إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d9f48-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="d9f48-112">لاحظ أن Dataverse تحتوي على مجموعة فرعية من بيانات Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d9f48-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="d9f48-113">لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .</span><span class="sxs-lookup"><span data-stu-id="d9f48-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="d9f48-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d9f48-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="d9f48-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="d9f48-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="d9f48-116">يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Human Resources من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d9f48-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="d9f48-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="d9f48-117">**Long-term solution**</span></span>

<span data-ttu-id="d9f48-118">ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d9f48-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]