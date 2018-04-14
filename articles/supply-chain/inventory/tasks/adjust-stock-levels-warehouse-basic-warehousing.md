---
title: "ضبط مستويات المخزون في المستودع (التخزين الأساسي)"
description: "يوضح لك هذا الإجراء عملية إنشاء دفتر يومية تعديل مخزون وترحيله لضبط مستويات المخزون من المنتجات في المستودع."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 84ed2bfa708664674af781c575cfab35640e7079
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="96566-103">ضبط مستويات المخزون في المستودع (التخزين الأساسي)</span><span class="sxs-lookup"><span data-stu-id="96566-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96566-104">يوضح لك هذا الإجراء عملية إنشاء دفتر يومية تعديل مخزون وترحيله لضبط مستويات المخزون من المنتجات في المستودع.</span><span class="sxs-lookup"><span data-stu-id="96566-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="96566-105">يجب أن يكون لديك اسم دفتر يومية مخزون تم إعداده لعمليات تعديل المخزون قبل البدء في هذا.</span><span class="sxs-lookup"><span data-stu-id="96566-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="96566-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="96566-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="96566-107">وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="96566-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="96566-108">إنشاء دفتر يومية تعديل مخزون</span><span class="sxs-lookup"><span data-stu-id="96566-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="96566-109">انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > الأصناف > تعديل المخزون.</span><span class="sxs-lookup"><span data-stu-id="96566-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="96566-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="96566-110">Click New.</span></span>
3. <span data-ttu-id="96566-111">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="96566-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="96566-112">في القائمة، انقر فوق اسم دفتر يومية تعديل المخزون الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="96566-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="96566-113">سيتم ملء بعض الحقول الأخرى حسب إعداد اسم دفتر يومية تعديل المخزون الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="96566-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="96566-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="96566-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="96566-115">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="96566-115">Create journal lines</span></span>
1. <span data-ttu-id="96566-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="96566-116">Click New.</span></span>
2. <span data-ttu-id="96566-117">في القائمة، ضع علامة على حقل "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="96566-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="96566-118">في الحقل "رقم الصنف"، حدد أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="96566-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="96566-119">إذا كنت تستخدم شركة بيانات العرض التقديمي USMF، فاكتب "D0001".</span><span class="sxs-lookup"><span data-stu-id="96566-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="96566-120">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="96566-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="96566-121">في القائمة، حدد أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="96566-121">In the list, select a site.</span></span>
6. <span data-ttu-id="96566-122">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="96566-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="96566-123">في القائمة، حدد مستودعًا.</span><span class="sxs-lookup"><span data-stu-id="96566-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="96566-124">إذا قمت بتحديد صنف باستخدام الموقع كبعد إلزامي، فقد تضطر إلى تحديد الموقع هنا.</span><span class="sxs-lookup"><span data-stu-id="96566-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="96566-125">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="96566-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="96566-126">يحدد الحقل "سعر التكلفة" التكلفة لكل وحدة بالنسبة لعمليات استلام المخزون.</span><span class="sxs-lookup"><span data-stu-id="96566-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="96566-127">وإذا لم يتم تحديد التكلفة لرقم الصنف أو إذا أردتَ تغييرها تلقائيًا، يمكنك تغييرها هنا.</span><span class="sxs-lookup"><span data-stu-id="96566-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="96566-128">التحقق من صحة دفتر يومية تعديل المخزون وترحيله</span><span class="sxs-lookup"><span data-stu-id="96566-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="96566-129">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="96566-129">Click Validate.</span></span>
2. <span data-ttu-id="96566-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="96566-130">Click OK.</span></span>
3. <span data-ttu-id="96566-131">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="96566-131">Click Post.</span></span>
    * <span data-ttu-id="96566-132">عندما تقوم بترحيل هذا النوع من دفاتر اليومية، سيتم ترحيل استلام مخزون أو إصدار مخزون وسيتم تغيير مستوى المخزون وقيمته وسيتم إنشاء حركات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="96566-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="96566-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="96566-133">Click OK.</span></span>
5. <span data-ttu-id="96566-134">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="96566-134">Close the form.</span></span>
6. <span data-ttu-id="96566-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="96566-135">Close the page.</span></span>

