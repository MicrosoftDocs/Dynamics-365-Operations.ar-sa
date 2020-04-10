---
title: جرد المخزون في مستودع
description: يصف هذا الموضوع عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين في موقع في المستودع.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e9457074b696efaf5958b3a3b4616f06f5a6ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145745"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="0b131-103">جرد المخزون في مستودع</span><span class="sxs-lookup"><span data-stu-id="0b131-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b131-104">يصف هذا الموضوع عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين في موقع في المستودع.</span><span class="sxs-lookup"><span data-stu-id="0b131-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="0b131-105">وينطبق الإجراء على وظيفة "التخزين الأساسي"، المتوفرة في الوحدة النمطية "إدارة المخزون"، وليس على وظيفة التخزين المتوفرة في الوحدة النمطية "إدارة المستودع".</span><span class="sxs-lookup"><span data-stu-id="0b131-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="0b131-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0b131-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0b131-107">إذا كنت تستخدم البيانات الخاصة بك، فتأكد من إعداد المنتجات والمواقع، وتأكد أنك قد أنشأت اسم دفتر يومية لدفاتر يومية الجرد.</span><span class="sxs-lookup"><span data-stu-id="0b131-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="0b131-108">يتم تنفيذ جرد المخزون عادة بواسطة موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="0b131-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="0b131-109">إنشاء دفتر يومية جرد مخزون</span><span class="sxs-lookup"><span data-stu-id="0b131-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="0b131-110">انتقل إلى **جزء التنقل > الوحدات النمطية > > إدارة المخزون > إدخالات دفتر اليومية > جرد الصنف > الجرد**.</span><span class="sxs-lookup"><span data-stu-id="0b131-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="0b131-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0b131-111">Select **New**.</span></span>
3. <span data-ttu-id="0b131-112">في حقل **الاسم**، حدد اسم دفتر يومية جرد المخزون الذي تريد استخدامه من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0b131-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="0b131-113">سيتم ملء بعض الحقول الأخرى حسب إعداد اسم دفتر يومية جرد المخزون الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="0b131-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="0b131-114">في الحقل **العامل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b131-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0b131-115">في القائمة، **حدد** العامل الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="0b131-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="0b131-116">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0b131-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="0b131-117">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="0b131-117">Create journal lines</span></span>
1. <span data-ttu-id="0b131-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0b131-118">Select **New**.</span></span>
2. <span data-ttu-id="0b131-119">في الحقل **رقم الصنف**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0b131-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="0b131-120">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد **A0001**.</span><span class="sxs-lookup"><span data-stu-id="0b131-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="0b131-121">في الحقل **الموقع**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0b131-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="0b131-122">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد الموقع **2**.</span><span class="sxs-lookup"><span data-stu-id="0b131-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="0b131-123">في الحقل **المستودع**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0b131-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="0b131-124">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد المستودع **24**.</span><span class="sxs-lookup"><span data-stu-id="0b131-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="0b131-125">في الحقل **الموقع**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0b131-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="0b131-126">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="0b131-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="0b131-127">في الحقل "تم جرده"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0b131-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="0b131-128">إذا أدخلتَ عددًا محسوبًا يختلف عن العدد الذي يظهر في الحقل **الكمية المتاحة**، سيتم تحديث الحقل **الكمية** لإظهار التباين.</span><span class="sxs-lookup"><span data-stu-id="0b131-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="0b131-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0b131-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="0b131-130">ترحيل دفتر يومية جرد المخزون</span><span class="sxs-lookup"><span data-stu-id="0b131-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="0b131-131">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="0b131-131">Select **Post**.</span></span> <span data-ttu-id="0b131-132">عند ترحيل دفتر يومية جرد مخزون، إذا كان المبلغ المحسوب يختلف عن المبلغ الذي تم الإعلام عنه في الحقل **الكمية المتاحة**، سيتم ترحيل استلام مخزون أو إصداره وتغيير مستوى المخزون وقيمته وإنشاء حركات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="0b131-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="0b131-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0b131-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="0b131-134">عرض حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="0b131-134">View inventory transactions</span></span>
1. <span data-ttu-id="0b131-135">حدد **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="0b131-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="0b131-136">حدد **الحركات**.</span><span class="sxs-lookup"><span data-stu-id="0b131-136">Select **Transactions**.</span></span> <span data-ttu-id="0b131-137">هنا يمكنك أن ترى أي حركات ذات صلة سيتم إنشاؤها عند ترحيل دفتر يومية جرد المخزون الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="0b131-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

