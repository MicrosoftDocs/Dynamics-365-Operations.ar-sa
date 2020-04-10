---
title: تسلسل وظائف الإنتاج للتصنيع التحويلي
description: يستخدم هذا الإجراء منتجات الطلاء كمثال لإظهار كيفية تسلسل الأوامر المخططة وفقًا لأولوية اللون وحجم الحزمة.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 872b9733e18945ca2ff047820afd122025575601
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148774"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="da748-103">تسلسل وظائف الإنتاج للتصنيع التحويلي</span><span class="sxs-lookup"><span data-stu-id="da748-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da748-104">يستخدم هذا الإجراء منتجات الطلاء كمثال لإظهار كيفية تسلسل الأوامر المخططة وفقًا لأولوية اللون وحجم الحزمة.</span><span class="sxs-lookup"><span data-stu-id="da748-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="da748-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USPI.</span><span class="sxs-lookup"><span data-stu-id="da748-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="da748-106">هذا الإجراء مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="da748-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="da748-107">قم بتشغيل التخطيط الرئيسي لـ USPI</span><span class="sxs-lookup"><span data-stu-id="da748-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="da748-108">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > تشغيل > التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da748-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="da748-109">في الحقل "الخطة الرئيسية‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="da748-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="da748-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="da748-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da748-111">حدد المخطط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da748-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="da748-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da748-112">Click OK.</span></span>
    * <span data-ttu-id="da748-113">وهذا يبدأ "المخطط الرئيسي"، بما في ذلك عملية التسلسل.</span><span class="sxs-lookup"><span data-stu-id="da748-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="da748-114">قد تستغرق هذه العملية بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="da748-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="da748-115">عرض الطلبات المخططة لمنتجات الطلاء</span><span class="sxs-lookup"><span data-stu-id="da748-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="da748-116">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > الطلبات المخططة.</span><span class="sxs-lookup"><span data-stu-id="da748-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="da748-117">قم بتوسيع مربع حقائق تفاصيل الصنف.</span><span class="sxs-lookup"><span data-stu-id="da748-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="da748-118">قم بتوسيع مربع حقائق التفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="da748-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="da748-119">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="da748-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="da748-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="da748-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da748-121">حدد المخطط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da748-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="da748-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="da748-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="da748-123">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P300".</span><span class="sxs-lookup"><span data-stu-id="da748-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="da748-124">قم بإلغاء التأمين للتمرير إلى اليمين لعرض تاريخ الطلب وتاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="da748-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="da748-125">لاحظ أن هذه العناصر لها تاريخ طلب اليوم وتواريخ تسليم للطلبات المخططة غير متسلسلة بعد أولوية اللون وحجم الحزمة، كما هو موضح في اسم المنتج.</span><span class="sxs-lookup"><span data-stu-id="da748-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="da748-126">يمكنك المرور فوق رقم صنف لرؤية اسم المنتج والأولوية.</span><span class="sxs-lookup"><span data-stu-id="da748-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="da748-127">تسلسل الطلبات المخططة للطلاء</span><span class="sxs-lookup"><span data-stu-id="da748-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="da748-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da748-128">Close the page.</span></span>
2. <span data-ttu-id="da748-129">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > الطلبات المخططة المتسلسلة.</span><span class="sxs-lookup"><span data-stu-id="da748-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="da748-130">قم بتوسيع مربع حقائق تفاصيل الصنف.</span><span class="sxs-lookup"><span data-stu-id="da748-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="da748-131">قم بتوسيع مربع حقائق التفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="da748-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="da748-132">ملاحظة: هنا ترى التاريخ/وقت البدء للطلبات المخططة مسلسلة وفقًا للون وحجم الحزمة خلال فترة زمنية مقدرها 28 يومًا.</span><span class="sxs-lookup"><span data-stu-id="da748-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="da748-133">يتم تعريف هذه الفترات برقم في الحملة الميدانية.</span><span class="sxs-lookup"><span data-stu-id="da748-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="da748-134">يعمل نموذج أمر مخطط مسلسل كنموذج طلب مخطط نموذجي، ويمكن لمخطط الإنتاج تأكيد الطلبات المخططة هنا.</span><span class="sxs-lookup"><span data-stu-id="da748-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="da748-135">ضع علامة على كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="da748-135">Mark all rows.</span></span>
6. <span data-ttu-id="da748-136">انقر فوق "قبول".</span><span class="sxs-lookup"><span data-stu-id="da748-136">Click Accept.</span></span>
    * <span data-ttu-id="da748-137">سيعمل هذا على تحديث الأوامر المخططة بإجراء التسلسل المحدد للمؤجل أو المتقدم.</span><span class="sxs-lookup"><span data-stu-id="da748-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="da748-138">تحقق من تسلسل الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="da748-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="da748-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da748-139">Close the page.</span></span>
2. <span data-ttu-id="da748-140">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > الطلبات المخططة.</span><span class="sxs-lookup"><span data-stu-id="da748-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="da748-141">قم بتوسيع مربع حقائق تفاصيل الصنف.</span><span class="sxs-lookup"><span data-stu-id="da748-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="da748-142">قم بتوسيع مربع حقائق التفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="da748-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="da748-143">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="da748-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="da748-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="da748-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da748-145">حدد المخطط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da748-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="da748-146">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="da748-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="da748-147">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P300".</span><span class="sxs-lookup"><span data-stu-id="da748-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="da748-148">لاحظ أن تسلسل الطلبات الآن متسلسلة وفقًا لأولوية اللون والحجم وبدء الطلبات المخططة في تاريخ الطلب الأحدث وتاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="da748-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="da748-149">تحقق من عمود تاريخ الطلب أو تاريخ البدء في مربع حقائق تفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="da748-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

