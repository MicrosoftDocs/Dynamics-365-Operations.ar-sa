---
title: "تسجيل استهلاك المواد باستخدام جهاز محمول"
description: "يصف هذا الموضوع سير عمل يمكّن تسجيل استهلاك المواد الخام في الإنتاج باستخدام جهاز محمول باليد."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f948b8f1d846a009afe59e39ff3772d4d1fed9bf
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="f3851-103">تسجيل استهلاك المواد باستخدام جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="f3851-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="f3851-104">يصف هذا الموضوع سير عمل يمكّن تسجيل استهلاك المواد الخام في الإنتاج باستخدام جهاز محمول باليد.</span><span class="sxs-lookup"><span data-stu-id="f3851-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="f3851-105">مقدمة</span><span class="sxs-lookup"><span data-stu-id="f3851-105">Introduction</span></span>
------------

<span data-ttu-id="f3851-106">يعتبر سير العمل هذا مناسبًا عند وجود متطلبات صارمة تتعلق بقابلية تعقب المواد.</span><span class="sxs-lookup"><span data-stu-id="f3851-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="f3851-107">وفي تلك الحالات، يجب أن يتم الإعلام عن وقت الاستهلاك وكميته بشكل دقيق للمحافظة على قابلية تعقب المواد.</span><span class="sxs-lookup"><span data-stu-id="f3851-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="f3851-108">يمكن اعتبار هذه العملية على أنها معاكسة لعمليات التفريغ المسبق والتفريغ الخلفي، حيث توجد إزاحة بين وقت التسجيل والوقت الذي يحدث فيه الاستهلاك الفعلي.</span><span class="sxs-lookup"><span data-stu-id="f3851-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="f3851-109">وهذا يشرح سبب عدم إمكانية استخدام استراتيجية الاستهلاك التلقائي لبعض المواد ذات متطلبات قابلية التعقب.</span><span class="sxs-lookup"><span data-stu-id="f3851-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="f3851-110">لنلقِ نظرة على سيناريو بسيط يوضح كيفية إعداد سير عمل لتمكين تسجيل استهلاك المواد الخام في الإنتاج باستخدام جهاز محمول باليد.</span><span class="sxs-lookup"><span data-stu-id="f3851-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="f3851-111">[![إعداد سير عمل لتمكين تسجيل استهلاك المواد الخام باستخدام جهاز محمول باليد](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="f3851-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="f3851-112">تفاصيل السيناريو</span><span class="sxs-lookup"><span data-stu-id="f3851-112">Scenario details</span></span>

