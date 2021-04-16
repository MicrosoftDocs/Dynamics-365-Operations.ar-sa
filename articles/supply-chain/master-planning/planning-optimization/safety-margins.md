---
title: هوامش الأمان
description: يصف هذا الموضوع كيفيه استخدام هوامش الأمان مع الوظيفة الإضافية تحسين التخطيط لـ Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b66951b9c742af4aa11f681af8f9583a2d97d8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841853"
---
# <a name="safety-margins"></a><span data-ttu-id="3bdb0-103">هوامش الأمان</span><span class="sxs-lookup"><span data-stu-id="3bdb0-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3bdb0-104">يصف هذا الموضوع كيفيه استخدام هوامش الأمان مع الوظيفة الإضافية تحسين التخطيط لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="3bdb0-105">نظره عامة حول هوامش الأمان</span><span class="sxs-lookup"><span data-stu-id="3bdb0-105">Safety margins overview</span></span>

<span data-ttu-id="3bdb0-106">الغرض من هوامش الأمان هو تمكين إجراء إعداد يوفر وقتًا احتياطيًا يتجاوز وقت الإنتاج العادي.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="3bdb0-107">على سبيل المثال، عندما يجب إلغاء تعبئة المواد أو فحصها بعد وصولها من المورّد، لا يمكنك إضافة الوقت الإضافي إلى وقت إنتاج المشتريات، لأن هذا الأسلوب سيمنح الوقت الاحتياطي الإضافي للمورّد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="3bdb0-108">في هذا المثال، يمكن استخدام هامش الاستلام لضمان قيام المورّد بتسليم المواد قبل الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="3bdb0-109">يوفر هذا الأسلوب وقتًا احتياطيًا بحيث يمكن معالجة البضائع داخليًا.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="3bdb0-110">‏‫هناك ثلاثة أنواع من هوامش الأمان:</span><span class="sxs-lookup"><span data-stu-id="3bdb0-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="3bdb0-111">**هامش إعادة الطلب** – الوقت الاحتياطي لتقديم أمر التوريد</span><span class="sxs-lookup"><span data-stu-id="3bdb0-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="3bdb0-112">**هامش الاستلام** -الوقت الاحتياطي لمعالجة التوريد الوارد</span><span class="sxs-lookup"><span data-stu-id="3bdb0-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="3bdb0-113">**هامش الإصدار** – الوقت الاحتياطي لمعالجة الشحنات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="3bdb0-114">يبين الرسم التوضيحي التالي كيفية تطبيق هوامش الأمان مع مرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-114">The following illustration shows how these safety margins apply over time.</span></span>

![هوامش الأمان](media/safety-margins-1.png)

<span data-ttu-id="3bdb0-116">يتم تحديد كافة الهوامش بالأيام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-116">All margins are defined in days.</span></span> <span data-ttu-id="3bdb0-117">تشير القيمة الافتراضية *0* (صفر) إلى عدم تطبيق أي هامش.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="3bdb0-118">إذا قمت بإعداد هوامش متعددة، ستقوم كلها بإضافة الوقت الإجمالي من *تاريخ طلب* التوريد إلى تاريخ *تاريخ متطلبات* الطلب .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="3bdb0-119">على سبيل المثال، الإعداد لا يتضمن وقت إنتاج، وتم تعيين جميع أنواع الهوامش الثلاثة إلى يوم واحد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="3bdb0-120">في هذه الحالة، ستكون هناك ثلاثة أيام بين تاريخ أمر التوريد وتاريخ متطلبات الطلب، وبالتالي إذا كان تاريخ الأمر 1 يوليو، فقد يكون تاريخ المتطلبات 4 يوليو.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="3bdb0-121">هامش الاستلام</span><span class="sxs-lookup"><span data-stu-id="3bdb0-121">Receipt margin</span></span>

