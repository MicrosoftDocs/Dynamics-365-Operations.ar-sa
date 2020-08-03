---
title: تغيير وعاء العمل في العمل
description: يشرح هذا الموضوع كيفية استخدام زر تغيير وعاء العمل لعناصر العمل لتغيير وعاء العمل الخاص بالعمل الموجود.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33238b114f0939711163b19ae7af98be7c8d0744
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597522"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="ceba7-103">تغيير وعاء العمل في العمل</span><span class="sxs-lookup"><span data-stu-id="ceba7-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceba7-104">يمكنك استخدام أوعية العمل لتنظيم العمل في مجموعات.</span><span class="sxs-lookup"><span data-stu-id="ceba7-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="ceba7-105">على سبيل المثال، يمكنك إنشاء وعاء عمل لتصنيف العمل الذي يحدث في موقع مستودع محدد.</span><span class="sxs-lookup"><span data-stu-id="ceba7-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="ceba7-106">تقوم ميزة *تغيير وعاء العمل الموجود علي العمل* بإضافة زر **تغيير وعاء العمل** إلى جزء الإجراءات الخاص بعناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="ceba7-107">التالي، يمكن لمديري المستودع تغيير وعاء العمل الخاص بالعمل الموجود بسهولة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="ceba7-108">تتيح هذه الميزة للمديرين التفاعل بسرعة مع التغييرات في حالة العمل الخاصة بالمستودع، كما أنه يساعد في تحسين قدرتهم علي التعامل مع المواقف والحاجة إلى تحويل الأعمال إلى وعاء عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="ceba7-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="ceba7-109">تشغيل ميزة تغيير وعاء العمل علي العمل</span><span class="sxs-lookup"><span data-stu-id="ceba7-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="ceba7-110">قبل البدء في إعداد هذه الميزة أو استخدامها، يجب التأكد من أنها متوفرة في نظامك.</span><span class="sxs-lookup"><span data-stu-id="ceba7-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="ceba7-111">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ceba7-112">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="ceba7-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ceba7-113">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="ceba7-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ceba7-114">**اسم الميزة:** *تغيير وعاء العمل علي العمل*</span><span class="sxs-lookup"><span data-stu-id="ceba7-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="ceba7-115">إعداد ميزة تغيير وعاء العمل علي العمل</span><span class="sxs-lookup"><span data-stu-id="ceba7-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="ceba7-116">لاستخدام هذه الميزة، يجب إعداد بعض أوعية العمل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="ceba7-117">يمكنك أيضا إعداد قوالب العمل لكي تقوم بتعيين الوعاء تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="ceba7-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="ceba7-118">إذا كنت ترغب في العمل من خلال سيناريو النموذج الذي تم توفيره لاحقًا في هذا الموضوع، فقم بإعداد النظام كما هو موضح في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="ceba7-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="ceba7-119">إعداد أوعية العمل</span><span class="sxs-lookup"><span data-stu-id="ceba7-119">Set up work pools</span></span>

<span data-ttu-id="ceba7-120">تسمح لك أوعية العمل بتنظيم عناصر العمل حسب النوع.</span><span class="sxs-lookup"><span data-stu-id="ceba7-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="ceba7-121">للعمل مع ميزة *تغيير وعاء العمل علي العمل*، يجب أن يتوفر لديك اثنين من أوعية العمل علي الأقل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="ceba7-122">لعرض وإضافة أوعية العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ceba7-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="ceba7-123">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> أوعية العمل**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="ceba7-124">إذا كنت تعمل باستخدام بيانات تجريبية من شركة **USMF** ستعمل من خلال سيناريو المثال لاحقا في هذا الموضوع، قم بإضافة اثنين من تجمعات العمل التي لها الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="ceba7-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="ceba7-125">وعاء العمل 1:</span><span class="sxs-lookup"><span data-stu-id="ceba7-125">Work pool 1:</span></span>

        - <span data-ttu-id="ceba7-126">**معرف وعاء العمل:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="ceba7-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="ceba7-127">**الوصف:** *متجر ويب*</span><span class="sxs-lookup"><span data-stu-id="ceba7-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="ceba7-128">وعاء العمل 2:</span><span class="sxs-lookup"><span data-stu-id="ceba7-128">Work pool 2:</span></span>

        - <span data-ttu-id="ceba7-129">**معرف وعاء العمل:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="ceba7-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="ceba7-130">**الوصف:** *مركز اتصالات*</span><span class="sxs-lookup"><span data-stu-id="ceba7-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="ceba7-131">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="ceba7-132">إعداد قوالب العمل</span><span class="sxs-lookup"><span data-stu-id="ceba7-132">Set up work templates</span></span>

