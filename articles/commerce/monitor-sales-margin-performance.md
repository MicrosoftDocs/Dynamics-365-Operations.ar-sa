---
title: مراقبة أداء المبيعات والهامش
description: يمكن مراقبة أداء المبيعات والهامش في الوقت الحقيقي باستخدام Dynamics 365 Commerce.
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
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51dc7c4b62a497e3dc9279b3c5a616057316c106
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985876"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="9bb0a-103">رصد أداء المبيعات والهامش</span><span class="sxs-lookup"><span data-stu-id="9bb0a-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9bb0a-104">يمكن مراقبة أداء المبيعات والهامش في الوقت الحقيقي باستخدام Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9bb0a-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9bb0a-105">كجزء من Commerce، يستطيع المستخدمون مراقبة أداء المبيعات والهامش في الوقت الحقيقي عبر مختلف مستويات التدرج الهرمي للمؤسسات للأبعاد التالية:</span><span class="sxs-lookup"><span data-stu-id="9bb0a-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="9bb0a-106">المنتجات</span><span class="sxs-lookup"><span data-stu-id="9bb0a-106">Products</span></span>
- <span data-ttu-id="9bb0a-107">فئات</span><span class="sxs-lookup"><span data-stu-id="9bb0a-107">Categories</span></span>
- <span data-ttu-id="9bb0a-108">الخصومات</span><span class="sxs-lookup"><span data-stu-id="9bb0a-108">Discounts</span></span>
- <span data-ttu-id="9bb0a-109">السنوات كفترة زمنية</span><span class="sxs-lookup"><span data-stu-id="9bb0a-109">Years as time period</span></span>
- <span data-ttu-id="9bb0a-110">السجلات‬/المحطات الطرفية</span><span class="sxs-lookup"><span data-stu-id="9bb0a-110">Registers/terminals</span></span>
- <span data-ttu-id="9bb0a-111">الموظفون</span><span class="sxs-lookup"><span data-stu-id="9bb0a-111">Staff/employees</span></span>
- <span data-ttu-id="9bb0a-112">العملاء</span><span class="sxs-lookup"><span data-stu-id="9bb0a-112">Customers</span></span>
- <span data-ttu-id="9bb0a-113">وحدات التشغيل</span><span class="sxs-lookup"><span data-stu-id="9bb0a-113">Operating units</span></span>

<span data-ttu-id="9bb0a-114">بالإضافة إلى ذلك، هناك تقريران فريدان يستفيدان من هيكل شبكة التدرج الهرمي ويسمحان للمستخدمين بمراقبة أداء المبيعات والهامش من خلال التنقل للأسفل من عقدة الفئة العليا وصولاً إلى عقد طرفية فردية للفئة في التدرج الهرمي الافتراضي لفئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="9bb0a-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="9bb0a-115">باستطاعة المستخدمين أيضًا التنقل للأسفل من وحدة التشغيل العليا إلى قناة فردية في التدرج الهرمي للمؤسسة المحدد كافتراضي لأغراض تتعلق بالتدرج الهرمي للمؤسسات للتقارير‬</span><span class="sxs-lookup"><span data-stu-id="9bb0a-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="9bb0a-116">يمكنك فتح التقارير من أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="9bb0a-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="9bb0a-117">مساحة عمل **إدارة المتاجر** &gt; **البيع بالتجزئة والتجارة** &gt; **القنوات** &gt; **إدارة المتاجر** &gt; **التقارير**</span><span class="sxs-lookup"><span data-stu-id="9bb0a-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9bb0a-118">مساحة عمل **إدارة الفئات والمنتجات** &gt; **البيع بالتجزئة والتجارة** &gt; **المنتجات والفئات** &gt; **إدارة المتاجر** &gt; **التقارير**</span><span class="sxs-lookup"><span data-stu-id="9bb0a-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9bb0a-119">مساحة عمل **إدارة التسعير والخصومات** &gt; **البيع بالتجزئة والتجارة** &gt; **التسعير والخصومات** &gt; **إدارة المتاجر** &gt; **التقارير**</span><span class="sxs-lookup"><span data-stu-id="9bb0a-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9bb0a-120">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة والتجارة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات**</span><span class="sxs-lookup"><span data-stu-id="9bb0a-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