<span data-ttu-id="3bdb0-122">هامش الاستلام هو على الأرجح الهامش الأكثر استخدامًا من هوامش الأمان الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="3bdb0-123">ويتم تطبيقه على *تاريخ التسليم* وبأثر رجعي من *تاريخ المتطلبات*.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="3bdb0-124">بمعنى آخر، يجب استلام المنتجات قبل عدد الأيام المطلوب المحدد لأيام هوامش الاستلام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="3bdb0-125">يوضح الرسم التوضيحي التالي هامش الاستلام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-125">The following illustration highlights the receipt margin.</span></span>

![هامش الاستلام](media/safety-margins-2.png)

<span data-ttu-id="3bdb0-127">يتم استخدام هامش الاستلام عادةً كوقت احتياطي لضمان الوقت لعمليات تسجيل المستودع أو عمليات أخرى تستهلك بعض الوقت التي لم يتم التقاطها كجزء من وقت الإنتاج العام في النظام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="3bdb0-128">بالنسبة للمشتريات، إحدى الميزات هو نقل *تاريخ تسليم* أمر الشراء إلى الأمام وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="3bdb0-129">إذا قمت بزيادة وقت الإنتاج بدلاً من استخدام هامش أمان، ستتم مطالبة المورّد مع ذلك بالتسليم في الدقيقة الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="3bdb0-130">لاحظ أن هامش الاستلام لا يغير *تاريخ المتطلبات* للتوريد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="3bdb0-131">وبالتالي، فإن هامش الاستلام ليس مرئيًا بشكل مباشر عندما تتم مقارنة تواريخ المتطلبات الخاصة بالطلب والتوريد (على سبيل المثال، في صفحة **صافي المتطلبات**).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="3bdb0-132">على سبيل المثال، إذا تم تعيين هامش الاستلام على أربعة أيام، وتمت جدولة بند أمر الشراء للاستلام في اليوم الخامس عشر من الشهر، تقوم الجدولة الرئيسية بحساب تاريخ الاستلام المعدل باعتباره اليوم التاسع عشر من الشهر.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="3bdb0-133">لاحظ عدم تطبيق هامش الاستلام إذا كان المخزون الفعلي مستخدمًا كتوريد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="3bdb0-134">يفترض أن يكون كل المخزون الفعلي متاحًا على الفور، بصرف النظر عن وقت استلامه بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="3bdb0-135">هامش إعادة الطلب</span><span class="sxs-lookup"><span data-stu-id="3bdb0-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="3bdb0-136">**قريبًا:** هذه الميزة غير مدعومة بعد لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="3bdb0-137">وحتى يتم دعمها، ستتم معاملة جميع القيم التي يتم إدخالها للخيار **هامش إعادة الطلب المضاف إلى وقت إنتاج الصنف** على أنها *0* (صفر).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="3bdb0-138">يوضح الرسم التوضيحي التالي هامش إعادة الطلب.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-138">The following illustration highlights the reorder margin.</span></span>

![هامش إعادة الطلب](media/safety-margins-3.png)

<span data-ttu-id="3bdb0-140">يُضاف هامش إعادة الطلب قبل وقت إنتاج الصنف لكافة الأوامر المخططة أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="3bdb0-141">وبالتالي، فهوي يضمن وقتًا إضافيًا لأمر التوريد الذي سيتم تقديمه.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="3bdb0-142">يُستخدم هذا الهامش عادةً كاحتياطي لضمان الوقت لعمليات الموافقة أو عمليات أخرى داخلية مطلوبة أثناء إنشاء أوامر التوريد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="3bdb0-143">يوضع هامش إعادة الطلب بين *تاريخ أمر* التوريد *وتاريخ البدء*.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="3bdb0-144">هامش الإصدار</span><span class="sxs-lookup"><span data-stu-id="3bdb0-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="3bdb0-145">**قريبًا:** هذه الميزة غير مدعومة بعد لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="3bdb0-146">وحتى يتم دعمها، ستتم معاملة جميع القيم التي يتم إدخالها للخيار **هامش الإصدار المقتطع من تاريخ المتطلبات** على أنها *0* (صفر).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="3bdb0-147">يوضح الرسم التوضيحي التالي هامش الإصدار.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-147">The following illustration highlights the issue margin.</span></span>

