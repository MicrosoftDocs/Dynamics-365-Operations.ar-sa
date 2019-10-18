---
title: تحليل أداء المتجر
description: تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Dynamics 365 Retail.
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
ms.openlocfilehash: b2ea6ad2e3d9589face06cd5f950973209c17d41
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017772"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="bff2a-103">تحليل أداء المتجر</span><span class="sxs-lookup"><span data-stu-id="bff2a-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bff2a-104">تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="bff2a-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="bff2a-105">كجزء من Retail، يستطيع المستخدمون دراسة أداء المتجر في الوقت الحقيقي على مختلف مستويات التدرج الهرمي للمؤسسات خلال فترة محددة عن طريق فتح تقرير **ملخص القناة** الجاهز من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="bff2a-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="bff2a-106">مساحة عمل**إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="bff2a-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="bff2a-107">مساحة عمل**ماليات متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **ماليات متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="bff2a-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="bff2a-108">قسم**الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير ملخص القناة**</span><span class="sxs-lookup"><span data-stu-id="bff2a-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="bff2a-109">يقدم هذا التقرير لقطةالملخصات التالية كجزء من أداء المتجر.</span><span class="sxs-lookup"><span data-stu-id="bff2a-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="bff2a-110">ملخص إجمالي المبيعات</span><span class="sxs-lookup"><span data-stu-id="bff2a-110">Gross sales summary</span></span>
- <span data-ttu-id="bff2a-111">ملخص نوع طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="bff2a-111">Tender type summary</span></span>
- <span data-ttu-id="bff2a-112">الملخص الضريبي</span><span class="sxs-lookup"><span data-stu-id="bff2a-112">Tax summary</span></span>
- <span data-ttu-id="bff2a-113">ملخص تجاوزات السعر</span><span class="sxs-lookup"><span data-stu-id="bff2a-113">Price overrides summary</span></span>
- <span data-ttu-id="bff2a-114">ملخص الخصومات</span><span class="sxs-lookup"><span data-stu-id="bff2a-114">Discounts summary</span></span>
