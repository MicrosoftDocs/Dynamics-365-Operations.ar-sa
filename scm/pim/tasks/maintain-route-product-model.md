--- 
title: "الاحتفاظ بمسار لطراز المنتج"
description: "يتطلب تشغيل هذا الإجراء تكوين نموذج منتج موجود."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: ar-sa
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="f33de-103">الاحتفاظ بمسار لطراز المنتج</span><span class="sxs-lookup"><span data-stu-id="f33de-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f33de-104">يتطلب تشغيل هذا الإجراء تكوين نموذج منتج موجود.</span><span class="sxs-lookup"><span data-stu-id="f33de-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="f33de-105">يستخدم هذا الإجراء نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF خلال العملية.</span><span class="sxs-lookup"><span data-stu-id="f33de-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="f33de-106">إضافة مسار عملية</span><span class="sxs-lookup"><span data-stu-id="f33de-106">Add a route operation</span></span>
1. <span data-ttu-id="f33de-107">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="f33de-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="f33de-108">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="f33de-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="f33de-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f33de-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f33de-110">حدد نموذج مكبر الصوت المتطور لهذا التمرين.</span><span class="sxs-lookup"><span data-stu-id="f33de-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="f33de-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f33de-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f33de-112">قم بتوسيع القسم "عمليات المسار".</span><span class="sxs-lookup"><span data-stu-id="f33de-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="f33de-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f33de-113">Click Add.</span></span>
7. <span data-ttu-id="f33de-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f33de-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="f33de-115">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f33de-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f33de-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f33de-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="f33de-117">إدخال تفاصيل مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="f33de-117">Enter route operation details</span></span>
1. <span data-ttu-id="f33de-118">انقر فوق "تفاصيل عملية المسار".</span><span class="sxs-lookup"><span data-stu-id="f33de-118">Click Route operation details.</span></span>
2. <span data-ttu-id="f33de-119">في الحقل "العملية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f33de-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="f33de-120">في حقل رقم</span><span class="sxs-lookup"><span data-stu-id="f33de-120">In the Oper.</span></span> <span data-ttu-id="f33de-121">العملية</span><span class="sxs-lookup"><span data-stu-id="f33de-121">No.</span></span> <span data-ttu-id="f33de-122">، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f33de-122">field, enter a number.</span></span>
    * <span data-ttu-id="f33de-123">تحدد أرقام العملية تسلسل المسار.</span><span class="sxs-lookup"><span data-stu-id="f33de-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="f33de-124">قد تحصل كل خاصية بعملية مسار على قيمة ثابتة أو يتم تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="f33de-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="f33de-125">يؤدي التعيين إلى سمة إلى تعيين القيمة كجزء من التكوين.</span><span class="sxs-lookup"><span data-stu-id="f33de-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="f33de-126">في الحقل "مجموعة المسارات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f33de-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="f33de-127">تحدد مجموعة المسارات السلوك الأساسي للتكاليف والاستهلاك والإعداد.</span><span class="sxs-lookup"><span data-stu-id="f33de-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="f33de-128">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="f33de-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="f33de-129">انقر فوق علامة التبويب "الأوقات".</span><span class="sxs-lookup"><span data-stu-id="f33de-129">Click the Times tab.</span></span>
7. <span data-ttu-id="f33de-130">في حقل كمية العمليات</span><span class="sxs-lookup"><span data-stu-id="f33de-130">In the Process qty.</span></span> <span data-ttu-id="f33de-131">، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f33de-131">field, enter a number.</span></span>
    * <span data-ttu-id="f33de-132">حدد العدد الذي سوف تتم معالجته أثناء عملية واحدة.</span><span class="sxs-lookup"><span data-stu-id="f33de-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="f33de-133">في الحقل "الساعات/الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f33de-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="f33de-134">أدخل نسبة الوقت.</span><span class="sxs-lookup"><span data-stu-id="f33de-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="f33de-135">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="f33de-135">Select the Set check box.</span></span>
10. <span data-ttu-id="f33de-136">في الحقل "وقت التشغيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f33de-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="f33de-137">حدد وقت المعالجة للكمية التي قمت بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="f33de-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="f33de-138">انقر فوق علامة التبويب "متطلبات المورد".</span><span class="sxs-lookup"><span data-stu-id="f33de-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="f33de-139">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f33de-139">Click Add.</span></span>
13. <span data-ttu-id="f33de-140">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f33de-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f33de-141">في الحقل "نوع المتطلب"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="f33de-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="f33de-142">حدد ما إذا كنت تريد تحديد موارد أو قدرات معينة يجب أن تتوفر لدى الموارد.</span><span class="sxs-lookup"><span data-stu-id="f33de-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="f33de-143">في الحقل "المتطلب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f33de-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="f33de-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f33de-144">Click OK.</span></span>


