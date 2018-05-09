--- 
title: "إنشاء خطة مادية للمنتجات المساعدة"
description: "يعمل مخطط الإنتاج على التخطيط للمتطلبات المادية للأصناف التي تعتبر منتجات مساعدة للمعادلة."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f3a411e8fc773957b5ce3f24749242d9d0c6ffd0
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6d372-103">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="6d372-103">Create a material plan for co-products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d372-104">يعمل مخطط الإنتاج على التخطيط للمتطلبات المادية للأصناف التي تعتبر منتجات مساعدة للمعادلة.</span><span class="sxs-lookup"><span data-stu-id="6d372-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="6d372-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USP2.</span><span class="sxs-lookup"><span data-stu-id="6d372-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="6d372-106">إنشاء متطلبات منتج مساعد</span><span class="sxs-lookup"><span data-stu-id="6d372-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="6d372-107">انتقل إلى لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="6d372-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="6d372-108">انقر فوق "الاستعلام عن أمر المبيعات ومعالجته‬".</span><span class="sxs-lookup"><span data-stu-id="6d372-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="6d372-109">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="6d372-109">Click New.</span></span>
4. <span data-ttu-id="6d372-110">انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="6d372-110">Click Sales order.</span></span>
5. <span data-ttu-id="6d372-111">في الحقل "حساب العميل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6d372-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="6d372-112">على سبيل المثال: US-001</span><span class="sxs-lookup"><span data-stu-id="6d372-112">Example: US-001</span></span>  
6. <span data-ttu-id="6d372-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d372-113">Click OK.</span></span>
7. <span data-ttu-id="6d372-114">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6d372-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6d372-115">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="6d372-115">Example: P6003</span></span>  
8. <span data-ttu-id="6d372-116">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6d372-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6d372-117">على سبيل المثال: 50000</span><span class="sxs-lookup"><span data-stu-id="6d372-117">Example: 50000</span></span>  
9. <span data-ttu-id="6d372-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6d372-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6d372-119">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="6d372-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="6d372-120">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="6d372-120">Click Master planning.</span></span>
2. <span data-ttu-id="6d372-121">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6d372-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6d372-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d372-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6d372-123">على سبيل المثال: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="6d372-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="6d372-124">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="6d372-124">Click Run.</span></span>
5. <span data-ttu-id="6d372-125">قم بتوسيع المقطع "السجلات المطلوب تضمينها‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="6d372-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="6d372-126">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="6d372-126">Click Filter.</span></span>
7. <span data-ttu-id="6d372-127">في القائمة، حدد الصف للحقل = رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="6d372-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="6d372-128">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6d372-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="6d372-129">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="6d372-129">Example: P6003</span></span>  
9. <span data-ttu-id="6d372-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d372-130">Click OK.</span></span>
10. <span data-ttu-id="6d372-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d372-131">Click OK.</span></span>
11. <span data-ttu-id="6d372-132">انقر فوق "الأوامر المخططة".</span><span class="sxs-lookup"><span data-stu-id="6d372-132">Click Planned orders.</span></span>
12. <span data-ttu-id="6d372-133">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="6d372-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6d372-134">على سبيل المثال، قم بإجراء التصفية على الحقل "رقم الصنف" باستخدام القيمة "P6000".</span><span class="sxs-lookup"><span data-stu-id="6d372-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="6d372-135">قم بإجراء التصفية حسب بند المعادلة الذي لديه منتج مساعد للصنف الذي أنشأت أمر المبيعات له.</span><span class="sxs-lookup"><span data-stu-id="6d372-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="6d372-136">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d372-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6d372-137">حدد أي واحد من الصفوف التي أرجعها عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="6d372-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="6d372-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d372-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="6d372-139">قم بتوسيع المقطع "تثبيت السعر" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="6d372-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="6d372-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d372-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6d372-141">يتم تثبيت الأمر المخطط لأمر المبيعات الخاص بالمنتج المساعد.</span><span class="sxs-lookup"><span data-stu-id="6d372-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="6d372-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d372-142">Close the page.</span></span>


