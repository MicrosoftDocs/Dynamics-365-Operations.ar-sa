---
title: ضبط مستويات المخزون في المستودع (التخزين الأساسي)
description: يوضح لك هذا الإجراء عملية إنشاء دفتر يومية تعديل مخزون وترحيله لضبط مستويات المخزون من المنتجات في المستودع.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c617517109146b96075d03b6f3549639a99d7d1c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146067"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="10137-103">ضبط مستويات المخزون في المستودع (التخزين الأساسي)</span><span class="sxs-lookup"><span data-stu-id="10137-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10137-104">يوضح لك هذا الإجراء عملية إنشاء دفتر يومية تعديل مخزون وترحيله لضبط مستويات المخزون من المنتجات في المستودع.</span><span class="sxs-lookup"><span data-stu-id="10137-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="10137-105">يجب أن يكون لديك اسم دفتر يومية مخزون تم إعداده لعمليات تعديل المخزون قبل البدء في هذا.</span><span class="sxs-lookup"><span data-stu-id="10137-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="10137-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="10137-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="10137-107">وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="10137-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="10137-108">إنشاء دفتر يومية تعديل مخزون</span><span class="sxs-lookup"><span data-stu-id="10137-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="10137-109">انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > الأصناف > تعديل المخزون.</span><span class="sxs-lookup"><span data-stu-id="10137-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="10137-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="10137-110">Click New.</span></span>
3. <span data-ttu-id="10137-111">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10137-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="10137-112">في القائمة، انقر فوق اسم دفتر يومية تعديل المخزون الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="10137-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="10137-113">سيتم ملء بعض الحقول الأخرى حسب إعداد اسم دفتر يومية تعديل المخزون الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="10137-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="10137-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10137-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="10137-115">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="10137-115">Create journal lines</span></span>
1. <span data-ttu-id="10137-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="10137-116">Click New.</span></span>
2. <span data-ttu-id="10137-117">في القائمة، ضع علامة على حقل "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="10137-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="10137-118">في الحقل "رقم الصنف"، حدد أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="10137-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="10137-119">إذا كنت تستخدم شركة بيانات العرض التقديمي USMF، فاكتب "D0001".</span><span class="sxs-lookup"><span data-stu-id="10137-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="10137-120">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10137-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="10137-121">في القائمة، حدد أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="10137-121">In the list, select a site.</span></span>
6. <span data-ttu-id="10137-122">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10137-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="10137-123">في القائمة، حدد مستودعًا.</span><span class="sxs-lookup"><span data-stu-id="10137-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="10137-124">إذا قمت بتحديد صنف باستخدام الموقع كبعد إلزامي، فقد تضطر إلى تحديد الموقع هنا.</span><span class="sxs-lookup"><span data-stu-id="10137-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="10137-125">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="10137-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="10137-126">يحدد الحقل "سعر التكلفة" التكلفة لكل وحدة بالنسبة لعمليات استلام المخزون.</span><span class="sxs-lookup"><span data-stu-id="10137-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="10137-127">وإذا لم يتم تحديد التكلفة لرقم الصنف أو إذا أردتَ تغييرها تلقائيًا، يمكنك تغييرها هنا.</span><span class="sxs-lookup"><span data-stu-id="10137-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="10137-128">التحقق من صحة دفتر يومية تعديل المخزون وترحيله</span><span class="sxs-lookup"><span data-stu-id="10137-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="10137-129">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="10137-129">Click Validate.</span></span>
2. <span data-ttu-id="10137-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10137-130">Click OK.</span></span>
3. <span data-ttu-id="10137-131">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="10137-131">Click Post.</span></span>
    * <span data-ttu-id="10137-132">عندما تقوم بترحيل هذا النوع من دفاتر اليومية، سيتم ترحيل استلام مخزون أو إصدار مخزون وسيتم تغيير مستوى المخزون وقيمته وسيتم إنشاء حركات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="10137-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="10137-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10137-133">Click OK.</span></span>
5. <span data-ttu-id="10137-134">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="10137-134">Close the form.</span></span>
6. <span data-ttu-id="10137-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10137-135">Close the page.</span></span>

