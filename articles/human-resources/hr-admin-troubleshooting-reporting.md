---
title: خيارات إعداد التقارير
description: يتناول هذا المقال كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Microsoft Dynamics 365 Human Resources أو إنشاء تقارير جديدة.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008031"
---
# <a name="reporting-options"></a><span data-ttu-id="2ce97-103">خيارات إعداد التقارير</span><span class="sxs-lookup"><span data-stu-id="2ce97-103">Reporting options</span></span>

<span data-ttu-id="2ce97-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="2ce97-104">**Environment details**</span></span>

<span data-ttu-id="2ce97-105">تنطبق هذه المشكلة على كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="2ce97-105">This issue applies to all environments.</span></span>

<span data-ttu-id="2ce97-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="2ce97-106">**Symptom**</span></span>

<span data-ttu-id="2ce97-107">يُريد العميل تخصيص تقارير Dynamics 365 Human Resources أو إنشاء تقارير جديدة.</span><span class="sxs-lookup"><span data-stu-id="2ce97-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="2ce97-108">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="2ce97-108">**Issue**</span></span>

<span data-ttu-id="2ce97-109">يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.</span><span class="sxs-lookup"><span data-stu-id="2ce97-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="2ce97-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="2ce97-110">**Solution**</span></span>

- <span data-ttu-id="2ce97-111">يمكن الإبلاغ عن بيانات Human Resources التي تتدفق إلى Common Data Service عبر موصل Power Apps Common Data Service إلى Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="2ce97-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="2ce97-112">لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2ce97-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="2ce97-113">لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .</span><span class="sxs-lookup"><span data-stu-id="2ce97-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="2ce97-114">يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2ce97-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="2ce97-115">يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="2ce97-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="2ce97-116">يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Human Resources من خلال تكامل Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="2ce97-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="2ce97-117">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="2ce97-117">**Long-term solution**</span></span>

<span data-ttu-id="2ce97-118">ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2ce97-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
