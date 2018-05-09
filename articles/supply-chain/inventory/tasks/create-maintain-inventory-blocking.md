---
title: "إنشاء وصيانة حظر المخزون"
description: "يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 06b1e552b1a0467e2e5665ebc9f44c9247e45180
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="282e0-103">إنشاء وصيانة حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="282e0-103">Create and maintain inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="282e0-104">يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="282e0-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="282e0-105">يمكنك تشغيل هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام قيم الأمثلة الموضحة.</span><span class="sxs-lookup"><span data-stu-id="282e0-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="282e0-106">يجب أن يتوفر لديك صنف مع مخزون فعلي موجود قبل بدء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="282e0-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="282e0-107">إنشاء حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="282e0-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="282e0-108">انتقل إلى إدارة المخزون > المهام الدورية > حظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="282e0-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="282e0-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="282e0-109">Click New.</span></span>
3. <span data-ttu-id="282e0-110">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="282e0-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="282e0-111">في القائمة، حدد الصنف الذي تريد اختياره.</span><span class="sxs-lookup"><span data-stu-id="282e0-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="282e0-112">حدد رقم صنف مع المخزون الفعلي الموجود الذي تريد حظره.</span><span class="sxs-lookup"><span data-stu-id="282e0-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="282e0-113">إذا كنت تستخدم USMF، فيمكنك تحديد الصنف M9201.</span><span class="sxs-lookup"><span data-stu-id="282e0-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="282e0-114">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="282e0-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="282e0-115">إذا كنت تستخدم الصنف M9201، فتحتاج إلى تحديد أقل من 200.</span><span class="sxs-lookup"><span data-stu-id="282e0-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="282e0-116">بدّل توسيع المقطع "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="282e0-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="282e0-117">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="282e0-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="282e0-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="282e0-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="282e0-119">إذا كنت تستخدم الصنف M9201، فيمكنك تحديد المستودع 51.</span><span class="sxs-lookup"><span data-stu-id="282e0-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="282e0-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="282e0-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="282e0-121">تحديث شروط حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="282e0-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="282e0-122">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="282e0-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="282e0-123">حدّث الحقل "كمية المخزون" لعكس الكمية التي تريد حظرها.</span><span class="sxs-lookup"><span data-stu-id="282e0-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="282e0-124">في الحقل "التاريخ المتوقع‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="282e0-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="282e0-125">قد تحتاج إلى الإشارة إلى الوقت الذي من المتوقع أن يصبح فيه المخزون المحظور متوفرًا للحجز عن طريق تعيين تاريخ متوقع.</span><span class="sxs-lookup"><span data-stu-id="282e0-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="282e0-126">إذا تم تحديد الخيار "الإيصالات المستلمة‬" لحظر المخزون، كما يتم بشكل افتراضي عندما تنشئ الحظر يدويًا، فسيظهر هذا التاريخ على الحركة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="282e0-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="282e0-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="282e0-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="282e0-128">إزالة حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="282e0-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="282e0-129">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="282e0-129">Click Delete.</span></span>
2. <span data-ttu-id="282e0-130">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="282e0-130">Click Yes.</span></span>
3. <span data-ttu-id="282e0-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="282e0-131">Close the page.</span></span>

