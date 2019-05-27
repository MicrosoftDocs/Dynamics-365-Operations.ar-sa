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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfe0f6995598757dcea824e1bb4f7ef8ab54a67b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549892"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="2efde-103">تصحيح معلومات تعقب المخزون</span><span class="sxs-lookup"><span data-stu-id="2efde-103">Correct inventory tracking information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2efde-104">يرشدك هذا الإجراء خلال عملية إنشاء وترحيل دفتر يومية تحويل المخزون من أجل تصحيح معلومات تعقب المخزون.</span><span class="sxs-lookup"><span data-stu-id="2efde-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="2efde-105">في هذا المثال، سنقوم بتحديث المعلومات من عنصر التحكم في الدفعة من خلال تغيير المجموعة المسجلة بشكل غير صحيح إلى دفعة أخرى.</span><span class="sxs-lookup"><span data-stu-id="2efde-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="2efde-106">يمكنك استعراض هذا الإجراء في عنوان USPI بشركة بيانات العرض التوضيحي، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2efde-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="2efde-107">إذا كنت تستخدم البيانات الخاصة بك، فستحتاج إلى وجود عنصر تم تمكين دفعته، ويجب ألا يكون متحكمًا في موقعه.</span><span class="sxs-lookup"><span data-stu-id="2efde-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="2efde-108">يجب أن يكون لديك أيضًا اسم دفتر يومية مخزون تم إعداده لعمليات نقل المخزون.</span><span class="sxs-lookup"><span data-stu-id="2efde-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="2efde-109">وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.</span><span class="sxs-lookup"><span data-stu-id="2efde-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="2efde-110">إنشاء دفتر يومية تحويل مخزون</span><span class="sxs-lookup"><span data-stu-id="2efde-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="2efde-111">انتقل إلى "التحويل".</span><span class="sxs-lookup"><span data-stu-id="2efde-111">Go to Transfer.</span></span>
2. <span data-ttu-id="2efde-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2efde-112">Click New.</span></span>
3. <span data-ttu-id="2efde-113">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2efde-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2efde-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2efde-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="2efde-115">إنشاء بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="2efde-115">Create journal lines</span></span>
1. <span data-ttu-id="2efde-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2efde-116">Click New.</span></span>
2. <span data-ttu-id="2efde-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2efde-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2efde-118">إذا كنت تستخدم USPI، فحدد الصنف M5003.</span><span class="sxs-lookup"><span data-stu-id="2efde-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="2efde-119">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2efde-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="2efde-120">انقر فوق علامة التبويب "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="2efde-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="2efde-121">في حقل "رقم الدفعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2efde-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="2efde-122">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2efde-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="2efde-123">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2efde-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="2efde-124">في حقل "رقم الدفعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2efde-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="2efde-125">ترحيل دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="2efde-125">Post the journal</span></span>
1. <span data-ttu-id="2efde-126">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="2efde-126">Click Post.</span></span>
2. <span data-ttu-id="2efde-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2efde-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="2efde-128">تحقق من معلومات التتبع</span><span class="sxs-lookup"><span data-stu-id="2efde-128">Check tracing information</span></span>
1. <span data-ttu-id="2efde-129">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="2efde-129">Click Inventory.</span></span>
2. <span data-ttu-id="2efde-130">انقر فوق "تعقب".</span><span class="sxs-lookup"><span data-stu-id="2efde-130">Click Trace.</span></span>
3. <span data-ttu-id="2efde-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2efde-131">Click OK.</span></span>
    * <span data-ttu-id="2efde-132">باستخدام معلومات التتبع هذه، يمكنك إجراء التتبع الخلفي للدفعة التي قمت بتصحيح المخزون منها.</span><span class="sxs-lookup"><span data-stu-id="2efde-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="2efde-133">يمكنك أيضا استخدام صفحة تتبع الصنف لمشاهدة هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="2efde-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="2efde-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2efde-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="2efde-135">تحقق من حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="2efde-135">Check inventory transactions</span></span>
1. <span data-ttu-id="2efde-136">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="2efde-136">Click Inventory.</span></span>
2. <span data-ttu-id="2efde-137">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="2efde-137">Click Transactions.</span></span>
    * <span data-ttu-id="2efde-138">هنا يمكنك أن ترى الحركات التي تم إنشاؤها عندما قمت بترحيل دفتر اليومية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2efde-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

