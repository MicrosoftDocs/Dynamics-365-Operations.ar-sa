---
title: تعيين ابعاد مختلفه للتعبئة والتخزين
description: يوضح هذا الموضوع كيفيه تحديد العملية (التعبئة أو التخزين أو التعبئة المتداخلة) يتم استخدام كل بعد محدد لها.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e997f8bccde7856303d8b3c6407143598ccc6030
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818910"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="d50c3-103">تعيين ابعاد مختلفه للتعبئة والتخزين</span><span class="sxs-lookup"><span data-stu-id="d50c3-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d50c3-104">يتم تعبئة بعض الأصناف أو تخزينها بطريقه قد تحتاجها لتتبع الابعاد الفعلية بشكل مختلف لكل عمليه من العمليات المتعددة المختلفة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="d50c3-105">تتيح لك ميزه *ابعاد تعبئة المنتج* اعداد نوع واحد أو عده أنواع من الابعاد لكل منتج.</span><span class="sxs-lookup"><span data-stu-id="d50c3-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="d50c3-106">ويوفر كل نوع من أنواع الابعاد مجموعه من القياسات الفعلية (الوزن والعرض والعمق والارتفاع) ، كما يقوم بإنشاء العملية حيث يتم تطبيق قيم القياس الفعلية هذه.</span><span class="sxs-lookup"><span data-stu-id="d50c3-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="d50c3-107">عند تمكين هذه الميزة ، سيقوم النظام بدعم الأنواع التالية من الابعاد:</span><span class="sxs-lookup"><span data-stu-id="d50c3-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="d50c3-108">*التخزين* - يتم استخدام ابعاد تخزين التخزين مع مقاييس حجم الموقع لتحديد عدد الأصناف التي يمكن تخزينها في مواقع المستودعات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="d50c3-109">*التعبئة* - يتم استخدام ابعاد التعبئة اثناء التعبئة في الحاويات وعمليه التعبئة اليدوية لتحديد عدد الأصناف التي سيتم احتواؤها في أنواع مختلفه من الحاويات.</span><span class="sxs-lookup"><span data-stu-id="d50c3-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="d50c3-110">*التعبئة المتداخلة* - يتم استخدام ابعاد التعبئة المتداخلة عند احتواء عمليه التعبئة علي مستويات متعددة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="d50c3-111">يتم دعم ابعاد *التخزين* حتى عند عدم تمكين ميزه *تعبئة ابعاد المنتج*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="d50c3-112">قم باعداد هذه باستخدام صفحه **البعد الفعلي** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d50c3-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="d50c3-113">يتم استخدام هذه الابعاد بواسطة كافة العمليات التي لم يتم فيها تحديد التعبئة وابعاد التعبئة المتداخلة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="d50c3-114">يتم اعداد ابعاد *التعبئة* و *التعبئة المتداخلة* باستخدام الصفحة **ابعاد المنتج الفعلية**، والتي تتم اضافتها عند تمكين ميزه *تعبئة ابعاد المنتج*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="d50c3-115">يوفر هذا الموضوع سيناريو يوضح كيفيه استخدام هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="d50c3-116">تشغيل ميزه تعبئة ابعاد المنتج</span><span class="sxs-lookup"><span data-stu-id="d50c3-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="d50c3-117">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="d50c3-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d50c3-118">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d50c3-119">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="d50c3-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d50c3-120">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="d50c3-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d50c3-121">**اسم الميزة:** *تعبئة ابعاد المنتج*</span><span class="sxs-lookup"><span data-stu-id="d50c3-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d50c3-122">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="d50c3-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d50c3-123">إعداد السيناريو</span><span class="sxs-lookup"><span data-stu-id="d50c3-123">Set up the scenario</span></span>

<span data-ttu-id="d50c3-124">قبل ان تتمكن من تشغيل سيناريو المثال، يجب عليك تحضير النظام كما هو موضح في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="d50c3-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="d50c3-125">تمكين بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="d50c3-125">Enable demo data</span></span>

