---
title: إنشاء أمر إنتاج
description: يوضح هذا الإجراء كيفية إنشاء أمر إنتاج.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce08532b8281d730cd5fae4ebd634a08c5baeedd
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826540"
---
# <a name="create-a-production-order"></a><span data-ttu-id="a6677-103">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="a6677-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6677-104">يوضح هذا الإجراء كيفية إنشاء أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="a6677-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="a6677-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a6677-106">هذا هو الإجراء الأول من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="a6677-107">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="a6677-107">Create a production order</span></span>
1. <span data-ttu-id="a6677-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="a6677-109">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="a6677-109">Click New production order.</span></span>
3. <span data-ttu-id="a6677-110">في الحقل "رقم الصنف، اكتب "D0001".</span><span class="sxs-lookup"><span data-stu-id="a6677-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="a6677-111">في الحقل "التسليم"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="a6677-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="a6677-112">يشير تاريخ التسليم إلى وقت انتهاء أمر الإنتاج لتسليمه في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="a6677-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="a6677-113">يمكن استخدام هذا التاريخ في عملية الجدولة.</span><span class="sxs-lookup"><span data-stu-id="a6677-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="a6677-114">على سبيل المثال، يمكنك جدولة الأمر بشكل عكسي من تاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="a6677-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="a6677-115">تعيين الكمية إلى "20".</span><span class="sxs-lookup"><span data-stu-id="a6677-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="a6677-116">ملاحظة: يعرض حقل رقم قائمة مكونات الصنف (BOM) بشكل تلقائي رقم أي BOM نشط للصنف الحالي، ولكن يمكنك تغيير BOM لأمر الإنتاج عن طريق تحديد BOM نشط من قائمة إصدارات BOM المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="a6677-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="a6677-117">يعرض حقل رقم المسار‬ بشكل تلقائي رقم أي مسار نشط للصنف الحالي، ولكن يمكنك تغيير مسار أمر الإنتاج عن طريق تحديد مسار نشط من قائمة إصدارات المسارات المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="a6677-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="a6677-118">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="a6677-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="a6677-119">التحقق من صحة أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a6677-119">Validate the production order</span></span>
1. <span data-ttu-id="a6677-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a6677-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a6677-121">انقر فوق الارتباط الخاص برقم أمر الإنتاج الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="a6677-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="a6677-122">سيؤدي ذلك إلى فتح صفحة التفاصيل للأمر.</span><span class="sxs-lookup"><span data-stu-id="a6677-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="a6677-123">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a6677-123">Click Edit.</span></span>
3. <span data-ttu-id="a6677-124">في الحقل "التسليم"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="a6677-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="a6677-125">على سبيل المثال، يمكنك تغيير تاريخ التسليم لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="a6677-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a6677-126">Click Save.</span></span>
5. <span data-ttu-id="a6677-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a6677-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="a6677-128">تحديث قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="a6677-128">Update the BOM</span></span>
1. <span data-ttu-id="a6677-129">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="a6677-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a6677-130">انقر فوق "قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="a6677-130">Click BOM.</span></span>
    * <span data-ttu-id="a6677-131">افتح صفحة قائمة مكونات الصنف (BOM) للتحقق من صحة بيانات BOM التي تم نسخها من البيانات الافتراضية عند إنشاء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="a6677-132">في هذا الإجراء، تحتاج إلى تحديث كمية BOM.</span><span class="sxs-lookup"><span data-stu-id="a6677-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="a6677-133">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a6677-133">Click Edit.</span></span>
4. <span data-ttu-id="a6677-134">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a6677-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a6677-135">يؤثر تغيير الكمية الموجودة في بند قائمة مكونات الصنف (BOM) على تقدير تكلفة استهلاك المواد لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="a6677-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a6677-136">Click Save.</span></span>
6. <span data-ttu-id="a6677-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a6677-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="a6677-138">تحديث مسار الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a6677-138">Update the production route</span></span>
1. <span data-ttu-id="a6677-139">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="a6677-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a6677-140">انقر فوق "المسار".</span><span class="sxs-lookup"><span data-stu-id="a6677-140">Click Route.</span></span>
    * <span data-ttu-id="a6677-141">افتح صفحة المسار للتحقق من صحة بيانات مسار الإنتاج التي تم نسخها من البيانات الافتراضية عند إنشاء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="a6677-142">في هذا الإجراء، تحتاج إلى تحديث الكمية لإحدى العمليات في مسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="a6677-143">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a6677-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a6677-144">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a6677-144">Click Edit.</span></span>
5. <span data-ttu-id="a6677-145">في الحقل "كمية العمليات‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a6677-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="a6677-146">يؤثر تغيير وقت المعالجة على استهلاك المسار المقدر وتكلفة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6677-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="a6677-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a6677-147">Click Save.</span></span>
7. <span data-ttu-id="a6677-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a6677-148">Close the page.</span></span>

