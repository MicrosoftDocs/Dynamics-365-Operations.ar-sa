---
title: "إنشاء أمر إنتاج"
description: "يوضح هذا الإجراء كيفية إنشاء أمر إنتاج."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 4db56f76c7f8ce0cccf85ab04024d9a1e88a8822
ms.contentlocale: ar-sa
ms.lasthandoff: 02/06/2018

---
# <a name="create-a-production-order"></a><span data-ttu-id="88a12-103">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="88a12-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88a12-104">يوضح هذا الإجراء كيفية إنشاء أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="88a12-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="88a12-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="88a12-106">هذا هو الإجراء الأول من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="88a12-107">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="88a12-107">Create a production order</span></span>
1. <span data-ttu-id="88a12-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="88a12-109">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="88a12-109">Click New production order.</span></span>
3. <span data-ttu-id="88a12-110">في الحقل "رقم الصنف، اكتب "D0001".</span><span class="sxs-lookup"><span data-stu-id="88a12-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="88a12-111">في الحقل "التسليم"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="88a12-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="88a12-112">يشير تاريخ التسليم إلى وقت انتهاء أمر الإنتاج لتسليمه في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="88a12-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="88a12-113">يمكن استخدام هذا التاريخ في عملية الجدولة.</span><span class="sxs-lookup"><span data-stu-id="88a12-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="88a12-114">على سبيل المثال، يمكنك جدولة الأمر بشكل عكسي من تاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="88a12-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="88a12-115">تعيين الكمية إلى "20".</span><span class="sxs-lookup"><span data-stu-id="88a12-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="88a12-116">ملاحظة: يعرض حقل رقم قائمة مكونات الصنف (BOM) بشكل تلقائي رقم أي BOM نشط للصنف الحالي، ولكن يمكنك تغيير BOM لأمر الإنتاج عن طريق تحديد BOM نشط من قائمة إصدارات BOM المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="88a12-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="88a12-117">يعرض حقل رقم المسار‬ بشكل تلقائي رقم أي مسار نشط للصنف الحالي، ولكن يمكنك تغيير مسار أمر الإنتاج عن طريق تحديد مسار نشط من قائمة إصدارات المسارات المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="88a12-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="88a12-118">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="88a12-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="88a12-119">التحقق من صحة أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="88a12-119">Validate the production order</span></span>
1. <span data-ttu-id="88a12-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="88a12-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="88a12-121">انقر فوق الارتباط الخاص برقم أمر الإنتاج الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="88a12-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="88a12-122">سيؤدي ذلك إلى فتح صفحة التفاصيل للأمر.</span><span class="sxs-lookup"><span data-stu-id="88a12-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="88a12-123">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="88a12-123">Click Edit.</span></span>
3. <span data-ttu-id="88a12-124">في الحقل "التسليم"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="88a12-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="88a12-125">على سبيل المثال، يمكنك تغيير تاريخ التسليم لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="88a12-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="88a12-126">Click Save.</span></span>
5. <span data-ttu-id="88a12-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="88a12-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="88a12-128">تحديث قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="88a12-128">Update the BOM</span></span>
1. <span data-ttu-id="88a12-129">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="88a12-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="88a12-130">انقر فوق "قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="88a12-130">Click BOM.</span></span>
    * <span data-ttu-id="88a12-131">افتح صفحة قائمة مكونات الصنف (BOM) للتحقق من صحة بيانات BOM التي تم نسخها من البيانات الافتراضية عند إنشاء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="88a12-132">في هذا الإجراء، تحتاج إلى تحديث كمية BOM.</span><span class="sxs-lookup"><span data-stu-id="88a12-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="88a12-133">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="88a12-133">Click Edit.</span></span>
4. <span data-ttu-id="88a12-134">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="88a12-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="88a12-135">يؤثر تغيير الكمية الموجودة في بند قائمة مكونات الصنف (BOM) على تقدير تكلفة استهلاك المواد لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="88a12-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="88a12-136">Click Save.</span></span>
6. <span data-ttu-id="88a12-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="88a12-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="88a12-138">تحديث مسار الإنتاج</span><span class="sxs-lookup"><span data-stu-id="88a12-138">Update the production route</span></span>
1. <span data-ttu-id="88a12-139">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="88a12-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="88a12-140">انقر فوق "المسار".</span><span class="sxs-lookup"><span data-stu-id="88a12-140">Click Route.</span></span>
    * <span data-ttu-id="88a12-141">افتح صفحة المسار للتحقق من صحة بيانات مسار الإنتاج التي تم نسخها من البيانات الافتراضية عند إنشاء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="88a12-142">في هذا الإجراء، تحتاج إلى تحديث الكمية لإحدى العمليات في مسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="88a12-143">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="88a12-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="88a12-144">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="88a12-144">Click Edit.</span></span>
5. <span data-ttu-id="88a12-145">في الحقل "كمية العمليات‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="88a12-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="88a12-146">يؤثر تغيير وقت المعالجة على استهلاك المسار المقدر وتكلفة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="88a12-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="88a12-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="88a12-147">Click Save.</span></span>
7. <span data-ttu-id="88a12-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="88a12-148">Close the page.</span></span>

