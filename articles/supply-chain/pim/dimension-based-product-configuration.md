---
title: "تكوين المنتج المستند إلى بُعد"
description: "يمثل تكوين المنتج المستند إلى بُعد‬ حلاً بسيطًا لإنشاء متغيرات منتج متعددة من أصل منتج واحد وقائمة مكونات الصنف الخاصة به."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e2ce0e95a5e1230df970b5d5249fdb248113cf54
ms.openlocfilehash: b6895726af6028035830893fdbb01a4a407d7076
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="cc732-103">تكوين المنتج المستند إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="cc732-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cc732-104">يمثل تكوين المنتج المستند إلى بُعد‬ حلاً بسيطًا لإنشاء متغيرات منتج متعددة من أصل منتج واحد وقائمة مكونات الصنف الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="cc732-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="cc732-105">تكوين المنتج المستند إلى بُعد هو أحد ثلاث تقنيات مضمنة لتكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="cc732-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="cc732-106">والتقنيتان الآخريتان عبارة عن متغيرات محددة مسبقاً وتكوين مستند إلى قيد.</span><span class="sxs-lookup"><span data-stu-id="cc732-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="cc732-107">وتستخدم كل التقنيات الثلاثة أصل المنتج كنقطة انطلاق وتسمح للمستخدم بإنشاء العديد من متغيرات المنتج لأصل منتج واحد.</span><span class="sxs-lookup"><span data-stu-id="cc732-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="cc732-108">المفاهيم الأساسية</span><span class="sxs-lookup"><span data-stu-id="cc732-108">Key concepts</span></span>
<span data-ttu-id="cc732-109">يستند تكوين المنتج المستند إلى بُعد إلى المفاهيم الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="cc732-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="cc732-110">أصول المنتجات</span><span class="sxs-lookup"><span data-stu-id="cc732-110">Product masters</span></span>
-   <span data-ttu-id="cc732-111">بُعد منتج التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-111">Configuration product dimension</span></span>
-   <span data-ttu-id="cc732-112">مجموعات التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-112">Configuration groups</span></span>
-   <span data-ttu-id="cc732-113">قائمة مكونات الصنف (BOM)</span><span class="sxs-lookup"><span data-stu-id="cc732-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="cc732-114">مسار التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-114">Configuration route</span></span>
-   <span data-ttu-id="cc732-115">قواعد التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="cc732-116">أصول المنتجات</span><span class="sxs-lookup"><span data-stu-id="cc732-116">Product masters</span></span>

<span data-ttu-id="cc732-117">أصل المنتج هو نقطة البداية لأي عملية تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="cc732-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="cc732-118">وبالنسبة إلى تكوين المنتج المستند إلى بُعد، تحتاج إلى أصل منتج باستخدام تقنية التكوين المحددة هذه ومجموعة أبعاد منتج تتضمن بُعد منتج التكوين.</span><span class="sxs-lookup"><span data-stu-id="cc732-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="cc732-119">بُعد منتج التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-119">Configuration product dimension</span></span>

<span data-ttu-id="cc732-120">يتم استخدام بُعد منتج التكوين لتحديد متغيرات المنتج لأصل المنتج باستخدام تقنية التكوين المستندة إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="cc732-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="cc732-121">ويتم إدخال قيمة بُعد التكوين بواسطة المستخدم ويجب أن تساعد على تحديد متغيرات المنتجات الفردية.</span><span class="sxs-lookup"><span data-stu-id="cc732-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="cc732-122">مجموعات التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-122">Configuration groups</span></span>

<span data-ttu-id="cc732-123">يتم تحديد مجموعات التكوين في مستودع مركزي ويمكن استخدامها لكافة نماذج تكوين المنتجات المستندة إلى البُعد.</span><span class="sxs-lookup"><span data-stu-id="cc732-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="cc732-124">وترتبط مجموعات التكوين ببنود قائمة مكونات الصنف الفردية وتحتفظ معًا بمجموعة من البنود التي يتم تبادلها شكل حصري.</span><span class="sxs-lookup"><span data-stu-id="cc732-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="cc732-125">ويعني هذا أنه يمكن تحديد بند واحد فقط في مجموعة لمتغير منتج واحد.</span><span class="sxs-lookup"><span data-stu-id="cc732-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="cc732-126">قائمة مكونات الصنف (BOM)</span><span class="sxs-lookup"><span data-stu-id="cc732-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="cc732-127">تمثل قائمة مكونات الصنف اللبنات الأساسية لتكوين المنتج المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="cc732-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="cc732-128">ويجب أن تتضمن كافة المنتجات المختلفة التي يمكن استخدامها في أي متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="cc732-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="cc732-129">ويمكن أن يشير كل بند في قائمة مكونات الصنف إلى مجموعة تكوين.</span><span class="sxs-lookup"><span data-stu-id="cc732-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="cc732-130">وإذا لم يشير بند إلى مجموعة تكوين، فسيتم تضمينه في كافة متغيرات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cc732-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="cc732-131">مسار التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-131">Configuration route</span></span>

