---
title: تجميع قوالب الموجات
description: يتيح تجميع قوالب الموجات للنظام استخدام إعدادات قالب الموجة لتحديد، استنادًا إلى المعايير التي تحددها، كيفية تقسيم البنود التي تم إصدارها وتعيينها إلى موجات جديدة أو موجودة. يمكن أن تكون هذه الميزة مفيدة في المستودعات حيث يتم إنشاء موجات استنادًا إلى معايير محددة، ولكن يفضل المديرون إنشاء موجات تلقائيًا بدلا من يدويًا.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 520338683443105ffd1df7fc2569cd95a5f50879
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245120"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="3357f-104">تجميع قوالب الموجات</span><span class="sxs-lookup"><span data-stu-id="3357f-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3357f-105">يتيح تجميع قوالب الموجات للنظام استخدام إعدادات [قالب الموجة](tasks/configure-wave-processing.md) لتحديد، استنادًا إلى المعايير التي تحددها، كيفية تقسيم البنود التي تم إصدارها وتعيينها إلى موجات جديدة أو موجودة.</span><span class="sxs-lookup"><span data-stu-id="3357f-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="3357f-106">يمكن أن تكون هذه الميزة مفيدة في المستودعات حيث يتم إنشاء موجات استنادًا إلى معايير محددة، ولكن يفضل المديرون إنشاء موجات تلقائيًا بدلا من يدويًا.</span><span class="sxs-lookup"><span data-stu-id="3357f-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="3357f-107">وهي تمكن النظام من إضافة كل شحنة تم إصدارها حديثًا إلى أول موجة يتم العثور عليها والتي تتضمن قيم حقل التجميع المطابقة.</span><span class="sxs-lookup"><span data-stu-id="3357f-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="3357f-108">في حالة عدم العثور على أي تطابق، يقوم النظام بإنشاء موجة جديد للشحنة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="3357f-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3357f-109">تجميع قالب الموجة غير مدعوم لأنواع عمل *انتقاء المادة الخام للإنتاج* أو *انتقاء كانبان*.</span><span class="sxs-lookup"><span data-stu-id="3357f-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="3357f-110">وهذا لأن تجميع الموجات يستند إلى الشحنات وأنواع العمل هذه لا تستخدم الشحنات.</span><span class="sxs-lookup"><span data-stu-id="3357f-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="3357f-111">تشغيل ميزة تجميع قوالب الموجات</span><span class="sxs-lookup"><span data-stu-id="3357f-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="3357f-112">قبل أن تتمكن من استخدام ميزة *تجميع قوالب الموجات*، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3357f-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="3357f-113">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3357f-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3357f-114">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3357f-115">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="3357f-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3357f-116">**اسم الموجة:** *تجميع قوالب الموجات*</span><span class="sxs-lookup"><span data-stu-id="3357f-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="3357f-117">تعيين قالب موجة لاستخدام تجميع قوالب الموجات</span><span class="sxs-lookup"><span data-stu-id="3357f-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="3357f-118">لجعل تجميع قوالب الموجات متاحا، اتبع الخطوات التالية لإعداد [قالب الموجة](tasks/configure-wave-processing.md) الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3357f-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="3357f-119">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="3357f-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="3357f-120">في الجزء الأيسر، حدد قالب الموجة المراد إعداده.</span><span class="sxs-lookup"><span data-stu-id="3357f-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="3357f-121">إذا كنت تقوم بالإعداد للعمل بالسيناريو لاحقًا في هذا الموضوع باستخدام البيانات التوضيحية، فحدد قالب **افتراضي الشحن 62**.</span><span class="sxs-lookup"><span data-stu-id="3357f-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="3357f-122">حدد **تحرير** لوضع الصفحة في وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="3357f-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="3357f-123">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3357f-124">**أتمتة إنشاء الموجة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="3357f-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="3357f-125">**التعيين إلى موجات مفتوحة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="3357f-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="3357f-126">**معالجة الموجة عند الإصدار إلى المستودع:** *لا*</span><span class="sxs-lookup"><span data-stu-id="3357f-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="3357f-127">في جزء الإجراءات، حدد **تحرير الاستعلام** لفتح مربع حوار الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="3357f-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="3357f-128">في مربع حوار استعلام، في علامة التبويب **فرز**، قم بمراجعة معايير الفرز، وتأكد من وجود قاعدة تتضمن الحقل الذي تريد استخدامه لتجميع موجاتك.</span><span class="sxs-lookup"><span data-stu-id="3357f-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="3357f-129">إذا كنت تقوم بالتجهيز للعمل في السيناريو باستخدام البيانات التوضيحية، قم بإضافة صف يحتوي على القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="3357f-130">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="3357f-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="3357f-131">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="3357f-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="3357f-132">**الحقل:** *خدمة شركة النقل*</span><span class="sxs-lookup"><span data-stu-id="3357f-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="3357f-133">بعد تحديد هذه القيمة، قد تتلقي الرسالة التالية: "خدمة شركة النقل الميدانية ليست حقل فهرس.</span><span class="sxs-lookup"><span data-stu-id="3357f-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="3357f-134">هل ترغب في إضافة فرز لها؟"</span><span class="sxs-lookup"><span data-stu-id="3357f-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="3357f-135">حدد **نعم** لإضافة الفرز.</span><span class="sxs-lookup"><span data-stu-id="3357f-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="3357f-136">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="3357f-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="3357f-137">حدد **موافق** لحفظ تغييراتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="3357f-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="3357f-138">في جزء الإجراءات، حدد **تجميع قوالب الموجات**.</span><span class="sxs-lookup"><span data-stu-id="3357f-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="3357f-139">في صفحة **تجميع قوالب الموجات**، حدد خانة الاختيار **تجميع حسب** لكل صف تريد استخدامه لتجميع بنود الأمر الخاص بك في موجات، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="3357f-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="3357f-140">إذا كنت تقوم بالتجهيز للعمل في السيناريو باستخدام البيانات التوضيحية، فحدد خانة الاختيار **تجميع حسب** لصف *خدمة النقل*.</span><span class="sxs-lookup"><span data-stu-id="3357f-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="3357f-141">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3357f-141">Select **Save**.</span></span>
1. <span data-ttu-id="3357f-142">أغلق صفحة **تجميع قوالب الموجات**.</span><span class="sxs-lookup"><span data-stu-id="3357f-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="3357f-143">حدد **حفظ** لحفظ القالب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3357f-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="3357f-144">سيناريو</span><span class="sxs-lookup"><span data-stu-id="3357f-144">Scenario</span></span>