<span data-ttu-id="ceba7-133">بالنسبة لكل من قوالب العمل الخاصة بك، يمكنك تعيين وعاء عمل افتراضي، كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ceba7-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="ceba7-134">لكل قالب مناسب، يمكنك تعيين وعاء عمل في العمود **معرف وعاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="ceba7-135">في هذه الحالة، ترث كافة عناصر العمل التي يتم إنشاؤها باستخدام قالب معين وعاء العمل المعين تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="ceba7-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="ceba7-136">إذا كنت تعمل باستخدام بيانات تجريبية من شركة **USMF** ستعمل من خلال سيناريو المثال لاحقا في هذا الموضوع، فاتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ceba7-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="ceba7-137">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ceba7-138">في جزء الإجراءات، حدد **تحرير** لوضع الصفحة في وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="ceba7-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="ceba7-139">يمكنك تحرير القالب عن طريق اعداد القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ceba7-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="ceba7-140">**قالب العمل:** *62 انتقاء إلى الحزم*</span><span class="sxs-lookup"><span data-stu-id="ceba7-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="ceba7-141">**معرف وعاء العمل:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="ceba7-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="ceba7-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ceba7-143">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="ceba7-143">Example scenario</span></span>

<span data-ttu-id="ceba7-144">يوضح هذا السيناريو كيفية تغيير دفق معالجة لعنصر عمل موجود عن طريق تغيير وعاء العمل الخاص به.</span><span class="sxs-lookup"><span data-stu-id="ceba7-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="ceba7-145">ويستخدم البيانات التوضيحية من شركة **USMF**والإعدادات التي تم اقتراحها مسبقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="ceba7-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="ceba7-146">إنشاء أمر مبيعات وإصداره للمستودع</span><span class="sxs-lookup"><span data-stu-id="ceba7-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="ceba7-147">قم بالتأكيد علي وجود مخزون فعلي كافٍ للأصناف *A0001*و*A0002* في المستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="ceba7-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="ceba7-148">انتقل إلى **إدارة المخزون \>الاستعلامات والتقارير \>القائمة الفعلية**، وقم بتحرير عوامل التصفية كما هو موضح هنا:</span><span class="sxs-lookup"><span data-stu-id="ceba7-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="ceba7-149">تبدأ قيمة **Warehouse** بـ *62*.</span><span class="sxs-lookup"><span data-stu-id="ceba7-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="ceba7-150">**قيمة رقم الصنف** إما *A001* أو *A002*.</span><span class="sxs-lookup"><span data-stu-id="ceba7-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="ceba7-151">يجب أن يكون لبيانات العرض التوضيحي كمية قيمتها 10.</span><span class="sxs-lookup"><span data-stu-id="ceba7-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="ceba7-152">بعد ذلك، يجب إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ceba7-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="ceba7-153">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ceba7-154">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ceba7-155">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ceba7-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ceba7-156">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="ceba7-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="ceba7-157">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="ceba7-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="ceba7-158">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ceba7-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ceba7-159">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="ceba7-159">The new sales order is opened.</span></span> <span data-ttu-id="ceba7-160">ويجب أن يتضمن بندًا فارغًا جديدًا في الشبكة في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ceba7-161">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ceba7-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="ceba7-162">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ceba7-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ceba7-163">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="ceba7-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="ceba7-164">في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="ceba7-165">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="ceba7-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="ceba7-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-166">Close the page.</span></span>
1. <span data-ttu-id="ceba7-167">في علامة التبويب السريعة **بنود أمر المبيعات**، حدد **إضافة بند** لإضافة بند آخر إلى أمر المبيعات الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ceba7-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="ceba7-168">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ceba7-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="ceba7-169">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ceba7-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="ceba7-170">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="ceba7-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="ceba7-171">في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="ceba7-172">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="ceba7-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="ceba7-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-173">Close the page.</span></span>
1. <span data-ttu-id="ceba7-174">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="ceba7-175">سوف تستلم رسائل معلوماتية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها من الإصدار.</span><span class="sxs-lookup"><span data-stu-id="ceba7-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="ceba7-176">قم بتدوين ملاحظة بمُعرف الموجة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="ceba7-177">مراجعه الموجة الصادرة</span><span class="sxs-lookup"><span data-stu-id="ceba7-177">Review the outbound wave</span></span>

