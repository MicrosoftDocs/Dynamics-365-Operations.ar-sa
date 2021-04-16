---
title: إنشاء أوامر العمل
description: يوضح هذا الموضوع كيفية إنشاء أوامر العمل في إدارة الأصول.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836724"
---
# <a name="creating-work-orders"></a><span data-ttu-id="99e80-103">إنشاء أوامر العمل</span><span class="sxs-lookup"><span data-stu-id="99e80-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99e80-104">بعد أن تنتهي من جدولة مهام الصيانة الوقائية، فإن الخطوة التالية هي إنشاء أوامر عمل لهم.</span><span class="sxs-lookup"><span data-stu-id="99e80-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="99e80-105">يمكنك إكمال هذه الخطوة باستخدام أحد جداول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="99e80-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="99e80-106">قد تتوفر أنواع مراجع مختلفة للمهام المجدولة في جدول صيانة، بالشكل الموصوف في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="99e80-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="99e80-107">نوع المرجع</span><span class="sxs-lookup"><span data-stu-id="99e80-107">Reference type</span></span> | <span data-ttu-id="99e80-108">الوصف</span><span class="sxs-lookup"><span data-stu-id="99e80-108">Description</span></span> |
|---|---|
| <span data-ttu-id="99e80-109">خطط الصيانة</span><span class="sxs-lookup"><span data-stu-id="99e80-109">Maintenance plans</span></span> | <span data-ttu-id="99e80-110">مهام الصيانة الوقائية التي تعتمد على أنواع خطط الصيانة *الوقت* أو *العداد*.</span><span class="sxs-lookup"><span data-stu-id="99e80-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="99e80-111">دورات الصيانة</span><span class="sxs-lookup"><span data-stu-id="99e80-111">Maintenance rounds</span></span> | <span data-ttu-id="99e80-112">مهام الصيانة الوقائية التي تحتوي على عدد كبير من الأصول التي تحتاج إلى نوع صيانة مماثل.</span><span class="sxs-lookup"><span data-stu-id="99e80-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="99e80-113">طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="99e80-113">Maintenance request</span></span> | <span data-ttu-id="99e80-114">طلب يتم إنشاؤه يدويا لصيانة أو لإصلاح أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="99e80-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="99e80-115">يمكن تحويل هذا الطلب إلى أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="99e80-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="99e80-116">إنشاء أوامر العمل وفقا لجدول الصيانة الخاص بك</span><span class="sxs-lookup"><span data-stu-id="99e80-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="99e80-117">لإنشاء أوامر العمل التي تستند إلى جدول الصيانة ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="99e80-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="99e80-118">قم بفتح أحدي الصفحات التالية استنادا إلى الطريقة التي ترغب في تحديدها لتحديد عناصر الجدول لأوامر العمل الخاصة بك:</span><span class="sxs-lookup"><span data-stu-id="99e80-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="99e80-119">كل جدول الصيانة (**أداره الأصول \> جدول الإدارة \> جدول الصيانة**)</span><span class="sxs-lookup"><span data-stu-id="99e80-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="99e80-120">فتح بنود جدول الصيانة (**أداره الأصول \> جدول الإدارة \> فتح بنود جدول الصيانة**)</span><span class="sxs-lookup"><span data-stu-id="99e80-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="99e80-121">فتح مجموعات جدول الصيانة (**أداره الأصول \> جدول الإدارة \> فتح مجموعات جدول الصيانة**)</span><span class="sxs-lookup"><span data-stu-id="99e80-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="99e80-122">في الشبكة، حدد خانه الاختيار لكل وظيفة صيانة مجدولة تريد إنشاء أمر العمل لها.</span><span class="sxs-lookup"><span data-stu-id="99e80-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="99e80-123">بعد ذلك، في جزء الإجراءات، حدد **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="99e80-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="99e80-124">يظهر مربع الحوار **إنشاء أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="99e80-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="99e80-125">يظهر العدد الإجمالي لساعات التنبؤ للبنود المحددة في الحقل **ساعات التنبؤ بمتطلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="99e80-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![مربع الحوار إنشاء أوامر العمل.](media/18-preventive-maintenance.png)

1. <span data-ttu-id="99e80-127">في قسم **المعلمات**، حدد عدد أوامر العمل التي ينبغي إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="99e80-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="99e80-128">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="99e80-128">Select one of the following options:</span></span>

    - <span data-ttu-id="99e80-129">**أمر عمل واحد لكل بند** – يستخدم لإنشاء أمر عمل واحد لكل بند من بنود جدول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="99e80-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="99e80-130">**أمر عمل واحد لكل** – يقوم بإنشاء أوامر العمل التي يتم تجميعها وفقا لإعدادات الخيارات الأخرى التي تصبح متوفرة عند تحديد هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="99e80-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="99e80-131">في الحقل **نوع أمر العمل**، حدد نوع أمر العمل المطلوب استخدامه لكافة أوامر العمل التي تقوم بإنشاءها.</span><span class="sxs-lookup"><span data-stu-id="99e80-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="99e80-132">حدد **موافق** لإنشاء أوامر العمل وفقا للإعدادات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="99e80-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="99e80-133">بنود أمر العمل الخاصة بالمجموعة التي يتم إنشاؤها تلقائيا اثناء تشغيل خطه الصيانة</span><span class="sxs-lookup"><span data-stu-id="99e80-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

