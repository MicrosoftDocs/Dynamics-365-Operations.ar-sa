---
title: "تقييم العميل وربحية المنتج"
description: "تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول العملاء وربحية المنتج‬ واستكشافها واكتسابها من بيانات Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 04ebc624212e6909eda7589b71cd84a22010e721
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="23b1d-103">تقييم العميل وربحية المنتج</span><span class="sxs-lookup"><span data-stu-id="23b1d-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="23b1d-104">تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول العملاء وربحية المنتج‬ واستكشافها واكتسابها من بيانات Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="23b1d-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="23b1d-105">وكجزء من Dynamics 365 for Retail، يستطيع المستخدمون دراسة الربحية لأفضل العملاء (من 10 إلى 100) على مختلف مستويات التدرج الهرمي للمؤسسات، بناء على أحد المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="23b1d-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="23b1d-106">مبلغ المبيعات</span><span class="sxs-lookup"><span data-stu-id="23b1d-106">Sales amount</span></span>
-   <span data-ttu-id="23b1d-107">الكمية</span><span class="sxs-lookup"><span data-stu-id="23b1d-107">Quantity</span></span>
-   <span data-ttu-id="23b1d-108">إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="23b1d-108">Gross profit margin</span></span>
-   <span data-ttu-id="23b1d-109">نسبة الهامش</span><span class="sxs-lookup"><span data-stu-id="23b1d-109">Margin percentage</span></span>

<span data-ttu-id="23b1d-110">لإجراء هذا التقييم، يمكنك استخدام تقرير **أفضل العملاء** الجاهز على العمل، والذي يمكنك من خلاله فتح أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="23b1d-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="23b1d-111">مساحة عمل **إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير أهم العملاء**</span><span class="sxs-lookup"><span data-stu-id="23b1d-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="23b1d-112">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير أهم العملاء**</span><span class="sxs-lookup"><span data-stu-id="23b1d-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="23b1d-113">وبالمثل، يستطيع المستخدمون دراسة الربحية لأفضل العملاء (من 10 إلى 100) على مختلف مستويات التدرج الهرمي للمؤسسات، بناء على أحد المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="23b1d-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="23b1d-114">مبلغ المبيعات</span><span class="sxs-lookup"><span data-stu-id="23b1d-114">Sales amount</span></span>
-   <span data-ttu-id="23b1d-115">الكمية</span><span class="sxs-lookup"><span data-stu-id="23b1d-115">Quantity</span></span>
-   <span data-ttu-id="23b1d-116">إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="23b1d-116">Gross profit margin</span></span>
-   <span data-ttu-id="23b1d-117">نسبة الهامش</span><span class="sxs-lookup"><span data-stu-id="23b1d-117">Margin percentage</span></span>

<span data-ttu-id="23b1d-118">لإجراء هذا التقييم، يمكنك استخدام تقرير **أفضل المنتجات**الجاهز على العمل، والذي يمكنك من خلاله فتح أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="23b1d-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="23b1d-119">مساحة عمل **إدارة متجر البيع بالتجزئة** &gt; **البيع بالتجزئة** &gt; **القنوات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير أهم المنتجات**</span><span class="sxs-lookup"><span data-stu-id="23b1d-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="23b1d-120">مساحة عمل **إدارة الفئات والمنتجات** &gt; **البيع بالتجزئة** &gt; **المنتجات والفئات** &gt; **إدارة متجر البيع بالتجزئة** &gt; **التقارير** &gt; **تقرير أهم المنتجات**</span><span class="sxs-lookup"><span data-stu-id="23b1d-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="23b1d-121">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير أهم المنتجات**</span><span class="sxs-lookup"><span data-stu-id="23b1d-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