1. <span data-ttu-id="ceba7-178">انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="ceba7-179">في الشبكة، ابحث عن معرف الموجة الذي تم إنشاؤه من إصدار أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ceba7-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="ceba7-180">حدد معرف الموجة لعرض التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="ceba7-181">في علامة التبويب السريعة **بنود الموجة**، تأكد من إظهار معرف الشحنة لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ceba7-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="ceba7-182">إذا كان الخيار **معالجة الموجة عند الإصدار إلى المستودع**معينا إلى *لا* في الإعداد الخاص بقالب موجة الشحن، فيجب عليك معالجة الموجة يدويا عن طريق تحديد **معالجة**من علامة التبويب **موجة** في جزء الإجراءات لإنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="ceba7-183">تأكد من أنه تمت معالجة الموجة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="ceba7-184">وتقوم هذه المعالجة بإنشاء العمل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="ceba7-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="ceba7-185">عرض تفاصيل العمل وتغيير وعاء العمل</span><span class="sxs-lookup"><span data-stu-id="ceba7-185">View work details and change the work pool</span></span>

<span data-ttu-id="ceba7-186">يمكنك استخدام الصفحة **تفاصيل العمل** لعرض العمل الذي تم إنشاؤه وإداره وعاء العمل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="ceba7-187">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ceba7-188">حدد صف العمل الذي تم إنشاؤه الآن.</span><span class="sxs-lookup"><span data-stu-id="ceba7-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="ceba7-189">سيعرض عمود **رقم الأمر** رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ceba7-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="ceba7-190">سيتم تعيين حقل **معرف وعاء العمل** إلى معرف وعاء العمل الذي تم إعداده في قالب العمل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="ceba7-191">إذا لم تشاهد الحقل **معرف وعاء العمل**، فقم بإضافة العمود إلى الشبكة، ثم قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ceba7-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="ceba7-192">لتغيير وعاء العمل المرتبط بمعرف العمل، في جزء الاجراءات، ضمن علامة التبويب **العمل**، حدد **تغيير معرف وعاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="ceba7-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="ceba7-193">في مربع الحوار **تغيير تجمع العمل**، علي علامة التبويب السريعة **المعلمات**، في الحقل **معرف تجمع العمل**، حدد *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="ceba7-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="ceba7-194">حدد **موافق** لتطبيق التغيير الذي قمت به.</span><span class="sxs-lookup"><span data-stu-id="ceba7-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="ceba7-195">لاحظ انه تم الآن تغيير قيمه حقل **معرف تجمع العمل** إلى *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="ceba7-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ceba7-196">عند ظهور مربع الحوار **تغيير وعاء العمل**، قد يكون الحقل **معرف وعاء العمل** فارغا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="ceba7-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="ceba7-197">إذا كان الحقل فارغا عندما تقوم بتحديد **موافق** لتطبيق التغييرات، فإنك ستقوم بازالة وعاء العمل بالكامل من العمل.</span><span class="sxs-lookup"><span data-stu-id="ceba7-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="ceba7-198">بالإضافة إلى تبديل أوعية العمل، يمكنك استخدام هذا الإجراء لإضافة وعاء عمل إلى أي عنصر عمل لا يحتوي علي واحد، أو لإزالة وعاء عمل من أي عنصر عمل يحتوي علي واحد.</span><span class="sxs-lookup"><span data-stu-id="ceba7-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