![هامش الإصدار](media/safety-margins-4.png)

<span data-ttu-id="3bdb0-149">يتم اقتطاع هامش الإصدار من تاريخ متطلبات الطلب أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="3bdb0-150">من شأن ذلك أن يساعد على حصولك على الوقت المطلوب للتفاعل مع أوامر الطلب الواردة وشحنها.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="3bdb0-151">يُستخدم هذا الهامش عادة كاحتياطي لضمان الوقت الكافي لعمليات الشحن وعمليات المستودع الصادرة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="3bdb0-152">عند تطبيق هامش إصدار، لا تتطابق تواريخ متطلبات التوريد ومتطلبات الطلب ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="3bdb0-153">بدلاً من ذلك، إنها تختلف مع هامش الإصدار بسبب إضافة هامش الإصدار بين *تاريخ متطلبات* التوريد و *تاريخ متطلبات*.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="3bdb0-154">إعداد هوامش الأمان</span><span class="sxs-lookup"><span data-stu-id="3bdb0-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="3bdb0-155">تشغيل هوامش الأمان في إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="3bdb0-156">قبل أن تتمكن من استخدام هذه الميزة مع تحسين التخطيط، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="3bdb0-157">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3bdb0-158">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="3bdb0-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3bdb0-159">**الوحدة:** _التخطيط الرئيسي_</span><span class="sxs-lookup"><span data-stu-id="3bdb0-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="3bdb0-160">**اسم الميزة:** _هوامش لتحسين التخطيط_</span><span class="sxs-lookup"><span data-stu-id="3bdb0-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="3bdb0-161">تحديد هوامش الأمان</span><span class="sxs-lookup"><span data-stu-id="3bdb0-161">Define safety margins</span></span>

<span data-ttu-id="3bdb0-162">تتميز هوامش الأمان بإعداد مرن.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="3bdb0-163">ويمكن تعيينها على كل من *مجموعة التغطية* و *الخطة الرئيسية*.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="3bdb0-164">من المهم أن تفهم ان الهوامش تُضاف فوق بعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="3bdb0-165">على سبيل المثال، سينتج عن هامش استلام من يومين في مجموعة التغطية وثلاثة أيام في الخطة الرئيسية هامش استلام فعال لخمسة أيام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="3bdb0-166">تعتبر القدرة على تعيين الهامش في الخطة الرئيسية مفيدة إذا كنت ترغب في محاكاة أوقات إنتاج أطول أو عدم اليقين لخطة معينة، ولكن بدون التأثير على التخطيط اليومي.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="3bdb0-167">هوامش أمان مجموعة التغطية</span><span class="sxs-lookup"><span data-stu-id="3bdb0-167">Coverage group safety margins</span></span>

<span data-ttu-id="3bdb0-168">لتطبيق هامش أمان على مجموعة تغطية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="3bdb0-169">انتقل إلى **التخطيط الرئيسي \> الإعداد \> مجموعات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="3bdb0-170">في جزء القائمة، حدد مجموعة التغطية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="3bdb0-171">على علامة التبويب السريعة **غير ذلك**، في القسم **هوامش الأمان بالأيام**، استخدم الحقول التالية لتعيين هوامش الأمان المطلوبة (بالأيام):</span><span class="sxs-lookup"><span data-stu-id="3bdb0-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="3bdb0-172">استلام الهامش المضاف إلى تاريخ المتطلبات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="3bdb0-173">إصدار الهامش المقتطع من تاريخ المتطلبات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="3bdb0-174">تمت إضافة ‏‫هامش حد الطلب‬ إلى وقت إنتاج الصنف</span><span class="sxs-lookup"><span data-stu-id="3bdb0-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="3bdb0-175">هوامش الأمان للخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="3bdb0-175">Master plan safety margins</span></span>

