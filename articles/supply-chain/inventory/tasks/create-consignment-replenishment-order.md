---
title: إنشاء أمر تزويد شحن
description: يوضح هذا الإجراء كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845536"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="fda46-103">إنشاء أمر تزويد شحن</span><span class="sxs-lookup"><span data-stu-id="fda46-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fda46-104">يوضح هذا الإجراء كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن.</span><span class="sxs-lookup"><span data-stu-id="fda46-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="fda46-105">ويوضح أيضًا كيفية تسجيل إيصال استلام المنتجات بحيث يتم تسجيل مخزون الشحن كمخزون فعلي يملكه المورّد.</span><span class="sxs-lookup"><span data-stu-id="fda46-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="fda46-106">يقوم عادةً أخصائي التدبير بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="fda46-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="fda46-107">ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="fda46-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="fda46-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="fda46-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="fda46-109">إنشاء أمر تزويد شحن</span><span class="sxs-lookup"><span data-stu-id="fda46-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="fda46-110">انتقل إلى التدبير وتحديد الموارد‬ > الشحن‬ > أوامر تزويد الشحن‬.</span><span class="sxs-lookup"><span data-stu-id="fda46-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="fda46-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fda46-111">Click New.</span></span>
3. <span data-ttu-id="fda46-112">في حقل "حساب المورّد‬"، أدخل المورّد "US-104".</span><span class="sxs-lookup"><span data-stu-id="fda46-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="fda46-113">يجب تحديد مورّد تم تسجيله كمالك في الصفحة "ملاك المخزون‬".</span><span class="sxs-lookup"><span data-stu-id="fda46-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="fda46-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fda46-114">Click OK.</span></span>
5. <span data-ttu-id="fda46-115">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="fda46-115">Click Add line.</span></span>
6. <span data-ttu-id="fda46-116">في الحقل "رقم الصنف" اكتب "M9211CI".</span><span class="sxs-lookup"><span data-stu-id="fda46-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="fda46-117">يجب تحديد عنصر تم إعداده لمخزون الشحن‬.</span><span class="sxs-lookup"><span data-stu-id="fda46-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="fda46-118">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fda46-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="fda46-119">في حقل "‏‫تاريخ التسليم المطلوب‬‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="fda46-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="fda46-120">يتم استخدام التواريخ المطلوبة والمؤكدة بواسطة محرك MRP لوصول البضائع المنتظر.</span><span class="sxs-lookup"><span data-stu-id="fda46-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="fda46-121">في حقل "‏‫تاريخ التسليم المؤكد‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="fda46-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="fda46-122">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="fda46-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="fda46-123">انقر فوق علامة التبويب "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="fda46-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="fda46-124">لإظهار المالك في الحقل "مالك أبعاد المخزون"، قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fda46-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="fda46-125">تم الآن إدراج المورّد US-104 كالمالك.</span><span class="sxs-lookup"><span data-stu-id="fda46-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="fda46-126">التحقق من حالة حركة المخزون</span><span class="sxs-lookup"><span data-stu-id="fda46-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="fda46-127">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="fda46-127">Click Inventory.</span></span>
2. <span data-ttu-id="fda46-128">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="fda46-128">Click Transactions.</span></span>
3. <span data-ttu-id="fda46-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fda46-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fda46-130">لاحظ أنه تم تعيين حقل "الاستلام" إلى "مطلوب‬".</span><span class="sxs-lookup"><span data-stu-id="fda46-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="fda46-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fda46-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="fda46-132">استلام الأصناف</span><span class="sxs-lookup"><span data-stu-id="fda46-132">Receive items</span></span>
1. <span data-ttu-id="fda46-133">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="fda46-133">Click Product receipt.</span></span>
2. <span data-ttu-id="fda46-134">في الحقل "إيصال استلام المنتجات الخارجي‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fda46-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="fda46-135">في حقل "الكمية"، أدخل رقمًا أقل من الرقم الذي يظهر هناك.</span><span class="sxs-lookup"><span data-stu-id="fda46-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="fda46-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fda46-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="fda46-137">التحقق من المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="fda46-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="fda46-138">انقر فوق المخزون.</span><span class="sxs-lookup"><span data-stu-id="fda46-138">Click Inventory.</span></span>
2. <span data-ttu-id="fda46-139">انقر فوق "الكمية المتاحة‬".</span><span class="sxs-lookup"><span data-stu-id="fda46-139">Click On-hand.</span></span>
3. <span data-ttu-id="fda46-140">انقر فوق "نظرة عامة".</span><span class="sxs-lookup"><span data-stu-id="fda46-140">Click Overview.</span></span>
    * <span data-ttu-id="fda46-141">تتوفر الأصناف التي تم استلامها كمخزون شحن مملوك من قِبل المورّد بشكل فعلي.</span><span class="sxs-lookup"><span data-stu-id="fda46-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="fda46-142">وتظهر الكمية المتبقية في أمر تزويد الشحن في حقل "الكمية المطلوبة إجمالاً‬".</span><span class="sxs-lookup"><span data-stu-id="fda46-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="fda46-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fda46-143">Close the page.</span></span>
5. <span data-ttu-id="fda46-144">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="fda46-144">Click Close.</span></span>

