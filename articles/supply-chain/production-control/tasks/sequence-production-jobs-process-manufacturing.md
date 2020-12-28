---
title: تسلسل وظائف الإنتاج للتصنيع التحويلي
description: يستخدم هذا الإجراء منتجات الطلاء كمثال لإظهار كيفية تسلسل الأوامر المخططة وفقًا لأولوية اللون وحجم الحزمة.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db2c881f60b6e5251e2bcdf198da9e1c9f39a0e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421326"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="abfad-103">تسلسل وظائف الإنتاج للتصنيع التحويلي</span><span class="sxs-lookup"><span data-stu-id="abfad-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abfad-104">يستخدم هذا الإجراء منتجات الطلاء كمثال لإظهار كيفية تسلسل الأوامر المخططة وفقًا لأولوية اللون وحجم الحزمة.</span><span class="sxs-lookup"><span data-stu-id="abfad-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="abfad-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USPI.</span><span class="sxs-lookup"><span data-stu-id="abfad-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="abfad-106">هذا الإجراء مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="abfad-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="abfad-107">قم بتشغيل التخطيط الرئيسي لـ USPI</span><span class="sxs-lookup"><span data-stu-id="abfad-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="abfad-108">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > تشغيل > التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="abfad-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="abfad-109">في الحقل "الخطة الرئيسية‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="abfad-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="abfad-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="abfad-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="abfad-111">حدد المخطط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="abfad-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="abfad-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="abfad-112">Click OK.</span></span>
    * <span data-ttu-id="abfad-113">وهذا يبدأ "المخطط الرئيسي"، بما في ذلك عملية التسلسل.</span><span class="sxs-lookup"><span data-stu-id="abfad-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="abfad-114">قد تستغرق هذه العملية بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="abfad-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="abfad-115">عرض الطلبات المخططة لمنتجات الطلاء</span><span class="sxs-lookup"><span data-stu-id="abfad-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="abfad-116">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > الطلبات المخططة.</span><span class="sxs-lookup"><span data-stu-id="abfad-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="abfad-117">قم بتوسيع مربع حقائق تفاصيل الصنف.</span><span class="sxs-lookup"><span data-stu-id="abfad-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="abfad-118">قم بتوسيع مربع حقائق التفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="abfad-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="abfad-119">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="abfad-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="abfad-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="abfad-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="abfad-121">حدد المخطط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="abfad-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="abfad-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="abfad-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="abfad-123">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P300".</span><span class="sxs-lookup"><span data-stu-id="abfad-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="abfad-124">قم بإلغاء التأمين للتمرير إلى اليمين لعرض تاريخ الطلب وتاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="abfad-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="abfad-125">لاحظ أن هذه العناصر لها تاريخ طلب اليوم وتواريخ تسليم للطلبات المخططة غير متسلسلة بعد أولوية اللون وحجم الحزمة، كما هو موضح في اسم المنتج.</span><span class="sxs-lookup"><span data-stu-id="abfad-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="abfad-126">يمكنك المرور فوق رقم صنف لرؤية اسم المنتج والأولوية.</span><span class="sxs-lookup"><span data-stu-id="abfad-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="abfad-127">تسلسل الطلبات المخططة للطلاء</span><span class="sxs-lookup"><span data-stu-id="abfad-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="abfad-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="abfad-128">Close the page.</span></span>
2. <span data-ttu-id="abfad-129">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > الطلبات المخططة المتسلسلة.</span><span class="sxs-lookup"><span data-stu-id="abfad-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="abfad-130">قم بتوسيع مربع حقائق تفاصيل الصنف.</span><span class="sxs-lookup"><span data-stu-id="abfad-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="abfad-131">قم بتوسيع مربع حقائق التفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="abfad-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="abfad-132">ملاحظة: هنا ترى التاريخ/وقت البدء للطلبات المخططة مسلسلة وفقًا للون وحجم الحزمة خلال فترة زمنية مقدرها 28 يومًا.</span><span class="sxs-lookup"><span data-stu-id="abfad-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="abfad-133">يتم تعريف هذه الفترات برقم في الحملة الميدانية.</span><span class="sxs-lookup"><span data-stu-id="abfad-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="abfad-134">يعمل نموذج أمر مخطط مسلسل كنموذج طلب مخطط نموذجي، ويمكن لمخطط الإنتاج تأكيد الطلبات المخططة هنا.</span><span class="sxs-lookup"><span data-stu-id="abfad-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="abfad-135">ضع علامة على كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="abfad-135">Mark all rows.</span></span>
6. <span data-ttu-id="abfad-136">انقر فوق "قبول".</span><span class="sxs-lookup"><span data-stu-id="abfad-136">Click Accept.</span></span>
    * <span data-ttu-id="abfad-137">سيعمل هذا على تحديث الأوامر المخططة بإجراء التسلسل المحدد للمؤجل أو المتقدم.</span><span class="sxs-lookup"><span data-stu-id="abfad-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="abfad-138">تحقق من تسلسل الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="abfad-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="abfad-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="abfad-139">Close the page.</span></span>
2. <span data-ttu-id="abfad-140">انتقل إلى التخطيط الرئيسي > التخطيط الرئيسي > الطلبات المخططة.</span><span class="sxs-lookup"><span data-stu-id="abfad-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="abfad-141">قم بتوسيع مربع حقائق تفاصيل الصنف.</span><span class="sxs-lookup"><span data-stu-id="abfad-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="abfad-142">قم بتوسيع مربع حقائق التفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="abfad-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="abfad-143">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="abfad-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="abfad-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="abfad-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="abfad-145">حدد المخطط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="abfad-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="abfad-146">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="abfad-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="abfad-147">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P300".</span><span class="sxs-lookup"><span data-stu-id="abfad-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="abfad-148">لاحظ أن تسلسل الطلبات الآن متسلسلة وفقًا لأولوية اللون والحجم وبدء الطلبات المخططة في تاريخ الطلب الأحدث وتاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="abfad-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="abfad-149">تحقق من عمود تاريخ الطلب أو تاريخ البدء في مربع حقائق تفاصيل الجدول.</span><span class="sxs-lookup"><span data-stu-id="abfad-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

