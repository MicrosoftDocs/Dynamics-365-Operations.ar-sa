---
title: التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع إلزامي
description: يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. يُعد بُعد المستودع إلزاميًا.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92160b45590245e2b1caab6732d1b0aaeaabd208
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975886"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="a8059-104">التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="a8059-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8059-105">يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية.</span><span class="sxs-lookup"><span data-stu-id="a8059-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="a8059-106">يُعد بُعد المستودع إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="a8059-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="a8059-107">يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="a8059-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="a8059-108">تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="a8059-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="a8059-109">تم تعيين بُعد المستودع على إلزامي ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="a8059-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="a8059-110">تم تعيين الموقع وأبعاد المستودع لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="a8059-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="a8059-111">يمكن تعيين أبعاد الأخرى لتخطيط التغطية أيضًا.</span><span class="sxs-lookup"><span data-stu-id="a8059-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="a8059-112">ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.</span><span class="sxs-lookup"><span data-stu-id="a8059-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="a8059-113">يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a8059-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="a8059-114">تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:</span><span class="sxs-lookup"><span data-stu-id="a8059-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="a8059-115">تم تعيين المستودع إلى **يدوي‏‎** .</span><span class="sxs-lookup"><span data-stu-id="a8059-115">The warehouse is set to **Manual** .</span></span> <span data-ttu-id="a8059-116">انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات** .</span><span class="sxs-lookup"><span data-stu-id="a8059-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses** .</span></span> <span data-ttu-id="a8059-117">وفي علامة التبويب السريع **التخطيط الرئيسي** ، راجع حقل **الدليل** .</span><span class="sxs-lookup"><span data-stu-id="a8059-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="a8059-118">تحديد تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="a8059-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="a8059-119">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة** .</span><span class="sxs-lookup"><span data-stu-id="a8059-119">Click **Product information management &gt; Products&gt; Released products** .</span></span> <span data-ttu-id="a8059-120">حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة** ، انقر فوق **تغطية الصنف** .</span><span class="sxs-lookup"><span data-stu-id="a8059-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage** .</span></span>
-   <span data-ttu-id="a8059-121">تحديد علاقات إعادة الملء للمستودع.</span><span class="sxs-lookup"><span data-stu-id="a8059-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="a8059-122">انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات** .</span><span class="sxs-lookup"><span data-stu-id="a8059-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses** .</span></span> <span data-ttu-id="a8059-123">وفي علامة التبويب السريع **التخطيط الرئيسي** ، راجع حقل **المستودع الرئيسي** .</span><span class="sxs-lookup"><span data-stu-id="a8059-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="a8059-124">يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان.</span><span class="sxs-lookup"><span data-stu-id="a8059-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="a8059-125">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة** .</span><span class="sxs-lookup"><span data-stu-id="a8059-125">Click **Product information management &gt; Products&gt; Released products** .</span></span> <span data-ttu-id="a8059-126">حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة** ، انقر فوق **إعدادات الأوامر الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="a8059-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings** .</span></span> <span data-ttu-id="a8059-127">وفي نموذج **إعدادات الأوامر الافتراضية** ، راجع **نوع الأمر الافتراضي** .</span><span class="sxs-lookup"><span data-stu-id="a8059-127">In the **Default order settings** form, see the **Default order type** .</span></span>

![طلب تغطية الموقع والمستودع، إلزاميًا](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="a8059-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a8059-129">Additional resources</span></span>
--------

[<span data-ttu-id="a8059-130">نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="a8059-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="a8059-131">التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="a8059-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="a8059-132">التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="a8059-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="a8059-133">التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="a8059-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="a8059-134">تحديد إصدار BOM</span><span class="sxs-lookup"><span data-stu-id="a8059-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



