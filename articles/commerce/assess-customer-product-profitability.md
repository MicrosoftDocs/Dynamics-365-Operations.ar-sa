---
title: تقييم العميل وربحية المنتج
description: تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول العملاء وربحية المنتج‬ واستكشافها واكتسابها من بيانات Dynamics 365 Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3770832cb8eee96931d8f8e68c726d5e09d3fceb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980044"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="6cb4a-103">تقييم العميل وربحية المنتج</span><span class="sxs-lookup"><span data-stu-id="6cb4a-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6cb4a-104">تشرح هذه المقالة كيفية استخدام التحليلات في الذاكرة وفي الوقت الحقيقي للوصول إلى معلومات حول العملاء وربحية المنتج‬ واستكشافها واكتسابها من بيانات Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6cb4a-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="6cb4a-105">وكجزء من Commerce، يستطيع المستخدمون دراسة الربحية لأفضل العملاء (من 10 إلى 100) على مختلف مستويات التدرج الهرمي للمؤسسات، بناء على أحد المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="6cb4a-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6cb4a-106">مبلغ المبيعات</span><span class="sxs-lookup"><span data-stu-id="6cb4a-106">Sales amount</span></span>
- <span data-ttu-id="6cb4a-107">الكمية</span><span class="sxs-lookup"><span data-stu-id="6cb4a-107">Quantity</span></span>
- <span data-ttu-id="6cb4a-108">إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="6cb4a-108">Gross profit margin</span></span>
- <span data-ttu-id="6cb4a-109">نسبة الهامش</span><span class="sxs-lookup"><span data-stu-id="6cb4a-109">Margin percentage</span></span>

<span data-ttu-id="6cb4a-110">لإجراء هذا التقييم، يمكنك استخدام تقرير **أفضل العملاء** الجاهز على العمل، والذي يمكنك من خلاله فتح أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="6cb4a-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6cb4a-111">مساحة عمل **إدارة المتجر** &gt; **البيع بالتجزئة والتجارة** &gt; **القنوات** &gt; **إدارة المتجر** &gt; **التقارير** &gt; **تقرير أهم العملاء**</span><span class="sxs-lookup"><span data-stu-id="6cb4a-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="6cb4a-112">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة والتجارة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير أهم العملاء‬**</span><span class="sxs-lookup"><span data-stu-id="6cb4a-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="6cb4a-113">وبالمثل، يستطيع المستخدمون دراسة الربحية لأفضل العملاء (من 10 إلى 100) على مختلف مستويات التدرج الهرمي للمؤسسات، بناء على أحد المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="6cb4a-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6cb4a-114">مبلغ المبيعات</span><span class="sxs-lookup"><span data-stu-id="6cb4a-114">Sales amount</span></span>
- <span data-ttu-id="6cb4a-115">الكمية</span><span class="sxs-lookup"><span data-stu-id="6cb4a-115">Quantity</span></span>
- <span data-ttu-id="6cb4a-116">إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="6cb4a-116">Gross profit margin</span></span>
- <span data-ttu-id="6cb4a-117">نسبة الهامش</span><span class="sxs-lookup"><span data-stu-id="6cb4a-117">Margin percentage</span></span>

<span data-ttu-id="6cb4a-118">لإجراء هذا التقييم، يمكنك استخدام تقرير **أفضل المنتجات** الجاهز على العمل، والذي يمكنك من خلاله فتح أي من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="6cb4a-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6cb4a-119">مساحة عمل **إدارة المتجر** &gt; **البيع بالتجزئة والتجارة** &gt; **القنوات** &gt; **إدارة المتجر** &gt; **التقارير** &gt; **تقرير أهم المنتجات**</span><span class="sxs-lookup"><span data-stu-id="6cb4a-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6cb4a-120">مساحة عمل **إدارة الفئات والمنتجات** &gt; **البيع بالتجزئة والتجارة** &gt; **المنتجات والفئات** &gt; **إدارة المتجر** &gt; **التقارير** &gt; **تقرير أهم المنتجات**</span><span class="sxs-lookup"><span data-stu-id="6cb4a-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6cb4a-121">قسم **الاستعلامات والتقارير** &gt; **البيع بالتجزئة والتجارة** &gt; **الاستعلامات والتقارير** &gt; **تقارير المبيعات** &gt; **تقرير أهم المنتجات‬**</span><span class="sxs-lookup"><span data-stu-id="6cb4a-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
