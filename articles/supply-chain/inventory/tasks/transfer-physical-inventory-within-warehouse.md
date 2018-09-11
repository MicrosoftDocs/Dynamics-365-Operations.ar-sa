--- 
title: "نقل المخزون الفعلي داخل المستودع"
description: "يوضح لك الإجراء عملية إنشاء دفتر يومية تحويل مخزون وترحيله لتسجيل حركة صنف من موقع لآخر بأحد المستودعات."
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 41057d0a35cab122840a20a5c65ab7ae3133052c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="ab9ac-103">نقل المخزون الفعلي داخل المستودع</span><span class="sxs-lookup"><span data-stu-id="ab9ac-103">Transfer physical inventory within the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab9ac-104">يوضح لك الإجراء عملية إنشاء دفتر يومية تحويل مخزون وترحيله لتسجيل حركة صنف من موقع لآخر بأحد المستودعات.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="ab9ac-105">يجب أن يكون لديك اسم دفتر يومية مخزون تم إعداده لعمليات تحويل المخزون قبل تنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="ab9ac-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام القيم المثال المعروضة، أو باستخدام البيانات الخاصة بك إذا تم إعداد المنتجات والمواقع.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="ab9ac-107">وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="ab9ac-108">إنشاء دفتر يومية تحويل مخزون</span><span class="sxs-lookup"><span data-stu-id="ab9ac-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="ab9ac-109">انتقل إلى "التحويل".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-109">Go to Transfer.</span></span>
2. <span data-ttu-id="ab9ac-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-110">Click New.</span></span>
3. <span data-ttu-id="ab9ac-111">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="ab9ac-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-112">Click OK.</span></span>
    * <span data-ttu-id="ab9ac-113">يوجد خيار تحديد البعدين "من" و"إلى" لكل بند بدفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="ab9ac-114">وهذا البُعدان ضروريان لنوع دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-114">These are essential for this journal type.</span></span> <span data-ttu-id="ab9ac-115">يمكنك تحويل الأصناف إلى مواقع باستخدام قواعد مختلفة.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="ab9ac-116">في هذا المثال سنحول صنفًا داخل نفس المستودع من موقع تتحكم به لوحة الترخيص إلى موقع لا تتحكم به لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="ab9ac-117">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="ab9ac-117">Create journal lines</span></span>
1. <span data-ttu-id="ab9ac-118">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-118">Click New.</span></span>
2. <span data-ttu-id="ab9ac-119">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-120">إذا كنت تستخدم USMF، يمكنك تحديد "A0001".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="ab9ac-121">في الحقل "من الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-122">إذا كنت تستخدم USMF، يمكنك تحديد "2".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="ab9ac-123">في الحقل "إلى الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-124">إذا كنت تستخدم USMF، يمكنك تحديد "2".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="ab9ac-125">في الحقل "من المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-126">إذا كنت تستخدم USMF، يمكنك تحديد "24".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="ab9ac-127">في الحقل "إلى المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-128">إذا كنت تستخدم USMF، يمكنك تحديد "24".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="ab9ac-129">في الحقل "من الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-130">إذا كنت تستخدم USMF، يمكنك تحديد "FL-001".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="ab9ac-131">في الحقل "إلى الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-132">إذا كنت تستخدم USMF، يمكنك تحديد "BULK-001".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="ab9ac-133">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="ab9ac-134">انقر فوق علامة التبويب "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="ab9ac-135">في الحقل "لوحة الترخيص"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="ab9ac-136">إذا كنت تستخدم USMF، يمكنك تحديد "24".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="ab9ac-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="ab9ac-138">ترحيل دفتر يومية نقل المخزون</span><span class="sxs-lookup"><span data-stu-id="ab9ac-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="ab9ac-139">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-139">Click Post.</span></span>
2. <span data-ttu-id="ab9ac-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="ab9ac-141">عرض حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="ab9ac-141">View inventory transactions</span></span>
1. <span data-ttu-id="ab9ac-142">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-142">Click Inventory.</span></span>
2. <span data-ttu-id="ab9ac-143">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="ab9ac-143">Click Transactions.</span></span>
    * <span data-ttu-id="ab9ac-144">هنا يمكنك أن ترى الحركات التي تم إنشاؤها عندما قمت بترحيل دفتر اليومية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-144">Here you can see the transactions that were created when you posted your journal.</span></span>  