<span data-ttu-id="d50c3-126">للعمل بهذا السيناريو باستخدام السجلات والقيم التجريبية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="d50c3-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d50c3-127">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني *USMF* قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="d50c3-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="d50c3-128">أضافه بعد فعلي جديد إلى منتج</span><span class="sxs-lookup"><span data-stu-id="d50c3-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="d50c3-129">قم باضافه بعد فعلي جديد لأحد المنتجات بالقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="d50c3-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="d50c3-130">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d50c3-131">حدد المنتج مع **رقم الصنف** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="d50c3-132">في جزء الإجراءات، في علامة التبويب **إدارة المخزون**، من مجموعة **المستودعات**، حدد **أبعاد المنتج الفعلية**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="d50c3-133">عندئذ يتم فتح الصفحة **ابعاد المنتج الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="d50c3-134">في جزء الإجراء، حدد **جديد** لإضافة بعد جديد إلى الشبكة، ثم قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="d50c3-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="d50c3-135">**نوع البعد الفعلي** - *تعبئة*</span><span class="sxs-lookup"><span data-stu-id="d50c3-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="d50c3-136">**الوحدة الفعلية** - *أجهزه كمبيوتر*</span><span class="sxs-lookup"><span data-stu-id="d50c3-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="d50c3-137">**الوزن** - *4*</span><span class="sxs-lookup"><span data-stu-id="d50c3-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="d50c3-138">**وحدة الوزن** - *كجم*</span><span class="sxs-lookup"><span data-stu-id="d50c3-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="d50c3-139">**العمق** - *3*</span><span class="sxs-lookup"><span data-stu-id="d50c3-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="d50c3-140">**الارتفاع** - *4*</span><span class="sxs-lookup"><span data-stu-id="d50c3-140">**Height** - *4*</span></span>
    - <span data-ttu-id="d50c3-141">**العرض** - *3*</span><span class="sxs-lookup"><span data-stu-id="d50c3-141">**Width** - *3*</span></span>
    - <span data-ttu-id="d50c3-142">**الطول** - *سم*</span><span class="sxs-lookup"><span data-stu-id="d50c3-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="d50c3-143">**وحدة التخزين** - *سم3*</span><span class="sxs-lookup"><span data-stu-id="d50c3-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="d50c3-144">يتم حساب الحقل **حجم الصوت** تلقائيا استنادا إلى إعدادات **العمق** و **الارتفاع** و **العرض**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="d50c3-145">إنشاء نوع حاوية جديد</span><span class="sxs-lookup"><span data-stu-id="d50c3-145">Create a new container type</span></span>

<span data-ttu-id="d50c3-146">انتقل إلى **أداره مستودع \> إعداد \> حاويات \> أنواع حاويات** وقم بإنشاء سجل جديد بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="d50c3-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="d50c3-147">**كود نوع الحاوية** - *صندوق قصير‎*</span><span class="sxs-lookup"><span data-stu-id="d50c3-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="d50c3-148">**مربع الوصف** - *القصير*</span><span class="sxs-lookup"><span data-stu-id="d50c3-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="d50c3-149">**الحد الأقصى للوزن الصافي** - *50*</span><span class="sxs-lookup"><span data-stu-id="d50c3-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="d50c3-150">**الحجم** - *144*</span><span class="sxs-lookup"><span data-stu-id="d50c3-150">**Volume** - *144*</span></span>
- <span data-ttu-id="d50c3-151">**الطول** - *6*</span><span class="sxs-lookup"><span data-stu-id="d50c3-151">**Length** - *6*</span></span>
- <span data-ttu-id="d50c3-152">**العرض** - *6*</span><span class="sxs-lookup"><span data-stu-id="d50c3-152">**Width** - *6*</span></span>
- <span data-ttu-id="d50c3-153">**الارتفاع** - *4*</span><span class="sxs-lookup"><span data-stu-id="d50c3-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="d50c3-154">إنشاء مجموعة حاويات</span><span class="sxs-lookup"><span data-stu-id="d50c3-154">Create a container group</span></span>

