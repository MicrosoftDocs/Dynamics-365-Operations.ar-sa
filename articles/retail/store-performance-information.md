---
title: تحليل أداء المتجر
description: تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c975c021b6db49d1e25fd036f4955c7223e438ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "346170"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="cfcd6-103">تحليل أداء المتجر</span><span class="sxs-lookup"><span data-stu-id="cfcd6-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cfcd6-104">تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="cfcd6-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="cfcd6-105">كجزء من Dynamics 365 for Retail، يستطيع المستخدمون دراسة أداء المتجر في الوقت الحقيقي على مختلف مستويات التدرج الهرمي للمؤسسات خلال فترة محددة عن طريق فتح تقرير **ملخص القناة** الجاهز من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="cfcd6-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="cfcd6-106">مساحة عمل**إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="cfcd6-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="cfcd6-107">مساحة عمل**ماليات متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **ماليات متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="cfcd6-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="cfcd6-108">قسم**الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير ملخص القناة**</span><span class="sxs-lookup"><span data-stu-id="cfcd6-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="cfcd6-109">يقدم هذا التقرير لقطةالملخصات التالية كجزء من أداء المتجر.</span><span class="sxs-lookup"><span data-stu-id="cfcd6-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="cfcd6-110">ملخص إجمالي المبيعات</span><span class="sxs-lookup"><span data-stu-id="cfcd6-110">Gross sales summary</span></span>
- <span data-ttu-id="cfcd6-111">ملخص نوع طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="cfcd6-111">Tender type summary</span></span>
- <span data-ttu-id="cfcd6-112">الملخص الضريبي</span><span class="sxs-lookup"><span data-stu-id="cfcd6-112">Tax summary</span></span>
- <span data-ttu-id="cfcd6-113">ملخص تجاوزات السعر</span><span class="sxs-lookup"><span data-stu-id="cfcd6-113">Price overrides summary</span></span>
- <span data-ttu-id="cfcd6-114">ملخص الخصومات</span><span class="sxs-lookup"><span data-stu-id="cfcd6-114">Discounts summary</span></span>