<span data-ttu-id="3bdb0-176">لتطبيق هامش أمان على خطة رئيسية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="3bdb0-177">انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط \> الخطط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="3bdb0-178">في جزء القائمة، حدد الخطة الرئيسية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="3bdb0-179">على علامة التبويب السريعة **هوامش الأمان بالأيام**، استخدم الحقول التالية لتعيين هوامش الأمان المطلوبة (بالأيام):</span><span class="sxs-lookup"><span data-stu-id="3bdb0-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="3bdb0-180">استلام الهامش المضاف إلى تاريخ المتطلبات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="3bdb0-181">إصدار الهامش المقتطع من تاريخ المتطلبات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="3bdb0-182">تمت إضافة ‏‫هامش حد الطلب‬ إلى وقت إنتاج الصنف</span><span class="sxs-lookup"><span data-stu-id="3bdb0-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="3bdb0-183">تحديد ما إذا كانت الحسابات تستند إلى أيام تقويم أو أيام عمل</span><span class="sxs-lookup"><span data-stu-id="3bdb0-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="3bdb0-184">يمكنك تعيين كافة هوامش الأمان بحيث يتم حسابها استنادًا إلى أيام التقويم أو أيام العمل.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="3bdb0-185">انتقل إلى **التخطيط الرئيسي \> إعداد \> محددات التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="3bdb0-186">على علامة التبويب **عام**، في القسم **هوامش الأمان بالأيام**، عيّن خيار **أيام العمل** إلى *نعم* لحساب الهوامش استنادًا إلى أيام العمل.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="3bdb0-187">قم بتعيين الخيار إلى  *لا* لحساب الهوامش استنادًا إلى أيام التقويم.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="3bdb0-188">على سبيل المثال، يُفتح تقويم من الإثنين إلى الجمعة وإغلاقه من السبت حتى الأحد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="3bdb0-189">إذا كان هناك هامش استلام ليوم واحد، فإن تاريخ المتطلبات ليوم الأحد ينتج تاريخ تسليم على يوم الخميس السابق، لأن يومي الجمعة والسبت ليسا أيام عمل.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="3bdb0-190">يعتمد التقويم المستخدم لتحديد أيام العمل على الإعداد ونوع التوريد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="3bdb0-191">ويمكن التحكم فيه بواسطة التقويمات الخاصة بمجموعة التغطية والمستودع والمورّد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="3bdb0-192">إذا لم يكن *المستودع* جزءًا من بُعد التغطية (بمعنى آخر، يستند التخطيط إلى *الموقع* فقط)، ولا يتم استخدام تقويم المستودع.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="3bdb0-193">يمكن للنظام معالجة إعداد حيث يتم تعريف تقويم واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="3bdb0-194">تصف الأقسام الفرعية التالية التركيبات الممكنة التي يمكن استخدامها للتحكم في النتيجة.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="3bdb0-195">التقويم المستخدم للمدة</span><span class="sxs-lookup"><span data-stu-id="3bdb0-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="3bdb0-196">تتحكم التقويمات المحددة في إجمالي وقت الإنتاج الفعلي في أيام التقويم، من تاريخ أمر التوريد إلى تاريخ متطلبات الطلب.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="3bdb0-197">يتم استخدام ترتيب أولويات التقويم التالية:</span><span class="sxs-lookup"><span data-stu-id="3bdb0-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="3bdb0-198">**وقت إنتاج المشتريات** – يؤخذ في الاعتبار تقويم مجموعة التغطية فقط.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="3bdb0-199">**هامش الاستلام** – يتم استخدام تقويم مجموعة التغطية، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-200">وإلا، يتم استخدام تقويم المستودع.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="3bdb0-201">**هامش الإصدار** – يتم استخدام تقويم مجموعة التغطية، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-202">وإلا، يتم استخدام تقويم المستودع.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="3bdb0-203">**هامش إعادة الطلب** – يؤخذ في الاعتبار تقويم مجموعة التغطية فقط.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="3bdb0-204">التقويم المستخدم للتاريخ النهائي</span><span class="sxs-lookup"><span data-stu-id="3bdb0-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="3bdb0-205">يتم تطبيق القواعد التالية لتحديد ما إذا كان بإمكان محرك التخطيط استخدام تاريخ معين لنوع تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="3bdb0-206">**تاريخ استلام المشتريات** – يتم استخدام تقويم المورّد، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-207">بخلاف ذلك، يتم استخدام تقويم مجموعة التغطية، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-208">إذا لم يتم تحديد أي واحد من هذه التقويمات، يتم استخدام تقويم المستودع.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="3bdb0-209">**تاريخ استلام أمر التحويل** – يتم استخدام تقويم مجموعة التغطية، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-210">وإلا، يتم استخدام تقويم المستودع.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="3bdb0-211">**تاريخ استلام الإنتاج** – يتم استخدام تقويم مجموعة التغطية، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-212">وإلا، يتم استخدام تقويم المستودع.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="3bdb0-213">**اليوم المفتوح لإصدار الطلب** – يتم استخدام تقويم المستودع، في حال تحديده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="3bdb0-214">بخلاف ذلك، يتم استخدام تقويم مجموعة التغطية.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="3bdb0-215">**اليوم المفتوح للأمر** – يتم استخدام تركيبة (تقاطع) من تقويم مجموعة التغطية وتقويم المورّد.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="3bdb0-216">يجب فتح كلا التقويمين لاستخدام التاريخ</span><span class="sxs-lookup"><span data-stu-id="3bdb0-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="3bdb0-217">إذا تم تحديد واحد فقط من هذه التقويمات، يتم استخدام هذا التقويم وحده.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="3bdb0-218">مصفوفة النظرة العامة على إعداد التقويم</span><span class="sxs-lookup"><span data-stu-id="3bdb0-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="3bdb0-219">يقدم الرسم التوضيحي التالي مصفوفة تلخص التقويمات التي يتم تطبيقها عند حساب هوامش الأمان.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="3bdb0-220">(حدد الصورة لفتح نسخه عالية الدقة منها.) يتم استخدام الاختصارات والألوان التالية للإشارة إلى مكان تحديد كل نوع تقويم:</span><span class="sxs-lookup"><span data-stu-id="3bdb0-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="3bdb0-221">**مجموعة التغطية (CG):** أخضر</span><span class="sxs-lookup"><span data-stu-id="3bdb0-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="3bdb0-222">**المستودع (WH):** أصفر</span><span class="sxs-lookup"><span data-stu-id="3bdb0-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="3bdb0-223">**المورّد (V):** أزرق</span><span class="sxs-lookup"><span data-stu-id="3bdb0-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="3bdb0-224">[![مصفوفة النظرة العامة على إعداد التقويم](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="3bdb0-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="3bdb0-225">حساب التأخيرات</span><span class="sxs-lookup"><span data-stu-id="3bdb0-225">Calculating delays</span></span>

<span data-ttu-id="3bdb0-226">يتم تضمين الأنواع الثلاثة لهوامش الأمان عندما يحدد النظام ما إذا تم تأخير الأمر.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="3bdb0-227">على سبيل المثال، وقت إنتاج الصنف هو من يوم واحد وهامش الاستلام من ثلاثة أيام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="3bdb0-228">يتم تعيين أمر مبيعات لهذا الصنف على أنه مطلوب اليوم.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="3bdb0-229">وفي هذه الحالة، يتم حساب التأخير باعتباره *وقت الإنتاج* + *هامش الاستلام* = أربعة أيام.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="3bdb0-230">وبالتالي، إذا كان اليوم هو 14 أغسطس، فإن فترة تأخير من أربعة أيام تُنتج التسليم في 18 أغسطس.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="3bdb0-231">يبين الرسم التوضيحي التالي هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-231">The following illustration shows this example.</span></span>

![مثال تأخير الحساب](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="3bdb0-233">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3bdb0-233">Additional resources</span></span>

[<span data-ttu-id="3bdb0-234">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="3bdb0-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="3bdb0-235">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="3bdb0-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]