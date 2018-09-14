--- 
title: "جرد المخزون في مستودع"
description: "يوضح لك هذا الإجراء عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين بأحد المواقع في المستودع."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="bf5ca-103">جرد المخزون في مستودع</span><span class="sxs-lookup"><span data-stu-id="bf5ca-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf5ca-104">يوضح لك هذا الإجراء عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين بأحد المواقع في المستودع.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="bf5ca-105">وينطبق الإجراء على وظيفة "التخزين الأساسي"، المتوفرة في الوحدة النمطية "إدارة المخزون"، وليس على وظيفة التخزين المتوفرة في الوحدة النمطية "إدارة المستودع".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="bf5ca-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="bf5ca-107">إذا كنت تستخدم البيانات الخاصة بك، فتأكد من إعداد المنتجات والمواقع، وتأكد أنك قد أنشأت اسم دفتر يومية لدفاتر يومية الجرد.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="bf5ca-108">يتم تنفيذ جرد المخزون عادة بواسطة موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="bf5ca-109">إنشاء دفتر يومية جرد مخزون</span><span class="sxs-lookup"><span data-stu-id="bf5ca-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="bf5ca-110">انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > جرد الصنف > الجرد.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="bf5ca-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-111">Click New.</span></span>
3. <span data-ttu-id="bf5ca-112">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bf5ca-113">في القائمة، انقر فوق اسم دفتر يومية جرد المخزون الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="bf5ca-114">سيتم ملء بعض الحقول الأخرى حسب إعداد اسم دفتر يومية جرد المخزون الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="bf5ca-115">في الحقل "العامل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bf5ca-116">في القائمة، حدد العامل الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="bf5ca-117">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-117">Click Select.</span></span>
8. <span data-ttu-id="bf5ca-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="bf5ca-119">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="bf5ca-119">Create journal lines</span></span>
1. <span data-ttu-id="bf5ca-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-120">Click New.</span></span>
2. <span data-ttu-id="bf5ca-121">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bf5ca-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bf5ca-123">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "A0001".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="bf5ca-124">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bf5ca-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bf5ca-126">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "الموقع 2".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="bf5ca-127">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bf5ca-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bf5ca-129">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "المستودع 24".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="bf5ca-130">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="bf5ca-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bf5ca-132">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "مجمع-001".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="bf5ca-133">في الحقل "تم جرده"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="bf5ca-134">إذا أدخلتَ عددًا محسوبًا يختلف عن العدد الذي يظهر في الحقل "الكمية المتاحة"، سيتم تحديث الحقل "الكمية" لإظهار التباين.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="bf5ca-135">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="bf5ca-136">ترحيل دفتر يومية جرد المخزون</span><span class="sxs-lookup"><span data-stu-id="bf5ca-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="bf5ca-137">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-137">Click Post.</span></span>
    * <span data-ttu-id="bf5ca-138">عند ترحيل دفتر يومية جرد مخزون، إذا كان المبلغ المحسوب يختلف عن المبلغ الذي تم الإعلام عنه في الحقل "الكمية المتاحة"، سيتم ترحيل استلام مخزون أو إصداره وتغيير مستوى المخزون وقيمته وإنشاء حركات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="bf5ca-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="bf5ca-140">عرض حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="bf5ca-140">View inventory transactions</span></span>
1. <span data-ttu-id="bf5ca-141">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-141">Click Inventory.</span></span>
2. <span data-ttu-id="bf5ca-142">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="bf5ca-142">Click Transactions.</span></span>
    * <span data-ttu-id="bf5ca-143">هنا يمكنك أن ترى أي حركات ذات صلة سيتم إنشاؤها عند ترحيل دفتر يومية جرد المخزون الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="bf5ca-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   


