--- 
title: "تخطيط الأحمال والشحنات باستخدام ‏‫منضدة عمل تخطيط الحِمل"
description: "يوضح هذا الإجراء كيفية استخدام منضدة تخطيط الحمل لإنشاء حمل لأمر مبيعات."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="d016a-103">تخطيط الأحمال والشحنات باستخدام ‏‫منضدة عمل تخطيط الحِمل</span><span class="sxs-lookup"><span data-stu-id="d016a-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d016a-104">يوضح هذا الإجراء كيفية استخدام منضدة تخطيط الحمل لإنشاء حمل لأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="d016a-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="d016a-105">كشرط مسبق، سنقوم بإنشاء أمر المبيعات أولاً.</span><span class="sxs-lookup"><span data-stu-id="d016a-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="d016a-106">يمثل هذا الإجراء جزءًا من العمل اليومي لمنسق النقل.</span><span class="sxs-lookup"><span data-stu-id="d016a-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="d016a-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="d016a-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="d016a-108">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="d016a-108">Create a sales order</span></span>
1. <span data-ttu-id="d016a-109">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d016a-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d016a-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d016a-110">Click New.</span></span>
3. <span data-ttu-id="d016a-111">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d016a-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d016a-112">حدد الحساب الولايات المتحدة-004.</span><span class="sxs-lookup"><span data-stu-id="d016a-112">Select account US-004.</span></span>
5. <span data-ttu-id="d016a-113">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d016a-113">Click OK.</span></span>
6. <span data-ttu-id="d016a-114">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d016a-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d016a-115">حدد الصنف A0001.</span><span class="sxs-lookup"><span data-stu-id="d016a-115">Select item A0001.</span></span>
    * <span data-ttu-id="d016a-116">تم تمكين A0001 لإدارة النقل.</span><span class="sxs-lookup"><span data-stu-id="d016a-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="d016a-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d016a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d016a-118">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d016a-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="d016a-119">في الحقل "المستودع"، اكتب "24".</span><span class="sxs-lookup"><span data-stu-id="d016a-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="d016a-120">في هذا المثال حدد المستودع 24.</span><span class="sxs-lookup"><span data-stu-id="d016a-120">In this example select warehouse 24.</span></span> <span data-ttu-id="d016a-121">يتم تمكين هذا المستودع لإدارة النقل وإدارة المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="d016a-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="d016a-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d016a-122">Click Save.</span></span>
12. <span data-ttu-id="d016a-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d016a-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="d016a-124">إنشاء حمل جديد</span><span class="sxs-lookup"><span data-stu-id="d016a-124">Create a new load</span></span>
1. <span data-ttu-id="d016a-125">انتقل إلى إدارة النقل > التخطيط > منضدة عمل تخطيط الحِمل‬.</span><span class="sxs-lookup"><span data-stu-id="d016a-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="d016a-126">انقر فوق علامة التبويب "بنود المبيعات".</span><span class="sxs-lookup"><span data-stu-id="d016a-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="d016a-127">والآن سوف تقوم بإنشاء التحميل الخاص بأمر المبيعات الذي قمت بإنشائه للتو.</span><span class="sxs-lookup"><span data-stu-id="d016a-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="d016a-128">يمكنك إنشاء الحمولات استناداً على العرض والطلب من أوامر الشراء وأوامر التحويل وأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d016a-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="d016a-129">في الجزء "الإجراءات"، انقر فوق "العرض والطلب".</span><span class="sxs-lookup"><span data-stu-id="d016a-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="d016a-130">انقر فوق "إلى حمل جديد".</span><span class="sxs-lookup"><span data-stu-id="d016a-130">Click To new load.</span></span>
5. <span data-ttu-id="d016a-131">في الحقل "معرف قالب الحمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d016a-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d016a-132">يحدد قالب التحميل القياسات القصوى للوزن والحجم للتحميل بالكامل.</span><span class="sxs-lookup"><span data-stu-id="d016a-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="d016a-133">على سبيل المثال، قد يمثل قالب تحميل حجم الحاوية أو الشاحنة.</span><span class="sxs-lookup"><span data-stu-id="d016a-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="d016a-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d016a-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d016a-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d016a-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="d016a-136">تقييم الحمل وتوجيهه</span><span class="sxs-lookup"><span data-stu-id="d016a-136">Rate and route the load</span></span>
1. <span data-ttu-id="d016a-137">انقر فوق "التقييم والتوجيه".</span><span class="sxs-lookup"><span data-stu-id="d016a-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="d016a-138">انقر فوق "تقييم منضدة عمل المسار".</span><span class="sxs-lookup"><span data-stu-id="d016a-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="d016a-139">انقر فوق "تقييم المتجر".</span><span class="sxs-lookup"><span data-stu-id="d016a-139">Click Rate shop.</span></span>
4. <span data-ttu-id="d016a-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d016a-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d016a-141">انقر فوق "تعيين".</span><span class="sxs-lookup"><span data-stu-id="d016a-141">Click Assign.</span></span>
6. <span data-ttu-id="d016a-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d016a-142">Close the page.</span></span>
7. <span data-ttu-id="d016a-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d016a-143">Close the page.</span></span>


