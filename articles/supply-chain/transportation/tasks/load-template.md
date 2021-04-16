---
title: قوالب حمل العمل
description: يصف هذا الموضوع كيفية إعداد قوالب حمل وكيفية إقران قالب تحميل بشحنة جديدة.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 175c8017b14cc298cdaa00031f8450015a747786
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831496"
---
# <a name="load-templates"></a><span data-ttu-id="0fb8b-103">قوالب حمل العمل</span><span class="sxs-lookup"><span data-stu-id="0fb8b-103">Load templates</span></span>

<span data-ttu-id="0fb8b-104">عند إنشاء تحميل جديد ، يمكنك تعيين قالب تحميل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="0fb8b-105">يحتوي قالب التحميل علي معلومات حول المعدات ، وحول المقاييس مثل الارتفاع والعرض والعمق وحجم الحمل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="0fb8b-106">يصف هذا الموضوع كيفية إعداد قوالب حمل وكيفية إقران قالب تحميل بشحنة جديدة.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="0fb8b-107">إعداد قالب حمل العمل</span><span class="sxs-lookup"><span data-stu-id="0fb8b-107">Set up a load template</span></span>

1. <span data-ttu-id="0fb8b-108">انتقل إلى **أداره النقل \> إعداد \> بناء التحميل \> قالب التحميل**.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="0fb8b-109">في جزء الاجراء، حدد **جديد** لأضافه قالب جديد **تحرير** لتحرير قالب موجود.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="0fb8b-110">في الصف الخاص بالقالب الجديد أو الموجود ، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="0fb8b-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="0fb8b-111">**معرف قالب التحميل** - إدخال معرف فريد (ID) لقالب التحميل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="0fb8b-112">**المعدات** – تحديد المعدات التي ينبغي استخدامها لشحن الحمل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="0fb8b-113">**ارتفاع التحميل** و **عرض التحميل** و **عمق التحميل** – إدخال ابعاد التحميل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="0fb8b-114">**الحد الأقصى لكميه التحميل** و **الحد الأقصى لوزن الحمل المسموح به** – إدخال الحد الأقصى لحجم الحمل والوزن المسموح به للتحميل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="0fb8b-115">**الحد الأقصى لوزن الإنتاجي المسموح به** – إدخال الحد الأقصى المسموح به لإجمالي وزن الحمل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="0fb8b-116">‏‫الوزن الإجمالي للحمل يشمل كلِ من وزن الفارغ ووزن التحميل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="0fb8b-117">**الحد الأقصى لعدد قطع الشحن المسموح بها** – إدخال الحد الأقصى لعدد أجزاء الشحن التي يمكن ان يحتويها التحميل.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="0fb8b-118">**تحميل المكدس عند الارضيه** – تحديد خانه الاختيار هذه لاستخدام تحميل الارضيه.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="0fb8b-119">في سيناريو التحميل الأرضي يتم تكديس الصناديق من الأرض إلى السقف، من الجدار إلى الجدار المقابل داخل الحاوية لزيادة السعة.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="0fb8b-120">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="0fb8b-121">إقران قالب حمل بحمولة جديدة</span><span class="sxs-lookup"><span data-stu-id="0fb8b-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="0fb8b-122">انتقل إلى **إدارة النقل \> التخطيط \> منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="0fb8b-123">في الجزء العلوي من الصفحة ، حدد أحدي علامات التبويب التالية ، استنادا إلى نوع المستند المصدر الذي تقوم بإنشاء تحميل له: **الشحنات** أو **خطوط المبيعات** أو **بنود التحويل** أو **بنود أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="0fb8b-124">حدد المستند المحدد لتخطيط التحميل له.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="0fb8b-125">في جزء الإجراءات، في علامة التبويب **العرض والطلب**، في مجموعة **إضافة**، حدد **إلى حمل جديد**.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="0fb8b-126">في مربع الحوار **قالب الحمل**، في الحقل **معرف قالب الحمل** حدد القالب المطلوب تطبيقه.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="0fb8b-127">حدد **موافق** لتطبيق القالب.</span><span class="sxs-lookup"><span data-stu-id="0fb8b-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]