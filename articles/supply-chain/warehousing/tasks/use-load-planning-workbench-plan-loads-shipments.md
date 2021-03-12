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
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976803"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="e3a79-103">تخطيط الأحمال والشحنات باستخدام أداة تخطيط الحِمل</span><span class="sxs-lookup"><span data-stu-id="e3a79-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3a79-104">يوضح هذا الموضوع كيفية استخدام منضدة تخطيط الحمل لإنشاء حمل لأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e3a79-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="e3a79-105">كشرط مسبق، سنقوم بإنشاء أمر المبيعات أولاً.</span><span class="sxs-lookup"><span data-stu-id="e3a79-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="e3a79-106">يمثل هذا الإجراء جزءًا من العمل اليومي لمنسق النقل.</span><span class="sxs-lookup"><span data-stu-id="e3a79-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="e3a79-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e3a79-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="e3a79-108">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="e3a79-108">Create a sales order</span></span>
1. <span data-ttu-id="e3a79-109">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الأوامر > كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="e3a79-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-110">Select **New**.</span></span>
3. <span data-ttu-id="e3a79-111">في الحقل **حساب العميل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e3a79-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e3a79-112">حدد الحساب **US-004**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="e3a79-113">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-113">Select **OK**.</span></span>
6. <span data-ttu-id="e3a79-114">في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e3a79-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e3a79-115">حدد الصنف **A0001**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-115">Select item **A0001**.</span></span> <span data-ttu-id="e3a79-116">تم تمكين **A0001** لإدارة النقل.</span><span class="sxs-lookup"><span data-stu-id="e3a79-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="e3a79-117">في الحقل **الموقع**، حدد زر القائمة المنسدلة لفتح البحث، ثم حدد صنفًا.</span><span class="sxs-lookup"><span data-stu-id="e3a79-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="e3a79-118">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e3a79-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="e3a79-119">في حقل **المستودع**، اكتب "24" لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="e3a79-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="e3a79-120">يتم تمكين هذا المستودع لإدارة النقل وإدارة المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="e3a79-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="e3a79-121">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-121">Select **Save**.</span></span>
12. <span data-ttu-id="e3a79-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e3a79-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="e3a79-123">إنشاء حمل جديد</span><span class="sxs-lookup"><span data-stu-id="e3a79-123">Create a new load</span></span>
1. <span data-ttu-id="e3a79-124">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النقل > التخطيط > منضدة عمل تخطيط الحمل**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="e3a79-125">حدد علامة التبويب **بنود المبيعات**. والآن سوف تنشئ حمل عمل أمر المبيعات الذي أنشـه للتو.</span><span class="sxs-lookup"><span data-stu-id="e3a79-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="e3a79-126">يمكنك إنشاء الحمولات استناداً على العرض والطلب من أوامر الشراء وأوامر التحويل وأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e3a79-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="e3a79-127">في جزء الإجراءات، حدد **العرض والطلب**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="e3a79-128">حدد **إلى حمل عمل جديد**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-128">Select **To new load**.</span></span>
5. <span data-ttu-id="e3a79-129">في الحقل **معرف قالب الحمل**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e3a79-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="e3a79-130">يحدد قالب التحميل القياسات القصوى للوزن والحجم للتحميل بالكامل.</span><span class="sxs-lookup"><span data-stu-id="e3a79-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="e3a79-131">على سبيل المثال، قد يمثل قالب تحميل حجم الحاوية أو الشاحنة.</span><span class="sxs-lookup"><span data-stu-id="e3a79-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="e3a79-132">حدد صنفًا.</span><span class="sxs-lookup"><span data-stu-id="e3a79-132">Select an item.</span></span>
6. <span data-ttu-id="e3a79-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="e3a79-134">تقييم الحمل وتوجيهه</span><span class="sxs-lookup"><span data-stu-id="e3a79-134">Rate and route the load</span></span>
1. <span data-ttu-id="e3a79-135">حدد **التقييم والتوجيه‬**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="e3a79-136">حدد **منضدة عمل مسار الأسعار‬**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="e3a79-137">حدد **سعر المتجر‬**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="e3a79-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e3a79-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e3a79-139">حدد **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="e3a79-139">Select **Assign**.</span></span>
6. <span data-ttu-id="e3a79-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e3a79-140">Close the page.</span></span>