<span data-ttu-id="f3851-113">تستهلك عملية إنتاج مستمرة (5) المواد الخام RM-100 التي يتم التحكم فيها بواسطة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="f3851-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="f3851-114">تكون المواد متوفرة في مجموعة المواقع 001 (1) على لوحة الترخيص PL-1 مع دفعتين، B1 وB2، كميتهما بمقدار 100 رطل.</span><span class="sxs-lookup"><span data-stu-id="f3851-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="f3851-115">يتم إصدار عمل المستودع (2) ومعالجته من أجل RM-100، ويتم انتقاء المواد من Bulk-001 إلى موقع إدخال الإنتاج PIL-01 (3)، المحدد على أنه خاضع لتحكم لوحة غير لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="f3851-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="f3851-116">يزن عامل تشغيل الجهاز المواد من موقع إدخال الإنتاج (3) ويقوم بتسجيل الوزن ورقم الدُفعة عند استهلاكها (4).</span><span class="sxs-lookup"><span data-stu-id="f3851-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="f3851-117">من موقع إدخال الإنتاج، يُضاف جزء من المواد يدويًا إلى عملية الإنتاج خلال فترات زمنية محددة.</span><span class="sxs-lookup"><span data-stu-id="f3851-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="f3851-118">عندما يضيف عامل تشغيل الجهاز المواد، يُقاس وزنها على مقياس ويتم تسجيل رقم الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="f3851-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="f3851-119">إعداد سير العمل لتسجيل الاستهلاك باستخدام جهاز محمول باليد</span><span class="sxs-lookup"><span data-stu-id="f3851-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="f3851-120">قم بإنشاء منتج نهائي جيد، FG-100، مع قائمة مكونات صنف‬ لديها المواد الخام RM-100 التي تتحكم فيها الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="f3851-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="f3851-121">أضف دُفعتين، B1 وB2، من RM-100 في كمية من 100 إلى الموقع: Bulk-001 على لوحة الترخيص: PL-1.</span><span class="sxs-lookup"><span data-stu-id="f3851-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="f3851-122">يتم تعيين قاعدة التفريغ في بند قائمة مكونات الصنف لـ RM-100 إلى **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="f3851-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="f3851-123">قم بتعيين موقع إدخال الإنتاج إلى PIL-01.</span><span class="sxs-lookup"><span data-stu-id="f3851-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="f3851-124">يمكنك القيام بذلك عن طريق تحديد هذا الموقع كموقع إدخال الإنتاج الافتراضي في المستودع 51.</span><span class="sxs-lookup"><span data-stu-id="f3851-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="f3851-125">أنشئ عنصر قائمة جهاز محمول جديدًا:</span><span class="sxs-lookup"><span data-stu-id="f3851-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="f3851-126">**اسم عنصر القائمة** - تسجيل استهلاك المواد.</span><span class="sxs-lookup"><span data-stu-id="f3851-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="f3851-127">**العنوان** - تسجيل استهلاك المواد.</span><span class="sxs-lookup"><span data-stu-id="f3851-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="f3851-128">**الوضع** -غير مباشر.</span><span class="sxs-lookup"><span data-stu-id="f3851-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="f3851-129">**كود النشاط** - تسجيل استهلاك المواد.</span><span class="sxs-lookup"><span data-stu-id="f3851-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="f3851-130">أضف عنصر القائمة إلى قائمة الجهاز **جهاز محمول للإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="f3851-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="f3851-131">قم بإنشاء أمر إنتاج للمنتج النهائي‬:</span><span class="sxs-lookup"><span data-stu-id="f3851-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="f3851-132">**رقم الصنف** - FG-100</span><span class="sxs-lookup"><span data-stu-id="f3851-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="f3851-133">**الموقع** - 5</span><span class="sxs-lookup"><span data-stu-id="f3851-133">**Site** - 5</span></span> 
-    <span data-ttu-id="f3851-134">**المستودع** - 51</span><span class="sxs-lookup"><span data-stu-id="f3851-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="f3851-135">**الكمية** - 150</span><span class="sxs-lookup"><span data-stu-id="f3851-135">**Quantity** - 150</span></span>

