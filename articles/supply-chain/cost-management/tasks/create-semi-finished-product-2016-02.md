--- 
title: "إنشاء منتج غير نهائي (فبراير 2016 فقط)"
description: "تركز هذه المهمة على إنشاء منتج غير نهائي."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 76fcba3732879f85c9bf0faa6d2481b9c5313a17
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="2807a-103">إنشاء منتج غير نهائي (فبراير 2016 فقط)</span><span class="sxs-lookup"><span data-stu-id="2807a-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2807a-104">تركز هذه المهمة على إنشاء منتج غير نهائي.</span><span class="sxs-lookup"><span data-stu-id="2807a-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="2807a-105">إنها المهمة الثانية في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="2807a-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="2807a-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="2807a-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="2807a-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="2807a-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2807a-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2807a-108">Click New.</span></span>
3. <span data-ttu-id="2807a-109">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2807a-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="2807a-110">بالنسبة إلى هذا المثال، اكتب BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2807a-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="2807a-111">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-112">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="2807a-112">Select STD.</span></span> <span data-ttu-id="2807a-113">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="2807a-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="2807a-114">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-115">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="2807a-115">For example, select Audio.</span></span> <span data-ttu-id="2807a-116">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="2807a-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="2807a-117">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-118">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="2807a-118">Select SiteWH.</span></span> <span data-ttu-id="2807a-119">سيتم استخدام الموقع والمستودع فقط لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="2807a-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="2807a-120">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-121">لن يتم استخدام أبعاد التعقب لهذا المثال، حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="2807a-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="2807a-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2807a-122">Click OK.</span></span>
9. <span data-ttu-id="2807a-123">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="2807a-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="2807a-124">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="2807a-124">Click Default order settings.</span></span>
11. <span data-ttu-id="2807a-125">في الحقل "نوع الأمر الافتراضي"، حدد "الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="2807a-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="2807a-126">لأن هذا المنتج عبارة عن منتج غير نهائي سيتم إنتاجه، حدد "الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="2807a-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="2807a-127">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-128">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="2807a-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="2807a-129">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-130">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="2807a-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="2807a-131">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-132">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="2807a-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="2807a-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2807a-133">Close the page.</span></span>
16. <span data-ttu-id="2807a-134">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="2807a-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="2807a-135">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="2807a-135">Click Item price.</span></span>
18. <span data-ttu-id="2807a-136">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2807a-136">Click New.</span></span>
19. <span data-ttu-id="2807a-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2807a-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="2807a-138">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="2807a-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-139">بالنسبة إلى هذا المثال، حدد الإصدار 10.</span><span class="sxs-lookup"><span data-stu-id="2807a-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="2807a-140">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-141">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="2807a-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="2807a-142">قم بتعيين "السعر" إلى "10"</span><span class="sxs-lookup"><span data-stu-id="2807a-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="2807a-143">بالنسبة إلى هذا المثال، اكتب سعر تكلفة من 10.</span><span class="sxs-lookup"><span data-stu-id="2807a-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="2807a-144">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2807a-144">Click Save.</span></span>
24. <span data-ttu-id="2807a-145">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="2807a-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="2807a-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2807a-146">Close the page.</span></span>
26. <span data-ttu-id="2807a-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2807a-147">Close the page.</span></span>
27. <span data-ttu-id="2807a-148">انقر فوق BOM_2 لفتحه.</span><span class="sxs-lookup"><span data-stu-id="2807a-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="2807a-149">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="2807a-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="2807a-150">في حقل "مجموعة التكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2807a-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="2807a-151">بالنسبة إلى هذا المثال، حدد "مجموعة التكلفة M1".</span><span class="sxs-lookup"><span data-stu-id="2807a-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="2807a-152">استخدام الاختصار لحفظ سجل.</span><span class="sxs-lookup"><span data-stu-id="2807a-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="2807a-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2807a-153">Close the page.</span></span>


