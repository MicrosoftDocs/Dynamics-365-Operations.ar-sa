---
title: إبلاغ عن الانتهاء من جهاز بطاقة الوظيفة
description: يصف هذا الموضوع كيفية تكوين النظام لتمكين مستخدمي جهاز بطاقة وظيفة من إرسال تقرير عن المنتجات المنتهية من أمر الإنتاج إلى المخزون.
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd21bdf532e1e607e66bb8f5ef032f0855c99612
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811620"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="a6ba7-103">إبلاغ عن الانتهاء من جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="a6ba7-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6ba7-104">يستخدم العاملون صفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة للإعلام عن الكميات التي تم إكمالها لوظيفة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span> <span data-ttu-id="a6ba7-105">يصف هذا الموضوع كيفية إعداد مختلف الخيارات التي تضع الطريقة التي يمكن للعاملين من خلالها الإبلاغ عن الانتهاء باستخدام هذه الصفحة وما يحدث بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-105">This topic describes how to set up various options that establish how workers can report as finished using this page and what happens next.</span></span> <span data-ttu-id="a6ba7-106">تتضمن الخيارات ما يلي:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-106">Options include:</span></span>

- <span data-ttu-id="a6ba7-107">التحكم في إمكانية إضافة الكميات التي تم الإبلاغ عنها كمنتهية إلى المخزون وفي كيفية القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-107">Control whether and how quantities that are reported as finished are added to inventory.</span></span>
- <span data-ttu-id="a6ba7-108">التحكم في إمكانية إنشاء أرقام الدُفعات وتطبيقها عند الإبلاغ عن الانتهاء وفي كيفية القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-108">Control whether and how batch numbers are generated and applied when reporting as finished.</span></span>
- <span data-ttu-id="a6ba7-109">التحكم في إمكانية إنشاء الأرقام التسلسلية وتطبيقها عند الإبلاغ عن الانتهاء وفي كيفية القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-109">Control whether and how serial numbers are generated and applied when reporting as finished.</span></span>
- <span data-ttu-id="a6ba7-110">التحكم في إمكانية الإبلاغ عن الانتهاء إلى لوحة ترخيص وفي كيفية القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-110">Control whether and how to report as finished to a license plate.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="a6ba7-111">التحكم في إضافة الكميات التي تم الإبلاغ عنها كمنتهية إلى المخزون</span><span class="sxs-lookup"><span data-stu-id="a6ba7-111">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="a6ba7-112">للتحكم في ما إذا كان يجب إضافة الكميات التي تم الإبلاغ عنها كمنتهية في العملية الأخيرة إلى المخزون أم لا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-112">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="a6ba7-113">انتقل إلى **التحكم في المنتج \> الإعداد‏‎ \> تنفيذ التصنيع \> الإعدادات الافتراضية لأمر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-113">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="a6ba7-114">على علامة التبويب **الإبلاغ كمنتهٍ‬**، قم بتعيين الحقل **تحديث تقرير الانتهاء عبر الإنترنت** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-114">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="a6ba7-115">**لا** – لن تتم إضافة أي كمية إلى المخزون عند الإبلاغ عن الكميات في العملية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-115">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="a6ba7-116">لن تتغير حالة أمر الإنتاج إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-116">The status of the production order will never change.</span></span>
    - <span data-ttu-id="a6ba7-117">**الحالة + الكمية** – ستتغير حالة أمر الإنتاج إلى *الإبلاغ كمنتهٍ*، وسيتم الإبلاغ عن الكمية كمنتهية في المخزون.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-117">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="a6ba7-118">**الكمية** – سيتم الإبلاغ عن الكمية كمنتهية في المخزون، ولكن حالة أمر الإنتاج لن تتغير إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-118">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="a6ba7-119">**الحالة** – حالة أمر الإنتاج وحدها هي التي ستتغير.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-119">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="a6ba7-120">لن تتم إضافة أي كميات إلى المخزون عند الإبلاغ عن الكميات في العملية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-120">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="a6ba7-121">لا يتم تعقب الكميات في المخزون إذا لم يتم تعريف العمليات التي يتم الإبلاغ عنها كمنتهية على أنها العملية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-121">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="a6ba7-122">ومع ذلك، يمكن استخدام هذه الكميات لعرض التقدم.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-122">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="a6ba7-123">كما يمكن تضمينها في القواعد التي تتحكم في إمكانية بدء العاملين العملية التالية قبل الوصول إلى الحد معرّف للكميات المبلغ عنها في العملية السابقة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-123">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="a6ba7-124">يمكنك تحديد هذه القواعد على علامة تبويب **التحقق من صحة الكمية** في صفحة **الإعدادات الافتراضية لأمر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-124">You can define these rules on the **Quantity validation** tab on the **Production order defaults** page.</span></span>

