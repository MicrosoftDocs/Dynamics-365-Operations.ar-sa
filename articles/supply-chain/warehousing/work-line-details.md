---
title: تفاصيل بنود العمل
description: يوفر هذا الموضوع معلومات حول صفحة تفاصيل بند العمل، التي تُظهر قائمة شاملة وقابلة للفرز وقابلة للتصفية لبنود العمل الفردية في النظام الخاص بك.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245096"
---
# <a name="work-line-details"></a><span data-ttu-id="bad64-103">تفاصيل بنود العمل</span><span class="sxs-lookup"><span data-stu-id="bad64-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bad64-104">تعرض صفحة **تفاصيل بند العمل** قائمة شاملة وقابلة للفرز وقابلة للتصفية لبنود العمل الفردية في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="bad64-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="bad64-105">وتوفر نظرة عامة كاملة حول العمل الذي يجري التخطيط له وتنفيذه في المستودع.</span><span class="sxs-lookup"><span data-stu-id="bad64-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="bad64-106">يمكنك التبديل بسهولة بين عرض كافة بنود العمل وعرض بنود العمل المفتوحة فقط.</span><span class="sxs-lookup"><span data-stu-id="bad64-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="bad64-107">تتضمن التفاصيل المتوفرة لكل بند حالة العمل ورقم الصنف والموقع وكمية العمل ومعرف الحمل ومعرف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="bad64-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="bad64-108">تشغيل ميزة تفاصيل بند العمل</span><span class="sxs-lookup"><span data-stu-id="bad64-108">Turn on the work line details feature</span></span>

<span data-ttu-id="bad64-109">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="bad64-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="bad64-110">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bad64-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bad64-111">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="bad64-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bad64-112">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="bad64-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bad64-113">**اسم الميزة:** *تفاصيل بند العمل*</span><span class="sxs-lookup"><span data-stu-id="bad64-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="bad64-114">فتح صفحة تفاصيل بند العمل واستخدامها</span><span class="sxs-lookup"><span data-stu-id="bad64-114">Open and use the Work line details page</span></span>

<span data-ttu-id="bad64-115">لعرض قائمة تفاصيل بند العمل، انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل بند العمل**.</span><span class="sxs-lookup"><span data-stu-id="bad64-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="bad64-116">من هنا، يمكنك تنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="bad64-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="bad64-117">استخدم حقل **عامل التصفية** للبحث عن البنود التي لها قيمة محددة لأي معلمة متوفرة.</span><span class="sxs-lookup"><span data-stu-id="bad64-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="bad64-118">(تتضمن المعلمات المتوفرة العديد من المعلمات غير المعروضة كأعمدة في الشبكة.)</span><span class="sxs-lookup"><span data-stu-id="bad64-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="bad64-119">استخدم خانة الاختيار **إظهار المغلق** لإظهار البنود المغلقة أو إخفائها.</span><span class="sxs-lookup"><span data-stu-id="bad64-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="bad64-120">حدد **أبعاد العرض** لفتح مربع الحوار **عرض الأبعاد**، حيث يمكنك اختيار إظهار أعمدة الأبعاد المختلفة أو إخفائها في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="bad64-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="bad64-121">حدد أي عنوان عمود لفتح قائمة حيث يمكنك اختيار فرز القائمة أو تصفيتها حسب القيم الموجودة في هذا العمود.</span><span class="sxs-lookup"><span data-stu-id="bad64-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="bad64-122">حدد بند عمل، ثم حدد **تغيير الموقع** لفتح مربع الحوار حيث يمكنك تغيير موقع بند العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="bad64-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="bad64-123">والموقع الذي تحدده سيتجاوز إعداد توجيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="bad64-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="bad64-124">حدد بند عمل، ثم حدد **إلغاء بند العمل** لفتح مربع الحوار حيث يمكنك تقليل كمية بند العمل بشكل جزئي أو كلي.</span><span class="sxs-lookup"><span data-stu-id="bad64-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="bad64-125">تعديل الكميات.</span><span class="sxs-lookup"><span data-stu-id="bad64-125">Adjust quantities.</span></span>
- <span data-ttu-id="bad64-126">عرض الحركات خلف أي بند من بنود العمل.</span><span class="sxs-lookup"><span data-stu-id="bad64-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="bad64-127">تجربه الميزة</span><span class="sxs-lookup"><span data-stu-id="bad64-127">Try out the feature</span></span>

<span data-ttu-id="bad64-128">يقدم هذا القسم توضيحًا من ثلاثة أجزاء يوضح كيفية العمل مع تفاصيل بند العمل.</span><span class="sxs-lookup"><span data-stu-id="bad64-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="bad64-129">جعل بيانات العينة متاحة</span><span class="sxs-lookup"><span data-stu-id="bad64-129">Make sample data available</span></span>

