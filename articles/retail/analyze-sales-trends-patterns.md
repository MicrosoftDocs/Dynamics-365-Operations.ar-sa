---
title: تحليل أنماط واتجاهات المبيعات
description: يمكن دراسة اتجاهات وأنماط المبيعات في الوقت الحقيقي في Dynamics 365 Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, SysReportViewerForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c54e707d312d7ac3bbcad71a914e528859038a13
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025807"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="2a387-103">تحليل أنماط واتجاهات المبيعات</span><span class="sxs-lookup"><span data-stu-id="2a387-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a387-104">يمكن دراسة اتجاهات وأنماط المبيعات في الوقت الحقيقي في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2a387-104">You can study sales trends and patterns in real time in Dynamics 365 Retail.</span></span>

<span data-ttu-id="2a387-105">كجزء من Retail، يستطيع المستخدمون دراسة اتجاهات وأنماط المبيعات في الوقت الحقيقي عبر مختلف مستويات التدرج الهرمي للمؤسسات على مدى فترة مكونة من سنوات باستخدام التقرير الجاهز **قناة المبيعات حسب السنة**‬.</span><span class="sxs-lookup"><span data-stu-id="2a387-105">As part of Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="2a387-106">يمكنك فتح هذا التقرير من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="2a387-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="2a387-107">مساحة عمل **إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير قناة المبيعات حسب السنة**</span><span class="sxs-lookup"><span data-stu-id="2a387-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="2a387-108">مساحة عمل **ماليات متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **ماليات متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير قناة المبيعات حسب السنة**</span><span class="sxs-lookup"><span data-stu-id="2a387-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="2a387-109">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير قناة المبيعات حسب السنة**</span><span class="sxs-lookup"><span data-stu-id="2a387-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="2a387-110">يستطيع المستخدمون أيضًا دراسة اتجاهات وأنماط المبيعات في الساعة عبر مختلف مستويات التدرج الهرمي للمؤسسة على مدى فترة محددة باستخدام تقرير **قناة المبيعات حسب الساعة‬** الجاهز.</span><span class="sxs-lookup"><span data-stu-id="2a387-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="2a387-111">يمكنك فتح هذا التقرير من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="2a387-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="2a387-112">مساحة عمل **إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير قناة المبيعات حسب الساعة**</span><span class="sxs-lookup"><span data-stu-id="2a387-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="2a387-113">مساحة عمل **ماليات متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **ماليات متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير قناة المبيعات حسب الساعة**</span><span class="sxs-lookup"><span data-stu-id="2a387-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="2a387-114">قسم**الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير قناة المبيعات حسب الساعة**</span><span class="sxs-lookup"><span data-stu-id="2a387-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>
