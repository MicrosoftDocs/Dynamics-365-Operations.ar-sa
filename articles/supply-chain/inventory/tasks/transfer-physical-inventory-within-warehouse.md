---
title: "نقل المخزون الفعلي داخل المستودع"
description: "يوضح لك الإجراء عملية إنشاء دفتر يومية تحويل مخزون وترحيله لتسجيل حركة صنف من موقع لآخر بأحد المستودعات."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: ar-sa
ms.lasthandoff: 09/12/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="f4ac9-103">نقل المخزون الفعلي داخل المستودع</span><span class="sxs-lookup"><span data-stu-id="f4ac9-103">Transfer physical inventory within the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4ac9-104">يوضح لك الإجراء عملية إنشاء دفتر يومية تحويل مخزون وترحيله لتسجيل حركة صنف من موقع لآخر بأحد المستودعات.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="f4ac9-105">يجب أن يكون لديك اسم دفتر يومية مخزون تم إعداده لعمليات تحويل المخزون قبل تنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="f4ac9-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام القيم المثال المعروضة، أو باستخدام البيانات الخاصة بك إذا تم إعداد المنتجات والمواقع.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="f4ac9-107">وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="f4ac9-108">إنشاء دفتر يومية تحويل مخزون</span><span class="sxs-lookup"><span data-stu-id="f4ac9-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="f4ac9-109">انتقل إلى "التحويل".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-109">Go to Transfer.</span></span>
2. <span data-ttu-id="f4ac9-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-110">Click New.</span></span>
3. <span data-ttu-id="f4ac9-111">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="f4ac9-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-112">Click OK.</span></span>
    * <span data-ttu-id="f4ac9-113">يوجد خيار تحديد البعدين "من" و"إلى" لكل بند بدفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="f4ac9-114">وهذا البُعدان ضروريان لنوع دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-114">These are essential for this journal type.</span></span> <span data-ttu-id="f4ac9-115">يمكنك تحويل الأصناف إلى مواقع باستخدام قواعد مختلفة.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="f4ac9-116">في هذا المثال سنحول صنفًا داخل نفس المستودع من موقع تتحكم به لوحة الترخيص إلى موقع لا تتحكم به لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="f4ac9-117">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f4ac9-117">Create journal lines</span></span>
1. <span data-ttu-id="f4ac9-118">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-118">Click New.</span></span>
2. <span data-ttu-id="f4ac9-119">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-120">إذا كنت تستخدم USMF، يمكنك تحديد "A0001".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="f4ac9-121">في الحقل "من الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-122">إذا كنت تستخدم USMF، يمكنك تحديد "2".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="f4ac9-123">في الحقل "إلى الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-124">إذا كنت تستخدم USMF، يمكنك تحديد "2".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="f4ac9-125">في الحقل "من المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-126">إذا كنت تستخدم USMF، يمكنك تحديد "24".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="f4ac9-127">في الحقل "إلى المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-128">إذا كنت تستخدم USMF، يمكنك تحديد "24".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="f4ac9-129">في الحقل "من الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-130">إذا كنت تستخدم USMF، يمكنك تحديد "FL-001".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="f4ac9-131">في الحقل "إلى الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-132">إذا كنت تستخدم USMF، يمكنك تحديد "BULK-001".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="f4ac9-133">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="f4ac9-134">انقر فوق علامة التبويب "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="f4ac9-135">في الحقل "لوحة الترخيص"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="f4ac9-136">إذا كنت تستخدم USMF، يمكنك تحديد "24".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="f4ac9-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="f4ac9-138">ترحيل دفتر يومية نقل المخزون</span><span class="sxs-lookup"><span data-stu-id="f4ac9-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="f4ac9-139">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-139">Click Post.</span></span>
2. <span data-ttu-id="f4ac9-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="f4ac9-141">عرض حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="f4ac9-141">View inventory transactions</span></span>
1. <span data-ttu-id="f4ac9-142">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-142">Click Inventory.</span></span>
2. <span data-ttu-id="f4ac9-143">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="f4ac9-143">Click Transactions.</span></span>
    * <span data-ttu-id="f4ac9-144">هنا يمكنك أن ترى الحركات التي تم إنشاؤها عندما قمت بترحيل دفتر اليومية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