<span data-ttu-id="3357f-145">يقدم هذا القسم برنامجًا نصيًا يمكنك العمل خلاله للتعرف على هذه الميزة وكيفية استخدامها.</span><span class="sxs-lookup"><span data-stu-id="3357f-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="3357f-146">جعل بيانات العينة متاحة</span><span class="sxs-lookup"><span data-stu-id="3357f-146">Make sample data available</span></span>

<span data-ttu-id="3357f-147">للعمل بهذا السيناريو باستخدام السجلات والقيم النموذجية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="3357f-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="3357f-148">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="3357f-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="3357f-149">يمكنك أيضًا استخدام هذا السيناريو كإرشاد لاستخدام الميزة عند العمل في نظام إنتاج.</span><span class="sxs-lookup"><span data-stu-id="3357f-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="3357f-150">مع ذلك، في هذه الحالة، يجب استبدال القيم الخاصة بك، وقد تفقد بعض أنواع السجلات المطلوبة التي توفرها بيانات العرض التوضيحي القياسية.</span><span class="sxs-lookup"><span data-stu-id="3357f-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="3357f-151">السيناريو: تجميع قوالب الموجات</span><span class="sxs-lookup"><span data-stu-id="3357f-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="3357f-152">يوضح هذا السيناريو كيفية استخدام تجميع قوالب الموجات لإنشاء موجات متعددة تلقائيًا استنادا إلى معايير التجميع التي تم تعريفها في قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="3357f-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="3357f-153">في هذا السيناريو ، يتم إعداد قالب الموجة في النظام لإنشاء موجة واحد لكل خدمة نقل.</span><span class="sxs-lookup"><span data-stu-id="3357f-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="3357f-154">قبل البدء، قم بتجهيز قالب الموجة كما هو موضح في قسم [تعيين قالب موجة لاستخدام تجميع قوالب الموجات](#set-up-template) المذكور سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="3357f-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="3357f-155">إذا كنت ستعمل باستخدام بيانات العرض التوضيحي لهذا السيناريو، فتأكد من استخدام قيم بيانات العرض التوضيحي المقترحة في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="3357f-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="3357f-156">سيقوم هذا الإعداد بتجميع موجاتك وفقًا لخدمة شركة النقل التي تم تعيينها لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="3357f-157">إنشاء أمر مبيعات 1</span><span class="sxs-lookup"><span data-stu-id="3357f-157">Create sales order 1</span></span>

