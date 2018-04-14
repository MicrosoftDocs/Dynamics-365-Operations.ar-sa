---
title: "التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي"
description: "يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية. يُعد المستودع بُعدًا إلزاميًا."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fcfdbf8cdc6aae7f82ba308d450b754d652ac699
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="712ac-104">التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="712ac-104">Master planning for site coverage, mandatory warehouse</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="712ac-105">يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية.</span><span class="sxs-lookup"><span data-stu-id="712ac-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="712ac-106">يُعد المستودع بُعدًا إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="712ac-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="712ac-107">يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="712ac-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="712ac-108">تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="712ac-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="712ac-109">لا يمكن تعديل هذا الإعداد.</span><span class="sxs-lookup"><span data-stu-id="712ac-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="712ac-110">تم تعيين بُعد المستودع على إلزامي ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="712ac-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="712ac-111">تعيين بُعد الموقع لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="712ac-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="712ac-112">ويمكن تعيين أبعاد أخرى لتخطيط التغطية أيضًا.</span><span class="sxs-lookup"><span data-stu-id="712ac-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="712ac-113">ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.</span><span class="sxs-lookup"><span data-stu-id="712ac-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="712ac-114">عدم تعيين بُعد المستودع لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="712ac-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="712ac-115">ولذلك يتم تجميع العرض والطلب حسب الموقع، وربما حسب الأبعاد الأخرى المخططة في التغطية أيضا.</span><span class="sxs-lookup"><span data-stu-id="712ac-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="712ac-116">يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="712ac-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="712ac-117">تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:</span><span class="sxs-lookup"><span data-stu-id="712ac-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="712ac-118">تحديد تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="712ac-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="712ac-119">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="712ac-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="712ac-120">حدد الصنف، ثم انقر فوق **خطة &gt; تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="712ac-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="712ac-121">تحديد علاقات إعادة الملء للمستودع.</span><span class="sxs-lookup"><span data-stu-id="712ac-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="712ac-122">انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="712ac-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="712ac-123">وفي علامة التبويب **التخطيط الرئيسي**، راجع مجموعة حقل **المستودع الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="712ac-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="712ac-124">يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان.</span><span class="sxs-lookup"><span data-stu-id="712ac-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="712ac-125">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="712ac-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="712ac-126">حدد الصنف، ثم انقر فوق **خطة &gt; إعدادات الأوامر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="712ac-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="712ac-127">وفي نموذج **إعدادات الأوامر الافتراضية**، راجع **نوع الأمر الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="712ac-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![طلب مستودع تغطية الموقع إلزاميًا](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="712ac-129">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="712ac-129">See also</span></span>
--------

[<span data-ttu-id="712ac-130">التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="712ac-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="712ac-131">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="712ac-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="712ac-132">التخطيط الرئيسي - تغطية الموقع. المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="712ac-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="712ac-133">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="712ac-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="712ac-134">التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="712ac-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