<span data-ttu-id="bad64-130">للعمل بهذا التوضيح باستخدام السجلات والقيم النموذجية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="bad64-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bad64-131">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="bad64-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="bad64-132">يمكنك أيضًا استخدام هذا العرض التوضيحي كإرشاد عند العمل في نظام إنتاج.</span><span class="sxs-lookup"><span data-stu-id="bad64-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="bad64-133">مع ذلك، يجب استبدال القيم الخاصة بك، وقد تفقد بعض أنواع السجلات المطلوبة التي توفرها بيانات العرض التوضيحي القياسية.</span><span class="sxs-lookup"><span data-stu-id="bad64-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="bad64-134">التحقق من أن إعداد السيناريو يشمل مخزون متوفر كاف</span><span class="sxs-lookup"><span data-stu-id="bad64-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="bad64-135">إذا كنت تتعامل مع البيانات التوضيحية **USMF**، فعليك أولاً التأكد من إعداد النظام لديك بحيث يكون هناك مخزون كاف في كل موقع انتقاء متعلق.</span><span class="sxs-lookup"><span data-stu-id="bad64-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="bad64-136">بالنسبة لهذا العرض التوضيحي، من المتوقع أن يكون لديك المخزون التالي متوفر:</span><span class="sxs-lookup"><span data-stu-id="bad64-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="bad64-137">**الصنف M9200:** 45 وحدة</span><span class="sxs-lookup"><span data-stu-id="bad64-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="bad64-138">(أو أكثر)</span><span class="sxs-lookup"><span data-stu-id="bad64-138">(or more)</span></span>
- <span data-ttu-id="bad64-139">**الصنف M9202:** 10 وحدة</span><span class="sxs-lookup"><span data-stu-id="bad64-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="bad64-140">(أو أكثر)</span><span class="sxs-lookup"><span data-stu-id="bad64-140">(or more)</span></span>

<span data-ttu-id="bad64-141">اتبع هذه الخطوات للتحقق من توفر المخزون الكافي وإجراء أية تسويات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bad64-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="bad64-142">انتقل إلى **إدارة المستودع \> الإعداد \> توجيهات الموقع**، وحدد مواقع الانتقاء التي يتم استخدامها لانتقاء أمر المبيعات في المستودع 51.</span><span class="sxs-lookup"><span data-stu-id="bad64-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="bad64-143">(لمزيد من المعلومات، راجع [مراقبة عمل المستودع باستخدام قوالب العمل والتوجيهات المتعلقة بالموقع](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="bad64-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="bad64-144">افحص مستويات المخزون في المواقع ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="bad64-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="bad64-145">قم بتسوية المخزون كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="bad64-145">Adjust inventory as required.</span></span> <span data-ttu-id="bad64-146">يمكنك إنشاء حركات يدوية أو استخدام تزويد أو تطبيق أي سير عمل آخر لتسوية المخزون.</span><span class="sxs-lookup"><span data-stu-id="bad64-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="bad64-147">الجزء 1: إنشاء عمل انتقاء</span><span class="sxs-lookup"><span data-stu-id="bad64-147">Part 1: Create picking work</span></span>

