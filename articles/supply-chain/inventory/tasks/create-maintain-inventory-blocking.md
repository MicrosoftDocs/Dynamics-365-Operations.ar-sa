---
title: إنشاء وصيانة حظر المخزون
description: يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e76c3d1f46e31dcd2171682a629dabe5bf5db418
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204138"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="c9c8c-103">إنشاء وصيانة حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="c9c8c-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9c8c-104">يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="c9c8c-105">يمكنك تشغيل هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام قيم الأمثلة الموضحة.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="c9c8c-106">يجب أن يتوفر لديك صنف مع مخزون فعلي موجود قبل بدء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="c9c8c-107">إنشاء حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="c9c8c-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="c9c8c-108">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة المخزون > المهام الدورية > حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="c9c8c-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-109">Click **New**.</span></span>
3. <span data-ttu-id="c9c8c-110">في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c9c8c-111">في القائمة، حدد الصنف الذي تريد اختياره.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="c9c8c-112">حدد رقم صنف مع المخزون الفعلي الموجود الذي تريد حظره.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="c9c8c-113">إذا كنت تستخدم USMF، فيمكنك تحديد الصنف M9201.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="c9c8c-114">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="c9c8c-115">إذا كنت تستخدم الصنف M9201، فتحتاج إلى تحديد أقل من 200.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="c9c8c-116">قم بتوسيع القسم **أبعاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="c9c8c-117">في الحقل **المستودع**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c9c8c-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="c9c8c-119">إذا كنت تستخدم الصنف M9201، فيمكنك تحديد المستودع 51.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="c9c8c-120">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="c9c8c-121">تحديث شروط حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="c9c8c-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="c9c8c-122">على علامة التبويب السريعة **عام**، أدخل رقمًا في حقل **الكمية**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="c9c8c-123">حدّث الحقل "كمية المخزون" لعكس الكمية التي تريد حظرها.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="c9c8c-124">أدخل تاريخًا في حقل **التاريخ المتوقع‬**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="c9c8c-125">قد تحتاج إلى الإشارة إلى الوقت الذي من المتوقع أن يصبح فيه المخزون المحظور متوفرًا للحجز عن طريق تعيين تاريخ متوقع.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="c9c8c-126">إذا تم تحديد الخيار "الإيصالات المستلمة‬" لحظر المخزون، كما يتم بشكل افتراضي عندما تنشئ الحظر يدويًا، فسيظهر هذا التاريخ على الحركة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="c9c8c-127">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="c9c8c-128">إزالة حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="c9c8c-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="c9c8c-129">في **جزء الإجراءات**، انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="c9c8c-130">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-130">Click **Yes**.</span></span>
3. <span data-ttu-id="c9c8c-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c9c8c-131">Close the page.</span></span>

