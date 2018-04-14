--- 
title: "تحديد مجموعات جداول محدودة الفاقد"
description: "يتم تعريف مجموعات الجداول محدودة الفاقد لتجميع المنتجات وتمييزها في جدولة كانبان."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 50435f858524013c3b0e67939bd29ab18b4272b0
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="8ba40-103">تحديد مجموعات جداول محدودة الفاقد</span><span class="sxs-lookup"><span data-stu-id="8ba40-103">Define lean schedule groups</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ba40-104">يتم تعريف مجموعات الجداول محدودة الفاقد لتجميع المنتجات وتمييزها في جدولة كانبان.</span><span class="sxs-lookup"><span data-stu-id="8ba40-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="8ba40-105">يمكن إجراء التجميع كاقتران عامة لكل شركة أو خاصة بخلية عمل.</span><span class="sxs-lookup"><span data-stu-id="8ba40-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="8ba40-106">تحتوي كل مجموعة على رمز ألوان معين للإشارة المرئية في صفحة قوائم جدولة كانبان.</span><span class="sxs-lookup"><span data-stu-id="8ba40-106">Each group has a color code assigned for visual indication in the kanban scheduling list page.</span></span> <span data-ttu-id="8ba40-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="8ba40-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="8ba40-108">تحديد مجموعات الجداول محدودة الفاقد</span><span class="sxs-lookup"><span data-stu-id="8ba40-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="8ba40-109">انتقل إلى إدارة معلومات المنتج > Lean manufacturing > مجموعة الجداول محدودة الفاقد.</span><span class="sxs-lookup"><span data-stu-id="8ba40-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="8ba40-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8ba40-110">Click New.</span></span>
3. <span data-ttu-id="8ba40-111">في الحقل "مجموعة الجداول"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8ba40-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="8ba40-112">يمكن تعريف مجموعة جداول كمجموعة عامة أو خاصة بخلية عمل.</span><span class="sxs-lookup"><span data-stu-id="8ba40-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="8ba40-113">في هذا المثال البسيط، نقوم بتعريف مجموعة عامة ويتم الاحتفاظ بخلية العمل فارغة.</span><span class="sxs-lookup"><span data-stu-id="8ba40-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="8ba40-114">تنطبق إعدادات هذه المجموعة على جميع خلايا العمل التي ليس لديها مجموعات جداول محددة.</span><span class="sxs-lookup"><span data-stu-id="8ba40-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="8ba40-115">حدد لونًا من خيارات تحديد اللون.</span><span class="sxs-lookup"><span data-stu-id="8ba40-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="8ba40-116">يتم استخدام الألوان لتمييز الوظائف على صفحة قائمة جداول كانبان أو لوحة عمليات كانبان.</span><span class="sxs-lookup"><span data-stu-id="8ba40-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="8ba40-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ba40-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8ba40-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ba40-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="8ba40-119">إقران منتج</span><span class="sxs-lookup"><span data-stu-id="8ba40-119">Associate product</span></span>
1. <span data-ttu-id="8ba40-120">إقران منتج معين</span><span class="sxs-lookup"><span data-stu-id="8ba40-120">Associate a specific product</span></span>
    * <span data-ttu-id="8ba40-121">هناك طريقتان لربط المنتجات لمجموعات الجداول محدودة الفاقد، إما كمنتج معين (نوع علاقة الصنف= الصنف) أو كجزء من مفتاح توزيع الصنف (نوع علاقة الصنف = المجموعة).</span><span class="sxs-lookup"><span data-stu-id="8ba40-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="8ba40-122">في الحقل "علاقة نوع الصنف"، حدد "صنف".</span><span class="sxs-lookup"><span data-stu-id="8ba40-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="8ba40-123">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8ba40-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="8ba40-124">في الحقل "معدل الإنتاجية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8ba40-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="8ba40-125">معدل الإنتاجية الافتراضي هو 1، وهو ما يعني أن المنتجات ذات الصلة تستهلك القدرة المحددة في أنشطة العملية لتدفقات الإنتاج تماما.</span><span class="sxs-lookup"><span data-stu-id="8ba40-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activities of the production flows.</span></span> <span data-ttu-id="8ba40-126">يحدد معدل الإنتاجية > 1 استهلاكًا أعلى للموارد، فيما يحدد معدل الإنتاجية< 1 استهلاكًا أقل للموارد.</span><span class="sxs-lookup"><span data-stu-id="8ba40-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="8ba40-127">يتم استخدام النسبة في حساب التكلفة وفي حساب استهلاك وظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="8ba40-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="8ba40-128">إقران مفتاح توزيع صنف</span><span class="sxs-lookup"><span data-stu-id="8ba40-128">Associate item allocation key</span></span>
1. <span data-ttu-id="8ba40-129">إقران مفتاح توزيع صنف</span><span class="sxs-lookup"><span data-stu-id="8ba40-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="8ba40-130">قم بإضافة اقتران لمفتاح توزيع صنف باستخدام مجموعة أنواع علاقة الصنف.</span><span class="sxs-lookup"><span data-stu-id="8ba40-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="8ba40-131">لاحظ أنه بالنسبة لهذه العملية، تحتاج إلى مفتاح تخصيص بند تنبؤ محدد في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8ba40-131">Note that for this process, you need a forecast item allocation key defined in your data.</span></span>  
2. <span data-ttu-id="8ba40-132">في الحقل "نوع علاقة الصنف"، حدد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="8ba40-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="8ba40-133">في الحقل "مفتاح توزيع الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8ba40-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8ba40-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ba40-134">In the list, click the link in the selected row.</span></span>


