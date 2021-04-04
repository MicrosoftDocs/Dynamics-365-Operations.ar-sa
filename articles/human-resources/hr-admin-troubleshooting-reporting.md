---
title: خيارات إعداد التقارير
description: يتناول هذا المقال كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Microsoft Dynamics 365 Human Resources أو إنشاء تقارير جديدة.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463276"
---
# <a name="reporting-options"></a><span data-ttu-id="2540b-103">خيارات إعداد التقارير</span><span class="sxs-lookup"><span data-stu-id="2540b-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2540b-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="2540b-104">**Environment details**</span></span>

<span data-ttu-id="2540b-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="2540b-105">This issue applies to all environments.</span></span>

<span data-ttu-id="2540b-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="2540b-106">**Symptom**</span></span>

<span data-ttu-id="2540b-107">يُريد العميل تخصيص تقارير Dynamics 365 Human Resources أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="2540b-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="2540b-108">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="2540b-108">**Issue**</span></span>

<span data-ttu-id="2540b-109">يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="2540b-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="2540b-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="2540b-110">**Solution**</span></span>

- <span data-ttu-id="2540b-111">يمكن الإبلاغ عن بيانات Human Resources التي تتدفق إلى Dataverse عبر موصل Power Apps Dataverse إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="2540b-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="2540b-112">لاحظ أن Dataverse تحتوي على مجموعة فرعية من بيانات Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2540b-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="2540b-113">لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .</span><span class="sxs-lookup"><span data-stu-id="2540b-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="2540b-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2540b-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="2540b-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="2540b-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="2540b-116">يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Human Resources من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="2540b-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="2540b-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="2540b-117">**Long-term solution**</span></span>

<span data-ttu-id="2540b-118">ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2540b-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]