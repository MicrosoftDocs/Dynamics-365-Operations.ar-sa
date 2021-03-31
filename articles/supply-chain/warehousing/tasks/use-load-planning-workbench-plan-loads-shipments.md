---
title: تخطيط الأحمال والشحنات باستخدام أداة تخطيط الحِمل
description: يوضح هذا الموضوع كيفية استخدام منضدة تخطيط الحمل لإنشاء حمل لأمر مبيعات.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 277b91944d8f7ee79bed9b85ee6ebd275e72c75b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223280"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="e4e5a-103">تخطيط الأحمال والشحنات باستخدام أداة تخطيط الحِمل</span><span class="sxs-lookup"><span data-stu-id="e4e5a-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4e5a-104">يوضح هذا الموضوع كيفية استخدام منضدة تخطيط الحمل لإنشاء حمل لأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="e4e5a-105">كشرط مسبق، سنقوم بإنشاء أمر المبيعات أولاً.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="e4e5a-106">يمثل هذا الإجراء جزءًا من العمل اليومي لمنسق النقل.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="e4e5a-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="e4e5a-108">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="e4e5a-108">Create a sales order</span></span>
1. <span data-ttu-id="e4e5a-109">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الأوامر > كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="e4e5a-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-110">Select **New**.</span></span>
3. <span data-ttu-id="e4e5a-111">في الحقل **حساب العميل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e4e5a-112">حدد الحساب **US-004**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="e4e5a-113">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-113">Select **OK**.</span></span>
6. <span data-ttu-id="e4e5a-114">في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e4e5a-115">حدد الصنف **A0001**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-115">Select item **A0001**.</span></span> <span data-ttu-id="e4e5a-116">تم تمكين **A0001** لإدارة النقل.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="e4e5a-117">في الحقل **الموقع**، حدد زر القائمة المنسدلة لفتح البحث، ثم حدد صنفًا.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="e4e5a-118">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="e4e5a-119">في حقل **المستودع**، اكتب "24" لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="e4e5a-120">يتم تمكين هذا المستودع لإدارة النقل وإدارة المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="e4e5a-121">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-121">Select **Save**.</span></span>
12. <span data-ttu-id="e4e5a-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="e4e5a-123">إنشاء حمل جديد</span><span class="sxs-lookup"><span data-stu-id="e4e5a-123">Create a new load</span></span>
1. <span data-ttu-id="e4e5a-124">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النقل > التخطيط > منضدة عمل تخطيط الحمل**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="e4e5a-125">حدد علامة التبويب **بنود المبيعات**. والآن سوف تنشئ حمل عمل أمر المبيعات الذي أنشـه للتو.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="e4e5a-126">يمكنك إنشاء الحمولات استناداً على العرض والطلب من أوامر الشراء وأوامر التحويل وأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="e4e5a-127">في جزء الإجراءات، حدد **العرض والطلب**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="e4e5a-128">حدد **إلى حمل عمل جديد**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-128">Select **To new load**.</span></span>
5. <span data-ttu-id="e4e5a-129">في الحقل **معرف قالب الحمل**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="e4e5a-130">يحدد قالب التحميل القياسات القصوى للوزن والحجم للتحميل بالكامل.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="e4e5a-131">على سبيل المثال، قد يمثل قالب تحميل حجم الحاوية أو الشاحنة.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="e4e5a-132">حدد صنفًا.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-132">Select an item.</span></span>
6. <span data-ttu-id="e4e5a-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="e4e5a-134">تقييم الحمل وتوجيهه</span><span class="sxs-lookup"><span data-stu-id="e4e5a-134">Rate and route the load</span></span>
1. <span data-ttu-id="e4e5a-135">حدد **التقييم والتوجيه‬**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="e4e5a-136">حدد **منضدة عمل مسار الأسعار‬**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="e4e5a-137">حدد **سعر المتجر‬**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="e4e5a-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e4e5a-139">حدد **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-139">Select **Assign**.</span></span>
6. <span data-ttu-id="e4e5a-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]