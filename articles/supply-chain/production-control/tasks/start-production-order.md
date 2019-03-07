---
title: بدء أمر الإنتاج
description: يوضح هذا الإجراء كيفية بدء أوامر الإنتاج بحالة العمل.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "346216"
---
# <a name="start-a-production-order"></a><span data-ttu-id="94c6d-103">بدء أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="94c6d-103">Start a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94c6d-104">يوضح هذا الإجراء كيفية بدء أوامر الإنتاج بحالة العمل.</span><span class="sxs-lookup"><span data-stu-id="94c6d-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="94c6d-105">يتم الإبلاغ عن استهلاك الوقت والمواد في هذه العملية.</span><span class="sxs-lookup"><span data-stu-id="94c6d-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="94c6d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="94c6d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="94c6d-107">هذا هو الإجراء الخامس من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="94c6d-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="94c6d-108">بدء أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="94c6d-108">Start a production order</span></span>
1. <span data-ttu-id="94c6d-109">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="94c6d-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="94c6d-110">حدد أمر إنتاج يكون في الحالة "تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="94c6d-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="94c6d-111">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="94c6d-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="94c6d-112">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="94c6d-112">Click Start.</span></span>
    * <span data-ttu-id="94c6d-113">في هذه الصفحة، يمكنك تأكيد بدء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="94c6d-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="94c6d-114">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="94c6d-114">Click the General tab.</span></span>
5. <span data-ttu-id="94c6d-115">في حقل "من العملية</span><span class="sxs-lookup"><span data-stu-id="94c6d-115">In the From Oper.</span></span> <span data-ttu-id="94c6d-116">رقم</span><span class="sxs-lookup"><span data-stu-id="94c6d-116">No.</span></span> <span data-ttu-id="94c6d-117">، أدخل "10".</span><span class="sxs-lookup"><span data-stu-id="94c6d-117">field, enter '10'.</span></span>
6. <span data-ttu-id="94c6d-118">في الحقل "استهلاك المسار التلقائي"، حدد "دائمًا".</span><span class="sxs-lookup"><span data-stu-id="94c6d-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="94c6d-119">انقر فوق خانة اختيار "ترحيل بطاقة المسار الآن".</span><span class="sxs-lookup"><span data-stu-id="94c6d-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="94c6d-120">في الحقل "استهلاك قائمة مكونات الصنف"، حدد "دائمًا".</span><span class="sxs-lookup"><span data-stu-id="94c6d-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="94c6d-121">انقر فوق خانة اختيار "ترحيل قائمة الانتقاء الآن".</span><span class="sxs-lookup"><span data-stu-id="94c6d-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="94c6d-122">انقر فوق خانة اختيار "طباعة قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="94c6d-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="94c6d-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="94c6d-123">Click OK.</span></span>
    * <span data-ttu-id="94c6d-124">فيما يلي قائمة الانتقاء المطبوعة التي تبين المواد المستخدمة لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="94c6d-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="94c6d-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="94c6d-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="94c6d-126">التحقق من صحة قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="94c6d-126">Validate the picking list</span></span>
1. <span data-ttu-id="94c6d-127">في جزء "الإجراءات"، انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="94c6d-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="94c6d-128">انقر فوق "قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="94c6d-128">Click Picking list.</span></span>
3. <span data-ttu-id="94c6d-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="94c6d-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="94c6d-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="94c6d-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="94c6d-131">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="94c6d-131">Click Edit.</span></span>
6. <span data-ttu-id="94c6d-132">في الحقل "الاستهلاك"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="94c6d-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="94c6d-133">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="94c6d-133">Click Post.</span></span>
8. <span data-ttu-id="94c6d-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="94c6d-134">Click OK.</span></span>
    * <span data-ttu-id="94c6d-135">في دفتر يومية قائمة الانتقاء، يتم ترحيل المواد المستهلكة بواسطة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="94c6d-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="94c6d-136">قبل ترحيل دفتر اليومية، يمكنك إجراء تعديلات في حالة وجود فرق بين الكمية المقدرة والكمية المستهلكة الفعلية.</span><span class="sxs-lookup"><span data-stu-id="94c6d-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="94c6d-137">انقر فوق علامة التبويب "GridPanel".</span><span class="sxs-lookup"><span data-stu-id="94c6d-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="94c6d-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="94c6d-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="94c6d-139">التحقق من دفتر يومية بطاقة المسار</span><span class="sxs-lookup"><span data-stu-id="94c6d-139">Verify the route card journal</span></span>
1. <span data-ttu-id="94c6d-140">في جزء "الإجراءات"، انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="94c6d-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="94c6d-141">انقر فوق "بطاقة المسار".</span><span class="sxs-lookup"><span data-stu-id="94c6d-141">Click Route card.</span></span>
3. <span data-ttu-id="94c6d-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="94c6d-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="94c6d-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="94c6d-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="94c6d-144">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="94c6d-144">Click Edit.</span></span>
6. <span data-ttu-id="94c6d-145">في الحقل "الساعات" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="94c6d-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="94c6d-146">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="94c6d-146">Click Post.</span></span>
8. <span data-ttu-id="94c6d-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="94c6d-147">Click OK.</span></span>
    * <span data-ttu-id="94c6d-148">في دفتر يومية بطاقة المسار، يتم تسجيل الوقت المستغرق في العمليات الفردية.</span><span class="sxs-lookup"><span data-stu-id="94c6d-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="94c6d-149">ويمكنك أيضا الإبلاغ عن كمية البضائع والأخطاء.</span><span class="sxs-lookup"><span data-stu-id="94c6d-149">Good and error quantity can also be reported.</span></span>  