<span data-ttu-id="d50c3-155">انتقل إلى **أداره مستودع \> إعداد \> حاويات \> مجموعات حاويات** وقم بإنشاء سجل جديد بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="d50c3-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="d50c3-156">**معرف مجموعه الحاويات** - *مربع قصير*</span><span class="sxs-lookup"><span data-stu-id="d50c3-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="d50c3-157">**مربع الوصف** - *القصير*</span><span class="sxs-lookup"><span data-stu-id="d50c3-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="d50c3-158">قم بإضافة بند جديد قسم **التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="d50c3-159">تعيين **نوع الحاوية** علي *صندوق قصير*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="d50c3-160">إعداد قالب إنشاء الحاوية</span><span class="sxs-lookup"><span data-stu-id="d50c3-160">Set up a container build template</span></span>

<span data-ttu-id="d50c3-161">انتقل إلى **إدارة المستودعات \> الإعداد \> الحاويات \> ‏‫قوالب إنشاء الحاوية**‬ وحدد **الصناديق**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="d50c3-162">قم بتغيير **معرف مجموعه الحاويات** إلى *صندوق قصير*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="d50c3-163">تشغيل السيناريو</span><span class="sxs-lookup"><span data-stu-id="d50c3-163">Run the scenario</span></span>

<span data-ttu-id="d50c3-164">بعد اعداد النظام كما هو موضح في المقطع السابق، ستكون جاهزا لتشغيل السيناريو كما هو موضح في المقطع التالي.</span><span class="sxs-lookup"><span data-stu-id="d50c3-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="d50c3-165">إنشاء أمر توريد وإنشاء شحنه</span><span class="sxs-lookup"><span data-stu-id="d50c3-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="d50c3-166">في هذه العملية، ستقوم بإنشاء شحنه استنادا إلى *ابعاد تعبئة الصنف* ، والتي يكون ارتفاعها اقل من 3.</span><span class="sxs-lookup"><span data-stu-id="d50c3-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="d50c3-167">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d50c3-168">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d50c3-169">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d50c3-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d50c3-170">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d50c3-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d50c3-171">**المستودع:** *63*</span><span class="sxs-lookup"><span data-stu-id="d50c3-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="d50c3-172">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="d50c3-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="d50c3-173">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="d50c3-173">The new sales order is opened.</span></span> <span data-ttu-id="d50c3-174">ويجب أن يتضمن بندًا فارغًا جديدًا في الشبكة في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d50c3-175">في هذا السطر، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d50c3-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="d50c3-176">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d50c3-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d50c3-177">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="d50c3-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="d50c3-178">على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="d50c3-179">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="d50c3-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="d50c3-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d50c3-180">Close the page.</span></span>
1. <span data-ttu-id="d50c3-181">في جزء الإجراءات، افتح علامة التبويب **المستودع**، وحدد **إصدار إلى المستودع‬** لإنشاء عمل للمستودع.</span><span class="sxs-lookup"><span data-stu-id="d50c3-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="d50c3-182">في علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المستودع \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="d50c3-183">في جزء الإجراءات، افتح علامة تبويب **المواصلات**، وحدد **عرض الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="d50c3-184">تاكد من ان العنصر تم تخزينه في حاوية داخل حاويات *الصندوق القصير*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="d50c3-185">وضع عنصر في المخزن</span><span class="sxs-lookup"><span data-stu-id="d50c3-185">Place an item into storage</span></span>

1. <span data-ttu-id="d50c3-186">افتح الجهاز المحمول، ثم قم بتسجيل الدخول إلى المستودع 63 وانتقل إلى **المخزون \> تعديل في**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="d50c3-187">ادخل **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="d50c3-188">إنشاء لوحه ترخيص جديده مع **العنصر** = *A0001* و **الكمية** = *أجهزه كمبيوتر*.</span><span class="sxs-lookup"><span data-stu-id="d50c3-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="d50c3-189">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d50c3-189">Select **OK**.</span></span> <span data-ttu-id="d50c3-190">وسوف تتلقي الخطا "الموقعSHORT-01 فشل نظرا لان الصنف A0001 لا يلائم الابعاد المحددة للموقع."</span><span class="sxs-lookup"><span data-stu-id="d50c3-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="d50c3-191">وهذا لان ابعاد نوع *التخزين* الخاصة بالمنتج أكبر من الابعاد المحددة في ملف تعريف الموقع.</span><span class="sxs-lookup"><span data-stu-id="d50c3-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]