<span data-ttu-id="a6ba7-125">لمزيد من المعلومات حول كيفية العمل مع صفحة **الإعدادات الافتراضية لأمر الإنتاج**، راجع [محددات الإنتاج لتنفيذ التصنيع‬](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="a6ba7-125">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="a6ba7-126">الإبلاغ عن أصناف تتحكم بها الدُفعات كمنتهية</span><span class="sxs-lookup"><span data-stu-id="a6ba7-126">Report batch-controlled items as finished</span></span>

<span data-ttu-id="a6ba7-127">يدعم جهاز بطاقة الوظيفة ثلاثة سيناريوهات لإعداد تقارير حول الأصناف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-127">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="a6ba7-128">تنطبق هذه السيناريوهات على الأصناف التي تم تمكينها لعمليات المستودعات المتقدمة والأصناف التي لم يتم تمكينها لعمليات المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-128">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="a6ba7-129">**أرقام الدُفعات المعيّنة يدويًا** - يُدخل العاملون رقم دُفعة مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-129">**Manually assigned batch numbers** - Workers enter a custom batch number.</span></span> <span data-ttu-id="a6ba7-130">قد يكون رقم الدُفعة هذا من مصدر خارجي غير معروف من قبل النظام.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-130">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="a6ba7-131">**أرقام الدُفعات المعرّفة مسبقًا** - يحدد العاملون رقم دُفعة في قائمة من أرقام دُفعات يقوم النظام بإنشائها تلقائيًا قبل إصدار أمر الإنتاج إلى جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-131">**Predefined batch numbers** - Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="a6ba7-132">**أرقام الدُفعات الثابتة** - لا يُدخل العاملون أو لا يحددون رقم دُفعة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-132">**Fixed batch numbers** - Workers don't enter or select a batch number.</span></span> <span data-ttu-id="a6ba7-133">بدلاً من ذلك، يعيّن النظام بشكل تلقائي رقم دُفعة لأمر الإنتاج قبل إصداره.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-133">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>


### <a name="enable-the-feature-on-your-system"></a><span data-ttu-id="a6ba7-134">تمكين الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="a6ba7-134">Enable the feature on your system</span></span>

<span data-ttu-id="a6ba7-135">لتمكين أجهزة بطاقة الوظائف لقبول رقم دُفعة أثناء إبلاغ عن الانتهاء، يجب استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="a6ba7-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="a6ba7-136">تجربة مستخدم محسنة لمربع حوار "الإبلاغ عن مدى التقدم" في جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="a6ba7-137">يمكنك تمكين إدخال أرقام الدُفعات والأرقام التسلسلية أثناء الإبلاغ عنها كمنتهية من "جهاز بطاقة الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="a6ba7-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device</span></span>

### <a name="configure-products-that-require-batch-number-reporting"></a><span data-ttu-id="a6ba7-138">تكوين المنتجات التي تتطلب الإبلاغ عن رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="a6ba7-138">Configure products that require batch number reporting</span></span>

<span data-ttu-id="a6ba7-139">لتمكين منتج لدعم أي من السيناريوهات المتوفرة التي تتحكم فيها الدُفعات، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-139">To enable a product to support any of the available batch-controlled scenarios, follow these steps:</span></span>

1. <span data-ttu-id="a6ba7-140">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-140">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a6ba7-141">حدد المنتج المراد تكوينه.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-141">Select the product to configure.</span></span>
1. <span data-ttu-id="a6ba7-142">على علامة التبويب السريعة **إدارة المخزون**، في حقل **مجموعة أرقام الدُفعة‬**، حدد مجموعة أرقام التعقب التي تم إعدادها لدعم السيناريو.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-142">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="a6ba7-143">بشكل افتراضي، إذا لم يتم تعيين مجموعة أرقام الدُفعة‬ إلى منتج يتم التحكم فيه بواسطة الدُفعة، يوفر جهاز بطاقة الوظيفة الإدخال اليدوي لرقم الدُفعة‬ اثناء الإبلاغ عن الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-143">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="a6ba7-144">تصف الأقسام التالية كيفية إعداد مجموعات أرقام التعقب لدعم كل واحد من السيناريوهات الثلاثة لإعداد تقارير عن أصناف الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-144">The following sections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="a6ba7-145">إعداد مجموعة أرقام تعقب تتيح للعاملين تعيين رقم دُفعة</span><span class="sxs-lookup"><span data-stu-id="a6ba7-145">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="a6ba7-146">للسماح بأرقام الدُفعات المعيّنة يدويًا، اتبع هذه الخطوات لإعداد مجموعة أرقام التعقب:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-146">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6ba7-147">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-147">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6ba7-148">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-148">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6ba7-149">على علامة التبويب السريعة **عام**، عيّن الخيار **يدوي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-149">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="a6ba7-150">![مجموعة أرقام تعقب لأرقام الدُفعات اليدوية](media/tracking-number-group-manual.png "مجموعة أرقام تعقب لأرقام الدُفعات اليدوية")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-150">![A tracking number group for manual batch numbers](media/tracking-number-group-manual.png "A tracking number group for manual batch numbers")</span></span>

1. <span data-ttu-id="a6ba7-151">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام الدُفعات للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-151">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6ba7-152">عندما تستخدم هذا السيناريو، فإن حقل **رقم الدُفعة** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة هو مربع نص يسمح للعاملين بإدخال أي قيمة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-152">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="a6ba7-153">![صفحة الإبلاغ عن مدى التقدم مع حقل لأرقام الدُفعات اليدوية](media/job-card-device-batch-manual.png "صفحة الإبلاغ عن مدى التقدم مع حقل لأرقام الدُفعات اليدوية")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-153">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="a6ba7-154">إعداد مجموعة أرقام تعقب توفر قائمة بأرقام الدُفعات المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="a6ba7-154">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="a6ba7-155">لتوفير قائمة بأرقام الدُفعات المعرفة مسبقًا، اتبع هذه الخطوات لإعداد مجموعة أرقام التعقب.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-155">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6ba7-156">انتقل إلى **إدارة المخزون \> إعداد > الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-156">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6ba7-157">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-157">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6ba7-158">على علامة التبويب السريعة **عام**، عيّن الخيار **لحركات المخزون فقط‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-158">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="a6ba7-159">استخدم الحقل **لكل كمية‬** لتقسيم أرقام الدُفعات لكل كمية، استنادًا إلى القيمة التي تدخلها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-159">Use the **Per qty** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="a6ba7-160">على سبيل المثال، لديك أمر إنتاج لعشر قطع، والحقل **لكل كمية** معيّن إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-160">For example, you have a production order for ten pieces, and the **Per qty** field is set to *2*.</span></span> <span data-ttu-id="a6ba7-161">في هذه الحالة، يتم تعيين خمسه أرقام دُفعات لأمر الإنتاج عند إنشائه.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-161">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="a6ba7-162">![مجموعة أرقام تعقب لأرقام الدُفعات المعرّفة مسبقًا](media/tracking-number-group-predefined.png "مجموعة أرقام تعقب لأرقام الدُفعات المعرّفة مسبقًا")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-162">![A tracking number group for predefined batch numbers](media/tracking-number-group-predefined.png "A tracking number group for predefined batch numbers")</span></span>

1. <span data-ttu-id="a6ba7-163">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام الدُفعات للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-163">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6ba7-164">عندما تستخدم هذا السيناريو، فإن حقل **رقم الدُفعة** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة هو قائمة منسدلة حيث يتعين على العاملين تحديد قيمة معرّفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-164">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="a6ba7-165">![صفحة الإبلاغ عن مدى التقدم مع قائمة من أرقام الدُفعات المعرّفة مسبقًا](media/job-card-device-batch-predefined.png "صفحة الإبلاغ عن مدى التقدم مع قائمة من أرقام الدُفعات المعرّفة مسبقًا")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-165">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="a6ba7-166">إعداد مجموعة أرقام تعقب تعيّن أرقام الدُفعات بشكل تلقائي</span><span class="sxs-lookup"><span data-stu-id="a6ba7-166">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="a6ba7-167">إذا كان يجب تعيين أرقام الدُفعات بشكل تلقائي، من دون إدخال من قبل العامل، اتبع هذه الخطوات لإعداد مجموعة أرقام تعقب.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-167">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6ba7-168">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-168">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6ba7-169">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-169">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6ba7-170">على علامة التبويب السريعة **عام**، عيّن الخيار **لحركات المخزون فقط‬** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-170">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="a6ba7-171">قم بتعيين الخيار **يدوي** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-171">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="a6ba7-172">![مجموعة أرقام تعقب لأرقام الدُفعات الثابتة](media/tracking-number-group-fixed.png "مجموعة أرقام تعقب لأرقام الدُفعات الثابتة")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-172">![A tracking number group for fixed batch numbers](media/tracking-number-group-fixed.png "A tracking number group for fixed batch numbers")</span></span>

1. <span data-ttu-id="a6ba7-173">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام الدُفعات للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-173">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6ba7-174">عندما تستخدم هذا السيناريو، فإن حقل **رقم الدُفعة** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة يوفر قيمة، ولكن يتعذر على العاملين تحريرها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-174">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="a6ba7-175">![صفحة الإبلاغ عن مدى التقدم مع رقم دُفعة ثابت](media/job-card-device-batch-fixed.png "صفحة الإبلاغ عن مدى التقدم مع رقم دُفعة ثابت")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-175">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-serial-controlled-items-as-finished"></a><span data-ttu-id="a6ba7-176">الإبلاغ عن أصناف تتحكم بها الأرقام التسلسلية كمنتهية</span><span class="sxs-lookup"><span data-stu-id="a6ba7-176">Report serial-controlled items as finished</span></span>

<span data-ttu-id="a6ba7-177">يدعم جهاز بطاقة الوظيفة ثلاثة سيناريوهات لإعداد تقارير حول الأصناف التي تتحكم بها الأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-177">The job card device supports three scenarios for reporting on serial-controlled items.</span></span> <span data-ttu-id="a6ba7-178">تنطبق هذه السيناريوهات على الأصناف التي تم تمكينها لعمليات المستودعات المتقدمة والأصناف التي لم يتم تمكينها لعمليات المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-178">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="a6ba7-179">**أرقام الدُفعات المعيّنة يدويًا** - يُدخل العاملون رقمًا تسلسليًا مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-179">**Manually assigned serial numbers** - Workers enter a custom serial number.</span></span> <span data-ttu-id="a6ba7-180">قد يكون الرقم التسلسلي هذا من مصدر خارجي غير معروف من قبل النظام.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-180">This serial number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="a6ba7-181">**أرقام تسلسلية معرّفة مسبقًا** - يحدد العاملون رقمًا تسلسليًا في قائمة من الأرقام التسلسلية يقوم النظام بإنشائها تلقائيًا قبل إصدار أمر الإنتاج إلى جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-181">**Predefined serial numbers** - Workers select a serial number in a list of serial numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="a6ba7-182">**رقم تسلسلي ثابت** - لا يُدخل العاملون أو لا يحددون رقمًا تسلسليًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-182">**Fixed serial number** - Workers don't enter or select a serial number.</span></span> <span data-ttu-id="a6ba7-183">بدلاً من ذلك، يعيّن النظام بشكل تلقائي رقمًا تسلسليًا لأمر الإنتاج قبل إصداره.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-183">Instead, the system automatically assigns a serial number to the production order before it's released.</span></span>

### <a name="enable-the-feature-on-your-system"></a><span data-ttu-id="a6ba7-184">تمكين الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="a6ba7-184">Enable the feature on your system</span></span>

<span data-ttu-id="a6ba7-185">لتمكين أجهزة بطاقة الوظائف لقبول رقم تسلسلي أثناء إبلاغ عن الانتهاء، يجب استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="a6ba7-185">To enable your job card devices to accept a serial number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="a6ba7-186">تجربة مستخدم محسنة لمربع حوار "الإبلاغ عن مدى التقدم" في جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-186">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="a6ba7-187">يمكنك تمكين إدخال أرقام الدُفعات والأرقام التسلسلية أثناء الإبلاغ عنها كمنتهية من "جهاز بطاقة الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="a6ba7-187">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device</span></span>

### <a name="configure-products-that-require-serial-number-reporting"></a><span data-ttu-id="a6ba7-188">تكوين المنتجات التي تتطلب الإبلاغ عن رقم تسلسلي</span><span class="sxs-lookup"><span data-stu-id="a6ba7-188">Configure products that require serial-number reporting</span></span>

<span data-ttu-id="a6ba7-189">لتمكين منتج لدعم أي من السيناريوهات المتوفرة التي تتحكم فيها الأرقام التسلسلية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-189">To enable a product to support any of the available serial-controlled scenarios, follow these steps:</span></span>

<span data-ttu-id="a6ba7-190">لتمكين كل سيناريو، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-190">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="a6ba7-191">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-191">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a6ba7-192">حدد المنتج المراد تكوينه.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-192">Select the product to configure.</span></span>
1. <span data-ttu-id="a6ba7-193">على علامة التبويب السريعة **إدارة المخزون**، في حقل **مجموعة الأرقام التسلسلية‬**، حدد مجموعة أرقام التعقب التي تم إعدادها لدعم السيناريو.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-193">On the **Manage inventory** FastTab, in the **Serial number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="a6ba7-194">بشكل افتراضي، إذا لم يتم تعيين مجموعة أرقام تسلسلية إلى منتج يتم التحكم فيه بواسطة الأرقام التسلسلية، يوفر جهاز بطاقة الوظيفة الإدخال اليدوي للرقم التسلسلي اثناء الإبلاغ عن الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-194">By default, if no serial number group is assigned to a serial-controlled product, the job card device provides manual entry for the serial number during reporting as finished.</span></span>

<span data-ttu-id="a6ba7-195">تصف الأقسام التالية كيفية إعداد مجموعات أرقام التعقب لدعم كل واحد من السيناريوهات الثلاثة لإعداد تقارير عن الأصناف التي تتحكم فيها الأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-195">The following sections describe how to set up tracking number groups to support each of the three scenarios for reporting on serial-controlled items.</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a><span data-ttu-id="a6ba7-196">إعداد مجموعة أرقام تعقب تتيح للعاملين تعيين رقم تسلسلي يدويًا</span><span class="sxs-lookup"><span data-stu-id="a6ba7-196">Set up a tracking number group that lets workers manually assign a serial number</span></span>

<span data-ttu-id="a6ba7-197">للسماح بالأرقام التسلسلية المعيّنة يدويًا، اتبع هذه الخطوات لإعداد مجموعة أرقام التعقب:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-197">To allow for manually assigned serial numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6ba7-198">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-198">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6ba7-199">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-199">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6ba7-200">على علامة التبويب السريعة **عام**، عيّن الخيار **يدوي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-200">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="a6ba7-201">![صفحة مجموعات أرقام التعقب، الأرقام التسلسلية](media/tracking-number-group-manual-serial.png "صفحة مجموعات أرقام التعقب، الأرقام التسلسلية")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-201">![Tracking number groups page, serial numbers](media/tracking-number-group-manual-serial.png "Tracking number groups page, serial numbers")</span></span>

1. <span data-ttu-id="a6ba7-202">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام تسلسلية للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-202">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6ba7-203">عندما تستخدم هذا السيناريو، فإن حقل **الرقم التسلسلي** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة هو مربع نص يسمح للعاملين بإدخال أي قيمة للرقم التسلسلي.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-203">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value for the serial number.</span></span> <span data-ttu-id="a6ba7-204">عند إدخال قيمة، تتم إضافتها إلى قائمة الأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-204">On entering a value, it is added to the serial number list.</span></span> <span data-ttu-id="a6ba7-205">في هذه القائمة، بإمكان العاملين القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-205">In this list,  workers can do the following:</span></span>

- <span data-ttu-id="a6ba7-206">لوضع علامة على رقم تسلسلي كخردة، حدد زر **الخردة** للصف المناسب.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-206">To mark a serial number as scrapped, select the **Scrap** button for the appropriate row.</span></span> <span data-ttu-id="a6ba7-207">ستتم مطالبة العامل بتقديم **سبب الخطأ**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-207">The worker will be prompted to provide an **Error cause**.</span></span>
- <span data-ttu-id="a6ba7-208">لحذف رقم تسلسلي، حدد الزر **حذف** للصف المناسب.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-208">To delete a serial number, select the **Delete** button for the appropriate row.</span></span>

<span data-ttu-id="a6ba7-209">![صفحة الإبلاغ عن مدى التقدم مع حقل للأرقام التسلسلية اليدوية](media/job-card-device-serial-manual.png "صفحة الإبلاغ عن مدى التقدم مع حقل للأرقام التسلسلية اليدوية")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-209">![Report progress page with a field for manual serial numbers](media/job-card-device-serial-manual.png "Report progress page with a field for manual serial numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a><span data-ttu-id="a6ba7-210">إعداد مجموعة أرقام تعقب توفر قائمة بالأرقام التسلسلية المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="a6ba7-210">Set up a tracking number group that provides a list of predefined serial numbers</span></span>

<span data-ttu-id="a6ba7-211">لتوفير قائمة بالأرقام التسلسلية المعرفة مسبقًا، اتبع هذه الخطوات لإعداد مجموعة أرقام التعقب.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-211">To provide a list of predefined serial numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6ba7-212">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-212">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6ba7-213">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-213">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6ba7-214">على علامة التبويب السريعة **عام**، عيّن الخيار **لحركات المخزون فقط‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-214">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="a6ba7-215">استخدم الحقل **لكل كمية** لتقسيم الأرقام التسلسلية لكل كمية واحدة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-215">Use the **Per qty** field to split serial numbers per quantity of one.</span></span>

    <span data-ttu-id="a6ba7-216">![مجموعة أرقام تعقب للأرقام التسلسلية المعرّفة مسبقًا](media/tracking-number-group-predefined-sn.png "مجموعة أرقام تعقب للأرقام التسلسلية المعرّفة مسبقًا")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-216">![A tracking number group for predefined serial numbers](media/tracking-number-group-predefined-sn.png "A tracking number group for predefined serial numbers")</span></span>

1. <span data-ttu-id="a6ba7-217">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام تسلسلية للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-217">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6ba7-218">عندما تستخدم هذا السيناريو، فإن حقل **الرقم التسلسلي** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة هو قائمة منسدلة حيث يتعين على العاملين تحديد قيمة معرّفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-218">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="a6ba7-219">![صفحة الإبلاغ عن مدى التقدم مع قائمة من الأرقام التسلسلية المعرّفة مسبقًا](media/job-card-device-serial-predefined.png "صفحة الإبلاغ عن مدى التقدم مع قائمة من الأرقام التسلسلية المعرّفة مسبقًا")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-219">![Report progress page with a list of predefined serial numbers](media/job-card-device-serial-predefined.png "Report progress page with a list of predefined serial numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a><span data-ttu-id="a6ba7-220">إعداد مجموعة أرقام تعقب تعيّن الأرقام التسلسلية بشكل تلقائي</span><span class="sxs-lookup"><span data-stu-id="a6ba7-220">Set up a tracking number group that automatically assigns serial numbers</span></span>

<span data-ttu-id="a6ba7-221">إذا كان يجب تعيين رقم تسلسلي بشكل تلقائي، من دون إدخال من قبل العامل، اتبع هذه الخطوات لإعداد مجموعة أرقام تعقب.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-221">If a serial number should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6ba7-222">انتقل إلى **إدارة المخزون \> إعداد \> الأبعاد \> مجموعات أرقام التعقب**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-222">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6ba7-223">أنشئ أو حدد مجموعة أرقام التعقب لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-223">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6ba7-224">على علامة التبويب السريعة **عام**، عيّن الخيار **لحركات المخزون فقط‬** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-224">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="a6ba7-225">قم بتعيين الخيار **يدوي** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-225">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="a6ba7-226">![مجموعة أرقام تعقب للأرقام التسلسلية الثابتة](media/tracking-number-group-fixed-sn.png "مجموعة أرقام تعقب للأرقام التسلسلية الثابتة")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-226">![A tracking number group for fixed serial numbers](media/tracking-number-group-fixed-sn.png "A tracking number group for fixed serial numbers")</span></span>

1. <span data-ttu-id="a6ba7-227">قم بتعيين القيم الأخرى وفق الحاجة، ثم حدد مجموعة أرقام التعقب هذه كمجموعة أرقام تسلسلية للمنتجات الصادرة التي تريد استخدام هذا السيناريو لها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-227">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6ba7-228">عندما تستخدم هذا السيناريو، فإن حقل **الرقم التسلسلي** الذي توفره الصفحة **الإبلاغ عن مدى التقدم** على جهاز بطاقة الوظيفة يوفر قيمة، ولكن يتعذر على العاملين تحريرها.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-228">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span> <span data-ttu-id="a6ba7-229">يكون هذا السيناريو ذا صلة فقط عند إنشاء أمر إنتاج لكمية من قطعة واحد من صنف يتحكم فيه رقم تسلسلي.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-229">This scenario is only relevant when a production order is created for a quantity of one piece of a serial number-controlled item.</span></span>

<span data-ttu-id="a6ba7-230">![صفحة الإبلاغ عن مدى التقدم مع رقم تسلسلي ثابت](media/job-card-device-serial-fixed.png "صفحة الإبلاغ عن مدى التقدم مع أرقام تسلسلية ثابتة")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-230">![Report progress page with a fixed serial number](media/job-card-device-serial-fixed.png "Report progress page with a fixed serial numbers")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="a6ba7-231">الإبلاغ عن الانتهاء إلى لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="a6ba7-231">Report as finished to a license plate</span></span>

<span data-ttu-id="a6ba7-232">بإمكان عمليات المستودعات المتقدمة استخدام بُعد لوحة الترخيص لتعقب المخزون على مواقع المستودعات التي تم إعدادها لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-232">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="a6ba7-233">في هذه الحالة، يكون رقم لوحة الترخيص مطلوبًا عندما يقوم أحد العمال بالإبلاغ عن الكميات كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-233">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="a6ba7-234">تمكين تقرير لوحة الترخيص وطباعة البطاقات</span><span class="sxs-lookup"><span data-stu-id="a6ba7-234">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="a6ba7-235">لاستخدام الميزات الموضحة التي تم وصفها هذا القسم، يجب استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="a6ba7-235">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="a6ba7-236">لوحة الترخيص للإبلاغ عند الانتهاء والمضافة إلى ‏‫جهاز بطاقة الوظيفة‬</span><span class="sxs-lookup"><span data-stu-id="a6ba7-236">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="a6ba7-237">تمكين إنشاء رقم لوحة الترخيص عند الإبلاغ عن الانتهاء في ‏‫جهاز بطاقة الوظيفة‬ بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-237">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="a6ba7-238">طباعة التسمية من جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="a6ba7-238">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="a6ba7-239">إعداد الإبلاغ عن الانتهاء إلى لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="a6ba7-239">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="a6ba7-240">للتحكم فيما إذا كان يجب على العاملين إعادة استخدام لوحة ترخيص موجودة أو إنشاء لوحة ترخيص جديدة عند الإبلاغ عن الكميات كمنتهية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-240">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="a6ba7-241">انتقل إلى **التحكم بالإنتاج \> إعداد \> تنفيذ التصنيع \> تكوين بطاقة الوظيفة للأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-241">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="a6ba7-242">عيّن الخيارات التالية لكل جهاز:</span><span class="sxs-lookup"><span data-stu-id="a6ba7-242">Set the following options for each device:</span></span>

    - <span data-ttu-id="a6ba7-243">**إنشاء لوحة الترخيص** – قم بتعيين هذا الخيار إلى **نعم** لإنشاء لوحة ترخيص جديدة لكل تقرير كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-243">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="a6ba7-244">عيّن هذا الخيار إلى **لا** إذا كان من الضروري استخدام لوحة ترخيص موجودة لكل عملية إبلاغ كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-244">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="a6ba7-245">**طباعة البطاقة** – عيّن هذا الخيار إلى **نعم** إذا كان يجب على العامل طباعة بطاقة‏‎ لوحة ترخيص لكل عملية إبلاغ عن الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-245">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="a6ba7-246">عيّن هذا الخيار إلى **لا** إذا لم تكن البطاقة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-246">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="a6ba7-247">![صفحة تكوين بطاقة الوظيفة للأجهزة](media/config-job-card-raf.png "صفحة تكوين بطاقة الوظيفة للأجهزة")</span><span class="sxs-lookup"><span data-stu-id="a6ba7-247">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="a6ba7-248">لتكوين البطاقة، انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> توجيه المستند**.</span><span class="sxs-lookup"><span data-stu-id="a6ba7-248">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="a6ba7-249">لمزيد من المعلومات، راجع [تمكين طباعة بطاقة لوحة الترخيص](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="a6ba7-249">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]