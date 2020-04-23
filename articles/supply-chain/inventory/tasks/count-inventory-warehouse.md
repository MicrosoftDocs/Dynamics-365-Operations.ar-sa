---
title: جرد المخزون في مستودع
description: يصف هذا الموضوع عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين في موقع في المستودع.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204161"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="b327b-103">جرد المخزون في مستودع</span><span class="sxs-lookup"><span data-stu-id="b327b-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b327b-104">يصف هذا الموضوع عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين في موقع في المستودع.</span><span class="sxs-lookup"><span data-stu-id="b327b-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="b327b-105">وينطبق الإجراء على وظيفة "التخزين الأساسي"، المتوفرة في الوحدة النمطية "إدارة المخزون"، وليس على وظيفة التخزين المتوفرة في الوحدة النمطية "إدارة المستودع".</span><span class="sxs-lookup"><span data-stu-id="b327b-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="b327b-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b327b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="b327b-107">إذا كنت تستخدم البيانات الخاصة بك، فتأكد من إعداد المنتجات والمواقع، وتأكد أنك قد أنشأت اسم دفتر يومية لدفاتر يومية الجرد.</span><span class="sxs-lookup"><span data-stu-id="b327b-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="b327b-108">يتم تنفيذ جرد المخزون عادة بواسطة موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="b327b-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="b327b-109">إنشاء دفتر يومية جرد مخزون</span><span class="sxs-lookup"><span data-stu-id="b327b-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="b327b-110">انتقل إلى **جزء التنقل > الوحدات النمطية > > إدارة المخزون > إدخالات دفتر اليومية > جرد الصنف > الجرد**.</span><span class="sxs-lookup"><span data-stu-id="b327b-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="b327b-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b327b-111">Select **New**.</span></span>
3. <span data-ttu-id="b327b-112">في حقل **الاسم**، حدد اسم دفتر يومية جرد المخزون الذي تريد استخدامه من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b327b-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="b327b-113">سيتم ملء بعض الحقول الأخرى حسب إعداد اسم دفتر يومية جرد المخزون الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="b327b-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="b327b-114">في الحقل **العامل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b327b-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b327b-115">في القائمة، **حدد** العامل الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="b327b-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="b327b-116">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b327b-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="b327b-117">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="b327b-117">Create journal lines</span></span>
1. <span data-ttu-id="b327b-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b327b-118">Select **New**.</span></span>
2. <span data-ttu-id="b327b-119">في الحقل **رقم الصنف**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b327b-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="b327b-120">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد **A0001**.</span><span class="sxs-lookup"><span data-stu-id="b327b-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="b327b-121">في الحقل **الموقع**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b327b-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="b327b-122">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد الموقع **2**.</span><span class="sxs-lookup"><span data-stu-id="b327b-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="b327b-123">في الحقل **المستودع**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b327b-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="b327b-124">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد المستودع **24**.</span><span class="sxs-lookup"><span data-stu-id="b327b-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="b327b-125">في الحقل **الموقع**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b327b-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="b327b-126">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="b327b-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="b327b-127">في الحقل "تم جرده"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b327b-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="b327b-128">إذا أدخلتَ عددًا محسوبًا يختلف عن العدد الذي يظهر في الحقل **الكمية المتاحة**، سيتم تحديث الحقل **الكمية** لإظهار التباين.</span><span class="sxs-lookup"><span data-stu-id="b327b-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="b327b-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b327b-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="b327b-130">ترحيل دفتر يومية جرد المخزون</span><span class="sxs-lookup"><span data-stu-id="b327b-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="b327b-131">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="b327b-131">Select **Post**.</span></span> <span data-ttu-id="b327b-132">عند ترحيل دفتر يومية جرد مخزون، إذا كان المبلغ المحسوب يختلف عن المبلغ الذي تم الإعلام عنه في الحقل **الكمية المتاحة**، سيتم ترحيل استلام مخزون أو إصداره وتغيير مستوى المخزون وقيمته وإنشاء حركات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="b327b-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="b327b-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b327b-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="b327b-134">عرض حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="b327b-134">View inventory transactions</span></span>
1. <span data-ttu-id="b327b-135">حدد **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="b327b-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="b327b-136">حدد **الحركات**.</span><span class="sxs-lookup"><span data-stu-id="b327b-136">Select **Transactions**.</span></span> <span data-ttu-id="b327b-137">هنا يمكنك أن ترى أي حركات ذات صلة سيتم إنشاؤها عند ترحيل دفتر يومية جرد المخزون الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b327b-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

