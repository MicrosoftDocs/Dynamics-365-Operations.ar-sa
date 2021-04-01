---
title: تحليل أداء المتجر
description: تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Dynamics 365 Commerce.
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
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: aced862e279135e25ca7380b746ae19b97227d10
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234235"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="b28e7-103">تحليل أداء المتجر</span><span class="sxs-lookup"><span data-stu-id="b28e7-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b28e7-104">تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول أداء المتجر واستكشافها واكتسابها استنادًا إلى بيانات Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b28e7-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="b28e7-105">كجزء من Retail، يستطيع المستخدمون دراسة أداء المتجر في الوقت الحقيقي على مختلف مستويات التدرج الهرمي للمؤسسات خلال فترة محددة عن طريق فتح تقرير **ملخص القناة** الجاهز من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="b28e7-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="b28e7-106">مساحة عمل **إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="b28e7-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="b28e7-107">مساحة عمل **ماليات متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **ماليات متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير ملخص القناة‬**</span><span class="sxs-lookup"><span data-stu-id="b28e7-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="b28e7-108">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير ملخص القناة**</span><span class="sxs-lookup"><span data-stu-id="b28e7-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="b28e7-109">يقدم هذا التقرير لقطةالملخصات التالية كجزء من أداء المتجر.</span><span class="sxs-lookup"><span data-stu-id="b28e7-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="b28e7-110">ملخص إجمالي المبيعات</span><span class="sxs-lookup"><span data-stu-id="b28e7-110">Gross sales summary</span></span>
- <span data-ttu-id="b28e7-111">ملخص نوع طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="b28e7-111">Tender type summary</span></span>
- <span data-ttu-id="b28e7-112">الملخص الضريبي</span><span class="sxs-lookup"><span data-stu-id="b28e7-112">Tax summary</span></span>
- <span data-ttu-id="b28e7-113">ملخص تجاوزات السعر</span><span class="sxs-lookup"><span data-stu-id="b28e7-113">Price overrides summary</span></span>
- <span data-ttu-id="b28e7-114">ملخص الخصومات</span><span class="sxs-lookup"><span data-stu-id="b28e7-114">Discounts summary</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]