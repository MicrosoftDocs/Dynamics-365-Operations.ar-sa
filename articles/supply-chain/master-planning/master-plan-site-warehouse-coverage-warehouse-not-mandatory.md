---
title: التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع غير إلزامي
description: يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. بُعد المستودع غير إلزامي.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34a1a2cec9f86932fe2de9f3886059621903b262
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578162"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="21574-104">التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="21574-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21574-105">يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية.</span><span class="sxs-lookup"><span data-stu-id="21574-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="21574-106">بُعد المستودع غير إلزامي.</span><span class="sxs-lookup"><span data-stu-id="21574-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="21574-107">يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="21574-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="21574-108">تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="21574-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="21574-109">لا يمكن تعديل هذا الإعداد.</span><span class="sxs-lookup"><span data-stu-id="21574-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="21574-110">عدم تعيين بُعد المستودع على إلزامي.</span><span class="sxs-lookup"><span data-stu-id="21574-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="21574-111">فقد يكون المستودع معروفًا، لكنه غير مستخدم في حساب التخططي الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="21574-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="21574-112">تم تعيين الموقع وأبعاد المستودع لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="21574-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="21574-113">يمكن تعيين أبعاد الأخرى لتخطيط التغطية أيضًا.</span><span class="sxs-lookup"><span data-stu-id="21574-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="21574-114">ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.</span><span class="sxs-lookup"><span data-stu-id="21574-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="21574-115">يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="21574-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="21574-116">تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:</span><span class="sxs-lookup"><span data-stu-id="21574-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="21574-117">تم تعيين المستودع إلى يدوي.</span><span class="sxs-lookup"><span data-stu-id="21574-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="21574-118">انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="21574-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="21574-119">وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **الدليل**.</span><span class="sxs-lookup"><span data-stu-id="21574-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="21574-120">تحديد تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="21574-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="21574-121">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="21574-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="21574-122">حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة**، انقر فوق **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="21574-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="21574-123">تحديد علاقات إعادة الملء للمستودع.</span><span class="sxs-lookup"><span data-stu-id="21574-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="21574-124">انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="21574-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="21574-125">وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **المستودع الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="21574-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="21574-126">يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان.</span><span class="sxs-lookup"><span data-stu-id="21574-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="21574-127">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="21574-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="21574-128">حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة**، انقر فوق **إعدادات الأوامر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="21574-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="21574-129">وفي نموذج **إعدادات الأوامر الافتراضية**، راجع **نوع الأمر الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="21574-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![طلب الموقع والمستودع، ليس المستودع](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="21574-131">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="21574-131">Additional resources</span></span>
--------

[<span data-ttu-id="21574-132">التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="21574-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="21574-133">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="21574-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="21574-134">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="21574-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="21574-135">التخطيط الرئيسي - تغطية الموقع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="21574-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="21574-136">التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="21574-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