<span data-ttu-id="bad64-148">قبل البدء في إنشاء العمل، تأكد من إعداد المستودع الخاص بك للاستجابة لطلبات العمل بالطريقة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="bad64-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="bad64-149">اتبع هذه الخطوات لإنشاء بعض أعمال الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="bad64-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="bad64-150">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="bad64-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="bad64-151">حدد **جديد** لفتح مربع حوار **إنشاء أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="bad64-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="bad64-152">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="bad64-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bad64-153">في علامة التبويب السريعة **العميل**، قم بتعيين حقل **حساب العميل** إلى _US-001_.</span><span class="sxs-lookup"><span data-stu-id="bad64-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="bad64-154">من علامة التبويب السريعة **عام**، قم بتعيين الحقل **المستودع** إلى _51_.</span><span class="sxs-lookup"><span data-stu-id="bad64-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="bad64-155">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="bad64-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bad64-156">يتم فتح أمر المبيعات الجديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="bad64-156">Your new sales order is opened.</span></span> <span data-ttu-id="bad64-157">ويتضمن صفًا فارغًا جديدة في شبكة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="bad64-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="bad64-158">في بند الأمر هذا، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="bad64-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="bad64-159">**رقم الصنف:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="bad64-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="bad64-160">**الكمية:** _20_</span><span class="sxs-lookup"><span data-stu-id="bad64-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="bad64-161">**الوحدة:** _ea_</span><span class="sxs-lookup"><span data-stu-id="bad64-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="bad64-162">حدد بند الأمر الجديد، ثم، في قائمة **المخزون**، حدد **حجز** لفتح صفحة **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="bad64-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="bad64-163">في صفحة **الحجز**، حدد **حجز لوط** لحجز الكمية الكاملة للبند المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="bad64-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="bad64-164">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bad64-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="bad64-165">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="bad64-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="bad64-166">يقوم النظام بإنشاء شحنة، وإضافتها إلى حمل جديد، وإنشاء العمل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="bad64-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="bad64-167">قم بإنشاء أمر مبيعات ثان لنفس حساب العميل والمستودع الذي استخدمته للأمر الأول.</span><span class="sxs-lookup"><span data-stu-id="bad64-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="bad64-168">أضف بندي الأمر التاليين إلى هذا الأمر:</span><span class="sxs-lookup"><span data-stu-id="bad64-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="bad64-169">**البند 1:** قم بتعيين حقل **رقم الصنف** إلى _M9200_، وحقل **الكمية** إلى _25_، وحقل **الوحدة** إلى _لكل واحدة_.</span><span class="sxs-lookup"><span data-stu-id="bad64-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="bad64-170">**البند 2:** قم بتعيين حقل **رقم الصنف** إلى _M9202_، وحقل **الكمية** إلى _10_، وحقل **الوحدة** إلى _لكل واحدة_.</span><span class="sxs-lookup"><span data-stu-id="bad64-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="bad64-171">كرر الخطوات من 6 إلى 8 لحجز المخزون لكل بند من بنود الأوامر (واحد في المرة)، ثم كرر الخطوة 9 لإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="bad64-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="bad64-172">الجزء 2: تغيير موقع بند عمل</span><span class="sxs-lookup"><span data-stu-id="bad64-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="bad64-173">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل بند العمل**.</span><span class="sxs-lookup"><span data-stu-id="bad64-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="bad64-174">ابحث عن أحد بنود العمل التي قمت بإنشائها لهذا العرض التوضيحي وقم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="bad64-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="bad64-175">حدد **تغيير الموقع** لفتح مربع الحوار **تحديد موقع جديد**.</span><span class="sxs-lookup"><span data-stu-id="bad64-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="bad64-176">في مربع الحوار **تحديد موقع جديد**، في حقل **الموقع**، حدد موقعًا جديدًا لبند العمل.</span><span class="sxs-lookup"><span data-stu-id="bad64-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="bad64-177">حدد **موافق** لتطبيق تغييراتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="bad64-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bad64-178">يمكنك إرسال تغييرات الموقع فقط إذا كان الموقع الجديد يحتوي على مخزون كاف (للانتقاء)، أو إذا اجتاز التحقق من نوع الموقع (لعملية الوضع).</span><span class="sxs-lookup"><span data-stu-id="bad64-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="bad64-179">الجزء 3: تغيير كمية بند العمل أو إلغاء بند العمل</span><span class="sxs-lookup"><span data-stu-id="bad64-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="bad64-180">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل بند العمل**.</span><span class="sxs-lookup"><span data-stu-id="bad64-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="bad64-181">ابحث عن أحد بنود العمل التي قمت بإنشائها لهذا العرض التوضيحي وقم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="bad64-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="bad64-182">لاحظ أنه يمكنك إلغاء أو تغيير الكميات فقط لبنود العمل حينما يكون نوع العمل _انتقاء_.</span><span class="sxs-lookup"><span data-stu-id="bad64-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="bad64-183">حدد **إلغاء بند العمل** لفتح مربع الحوار **الكمية المطلوب إلغاؤها**.</span><span class="sxs-lookup"><span data-stu-id="bad64-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="bad64-184">في مربع الحوار **الكمية المطلوب إلغاؤها**، قم بتغيير القيمة في حقل **الكمية** لتحديد الكمية التي يجب *طرحها من* الكمية المحددة حاليًا للبند.</span><span class="sxs-lookup"><span data-stu-id="bad64-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="bad64-185">بشكل افتراضي، يعرض حقل **الكمية** الكمية الكاملة.</span><span class="sxs-lookup"><span data-stu-id="bad64-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="bad64-186">إذا قمت بإلغاء الكمية الكاملة، سيتم تغيير قيمة **حالة العمل** إلى _ملغي_، ولكن سيظل حقل **كمية العمل** يعرض القيمة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="bad64-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="bad64-187">إذا قمت بإلغاء جزء فقط من الكمية، سيتم تحديث حقل **كمية العمل** لإظهار القيمة الجديدة، ولكن ستظل قيمة **حالة العمل** بلا تغيير.</span><span class="sxs-lookup"><span data-stu-id="bad64-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="bad64-188">حدد **موافق** لتطبيق تغييراتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="bad64-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bad64-189">إذا قمت فقط بإلغاء جزء من الكمية لبند العمل، فيجب عليك أيضًا إزالة الكمية المهملة من بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="bad64-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="bad64-190">خلاف ذلك، ما لم يتم إعداد التسليم بالنقص بشكل صحيح، لا يمكن تأكيد الشحن لبند الحمل.</span><span class="sxs-lookup"><span data-stu-id="bad64-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]