1. <span data-ttu-id="3357f-158">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3357f-159">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3357f-160">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3357f-161">في علامة التبويب السريعة **العميل**، قم بتعيين حقل **حساب العميل** إلى *US-004*.</span><span class="sxs-lookup"><span data-stu-id="3357f-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="3357f-162">من علامة التبويب السريعة **عام**، قم بتعيين الحقل **المستودع** إلى *62*.</span><span class="sxs-lookup"><span data-stu-id="3357f-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="3357f-163">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار **إنشاء أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="3357f-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="3357f-164">يتم فتح أمر المبيعات الجديد في طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="3357f-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="3357f-165">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="3357f-166">قم بالتبديل إلى طريقة عرض **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="3357f-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3357f-167">في علامة التبويب السريعة **التسليم**، في قسم **النقل**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3357f-168">**شركة الشحن:** *Air cargo*</span><span class="sxs-lookup"><span data-stu-id="3357f-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="3357f-169">**خدمة شركة النقل:** *Air*</span><span class="sxs-lookup"><span data-stu-id="3357f-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="3357f-170">قم بالتبديل مرة أخرى إلى طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="3357f-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="3357f-171">في قسم **بنود أمر المبيعات**، انقر فوق **إضافة بند** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3357f-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="3357f-172">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3357f-173">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="3357f-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="3357f-174">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="3357f-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="3357f-175">حدد بند الأمر الجديد، ثم، في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="3357f-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3357f-176">في صفحة **الحجز**، في جزء الإجراءات، حدد **حجز لوط** لحجز الكمية الكاملة للبند المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="3357f-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3357f-177">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3357f-178">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3357f-179">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="3357f-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3357f-180">قم بتدوين رقم معرف الموجة وأرقام معرفات الشحنة.</span><span class="sxs-lookup"><span data-stu-id="3357f-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="3357f-181">عرض الموجة التي تم إنشاؤها من أمر المبيعات 1</span><span class="sxs-lookup"><span data-stu-id="3357f-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="3357f-182">انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3357f-183">حدد معرف الموجة التي تم إنشاؤها من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="3357f-184">حدد ارتباط معرف الموجة لفتح صفحة تفاصيل الموجة.</span><span class="sxs-lookup"><span data-stu-id="3357f-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="3357f-185">لاحظ أنه تمت إضافة الشحنة إلى علامة التبويب السريعة **بنود الموجة**.</span><span class="sxs-lookup"><span data-stu-id="3357f-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="3357f-186">إنشاء أمر مبيعات 2</span><span class="sxs-lookup"><span data-stu-id="3357f-186">Create sales order 2</span></span>