<span data-ttu-id="f3851-136">يتم **تقدير** أمر الإنتاج وأيضًا **إصداره** ويتم إنتاج عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="f3851-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="f3851-137">أكمل العمل باستخدام سير العمل لانتقاء المواد الخام للجهاز المحمول باليد.</span><span class="sxs-lookup"><span data-stu-id="f3851-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="f3851-138">يؤدي ذلك إلى إحضار المواد من الموقع الكبير إلى موقع إدخال الإنتاج PIL-01.</span><span class="sxs-lookup"><span data-stu-id="f3851-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="f3851-139">بعد الانتهاء من العمل، تكون حالة المواد **منتقاة في موقع إدخال الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="f3851-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="f3851-140">بإمكان الحالة أن تكون **منتقاة** أو **الفعلي المحجوز** بعد معالجة العمل.</span><span class="sxs-lookup"><span data-stu-id="f3851-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="f3851-141">يتم تكوين ذلك باستخدام المعلمة **حالة الإصدار بعد الوضع في نموذج المستودع**.</span><span class="sxs-lookup"><span data-stu-id="f3851-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="f3851-142">ابدأ أمر الإنتاج من العميل أو من الجهاز المحمول باليد باستخدام عنصر القائمة **بدء الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="f3851-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="f3851-143">بعد بدء أمر الإنتاج، يمكنك تسجيل استهلاك المواد مع سير العمل للجهاز المحمول باليد.</span><span class="sxs-lookup"><span data-stu-id="f3851-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="f3851-144">دعنا نبدأ تسجيل استهلاك 25 رطلاً من الدُفعة B1.</span><span class="sxs-lookup"><span data-stu-id="f3851-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="f3851-145">حدد عنصر القائمة **تسجيل استهلاك** **المواد** في قائمة الجهاز المحمول باليد، وأدخل التفاصيل التالية:</span><span class="sxs-lookup"><span data-stu-id="f3851-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="f3851-146">رقم أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f3851-146">The production order number.</span></span> 
-    <span data-ttu-id="f3851-147">الموقع حيث سيتم استهلاك المواد، في هذه الحالة PIL-01.</span><span class="sxs-lookup"><span data-stu-id="f3851-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="f3851-148">رقم الصنف RM-100.</span><span class="sxs-lookup"><span data-stu-id="f3851-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="f3851-149">رقم الدُفعة B1.</span><span class="sxs-lookup"><span data-stu-id="f3851-149">Batch number B1.</span></span> 
-    <span data-ttu-id="f3851-150">كمية من 25.</span><span class="sxs-lookup"><span data-stu-id="f3851-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="f3851-151">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f3851-151">Select **OK**.</span></span>

<span data-ttu-id="f3851-152">لاحظ ظهور الرسالة "بند دفتر اليومية تم إنشاؤه" على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="f3851-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="f3851-153">في أمر الإنتاج، يوجد دفتر يومية مفتوح من النوع **قائمة انتقاء الإنتاج‬** لرقم الصنف RM-100 ورقم الدُفعة B1.</span><span class="sxs-lookup"><span data-stu-id="f3851-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="f3851-154">يمكنك الآن اختيار متابعة التسجيل، على سبيل المثال على رقم الدُفعة B2، وكلما حددت **موافق،** يُضاف بند دفتر يومية جديد إلى دفتر اليومية المفتوح.</span><span class="sxs-lookup"><span data-stu-id="f3851-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="f3851-155">بعد الانتهاء من التسجيل، حدد **تم** لترحيل دفتر اليومية وإنهاء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="f3851-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="f3851-156">تعليقات إضافية</span><span class="sxs-lookup"><span data-stu-id="f3851-156">Additional comments</span></span> 

-   <span data-ttu-id="f3851-157">إذا ألغى المستخدم سير العمل بعد إنشاء بند دفتر يومية، يعتبر دفتر اليومية في الحالة "غير مرحل"، ولكن إذا قام المستخدم في وقت لاحق باستخدام سير العمل لأمر الإنتاج نفسه، فستُضاف البنود إلى دفتر يومية مفتوح بدلاً من دفتر يومية جديد.</span><span class="sxs-lookup"><span data-stu-id="f3851-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="f3851-158">يدعم سير العمل الجديد أيضًا تسجيل الأرقام المسلسلة.</span><span class="sxs-lookup"><span data-stu-id="f3851-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="f3851-159">يمكن تسجيل فقط رقم الصنف الذي تم تحديده في قائمة مكونات الصنف أو في المعادلة لأمر الإنتاج أو الأمر الدفعي المحدد.</span><span class="sxs-lookup"><span data-stu-id="f3851-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="f3851-160">قد تتعرض المواد لاستهلاك زائد.</span><span class="sxs-lookup"><span data-stu-id="f3851-160">Material can be overconsumed.</span></span> <span data-ttu-id="f3851-161">على سبيل المثال، إذا تم تقدير استهلاك المواد بكمية من 100 رطل، فقد تخضع لاستهلاك زائد إذا كانت الكمية من 105 أرطال، على سبيل المثال.</span><span class="sxs-lookup"><span data-stu-id="f3851-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>


