---
title: "تحليل أداء المتجر"
description: "تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c975c021b6db49d1e25fd036f4955c7223e438ea
ms.contentlocale: ar-sa
ms.lasthandoff: 01/04/2019

---

# <a name="analyze-store-performance"></a><span data-ttu-id="945b3-103">تحليل أداء المتجر</span><span class="sxs-lookup"><span data-stu-id="945b3-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="945b3-104">تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="945b3-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="945b3-105">كجزء من Dynamics 365 for Retail، يستطيع المستخدمون دراسة أداء المتجر في الوقت الحقيقي على مختلف مستويات التدرج الهرمي للمؤسسات خلال فترة محددة عن طريق فتح تقرير **ملخص القناة** الجاهز من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="945b3-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="945b3-106">مساحة عمل**إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="945b3-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="945b3-107">مساحة عمل**ماليات متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **ماليات متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="945b3-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="945b3-108">قسم**الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير ملخص القناة**</span><span class="sxs-lookup"><span data-stu-id="945b3-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="945b3-109">يقدم هذا التقرير لقطةالملخصات التالية كجزء من أداء المتجر.</span><span class="sxs-lookup"><span data-stu-id="945b3-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="945b3-110">ملخص إجمالي المبيعات</span><span class="sxs-lookup"><span data-stu-id="945b3-110">Gross sales summary</span></span>
- <span data-ttu-id="945b3-111">ملخص نوع طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="945b3-111">Tender type summary</span></span>
- <span data-ttu-id="945b3-112">الملخص الضريبي</span><span class="sxs-lookup"><span data-stu-id="945b3-112">Tax summary</span></span>
- <span data-ttu-id="945b3-113">ملخص تجاوزات السعر</span><span class="sxs-lookup"><span data-stu-id="945b3-113">Price overrides summary</span></span>
- <span data-ttu-id="945b3-114">ملخص الخصومات</span><span class="sxs-lookup"><span data-stu-id="945b3-114">Discounts summary</span></span>

