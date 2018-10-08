--- 
title: "التحقق من توفر المخزون"
description: "يوضح هذا الإجراء كيفية التحقق من المخزون الفعلي والمخزون الفعلي الحالي لرقم صنف معين."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6db29d422e7dfd7b2481b4fcbc404278e37511d1
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.contentlocale: ar-sa
ms.lasthandoff: 10/08/2018

---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="65d08-103">التحقق من توفر المخزون</span><span class="sxs-lookup"><span data-stu-id="65d08-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65d08-104">يوضح هذا الإجراء كيفية التحقق من المخزون الفعلي والمخزون الفعلي الحالي لرقم صنف معين.</span><span class="sxs-lookup"><span data-stu-id="65d08-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="65d08-105">كما يوضح لك كيفية الحصول على معلومات التوريد المتعلقة بصنف معين.</span><span class="sxs-lookup"><span data-stu-id="65d08-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="65d08-106">المخزون الفعلي الحالي هو المخزون الفعلي المتوفر – أي، تم شراؤه واستلامه وتسجيله.</span><span class="sxs-lookup"><span data-stu-id="65d08-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="65d08-107">يتضمن المخزون الفعلي المخزون الفعلي المتوفر، ولكن أيضا المخزون الذي تم طلبه والمتوقع وصوله، ولكن لم يتم استلامه أو تسجيله.</span><span class="sxs-lookup"><span data-stu-id="65d08-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="65d08-108">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="65d08-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="65d08-109">إذا كنت تستخدم USMF، فيمكنك استخدام القيم المعروضة التي تم استخدامها كأمثلة.</span><span class="sxs-lookup"><span data-stu-id="65d08-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="65d08-110">وعادة ما تُنفذ هذه المهام عن طريق عامل مستودع.</span><span class="sxs-lookup"><span data-stu-id="65d08-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="65d08-111">تحديد المخزون الفعلي‬ لصنف معين</span><span class="sxs-lookup"><span data-stu-id="65d08-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="65d08-112">انتقل إلى إدارة المخزون > الاستعلامات والتقارير > المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="65d08-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="65d08-113">حدد صف "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="65d08-113">Select the Item number row.</span></span>
    * <span data-ttu-id="65d08-114">للاستعلام عن المخزون الفعلي حسب رقم الصنف، حدد الصف حيث تم تعيين "الجدول" إلى "المخزون الفعلي" وحيث تم تعيين "الحقل" إلى "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="65d08-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="65d08-115">في الحقل "المعايير"، حدد الصنف الذي ترغب في الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="65d08-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="65d08-116">إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فيمكنك تحديد "M9201".</span><span class="sxs-lookup"><span data-stu-id="65d08-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="65d08-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="65d08-117">Click OK.</span></span>
5. <span data-ttu-id="65d08-118">انقر فوق "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="65d08-118">Click Dimensions.</span></span>
    * <span data-ttu-id="65d08-119">تسمح علامة التبويب "الأبعاد" بتحديد مقدار التفاصيل التي تريد مشاهدتها حول المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="65d08-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="65d08-120">إذا كنت تحتاج إلى البيانات المتعلقة بالحجز، فيجب عرض كافة أبعاد المخزون للأصناف التي تستخدم عمليات المستودع المتقدمة (WHS).</span><span class="sxs-lookup"><span data-stu-id="65d08-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="65d08-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="65d08-121">Click OK.</span></span>
7. <span data-ttu-id="65d08-122">في جزء الإجراءات، انقر فوق "معلومات ذات صلة‬".</span><span class="sxs-lookup"><span data-stu-id="65d08-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="65d08-123">إذا لم تشاهد هذا، فقد تحتاج إلى النقر فوق زر علامة القطع (...) لمشاهدة خيارات إضافية في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="65d08-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="65d08-124">انقر فوق "نظرة عامة على التوريد‬".</span><span class="sxs-lookup"><span data-stu-id="65d08-124">Click Supply overview.</span></span>
    * <span data-ttu-id="65d08-125">توفر علامة التبويب "نظرة عامة على التوريد‬" معلومات التوريد لصنف معين، مثل الكمية الفعلية وزمن الوصول ومعلومات المورّد.</span><span class="sxs-lookup"><span data-stu-id="65d08-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="65d08-126">قم بتوسيع مقطع "الكمية المتاحة".</span><span class="sxs-lookup"><span data-stu-id="65d08-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="65d08-127">قم بتوسيع مقطع "المورّدون".</span><span class="sxs-lookup"><span data-stu-id="65d08-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="65d08-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="65d08-128">Close the page.</span></span>
12. <span data-ttu-id="65d08-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="65d08-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="65d08-130">تحديد المخزون الفعلي الحالي</span><span class="sxs-lookup"><span data-stu-id="65d08-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="65d08-131">انتقل إلى إدارة المستودعات > الاستعلامات والتقارير > المخزون الفعلي الحالي.</span><span class="sxs-lookup"><span data-stu-id="65d08-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="65d08-132">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="65d08-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="65d08-133">يمكنك استخدام حقلي "الموقع" و"المستودع" لتصفية قائمة الأصناف.</span><span class="sxs-lookup"><span data-stu-id="65d08-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="65d08-134">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="65d08-134">Refresh the page.</span></span>
4. <span data-ttu-id="65d08-135">انقر فوق "عرض الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="65d08-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="65d08-136">تسمح علامة التبويب "عرض الأبعاد‬" بتحديد مقدار التفاصيل التي تريد مشاهدتها حول المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="65d08-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="65d08-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="65d08-137">Click OK.</span></span>
6. <span data-ttu-id="65d08-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="65d08-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="65d08-139">تحديد المخزون الفعلي حسب الموقع</span><span class="sxs-lookup"><span data-stu-id="65d08-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="65d08-140">انتقل إلى إدارة المستودعات > الاستعلامات والتقارير > الفعلي حسب الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="65d08-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="65d08-141">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="65d08-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="65d08-142">إذا كنت تستخدم شركة العرض التوضيحي USMF، فيمكنك استخدام "51".</span><span class="sxs-lookup"><span data-stu-id="65d08-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="65d08-143">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="65d08-143">Refresh the page.</span></span>
4. <span data-ttu-id="65d08-144">انقر فوق "عرض الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="65d08-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="65d08-145">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="65d08-145">Click OK.</span></span>
6. <span data-ttu-id="65d08-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="65d08-146">Close the page.</span></span>


