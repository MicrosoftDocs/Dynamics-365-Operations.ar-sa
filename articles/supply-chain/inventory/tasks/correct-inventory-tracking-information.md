---
title: تصحيح معلومات تعقب المخزون
description: يرشدك هذا الإجراء خلال عملية إنشاء وترحيل دفتر يومية تحويل المخزون من أجل تصحيح معلومات تعقب المخزون.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8269e5119e45522373eca6cb8fb06bfb94a37566
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845560"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="6d398-103">تصحيح معلومات تعقب المخزون</span><span class="sxs-lookup"><span data-stu-id="6d398-103">Correct inventory tracking information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d398-104">يرشدك هذا الإجراء خلال عملية إنشاء وترحيل دفتر يومية تحويل المخزون من أجل تصحيح معلومات تعقب المخزون.</span><span class="sxs-lookup"><span data-stu-id="6d398-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="6d398-105">في هذا المثال، سنقوم بتحديث المعلومات من عنصر التحكم في الدفعة من خلال تغيير المجموعة المسجلة بشكل غير صحيح إلى دفعة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6d398-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="6d398-106">يمكنك استعراض هذا الإجراء في عنوان USPI بشركة بيانات العرض التوضيحي، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="6d398-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="6d398-107">إذا كنت تستخدم البيانات الخاصة بك، فستحتاج إلى وجود عنصر تم تمكين دفعته، ويجب ألا يكون متحكمًا في موقعه.</span><span class="sxs-lookup"><span data-stu-id="6d398-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="6d398-108">يجب أن يكون لديك أيضًا اسم دفتر يومية مخزون تم إعداده لعمليات نقل المخزون.</span><span class="sxs-lookup"><span data-stu-id="6d398-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="6d398-109">وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="6d398-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="6d398-110">إنشاء دفتر يومية تحويل مخزون</span><span class="sxs-lookup"><span data-stu-id="6d398-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="6d398-111">انتقل إلى "التحويل".</span><span class="sxs-lookup"><span data-stu-id="6d398-111">Go to Transfer.</span></span>
2. <span data-ttu-id="6d398-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6d398-112">Click New.</span></span>
3. <span data-ttu-id="6d398-113">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d398-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="6d398-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d398-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="6d398-115">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6d398-115">Create journal lines</span></span>
1. <span data-ttu-id="6d398-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6d398-116">Click New.</span></span>
2. <span data-ttu-id="6d398-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d398-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6d398-118">إذا كنت تستخدم USPI، فحدد الصنف M5003.</span><span class="sxs-lookup"><span data-stu-id="6d398-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="6d398-119">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6d398-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="6d398-120">انقر فوق علامة التبويب "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="6d398-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="6d398-121">في حقل "رقم الدفعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d398-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="6d398-122">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d398-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="6d398-123">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d398-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="6d398-124">في حقل "رقم الدفعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d398-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="6d398-125">ترحيل دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6d398-125">Post the journal</span></span>
1. <span data-ttu-id="6d398-126">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="6d398-126">Click Post.</span></span>
2. <span data-ttu-id="6d398-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d398-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="6d398-128">تحقق من معلومات التتبع</span><span class="sxs-lookup"><span data-stu-id="6d398-128">Check tracing information</span></span>
1. <span data-ttu-id="6d398-129">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="6d398-129">Click Inventory.</span></span>
2. <span data-ttu-id="6d398-130">انقر فوق "تعقب".</span><span class="sxs-lookup"><span data-stu-id="6d398-130">Click Trace.</span></span>
3. <span data-ttu-id="6d398-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d398-131">Click OK.</span></span>
    * <span data-ttu-id="6d398-132">باستخدام معلومات التتبع هذه، يمكنك إجراء التتبع الخلفي للدفعة التي قمت بتصحيح المخزون منها.</span><span class="sxs-lookup"><span data-stu-id="6d398-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="6d398-133">يمكنك أيضا استخدام صفحة تتبع الصنف لمشاهدة هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="6d398-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="6d398-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d398-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="6d398-135">تحقق من حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="6d398-135">Check inventory transactions</span></span>
1. <span data-ttu-id="6d398-136">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="6d398-136">Click Inventory.</span></span>
2. <span data-ttu-id="6d398-137">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="6d398-137">Click Transactions.</span></span>
    * <span data-ttu-id="6d398-138">هنا يمكنك أن ترى الحركات التي تم إنشاؤها عندما قمت بترحيل دفتر اليومية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="6d398-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

