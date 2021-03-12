---
title: التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي
description: يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية.
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe5cb5f9d21afcd12f3041bb9acc89fff360c95e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970446"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="7aa2c-103">التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="7aa2c-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7aa2c-104">يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="7aa2c-105">يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="7aa2c-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="7aa2c-106">تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="7aa2c-107">عدم تعيين بُعد المستودع على إلزامي.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="7aa2c-108">فقد يكون المستودع معروفًا، لكنه غير مستخدم في حساب التخططي الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="7aa2c-109">تعيين بُعد الموقع لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="7aa2c-110">عدم تعيين بُعد المستودع لتخطيط التغطية.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="7aa2c-111">ولذلك يتم تجميع العرض والطلب حسب الموقع، وربما حسب الأبعاد الأخرى المخططة في التغطية أيضا.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="7aa2c-112">يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="7aa2c-113">تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:</span><span class="sxs-lookup"><span data-stu-id="7aa2c-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="7aa2c-114">تحديد تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="7aa2c-115">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="7aa2c-116">حدد الصنف، ثم انقر فوق **خطة &gt; تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="7aa2c-117">تحديد علاقات إعادة الملء للمستودع.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="7aa2c-118">انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="7aa2c-119">وفي علامة التبويب **التخطيط الرئيسي**، راجع مجموعة حقل **المستودع الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="7aa2c-120">يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="7aa2c-121">انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="7aa2c-122">حدد الصنف، ثم انقر فوق **خطة &gt; إعدادات الأوامر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="7aa2c-123">وفي نموذج **إعدادات الأوامر الافتراضية**، راجع حقل **نوع الأمر الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="7aa2c-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![طلب مستودع تغطية الموقع ليس إلزاميًا    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="7aa2c-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7aa2c-125">Additional resources</span></span>
--------

[<span data-ttu-id="7aa2c-126">نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="7aa2c-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="7aa2c-127">التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="7aa2c-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="7aa2c-128">التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="7aa2c-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="7aa2c-129">التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="7aa2c-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="7aa2c-130">تحديد إصدار BOM</span><span class="sxs-lookup"><span data-stu-id="7aa2c-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