<span data-ttu-id="99e80-134">تتيح لك هذه الميزة تعريف قواعد لتجميع بنود أمر العمل تحت أمر عمل واحد عند اعداد النظام لإنشاء أوامر العمل تلقائيا، وذلك استنادا إلى خطه الصيانة.</span><span class="sxs-lookup"><span data-stu-id="99e80-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="99e80-135">وسابقا ، يمكن ان تحتوي أوامر العمل التي تم إنشاؤها تلقائيا علي بند واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="99e80-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="99e80-136">ومع ذلك، يمكنك الآن تجميع أوامر العمل حسب، علي سبيل المثال، الأصل أو نوع الأصل أو موقع وظيفي.</span><span class="sxs-lookup"><span data-stu-id="99e80-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="99e80-137">(يمكن تجميع أوامر العمل المنشاة يدويا بهذه الطريقة كما هو موضح في القسم السابق من هذا الموضوع.)</span><span class="sxs-lookup"><span data-stu-id="99e80-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="99e80-138">تمكين تجميع أوامر العمل التي تم إنشاؤها تلقائيا</span><span class="sxs-lookup"><span data-stu-id="99e80-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="99e80-139">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="99e80-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="99e80-140">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="99e80-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="99e80-141">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="99e80-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="99e80-142">**الوحدة النمطية:** *إدارة الأصول‎*</span><span class="sxs-lookup"><span data-stu-id="99e80-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="99e80-143">**اسم الميزة:** *(إصدار أولي) تطبيق قواعد لتجميع أوامر العمل اثناء تشغيل خطه الصيانة*</span><span class="sxs-lookup"><span data-stu-id="99e80-143">**Feature name:** *Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="99e80-144">إعداد تجميع أوامر العمل التي تم إنشاؤها تلقائيا</span><span class="sxs-lookup"><span data-stu-id="99e80-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="99e80-145">لإعداد تجميع أوامر العمل التي تم إنشاؤها تلقائيا، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="99e80-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="99e80-146">انتقل إلى **إدارة الأصول \> الإعداد \> الصيانة الوقائية \> خطط الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="99e80-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="99e80-147">بالنسبة لكل خطه ترغب في إنشاء أوامر عمل مجمعه لها، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="99e80-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="99e80-148">في جزء القائمة، حدد الخطة الرئيسية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="99e80-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="99e80-149">في علامة التبويب السريعة **البنود**، تاكد من تحديد خانه الاختيار **إنشاء تلقائي** في كل بند.</span><span class="sxs-lookup"><span data-stu-id="99e80-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="99e80-150">انتقل إلى **إدارة الأصول \> دوري \> الصيانة الوقائية \> جدولة خطط الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="99e80-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="99e80-151">في مربع الحوار **جدوله خطط الصيانة**، في القسم **الفترة**، حدد الفترة الزمنيه للخطة (ما هي المدة التي سيتم البحث عنها عند البحث عن مهام الصيانة المجدولة لإنشاء عمل لها).</span><span class="sxs-lookup"><span data-stu-id="99e80-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="99e80-152">قم بتعيين الخيار **إنشاء أمر العمل من الجدول** تلقائيا إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="99e80-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="99e80-153">في القسم **أمر العمل**، حدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="99e80-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="99e80-154">**أمر عمل واحد لكل بند** – يستخدم لإنشاء أمر عمل واحد لكل بند من بنود جدول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="99e80-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="99e80-155">(يوفر هذا الخيار نفس الوظيفة المتاحة عند *تطبيق القواعد الخاصة بتجميع أوامر العمل اثناء إيقاف تشغيل ميزه خطه الصيانة*.)</span><span class="sxs-lookup"><span data-stu-id="99e80-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="99e80-156">**أمر عمل واحد لكل** – يقوم بإنشاء أوامر العمل التي يتم تجميعها وفقا لإعدادات الخيارات الأخرى التي تصبح متوفرة عند تحديد هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="99e80-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="99e80-157">إذا كنت ترغب في تطبيق الخيارات عند تشغيلك لبعض خطط الصيانة فقط ، علي علامة التبويب السريعة **السجلات المراد تضمينها**، قم باضافه عوامل التصفية كما تحتاج، تماما كما هو الحال مع وظائف المجموعة الأخرى في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="99e80-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="99e80-158">في علامة التبويب السريعة **التشغيل في الخلفية**، قم باعداد خيارات المجموعة والجدولة كما طلبت ، تماما كما هو الحال بالنسبة لوظائف المجموعة الأخرى في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="99e80-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="99e80-159">حدد **موافق** لتشغيل و/أو جدوله خطط الصيانة المحددة.</span><span class="sxs-lookup"><span data-stu-id="99e80-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]