<span data-ttu-id="cc732-132">يحدد مسار التكوين تسلسل مجموعات التكوين، كما سيتم عرضها للمستخدم أثناء عملية تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="cc732-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="cc732-133">قواعد التكوين</span><span class="sxs-lookup"><span data-stu-id="cc732-133">Configuration rules</span></span>

<span data-ttu-id="cc732-134">تمثل قواعد تكوين آلية للتأكد من أن المنتج المضمن في مجموعة التكوين في قائمة مكونات الصنف تفرض إما تضمين أو استبعاد المنتج في مجموعة تكوين مختلفة في نفس قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="cc732-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="cc732-135">عملية تصميم المنتج</span><span class="sxs-lookup"><span data-stu-id="cc732-135">Product modeling process</span></span>
<span data-ttu-id="cc732-136">يبدأ التسلسل الطبيعي لبناء نموذج منتج لمنتج مستند إلى بُعد بتحديد مجموعات التكوين ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="cc732-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="cc732-137">من المهم ضمان إصدار كافة المنتجات التي سيتم استخدامها في قائمة مكونات الصنف إلى الشركة التي تم تصميم نموذج المنتج لها.</span><span class="sxs-lookup"><span data-stu-id="cc732-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="cc732-138">من خلال استخدام هذه اللبنات، يمكن للمستخدم إنشاء قائمة مكونات الصنف وتعيين مجموعات التكوين لكافة بنود قائمة مكونات الصنف ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="cc732-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="cc732-139">وعند اكتمال قائمة مكونات الصنف، يمكن تحديد مسار تكوين لترتيب مجموعات التكوين في الترتيب المناسب.‬</span><span class="sxs-lookup"><span data-stu-id="cc732-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="cc732-140">[![عملية تصميم المنتجات المستندة إلى بُعد](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) إذا كان هناك بعض المنتجات من مجموعات تكوين مختلفة يجب أو يجب ألا يتم استخدامها معًا، فيمكنك إنشاء قواعد التكوين التي ستفرض علاقات المنتج هذه.‬</span><span class="sxs-lookup"><span data-stu-id="cc732-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="cc732-141">وبعد ربط قائمة مكونات الصنف بأصل منتج مستند إلى بُعد من خلال إصدار قائمة مكونات الصنف واعتماد كليهما وتنشيطهما، يمكنك إنشاء تكوينات المنتج وإدخال اسم لكل تكوين.</span><span class="sxs-lookup"><span data-stu-id="cc732-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="cc732-142">يمكن تحديد التكوينات قبل أن يتم إنشاء أية حركات أو يمكن القيام بها عند الحاجة إلى تكوين معين.</span><span class="sxs-lookup"><span data-stu-id="cc732-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="cc732-143">الاستخدام المقترح</span><span class="sxs-lookup"><span data-stu-id="cc732-143">Suggested use</span></span>

<span data-ttu-id="cc732-144">يتم استخدام تقنية التكوين المستندة إلى بعد بشكل أفضل للمنتجات ذات التغير المحدود ومجموعة حجم ونمط ولون المنتج القياسي، ويكون التكوين غير صالح لتحديد متغير منتج معين.</span><span class="sxs-lookup"><span data-stu-id="cc732-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="cc732-145">يمكن أن يكون مثالاً على ذلك الدراجات مع ارتفاع الإطار وحجم العجلات وأنواع الفرامل والتروس المختلفة.</span><span class="sxs-lookup"><span data-stu-id="cc732-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="cc732-146">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="cc732-146">Next step</span></span> 

<span data-ttu-id="cc732-147">يتم سرد دلائل المهام الثمانية التالية بحسب الترتيب التي يجب عليك اتباعه لإكمالها.</span><span class="sxs-lookup"><span data-stu-id="cc732-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="cc732-148">إنشاء أصل منتج مستند إلى البعد (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="cc732-149">إصدار أصل منتج مستند إلى بعد (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="cc732-150">إكمال الإعداد الأساسي لأصل منتج تم إصداره (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="cc732-151">تحديد مجموعات التكوين (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="cc732-152">إنشاء قائمة مكونات الصنف لأصل منتج مستند إلى بعد (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="cc732-153">تحديد مسارات التكوين (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="cc732-154">إنشاء قواعد التكوين (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="cc732-155">إنشاء التكوينات المستندة إلى أبعاد (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="cc732-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)

