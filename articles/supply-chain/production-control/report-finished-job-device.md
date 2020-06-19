---
title: إبلاغ عن الانتهاء من جهاز بطاقة الوظيفة
description: يصف هذا الموضوع كيفية تكوين النظام لتمكين مستخدمي جهاز بطاقة وظيفة من إرسال تقرير عن المنتجات المنتهية من أمر الإنتاج إلى المخزون.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403252"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="e9ffa-103">إبلاغ عن الانتهاء من جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="e9ffa-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9ffa-104">يستخدم العاملون صفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة للإعلام عن الكميات التي تم إكمالها لوظيفة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="e9ffa-105">التحكم في إضافة الكميات التي تم الإبلاغ عنها كمنتهية إلى المخزون</span><span class="sxs-lookup"><span data-stu-id="e9ffa-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="e9ffa-106">للتحكم في ما إذا كان يجب إضافة الكميات التي تم الإبلاغ عنها كمنتهية في العملية الأخيرة إلى المخزون أم لا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="e9ffa-107">انتقل إلى **التحكم في المنتج \> الإعداد‏‎ \> تنفيذ التصنيع \> الإعدادات الافتراضية لأمر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="e9ffa-108">على علامة التبويب **الإبلاغ كمنتهٍ‬**، قم بتعيين الحقل **تحديث تقرير الانتهاء عبر الإنترنت** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9ffa-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="e9ffa-109">**لا** – لن تتم إضافة أي كمية إلى المخزون عند الإبلاغ عن الكميات في العملية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="e9ffa-110">لن تتغير حالة أمر الإنتاج إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="e9ffa-111">**الحالة + الكمية** – ستتغير حالة أمر الإنتاج إلى *الإبلاغ كمنتهٍ*، وسيتم الإبلاغ عن الكمية كمنتهية في المخزون.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="e9ffa-112">**الكمية** – سيتم الإبلاغ عن الكمية كمنتهية في المخزون، ولكن حالة أمر الإنتاج لن تتغير إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="e9ffa-113">**الحالة** – حالة أمر الإنتاج وحدها هي التي ستتغير.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="e9ffa-114">لن تتم إضافة أي كميات إلى المخزون عند الإبلاغ عن الكميات في العملية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="e9ffa-115">لا يتم تعقب الكميات في المخزون إذا لم يتم تعريف العمليات التي يتم الإبلاغ عنها كمنتهية على أنها العملية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="e9ffa-116">ومع ذلك، يمكن استخدام هذه الكميات لعرض التقدم.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="e9ffa-117">كما يمكن تضمينها في القواعد التي تتحكم في إمكانية بدء العاملين العملية التالية قبل الوصول إلى الحد معرّف للكميات المبلغ عنها في العملية السابقة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="e9ffa-118">يمكنك تحديد هذه القواعد على علامة تبويب **التحقق من صحة الكمية** في صفحة **الإعدادات الافتراضية لأمر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="e9ffa-119">لمزيد من المعلومات حول كيفية العمل مع صفحة **الإعدادات الافتراضية لأمر الإنتاج**، راجع [محددات الإنتاج لتنفيذ التصنيع‬](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="e9ffa-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="e9ffa-120">الإبلاغ عن أصناف تتحكم بها الدُفعات كمنتهية</span><span class="sxs-lookup"><span data-stu-id="e9ffa-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="e9ffa-121">يدعم جهاز بطاقة الوظيفة ثلاثة سيناريوهات لإعداد تقارير حول الأصناف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="e9ffa-122">تنطبق هذه السيناريوهات على الأصناف التي تم تمكينها لعمليات المستودعات المتقدمة والأصناف التي لم يتم تمكينها لعمليات المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="e9ffa-123">**أرقام الدُفعات المعيّنة يدويًا:** يُدخل العاملون رقم دُفعة مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="e9ffa-124">قد يكون رقم الدُفعة هذا من مصدر خارجي غير معروف من قبل النظام.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="e9ffa-125">**أرقام الدُفعات المعرّفة مسبقًا:** يحدد العاملون رقم دُفعة في قائمة من أرقام دُفعات يقوم النظام بإنشائها تلقائيًا قبل إصدار أمر الإنتاج إلى جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="e9ffa-126">**أرقام الدُفعات الثابتة:** لا يُدخل العاملون أو لا يحددون رقم دُفعة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="e9ffa-127">بدلاً من ذلك، يعيّن النظام بشكل تلقائي رقم دُفعة لأمر الإنتاج قبل إصداره.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="e9ffa-128">لتمكين كل سيناريو، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="e9ffa-129">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e9ffa-130">حدد المنتج المراد تكوينه.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-130">Select the product to configure.</span></span>
1. <span data-ttu-id="e9ffa-131">على علامة التبويب السريعة **إدارة المخزون**، في حقل **مجموعة أرقام الدُفعة‬**، حدد مجموعة أرقام التعقب التي تم إعدادها لدعم السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="e9ffa-132">بشكل افتراضي، إذا لم يتم تعيين مجموعة أرقام الدُفعة‬ إلى منتج يتم التحكم فيه بواسطة الدُفعة، يوفر جهاز بطاقة الوظيفة الإدخال اليدوي لرقم الدُفعة‬ اثناء الإبلاغ عن الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="e9ffa-133">تصف الأقسام الفرعية التالية كيفية إعداد مجموعات أرقام التعقب لدعم كل واحد من السيناريوهات لإعداد تقارير عن أصناف الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="e9ffa-134">تمكين الإبلاغ عن أرقام الدُفعات على جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="e9ffa-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="e9ffa-135">لتمكين أجهزة بطاقة الوظائف لقبول رقم دُفعة أثناء إبلاغ عن الانتهاء، يجب استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="e9ffa-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="e9ffa-136">تجربة مستخدم محسنة لمربع حوار "الإبلاغ عن مدى التقدم" في جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="e9ffa-137">أدخل رقم الدُفعة والأرقام التسلسلية أثناء إبلاغ عن الانتهاء من جهاز بطاقة الوظيفة (معاينة).</span><span class="sxs-lookup"><span data-stu-id="e9ffa-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="e9ffa-138">إعداد مجموعة أرقام تعقب تتيح للعاملين تعيين رقم دُفعة</span><span class="sxs-lookup"><span data-stu-id="e9ffa-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="e9ffa-139">للسماح بأرقام الدُفعات المعيّنة يدويًا، اتبع هذه الخطوات لإعداد مجموعة أرقام التعقب:</span><span class="sxs-lookup"><span data-stu-id="e9ffa-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="e9ffa-140">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="e9ffa-141">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="e9ffa-142">على علامة التبويب السريعة **عام**، عيّن الخيار **يدوي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="e9ffa-143">![صفحة مجموعات أرقام التعقب](media/tracking-number-group-manual.png "صفحة مجموعات أرقام التعقب")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="e9ffa-144">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام الدُفعات للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="e9ffa-145">عندما تستخدم هذا السيناريو، فإن حقل **رقم الدُفعة** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة هو مربع نص يسمح للعاملين بإدخال أي قيمة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="e9ffa-146">![صفحة الإبلاغ عن مدى التقدم مع حقل لأرقام الدُفعات اليدوية](media/job-card-device-batch-manual.png "صفحة الإبلاغ عن مدى التقدم مع حقل لأرقام الدُفعات اليدوية")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="e9ffa-147">إعداد مجموعة أرقام تعقب توفر قائمة بأرقام الدُفعات المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="e9ffa-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="e9ffa-148">لتوفير قائمة بأرقام الدُفعات المعرفة مسبقًا، اتبع هذه الخطوات لإعداد مجموعة أرقام التعقب.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="e9ffa-149">انتقل إلى **إدارة المخزون \> إعداد > الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="e9ffa-150">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="e9ffa-151">على علامة التبويب السريعة **عام**، عيّن الخيار **لحركات المخزون فقط‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="e9ffa-152">استخدم الحقل **لكل كمية‬** لتقسيم أرقام الدُفعات لكل كمية، استنادًا إلى القيمة التي تدخلها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="e9ffa-153">على سبيل المثال، لديك أمر إنتاج لعشر قطع، والحقل **لكل كمية** معيّن إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="e9ffa-154">في هذه الحالة، يتم تعيين خمسه أرقام دُفعات لأمر الإنتاج عند إنشائه.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="e9ffa-155">![صفحة مجموعات أرقام التعقب](media/tracking-number-group-predefined.png "صفحة مجموعات أرقام التعقب")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="e9ffa-156">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام الدُفعات للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="e9ffa-157">عندما تستخدم هذا السيناريو، فإن حقل **رقم الدُفعة** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة هو قائمة منسدلة حيث يتعين على العاملين تحديد قيمة معرّفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="e9ffa-158">![صفحة الإبلاغ عن مدى التقدم مع قائمة من أرقام الدُفعات المعرّفة مسبقًا](media/job-card-device-batch-predefined.png "صفحة الإبلاغ عن مدى التقدم مع قائمة من أرقام الدُفعات المعرّفة مسبقًا")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="e9ffa-159">إعداد مجموعة أرقام تعقب تعيّن أرقام الدُفعات بشكل تلقائي</span><span class="sxs-lookup"><span data-stu-id="e9ffa-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="e9ffa-160">إذا كان يجب تعيين أرقام الدُفعات بشكل تلقائي، من دون إدخال من قبل العامل، اتبع هذه الخطوات لإعداد مجموعة أرقام تعقب.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="e9ffa-161">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="e9ffa-162">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="e9ffa-163">على علامة التبويب السريعة **عام**، عيّن الخيار **لحركات المخزون فقط‬** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="e9ffa-164">قم بتعيين الخيار **يدوي** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="e9ffa-165">![صفحة مجموعات أرقام التعقب](media/tracking-number-group-fixed.png "صفحة مجموعات أرقام التعقب")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="e9ffa-166">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام الدُفعات للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="e9ffa-167">عندما تستخدم هذا السيناريو، فإن حقل **رقم الدُفعة** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة يوفر قيمة، ولكن يتعذر على العاملين تحريرها.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="e9ffa-168">![صفحة الإبلاغ عن مدى التقدم مع رقم دُفعة ثابت](media/job-card-device-batch-fixed.png "صفحة الإبلاغ عن مدى التقدم مع رقم دُفعة ثابت")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="e9ffa-169">الإبلاغ عن الانتهاء إلى لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="e9ffa-169">Report as finished to a license plate</span></span>

<span data-ttu-id="e9ffa-170">بإمكان عمليات المستودعات المتقدمة استخدام بُعد لوحة الترخيص لتعقب المخزون على مواقع المستودعات التي تم إعدادها لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="e9ffa-171">في هذه الحالة، يكون رقم لوحة الترخيص مطلوبًا عندما يقوم أحد العمال بالإبلاغ عن الكميات كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="e9ffa-172">تمكين تقرير لوحة الترخيص وطباعة البطاقات</span><span class="sxs-lookup"><span data-stu-id="e9ffa-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="e9ffa-173">لاستخدام الميزات الموضحة التي تم وصفها هذا القسم، يجب استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="e9ffa-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="e9ffa-174">لوحة الترخيص للإبلاغ عند الانتهاء والمضافة إلى ‏‫جهاز بطاقة الوظيفة‬</span><span class="sxs-lookup"><span data-stu-id="e9ffa-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="e9ffa-175">تمكين إنشاء رقم لوحة الترخيص عند الإبلاغ عن الانتهاء في ‏‫جهاز بطاقة الوظيفة‬ بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="e9ffa-176">طباعة التسمية من جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="e9ffa-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="e9ffa-177">إعداد الإبلاغ عن الانتهاء إلى لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="e9ffa-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="e9ffa-178">للتحكم فيما إذا كان يجب على العاملين إعادة استخدام لوحة ترخيص موجودة أو إنشاء لوحة ترخيص جديدة عند الإبلاغ عن الكميات كمنتهية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="e9ffa-179">انتقل إلى **التحكم بالإنتاج \> إعداد \> تنفيذ التصنيع \> تكوين بطاقة الوظيفة للأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="e9ffa-180">عيّن الخيارات التالية لكل جهاز:</span><span class="sxs-lookup"><span data-stu-id="e9ffa-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="e9ffa-181">**إنشاء لوحة الترخيص** – قم بتعيين هذا الخيار إلى **نعم** لإنشاء لوحة ترخيص جديدة لكل تقرير كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="e9ffa-182">عيّن هذا الخيار إلى **لا** إذا كان من الضروري استخدام لوحة ترخيص موجودة لكل عملية إبلاغ كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="e9ffa-183">**طباعة البطاقة** – عيّن هذا الخيار إلى **نعم** إذا كان يجب على العامل طباعة بطاقة‏‎ لوحة ترخيص لكل عملية إبلاغ عن الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="e9ffa-184">عيّن هذا الخيار إلى **لا** إذا لم تكن البطاقة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="e9ffa-185">![صفحة تكوين بطاقة الوظيفة للأجهزة](media/config-job-card-raf.png "صفحة تكوين بطاقة الوظيفة للأجهزة")</span><span class="sxs-lookup"><span data-stu-id="e9ffa-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="e9ffa-186">لتكوين البطاقة، انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> توجيه المستند**.</span><span class="sxs-lookup"><span data-stu-id="e9ffa-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="e9ffa-187">لمزيد من المعلومات، راجع [تمكين طباعة بطاقة لوحة الترخيص](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="e9ffa-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