1. <span data-ttu-id="3357f-187">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3357f-188">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3357f-189">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3357f-190">في علامة التبويب السريعة **العميل**، قم بتعيين حقل **حساب العميل** إلى *US-005*.</span><span class="sxs-lookup"><span data-stu-id="3357f-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="3357f-191">من علامة التبويب السريعة **عام**، قم بتعيين الحقل **المستودع** إلى *62*.</span><span class="sxs-lookup"><span data-stu-id="3357f-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="3357f-192">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار **إنشاء أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="3357f-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="3357f-193">يتم فتح أمر المبيعات الجديد في طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="3357f-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="3357f-194">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="3357f-195">قم بالتبديل إلى طريقة عرض **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="3357f-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3357f-196">في علامة التبويب السريعة **التسليم**، في قسم **النقل**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3357f-197">**شركة الشحن:** *نقل الزهور*</span><span class="sxs-lookup"><span data-stu-id="3357f-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="3357f-198">**خدمة شركة النقل:** *قياسية*</span><span class="sxs-lookup"><span data-stu-id="3357f-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="3357f-199">قم بالتبديل مرة أخرى إلى طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="3357f-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="3357f-200">في قسم **بنود أمر المبيعات**، انقر فوق **إضافة بند** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3357f-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="3357f-201">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3357f-202">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3357f-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3357f-203">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="3357f-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="3357f-204">حدد بند الأمر الجديد، ثم، في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="3357f-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3357f-205">في صفحة **الحجز**، في جزء الإجراءات، حدد **حجز لوط** لحجز الكمية الكاملة للبند المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="3357f-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3357f-206">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3357f-207">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3357f-208">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="3357f-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3357f-209">قم بتدوين رقم معرف الموجة وأرقام معرفات الشحنة.</span><span class="sxs-lookup"><span data-stu-id="3357f-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="3357f-210">لاحظ أن معرف الموجة يختلف عن معرف الموجة الخاص بأمر المبيعات الأول.</span><span class="sxs-lookup"><span data-stu-id="3357f-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="3357f-211">عرض الموجة التي تم إنشاؤها من أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="3357f-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="3357f-212">انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3357f-213">حدد معرف الموجة التي تم إنشاؤها من أمر المبيعات الثاني.</span><span class="sxs-lookup"><span data-stu-id="3357f-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="3357f-214">حدد ارتباط معرف الموجة لفتح صفحة تفاصيل الموجة.</span><span class="sxs-lookup"><span data-stu-id="3357f-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="3357f-215">لاحظ أنه تمت إضافة الشحنة إلى علامة التبويب السريعة **بنود الموجة**.</span><span class="sxs-lookup"><span data-stu-id="3357f-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="3357f-216">تم إنشاء موجة جديدة لهذه الشحنة، نظرا لأنها تستخدم خدمة شركة نقل مختلفة عن أمر المبيعات الأول.</span><span class="sxs-lookup"><span data-stu-id="3357f-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="3357f-217">إنشاء أمر مبيعات 3</span><span class="sxs-lookup"><span data-stu-id="3357f-217">Create sales order 3</span></span>

1. <span data-ttu-id="3357f-218">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3357f-219">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3357f-220">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3357f-221">في علامة التبويب السريعة **العميل**، قم بتعيين حقل **حساب العميل** إلى *US-006*.</span><span class="sxs-lookup"><span data-stu-id="3357f-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="3357f-222">من علامة التبويب السريعة **عام**، قم بتعيين الحقل **المستودع** إلى *62*.</span><span class="sxs-lookup"><span data-stu-id="3357f-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="3357f-223">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار **إنشاء أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="3357f-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="3357f-224">يتم فتح أمر المبيعات الجديد في طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="3357f-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="3357f-225">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="3357f-226">قم بالتبديل إلى طريقة عرض **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="3357f-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3357f-227">في علامة التبويب السريعة **التسليم**، في قسم **النقل**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3357f-228">**شركه الشحن:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="3357f-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="3357f-229">**خدمة شركة النقل:** *Air*</span><span class="sxs-lookup"><span data-stu-id="3357f-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="3357f-230">قم بالتبديل مرة أخرى إلى طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="3357f-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="3357f-231">في قسم **بنود أمر المبيعات**، انقر فوق **إضافة بند** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3357f-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="3357f-232">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3357f-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3357f-233">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3357f-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3357f-234">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="3357f-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="3357f-235">حدد بند الأمر الجديد، ثم، في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="3357f-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3357f-236">في صفحة **الحجز**، في جزء الإجراءات، حدد **حجز لوط** لحجز الكمية الكاملة للبند المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="3357f-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3357f-237">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3357f-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3357f-238">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3357f-239">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="3357f-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3357f-240">قم بتدوين رقم معرف الموجة وأرقام معرفات الشحنة.</span><span class="sxs-lookup"><span data-stu-id="3357f-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="3357f-241">تم تعيين الشحنة للموجة الموجود من أمر المبيعات الأول.</span><span class="sxs-lookup"><span data-stu-id="3357f-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="3357f-242">عرض موجة لأوامر المبيعات 1 و3</span><span class="sxs-lookup"><span data-stu-id="3357f-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="3357f-243">انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.</span><span class="sxs-lookup"><span data-stu-id="3357f-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3357f-244">حدد معرف الموجة التي تم إنشاؤها من أمر المبيعات الثالث.</span><span class="sxs-lookup"><span data-stu-id="3357f-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="3357f-245">حدد ارتباط معرف الموجة لفتح صفحة تفاصيل الموجة.</span><span class="sxs-lookup"><span data-stu-id="3357f-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="3357f-246">لاحظ أنه تمت إضافة الشحنة إلى علامة التبويب السريعة **بنود الموجة**، مع الشحنة الخاصة بأمر المبيعات الأول.</span><span class="sxs-lookup"><span data-stu-id="3357f-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]