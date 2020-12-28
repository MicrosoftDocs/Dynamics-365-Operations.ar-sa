---
title: قوالب حمل العمل
description: يصف هذا الموضوع كيفية إعداد قوالب حمل وكيفية إقران قالب تحميل بشحنة جديدة.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646356"
---
# <a name="load-templates"></a><span data-ttu-id="6cf69-103">قوالب حمل العمل</span><span class="sxs-lookup"><span data-stu-id="6cf69-103">Load templates</span></span>

<span data-ttu-id="6cf69-104">عند إنشاء تحميل جديد ، يمكنك تعيين قالب تحميل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="6cf69-105">يحتوي قالب التحميل علي معلومات حول المعدات ، وحول المقاييس مثل الارتفاع والعرض والعمق وحجم الحمل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="6cf69-106">يصف هذا الموضوع كيفية إعداد قوالب حمل وكيفية إقران قالب تحميل بشحنة جديدة.</span><span class="sxs-lookup"><span data-stu-id="6cf69-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="6cf69-107">إعداد قالب حمل العمل</span><span class="sxs-lookup"><span data-stu-id="6cf69-107">Set up a load template</span></span>

1. <span data-ttu-id="6cf69-108">انتقل إلى **أداره النقل \> إعداد \> بناء التحميل \> قالب التحميل**.</span><span class="sxs-lookup"><span data-stu-id="6cf69-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="6cf69-109">في جزء الاجراء، حدد **جديد** لأضافه قالب جديد **تحرير** لتحرير قالب موجود.</span><span class="sxs-lookup"><span data-stu-id="6cf69-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="6cf69-110">في الصف الخاص بالقالب الجديد أو الموجود ، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="6cf69-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="6cf69-111">**معرف قالب التحميل** - إدخال معرف فريد (ID) لقالب التحميل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="6cf69-112">**المعدات** – تحديد المعدات التي ينبغي استخدامها لشحن الحمل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="6cf69-113">**ارتفاع التحميل** و **عرض التحميل** و **عمق التحميل** – إدخال ابعاد التحميل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="6cf69-114">**الحد الأقصى لكميه التحميل** و **الحد الأقصى لوزن الحمل المسموح به** – إدخال الحد الأقصى لحجم الحمل والوزن المسموح به للتحميل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="6cf69-115">**الحد الأقصى لوزن الإنتاجي المسموح به** – إدخال الحد الأقصى المسموح به لإجمالي وزن الحمل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="6cf69-116">‏‫الوزن الإجمالي للحمل يشمل كلِ من وزن الفارغ ووزن التحميل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="6cf69-117">**الحد الأقصى لعدد قطع الشحن المسموح بها** – إدخال الحد الأقصى لعدد أجزاء الشحن التي يمكن ان يحتويها التحميل.</span><span class="sxs-lookup"><span data-stu-id="6cf69-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="6cf69-118">**تحميل المكدس عند الارضيه** – تحديد خانه الاختيار هذه لاستخدام تحميل الارضيه.</span><span class="sxs-lookup"><span data-stu-id="6cf69-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="6cf69-119">في سيناريو التحميل الأرضي يتم تكديس الصناديق من الأرض إلى السقف، من الجدار إلى الجدار المقابل داخل الحاوية لزيادة السعة.</span><span class="sxs-lookup"><span data-stu-id="6cf69-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="6cf69-120">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="6cf69-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="6cf69-121">إقران قالب حمل بحمولة جديدة</span><span class="sxs-lookup"><span data-stu-id="6cf69-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="6cf69-122">انتقل إلى **إدارة النقل \> التخطيط \> منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="6cf69-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="6cf69-123">في الجزء العلوي من الصفحة ، حدد أحدي علامات التبويب التالية ، استنادا إلى نوع المستند المصدر الذي تقوم بإنشاء تحميل له: **الشحنات** أو **خطوط المبيعات** أو **بنود التحويل** أو **بنود أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="6cf69-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="6cf69-124">حدد المستند المحدد لتخطيط التحميل له.</span><span class="sxs-lookup"><span data-stu-id="6cf69-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="6cf69-125">في جزء الإجراءات، في علامة التبويب **العرض والطلب**، في مجموعة **إضافة**، حدد **إلى حمل جديد**.</span><span class="sxs-lookup"><span data-stu-id="6cf69-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="6cf69-126">في مربع الحوار **قالب الحمل**، في الحقل **معرف قالب الحمل** حدد القالب المطلوب تطبيقه.</span><span class="sxs-lookup"><span data-stu-id="6cf69-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="6cf69-127">حدد **موافق** لتطبيق القالب.</span><span class="sxs-lookup"><span data-stu-id="6cf69-127">Select **OK** to apply the template.</span></span>
