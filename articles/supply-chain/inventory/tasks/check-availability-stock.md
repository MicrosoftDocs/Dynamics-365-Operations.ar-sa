---
title: التحقق من توفر المخزون
description: يوضح هذا الإجراء كيفية التحقق من المخزون الفعلي والمخزون الفعلي الحالي لرقم صنف معين.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3f6f601d2d48ede2c4db198ac5438aa32e056d
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829767"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="f51ee-103">التحقق من توفر المخزون</span><span class="sxs-lookup"><span data-stu-id="f51ee-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f51ee-104">يوضح هذا الإجراء كيفية التحقق من المخزون الفعلي والمخزون الفعلي الحالي لرقم صنف معين.</span><span class="sxs-lookup"><span data-stu-id="f51ee-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="f51ee-105">كما يوضح لك كيفية الحصول على معلومات التوريد المتعلقة بصنف معين.</span><span class="sxs-lookup"><span data-stu-id="f51ee-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="f51ee-106">المخزون الفعلي الحالي هو المخزون الفعلي المتوفر – أي، تم شراؤه واستلامه وتسجيله.</span><span class="sxs-lookup"><span data-stu-id="f51ee-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="f51ee-107">يتضمن المخزون الفعلي المخزون الفعلي المتوفر، ولكن أيضا المخزون الذي تم طلبه والمتوقع وصوله، ولكن لم يتم استلامه أو تسجيله.</span><span class="sxs-lookup"><span data-stu-id="f51ee-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="f51ee-108">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f51ee-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="f51ee-109">إذا كنت تستخدم USMF، فيمكنك استخدام القيم المعروضة التي تم استخدامها كأمثلة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="f51ee-110">وعادة ما تُنفذ هذه المهام عن طريق عامل مستودع.</span><span class="sxs-lookup"><span data-stu-id="f51ee-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="f51ee-111">تحديد المخزون الفعلي‬ لصنف معين</span><span class="sxs-lookup"><span data-stu-id="f51ee-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="f51ee-112">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المخزون > الاستعلامات والتقارير‬ > المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="f51ee-113">حدد صف **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-113">Select the **Item number** row.</span></span> <span data-ttu-id="f51ee-114">للاستعلام عن المخزون الفعلي حسب رقم الصنف، حدد الصف حيث تم تعيين "الجدول" إلى **المخزون الفعلي** وحيث تم تعيين "الحقل" إلى **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="f51ee-115">في الحقل **المعايير**، حدد الصنف الذي ترغب في الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="f51ee-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="f51ee-116">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فيمكنك تحديد "M9201".</span><span class="sxs-lookup"><span data-stu-id="f51ee-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="f51ee-117">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-117">Click **OK**.</span></span>
5. <span data-ttu-id="f51ee-118">في **جزء الإجراءات**، انقر فوق **الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="f51ee-119">تسمح علامة التبويب **الأبعاد** بتحديد مقدار التفاصيل التي تريد مشاهدتها حول المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="f51ee-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="f51ee-120">إذا كنت تحتاج إلى البيانات المتعلقة بالحجز، فيجب عرض كافة أبعاد المخزون للأصناف التي تستخدم عمليات المستودع المتقدمة (WMS).</span><span class="sxs-lookup"><span data-stu-id="f51ee-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="f51ee-121">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-121">Click **OK**.</span></span>
7. <span data-ttu-id="f51ee-122">في **جزء الإجراءات**، انقر فوق **معلومات ذات صلة‬**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="f51ee-123">إذا لم تشاهد هذا الخيار، فقد تحتاج إلى النقر فوق زر علامة القطع (...) لمشاهدة خيارات إضافية في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="f51ee-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="f51ee-124">انقر فوق **نظرة عامة على التوريد‬**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-124">Click **Supply overview**.</span></span> <span data-ttu-id="f51ee-125">توفر علامة التبويب **نظرة عامة على التوريد‬** معلومات التوريد لصنف معين، مثل الكمية الفعلية وزمن الوصول ومعلومات المورّد.</span><span class="sxs-lookup"><span data-stu-id="f51ee-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="f51ee-126">قم بتوسيع قسم **الكمية المتاحة**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="f51ee-127">قم بتوسيع قسم **المورّدون**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="f51ee-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-128">Close the page.</span></span>
12. <span data-ttu-id="f51ee-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="f51ee-130">تحديد المخزون الفعلي الحالي</span><span class="sxs-lookup"><span data-stu-id="f51ee-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="f51ee-131">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الاستعلامات والتقارير‬ > المخزون الفعلي الحالي‬**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="f51ee-132">في حقل **رقم الصنف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="f51ee-133">يمكنك استخدام حقلي "الموقع" و"المستودع" لتصفية قائمة الأصناف.</span><span class="sxs-lookup"><span data-stu-id="f51ee-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="f51ee-134">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-134">Refresh the page.</span></span>
4. <span data-ttu-id="f51ee-135">في **جزء الإجراءات**، انقر فوق **عرض الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="f51ee-136">تسمح علامة التبويب "عرض الأبعاد‬" بتحديد مقدار التفاصيل التي تريد مشاهدتها حول المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="f51ee-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="f51ee-137">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-137">Click **OK**.</span></span>
6. <span data-ttu-id="f51ee-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="f51ee-139">تحديد المخزون الفعلي حسب الموقع</span><span class="sxs-lookup"><span data-stu-id="f51ee-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="f51ee-140">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الاستعلامات والتقارير‬ > الفعلي حسب الموقع‬‬**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="f51ee-141">في الحقل **المستودع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="f51ee-142">إذا كنت تستخدم شركة العرض التوضيحي USMF، فيمكنك استخدام "51".</span><span class="sxs-lookup"><span data-stu-id="f51ee-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="f51ee-143">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-143">Refresh the page.</span></span>
4. <span data-ttu-id="f51ee-144">انقر فوق **عرض الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="f51ee-145">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f51ee-145">Click **OK**.</span></span>
6. <span data-ttu-id="f51ee-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f51ee-146">Close the page.</span></span>

