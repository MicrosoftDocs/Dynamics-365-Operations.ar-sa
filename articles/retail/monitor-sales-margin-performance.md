---
title: مراقبة أداء المبيعات والهامش
description: يمكن مراقبة أداء المبيعات والهامش في الوقت الحقيقي باستخدام Dynamics 365 Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 46ecefdd15a3a208588aaf630571764047464cdb
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018054"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="b452f-103">رصد أداء المبيعات والهامش</span><span class="sxs-lookup"><span data-stu-id="b452f-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b452f-104">يمكن مراقبة أداء المبيعات والهامش في الوقت الحقيقي باستخدام Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="b452f-104">You can monitor sales and margin performance in real time using Dynamics 365 Retail.</span></span>

<span data-ttu-id="b452f-105">كجزء من البيع بالتجزئة، يستطيع المستخدمون مراقبة أداء المبيعات والهامش في الوقت الحقيقي عبر مختلف مستويات التدرج الهرمي للمؤسسات للأبعاد التالية:</span><span class="sxs-lookup"><span data-stu-id="b452f-105">As part of Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="b452f-106">المنتجات</span><span class="sxs-lookup"><span data-stu-id="b452f-106">Products</span></span>
- <span data-ttu-id="b452f-107">فئات</span><span class="sxs-lookup"><span data-stu-id="b452f-107">Categories</span></span>
- <span data-ttu-id="b452f-108">الخصومات</span><span class="sxs-lookup"><span data-stu-id="b452f-108">Discounts</span></span>
- <span data-ttu-id="b452f-109">السنوات كفترة زمنية</span><span class="sxs-lookup"><span data-stu-id="b452f-109">Years as time period</span></span>
- <span data-ttu-id="b452f-110">السجلات‬/المحطات الطرفية</span><span class="sxs-lookup"><span data-stu-id="b452f-110">Registers/terminals</span></span>
- <span data-ttu-id="b452f-111">الموظفون</span><span class="sxs-lookup"><span data-stu-id="b452f-111">Staff/employees</span></span>
- <span data-ttu-id="b452f-112">العملاء</span><span class="sxs-lookup"><span data-stu-id="b452f-112">Customers</span></span>
- <span data-ttu-id="b452f-113">وحدات التشغيل</span><span class="sxs-lookup"><span data-stu-id="b452f-113">Operating units</span></span>

<span data-ttu-id="b452f-114">بالإضافة إلى ذلك، هناك تقريران فريدان يستفيدان من هيكل شبكة التدرج الهرمي ويسمحان للمستخدمين بمراقبة أداء المبيعات والهامش من خلال التنقل للأسفل من عقدة الفئة العليا وصولاً إلى عقد طرفية فردية للفئة في التدرج الهرمي الافتراضي لفئات منتجات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="b452f-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="b452f-115">باستطاعة المستخدمين أيضًا التنقل للأسفل من وحدة التشغيل العليا إلى قناة فردية في التدرج الهرمي للمؤسسة المحدد كافتراضي لأغراض تتعلق بالتدرج الهرمي لتقارير البيع بالتجزئة‬</span><span class="sxs-lookup"><span data-stu-id="b452f-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="b452f-116">يمكنك فتح التقارير من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="b452f-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="b452f-117">مساحة عمل **إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير**</span><span class="sxs-lookup"><span data-stu-id="b452f-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="b452f-118">مساحة عمل **إدارة الفئات والمنتجات** &gt; **البيع بالتجزئة** &gt; **المنتجات والفئات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير**</span><span class="sxs-lookup"><span data-stu-id="b452f-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="b452f-119">مساحة عمل **إدارة التسعير والخصومات** &gt; **البيع بالتجزئة** &gt; **التسعير والخصومات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير**</span><span class="sxs-lookup"><span data-stu-id="b452f-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="b452f-120">مقطع **الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات**</span><span class="sxs-lookup"><span data-stu-id="b452f-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
